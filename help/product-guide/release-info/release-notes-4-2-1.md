---
title: Opmerkingen bij de release | Upgradeinstructies en opgeloste problemen in Adobe Experience Manager Guides 4.2.1-versie
description: Meer informatie over de opgeloste problemen en hoe u een upgrade uitvoert naar 4.2.1-releases van Adobe Experience Manager Guides
exl-id: a75ec83f-564b-4243-b5c5-341049521adb
feature: Release Notes
role: Leader
source-git-commit: 6d8c01f20f7b59fed92c404561b647d9ebecb050
workflow-type: tm+mt
source-wordcount: '876'
ht-degree: 0%

---

# 4.2.1 release van Adobe Experience Manager Guides (mei 2023)

Deze versienota behandelt de verbeteringsinstructies, verenigbaarheidsmatrijs, en kwesties die in versie 4.2.1 van Adobe Experience Manager Guides (later als *worden bedoeld AEM Guides*) worden bevestigd.

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, zie [&#x200B; wat in versie 4.2.1 van Adobe Experience Manager Guides &#x200B;](whats-new-4-2-1-release.md) nieuw is.

## Upgrade naar versie 4.2.1 van AEM Guides


U kunt uw huidige versie van AEM Guides eenvoudig upgraden naar versie 4.2.1 Voordat u verdergaat met de upgrade naar versie 4.2.1 van AEM Guides, moet u rekening houden met de volgende punten:
U kunt uw huidige versie van AEM Guides upgraden naar versie 4.2.1
* Als u versie 4.1, 4.1.x of 4.2 gebruikt, kunt u rechtstreeks upgraden naar versie 4.2.1.
* Als u versie 4.0 gebruikt, moet u een upgrade naar versie 4.2 uitvoeren voordat u een upgrade naar versie 4.2.1 uitvoert.
* Als u versie 3.8.5 gebruikt, moet u een upgrade naar versie 4.0 uitvoeren voordat u een upgrade naar versie 4.2 uitvoert.
* Raadpleeg de sectie Upgrade AEM Guides in de productspecifieke installatiehandleiding als u werkt met een versie die ouder is dan 3.8.5.

>[!NOTE]
>
>U moet AEM servicepack installeren voordat u de AEM Guides-versie kunt upgraden.

Voor details, zie [&#x200B; instructies van de Verbetering &#x200B;](../install-guide/upgrade-xml-documentation.md).

## Compatibiliteitsmatrix

Deze sectie bevat een overzicht van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door AEM Guides 4.2. 1 release.

### Adobe Experience Manager

**niet-UUID**
Versie 6.5 Service Pack 15, 14, 13 of 12

**UUID**
Versie 6.5 Service Pack 15, 14, 13 of 12

Voor meer details, zie de *Technische vereisten* sectie in installeer en vorm de gids van Adobe Experience Manager Guides.

### FrameMaker en FrameMaker Publishing Server

| Geen | FMPS 2022 | FMPS 2020 | Fm 2022 | Fm 2020 |
| --- | --- | --- | --- | --- |
| 4.2.1 (niet-UUID) | 2022 of hoger | 2020.2 of hoger* | 2022 of hoger | 2020.3 of hoger |
| 4.2.1 (UUID) | 2022 of hoger | 2020.2 of hoger* | 2022 of hoger | 2020.4 of hoger |
| | | | |

*Basislijn en voorwaarden die in AEM zijn gemaakt, worden vanaf 2020.2 ondersteund in FMPS-releases.

### Zuurstofaansluiting

| Geen | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- |--- |--- |
| 4.2.1 (niet-UUID) | 2.2-regelmatig-3 | 2.2-regelmatig-3 | 1,6 | 1,6 |
| 4.2.1 (UUID) | 2.9-uuid-2 | 2.9-uuid-2 | 2,3 | 2,3 |
|  |  |   |

## Opgeloste problemen

De fouten die in verschillende gebieden zijn gecorrigeerd, worden hieronder weergegeven:

### Authoring

* Navigatitel wordt verwijderd uit de inhoud wanneer de layoutweergave wordt gewijzigd in de auteur- of bronweergave. 12174
* De sluitknop in de webeditor leidt niet tot AEM navigatiepagina. (1948)
* Soms treedt een toepassingsfout op bij het klikken op een DITA-kaart. (11842)
* Probleem doet zich voor bij het verplaatsen (slepen en neerzetten) in plaats van een bestaand lijstitem met Wijzigingen bijhouden ingeschakeld. (11570)
* Probleem doet zich voor bij het verplaatsen (slepen en neerzetten) als een nieuw lijstitem met Wijzigingen bijhouden ingeschakeld. (11569)
* Lijstitems inspringen of uitspringen werken niet zoals u had verwacht bij Wijzigingen bijhouden ingeschakeld. (11568)
* Als u inhoud toevoegt op een regel met Wijzigingen bijhouden ingeschakeld en vervolgens Wijzigingen bijhouden uitschakelt, wordt de inhoud niet daadwerkelijk uitgeschakeld. 11567
* Moeilijk om een list-item te slepen en neer te zetten, wordt tekst verplaatst in plaats van het list-item. (11566)
* Bij het ontwerpen in het element dat groen (Wijzigingen bijhouden) wordt weergegeven, wordt de nieuwe inhoud weergegeven als een wijziging in de track, ook al is de trackwijziging uitgeschakeld. 7021)
* Browser (de Redacteur van het Web) bevriest bij het laden van inhoud met douaneschema. (1121)
* Native PDF | Bij het maken van een uitvoervoorinstelling met de optie Toevoegen aan mapprofiel mislukt het genereren van de PDF met een Null-aanwijzer. 10950
* Native PDF | Met de tag Afbeelding wordt het kenmerk display-inline toegevoegd aan alle afbeeldingen. 10653
* De toevoeging voor audio en videodossiers van verschillende media ontbreekt in het formaat van YouTube onder het **Multimedia van het Tussenvoegsel** pictogram. 11320
* Validatiefout treedt op wanneer een kaart wordt gemaakt met behulp van de sjabloon met een speciaal titelelement. 11212
* Webeditor | De vaste ruimte wordt toegevoegd in de Redacteur van XML terwijl het uitgeven van een onderwerp. (11786)

### Beheer

* Het lusje van rapporten in de Redacteur UI van het Web toont niet de onderwerpenlijst van oude kaarten DITA die vóór 4.2 verbetering worden gecreeerd. (11708)

* De functionaliteit van de knop Bestanden uploaden in het gebruikersinterface-einde van Assets in versie 4.2. (11633)


### Publiceren

* Native PDF | Het publiceren van inhoud die een outputklasse met steunen () heeft leidt tot een het publiceren bevriezing. (1936)
* JSON-uitvoer | Metagegevens met een eigenschap toewijzen die de waarde `"value in spaces and double quotes"` heeft, leiden tot een publicatiefout. (1933)
* Het probleem doet zich voor in AEM zoekopdracht op de site (werkt niet meer dan 2-3 knooppunten op het niveau). 11352
* Webeditor | Uitvoerpad en sjabloon kunnen niet worden geselecteerd in de AEM Voorinstelling. (11530)
* Bij een upgrade van 4.1.x naar 4.2 werkt de Native PDF-engine niet en wordt zelfs voor het ondersteunde besturingssysteem NullPointerException gegenereerd.11526
* Het proces van de PDF van de download werkt niet geschikt in de Redacteur van het Web. 11496
* Native PDF | Conceptopmerkingen worden standaard verborgen in de gegenereerde uitvoer. 10560
* Native PDF | navtitle wordt niet geëerd voor topichead . 10509
* Native PDF | Als u `xref` toevoegt aan een afbeelding, wordt de afbeelding op de gegenereerde PDF niet weergegeven. 11346
* Native PDF | voetnoot in de tabelkoptekst leidt tot vette en gecentreerde tekst in de bijbehorende voettekst op de pagina in de PDF-uitvoer. 10610

### Vertaling

* Bij de upgrade naar 4.2 wordt alle vertaalinhoud weergegeven als Niet-gesynchroniseerd of Ontbrekend exemplaar. (11834)

### Controleren

* Voltooide revisie wordt niet geopend in de modus Alleen-lezen. 11387
