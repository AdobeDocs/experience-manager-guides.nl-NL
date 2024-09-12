---
title: REST API's voor uitvoerbeheer
description: Meer informatie over REST API's voor uitvoerbeheer
exl-id: dab654f5-555d-4a89-bc94-55b1e938f255
feature: Rest API Output Management
role: Developer
level: Experienced
source-git-commit: 45ae1471fe0f0586764ede9dd96530b7f75f69ee
workflow-type: tm+mt
source-wordcount: '1175'
ht-degree: 0%

---

# REST API&#39;s voor uitvoerbeheer {#id175UB30E05Z}

De volgende REST API&#39;s zijn beschikbaar voor het beheer van de uitvoer in AEM Guides.

## Alle uitvoervoorinstellingen voor een DITA-kaart ophalen {#get-output-presets-dita-map}

Een methode van de POST die alle die outputvoorinstellingen terugwint voor een kaart DITA worden gevormd.

**Verzoek URL**:
http://*&lt;aem-guides-server\>*: *&lt;port-number\>*/bin/publishlistener

**Parameters**:

| Naam | Type | Vereist | Beschrijving |
|----|----|--------|-----------|
| `:operation` | String | Ja | Naam van de bewerking die wordt aangeroepen. De waarde van deze parameter is `getalloutputs`.<br> **Nota:** de waarde is case-insensitive. |
| `sourcePath` | String | Ja | Absoluut pad van het DITA-kaartbestand. |

**waarden van de Reactie**:
Retourneert een array van objecten met JSON Output Preset, elk object dat de volgende elementen bevat:

| Element | Beschrijving |
|-------|-----------|
| `outputName` | Naam van de uitvoervoorinstelling. Uitvoernamen zijn uniek in het bereik van de DITA-kaart waarin ze zijn gedefinieerd. |
| `outputType` | Type uitvoer dat is gegenereerd met deze voorinstelling, bijvoorbeeld AEM Site, PDF, EPUB of andere. De beschikbare opties zijn:<br>-   AEMSITE <br>-   PDF <br>-   HTML5 <br>-   EPUB <br>-   AANGEPAST |
| `outputTitle` | Een beschrijvende naam voor de instellingen van de uitvoervoorinstelling. Hiermee definieert u de waarde voor de eigenschap Naam instellen voor de uitvoervoorinstelling. |
| `ditaValPathList` | Array met DITAVAL-bestandspaden die moet worden gebruikt om de gewenste uitvoer te genereren. |
| `targetPath` | Pad waar de uitvoer wordt gepubliceerd of opgeslagen. |
| `siteName` | *\(Voor AEM Site-uitvoer\)* Naam van de AEM-site. |
| `templatePath` | *\ (voor AEM output \ van de Plaats)* Weg van de malplaatjeknoop die moet worden gebruikt om de gewenste output te produceren. |
| `searchScope` | Geef het bereik voor de zoekopdracht op. De waarde voor deze parameter moet worden ingesteld op `local` . |
| `generateTOC` | *\(Voor AEM Site-uitvoer\)* Geef op of een inhoudsopgave \(true\) moet worden gegenereerd of niet \(false\). |
| `generateBreadcrumbs` | *\(Voor AEM Site-uitvoer\)* Geef op of de broodkruimels \(true\) worden gegenereerd of niet \(false\). |
| `overwriteStrategy` | *\(Voor AEM Site-uitvoer\)* Geef op of bestanden op de bestemming \(true\) worden overschreven of niet \(false\). |
| `pdfGenerator` | Geef de PDF-genereringsengine op die u wilt gebruiken. De mogelijke waarden zijn:<br> -   DITAOT <br>-   FMPS |

>[!NOTE]
>
> `DitaValPath` -element wordt niet meer ondersteund.

## Uitvoervoorinstelling maken

Een methode van de POST die tot een nieuwe output vooraf instelt voor een kaart DITA.

**Verzoek URL**:
http://*&lt;aem-guides-server\>*: *&lt;port-number\>*/bin/publishlistener

**Parameters**:

| Naam | Type | Vereist | Beschrijving |
|----|----|--------|-----------|
| `:operation` | String | Ja | Naam van de bewerking die wordt aangeroepen. De waarde van deze parameter is ``createoutput``.<br> **Nota:** de waarde is case-insensitive. |
| `sourcePath` | String | Ja | Absoluut pad van het DITA-kaartbestand. |
| `outputTitle` | String | Ja | Een beschrijvende naam voor de instellingen van de uitvoervoorinstelling. Dit wordt gebruikt om de waarde voor het Plaatsende bezit van de Naam voor de output vooraf ingesteld te bepalen.<br> **Nota:** wanneer een nieuwe output vooraf ingesteld wordt gecreeerd, drijft het achterste deelsysteem een unieke naam voor de output vooraf ingesteld van de bepaalde titel. |
| `outputType` | String | Ja | Type uitvoer dat is gegenereerd met deze voorinstelling, bijvoorbeeld AEM Site, PDF, EPUB of andere. De beschikbare opties zijn:<br>-   AEMSITE <br>-   PDF <br>-   HTML5 <br>-   EPUB <br>-   AANGEPAST |

**waarden van de Reactie**:

| Element | Beschrijving |
|-------|-----------|
| `outputName` | Een unieke naam voor de nieuwe uitvoervoorinstelling. Deze naam wordt afgeleid van de waarde van de parameter `outputTitle` . |

## Uitvoervoorinstelling opslaan

Een methode van de POST die veranderingen bewaart die in een outputvooraf ingesteld worden aangebracht.

**Verzoek URL**:
http://*&lt;aem-guides-server\>*: *&lt;port-number\>*/bin/publishlistener

**Parameters**:

| Naam | Type | Vereist | Beschrijving |
|----|----|--------|-----------|
| `:operation` | String | Ja | Naam van de bewerking die wordt aangeroepen. De waarde van deze parameter is ``saveoutput``.<br> **Nota:** de waarde is case-insensitive. |
| `sourcePath` | String | Ja | Absoluut pad van het DITA-kaartbestand. |
| `outputObj` | String | Ja | Een JSON-object dat eigenschappen bevat van de uitvoervoorinstelling die wordt bijgewerkt. De eigenschap `outputObj.outputName` bevat de naam van de uitvoervoorinstelling die moet worden bijgewerkt. Voor het formaat van het voorwerp JSON, zie de **waarden van de Reactie** lijst in [ krijgt alle outputvoorinstellingen voor een kaart DITA ](#get-output-presets-dita-map). |

**waarden van de Reactie**:
Retourneert een HTTP 200 \(Successful\) reactie.

## Een specifieke uitvoervoorinstelling ophalen

Een POST-methode waarmee een bestaande uitvoervoorinstelling wordt opgehaald.

**Verzoek URL**:
http://*&lt;aem-guides-server\>*: *&lt;port-number\>*/bin/publishlistener

**Parameters**:

| Naam | Type | Vereist | Beschrijving |
|----|----|--------|-----------|
| `:operation` | String | Ja | Naam van de bewerking die wordt aangeroepen. De waarde van deze parameter is `getoutput` . <br>**Nota:** de waarde is case-insensitive. |
| `sourcePath` | String | Ja | Absoluut pad van het DITA-kaartbestand. |
| `outputName` | String | Ja | Naam van de uitvoervoorinstelling waarvoor de details moeten worden opgehaald. |

**waarden van de Reactie**:

| Element | Beschrijving |
|-------|-----------|
| `outputName` | Naam van de uitvoervoorinstelling. Uitvoernamen zijn uniek in het bereik van de DITA-kaart waarin ze zijn gedefinieerd. |
| `outputType` | Type uitvoer dat is gegenereerd met deze voorinstelling, bijvoorbeeld AEM Site, PDF, EPUB of andere. De beschikbare opties zijn:<br>-   AEMSITE <br>-   PDF <br>-   HTML5 <br>-   EPUB <br>-   AANGEPAST <br> |
| `outputTitle` | Een beschrijvende naam voor de instellingen van de uitvoervoorinstelling. Hiermee definieert u de waarde voor de eigenschap Naam instellen voor de uitvoervoorinstelling. |
| `ditaValPathList` | Array met DITAVAL-bestandspaden die moet worden gebruikt om de gewenste uitvoer te genereren. |
| `targetPath` | Pad waar de uitvoer wordt gepubliceerd of opgeslagen. |
| `siteName` | \(Voor AEM Site-uitvoer\) Naam van de AEM Site. |
| `siteTitle` | \(Voor AEM Site-uitvoer\) Titel van de AEM Site. |
| `templatePath` | \(Voor AEM Site-uitvoer\) pad van het sjabloonknooppunt dat moet worden gebruikt om de gewenste uitvoer te genereren. |
| `searchScope` | Geef het bereik voor de zoekopdracht op. De waarde voor deze parameter moet worden ingesteld op `local` . |
| `generateTOC` | \(Voor AEM Site-uitvoer\) Geef op of een inhoudsopgave moet worden gegenereerd \(true\) of niet \(false\). |
| `generateBreadcrumbs` | \(Voor AEM Site-uitvoer\) Geef op of de broodkruimels \(true\) worden gegenereerd of niet \(false\). |
| `overwriteFiles` | \(Voor AEM Site-uitvoer\) Geef op of bestanden op de bestemming \(true\) worden overschreven of niet \(false\). |
| `pdfGenerator` | Geef de PDF-genereringsengine op die u wilt gebruiken. De mogelijke waarden zijn:<br> -   DITAOT <br>-   FMPS |

>[!NOTE]
>
> `DitaValPath` -element wordt niet meer ondersteund.

## Uitvoer genereren

Een methode van de GET die output gebruikend één of meerdere output vooraf instelt produceert.

**Verzoek URL**:
http://*&lt;aem-guides-server\>*: *&lt;port-number\>*/bin/publishlistener

**Parameters**:

| Naam | Type | Vereist | Beschrijving |
|----|----|--------|-----------|
| `operation` | String | Ja | Naam van de bewerking die wordt aangeroepen. De waarde van deze parameter is `GENERATEOUTPUT`.<br> **Nota:** de waarde is case-sensitive. |
| `source` | String | Ja | Absoluut pad van het DITA-kaartbestand. |
| `outputName` | String | Ja | Naam van de uitvoervoorinstelling\(en\) die moet worden gebruikt om uitvoer te genereren. U kunt meerdere uitvoervoorinstellingen opgeven met een scheidingsteken voor de pipe \(&quot;\|&quot;\), bijvoorbeeld `aemsite|pdfoutput` . |

**waarden van de Reactie**:
Retourneert een HTTP 200 \(Successful\) reactie.

## Incrementele uitvoer genereren

Een methode van GET die stijgende output voor een AEMPlaats gebruikend één of meerdere output vooraf instelt produceert.

**Verzoek URL**:
http://*&lt;aem-guides-server\>*: *&lt;port-number\>*/bin/publishlistener

**Parameters**:

| Naam | Type | Vereist | Beschrijving |
|----|----|--------|-----------|
| `operation` | String | Ja | Naam van de bewerking die wordt aangeroepen. De waarde van deze parameter is `INCREMENTALPUBLISH` . <br>**Nota:** de waarde is case-sensitive. |
| `contentPath` | JSON | Ja | Absoluut pad van het DITA-toewijzingsbestand en onderwerpbestanden samen met de naam van uitvoervoorinstellingen. Gebruik het volgende voorbeeld als bouwsteen: |

```XML
{
   {   
   "ditamap": 
      "/content/dam/sample/sample.ditamap",   
   "topics": [     
      "/content/dam/sample/topic1.xml",     
      "/content/dam/sample/topic2.xml"   
         ],   
   "fullMaps": [     
      "/content/dam/sample/submap.ditamap"   
      ],   
   "maps": [     
      "/content/dam/sample/keyspace.ditamap"   
      ],   
   "outputs": [     
      "aemsite"   
      ] 
   }
}
```

- Het attribuut `ditamap` neemt de absolute weg van de kaart DITA die wordt gebruikt om de output te produceren.
- Het attribuut `topics` neemt een serie van onderwerpen die worden bijgewerkt en moeten opnieuw worden gepubliceerd.
- Het attribuut `fullMaps` bevat weg van de kaartdossiers \ (als afgeknotte submaps \) die samen met hun onderwerpen voor stijgende outputgeneratie nodig zijn.
- Het kenmerk `maps` bevat het pad van de kaartbestanden \(voor het oplossen van toetsruimteverwijzingen\) die zonder onderwerpen op de schijf worden geëxtraheerd.
- Het kenmerk `outputs` neemt een array met namen van uitvoervoorinstellingen die worden gebruikt om de uitvoer te genereren.

**waarden van de Reactie**:
Retourneert een HTTP 200 \(Successful\) reactie.

## Uitvoervoorinstelling verwijderen

Een POST-methode waarmee een uitvoervoorinstelling wordt verwijderd.

**Verzoek URL**:
http://*&lt;aem-guides-server\>*: *&lt;port-number\>*/bin/publishlistener

**Parameters**:

| Naam | Type | Vereist | Beschrijving |
|----|----|--------|-----------|
| `:operation` | String | Ja | Naam van de bewerking die wordt aangeroepen. De waarde van deze parameter is `deleteoutput`.<br> **Nota:** de waarde is case-insensitive. |
| `sourcePath` | String | Ja | Absoluut pad van het DITA-kaartbestand. |
| `outputName` | String | Ja | Naam van de uitvoervoorinstelling die moet worden verwijderd. |

**waarden van de Reactie**:
Retourneert een HTTP 200 \(Successful\) reactie.
