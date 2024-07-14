---
title: Opmerkingen bij de release | Adobe Experience Manager Guides as a Cloud Service, release augustus 2022
description: Release van Adobe Experience Manager Guides as a Cloud Service in augustus
exl-id: a01bfe8a-4715-438c-bb94-aa1d31f6662d
feature: Release Notes
role: Leader
source-git-commit: 6d8c01f20f7b59fed92c404561b647d9ebecb050
workflow-type: tm+mt
source-wordcount: '1169'
ht-degree: 0%

---

# Release van Adobe Experience Manager Guides as a Cloud Service in augustus

## Upgrade naar de release van augustus

Bevorder uw huidige as a Cloud Service Adobe Experience Manager Guides (later als *wordt bedoeld AEM Guides as a Cloud Service*) opstelling door de volgende stappen uit te voeren:
1. Controle uit de code van Git van Cloud Servicen en schakelaar aan de tak die in de pijpleiding van Cloud Servicen wordt gevormd die aan het milieu beantwoordt u wilt bevorderen.
1. Werk de eigenschap `<dox.version>` in het `/dox/dox.installer/pom.xml` -bestand van de Git-code van de Cloud Service bij naar 2022.8.167.
1. Leg de wijzigingen vast en voer de pijplijn met Cloud Servicen uit om de release van AEM Guides as a Cloud Service in augustus te upgraden.

## Compatibiliteitsmatrix

In deze sectie wordt een overzicht gegeven van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door de AEM Guides-release van as a Cloud Service augustus 2022.

### FrameMaker en FrameMaker Publishing Server

| FMPS | FrameMaker |
| --- | --- |
| Niet compatibel | 2020-update 4 en hoger |
| | |

*Basislijn en voorwaarden die in AEM zijn gemaakt, worden vanaf 2020.2 ondersteund in FMPS-releases.

### Zuurstofaansluiting

| AEM Guides als Cloud Release | Oxygeenaansluiting, Windows | Oxygeenconnector Mac |
| --- | --- | --- |
| 2022,8,0 | 2.7.5. | 2.7.5. |
|  |  |  |


## Nieuwe en verbeterde functies

AEM Guides as a Cloud Service biedt veel verbeteringen en nieuwe functies in de release van augustus:

### Layoutweergave in de Kaarteditor

Nu kunt u de volledige lay-out van een kaart DITA in de Redacteur van de Kaart bekijken. Wanneer u een kaart voor het uitgeven opent, opent het de **mening van de Lay-out** van de Redacteur van de Kaart. In deze weergave kunt u de kaarthiërarchie in een boomstructuurweergave zien en de onderwerpen in een kaart ordenen of structureren.

![ lay-outweergave ](assets/layout-view-map.png)

De layoutweergave bevat een aparte werkbalk waarmee u veel taken kunt uitvoeren met betrekking tot de onderwerpen in een kaart.
U kunt onderwerpverwijzingen, onderwerpgroep, zeer belangrijke definities in een kaart opnemen. U kunt de onderwerpen in een kaart reorganiseren door ze omhoog, omlaag, links of rechts te verplaatsen. U kunt de onderwerpen ook slepen en neerzetten om ze in een kaart te verplaatsen. De Kaarteditor verstrekt ook de pictogrammen om dossiers te sluiten of te ontgrendelen, de versiegeschiedenis te controleren, en een beheer van het versielabel te doen.


De mening van de Lay-out verstrekt ook de **Opties van de Mening** om lijnaantal te tonen of te verbergen, of controledoos te tonen of te verbergen, of de dossier - naam of titel voor de onderwerpen in een kaart te tonen.


![ mening-opties ](assets/view-options.png)

U kunt de onderwerpen ook bekijken die op de voorwaardelijke filters worden gebaseerd die op hen worden toegepast.

Naast het organiseren van onderwerpen in het kaartdossier, kunt u ook toevoegen, bewegen, kopiëren, kleven, of verwijzingen schrappen gebruikend het **menu van Opties** beschikbaar voor een element in de mening van de Lay-out. U kunt ook een onderwerp of een kaart van het paneel van de bewaarplaats aan de kaart slepen en neerzetten die in de Redacteur van de Kaart wordt geopend.

In het rechterdeelvenster worden de eigenschappen Inhoud en Kaart weergegeven in de layoutweergave van de Kaarteditor. De gealigneerde Attributen die voor het geselecteerde onderwerp worden bepaald worden getoond tegen het onderwerp in de mening van de Lay-out. U kunt bijvoorbeeld snel alle onderwerpen vinden waarvoor het platformkenmerk is gedefinieerd als `IOS` .

Nu kunt u de meta-gegevensinformatie voor de onderwerpen of de kaart ook plaatsen. U kunt de Titel Nav, de Tekst van de Verbinding, Korte Beschrijving, en Sleutelwoorden voor het geselecteerde onderwerp of de kaart bepalen.

![ het juiste paneel van de lay-outweergave ](assets/layout-inline-attributes.png)

Voor meer details, zie *sectie van de mening van de Lay-out van 0} in het Gebruiken van Adobe Experience Manager Guides as a Cloud Service.*

### Inline-kenmerken in de Editor-instellingen

AEM Guides staat nu de configuratie van **Gealigneerde Attributen** door uw beheerder van de **Montages van de Redacteur** toe. U kunt nieuwe gealigneerde attributen ook toevoegen of bestaande degenen van het **Gealigneerde lusje van Attributen** in de Montages van de Redacteur schrappen.
De gevormde Inline Attributen die voor een onderwerp worden bepaald worden getoond tegen het onderwerp in de mening van de Lay-out.

![ Montages van de Redacteur ](assets/editor-settings-inline-attributes.png)


### Extra filters in de weergave Opslagplaats

De filterzoekopdracht in de dataweergave is nu krachtiger gemaakt. Twee nieuwe onderzoekscriteria, **Laatst Gewijzigde** en **Codes** zijn toegevoegd om de dossiers te filtreren en uw onderzoek in de AEM bewaarplaats te beperken:
* **Laatste Gewijzigd**: U kunt naar dossiers zoeken die na een geselecteerde datum maar vóór een geselecteerde datum zijn gewijzigd. U kunt ook de vooraf gedefinieerde criteria gebruiken en zoeken naar bestanden die de laatste twee uur, vorige week, vorige maand of vorig jaar zijn gewijzigd.
* **Markeringen**: U kunt dossiers ook zoeken die specifieke markeringen hebben op hen worden toegepast. U kunt de tag typen of deze selecteren in de vervolgkeuzelijst.

![ de meningsfilters van de Bewaarplaats ](assets/repo-filter-search.png)


## Opgeloste problemen

De fouten die in verschillende gebieden zijn gecorrigeerd, worden hieronder weergegeven:

* Vervangen Lucene-index wordt gebruikt in /core/article-publish/src/main/java/com/adobe/dxml/article/publish/util/DoxUtils.java (9291)
* Bijgewerkte Node.js wordt niet gebruikt voor het publiceren. 9835
* Het onderwerp DITA wordt niet automatisch bijgewerkt met de veranderingen die op de **pagina van Eigenschappen** worden gedaan. 8745
* FrontMattelement wanneer toegevoegd aan een DITA-boekenkaart werkt niet correct. 9507
* Native PDF | Een lege PDF wordt geproduceerd bij het gebruiken van **snel produceert** voor veelvoudige dossiers wanneer een leeg element wordt geselecteerd. (9822)
* Native PDF | Aanhangsel wordt gepubliceerd als een hoofdstuk in de uitvoer van PDF. 9829
* Native PDF | Wanneer een SVG-afbeelding wordt bewerkt, wordt deze niet bijgewerkt weergegeven in de paginalay-out. 9069
* Een regelmatig afbreekkarakter wordt opgenomen wanneer a `Nonbreaking Hyphen` karakter gebruikend het **Speciale Karakter van het Tussenvoegsel** dialoog wordt opgenomen. 8919
* De Redacteur van XML toont geen bijgewerkte beelden in de onderwerpen als zij zijn uitgegeven. 9500
* Terwijl het publiceren van de output via de Redacteur, kunnen vooraf instelt niet van de **Output** tabel worden geschrapt. 9100
* Submaps van een kaart DITA worden niet gecontroleerd gebruikend **Uitgezochte Al** optie van het ellipsmenu. 9814
* Onbekwaam om kaart of onderwerpmalplaatjes van het **menu van Malplaatjes** aan het malplaatje van de douanekaart in de redacteur van het Web te slepen. 9846
* Onbekwaam om een nieuw onderwerp of kaartmalplaatje in subfolder van een kaart of onderwerpmalplaatje tot stand te brengen. (9888)
* Er is geen optie aanwezig om door de onderwerpen of kaarten te bladeren die aanwezig zijn in de submappen van een kaart of onderwerpsjabloon. (9889)
* Wanneer een Schematron-bestand samen met het DITA-bestand wordt bijgewerkt en opgeslagen, wordt het rechterdeelvenster niet weergegeven (als het DITA-bestand de validaties in het Schematron-bestand verbreekt). (986)
* Er kan een nieuwe voorinstelling voor gedupliceerde uitvoer worden gemaakt als de naam van deze voorinstelling gelijk is aan die van een bestaande voorinstelling. (997)
* SVG-afbeeldingen worden beschadigd en publiceren niet correct wanneer de HTML-uitvoer wordt gegenereerd. (9949)


## Bekende problemen

Adobe heeft de volgende bekende problemen voor de release van AEM Guides as a Cloud Service augustus 2022 vastgesteld.

### Bekende problemen met tijdelijke oplossing

Gebruik de opgegeven tijdelijke oplossing voor de volgende bekende problemen:

* De layoutweergave is niet zichtbaar in de Kaarteditor.

  **Oplossing**: Werk ui_config.json in het Profiel van de Omslag bij.

* Symbols.json wordt overschreven, zodat uitgave 8919 voorkomt.

  **Oplossing**: Bijgewerkte symbolen.json moet met met met voeten getreden symbols.json worden samengevoegd.

### Andere bekende problemen

* Als er meerdere bestanden zijn geselecteerd in de resultatensectie die wordt weergegeven bij het uitvoeren van een zoekopdracht in de opslagplaats en vervolgens slepen en neerzetten in de auteurweergave, wordt slechts één bestand toegevoegd.
