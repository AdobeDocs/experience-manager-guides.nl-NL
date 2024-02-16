---
title: Opmerkingen bij de release | Upgradeinstructies en opgeloste problemen in Adobe Experience Manager Guides, release van februari 2024
description: Leer over de insectenmoeilijke situaties en hoe te om aan de versie van februari 2024 as a Cloud Service Gidsen van Adobe Experience Manager te bevorderen.
source-git-commit: 6d8c01f20f7b59fed92c404561b647d9ebecb050
workflow-type: tm+mt
source-wordcount: '1311'
ht-degree: 0%

---

# Release van Adobe Experience Manager Guides, februari 2024 as a Cloud Service

In deze releaseopmerking worden de instructies voor het bijwerken, de compatibiliteitsmatrix en de problemen behandeld die zijn opgelost in versie februari 2024 van de as a Cloud Service Adobe Experience Manager-hulplijnen (later genoemd als *Experience Manager-hulplijnen as a Cloud Service*).

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, mening [Nieuwe functies in de release van Experience Manager Guides van februari 2024 as a Cloud Service](whats-new-2024-02-0.md).

## Upgrade naar release van februari 2024

Voer de volgende stappen uit om de huidige as a Cloud Service installatie van de hulplijnen voor Experience Managers bij te werken:

1. Controle uit de code van Git van Cloud Servicen en schakelaar aan de tak die in de pijpleiding van Cloud Servicen wordt gevormd die aan het milieu beantwoordt dat u wilt bevorderen.
2. Bijwerken `<dox.version>` eigenschap in `/dox/dox.installer/pom.xml` bestand van uw Cloud Servicen Git-code naar 2024.02.0.15.
3. Leg de wijzigingen vast en voer de pijplijn met Cloud Servicen uit om naar de release van februari 2024 van as a Cloud Service hulplijnen voor Experience Manager te upgraden.

## Stappen om de trigger van een script via een servlet in te schakelen

(Alleen als u een versie hebt die ouder is dan de versie van juni 2023 van de hulplijnen voor Experience Managers as a Cloud Service)

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

## Stappen om de bestaande inhoud te posten om het verbroken koppelingsrapport te gebruiken

(Alleen als u een versie hebt die ouder is dan de versie van juni 2023 van de hulplijnen voor Experience Managers as a Cloud Service)

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

## Stappen om de bestaande inhoud te indexeren om de nieuwe zoek- en vervangings- en onderwerpenlijst onder het tabblad Rapporten te gebruiken:

(Alleen als u een versie hebt die ouder is dan de versie van juni 2023 van de hulplijnen voor Experience Managers as a Cloud Service)

Voer de volgende stappen uit om de bestaande inhoud te indexeren en de nieuwe vondst en vervangt tekst op kaartniveau en onderwerpenlijst onder het rapportlusje te gebruiken:

1. Voer een verzoek van de POST op de server uit (met correcte authentificatie) - `http://<server:port>/bin/guides/map-find/indexing`. (Optioneel) U kunt specifieke paden van de kaarten doorgeven om deze te indexeren. Standaard worden alle kaarten geïndexeerd|| Bijvoorbeeld: `https://<Server:port>/bin/guides/map-find/indexing?paths=<path of the MAP in repository>`)

1. De API retourneert een jobId. Als u de status van de taak wilt controleren, kunt u een aanvraag van een GET met taak-id naar hetzelfde eindpunt verzenden - `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}`(Bijvoorbeeld: `http://localhost:8080/bin/guides/reports/upgrade?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678`)

1. Zodra de baan wordt voltooid, antwoordt het vorige verzoek van de GET met succes. Als de taak om een of andere reden mislukt, kan de fout worden gezien in de serverlogboeken.

1. Terugkeren naar de standaardwaarde of vorige bestaande waarde van queryLimitReads als u deze hebt gewijzigd in stap 1.

## Stappen om de `'fmdita rewriter'` conflict

Hulplijnen voor Experience Manager hebben een [**aangepaste herschrijffunctie voor verkoop**](../cs-install-guide/conf-output-generation.md#custom-rewriter) module voor het afhandelen van de koppelingen die worden gegenereerd in het geval van cross-maps (koppelingen tussen de onderwerpen van twee verschillende kaarten).

Als u een andere aangepaste schrijver voor de spelling in uw codebase hebt, gebruikt u een `'order'` waarde groter dan 50, aangezien de Experience Manager Gidsen herschrijver gebruikt `'order'` 50  Als u dit wilt overschrijven, hebt u een waarde > 50 nodig. Voor meer informatie, bekijkt u [Output Rewriting Pipelines](https://sling.apache.org/documentation/bundles/output-rewriting-pipelines-org-apache-sling-rewriter.html).

Tijdens deze upgrade, sinds de `'order'` waarde is gewijzigd van 1000 in 50, moet u de bestaande aangepaste rewriter, indien aanwezig, samenvoegen met `'fmdita-rewriter'`.


## Compatibiliteitsmatrix

In deze sectie wordt een overzicht gegeven van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door de release van Experience Manager Guides van februari 2024.

### FrameMaker en FrameMaker Publishing Server

| Hulplijnen Experience Managers als cloudrelease | FMPS | FrameMaker |
| --- | --- | --- |
| 2024,02,0 | Niet compatibel | 2022 of hoger |
| | | |


### Zuurstofaansluiting

| Hulplijnen Experience Managers als cloudrelease | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2024,02,0 | 3.1-uuid.17 | 3.1-uuid.17 | 2,3 | 2,3 |
|  |  |  |  |


### Versie van basissjabloon

| Naam van componentenpakket | Versie van componenten | Sjabloonversie |
|---|---|---|
| Experience Manager Guides Components Content Package for Cloud Service | dxml-components.all-1.2.2 | aem-site-template-dxml.all-1.0.15 |

## Opgeloste problemen

De fouten die in verschillende gebieden zijn gecorrigeerd, worden hieronder weergegeven:

### Authoring

- Spellingcontrole in de Editor staat niet toe dat suggesties worden geselecteerd. 15045
- De algemene navigatieknop werkt niet en het dashboard kan niet worden geladen. 14968
- In de Redacteur van het Web, ontbreekt de eigenschap van de downloadkaart om een pop-up bericht teweeg te brengen wanneer het klaar is om te downloaden. 14626
- In de Redacteur van het Web, ontbreekt de eigenschap van de downloadkaart om een kaart met basislijn te downloaden. (14622)
- Ongeldige DTD-fout in as a Cloud Service versie 2310 van de Experience Manager-hulplijnen. (14482)
- Het slepen van een verklarend woordenlijstonderwerp van de bewaarplaats in een verklarende woordenlijstkaart leidt tot `topicref`. 10767
- De webeditor wordt verwijderd nadat u Adobe Experience Manager Guides versie 4.3.1 opnieuw hebt geïnstalleerd. 14519
- Het installatieprogramma van versie 4.3.1 vindt een filterconflict, wat leidt tot het overschrijven van `apps/cq/core/content/projects/properties`. 14517
- Het voorvertoningsscherm voor fragmenten is bevroren. 14840

### Publiceren

- In publicaties met native PDF werken aangepaste kenmerken binnen voorinstellingen voor voorwaarde niet voor publicatie met eigen PDF. 14943
- Kan geen aangepaste sjabloon toevoegen vanuit het dialoogvenster **Uitvoer** in de Editor. 14846
- **Site AEM** De voorinstelling werkt niet vanwege een leeg sjabloonpad. 14804
- AEM de regeneratie van de Plaats ontbreekt voor kaarten DITA met onderwerpen die vergelijkingen MathML bevatten. 14790
- In het Publiceren van Native PDF, genereren van PDF fouten in het krijgen van afhankelijkheden voor `Node.js` publiceren. (1445)
- Met AEM voorinstelling kunt u geen sjabloon buiten de `/content` in de webeditor. (14260)
- In de AEM Sites-uitvoer gingen de stijl of regeleinden verloren voor de `<lines>` element met subelementen.12542
- Aangepaste metagegevens zijn niet beschikbaar in de uiteindelijke uitvoer. (1216)
- Bij de upgrade naar versie 4.3.1 zijn er enkele uitzonderingen in het knooppunt Native PDF. (1492)


### Beheer

- **Basislijnfilter** de dossiers werken niet met de Naam van het Dossier in de Redacteur van het Web. 13486
- Het onbruikbaar maken van het indexeren van de ouderkaart DITA om betere prestaties te krijgen kan de functionaliteit van bepaalde eigenschappen beïnvloeden.12213
- Labels uit de `labels.json` bestand wordt in willekeurige volgorde weergegeven in de webeditor. 10508

### Controleren

- Klikken met rechtermuisknop in contextmenu werkt niet voor **Accepteren** of **Afwijzen** wijzigingen bijhouden. 14607
- In- en uitschakelen om DITA-onderwerpen in het revisiescherm te sluiten, werkt niet in versie 4.3.1 van Adobe Experience Manager-hulplijnen. 14537
- Het aanpassen van e-mailsjablonen voor de revisiewerkstroom werkt niet met overlay. 13954

## Bekend probleem

Adobe heeft voor de release van februari 2024 het volgende bekende probleem geïdentificeerd:

- Versie 1.0 wordt niet getoond op UI voor het gedupliceerde DITA- dossier.
