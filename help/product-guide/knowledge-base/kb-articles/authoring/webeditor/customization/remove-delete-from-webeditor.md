---
title: De optie Verwijderen verwijderen uit het contextmenu van het bestand in de webbrowser voor specifieke gebruikers
description: Leer hoe u de webbrowser kunt aanpassen door de optie Verwijderen te verwijderen uit het contextmenu van het bestand voor specifieke gebruikers/groepen
source-git-commit: aacc04e2fb6ca061825e5e219ad6e03bf711b3d0
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---


# De optie Verwijderen verwijderen uit het contextmenu van het bestand in de webbrowser

In dit artikel leert u hoe u de optie Verwijderen in het contextmenu voor bestanden in AEM de webeditor voor hulplijnen verbergt voor specifieke gebruikers of groepen. Voor andere aanpassingen in de menuopties van de dossiercontext, gelieve het kader van de Uitbreiding van Gidsen te controleren. Meer details zijn te vinden [hier](https://github.com/adobe/guides-extension/tree/main).

Zoals u onder het fragment kunt zien, is de optie Verwijderen beschikbaar voor deze specifieke gebruiker.

![Contextmenu Bestand met verwijderen](../../../assets/authoring/file-contextmenu-Delete.png)

Laten we nu bekijken hoe we de optie Verwijderen kunnen verbergen voor deze gebruiker.

## Implementatiestappen:

- Navigeer naar Gereedschappen > Beveiliging > Rechten van AEM startpagina.
- Kies de groep of de gebruiker in het zoekvak.
- Klik op ACE toevoegen in de rechterbovenhoek.
- Kies het mappad.
- Inclusief rechten &quot;jcr:removeChildNodes&quot; en &quot;jcr:removeNode&quot;.
- Kies Machtigingstype als &#39;weigeren&#39; en klik op Toevoegen zoals hieronder wordt weergegeven.

![Gebruikersmachtiging weigert ACE](../../../assets/authoring/permission-ACE-Delete.png)

![Toegangsbeheerlijst in machtigingen](../../../assets/authoring/delete-acl.png)

### Testen

- Login aan AEM als gebruiker waarvoor ACE is toegevoegd.
- Webeditor openen.
- Ga naar de dataweergave en kies de map waarvoor de ACE&#39;s zijn toegevoegd.
- Open het contextmenu voor bestanden.
- De optie Verwijderen wordt niet weergegeven in het contextmenu.

Het contextmenu voor bestanden ziet er nu als volgt uit:

![Contextmenu Bestand zonder verwijderen](../../../assets/authoring/file-contextmenu-Delete-removed.png)

```
Please note that these steps would also remove 'move' and 'rename' options from the Web Editor as they are also tied to delete process at the backend.
```
