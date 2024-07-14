---
title: Opmerkingen bij de release | Upgradeinstructies en opgeloste problemen in Adobe Experience Manager Guides 4.3.0-versie
description: Meer informatie over de opgeloste problemen en over het upgraden naar 4.3.0-releases van Adobe Experience Manager Guides
exl-id: 7fb568a0-0b88-4ea0-9b79-2625336348ff
feature: Release Notes
role: Leader
source-git-commit: 5a444e88b0adba7fa3d498437df39b729b10b5eb
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 0%

---

# 4.3.0 release van Adobe Experience Manager Guides (juli 2023)

Deze versienota behandelt de verbeteringsinstructies, verenigbaarheidsmatrijs, en kwesties die in versie 4.3.0 van Adobe Experience Manager Guides (later als *worden bedoeld AEM Guides*) worden bevestigd.

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, zie [ wat in versie 4.3.0 van Adobe Experience Manager Guides ](./whats-new-4-3-release.md) nieuw is.

## Upgrade naar versie 4.3.0 van AEM Guides


U kunt uw huidige versie van AEM Guides eenvoudig upgraden naar versie 4.3.0. Voordat u verdergaat met de upgrade naar versie 4.3.0 van AEM Guides, moet u rekening houden met de volgende punten:
U kunt uw huidige versie van AEM Guides upgraden naar versie 4.3.0

- Als u versie 4.2 of 4.2.x gebruikt, kunt u rechtstreeks upgraden naar versie 4.3.0.
- Als u versie 4.1 of 4.1.x gebruikt, moet u een upgrade naar versie 4.2 of 4.2.x uitvoeren voordat u een upgrade naar versie 4.3.0 uitvoert.
- Als u versie 4.0 gebruikt, moet u een upgrade naar versie 4.2 uitvoeren voordat u een upgrade naar versie 4.3.0 uitvoert.
- Als u versie 3.8.5 gebruikt, moet u een upgrade naar versie 4.0 uitvoeren voordat u een upgrade naar versie 4.2 uitvoert.
- Raadpleeg de sectie Upgrade AEM Guides in de productspecifieke installatiehandleiding als u werkt met een versie die ouder is dan 3.8.5.



>[!NOTE]
>
>U moet AEM servicepack installeren voordat u de AEM Guides-versie kunt upgraden.

Voor details, zie [ instructies van de Verbetering ](../install-guide/upgrade-xml-documentation.md).

## Compatibiliteitsmatrix

In deze sectie wordt een overzicht gegeven van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door de release van AEM Guides 4.3.0.

### Adobe Experience Manager

**4.3.0 niet-UUID**
Versie 6.5 Service Pack 18, 17, 16, 15 of 14

**4.3.0 UUID**
Versie 6.5 Service Pack 18, 17, 16, 15 of 14

Voor meer details, zie de *Technische vereisten* sectie in installeer en vorm de gids van Adobe Experience Manager Guides.

### FrameMaker en FrameMaker Publishing Server

| Geen | FMPS 2022 | FMPS 2020 | Fm 2022 | Fm 2020 |
| --- | --- | --- | --- | --- |
| 4.3.0 (niet-UUID) | 2022 of hoger | 2020.2 of hoger* | 2022 of hoger | 2020.3 of hoger |
| 4.3.0 (UUID) | 2022 of hoger | 2020.2 of hoger* | 2022 of hoger | 2020.4 of hoger |
| | | | |

*Basislijn en voorwaarden die in AEM zijn gemaakt, worden vanaf 2020.2 ondersteund in FMPS-releases.

### Zuurstofaansluiting

| Geen | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- |--- |--- |
| 4.3.0 (niet-UUID) | 2.3-regelmatig-5 | 2.3-regelmatig-5 | 1,6 | 1,6 |
| 4.3.0 (UUID) | 3.0-uuid-4 | 3.0-uuid-3 | 2,3 | 2,3 |
|  |  |   |

## Opgeloste problemen

De fouten die in verschillende gebieden zijn gecorrigeerd, worden hieronder weergegeven:

### Authoring

- Het onderwerpdossier wordt niet ontgrendeld in de Redacteur van het Web, hoewel de Ontgrendel de optie van het Dossier en niet sparen optie worden geselecteerd. (1258)
- Kan een bestand niet uitchecken in de webeditor, ondanks dat u de optie NO hebt gekozen om de wijzigingen vóór het inchecken te verwijderen. (1257)
- De knopinfo voor de pictogrammen voor vergrendelen en ontgrendelen van bestanden op de hoofdwerkbalk in de webeditor is niet consistent met de pictogrammen die worden weergegeven in de weergave Opslagplaats.(12555)
- De optie Uitchecken annuleren en Ontgrendelen wordt weergegeven voor een bestand in de webeditor dat nog niet is uitgecheckt in de Kaartweergave. (12556)
- Kan de PDF-elementen niet selecteren in de bestaande &quot;topicref&quot;-koppelingen. (12477).
- Bij het samenvoegen en splitsen in de tabellen genereert AEM Guides 4.2 extra tabelcellen. (11793)
- In de weergave Opslagplaats kunnen de onderwerpen of afbeeldingen na gebruik van de functie Zoeken/Filteren niet meer worden gesleept. 12396
- De zoekresultaten worden uitgeschakeld in het deelvenster Zoeken en vervangen nadat een doorzocht bestand is geopend. 12142
- De cijfertoets &quot;8&quot; op het zijtoetsenbord werkt niet in de AEM Guides-editor. 12106
- De inline-/weergavekenmerken worden niet weergegeven in de layoutweergave van de webeditor. 12498
- De configuratie van de globale profiel-UI komt niet overeen met het mapprofiel. (1970)
- Inhoudsverwijzingen worden verbroken wanneer DITA-bestanden worden gekopieerd en geplakt. (1959)
- Kan inhoudsfragment niet bewerken in de kolomweergave als AEM Guides is geïnstalleerd. 7342
- Inhoud gaat verloren wanneer een onverpakt xref zich onder subelementtags bevindt. 12532
- De goedkeuringswerkstroom werkt niet wanneer de documentstatus wordt gewijzigd in &quot;eindstatus&quot; in de bestandseigenschappen van het rechterdeelvenster. (1026)
- Elementinterface | In de lijstweergave kunnen de overschreven beschikbare kolommen niet worden samengevoegd. 11528
- Keyref wordt niet opgelost in de kaartweergave. (11490)
- Het bovenste menu wordt niet weergegeven wanneer u door de XML-editor navigeert. 10868
- `conref` in tag ph | Het weergegeven dialoogvenster Bladeren is onjuist. 9481
- Lokale koppelingen naar andere elementen worden niet opgelost in de webeditor. 8790
- De functie Matches() werkt niet in de functie schema. (11224)



### Beheer

- Het veld &quot;title&quot; in de metagegevenseigenschappen van de DITA-kaart wordt overschreven door het element `<title>` voor de kaart. 10702
- Wanneer u probeert de versie van onderwerpen in de basislijn te openen of bij te werken, wordt de lader &quot;Fetching information from the server&quot; voor onbepaalde tijd uitgevoerd.12478


### Controleren

- Nieuwe revisie-interface | De voorwaarden benadrukken, en tonen verberg werk anders dan hoe zij in de Redacteur van het Web werken. (11628)

### Publiceren

- Publiceren mislukt bij het wijzigen van de naam van een Native PDF-voorinstelling. 12564
- Als u een Native PDF-sjabloon dupliceert, wordt de standaardsjabloonlocatie gebruikt in plaats van de beschikbare aangepaste sjabloonlocatie. 12563
- Native PDF | De taalmeta-gegevens kunnen niet in geproduceerde PDF worden geplaatst om aan WCAG 2.0 te voldoen. 12407
- Publiceren naar AEM site mislukt bij het lezen van tijdelijke bestanden uit pod die mogelijk zijn vernieuwd of opnieuw zijn gestart. (1213)
- Native PDF | Aangepaste kenmerken worden niet doorgegeven aan de HTML- of PDF-engine. (DXML-12005)
- Native PDF |  Java OutOfMemoryError treedt op bij het publiceren van grote inhoud. (11789)
- Native PDF | Xref drukt de inhoud van href onderwerptitel in plaats van het etiket Xref. (11322)
- Native PDF | Kan de sjablooninstellingen voor PDF niet opslaan. 10751
- Native PDF | De tekst breidt zich voorbij de kolombreedte uit bij het opnemen van meerdere Xrefs. 10876
- Native PDF | `<note>``</note>` -element genereert geen extra bereiktitel van het type. 10549
- JSON-uitvoer | De eigenschap `fmUuid` op het knooppunt jcr:content van JSON verschilt van de eigenschap &quot;id&quot; in de JSON. 11564
- JSON-uitvoer | Als de kaart en het onderwerp met zelfde filename aanwezig zijn, wordt JSON voor de kaart verwijderd. 11524

## Bekend probleem

Adobe heeft het volgende bekende probleem voor AEM Guides 4.3.0-release geïdentificeerd:

- De algemene pagina-indeling die in de sjabloon Standaard is gedefinieerd, wordt niet als standaardsjabloon toegepast.

  Oplossing:
Voeg de algemene paginalay-out toe als vooromslag en achteromslag dan begint het voor elke pagina te komen.
- Het probleem doet zich voor in Sitezoekopdrachten terwijl u op de pagina AEM site-uitvoer op AEM Service Pack 16 of 17 zoekt.

  Oplossing:

   1. Bestand openen met pad: `/libs/foundation/components/search/search.jsp` in `crx/de`
   1. Regelnummer 234 vervangen door de volgende code:

      ```
      <a href="<c:url value="${hit.URL}" context="/"/>" onclick="trackSelectedResult(this, ${status.index + 1})"><%= xssAPI.filterHTML(((Search.Hit) pageContext.getAttribute("hit")).getTitle()) %></a>
      
      *(Add the missing closing anchor tag at the end).
      ```

   1. Sla het bestand op.
