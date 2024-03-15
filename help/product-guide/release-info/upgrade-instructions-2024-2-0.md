---
title: Opmerkingen bij de release | Upgrade-instructies en opgeloste problemen in Adobe Experience Manager-hulplijnen, release 2024.2.0
description: Leer meer over de compatibiliteitsmatrix en hoe u een upgrade uitvoert naar de 2024.2.0-release van de as a Cloud Service Adobe Experience Manager-hulplijnen.
source-git-commit: 9022b8fbae9ff9eba962ca75e25c1f1137b008f8
workflow-type: tm+mt
source-wordcount: '866'
ht-degree: 0%

---

# Upgrade-instructies voor de release van 2024.2.0

Dit artikel behandelt de upgrade-instructies en de compatibiliteitsmatrix voor de release van Adobe Experience Manager Guides 2024.2.0 as a Cloud Service.

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, mening [Nieuwe functies in de release 2024.2.0](whats-new-2024-2-0.md).

Voor de lijst met problemen die in deze release zijn opgelost, raadpleegt u [Opgeloste problemen in de release 2024.2.0](fixed-issues-2024-2-0.md).


## Compatibiliteitsmatrix

In deze sectie wordt een overzicht gegeven van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door de 2024.2.0-release van Experience Manager Guides as a Cloud Service.

### FrameMaker en FrameMaker Publishing Server

| Hulplijnen Experience Managers als cloudrelease | FMPS | FrameMaker |
| --- | --- | --- |
| 2024,2,0 | Niet compatibel | 2022 of hoger |
| | | |


### Zuurstofaansluiting

| Hulplijnen Experience Managers als cloudrelease | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2024,2,0 | 3,5-uuid 1 | 3,5-uuid 1 | 2,3 | 2,3 |
|  |  |  |  |


### Versie van basissjabloon

| Naam van componentenpakket | Versie van componenten | Sjabloonversie |
|---|---|---|
| Experience Manager Guides Components Content Package for Cloud Service | dxml-components.all-1.2.2 | aem-site-template-dxml.all-1.0.15 |

## Upgrade naar 2024.2.0-release

De Gidsen van de Experience Manager wordt automatisch bevorderd na bevordering van de huidige (recentste) versie van as a Cloud Service Experience Manager.


Voer de volgende stappen voor as a Cloud Service Gidsen van de Experience Manager uit als u niet eerder voor uw bestaande versie hebt gedaan:

### Stappen om de trigger van een script via een servlet in te schakelen

(Alleen als u een release hebt ontvangen vóór de release van juni 2023 met hulplijnen voor Experience Managers as a Cloud Service)

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

In de vorige reactie van JSON was de sleutel `lockNodePath` bevat het pad naar het knooppunt dat in de opslagplaats is gemaakt en dat naar de ingediende taak verwijst. Het wordt automatisch verwijderd als de taak is voltooid en u kunt naar dit knooppunt verwijzen voor de status van de taak.

Wacht tot deze taak is voltooid voordat u verdergaat met de volgende stappen.

>[!NOTE]
>
> Controleer of het knooppunt nog aanwezig is en wat de status van de taak is.

```
GET
http://<aem_domain>/var/dxml/executor-locks/translation-map-upgrade/1683190032886.json
```

### Stappen om de bestaande inhoud te posten om het verbroken koppelingsrapport te gebruiken

(Alleen als u een release hebt ontvangen vóór de release van juni 2023 met hulplijnen voor Experience Managers as a Cloud Service)

Voer de volgende stappen uit voor de nabewerking van de bestaande inhoud en het gebruik van het nieuwe verbroken koppelingsrapport:

1. (Optioneel) Als het systeem meer dan 100.000 DITA-bestanden bevat, werkt u de `queryLimitReads` en `queryLimitInMemory` krachtens `org.apache.jackrabbit.oak.query.QueryEngineSettingsService` naar een hogere waarde (een waarde die groter is dan het aantal aanwezige elementen, bijvoorbeeld 200.000) en vervolgens opnieuw te implementeren.

   - Gebruik de instructies in de *Configuratieoverschrijvingen* in Installeer en configureer as a Cloud Service Adobe Experience Manager-hulplijnen om het configuratiebestand te maken.
   - In het configuratiedossier, verstrek de volgende (bezit) details om het `queryLimitReads` en `queryLimitInMemory` optie:

     | PID | Eigenschappensleutel | Waarde van eigenschap |
     |---|---|---|
     | org.apache.jackrabbit.oak.query.QueryEngineSettingsService | queryLimitReads | Waarde: 200000 Standaardwaarde: 100000 |
     | org.apache.jackrabbit.oak.query.QueryEngineSettingsService | queryLimitInMemory | Waarde: 200000 Standaardwaarde: 100000 |

1. Voer een verzoek van de POST op de server uit (met correcte authentificatie) - `http://<server>//bin/guides/reports/upgrade`.

1. De API retourneert een jobId. Als u de status van de taak wilt controleren, kunt u een aanvraag van een GET met taak-id naar hetzelfde eindpunt verzenden - `http://<server>/bin/guides/reports/upgrade?jobId= {jobId}`
(Bijvoorbeeld: `http://localhost:8080/bin/guides/reports/upgrade?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678`)

1. Zodra de baan wordt voltooid, antwoordt het vorige verzoek van de GET met succes. Als de taak om een of andere reden mislukt, kan de fout worden gezien in serverlogboeken.

1. Terugkeren naar de standaardwaarde of vorige bestaande waarde van `queryLimitReads` als u dit in stap 1 hebt gewijzigd.

### Stappen om de bestaande inhoud te indexeren om de nieuwe zoek- en vervangings- en onderwerpenlijst onder het tabblad Rapporten te gebruiken:

(Alleen als u een release hebt ontvangen vóór de release van juni 2023 met hulplijnen voor Experience Managers as a Cloud Service)

Voer de volgende stappen uit om de bestaande inhoud te indexeren en de nieuwe vondst en vervangt tekst op kaartniveau en onderwerpenlijst onder het rapportlusje te gebruiken:

1. Voer een verzoek van de POST op de server uit (met correcte authentificatie) - `http://<server:port>/bin/guides/map-find/indexing`. (Optioneel) U kunt specifieke paden van de kaarten doorgeven om deze te indexeren. Standaard worden alle kaarten geïndexeerd|| Bijvoorbeeld: `https://<Server:port>/bin/guides/map-find/indexing?paths=<path of the MAP in repository>`)

1. De API retourneert een jobId. Als u de status van de taak wilt controleren, kunt u een aanvraag van een GET met taak-id naar hetzelfde eindpunt verzenden - `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}`(Bijvoorbeeld: `http://localhost:8080/bin/guides/reports/upgrade?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678`)

1. Zodra de baan wordt voltooid, antwoordt het vorige verzoek van de GET met succes. Als de taak om een of andere reden mislukt, kan de fout worden gezien in de serverlogboeken.

1. Terugkeren naar de standaardwaarde of vorige bestaande waarde van queryLimitReads als u deze hebt gewijzigd in stap 1.

### Stappen om de `'fmdita rewriter'` conflict

Hulplijnen voor Experience Manager hebben een [**aangepaste herschrijffunctie voor verkoop**](../cs-install-guide/conf-output-generation.md#custom-rewriter) module voor het afhandelen van de koppelingen die worden gegenereerd in het geval van cross-maps (koppelingen tussen de onderwerpen van twee verschillende kaarten).

Als u een andere aangepaste schrijver voor de spelling in uw codebase hebt, gebruikt u een `'order'` waarde groter dan 50, aangezien de Experience Manager Gidsen herschrijver gebruikt `'order'` 50  Als u dit wilt overschrijven, hebt u een waarde > 50 nodig. Voor meer informatie, bekijkt u [Output Rewriting Pipelines](https://sling.apache.org/documentation/bundles/output-rewriting-pipelines-org-apache-sling-rewriter.html).

Tijdens deze upgrade, sinds de `'order'` waarde is gewijzigd van 1000 in 50, moet u de bestaande aangepaste rewriter, indien aanwezig, samenvoegen met `'fmdita-rewriter'`.



