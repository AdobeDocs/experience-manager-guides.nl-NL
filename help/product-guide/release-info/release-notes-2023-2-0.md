---
title: Opmerkingen bij de release | Adobe Experience Manager Guides as a Cloud Service, release februari 2023
description: Release van Adobe Experience Manager Guides as a Cloud Service in februari
exl-id: c639b136-11ed-4a8b-a595-4bb5da879747
feature: Release Notes
role: Leader
source-git-commit: 6d8c01f20f7b59fed92c404561b647d9ebecb050
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 0%

---

# Release van Adobe Experience Manager Guides as a Cloud Service in februari 2023

Deze versienota behandelt de verbeteringsinstructies, verenigbaarheidsmatrijs, en kwesties die in versie Februari 2023 van Adobe Experience Manager Guides (later als *worden bedoeld AEM Guides as a Cloud Service*) worden bevestigd.

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, zie [&#x200B; wat in de versie van februari 2023 van AEM Guides as a Cloud Service &#x200B;](whats-new-2023-2-0.md) nieuw is.

## Upgrade naar de release van februari 2023

Voer de volgende stappen uit om uw huidige AEM Guides as a Cloud Service-installatie bij te werken:
1. Controle uit de code van Git van Cloud Servicen en schakelaar aan de tak die in de pijpleiding van Cloud Servicen wordt gevormd die aan het milieu beantwoordt dat u wilt bevorderen.
2. Werk de eigenschap `<dox.version>` in het `/dox/dox.installer/pom.xml` -bestand van de Git-code van de Cloud Service bij naar 2023.2.235.
3. Leg de wijzigingen vast en voer de pijplijn met Cloud Servicen uit om te upgraden naar de release van AEM Guides as a Cloud Service in februari 2023.

## Stappen om de bestaande inhoud te indexeren (Alleen als u een versie hebt die ouder is dan de release van AEM Guides as a Cloud Service in september)

Voer de volgende stappen uit om de bestaande inhoud te indexeren en de nieuwe tekst zoeken en vervangen op kaartniveau te gebruiken:

* Voer een verzoek van de POST op de server uit (met correcte authentificatie) - `http://<server:port>/bin/guides/map-find/indexing`.
(Optioneel) U kunt specifieke paden van de kaarten doorgeven om deze te indexeren. Standaard worden alle kaarten geïndexeerd || Voorbeeld: `https://<Server:port>/bin/guides/map-find/indexing?paths=<map_path_in_repository>`)

* De API retourneert een jobId. Als u de status van de taak wilt controleren, kunt u een aanvraag voor een GET met taak-id naar hetzelfde eindpunt verzenden - `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}`
(Bijvoorbeeld: http://&lt;_localhost:8080_>/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c183 79f11c42_678)

* Als de taak is voltooid, reageert het bovenstaande verzoek van de GET met succes en vermeldt u of kaarten zijn mislukt. De met succes geïndexeerde kaarten kunnen van de serverlogboeken worden bevestigd.

## Compatibiliteitsmatrix

Deze sectie bevat een overzicht van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door de AEM Guides-release van as a Cloud Service februari 2023.

### FrameMaker en FrameMaker Publishing Server

| AEM Guides als Cloud Release | FMPS | FrameMaker |
| --- | --- | --- |
| 2023,02,0 | Niet compatibel | 2022 of hoger |
| | | |

*Basislijn en voorwaarden die in AEM zijn gemaakt, worden vanaf 2020.2 ondersteund in FMPS-releases.

### Zuurstofaansluiting

| AEM Guides als Cloud Release | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2023,02,0 | 2,8-uuid-8 | 2,8-uuid-8 | 2,3 | 2,3 |
|  |  |  |  |

## Opgeloste problemen

De fouten die in verschillende gebieden zijn gecorrigeerd, worden hieronder weergegeven:

### Authoring

* Wijzigingen in de HTML van de webeditor veroorzaken problemen met `<dl>` en `<dlentry>` . (1024)
* Sommige kenmerken worden niet behandeld als voorwaardelijk en veroorzaken problemen. 10895
* Drie niveaus of meer geneste `<indexterm>` zijn niet genest in native PDF-export. (10799)
* De inhoud verdwijnt in de hoofdtekst van een taak bij het schakelen van de weergave Auteur naar de weergave Source. 10735
* Opmerkingen voor revisies worden verkeerd geplaatst in een revisietaak. 10625
* **ongedaan maken** of **opnieuw** werkt niet correct aan sommige dossiers. 10373
* Aangepaste metagegevens blijven niet behouden bij kopiëren en plakken. 10367
* Met de optie Ongedaan maken in de XML-editor komt de gebruiker boven aan de pagina. 10091
* Node-eigenschappen worden verwijderd na kopiëren en plakken van een element. 10053
* mimeType is hardcoded voor DITA activa verwezenlijking en update. 8979
* De naam van de maker van de versie in Versiehistorie is &quot;fmdita-servicegebruiker&quot; voor de bestanden die zijn geüpload via de gebruikersinterface van Assets. 8910
* Inhoudsfragmenten kunnen niet worden gekopieerd en geplakt wanneer AEM Guides op Cloud wordt geïnstalleerd. 11315
* Browser (de Redacteur van het Web) bevriest bij het laden van inhoud met douaneschema. (1121)

### Beheer

* Het kopiëren van een DITA-kaart-element (van de Asset UI) veroorzaakt onjuiste basislijnen in het gekopieerde element. 11218
* Er wordt geen waarschuwingsbericht weergegeven bij het uploaden van een bestand dat groter is dan de limiet die is toegestaan in AEM (standaard 2 GB). 10817
* Web Editor-basislijn | Het gedrag van de Meest recente kolom is verschillend in het nieuwe basislijndashboard binnen de Redacteur van het Web. 10808
* Vertaling | De vertaaltaak wordt niet gestart vanwege ongeldige /libs/fmdita/i18n/ja.json. 10543
* Vertaling | Er is een fout opgetreden in een bereikvertaalproject dat is gemaakt op het vertaaldashboard (Menselijke vertaling). 10526
* Vertaling | Post-verwerking wordt geblokkeerd voor de gehele taalmap waarvan de middelen aanwezig zijn in een actief vertaalproject. (1032)
* Er worden meerdere pop-ups weergegeven voor elk element als de versie wordt gewijzigd en opgeslagen in de basislijneditor. 10399
* Sessieklek treedt op om `com.day.cq.search.impl.builder.QueryBuilderImpl.createResourceResolver(QueryBuilderImpl.java:210)` . 10279

### Publiceren

* De regeneratie van het onderwerp werkt niet voor sommige scenario&#39;s. 10635
* De luisteraar van de uitgever toont niet de gevraagde gegevens in info- logboeken, en het bevat ook sommige junk logboeken.(10567)
* Native PDF | Bij het maken van een uitvoervoorinstelling met de optie Toevoegen aan mapprofiel mislukt het genereren van de PDF met een Null-aanwijzer. 10950
* Native PDF | Er treden problemen op bij het roteren van de tabelkop. (10555)
* Native PDF | Geneste `<indexterm>` zijn niet genest bij native PDF-export. 10521
* Native PDF | Geneste topicref in aanhangsels wordt allen omgezet aan h1 in tijdelijke HTML. 10454
* Het publiceren van de basislijn ontbreekt voor PDF die gebruikend FrameMaker Publishing Server 2020 wordt geproduceerd. (10551)
* Native PDF | Als u `xref` toevoegt aan een afbeelding, wordt de afbeelding op de gegenereerde PDF niet weergegeven. 11346
* Native PDF | Met de tag Afbeelding wordt het kenmerk display-inline toegevoegd aan alle afbeeldingen. 10653
* Native PDF | Conceptopmerkingen worden standaard verborgen in de gegenereerde uitvoer. 10560
* Native PDF | navtitle wordt niet geëerd voor topichead . 10509
