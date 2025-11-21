---
title: Opmerkingen bij de release | Upgradeinstructies en opgeloste problemen in Adobe Experience Manager Guides, release van september 2023
description: Meer informatie over de opgeloste problemen en hoe u een upgrade uitvoert naar de release van Adobe Experience Manager Guides as a Cloud Service van september 2023
exl-id: 795b86a0-e763-404a-a4bb-35d3d2a42672
feature: Release Notes
role: Leader
source-git-commit: 6e23f52fc9124d0f07f8108da1b5fe574f553469
workflow-type: tm+mt
source-wordcount: '1485'
ht-degree: 0%

---

# Release van Adobe Experience Manager Guides as a Cloud Service in september 2023

Deze versienota behandelt de verbeteringsinstructies, verenigbaarheidsmatrijs, en kwesties die in versie September 2023 van Adobe Experience Manager Guides (later als *worden bedoeld as a Cloud Service van AEM Guides*) worden bevestigd.

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, zie [&#x200B; wat in September 2023 versie van AEM Guides as a Cloud Service &#x200B;](whats-new-2023-9-0.md) nieuw is.

## Upgrade naar release september 2023

Voer de volgende stappen uit om uw huidige AEM Guides as a Cloud Service-installatie bij te werken:

1. Bekijk de Git-code van Cloud Services en schakel over naar de vertakking die is geconfigureerd in de Cloud Services-pijplijn die overeenkomt met de omgeving die u wilt upgraden.
2. Werk de eigenschap `<dox.version>` in het `/dox/dox.installer/pom.xml` -bestand van de Git-code voor Cloud Services bij naar 2023.9.0.359.
3. Leg de wijzigingen vast en voer de Cloud Services-pijplijn uit om naar de release van september 2023 van AEM Guides as a Cloud Service te upgraden.

## Stappen om de trigger van een script via een servlet in te schakelen

(Alleen als u een versie hebt die ouder is dan juni 2023, release van AEM Guides as a Cloud Service)

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

(Alleen als u een versie hebt die ouder is dan juni 2023, release van AEM Guides as a Cloud Service)

Voer de volgende stappen uit voor de naverwerking van de bestaande inhoud en het gebruik van het nieuwe verbroken koppelingsrapport:

1. (Optioneel) Als het systeem meer dan 100.000 dita-bestanden bevat, werkt u `queryLimitReads` under `org.apache.jackrabbit.oak.query.QueryEngineSettingsService` bij tot een hogere waarde (een waarde die groter is dan het aantal aanwezige elementen, bijvoorbeeld 200.000) en herstelt u deze vervolgens.

   - Gebruik de instructies die in *worden gegeven de met voeten treedt van de Configuratie* sectie in installeer en vorm Adobe Experience Manager Guides
as a Cloud Service, om het configuratiebestand te maken.
   - In het configuratiedossier, verstrek de volgende (bezit) details om de queryLimitReads optie te vormen:

     | PID | Eigenschappensleutel | Waarde van eigenschap |
     |---|---|---|
     | org.apache.jackrabbit.oak.query.QueryEngineSettingsService | queryLimitReads | Waarde: 200000 Standaardwaarde: 100000 |

1. Voer een POST-aanvraag uit op de server (met correcte verificatie) - `http://<server:port>//bin/guides/reports/upgrade` .

1. De API retourneert een jobId. Als u de status van de taak wilt controleren, kunt u een GET-aanvraag met taak-id naar hetzelfde eindpunt verzenden - `http://<server:port>/bin/guides/reports/upgrade?jobId= {jobId}`
(Bijvoorbeeld: `http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678`)

1. Zodra de taak is voltooid, reageert het vorige GET-verzoek met succes. Als de taak om een of andere reden mislukt, kan de fout worden gezien in de serverlogboeken.

1. Terugkeren naar de standaardwaarde of vorige bestaande waarde van `queryLimitReads` als u deze hebt gewijzigd in stap 1.

## Stappen om de bestaande inhoud te indexeren om de nieuwe zoek- en vervangings- en onderwerpenlijst onder het tabblad Rapporten te gebruiken:

(Alleen als u een versie hebt die ouder is dan juni 2023, release van AEM Guides as a Cloud Service)

Voer de volgende stappen uit om de bestaande inhoud te indexeren en de nieuwe vondst en vervangt tekst op kaartniveau en onderwerpenlijst onder het rapportlusje te gebruiken:

1. Voer een POST-aanvraag uit op de server \(met correcte verificatie\) - `http://<server:port\>/bin/guides/map-find/indexing` . (Optioneel: u kunt specifieke paden van de kaarten doorgeven om deze te indexeren. Standaard worden alle kaarten geïndexeerd \|\| Bijvoorbeeld : `https://<Server:port\>/bin/guides/map-find/indexing?paths=<map\_path\_in\_repository\>`)

1. U kunt ook een hoofdmap doorgeven om de DITA-kaarten van een specifieke map (en de bijbehorende submappen) te indexeren. Bijvoorbeeld `http://<server:port\>/bin/guides/map-find/indexing?root=/content/dam/test` . Wanneer zowel de parameter paths als de hoofdparameter worden doorgegeven, wordt alleen de parameter paths gebruikt.

1. De API retourneert een jobId. Als u de status van de taak wilt controleren, kunt u een GET-aanvraag met taak-id naar hetzelfde eindpunt verzenden - `http://<server:port\>/bin/guides/map-find/indexing?jobId=\{jobId\}`\(bijvoorbeeld: `http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42`\)


1. Als de taak is voltooid, reageert het vorige GET-verzoek met succes en vermeldt u of kaarten zijn mislukt. De met succes geïndexeerde kaarten kunnen van de serverlogboeken worden bevestigd.

## Compatibiliteitsmatrix

Deze sectie bevat een overzicht van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door de AEM Guides as a Cloud Service-release van september 2023.

### FrameMaker en FrameMaker Publishing Server

| AEM Guides als Cloud Release | FMPS | FrameMaker |
| --- | --- | --- |
| 2023,09,0 | Niet compatibel | 2022 of hoger |
| | | |


### Zuurstofaansluiting

| AEM Guides als Cloud Release | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2023,09,0 | 3.1-uuid 17 | 3.1-uuid 17 | 2,3 | 2,3 |
|  |  |  |  |  |


### Versie van basissjabloon

| Naam van componentenpakket | Versie van componenten | Sjabloonversie |
|---|---|---|
| AEM Guides Components Content Package voor Cloud Service | dxml-components.all-1.2.2 | aem-site-template-dxml.all-1.0.15 |

## Opgeloste problemen

De fouten die in verschillende gebieden zijn gecorrigeerd, worden hieronder weergegeven:

### Authoring

- Het onderwerpdossier wordt niet ontgrendeld in de Redacteur van het Web, hoewel de Ontgrendel de optie van het Dossier en niet sparen optie worden geselecteerd. (1258)
- Kan een bestand niet uitchecken in de webeditor, ondanks dat u de optie NO hebt gekozen om de wijzigingen vóór het inchecken te verwijderen. (1257)
- De knopinfo voor de pictogrammen voor vergrendelen en ontgrendelen van bestanden op de hoofdwerkbalk in de webeditor is niet consistent met de pictogrammen die worden weergegeven in de weergave Opslagplaats.(12555)
- De optie Uitchecken annuleren en Ontgrendelen wordt weergegeven voor een bestand in de webeditor dat nog niet is uitgecheckt in de Kaartweergave. (12556)
- Kan de PDF-elementen niet selecteren in de bestaande &quot;topicref&quot;-koppelingen. (12477).
- In de weergave Opslagplaats kunnen de onderwerpen of afbeeldingen na gebruik van de functie Zoeken/Filteren niet meer worden gesleept. 12396
- De zoekresultaten worden uitgeschakeld in het deelvenster Zoeken en vervangen nadat een doorzocht bestand is geopend. 12142
- De cijfertoets &quot;8&quot; op het zijtoetsenbord werkt niet in de AEM Guides-editor. 12106

- Het voorvoegsel wordt gedupliceerd in de voorvertoningsmodus van de webeditor. (13133)
- `Choicetable` -rijen worden niet weergegeven of kunnen niet worden geselecteerd. 12616
- De Redacteur van het Web werpt bevestigingsfouten in specifieke scenario&#39;s wanneer het creëren van een onderwerp gebruikend een douaneschema. 12576
- De verwijzingen van het ditaval onderwerpmalplaatje leiden tot geen exemplaar in de inhoudsomslag wanneer het creëren van een kaart van het kaartmalplaatje. 12150
- Het zoekvak in DITA-kaarten heeft geen knop Sluiten. (11867)
- Wanneer u lange bestanden opslaat in de webeditor, genereert `DirtyChecker` een uitzondering met een lange stacktracering en worden de logbestanden gevuld. (11860)
- Het creëren van onderwerpen DITA vereist de toestemming van de Schrapping op de overeenkomstige omslagknoop, hoewel de kaart met schrijftoestemming kan worden gecreeerd. 11706
- De Redacteur van het Web toont een onjuiste titel wanneer een schuine streep aanwezig is. 10949


### Beheer

- Het veld &quot;title&quot; in de metagegevenseigenschappen van de DITA-kaart wordt overschreven door het element `<title>` voor de kaart. 10702
- De verwijzing van de inhoud is gebroken exemplaar-kleeft DITA- dossiers wanneer onderwerpidentiteitskaart niet het zelfde als GUID is. 12614
- In dynamische basislijnen, wordt de lijst van etiketten niet getrokken uit de directe verwijzingen van het werkende exemplaar van een kaart DITA. (1917)

### Publiceren

- Publiceren mislukt bij het wijzigen van de naam van een native PDF-voorinstelling. 12564
- Als u een native PDF-sjabloon dupliceert, wordt de standaardsjabloonlocatie gebruikt in plaats van de beschikbare aangepaste sjabloonlocatie. 12563

- Oorspronkelijke PDF | Als u meerdere Xrefs toevoegt, wordt de tekst breder dan de kolombreedte. 13004
- Oorspronkelijke PDF | Wanneer het onderwerp en de titel zelfde identiteitskaart hebben, leidt het tot een misvormde generatie van de output van PDF. (12644)
- Oorspronkelijke PDF | Bij het toevoegen van een outputklasse aan een ouder `<topicref>` element in een kaart DITA en het toepassen van douanestijl op de outputklasse, wordt het stileren toegepast op elementen binnen het onderwerplichaam, met inbegrip van sectitels.(12166)
- Incrementeel publiceren werkt niet als een DITA-kaart meerdere databases heeft. (1217)
- AEM-site | Bij het creëren van een kaart met keydef richtend aan een onderwerp als variabele en toevoegend verwerkings-rol=middel-slechts leidt tot sommige onverwachte pagina&#39;s. (12099)
- Als om het even welke activa van AEM DAM in om het even welke output buiten de plaats van AEM worden gebruikt, dan weerspiegelen de meta-gegevens &quot;jcr :createdBy&quot;niet de naam van de uitgever of de naam van de gebruiker die het DITA- kaart of onderwerp het laatst wijzigde. 12090
- AEM Sites | De DITA-kaart met padgegevens in de navtitle (met niet-ondersteunde tekens) leidt tot onjuiste pagina-URL&#39;s. (1978)
- Oorspronkelijke PDF | Er doen zich problemen voor ter ondersteuning van topichead / topicmeta / navtitle in FrontMatting en Backissue. (1969)
- Oorspronkelijke PDF | Het genereren van PDF&#39;s voor grote documenten kost veel tijd. (1955)
- Oorspronkelijke PDF | Als de naam van een voorinstelling wordt gewijzigd, wordt een NullPointerException gegenereerd terwijl een PDF-uitvoer wordt gegenereerd. (11889)
- De `<conref>` -inhoud wordt niet weergegeven in de PDF-uitvoer. (1131)
- Er wordt een extra spatie toegevoegd in de `<div>` -elementen bij het schakelen tussen de weergave Auteur en Source in de pagina-indelingseditor. 10750
- De inhoud die in AEM Cloud Manager wordt gerepliceerd, is niet zichtbaar in de instantie Publiceren. 9564

### Vertaling

- Het exporteren van een hernoemde basislijn voor een vertaling mislukt. (12993)
- De titel van het vertaalde bestand wordt weergegeven in plaats van de titel van het bronbestand. (11630)
