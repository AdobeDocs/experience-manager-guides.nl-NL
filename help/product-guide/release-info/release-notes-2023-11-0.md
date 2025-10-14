---
title: Opmerkingen bij de release | Upgradeinstructies en opgeloste problemen in Adobe Experience Manager Guides, release november 2023
description: Leer over de insectenmoeilijke situaties en hoe te aan de versie van November 2023 van Adobe Experience Manager Guides as a Cloud Service te bevorderen
exl-id: 80839890-075f-4187-a167-444c73215496
feature: Release Notes
role: Leader
source-git-commit: 6d8c01f20f7b59fed92c404561b647d9ebecb050
workflow-type: tm+mt
source-wordcount: '1673'
ht-degree: 0%

---

# Release van Adobe Experience Manager Guides as a Cloud Service in november 2023

Deze versienota behandelt de verbeteringsinstructies, verenigbaarheidsmatrijs, en kwesties die in versie November 2023 van as a Cloud Service Adobe Experience Manager Guides worden bevestigd (later die als *worden bedoeld Experience Manager Guides as a Cloud Service*).

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, mening [&#x200B; wat in de versie van november 2023 van Experience Manager Guides as a Cloud Service &#x200B;](whats-new-2023-11-0.md) nieuw is.

## Upgrade naar release november 2023

Voer de volgende stappen uit om uw huidige Experience Manager Guides as a Cloud Service-installatie bij te werken:

1. Controle uit de code van Git van Cloud Servicen en schakelaar aan de tak die in de pijpleiding van Cloud Servicen wordt gevormd die aan het milieu beantwoordt dat u wilt bevorderen.
2. Werk de eigenschap `<dox.version>` in het `/dox/dox.installer/pom.xml` -bestand van de Git-code van de Cloud Service bij naar 2023.11.0.406.
3. Leg de wijzigingen vast en voer de Cloud Servicen-pijplijn uit om naar de release van november 2023 van Experience Manager Guides as a Cloud Service te upgraden.

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

In de vorige reactie JSON bevat de sleutel `lockNodePath` het pad naar het knooppunt dat in de opslagplaats is gemaakt en dat naar de verzonden taak wijst. Het wordt automatisch verwijderd als de taak is voltooid. U kunt dan naar dit knooppunt verwijzen voor de status van de taak.

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

1. Voer een verzoek van de POST op de server uit (met correcte authentificatie) - `http://<server:port>//bin/guides/reports/upgrade`.

1. De API retourneert een jobId. Als u de status van de taak wilt controleren, kunt u een aanvraag voor een GET met taak-id naar hetzelfde eindpunt verzenden - `http://<server:port>/bin/guides/reports/upgrade?jobId= {jobId}`
(Bijvoorbeeld: `http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678`)

1. Zodra de baan wordt voltooid, antwoordt het vorige verzoek van de GET met succes. Als de taak om een of andere reden mislukt, kan de fout worden gezien in serverlogboeken.

1. Keer terug naar de standaardwaarde of vorige bestaande waarde van `queryLimitReads` als u deze in stap 1 hebt gewijzigd.

## Stappen om de bestaande inhoud te indexeren om de nieuwe zoek- en vervangings- en onderwerpenlijst onder het tabblad Rapporten te gebruiken:

(Alleen als u een versie hebt die ouder is dan de release van Experience Manager Guides as a Cloud Service in juni 2023)

Voer de volgende stappen uit om de bestaande inhoud te indexeren en de nieuwe vondst en vervangt tekst op kaartniveau en onderwerpenlijst onder het rapportlusje te gebruiken:

1. Voer een verzoek van de POST op de server uit (met correcte authentificatie) - `http://<server:port>/bin/guides/map-find/indexing`. (Optioneel) U kunt specifieke paden van de kaarten doorgeven om deze te indexeren. Standaard worden alle kaarten geïndexeerd || Bijvoorbeeld : `https://<Server:port>/bin/guides/map-find/indexing?paths=<map_path_in_repository>`)

1. U kunt ook een hoofdmap doorgeven om de DITA-kaarten van een specifieke map (en de bijbehorende submappen) te indexeren. Bijvoorbeeld `http://<server:port>/bin/guides/map-find/indexing?root=/content/dam/test` . Wanneer zowel de parameter paths als de hoofdparameter worden doorgegeven, wordt alleen de parameter paths gebruikt.

1. De API retourneert een jobId. Als u de status van de taak wilt controleren, kunt u een aanvraag van een GET met taak-id naar hetzelfde eindpunt verzenden - `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}` (bijvoorbeeld: `http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42`)


1. Zodra de baan wordt voltooid, antwoordt het vorige verzoek van de GET met succes en vermeld als om het even welke kaarten ontbrak. De met succes geïndexeerde kaarten kunnen van de serverlogboeken worden bevestigd.

## Stappen voor het afhandelen van het `'fmdita rewriter'` -conflict

Experience Manager Guides heeft de module van de a [**douane die herschrijver**](../cs-install-guide/conf-output-generation.md#custom-rewriter) voor de behandeling van de verbindingen in het geval van dwars-kaarten (verbindingen tussen de onderwerpen van twee verschillende kaarten) worden geproduceerd.

Als u nog een aangepaste schrijfbewerking voor tekenreeksen in uw codebase hebt, gebruikt u een `'order'` -waarde groter dan 50, omdat Experience Manager Guides anders `'order'` 50 gebruikt.  Als u dit wilt overschrijven, hebt u een waarde > 50 nodig. Voor meer details, mening [&#x200B; Output die pijplijnen herschrijft &#x200B;](https://sling.apache.org/documentation/bundles/output-rewriting-pipelines-org-apache-sling-rewriter.html).

Aangezien de waarde van `'order'` tijdens deze upgrade is gewijzigd van 1000 in 50, moet u eventueel de bestaande aangepaste rewriter samenvoegen met `'fmdita-rewriter'` .


## Compatibiliteitsmatrix

Deze sectie maakt een lijst van de verenigbaarheidsmatrijs voor de softwaretoepassingen die door de versie van Experience Manager Guides as a Cloud Service November 2023 worden gesteund.

### FrameMaker en FrameMaker Publishing Server

| Experience Manager Guides-hulplijnen als een cloudrelease | FMPS | FrameMaker |
| --- | --- | --- |
| 2023 11,0 | Niet compatibel | 2022 of hoger |
| | | |


### Zuurstofaansluiting

| Experience Manager Guides als Cloud Release | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2023 11,0 | 3.2-uuid 5 | 3.2-uuid 5 | 2,3 | 2,3 |
|  |  |  |  |


### Versie van basissjabloon

| Naam van componentenpakket | Versie van componenten | Sjabloonversie |
|---|---|---|
| Experience Manager Guides Components Content Package voor Cloud Service | dxml-components.all-1.2.2 | aem-site-template-dxml.all-1.0.15 |

## Opgeloste problemen

De fouten die in verschillende gebieden zijn gecorrigeerd, worden hieronder weergegeven:



### Authoring

- Ruimte na conref `<ph>` -element verdwijnt bij het opslaan van het onderwerp. 13642
- Toepassingsfout treedt op wanneer u probeert DITA-bestanden op te slaan voordat de naverwerking is voltooid. 13571
- Als de titel van een onderwerp een schuine streep `/` bevat, toont het lusje in de redacteur slechts de brieven die na het komen. (13455)
- De voorvertoning van de afbeelding verdwijnt niet nadat de voorvertoning in de Editor is weergegeven. 13454
- Het sleutelwoord van het Tussenvoegsel pop-up verschijnt niet wanneer het gebruiken van wortel kaart-bepaalde sleutels in andere onderwerpen. 12950
- Pictogrammen sluiten is niet zichtbaar wanneer een voorvertoning wordt weergegeven van zeer grote afbeeldingen in het deelvenster Versiehistorie. 12867
- Onbekwaam om timezone van **Versie te wijzigen die op** wordt gecreeerd kolom voor Baselines. (1271)
- Het **paneel van de Geschiedenis van de Versie** in Assets UI toont een onjuiste timestamp voor het **Huidige** gebied. 12624
- Als u een DITA-bestand maakt op basis van een sjabloon met een bestandsnaam die begint met numerieke tekens, treedt er een naamruimtefout op. (12188)
- In de Redacteur van het Web, opent het **Zeer belangrijke venster van Verwijzingen** wanneer het opnemen van de `varname` markering. 10940
- Zip-bestanden worden niet herkend in de webeditor en u kunt ze niet slepen en neerzetten. 12709
- De inhoud waarop bepaalde kenmerken zijn toegepast, wordt niet gemarkeerd in de modus Auteur of Voorvertoning. (1063)
- Wanneer u een onderwerp sluit nadat u het hebt bewerkt, wordt u omgeleid naar de AEM startpagina in plaats van terug te keren naar de mappenweergave. (13306)
- De verwerking van bestanden die naar de cloudservices zijn gekopieerd en geplakt, verloopt traag. 12457
- De rootmap-instelling blijft bestaan in de webeditor, zelfs als de gebruiker deze niet expliciet heeft ingesteld in de gebruikersvoorkeuren. (11551)


### Publiceren

- Publish als functionaliteit voor inhoudsfragmenten werkt niet voor bestanden die in zoekresultaten worden vermeld. (14090)
- In publicaties met native PDF vereist de achtergrondkleur die u in de sjabloonlay-out selecteert, dat de pagina opnieuw wordt geladen wanneer u terugkeert naar `None` . 13621
- Probleem bij het vastleggen van datastore voor een grote DITA-kaart met &#39;scope peer&#39;-koppelingen in AEM publicatie van de site. (13530)
- In het publiceren van de Eigen PDF, wordt de toegankelijkheid gecompromitteerd aangezien de beelden in kopbal en footer alt geen tekst tonen. 12829
- Het dupliceren van de paginalay-out in de native PDF werkt niet zonder automatische toevoeging. 12534
- Wanneer u de PDF-uitvoer genereert met Native PDF-publicatie, wordt de bestandsnaam na een punt afgekapt. 13620
- Het onjuiste pictogram en tooltip worden getoond voor **geef inhoud** optie in de toolbar van de Lay-outs van de Pagina van de Malplaatjes uit die in het Inheemse publiceren van PDF worden gebruikt. 13492
- Aangepaste metagegevens zijn niet beschikbaar in de uiteindelijke uitvoer. (1216)
- fmdita rewriter veroorzaakt een conflict met de rewriter-config van de gebruiker en leidt tot de weergave van lange URL&#39;s in plaats van de koppelingen. (12076)
- In de AEM vooraf ingestelde Plaats, is de optie om **afzonderlijke PDF voor elk onderwerp** te produceren niet-functioneel. (11555)
- Native PDF-publicaties bieden geen ondersteuning voor het omzetten van CMYK-kleurruimten. 10754
- Dynamische basislijnaanroepen gebruiken de naam in plaats van de titel, wat resulteert in een fout van de DITA-kaart-API exporteren. 14268

### Beheer

- De verwijzing van de inhoud wordt gebroken op kopiëren-kleeft de DITA- dossiers die zelfverwijzingsverbindingen zonder GUID hebben. 13540)
- In de Redacteur van het Web, toont de basislijn de titel voor de vorige versie in plaats van de geselecteerde versie van het DITA- dossier. (13444)
- Het **lusje van Rapporten** in de Redacteur UI van het Web ontbreekt om de onderwerpenlijst voor oude kaarten te tonen DITA die voorafgaand aan de verbetering van juli 2023 van Experience Manager Guides as a Cloud Service worden gecreeerd. (11852)
- Voorinstellingen voor voorwaarden voor grote DITA-kaarten worden niet gemaakt. 10936
- Er wordt een koppeling met een zelfverwijzing weergegeven onder de lijst Verbroken koppelingen in Rapporten. 13539

### Controleren

- In de release van oktober 2023 van Experience Manager Guides as a Cloud Service zijn de revisiedeelvensters naast elkaar van de vorige en de huidige versies in de webeditor niet correct. 14156
- De aanpassing van het e-mailmalplaatje voor **Overzicht** werkschema werkt niet met het bedekken van de knopen. 13954
- De **dichte** knoop op de pagina van het Overzicht in Experience Manager Guides neemt de gebruikers aan de AEM Homepage. 13535
- Verbroken tekens worden weergegeven tijdens het maken van de fragmenten in de Koreaanse taal. 13489
- Op Koreaanse bijlagen kan niet worden geklikt in het scherm Experience Manager Guides Review. 13436
- De kaarthandleiding wordt afgesneden in het overzichts- en samenwerkingsscherm, zonder optie om de volledige titel te bekijken. 13012

### Vertaling

- Auto keurt niet soms goed, en de uitzonderingen komen voor als een onjuiste waarde op **de Status van de Vertaling** wordt geplaatst. 13607
- De basislijn die u exporteert vanaf het dashboard Vertalen mislukt en wordt niet geopend in de doeltaal. (12993)

## Bekend probleem

Adobe heeft het volgende bekende probleem voor de release van november 2023 geïdentificeerd.

- Selectieve onderwerpregeneratie voor AEM output van de Plaats ontbreekt.
