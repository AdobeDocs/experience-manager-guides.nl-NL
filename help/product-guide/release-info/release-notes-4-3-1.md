---
title: Opmerkingen bij de release | Upgradeinstructies en opgeloste problemen in Adobe Experience Manager Guides 4.3.1-versie
description: Meer informatie over de opgeloste problemen en hoe u een upgrade uitvoert naar 4.3.1-releases van Adobe Experience Manager Guides
exl-id: 3fb6dc31-ec6e-40f5-ab3f-a6e591da315e
feature: Release Notes
role: Leader
source-git-commit: 1b25f1df67fa2442ab79830dc2ac5a6eabd0394c
workflow-type: tm+mt
source-wordcount: '1308'
ht-degree: 0%

---

# 4.3.1. Vrijgave van Adobe Experience Manager Guides (oktober 2023)

Deze versienota behandelt de verbeteringsinstructies, verenigbaarheidsmatrijs, en kwesties die in versie 4.3.1 van Adobe Experience Manager Guides (later als *worden bedoeld Experience Manager Guides*) worden bevestigd.

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, zie [ wat in versie 4.3.1 van Adobe Experience Manager Guides ](./whats-new-4-3-1-release.md) nieuw is.

## Upgrade naar versie 4.3.1 van Experience Manager Guides


U kunt uw huidige versie van Experience Manager Guides eenvoudig upgraden naar versie 4.3.1. Voordat u verdergaat met de upgrade naar versie 4.3.1 van Experience Manager Guides, moet u rekening houden met de volgende punten:
U kunt uw huidige versie van Experience Manager Guides upgraden naar versie 4.3.1


- Als u versie 4.3.0, 4.2 of 4.2.1 gebruikt, kunt u rechtstreeks upgraden naar versie 4.3.1.
- Als u versie 4.1 of 4.1.x gebruikt, moet u een upgrade naar versie 4.3.0, 4.2 of 4.2.x uitvoeren voordat u een upgrade naar versie 4.3.1 uitvoert.
- Als u versie 4.0 gebruikt, moet u een upgrade naar versie 4.2 uitvoeren voordat u een upgrade naar versie 4.3.1 uitvoert.
- Als u versie 3.8.5 gebruikt, moet u een upgrade naar versie 4.0 uitvoeren voordat u een upgrade naar versie 4.2 uitvoert.
- Raadpleeg de sectie Upgrade Experience Manager Guides in de productspecifieke installatiehandleiding als u werkt met een versie die ouder is dan 3.8.5.


>[!NOTE]
>
>U moet AEM servicepack installeren voordat u de Experience Manager Guides-versie kunt upgraden.

Voor details, zie [ instructies van de Verbetering ](../install-guide/upgrade-xml-documentation.md).

## Compatibiliteitsmatrix

In deze sectie wordt een overzicht gegeven van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door de Experience Manager Guides 4.3.1-release.

### Adobe Experience Manager

**4.3.1 niet-UUID**
Versie 6.5 Service Pack 18, 17, 16, 15 of 14

**4.3.1 UUID**
Versie 6.5 Service Pack 18, 17, 16, 15 of 14

Voor meer details, zie de *Technische vereisten* sectie in installeer en vorm de gids van Adobe Experience Manager Guides.

### FrameMaker en FrameMaker Publishing Server

| Geen | FMPS 2022 | FMPS 2020 | Fm 2022 | Fm 2020 |
| --- | --- | --- | --- | --- |
| 4.3.1 (niet-UUID) | 2022 of hoger | 2020.2 of hoger* | 2022 of hoger | 2020.3 of hoger |
| 4.3.1 (UUID) | 2022 of hoger | 2020.2 of hoger* | 2022 of hoger | 2020.4 of hoger |
| | | | |

*Basislijn en voorwaarden die in AEM zijn gemaakt, worden vanaf 2020.2 ondersteund in FMPS-releases.

### Zuurstofaansluiting

| Geen | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- |--- |--- |
| 4.3.1 (niet-UUID) | 2.3-regelmatig-5 | 2.3-regelmatig-5 | 1,6 | 1,6 |
| 4.3.1 (UUID) | 3.2-uuid-5 | 3.2-uuid-5 | 2,3 | 2,3 |
|  |  |   |



### Versie van basissjabloon

| Naam van componentenpakket | Versie van componenten | Sjabloonversie |
|---|---|---|
| Experience Manager Guides Components Content Package voor Cloud Service | dxml-components.all-1.2.2 | aem-site-template-dxml.all-1.0.15 |

## Opgeloste problemen

De fouten die in verschillende gebieden zijn gecorrigeerd, worden hieronder weergegeven:

### Authoring

- De uren van de middag worden niet geplaatst in de **Datum** voor de verwezenlijking van basislijnen. 12712
- Kan de JSON-code niet plakken in het `<codeblock>` -element van de webeditor. 12326
- Niet-opgeslagen versiewijzigingen en de indicatoren daarvoor worden niet weergegeven voor grote bestanden. (11784)
- Tijdens het bewerken in de Koreaanse taal verandert het eerste teken in de standaardwaarde. 10049

- Het voorvoegsel wordt gedupliceerd in de voorvertoningsmodus van de webeditor. (13133)
- `Choicetable` -rijen worden niet weergegeven of kunnen niet worden geselecteerd. 12616
- De Redacteur van het Web werpt bevestigingsfouten in specifieke scenario&#39;s wanneer het creëren van een onderwerp gebruikend een douaneschema. 12576
- De verwijzingen van het ditaval onderwerpmalplaatje leiden tot geen exemplaar in de inhoudsomslag wanneer het creëren van een kaart van het kaartmalplaatje. 12150

- Het zoekvak in DITA-kaarten heeft geen knop Sluiten. (11867)
- Wanneer u lange bestanden opslaat in de webeditor, genereert `DirtyChecker` een uitzondering met een lange stacktracering en worden de logbestanden gevuld. (11860)
- Het creëren van onderwerpen DITA vereist de toestemming van de Schrapping op de overeenkomstige omslagknoop, hoewel de kaart met schrijftoestemming kan worden gecreeerd. 11706
- De Redacteur van het Web toont een onjuiste titel wanneer een schuine streep aanwezig is. 10949

- Als de titel van een onderwerp een schuine streep &quot;/&quot;bevat, toont het lusje in de redacteur slechts de brieven die na dat komen. (13455)
- De voorvertoning van de afbeelding verdwijnt niet nadat de voorvertoning in de Editor is weergegeven. 13454
- Enkele bestaande versie of de labels ervan worden na de upgrade naar 4.x niet weergegeven in Versiehistorie. (13247)
- Het paneel van de Geschiedenis van de Versie in Assets UI toont onjuiste timestamp voor het **Huidige** gebied. 12624
- Onderwerp met conref-titel wordt niet opgelost in de weergave Opslagplaats of Kaartweergave.(13304)


### Publiceren

- Native PDF | De orde van de onderwerpen is niet vast wanneer de output van de PDF wordt geproduceerd. 13157
- Oorspronkelijke PDF| Geen standaardstijlmarkering is beschikbaar voor `<p>` element. (12559)
- Native PDF | Inline stijlen die worden toegepast op het inhoudsgebied, worden niet toegepast op de onderwerpen voor- en achtermaterie. 13510
- Het kenmerk `DeliveryTarget` wordt niet doorgegeven bij het genereren van de AEM Site-uitvoer.  13132
- Het **Publish** werkschema wordt geplakt terwijl het produceren van AEM output van de Plaats voor inhoud met bepaalde fouten. 12000

- Native PDF | Als u meerdere Xrefs toevoegt, wordt de tekst breder dan de kolombreedte. 13004
- Native PDF | Wanneer het onderwerp en de titel zelfde identiteitskaart hebben, leidt het tot een misvormde generatie van de output van PDF. (12644)
- Native PDF | Bij het toevoegen van een outputklasse aan een ouder `<topicref>` element in een kaart DITA en het toepassen van douanestijl op de outputklasse, wordt het stileren toegepast op elementen binnen het onderwerplichaam, met inbegrip van sectitels. (12166)
- Incrementeel publiceren werkt niet als een DITA-kaart meerdere databases heeft. (1217)
- Site AEM | Bij het creëren van een kaart met keydef richtend aan een onderwerp als variabele en toevoegend verwerkings-rol=middel-slechts leidt tot sommige onverwachte pagina&#39;s. (12099)
- Als om het even welke activa van AEM DAM in om het even welke output buiten de AEM plaats worden gebruikt, dan weerspiegelen de meta-gegevens &quot;jcr:createdBy&quot;niet de naam van de uitgever of de naam van de gebruiker die het DITA- kaart of onderwerp het laatst wijzigde. 12090
- AEM Sites | De DITA-kaart met padgegevens in de navtitle (met niet-ondersteunde tekens) leidt tot onjuiste pagina-URL&#39;s. (1978)
- Native PDF | Er doen zich problemen voor ter ondersteuning van topichead / topicmeta / navtitle in FrontMatting en Backissue. (1969)
- Native PDF | Het genereren van PDF voor grote documenten kost veel tijd. (1955)
- Native PDF | Als de naam van een voorinstelling wordt gewijzigd, wordt een NullPointerException gegenereerd terwijl een PDF-uitvoer wordt gegenereerd. (11889)
- De `<conref>` -inhoud wordt niet weergegeven in de PDF-uitvoer. (1131)
- Er wordt een extra spatie toegevoegd in de `<div>` -elementen bij het schakelen tussen de weergave Auteur en Source in de pagina-indelingseditor. 10750
- De inhoud die via AEM Cloud Manager wordt gerepliceerd, is niet zichtbaar op de Publish-instantie. 9564


### Beheer

- Versiegeschiedenis wordt niet weergegeven, zelfs niet als de eigenschap `dc:format` niet aanwezig is voor een element. 10463
- De verwijzing van de inhoud is gebroken exemplaar-kleeft DITA- dossiers wanneer onderwerpidentiteitskaart niet het zelfde als GUID is. 12614
- In dynamische basislijnen, wordt de lijst van etiketten niet getrokken uit de directe verwijzingen van het werkende exemplaar van een kaart DITA. (1917)
- De basislijn toont het onjuiste aantal dossiers op het Dashboard van de Kaart wanneer het gebruiken van Browse alle onderwerpfunctionaliteit. 13265)
- In de Redacteur van het Web, toont de basislijn de titel voor de vorige versie in plaats van de geselecteerde versie van het DITA- dossier. (13444)

### Controleren

- In de revisie over een onderwerp worden onjuiste opmerkingen weergegeven. 13453
- Met de knop Sluiten op de pagina Revisie in de Experience Manager Guides gaan de gebruikers naar de AEM Homepage. 13535
- De gehechtheid wordt niet getoond op het juiste paneel van de redacteur voor een onderwerp in-overzicht. (1301)



### Vertaling

- De basislijn die van **wordt uitgevoerd Vertaling** dashboard ontbreekt en opent niet in de doeltaal. (13466)

- Er worden nieuwe vertaalprojecten gemaakt in plaats van nieuwe banen toe te voegen aan de geselecteerde bestaande vertaalprojecten.  10214
- De titel van het vertaalde bestand wordt weergegeven in plaats van de titel van het bronbestand. (11630)
- Automatisch goedkeuren werkt soms niet, en de uitzonderingen komen voor als een onjuiste waarde bij de Status van de Vertaling wordt geplaatst. 13607
- De basislijn die u exporteert vanaf het dashboard Vertalen mislukt en wordt niet geopend in de doeltaal. (12993)
- Sommige bestanden ontbreken bij het gebruik van basislijnen bij het vertalen. (13021)
