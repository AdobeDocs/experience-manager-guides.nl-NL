---
title: Opmerkingen bij de release | Adobe Experience Manager Guides as a Cloud Service, release maart 2023
description: Release van Adobe Experience Manager Guides as a Cloud Service in maart
exl-id: 6a0bba92-7d7d-4b20-ad46-0eacc91268da
feature: Release Notes
role: Leader
source-git-commit: 6e23f52fc9124d0f07f8108da1b5fe574f553469
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 0%

---

# Release van Adobe Experience Manager Guides as a Cloud Service in maart 2023

Deze versienota behandelt de verbeteringsinstructies, verenigbaarheidsmatrijs, en kwesties die in versie Maart 2023 van Adobe Experience Manager Guides (later als *worden bedoeld as a Cloud Service van AEM Guides*) worden bevestigd.

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, zie [ wat in Maart 2023 versie van AEM Guides as a Cloud Service ](whats-new-2023-3-0.md) nieuw is.

## Upgrade naar release maart 2023

Voer de volgende stappen uit om uw huidige AEM Guides as a Cloud Service-installatie bij te werken:

1. Bekijk de Git-code van Cloud Services en schakel over naar de vertakking die is geconfigureerd in de Cloud Services-pijplijn die overeenkomt met de omgeving die u wilt upgraden.
1. Werk de eigenschap `<dox.version>` in het `/dox/dox.installer/pom.xml` -bestand van de Git-code voor Cloud Services bij naar 2023.3.242.
1. Leg de wijzigingen vast en voer de Cloud Services-pijplijn uit om naar de release van maart 2023 van AEM Guides as a Cloud Service te upgraden.

## Stappen om de bestaande inhoud te indexeren (alleen als u een versie hebt die ouder is dan de release van AEM Guides as a Cloud Service in september)

Voer de volgende stappen uit om de bestaande inhoud te indexeren en de nieuwe tekst zoeken en vervangen op kaartniveau te gebruiken:

* Voer een POST-aanvraag uit op de server (met correcte verificatie) - `http://<server:port>/bin/guides/map-find/indexing` .
(Optioneel) U kunt specifieke paden van de kaarten doorgeven om deze te indexeren. Standaard worden alle kaarten geïndexeerd || Voorbeeld: `https://<Server:port>/bin/guides/map-find/indexing?paths=<map_path_in_repository>`)

* De API retourneert een jobId. Als u de status van de taak wilt controleren, kunt u een GET-aanvraag met taak-id naar hetzelfde eindpunt verzenden - `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}`
(Bijvoorbeeld: http://&lt;_localhost :8080_>/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c 42_678)

* Zodra de taak is voltooid, reageert het bovenstaande GET-verzoek met succes en vermeldt het of kaarten zijn mislukt. De met succes geïndexeerde kaarten kunnen van de serverlogboeken worden bevestigd.

## Compatibiliteitsmatrix

In deze sectie wordt een overzicht gegeven van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door de release van AEM Guides as a Cloud Service van maart 2023.

### FrameMaker en FrameMaker Publishing Server

| AEM Guides als Cloud Release | FMPS | FrameMaker |
| --- | --- | --- |
| 2023,03,0 | Niet compatibel | 2022 of hoger |
| | | |


### Zuurstofaansluiting

| AEM Guides als Cloud Release | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2023,03,0 | 2.9-uuid-2 | 2.9-uuid-2 | 2,3 | 2,3 |
|  |  |  |  |  |

## Opgeloste problemen

De fouten die in verschillende gebieden zijn gecorrigeerd, worden hieronder weergegeven:

* Het PDF-proces voor downloaden werkt niet correct in de webeditor. 11496
* JSON-uitvoer | Metagegevens met een eigenschap toewijzen die de waarde `"value in spaces and double quotes"` heeft, leiden tot een publicatiefout. 11438
* De toevoeging voor audio en videodossiers van verschillende media ontbreekt in het formaat van YouTube onder het **Multimedia van het Tussenvoegsel** pictogram. 11320
* Validatiefout treedt op wanneer een kaart wordt gemaakt met behulp van de sjabloon met een speciaal titelelement. 11212
* Oorspronkelijke PDF | voetnoot in de tabelkoptekst leidt tot vette en gecentreerde tekst in de bijbehorende voettekst op de pagina in de PDF-uitvoer. 10610
>[!NOTE]
>
>Als u de Native PDF-wijziging wilt weerspiegelen, verwijdert u de PDF-map op /content/dam/dita-templates en voert u een upgrade uit naar de nieuwste build. 10610

### Bekend probleem met tijdelijke oplossing

Adobe heeft het volgende bekende probleem voor de release van AEM Guides as a Cloud Service in maart 2023 geïdentificeerd.

* Gebruikers kunnen geen versie van een gedupliceerd element opslaan of maken.

**Oplossing**: Alvorens om het even welke veranderingen in de dubbele activa aan te brengen herverwerken het van Assets UI.
