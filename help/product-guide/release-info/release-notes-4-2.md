---
title: Opmerkingen bij de release | Adobe Experience Manager Guides 4.2-release
description: Meer informatie over de opgeloste problemen en hoe u een upgrade uitvoert naar 4.2-releases van Adobe Experience Manager Guides
exl-id: 8a7fef77-63af-462f-89c5-054ab31e079b
feature: Release Notes
role: Leader
source-git-commit: 6d8c01f20f7b59fed92c404561b647d9ebecb050
workflow-type: tm+mt
source-wordcount: '1391'
ht-degree: 0%

---

# 4.2. Release van Adobe Experience Manager Guides (februari 2023)

Deze versienota behandelt de verbeteringsinstructies, verenigbaarheidsmatrijs, en kwesties die in versie 4.2 van Adobe Experience Manager Guides (later als *worden bedoeld AEM Guides*) worden bevestigd.

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, zie [ wat in versie 4.2 van Adobe Experience Manager Guides ](whats-new-4-2-release.md) nieuw is.

## Upgrade naar versie 4.2 van AEM Guides

U kunt uw huidige versie van AEM Guides eenvoudig upgraden naar versie 4.2. Voordat u verdergaat met de upgrade naar versie 4.2 van AEM Guides, moet u rekening houden met de volgende punten:
* Als u versie 4.0, 4.1 of 4.1.x gebruikt, kunt u rechtstreeks upgraden naar versie 4.2.
* Als u versie 3.8.5 gebruikt, moet u een upgrade naar versie 4.0 uitvoeren voordat u een upgrade naar versie 4.2 uitvoert.
* Als u op een versie voorafgaand aan 3.8.5 bent, verwijs naar de *sectie van de Verbetering AEM Guides* in de product-specifieke installatiegids.

>[!NOTE]
>
>U moet AEM servicepack installeren voordat u de AEM Guides-versie kunt upgraden.

Voor details, zie [ instructies van de Verbetering ](assets/Adobe-Experience-Manager-Guides-Upgrade-Instructions-EN.pdf).

## Compatibiliteitsmatrix

In deze sectie wordt een overzicht gegeven van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door de AEM Guides 4.2-release.

### Adobe Experience Manager

**niet-UUID**
Versie 6.5 Service Pack 15, 14, 13 of 12

**UUID**
Versie 6.5 Service Pack 15, 14, 13 of 12

Voor meer details, zie de *Technische vereisten* sectie in installeer en vorm de gids van Adobe Experience Manager Guides.

### FrameMaker en FrameMaker Publishing Server

| Geen | FMPS 2022 | FMPS 2020 | Fm 2022 | Fm 2020 |
| --- | --- | --- | --- | --- |
| 4.2 (Niet-UUID) | 2022 of hoger | 2020.2 of hoger* | 2022 of hoger | 2020.3 of hoger |
| 4.2 (UUID) | 2022 of hoger | 2020.2 of hoger* | 2022 of hoger | 2020.4 of hoger |
| | | | |

*Basislijn en voorwaarden die in AEM zijn gemaakt, worden vanaf 2020.2 ondersteund in FMPS-releases.

### Zuurstofaansluiting

| Geen | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- |--- |--- |
| 4.2 (Niet-UUID) | 2.1-regelmatig-4 | 2.1-regelmatig-4 | 1,6 | 1,6 |
| 4.2 (UUID) | 2,8-uuid-8 | 2,8-uuid-8 | 2,3 | 2,3 |
|  |  |   |

## Opgeloste problemen

De fouten die in verschillende gebieden zijn gecorrigeerd, worden hieronder weergegeven:

### Authoring

* Het linkerpaneel breekt bij het toevoegen van een lusje. (1126)
* Wijzigingen in de HTML van de webeditor veroorzaken problemen met `<dl>` en `<dlentry>` . (1024)
* Sommige kenmerken worden niet behandeld als voorwaardelijk en veroorzaken problemen. 10895
* Drie niveaus of meer geneste `<indexterm>` zijn niet genest in native PDF-export. (10799)
* De inhoud verdwijnt in de hoofdtekst van een taak bij het schakelen van de weergave Auteur naar de weergave Source. 10735
* Opmerkingen voor revisies worden verkeerd geplaatst in een revisietaak. 10625
* `<conref>` -notitie in een para-tag wordt niet weergegeven in de voorvertoningsmodus. (10559)
* Als u de backspace aan het einde van een lijstitem aanpast, wordt de hele lijst verwijderd. 10540
* Het scherm wordt als leeg weergegeven in Chrome v106 bij het slepen en neerzetten van een element vanuit de gebruikersinterface (bijvoorbeeld vanuit het deelvenster Voorwaarden). 10524
* De auto knoop van de Inspringing mist van de toolbar in de **** mening van Source. (10448)
* Het eerste teken van een lijstitem gaat soms verloren wanneer de lijst in de editor wordt geschreven.(10447)
* **ongedaan maken** of **opnieuw** werkt niet correct aan sommige dossiers. 10373
* Aangepaste metagegevens blijven niet behouden bij kopiëren en plakken. 10367
* Er treedt een fout op bij het kopiëren (ctrl+c) en plakken (ctrl+v) van inhoud. 10304
* In het deelvenster Omtrek wordt geen inhoud weergegeven wanneer van de modus Auteur naar de modus Source wordt geschakeld. 10296
* Submap wordt niet gecreeerd wanneer het naar een hoofdkaart in Malplaatjes DITA verwijst. 10231
* De kwesties van de navigatie komen in de Redacteur van het Web na 4.0 verbetering voor. 10159
* Met de optie Ongedaan maken in de XML-editor komt de gebruiker boven aan de pagina. 10091
* Node-eigenschappen worden verwijderd na kopiëren en plakken van een element. 10053
* SVG-bestanden die aan DITA-onderwerpen worden toegevoegd, worden niet weergegeven in de voorbeeldmodus van de editor. 10010
* Zoekresultaten voor zoeken en vervangen in de webeditor zijn niet leesbaar in de modus Donker. (978)
* Er bestaat geen lader tijdens het maken van een kaart van de kaartsjabloon. 9891
* Conref in het onderwerpmalplaatje werkt niet en gekopieerde knoeiboelidentiteitskaart wordt niet bijgewerkt in het inhoudsexemplaar. 9890
* Geen optie wordt getoond om de onderwerpen of kaartmalplaatje binnen subfolders van de onderwerp of kaartomslag te doorbladeren. (9889)
* Geen optie om een nieuw malplaatje op subfolders van onderwerpen of kaarten te creëren. (9888)
* De redacteur van XML werkt niet de beelden op onderwerpen bij. 9500
* mimeType is hardcoded voor DITA activa verwezenlijking en update. 8979
* Een normaal afbreekstreepje wordt opgenomen bij het selecteren van Vast afbreekstreepje in het **Speciale Teken van het Tussenvoegsel** dialoog. 8919
* De naam van de maker van de versie in Versiehistorie is &quot;fmdita-servicegebruiker&quot; voor de bestanden die zijn geüpload via de gebruikersinterface van Assets. 8910
* De optie Bewerken werkt niet voor afbeeldingen wanneer u werkt in de kolomweergave van de gebruikersinterface van Assets. 8758
* Het onderwerp DITA wordt niet auto bijgewerkt met veranderingen die op **worden gedaan Eigenschappen** pagina. 8745
* Terwijl het bewegen van elementen binnen het onderwerp in de Redacteur van het Web, toegewezen IDs op elementen wordt overschreven door auto-toegewezen IDs. 7895

### Beheer

* Het kopiëren van een DITA-kaart-element (van de Asset UI) veroorzaakt onjuiste basislijnen in het gekopieerde element. 11218
* Er wordt geen waarschuwingsbericht weergegeven bij het uploaden van een bestand dat groter is dan de limiet die is toegestaan in AEM (standaard 2 GB). 10817
* Web Editor-basislijn | Het gedrag van de Meest recente kolom is verschillend in het nieuwe basislijndashboard binnen de Redacteur van het Web. 10808
* Vertaling | De vertaaltaak wordt niet gestart vanwege ongeldige /libs/fmdita/i18n/ja.json. 10543
* Vertaling | Er is een fout opgetreden in een bereikvertaalproject dat is gemaakt op het vertaaldashboard (Menselijke vertaling). 10526
* Vertaling | Post-verwerking wordt geblokkeerd voor de gehele taalmap waarvan de middelen aanwezig zijn in een actief vertaalproject. (1032)
* Vertaling| Metagegevens en tags worden niet doorgegeven aan de vertaalde kopieën. 4696
* Er worden meerdere pop-ups weergegeven voor elk element als de versie wordt gewijzigd en opgeslagen in de basislijneditor. 10399
* De lekkage van de zitting komt bij com.day.cq.search.impl.builder.QueryBuilderImpl.createResourceResolver (QueryBuilderImpl.java:210) voor. 10279
* Het videobestand ontbreekt vanaf de basislijn als de bovenliggende map ruimte in de naam bevat. 10031

### Publiceren

* De regeneratie van het onderwerp werkt niet voor sommige scenario&#39;s. 10635
* Publiceren via PDF mislukt bij het genereren van de uitvoer voor een dubbele voorinstelling (van een bestaande voorinstelling). 10584
* De knop Logbestand weergeven werkt niet als het genereren van de PDF mislukt voor een voorinstelling. 10576
* De luisteraar van de uitgever toont niet de gevraagde gegevens in info- logboeken, en het bevat ook sommige junk logboeken.(10567)
* Native PDF | PDF genereren mislukt met een Null-aanwijzeruitzondering. 10950
* Native PDF | conkeyref wordt niet opgelost in de geproduceerde output. 10564
* Native PDF | Problemen treden op met de metagegevens van een kaart waarnaar in de uitvoer van de PDF moet worden verwezen.(10556)
* Native PDF | Er treden problemen op bij het roteren van de tabelkop. (10555)
* Native PDF | De kwesties komen bij het verwijderen van onderwerpen voor die verwerkingsrol=&#39;middel-slechts&#39; hebben. (10554)
* Native PDF | Lege toetsaanslagen worden weergegeven in PDF-uitvoer. (10553)
* Native PDF | Geneste `<indexterm>` zijn niet genest bij native PDF-export. 10521
* Native PDF | Native PDF gebruikt inline stijl in plaats van klassenaam voor de gegenereerde tags. 10498
* Native PDF | Geneste topicref in aanhangsels wordt allen omgezet aan h1 in tijdelijke HTML.(10454)
* Native PDF | Kan de onderwerpen frontMatrix niet verbergen in de inhoudsopgave. 10355
* Native PDF | Kenmerk tabelframe niet doorgegeven aan de tijdelijke HTML (als klasse). 10353
* Native PDF | Tijdelijke HTML-bestanden voegen de klassen colsep en rowsep toe aan <td> en <th> zelfs als hun waarde 0 in bronDITA is. 10352
* Native PDF | Als u de paginanummers opnieuw instelt in de hoofdstuklayout, wordt de nummering vanaf het einde van het vorige hoofdstuk willekeurig gestart. 10154
* Native PDF | Belangrijke referenties voor toetsaanslagen met afbeeldings- of externe koppelingen worden niet opgelost. 10063
* Native PDF | Bijlage wordt weergegeven als een hoofdstuk in gegenereerde PDF. 9829
* Het tabblad Sjabloon in de XML-editor wordt niet weergegeven bij Mapprofielbeheerders. (10266)
* Het publiceren van de basislijn ontbreekt voor PDF die gebruikend FrameMaker Publishing Server 2020 wordt geproduceerd. (10551)
* Er treedt een toepassingsfout op wanneer u op de knop Bewerken klikt nadat u alle voorinstellingen hebt geselecteerd via het selectievakje Voorinstellingen uitvoer in het pop-upvenster Snel genereren. (10388)
* Als op het tabblad Uitvoer in de webeditor meer voorinstellingen beschikbaar zijn, kan in de sectie Voorinstellingen niet verticaal worden geschoven en worden niet alle beschikbare voorinstellingen weergegeven. 9787
* Kan voorinstellingen niet verwijderen uit de uitvoerworkflow tijdens het publiceren via de Editor. 9100
* Peer-koppeling wordt weergegeven als normale tekst in plaats van als een koppeling op de gegenereerde pagina. (774)

## Bekend probleem

Adobe heeft het volgende bekende probleem voor AEM Guides 4.2-release geïdentificeerd:

* Gebruikers kunnen revisiebewerkingen zelfs uitvoeren nadat de revisietaak is voltooid.
