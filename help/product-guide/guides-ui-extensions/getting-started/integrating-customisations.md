---
title: Installatie en installatie
description: AEM Guides Extension Package installeren en gebruiken
role: User, Admin
exl-id: 0304c8d0-35a8-4712-a9af-36557e3b247f
source-git-commit: b4d6c1c8c2d413bb4137e58391554abf2fb68b8c
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---

# AEM Guides Extension Package installeren en gebruiken

Met extensies kunt u uw AEM Guides-app aanpassen aan uw wensen. Dit extensieframework wordt ondersteund in AEM Guides v4.3 en hoger (on-prem) en 2310 (cloud).

## Vereisten

Dit pakket vereist [ git bash ](https://github.com/git-guides/install-git) en npm

## Installatie

De eenvoudigste manier om AEM Guides Framework-installatie te starten, is via cli

```bash
npx @adobe/create-guides-extension
```

## Aanpassingscode toevoegen

1. Voeg codebestanden toe voor elke component die u wilt uitbreiden in de map `src/` . Sommige voorbeeldbestanden zijn al voor u toegevoegd.
2. Nu in het bestand `index.ts` in de map `src/` :
   - Importeer de `.ts` -bestanden met de aanpassingen die u in de build wilt toevoegen.
   - De importbewerkingen toevoegen aan `window.extension`
   - De aangepaste component `id` en de corresponderende import registreren in `tcx extensions`
   - Zie het voorbeeld `/src/index.ts`

## De aangepaste code maken

- Voer `npm run build` uit in de hoofdmap. Er worden 3 bestanden opgehaald in de map, `dist/` :
   - `build.css`
   - `guides-extension.js`
   - `guides-extension.umd.cjs`

![ bouwt Output ](./../imgs/build_output.png)

## De aanpassing toevoegen aan AEM

- Ga naar `CRXDE` `crx/de/index.jsp#/`
- Maak onder de map `apps` een nieuw knooppunt van het type `cq:ClientLibraryFolder`

![ de structuur van de Omslag ](./../imgs/crxde_folder_structure.png)

- Selecteer in de `properties` van het knooppunt `Multi` de volgende eigenschap toevoegen
Naam: `categories`
Type: `String []`
Waarde: `apps.fmdita.review_overrides`, `apps.fmdita.xml_editor.page_overrides`

>[!NOTE]
>
> Voor de op één na laatste gebruikersinterface zijn de waarden: `apps.fmdita.penultimate.xml_editor.page_overrides` en `apps.fmdita.review_overrides`


![ Eigenschappen van de Omslag ](./../imgs/crxde_folder_properties.png)

- Als u de gebouwde JS wilt toevoegen, maakt u bijvoorbeeld een nieuw bestand `tcx1.js` in het hierboven gemaakte knooppunt. Voeg hier de code uit `dist/guides-extension.umd.cjs` of `dist/guides-extension.js` toe. Maak nu een nieuw bestand `js.txt` en voeg hier de naam van ons JS-bestand toe. In dit geval is dit:

```t
#base=.
tcx1.js
```

- Als u de ingebouwde css wilt toevoegen, maakt u bijvoorbeeld een nieuw bestand `tcx1.css` in het hierboven gemaakte knooppunt. Voeg hier de code uit `dist/build.css` toe. Maak nu een nieuw bestand `css.txt` en voeg hier de naam van ons CSS-bestand toe. In dit geval is dit:

```t
#base=.
tcx1.css
```

- Voer een `shift + refresh` uit om de app te laden met de aanpassingen!

## Problemen oplossen

Controleer of alle bovenstaande stappen correct zijn uitgevoerd.
Nadat u de code aan tcx.js hebt toegevoegd, moet u de code hard vernieuwen (shift+refresh).
Open nu AEM, klik met de rechtermuisknop en klik op `Inspect`
Ga naar Bronnen en zoek naar het bestand `[node_name].js` (bijvoorbeeld extensions.js). Voer een Besturing / Cmd + D uit om naar het bestand te zoeken. Als het `.js` -bestand bestaat met de JS-code die u van `dist/guides-extension.umd.cjs` of `dist/guides-extension.js` hebt geplakt, is de installatie voltooid
