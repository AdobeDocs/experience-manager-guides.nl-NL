---
title: Opmerkingen bij de release | Upgradeinstructies en opgeloste problemen in Adobe Experience Manager Guides, release 2025.02.0
description: Leer meer over de compatibiliteitsmatrix en hoe u een upgrade uitvoert naar de release van 2025.02.0 van Adobe Experience Manager Guides as a Cloud Service.
exl-id: 7b01be4c-031f-4153-8d6d-d6352e94be65
source-git-commit: 6e23f52fc9124d0f07f8108da1b5fe574f553469
workflow-type: tm+mt
source-wordcount: '1035'
ht-degree: 0%

---

# Upgrade-instructies voor de release van 2025.02.0

Dit artikel behandelt de upgrade-instructies en de compatibiliteitsmatrix voor de release 2025.02.0 van Adobe Experience Manager Guides as a Cloud Service.

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, mening [&#x200B; wat in de versie 2025.02.0 &#x200B;](whats-new-2025-02-0.md) nieuw is.

Voor de lijst van kwesties die in deze versie worden bevestigd, mening [&#x200B; Vaste kwesties in de 2025.02.0 versie &#x200B;](fixed-issues-2025-02-0.md).

## Compatibiliteitsmatrix

Deze sectie bevat een overzicht van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door de release 2025.02.0 van Experience Manager Guides as a Cloud Service.

### FrameMaker en FrameMaker Publishing Server

| Experience Manager Guides als Cloud Release | FMPS | FrameMaker |
| --- | --- | --- |
| 2025,02,0 | Niet compatibel | 2022 of hoger |
| | | |


### Zuurstofaansluiting

| Experience Manager Guides als Cloud Release | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2025,02,0 | 3,8-uuid 1 | 3,8-uuid 1 | 2,3 | 2,3 |
|  |  |  |  |  |


### Versie van basissjabloon

| Naam van componentenpakket | Versie van componenten | Sjabloonversie |
|---|---|---|
| Experience Manager Guides Components Content Package voor Cloud Service | guides-components.all-1.3.0 | aem-site-template-dxml-1.0.17 |


### Nieuwe sjabloonversie voor AEM-site

| Versie van componenten | Site-versie |
|---|---|
| guides-components.all-1.3.0 | aemg-sites-template-1.2.0 |


## Upgrade naar 2025.02.0-release

Experience Manager Guides wordt automatisch bijgewerkt bij het upgraden van de huidige (nieuwste) release van Experience Manager as a Cloud Service.

>[!NOTE]
>
> Als u de huidige (nieuwste) release hebt gebruikt, kunt u alle overschreven configuraties vergelijken met de nieuwste configuraties om de nieuwste functies te krijgen:
>- ui_config.json (kan zijn ingesteld in mapprofielen)


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

In de vorige reactie JSON bevat de sleutel `lockNodePath` het pad naar het knooppunt dat in de opslagplaats is gemaakt en dat naar de verzonden taak wijst. Deze wordt automatisch verwijderd als de taak is voltooid en u kunt naar dit knooppunt verwijzen voor de status van de taak.

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

   - Gebruik de instructies die in de *sectie van de Configuratie worden gegeven met voeten treedt* in installeer en vorm Adobe Experience Manager Guides as a Cloud Service, om het configuratiedossier tot stand te brengen.
   - Geef in het configuratiebestand de volgende gegevens (eigenschap) op om de optie `queryLimitReads` en `queryLimitInMemory` te configureren:

     | PID | Eigenschappensleutel | Waarde van eigenschap |
     |---|---|---|
     | org.apache.jackrabbit.oak.query.QueryEngineSettingsService | queryLimitReads | Waarde: 200000 Standaardwaarde: 100000 |
     | org.apache.jackrabbit.oak.query.QueryEngineSettingsService | queryLimitInMemory | Waarde: 200000 Standaardwaarde: 100000 |

1. Voer een POST-aanvraag uit op de server (met correcte verificatie) - `http://<server>//bin/guides/reports/upgrade` .

1. De API retourneert een jobId. Als u de status van de taak wilt controleren, kunt u een GET-aanvraag met taak-id naar hetzelfde eindpunt verzenden - `http://<server>/bin/guides/reports/upgrade?jobId= {jobId}`
(Bijvoorbeeld: `http://localhost:8080/bin/guides/reports/upgrade?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678`)

1. Zodra de taak is voltooid, reageert het vorige GET-verzoek met succes. Als de taak om een of andere reden mislukt, kan de fout worden gezien in serverlogboeken.

1. Terugkeren naar de standaardwaarde of vorige bestaande waarde van `queryLimitReads` als u deze hebt gewijzigd in stap 1.

### Stappen om de bestaande inhoud te indexeren om de nieuwe zoek- en vervangings- en onderwerpenlijst onder het tabblad Rapporten te gebruiken:

(Alleen als u een release hebt ontvangen vóór de release van Experience Manager Guides as a Cloud Service in juni 2023)

Voer de volgende stappen uit om de bestaande inhoud te indexeren en de nieuwe vondst en vervangt tekst op kaartniveau en onderwerpenlijst onder het rapportlusje te gebruiken:

1. Voer een POST-aanvraag uit op de server (met correcte verificatie) - `http://<server:port>/bin/guides/map-find/indexing` . (Optioneel) U kunt specifieke paden van de kaarten doorgeven om deze te indexeren, standaard worden alle kaarten geïndexeerd|| Voorbeeld: `https://<Server:port>/bin/guides/map-find/indexing?paths=<path of the MAP in repository>`)

1. U kunt ook een hoofdmap doorgeven om de DITA-kaarten van een specifieke map (en de bijbehorende submappen) te indexeren. Bijvoorbeeld `http://<server:port\>/bin/guides/map-find/indexing?root=/content/dam/test` . Wanneer zowel de parameter paths als de hoofdparameter worden doorgegeven, wordt alleen de parameter paths gebruikt.

1. De API retourneert een jobId. Als u de status van de taak wilt controleren, kunt u een GET-aanvraag met taak-id naar hetzelfde eindpunt verzenden - `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}` (bijvoorbeeld: `http://localhost:8080/bin/guides/reports/upgrade?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678`)

1. Nadat de taak is voltooid, reageert het vorige GET-verzoek met succes en wordt vermeld of kaarten zijn mislukt. De met succes geïndexeerde kaarten kunnen van serverlogboeken worden bevestigd.

### Stappen voor het afhandelen van het `'fmdita rewriter'` -conflict

Experience Manager Guides heeft de module van de a [**douane die herschrijver**](../cs-install-guide/conf-output-generation.md#custom-rewriter) voor de behandeling van de verbindingen in het geval van dwars-kaarten (verbindingen tussen de onderwerpen van twee verschillende kaarten) worden geproduceerd.

Als u nog een aangepaste schrijfbewerking voor tekenreeksen in uw codebase hebt, gebruikt u een `'order'` -waarde groter dan 50, omdat Experience Manager Guides anders `'order'` 50 gebruikt. Als u dit wilt overschrijven, hebt u een waarde > 50 nodig. Voor meer details, mening [&#x200B; Output die pijplijnen herschrijft &#x200B;](https://sling.apache.org/documentation/bundles/output-rewriting-pipelines-org-apache-sling-rewriter.html).

Aangezien de waarde van `'order'` tijdens deze upgrade is gewijzigd van 1000 in 50, moet u eventueel de bestaande aangepaste rewriter samenvoegen met `fmdita-rewriter` .

### Stappen voor het uitvoeren van B-structuurmigratie voor inhoudsfragmenten

Als er geen referenties worden weergegeven voor inhoudsfragmenten, kunt u de trigger HIT om de migratietaak te starten:

POST:

```
http://localhost:4503/bin/guides/script/start?jobType=cf-reference-store-btree-migration
```


Reactie:

```
{
"msg": "Job is successfully submitted and lock node is created for future reference",
"lockNodePath": "/var/dxml/executor-locks/cf-reference-store-btree-migration/1683190032886",
"status": "SCHEDULED"
}
```

In de vorige reactie, JSON, houdt de sleutel `lockNodePath` de weg aan de knoop die in de bewaarplaats wordt gecreeerd, die aan de voorgelegde baan richt. Deze wordt automatisch verwijderd als de taak is voltooid. U kunt naar dit knooppunt verwijzen voor de status van de taak.

Wacht tot deze taak is voltooid voordat u verdergaat met de volgende stappen.

>[!NOTE]
>
>Controleer of het knooppunt nog aanwezig is en wat de status van de taak is.

GET:

```
http://<aem_domain>/var/dxml/executor-locks/cf-reference-store-btree-migration/1683190032886.json
```
