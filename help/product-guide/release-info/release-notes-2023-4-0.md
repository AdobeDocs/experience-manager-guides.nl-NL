---
title: Opmerkingen bij de release | Adobe Experience Manager Guides as a Cloud Service, release april 2023
description: Release van Adobe Experience Manager Guides as a Cloud Service in april 2023
exl-id: fa339eab-d3d0-4763-adbf-6411e39aa213
feature: Release Notes
role: Leader
source-git-commit: 6e23f52fc9124d0f07f8108da1b5fe574f553469
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 0%

---

# Release van Adobe Experience Manager Guides as a Cloud Service in april 2023

Deze versienota behandelt de verbeteringsinstructies, verenigbaarheidsmatrijs, en kwesties die in versie April 2023 van Adobe Experience Manager Guides (later als *worden bedoeld as a Cloud Service van AEM Guides*) worden bevestigd.

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, zie [&#x200B; wat in April 2023 versie van AEM Guides as a Cloud Service &#x200B;](whats-new-2023-4-0.md) nieuw is.

## Upgrade naar de release van april 2023

Voer de volgende stappen uit om uw huidige AEM Guides as a Cloud Service-installatie bij te werken:

1. Bekijk de Git-code van Cloud Services en schakel over naar de vertakking die is geconfigureerd in de Cloud Services-pijplijn die overeenkomt met de omgeving die u wilt upgraden.
2. Werk de eigenschap `<dox.version>` in het `/dox/dox.installer/pom.xml` -bestand van de Git-code voor Cloud Services bij naar 2023.4.249.
3. Leg de wijzigingen vast en voer de Cloud Services-pijplijn uit om naar de release van april 2023 van AEM Guides as a Cloud Service te upgraden.

## Stappen om de bestaande inhoud te indexeren (alleen als u een versie hebt die ouder is dan de release van AEM Guides as a Cloud Service in september)

Voer de volgende stappen uit om de bestaande inhoud te indexeren en de nieuwe tekst zoeken en vervangen op kaartniveau te gebruiken:

* Voer een POST-aanvraag uit op de server (met correcte verificatie) - `http://<server:port>/bin/guides/map-find/indexing` .
(Optioneel) U kunt specifieke paden van de kaarten doorgeven om deze te indexeren. Standaard worden alle kaarten geïndexeerd || Voorbeeld: `https://<Server:port>/bin/guides/map-find/indexing?paths=<map_path_in_repository>`)

* De API retourneert een jobId. Als u de status van de taak wilt controleren, kunt u een GET-aanvraag met taak-id naar hetzelfde eindpunt verzenden - `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}`
(Bijvoorbeeld: http://&lt;_localhost :8080_>/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c 42_678)

* Zodra de taak is voltooid, reageert het bovenstaande GET-verzoek met succes en vermeldt het of kaarten zijn mislukt. De met succes geïndexeerde kaarten kunnen van de serverlogboeken worden bevestigd.

## Compatibiliteitsmatrix

Deze sectie bevat een overzicht van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door de AEM Guides as a Cloud Service-release van april 2023.

### FrameMaker en FrameMaker Publishing Server

| AEM Guides als Cloud Release | FMPS | FrameMaker |
| --- | --- | --- |
| 2023,04,0 | Niet compatibel | 2022 of hoger |
| | | |


### Zuurstofaansluiting

| AEM Guides als Cloud Release | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2023,04,0 | 2.9-uuid-2 | 2.9-uuid-2 | 2,3 | 2,3 |
|  |  |  |  |  |



## Opgeloste problemen

De fouten die in verschillende gebieden zijn gecorrigeerd, worden hieronder weergegeven:

* Oorspronkelijke PDF | Het publiceren van inhoud die een outputklasse met steunen () heeft leidt tot een het publiceren bevriezing. (11596)
* Probleem doet zich voor bij het verplaatsen (slepen en neerzetten) in plaats van een bestaand lijstitem met Wijzigingen bijhouden ingeschakeld. (11570)
* Probleem doet zich voor bij het verplaatsen (slepen en neerzetten) als een nieuw lijstitem met Wijzigingen bijhouden ingeschakeld. (11569)
* Lijstitems inspringen of uitspringen werken niet zoals u had verwacht bij Wijzigingen bijhouden ingeschakeld. (11568)
* Als u inhoud toevoegt op een regel met Wijzigingen bijhouden ingeschakeld en vervolgens Wijzigingen bijhouden uitschakelt, wordt de inhoud niet daadwerkelijk uitgeschakeld. 11567
* Moeilijk om een list-item te slepen en neer te zetten, wordt tekst verplaatst in plaats van het list-item. (11566)
* Voltooide revisie wordt niet geopend in de modus Alleen-lezen. 11387
* Het probleem doet zich voor bij het zoeken naar de AEM-site (werkt niet meer dan 2-3 knooppunten op niveau). 11352
* Bij het ontwerpen in het element dat groen (Wijzigingen bijhouden) wordt weergegeven, wordt de nieuwe inhoud weergegeven als een wijziging in de track, ook al is de trackwijziging uitgeschakeld. 7021)

### Bekend probleem met tijdelijke oplossing

Adobe heeft het volgende bekende probleem voor de release van AEM Guides as a Cloud Service van april 2023 geïdentificeerd.

* Oorspronkelijke PDF | De oude metagegevens worden pas gevuld wanneer de uitvoervoorinstelling expliciet wordt geopend.
