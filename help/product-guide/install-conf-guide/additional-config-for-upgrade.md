---
title: Aanvullende configuratie voor de upgrade van de cloudservice
description: Meer informatie over de extra configuratie voor de upgrade van de cloudservice
source-git-commit: 453da51a42984b912547570f2e1de70806b41171
workflow-type: tm+mt
source-wordcount: '849'
ht-degree: 0%

---

# Aanvullende configuratie voor het upgraden van AEM Guides als Cloud Service

>[!INFO]
>
>Dit artikel is van toepassing als u aangepaste instellingen voor mapprofielen hebt geconfigureerd (`ui_config.json`). Controleer na elke upgrade de instellingen en wijzig deze zo nodig om ervoor te zorgen dat deze compatibel zijn met de meest recente wijzigingen.

Afhankelijk van de versie waarvan u een upgrade uitvoert, zijn mogelijk aanvullende configuratiestappen vereist om de wijzigingen te integreren die zijn geïntroduceerd in nieuwere Cloud Service-versies.

Sommige configuraties zijn alleen van toepassing op specifieke versies. Zorg ervoor dat u naar de onderstaande configuratiesecties verwijst en pas de vereiste configuraties toe die van toepassing zijn op de configuratie.

## Stappen om zoekfilters toe te passen op DITAVAL-bestanden voor alle uitvoervoorinstellingen

Werk ui_config.json bij om ervoor te zorgen dat filters correct werken. Verander de eigenschappen die onder **worden vermeld browseFilters** > **niet-DITA dossiers** > **Ditaval Dossiers** zoals hieronder getoond:

```
{
  "title": "Ditaval Files",
  "property": "LOWER_NAME",
  "operation": "like",
  "value": ".ditaval"
}
```

## Stappen voor het uitvoeren van B-structuurmigratie voor inhoudsfragmenten

Als er geen verwijzingen worden weergegeven voor inhoudsfragmenten, kunt u ervoor kiezen de migratietaak uit te voeren:

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

## Stappen voor het afhandelen van het `'fmdita rewriter'` -conflict

Experience Manager Guides heeft de module van de a [**douane die herschrijver**](../install-conf-guide/conf-output-generation.md#custom-rewriter) voor de behandeling van de verbindingen in het geval van dwars-kaarten (verbindingen tussen de onderwerpen van twee verschillende kaarten) worden geproduceerd.

Als u nog een aangepaste schrijfbewerking voor tekenreeksen in uw codebase hebt, gebruikt u een `'order'` -waarde groter dan 50, omdat Experience Manager Guides anders `'order'` 50 gebruikt. Als u dit wilt overschrijven, hebt u een waarde > 50 nodig. Voor meer details, mening [&#x200B; Output die pijplijnen herschrijft &#x200B;](https://sling.apache.org/documentation/bundles/output-rewriting-pipelines-org-apache-sling-rewriter.html).

Aangezien de waarde van `'order'` tijdens deze upgrade is gewijzigd van 1000 in 50, moet u eventueel de bestaande aangepaste rewriter samenvoegen met `fmdita-rewriter` .

## Configuraties die van toepassing zijn op versies die dateren van vóór juni 2023

De volgende configuraties zijn alleen vereist als u een versie van Experience Manager Guides as a Cloud Service gebruikt die vóór juni 2023 is uitgebracht. Vouw de relevante secties hieronder uit om de benodigde instellingen toe te passen en zorg ervoor dat deze compatibel zijn met de benodigde updates.

+++Stappen om de bestaande inhoud te indexeren om de nieuwe zoek- en onderwerpenlijst onder het tabblad Rapporten te gebruiken
Voer de volgende stappen uit om de bestaande inhoud te indexeren en de nieuwe vondst en vervangt tekst op kaartniveau en onderwerpenlijst onder het rapportlusje te gebruiken:

1. Voer een POST-aanvraag uit op de server (met correcte verificatie) - `http://<server:port>/bin/guides/map-find/indexing` . (Optioneel: u kunt specifieke paden van de kaarten doorgeven om deze te indexeren. Standaard worden alle kaarten geïndexeerd|| Voorbeeld: `https://<Server:port>/bin/guides/map-find/indexing?paths=<path of the MAP in repository>`)

1. U kunt ook een hoofdmap doorgeven om de DITA-kaarten van een specifieke map (en de bijbehorende submappen) te indexeren. Bijvoorbeeld `http://<server:port\>/bin/guides/map-find/indexing?root=/content/dam/test` . Wanneer zowel de parameter paths als de hoofdparameter worden doorgegeven, wordt alleen de parameter paths gebruikt.

1. De API retourneert een jobId. Als u de status van de taak wilt controleren, kunt u een GET-aanvraag met taak-id naar hetzelfde eindpunt verzenden - `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}` (bijvoorbeeld: `http://localhost:8080/bin/guides/reports/upgrade?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678`)

1. Nadat de taak is voltooid, reageert het vorige GET-verzoek met succes en wordt vermeld of kaarten zijn mislukt. De met succes geïndexeerde kaarten kunnen van serverlogboeken worden bevestigd.

+++

+++Stappen om de bestaande inhoud te posten om het verbroken koppelingsrapport te gebruiken 
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

+++

+++Stappen om de trigger van een script via een servlet in te schakelen
Nadat u de installatie hebt voltooid, kunt u de vertaaltaak starten:

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

+++
