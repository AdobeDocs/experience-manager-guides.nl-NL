---
title: Opmerkingen bij de release | Upgradeinstructies en opgeloste problemen in Adobe Experience Manager Guides, release van december 2023
description: Leer over de insectenmoeilijke situaties en hoe te aan de versie van December 2023 van Adobe Experience Manager Guides as a Cloud Service te bevorderen.
feature: Release Notes
role: Leader
exl-id: 63efe42a-b817-49df-8f76-df8d7acf9194
source-git-commit: e40ebf4122decc431d0abb2cdf1794ea704e5496
workflow-type: tm+mt
source-wordcount: '1319'
ht-degree: 0%

---

# Release van Adobe Experience Manager Guides as a Cloud Service in december 2023

Deze versienota behandelt de verbeteringsinstructies, verenigbaarheidsmatrijs, en kwesties die in versie December 2023 van Adobe Experience Manager Guides as a Cloud Service worden bevestigd (later die als *worden bedoeld Experience Manager Guides as a Cloud Service*).

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, mening [ wat in de versie van December 2023 van Experience Manager Guides as a Cloud Service ](whats-new-2023-12-0.md) nieuw is.

## Upgrade naar release december 2023

Voer de volgende stappen uit om uw huidige Experience Manager Guides as a Cloud Service-installatie bij te werken:

1. Controle uit de code van Git van Cloud Servicen en schakelaar aan de tak die in de pijpleiding van Cloud Servicen wordt gevormd die aan het milieu beantwoordt dat u wilt bevorderen.
2. Werk de eigenschap `<dox.version>` in het `/dox/dox.installer/pom.xml` -bestand van de Git-code van de Cloud Service bij naar 2023.12.0.16.
3. Leg de wijzigingen vast en voer de pijplijn met Cloud Servicen uit om de release van Experience Manager Guides as a Cloud Service in december 2023 te voltooien.

## Stappen om de trigger van een script via een servlet in te schakelen

(Alleen als u een versie hebt die ouder is dan de release van Experience Manager Guides as a Cloud Service in juni 2023)

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

## Stappen om de bestaande inhoud te posten om het verbroken koppelingsrapport te gebruiken

(Alleen als u een versie hebt die ouder is dan de release van Experience Manager Guides as a Cloud Service in juni 2023)

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

1. Keer terug naar de standaardwaarde of vorige bestaande waarde van `queryLimitReads` als u deze in stap 1 hebt gewijzigd.

## Stappen om de bestaande inhoud te indexeren om de nieuwe zoek- en vervangings- en onderwerpenlijst onder het tabblad Rapporten te gebruiken:

(Alleen als u een versie hebt die ouder is dan de release van Experience Manager Guides as a Cloud Service in juni 2023)

Voer de volgende stappen uit om de bestaande inhoud te indexeren en de nieuwe vondst en vervangt tekst op kaartniveau en onderwerpenlijst onder het rapportlusje te gebruiken:

1. Voer een verzoek van de POST op de server uit (met correcte authentificatie) - `http://<server:port>/bin/guides/map-find/indexing`. (Optioneel) U kunt specifieke paden van de kaarten doorgeven om deze te indexeren. Standaard worden alle kaarten geïndexeerd|| Bijvoorbeeld : `https://<Server:port>/bin/guides/map-find/indexing?paths=<map_path_in_repository>`)

1. U kunt ook een hoofdmap doorgeven om de DITA-kaarten van een specifieke map (en de bijbehorende submappen) te indexeren. Bijvoorbeeld `http://<server:port>/bin/guides/map-find/indexing?root=/content/dam/test` . Wanneer zowel de parameter paths als de hoofdparameter worden doorgegeven, wordt alleen de parameter paths gebruikt.

1. De API retourneert een jobId. Als u de status van de taak wilt controleren, kunt u een aanvraag van een GET met taak-id naar hetzelfde eindpunt verzenden - `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}` (bijvoorbeeld: `http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678`)


1. Zodra de baan wordt voltooid, antwoordt het vorige verzoek van de GET met succes en vermeld als om het even welke kaarten ontbrak. De met succes geïndexeerde kaarten kunnen van de serverlogboeken worden bevestigd.

## Stappen voor het afhandelen van het `'fmdita rewriter'` -conflict

Experience Manager Guides heeft de module van de a [**douane die herschrijver**](../cs-install-guide/conf-output-generation.md#custom-rewriter) voor de behandeling van de verbindingen in het geval van dwars-kaarten (verbindingen tussen de onderwerpen van twee verschillende kaarten) worden geproduceerd.

Als u nog een aangepaste schrijfbewerking voor tekenreeksen in uw codebase hebt, gebruikt u een `'order'` -waarde groter dan 50, omdat Experience Manager Guides anders `'order'` 50 gebruikt.  Als u dit wilt overschrijven, hebt u een waarde > 50 nodig. Voor meer details, mening [ Output die pijplijnen herschrijft ](https://sling.apache.org/documentation/bundles/output-rewriting-pipelines-org-apache-sling-rewriter.html).

Aangezien de waarde van `'order'` tijdens deze upgrade is gewijzigd van 1000 in 50, moet u eventueel de bestaande aangepaste rewriter samenvoegen met `'fmdita-rewriter'` .


## Compatibiliteitsmatrix

In deze sectie wordt een overzicht gegeven van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door de Experience Manager Guides as a Cloud Service-release van december 2023.

### FrameMaker en FrameMaker Publishing Server

| Experience Manager Guides als Cloud Release | FMPS | FrameMaker |
| --- | --- | --- |
| 2023 12,0 | Niet compatibel | 2022 of hoger |
| | | |


### Zuurstofaansluiting

| Experience Manager Guides als Cloud Release | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2023 12,0 | 3.3-uuid.5 | 3.3-uuid.5 | 2,3 | 2,3 |
|  |  |  |  |


### Versie van basissjabloon

| Naam van componentenpakket | Versie van componenten | Sjabloonversie |
|---|---|---|
| Experience Manager Guides Components Content Package voor Cloud Service | dxml-components.all-1.2.2 | aem-site-template-dxml.all-1.0.15 |

## Opgeloste problemen

De fouten die in verschillende gebieden zijn gecorrigeerd, worden hieronder weergegeven:



### Authoring

- De **Titel** in het lusje van de Redacteur van het Web wordt beknot na een punt (.) teken. 14372
- Foutberichten voor dubbele kaartnamen in de gebruikersinterface van Assets worden niet bijgewerkt. 14320
- Er treedt een fout op in de logica voor het maken van versies tijdens het slepen en neerzetten van elementen. 14291
- Herbruikbare inhoud slaat de element-id&#39;s over. 14213
- De plaatsende controle om **paneel van de Variabelen van de Taal te verbergen** onder **lusje van de Output {ontbreekt.** (14194)
- De Redacteur van het Web werpt toepassingsfouten wanneer het toevoegen van een nieuwe verwijzing of een onderwerp gebruikend een gespecialiseerd schema in de mening van de Lay-out. (14094)
- Een ankerkoppeling naar `<dlentry>` of `<dt>` -element geeft de koppelingstekst niet weer. 13543
- De **inzameling van Favorieten** in de Redacteur van het Web slaagt er niet in om te laden. 13495
- Bij het maken van een unieke id met spaties worden niet-klikbare koppelingen weergegeven. (13447)
- In de **mening van de Lay-out** voor een Bookmap, gebruikend **Beweging Juist** om een geselecteerd hoofdstuk te maken werkt een subelement niet. 12567
- Het voorvertoningsvenster van de XML-editor wordt afgebroken in Google Chrome- en Microsoft Edge-browsers. 10755
- In de webeditor is het niet mogelijk een element binnen de mogelijke bovenliggende elementen te plaatsen. 8791

### Publiceren

- Fmdita-componenten hebben een hardcoderingspad van `delegator.jsp`, waardoor de bedekking van AEM Sites-componenten wordt voorkomen. (13993)
- De getagde weergave van de PDF-reactor in Native PDF-publicatie-uitvoer werkt niet zoals u had verwacht. (13622)
- AEM het publiceren van de Plaats ontmoet een kwestie wanneer het begaan aan aan de datastore voor grote kaarten met werkingsgebied peer verbindingen. 13531
- Kan een site niet activeren met het Experience Manager Guides Bulk Publication dashboard. 13439
- De lokalisatie van de elementlabels werkt niet goed in de AEM Sites-uitvoer. (12144)
- Ontbrekende **ditaval** optie in het niveau van de output van het omslagprofiel vooraf instelt die via de Redacteur UI van het Web worden gecreeerd. (1903)

### Beheer

- AEM cloudomgevingen hebben een MongoWrite-uitzondering vanwege grote knooppunten. 13509

### Vertaling

- De **Accepteren/verwerpen** knopen verschijnen abusievelijk voor auto-goedgekeurde menselijke vertaling. (14318)
- Problemen met internationalisatie (i18n) treden op tijdens de transformatie van DITA-bestanden die niet in het Engels staan, naar AEM pagina&#39;s. 14286
- De vertaalde inhoud synchroniseert niet van tijdelijke vertaalprojecten, en de redacteurs vertaaltovenaar van DITA XML toont verkeerd **Bezig** status voor goedgekeurde banen. (9938)

### Toegankelijkheid

- Kan niet door de gebruikersinterface van het auteurcanvas navigeren, aangezien de nadruk gevangen in de onderwerpredacteur wordt. 13517

## Bekend probleem

Adobe heeft voor de release van december 2023 het volgende bekende probleem geïdentificeerd:
- &quot;Ongeldige DTD-fout opvragen&quot; treedt soms op bij de upgrade naar de release van december 2023.
