---
title: REST API's voor conversieworkflow
description: Meer informatie over de REST API's voor de conversieworkflow
exl-id: f091782e-ab54-4db4-9018-9bcbff9da7b2
feature: Rest API Conversion Workflow
role: Developer
level: Experienced
source-git-commit: 45ae1471fe0f0586764ede9dd96530b7f75f69ee
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# REST API&#39;s voor conversieworkflow {#id175UB30E05Z}

Met de volgende REST API&#39;s kunt u Word-, HTML- en InDesign-documenten converteren naar DITA-indeling.

## Word-documenten converteren

A GET method that converts Word documents into DITA format.

**Verzoek URL**:
http://*&lt;aem-guides-server\>*: *&lt;port-number\>*/bin/fmdita/conversion

| Naam | Type | Vereist | Beschrijving |
|----|----|--------|-----------|
| ``operation`` | String | Ja | Naam van de bewerking die wordt aangeroepen. De waarde van deze parameter is ``word2dita`` . <br> **Nota:** de waarde is case-insensitive. |
| `inputFile` | String | Ja | Absoluut pad van de Word-bronbestanden in AEM opslagplaats. |
| `destPath` | String | Ja | Absoluut pad van de doellocatie waar de geconverteerde DITA-bestanden worden opgeslagen. |
| `createRev` | Boolean | Ja | Geef op of er een revisie van de bestanden \( `true`\) op het opgegeven doel wordt gemaakt of niet \( `false`\). Dit wordt alleen overwogen wanneer de doellocatie een bestaande versie van de omgezette bestanden bevat. |
| `style2tagMap` | String | Ja | Absoluut pad van het stijltoewijzingsbestand dat wordt gebruikt voor conversie. |

**waarden van de Reactie**:
Retourneert een HTTP 200 \(Successful\) reactie.

## HTML-documenten converteren

A GET method that converts HTML documents into DITA format.

**Verzoek URL**:

http://*&lt;aem-guides-server\>*: *&lt;port-number\>*/bin/fmdita/conversion

**Parameters**:

| Naam | Type | Vereist | Beschrijving |
|----|----|--------|-----------|
| `operation` | String | Ja | Naam van de bewerking die wordt aangeroepen. De waarde van deze parameter is ``html2dita`` . <br> **Nota:** de waarde is case-insensitive. |
| `inputFile` | String | Ja | Absoluut pad van de HTML-bronbestanden in AEM opslagplaats. |
| `destPath` | String | Ja | Absoluut pad van de doellocatie waar de geconverteerde DITA-bestanden worden opgeslagen. |
| `createRev` | Boolean | Ja | Geef op of er een revisie van de bestanden \( `true`\) op het opgegeven doel wordt gemaakt of niet \( `false`\). Dit wordt alleen overwogen wanneer de doellocatie een bestaande versie van de omgezette bestanden bevat. |

**waarden van de Reactie**:

Retourneert een HTTP 200 \(Successful\) reactie.

## InDesign-documenten converteren

A GET method that converts InDesign documents into DITA format.

**Verzoek URL**:
http://*&lt;aem-guides-server\>*: *&lt;port-number\>*/bin/fmdita/conversion

**Parameters**:

| Naam | Type | Vereist | Beschrijving |
|----|----|--------|-----------|
| ``operation`` | String | Ja | Naam van de bewerking die wordt aangeroepen. De waarde van deze parameter is ``idml2dita`` . <br> **Nota:** de waarde is case-insensitive. |
| `inputFile` | String | Ja | Absoluut pad van de bronbestanden van het InDesign in AEM opslagplaats. |
| `destPath` | String | Ja | Absoluut pad van de doellocatie waar de geconverteerde DITA-bestanden worden opgeslagen. |
| `createRev` | Boolean | Ja | Geef op of er een revisie van de bestanden \( `true`\) op het opgegeven doel wordt gemaakt of niet \( `false`\). Dit wordt alleen overwogen wanneer de doellocatie een bestaande versie van de omgezette bestanden bevat. |

**waarden van de Reactie**:
Retourneert een HTTP 200 \(Successful\) reactie.
