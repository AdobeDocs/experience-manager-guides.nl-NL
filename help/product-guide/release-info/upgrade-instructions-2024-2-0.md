---
title: Opmerkingen bij de release | Upgradeinstructies en opgeloste problemen in Adobe Experience Manager Guides, release 2024.2.0
description: Leer meer over de compatibiliteitsmatrix en hoe u een upgrade uitvoert naar de release 2024.2.0 van Adobe Experience Manager Guides as a Cloud Service.
exl-id: 7aaa4317-eb96-4fff-8a45-b38b9dfc234a
source-git-commit: e40ebf4122decc431d0abb2cdf1794ea704e5496
workflow-type: tm+mt
source-wordcount: '866'
ht-degree: 0%

---

# Upgrade-instructies voor de release van 2024.2.0

Dit artikel behandelt de upgrade-instructies en de compatibiliteitsmatrix voor de release van Adobe Experience Manager Guides as a Cloud Service in 2024.2.0.

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, mening [&#x200B; wat in de versie 2024.2.0 &#x200B;](whats-new-2024-2-0.md) nieuw is.

Voor de lijst van kwesties die in deze versie zijn bevestigd, mening [&#x200B; Vaste kwesties in de versie 2024.2.0 &#x200B;](fixed-issues-2024-2-0.md).


## Compatibiliteitsmatrix

In deze sectie wordt een overzicht gegeven van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door de release 2024.2.0 van Experience Manager Guides as a Cloud Service.

### FrameMaker en FrameMaker Publishing Server

| Experience Manager Guides als Cloud Release | FMPS | FrameMaker |
| --- | --- | --- |
| 2024,2,0 | Niet compatibel | 2022 of hoger |
| | | |


### Zuurstofaansluiting

| Experience Manager Guides als Cloud Release | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2024,2,0 | 3,5-uuid 1 | 3,5-uuid 1 | 2,3 | 2,3 |
|  |  |  |  |


### Versie van basissjabloon

| Naam van componentenpakket | Versie van componenten | Sjabloonversie |
|---|---|---|
| Experience Manager Guides Components Content Package voor Cloud Service | dxml-components.all-1.2.2 | aem-site-template-dxml.all-1.0.15 |

## Upgrade naar 2024.2.0-release

Experience Manager Guides wordt automatisch bijgewerkt bij het upgraden van de huidige (nieuwste) release van Experience Manager as a Cloud Service.


Voer de volgende stappen uit voor Experience Manager Guides as a Cloud Service als u dit nog niet eerder hebt gedaan voor uw bestaande release:

### Stappen om de trigger van een script via een servlet in te schakelen

(Alleen als u een release hebt ontvangen vóór de release van Experience Manager Guides as a Cloud Service in juni 2023)

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

In de vorige reactie JSON bevat de sleutel `lockNodePath` het pad naar het knooppunt dat in de opslagplaats is gemaakt en dat naar de verzonden taak wijst. Het wordt automatisch verwijderd als de taak is voltooid en u kunt naar dit knooppunt verwijzen voor de status van de taak.

Wacht tot deze taak is voltooid voordat u verdergaat met de volgende stappen.

>[!NOTE]
>
> Controleer of het knooppunt nog aanwezig is en wat de status van de taak is.

```
GET
http://<aem_domain>/var/dxml/executor-locks/translation-map-upgrade/1683190032886.json
```

### Stappen om de bestaande inhoud te posten om het verbroken koppelingsrapport te gebruiken

(Alleen als u een release hebt ontvangen vóór de release van Experience Manager Guides as a Cloud Service in juni 2023)

Voer de volgende stappen uit voor de nabewerking van de bestaande inhoud en het gebruik van het nieuwe verbroken koppelingsrapport:

1. (Optioneel) Als er zich meer dan 100.000 DITA-bestanden in het systeem bevinden, werkt u de `queryLimitReads` en `queryLimitInMemory` under `org.apache.jackrabbit.oak.query.QueryEngineSettingsService` naar een hogere waarde bij (een waarde die groter is dan het aantal aanwezige elementen, bijvoorbeeld 200.000) en herstelt u de bestanden.

   - Gebruik de instructies die in de *sectie van de Configuratie worden gegeven met voeten treedt* in installeer en vorm as a Cloud Service Adobe Experience Manager Guides, om het configuratiedossier tot stand te brengen.
   - Geef in het configuratiebestand de volgende gegevens (eigenschap) op om de optie `queryLimitReads` en `queryLimitInMemory` te configureren:

     | PID | Eigenschappensleutel | Waarde van eigenschap |
     |---|---|---|
     | org.apache.jackrabbit.oak.query.QueryEngineSettingsService | queryLimitReads | Waarde: 200000 Standaardwaarde: 100000 |
     | org.apache.jackrabbit.oak.query.QueryEngineSettingsService | queryLimitInMemory | Waarde: 200000 Standaardwaarde: 100000 |

1. Voer een verzoek van de POST op de server uit (met correcte authentificatie) - `http://<server>//bin/guides/reports/upgrade`.

1. De API retourneert een jobId. Als u de status van de taak wilt controleren, kunt u een aanvraag voor een GET met taak-id naar hetzelfde eindpunt verzenden - `http://<server>/bin/guides/reports/upgrade?jobId= {jobId}`
(Bijvoorbeeld: `http://localhost:8080/bin/guides/reports/upgrade?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678`)

1. Zodra de baan wordt voltooid, antwoordt het vorige verzoek van de GET met succes. Als de taak om een of andere reden mislukt, kan de fout worden gezien in serverlogboeken.

1. Terugkeren naar de standaardwaarde of vorige bestaande waarde van `queryLimitReads` als u deze hebt gewijzigd in stap 1.

### Stappen om de bestaande inhoud te indexeren om de nieuwe zoek- en vervangings- en onderwerpenlijst onder het tabblad Rapporten te gebruiken:

(Alleen als u een release hebt ontvangen vóór de release van Experience Manager Guides as a Cloud Service in juni 2023)

Voer de volgende stappen uit om de bestaande inhoud te indexeren en de nieuwe vondst en vervangt tekst op kaartniveau en onderwerpenlijst onder het rapportlusje te gebruiken:

1. Voer een verzoek van de POST op de server uit (met correcte authentificatie) - `http://<server:port>/bin/guides/map-find/indexing`. (Optioneel) U kunt specifieke paden van de kaarten doorgeven om deze te indexeren. Standaard worden alle kaarten geïndexeerd|| Bijvoorbeeld : `https://<Server:port>/bin/guides/map-find/indexing?paths=<path of the MAP in repository>`)

1. De API retourneert een jobId. Als u de status van de taak wilt controleren, kunt u een aanvraag van een GET met taak-id naar hetzelfde eindpunt verzenden - `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}` (bijvoorbeeld: `http://localhost:8080/bin/guides/reports/upgrade?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678`)

1. Zodra de baan wordt voltooid, antwoordt het vorige verzoek van de GET met succes. Als de taak om een of andere reden mislukt, kan de fout worden gezien in de serverlogboeken.

1. Terugkeren naar de standaardwaarde of vorige bestaande waarde van queryLimitReads als u deze hebt gewijzigd in stap 1.

### Stappen voor het afhandelen van het `'fmdita rewriter'` -conflict

Experience Manager Guides heeft de module van de a [**douane die herschrijver**](../cs-install-guide/conf-output-generation.md#custom-rewriter) voor de behandeling van de verbindingen in het geval van dwars-kaarten (verbindingen tussen de onderwerpen van twee verschillende kaarten) worden geproduceerd.

Als u nog een aangepaste schrijfbewerking voor tekenreeksen in uw codebase hebt, gebruikt u een `'order'` -waarde groter dan 50, omdat Experience Manager Guides anders `'order'` 50 gebruikt.  Als u dit wilt overschrijven, hebt u een waarde > 50 nodig. Voor meer details, mening [&#x200B; Output die pijplijnen herschrijft &#x200B;](https://sling.apache.org/documentation/bundles/output-rewriting-pipelines-org-apache-sling-rewriter.html).

Aangezien de waarde van `'order'` tijdens deze upgrade is gewijzigd van 1000 in 50, moet u eventueel de bestaande aangepaste rewriter samenvoegen met `'fmdita-rewriter'` .
