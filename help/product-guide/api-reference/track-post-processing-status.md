---
title: API om naverwerking voor een map of middel bij te houden
description: Meer informatie over de API voor het bijhouden van de naverwerking voor een map of middel
feature: Post-Processing Event Handler
role: Developer
level: Experienced
source-git-commit: 558108650aeeeda440895972e460fa523b804bb2
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 1%

---

# API om de status van naverwerking voor een map of middel bij te houden

Hieronder volgt een POST-methode waarmee een asynchrone taak wordt gestart om de status van elementen op te halen.

## De status van elementen in hulplijnen zoeken

**Verzoek URL**

`http://<aem-guides-server>:<port-number>bin/guides/v1/assets/status `

**Parameters**

| Naam | Type | Vereist | Beschrijving |
|----|----|--------|-----------|
| `path` | String | Ja | Map- of middelenpad waarvoor de status moet worden opgehaald. |
| `excludedPaths` | String | Nee | Mappaden die moeten worden uitgesloten van de bovenstaande lijst. |

```JSON
{ 

    "paths": [ 

        "/content/dam/status-fetch1", 

        "/content/dam/status-fetch2" 

    ], 

    "excludedPaths": [ 

        "content/dam/status-fetch1/excluded-folder" 

    ] 

} 
```

**waarden van de Reactie**
jobId die moet worden opiniepeild om de status van een asynchrone taak op te halen.

```JSON
{ 

  "jobId": "akjhdfalkj1132", 

  "status": "WAITING", 

 

} 
```

## Poller-API

Een GET-methode waarmee de status van een asynchrone taak wordt opgehaald die door de bovenstaande API wordt uitgevoerd.

**Verzoek URL**

`http://<aem-guides-server>:<port-number>bin/guides/v1/assets/status`

**Parameters**

| Naam | Type | Vereist | Beschrijving |
|----|----|--------|-----------|
| `jobId` | String | Ja | Taak-id die is geretourneerd door de bovenstaande API. |

**waarden van de Reactie**

Lijst van elementen en hun status.

```JSON
{ 

  "jobId": " akjhdfalkj1132", 

  "status": "SUCCESS", 

  "assets": [ 

    { 

      "path": "/content/dam/status-fetch1/a.dita", 

      "uuid": "GUID-1293914ansd", 

      "status": "SUCCESS", 

      "exists": true 

    }, 

    { 

      "path": "/content/dam/status-fetch1/b.dita", 

      "uuid": "GUID-1883241", 

      "status": "FAILURE", 

      "exists": true 

    } 

 

  ] 

} 
```

**de waarden van de Status:** SUCCESS, MISLUKKEN, VERWERKING, IN BEHANDELING
