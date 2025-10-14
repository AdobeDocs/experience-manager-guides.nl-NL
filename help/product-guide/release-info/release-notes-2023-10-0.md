---
title: Opmerkingen bij de release | Upgradeinstructies en opgeloste problemen in Adobe Experience Manager Guides, release van oktober 2023
description: Meer informatie over de opgeloste problemen en hoe u een upgrade uitvoert naar de release van oktober 2023 van Adobe Experience Manager Guides as a Cloud Service
exl-id: 536d2ec2-31a0-4533-9c29-16a27525acca
feature: Release Notes
role: Leader
source-git-commit: 6d8c01f20f7b59fed92c404561b647d9ebecb050
workflow-type: tm+mt
source-wordcount: '1045'
ht-degree: 0%

---

# Release van Adobe Experience Manager Guides as a Cloud Service in oktober 2023

Deze versienota behandelt de verbeteringsinstructies, verenigbaarheidsmatrijs, en kwesties die in versie Oktober 2023 van Adobe Experience Manager Guides worden bevestigd (later die als *wordt bedoeld AEM Guides as a Cloud Service*).

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, zie [&#x200B; wat in de versie van Oktober 2023 van AEM Guides as a Cloud Service &#x200B;](whats-new-2023-10-0.md) nieuw is.

## Upgrade naar oktober 2023

Voer de volgende stappen uit om uw huidige AEM Guides as a Cloud Service-installatie bij te werken:

1. Controle uit de code van Git van Cloud Servicen en schakelaar aan de tak die in de pijpleiding van Cloud Servicen wordt gevormd die aan het milieu beantwoordt dat u wilt bevorderen.
2. Werk de eigenschap `<dox.version>` in het `/dox/dox.installer/pom.xml` -bestand van de Git-code van de Cloud Service bij naar 2023.10.0.373.
3. Leg de wijzigingen vast en voer de pijplijn met Cloud Servicen uit om te upgraden naar de release van AEM Guides as a Cloud Service in oktober 2023.

## Stappen om de trigger van een script via een servlet in te schakelen

(Alleen als u een versie hebt die ouder is dan de release van AEM Guides as a Cloud Service in juni 2023)

Nadat u de installatie hebt voltooid, kunt u ervoor kiezen om de trigger te HIT om de vertaaltaak te starten:

POST:

```
http://localhost:4503/bin/guides/script/start?jobType=translation-map-upgrade
```

Reactie:

```
{
"msg": "Job is successfully submitted and lock node is created for future reference",
"lockNodePath": "/var/dxml/executor-locks/translation-map-upgrade/1683190032886",
"status": "SCHEDULED"
}
```

In de vorige reactie JSON bevat de sleutel `lockNodePath` het pad naar het knooppunt dat in de opslagplaats is gemaakt en dat naar de verzonden taak wijst. Het wordt automatisch verwijderd als de taak is voltooid. Tot dan kunt u naar dit knooppunt verwijzen voor de huidige status van de taak.

Wacht tot deze taak is voltooid voordat u verdergaat met de volgende stappen.

>[!NOTE]
>
> Controleer of het knooppunt nog aanwezig is en wat de status van de taak is.

```
GET
http://<aem_domain>/var/dxml/executor-locks/translation-map-upgrade/1683190032886.json
```

## Stappen om de bestaande inhoud te posten om het verbroken koppelingsrapport te gebruiken

(Alleen als u een versie hebt die ouder is dan de release van AEM Guides as a Cloud Service in juni 2023)

Voer de volgende stappen uit voor de nabewerking van de bestaande inhoud en het gebruik van het nieuwe verbroken koppelingsrapport:

1. (Optioneel) Als er zich meer dan 100.000 DITA-bestanden in het systeem bevinden, werkt u `queryLimitReads` under `org.apache.jackrabbit.oak.query.QueryEngineSettingsService` bij tot een hogere waarde (een waarde die groter is dan het aantal aanwezige elementen, bijvoorbeeld 200.000) en herstelt u deze vervolgens.

   - Gebruik de instructies die in de *sectie van de Configuratie worden gegeven met voeten treedt* in installeer en vorm as a Cloud Service Adobe Experience Manager Guides, om het configuratiedossier tot stand te brengen.
   - In het configuratiedossier, verstrek de volgende (bezit) details om de queryLimitReads optie te vormen:

     | PID | Eigenschappensleutel | Waarde van eigenschap |
     |---|---|---|
     | org.apache.jackrabbit.oak.query.QueryEngineSettingsService | queryLimitReads | Waarde: 200000 Standaardwaarde: 100000 |

1. Voer een verzoek van de POST op de server uit (met correcte authentificatie) - `http://<server:port>//bin/guides/reports/upgrade`.

1. De API retourneert een jobId. Als u de status van de taak wilt controleren, kunt u een aanvraag voor een GET met taak-id naar hetzelfde eindpunt verzenden - `http://<server:port>/bin/guides/reports/upgrade?jobId= {jobId}`
(Bijvoorbeeld: `http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678`)

1. Zodra de baan wordt voltooid, antwoordt het vorige verzoek van de GET met succes. Als de taak om een of andere reden mislukt, kan de fout worden gezien in serverlogboeken.

1. Keer terug naar de standaardwaarde of vorige bestaande waarde van `queryLimitReads` als u deze in stap 1 hebt gewijzigd.

## Stappen om de bestaande inhoud te indexeren om de nieuwe zoek- en vervangings- en onderwerpenlijst onder het tabblad Rapporten te gebruiken:

(Alleen als u een versie hebt die ouder is dan de release van AEM Guides as a Cloud Service in juni 2023)

Voer de volgende stappen uit om de bestaande inhoud te indexeren en de nieuwe vondst en vervangt tekst op kaartniveau en onderwerpenlijst onder het rapportlusje te gebruiken:

1. Voer een POST-aanvraag uit op de server \(met correcte verificatie\) - `http://<server:port\>/bin/guides/map-find/indexing` . (Optioneel: u kunt specifieke paden van de kaarten doorgeven om deze te indexeren. Standaard worden alle kaarten geïndexeerd \|\| Bijvoorbeeld : `https://<Server:port\>/bin/guides/map-find/indexing?paths=<map\_path\_in\_repository\>`)

1. U kunt ook een hoofdmap doorgeven om de DITA-kaarten van een specifieke map (en de bijbehorende submappen) te indexeren. Bijvoorbeeld `http://<server:port\>/bin/guides/map-find/indexing?root=/content/dam/test` . Wanneer zowel de parameter paths als de hoofdparameter worden doorgegeven, wordt alleen de parameter paths gebruikt.

1. De API retourneert een jobId. Als u de status van de taak wilt controleren, kunt u een aanvraag van een GET met taak-id naar hetzelfde eindpunt verzenden - `http://<server:port\>/bin/guides/map-find/indexing?jobId=\{jobId\}`\(bijvoorbeeld: `http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42`\)


1. Zodra de baan wordt voltooid, antwoordt het vorige verzoek van de GET met succes en vermeld als om het even welke kaarten ontbrak. De met succes geïndexeerde kaarten kunnen van de serverlogboeken worden bevestigd.

## Compatibiliteitsmatrix

Deze sectie bevat een overzicht van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door de AEM Guides as a Cloud Service oktober 2023-release.

### FrameMaker en FrameMaker Publishing Server

| AEM Guides als Cloud Release | FMPS | FrameMaker |
| --- | --- | --- |
| 2023 10,0 | Niet compatibel | 2022 of hoger |
| | | |


### Zuurstofaansluiting

| AEM Guides als Cloud Release | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2023 10,0 | 3.2-uuid 5 | 3.2-uuid 5 | 2,3 | 2,3 |
|  |  |  |  |


### Versie van basissjabloon

| Naam van componentenpakket | Versie van componenten | Sjabloonversie |
|---|---|---|
| AEM Guides Components Content Package voor Cloud Service | dxml-components.all-1.2.2 | aem-site-template-dxml.all-1.0.15 |

## Opgeloste problemen

De fouten die in verschillende gebieden zijn gecorrigeerd, worden hieronder weergegeven:

### Authoring

- De uren van de middag worden niet geplaatst in de **Datum** voor de verwezenlijking van basislijnen. 12712
- Kan de JSON-code niet plakken in het `<codeblock>` -element van de webeditor. 12326
- Niet-opgeslagen versiewijzigingen en de indicatoren daarvoor worden niet weergegeven voor grote bestanden. (11784)
- Tijdens het bewerken in de Koreaanse taal verandert het eerste teken in de standaardwaarde. 10049


### Publiceren

- Native PDF | De orde van de onderwerpen is niet vast wanneer de output van de PDF wordt geproduceerd. 13157
- Oorspronkelijke PDF| Geen standaardstijlmarkering is beschikbaar voor `<p>` element. (12559)
- Native PDF | Inline stijlen die worden toegepast op het inhoudsgebied, worden niet toegepast op de onderwerpen voor- en achtermaterie. 13510
- Het kenmerk `DeliveryTarget` wordt niet doorgegeven bij het genereren van de AEM Site-uitvoer.  13132
- Het **Publish** werkschema wordt geplakt terwijl het produceren van AEM output van de Plaats voor inhoud met bepaalde fouten. 12000

### Beheer

- Versiegeschiedenis wordt niet weergegeven, zelfs niet als de eigenschap `dc:format` niet aanwezig is voor een element. 10463


### Controleren

- In de revisie over een onderwerp worden onjuiste opmerkingen weergegeven. 13453



### Vertaling

- De basislijn die van **wordt uitgevoerd Vertaling** dashboard ontbreekt en opent niet in de doeltaal. (13466)

- Er worden nieuwe vertaalprojecten gemaakt in plaats van nieuwe banen toe te voegen aan de geselecteerde bestaande vertaalprojecten.  10214

## Bekend probleem

Adobe heeft de volgende bekende kwestie voor de release van oktober 2023 geïdentificeerd.

- Opnieuw publiceren van inhoudsfragment mislukt.
