---
title: API om bulkverwerking voor middelen te starten
description: Meer informatie over de API om bulkverwerking voor middelen te starten
feature: Post-Processing Event Handler
role: Developer
level: Experienced
source-git-commit: 8671a26bfee2d9e3b4e70a8f2615568c08c0a370
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 1%

---

# API om bulkverwerking voor middelen te starten

A POST method that initiates bulkasset processing for a specified path. Deze API ondersteunt zowel op JCR gebaseerde als op database gebaseerde verwerking van middelen. Het begint een asynchrone baan die alle activa onder de bepaalde weg en zijn sub-wegen verwerkt. Na initiatie retourneert de API een unieke processingID, die kan worden gebruikt om de taakstatus bij te houden.

**Verzoek URL**

`http://<aem-guides-server>:<port-number>/bin/guides/v1/assets/process`

**Parameters van het Verzoek**

| Naam | Type | Vereist | Beschrijving |
|----|----|--------|-----------|
| `path` | String | Ja | Absoluut pad van de map of het middel in de AEM-opslagplaats die moet worden verwerkt. |
| `excludedPaths` | String | Nee | Lijst met paden die moeten worden uitgesloten van verwerking |
| `type` | String | Ja | Soort verwerking die moet worden uitgevoerd. Bijvoorbeeld: ASSET_PROCESSING. |
| `filter` | Object | Nee | Filters die zijn toegepast op de geselecteerde elementen |

**de objecten van de Filter gebieden**

| Naam | Type | Beschrijving |
|----|----|-----------|
| fileTypes | String | Te verwerken elementtypen. Toegestane waarden: DITATOPIC, DITAMAP, MARKDOWN, HTML/CSS, DITAVAL, ANDERE. |
| startTime | Geheel | Ondergrens voor aanmaaktijd van elementen |
| endTime | Geheel | Bovengrens voor aanmaaktijd van middelen |

**Voorbeeld van het Verzoek**

```JSON
{
  "path": "/content/dam/status-fetch1",
  "excludedPaths": [
    "content/dam/status-fetch1/excluded-folder"
  ],
  "type": "ASSET_PROCESSING",
  "filter": {
        "fileTypes": ["DITAMAP", "DITATOPIC"],
        "startTime": 1758876933000
        "endTime": 1764932039000
    }
}
```

**waarden van de Reactie**

verwerkingsId aan opiniepeiling over om de status van asynchrone baan te krijgen.

```JSON
{
  "processingId": "akjhdfalkj1132"
}
```

**Codes van de Reactie**

- 200 succesvol
- 400 Ongeldige invoer
- 401 Onbevoegde toegang
- 500 interne serverfout

## Taakstatus controleren

Een GET-methode die de huidige status ophaalt van een eerder begonnen elementverwerkingstaak.

**Verzoek URL**

`http://<aem-guides-server>:<port-number>/bin/guides/v1/assets/process/status`

**Parameters van het Verzoek**

| Naam | Type | Vereist | Beschrijving |
|----|----|--------|-----------|
| `processingId` | String | Ja | De unieke id van de taak waarvan de status wordt gevraagd. |

**Voorbeeld van de Reactie**

```JSON
{
  "processingId": "string",
  "path": "string",
  "excludedPaths": ["string"],
  "status": "WAITING",
  "triggeredCount": 0,
  "startedAt": 0,
  "completedAt": 0,
  "hasLogs": true,
  "createdBy": "string",
  "type": "ASSET_PROCESSING",
  "migrationSet": {
    "totalFiles": 0,
    "calculationStatus": "WAITING"
  },
  "eta": {
    "value": 0,
    "unit": "string"
  },
  "comments": "string",
  "restartable": true,
  "resumable": true,
  "cancellable": true
}
```

**Codes van de Reactie**

- 200 succesvol
- 400 Ongeldige invoer
- 401 Onbevoegde toegang
- 500 interne serverfout

## Taaklogbestanden weergeven

Een GET-methode waarmee logbestanden voor een bepaalde taak-id worden opgehaald. Deze API haalt de logboeken van de elementverwerkingstaak op. De verwerkings-id is verplicht. De API biedt naast verschuivings- en limietparameters ook een eindstrategie.

**Verzoek URL**

`http://<aem-guides-server>:<port-number>/bin/guides/v1/assets/process/logs`

**Parameters van het Verzoek**

| Naam | Type | Vereist | Beschrijving |
|----|----|--------|-----------|
| `processingId` | String | Ja | De unieke id van de taak waarvan het logbestand moet worden weergegeven. |
| `offset` | Geheel | Nee | Het beginpunt (regelnummer) voor het lezen van logbestanden. Wordt gebruikt voor paginering om de eerste N-regels over te slaan. |
| `limit` | Geheel | Nee | Het maximumaantal loglijnen dat moet worden opgehaald. |
| `tail` | Geheel | Nee | Aantal logboeklijnen om van het eind terug te winnen. |


**Voorbeeld van de Reactie**

```JSON
{
  "lines": [
    "string"
  ],
  "limit": 0,
  "offset": 0,
  "hasMore": true
}
```

**Codes van de Reactie**

- 200 succesvol
- 400 Ongeldige invoer
- 401 Onbevoegde toegang
- 500 Interne serverfout


## Taaklogbestanden downloaden

Een GET-methode waarmee het logbestand voor een bepaalde taak wordt gedownload als een ZIP-bestand.

**Verzoek URL**

`http://<aem-guides-server>:<port-number>/bin/guides/v1/assets/process/logs/download`

**Parameters van het Verzoek**

| Naam | Type | Vereist | Beschrijving |
|----|----|--------|-----------|
| `processingId` | String | Ja | De unieke id van de taak waarvan het logbestand moet worden gedownload. |


**Voorbeeld van de Reactie**

```JSON
{
  "logFilePaths": [
    "string"
  ]
}
 
```

**Codes van de Reactie**

- 400 Ongeldige invoer
- 401 Onbevoegde toegang
- 500 Interne serverfout

## Taak annuleren

Een POST-API die een aanvraag voor de verwerking van bulkmiddelen annuleert. Als de taak niet wordt gevonden, retourneert de API een fout.

**Verzoek URL**

`http://<aem-guides-server>:<port-number>/bin/guides/v1/assets/process/cancel`

**Parameters van het Verzoek**

| Naam | Type | Vereist | Beschrijving |
|----|----|--------|-----------|
| `processingId` | String | Ja | De unieke id van de taak waarvan de status wordt gevraagd. |


**Codes van de Reactie**

- 200 succesvol
- 400 Ongeldige invoer
- 401 Onbevoegde toegang
- 500 Interne serverfout


## Taak hervatten

Een POST-API die een eerder geannuleerde of mislukte aanvraag voor de verwerking van bulkmiddelen opnieuw start. Het hervat verwerking vanaf het laatste controlepunt. Als de taak niet wordt gevonden of momenteel wordt uitgevoerd, retourneert de API een fout.

**Verzoek URL**

`http://<aem-guides-server>:<port-number>/bin/guides/v1/assets/process/resume`

**Parameters van het Verzoek**

| Naam | Type | Vereist | Beschrijving |
|----|----|--------|-----------|
| `processingId` | String | Ja | De unieke id van de taak waarvan de status wordt gevraagd. |


**Codes van de Reactie**

- 200 succesvol
- 400 Ongeldige invoer
- 401 Onbevoegde toegang
- 500 Interne serverfout

## Taakgeschiedenis weergeven

Een GET API die de laatste &#39;N&#39;-executies van Asset Naprocessing retourneert.

**Verzoek URL**

`http://<aem-guides-server>:<port-number>/bin/guides/v1/assets/process/history`

**Parameters van het Verzoek**

Geen. Deze GET-aanvraag haalt de taakgeschiedenis op zonder invoerparameters te vereisen.

**Voorbeeld van de Reactie**

```JSON
{
  "executionHistory": [
    {
      "processingId": "165f1de6-68c4-4dcd-9223-2b7242b62306",
      "path": "/content/dam/22858",
      "status": "SUCCESS",
      "triggeredCount": 6,
      "startedAt": 1761291362776,
      "completedAt": 1761291364026,
      "hasLogs": true,
      "createdBy": "user",
      "type": "ASSET_PROCESSING",
      "migrationSet": {
        "totalFiles": 6,
        "calculationStatus": "SUCCESS"
      },
      "eta": {
        "value": 0,
        "unit": "SECONDS"
      },
      "comments": "",
      "filter": {
        "fileTypes": [],
        "filterProcessedAssets": false
      },
      "cancellable": false,
      "resumable": false,
      "restartable": true
    }
  ]
}
```



