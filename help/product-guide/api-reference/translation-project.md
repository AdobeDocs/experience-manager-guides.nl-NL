---
title: Vertaalproject maken
description: Meer informatie over het maken van een API-vertaalproject
feature: Post-Processing Event Handler
role: Developer
level: Experienced
source-git-commit: 41dd3dee5f9d64fb5c58b5b302cc9759e48e3631
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 1%

---

# Vertaalproject maken

Een POST-methode waarmee u een vertaalproject kunt maken door de vereiste projectdetails te accepteren.

## Aanvraag-URL

`http://<aem-guides-server>:<port-number>/bin/guides/v1/translation/project/create`

## Type aanvraag

POST

## Parameters aanvragen

| Naam | Type | Beschrijving |
|----|----|-----------|
| `type` | String | newTranslationProject, xliffTranslationProject, newMultiLingualTranslationProject, addToExistingProject, newScopingTranslationProject |
| `versionDetails`, `versionSelector` | String | Basislijn, nieuwste versie, versionAsOfDate |
| `language` | String | Door komma&#39;s gescheiden talen &quot;de&quot;, &quot;fr&quot; |
| `map.id` | String | GUID van de bronkaart die moet worden vertaald |
| `map.path` | String | Pad van de te vertalen bronkaart |
| `referenceType` | String | Indirect, Direct |
| `fileType` | String | Kaart, Onderwerp, andere |
| `documentState` | String | kan een van de lijsten zijn die door het profiel van de gebruiker op de kaart worden toegewezen |
| `translationStatus` | String | Niet-gesynchroniseerd, In synchroon, Bijgewerkt, Verouderd, In uitvoering, Kopie ontbreekt, GEEN, N.v.t. |

>[!NOTE]
>
>U kunt `map.id` of `map.path` gebruiken bij het maken van een vertaalproject.

## Voorbeeld aanvragen

```JSON
{
  "title": "Test Project 1 on Dec 5",
  "type": "newTranslationProject",
  "translationDetails": {
    "map": {
      "id": "GUID-06527014-062d-46dc-8fea-48b4b4497c51-en",
      "path": "/content/dam/ajay-test/lang/en/m2.ditamap"
    },
    "languages": ["de"],
    "versionDetails": {
      "versionSelector": "latestVersion"
    }
  },
  "filterDetails": [
    { "name": "referenceType", "values": [] },
    { "name": "fileType", "values": [] },
    { "name": "documentState", "values": [] },
    { "name": "translationStatus", "values": [] }
   ]
```

## Responswaarden

```JSON
{
  "executionId": "5c13c571-3407-46d5-8f45-50ea9e05a212",
  "path": "/content/projects/test_project_1_ondec5"
}
```

**Codes van de Reactie**

- 200 succesvol
- 400 Ongeldige invoer
- 401 Onbevoegde toegang
- 500 interne serverfout

## Voorbeeldverzoeken

### Toevoegen aan bestaand project

```json
{
  "title": "Add to existing Project",
  "type": "addToExistingProject",
  "path": "/content/projects/test_project_1_existing",
  "translationDetails": {
    "map": {
      "id": "GUID-06527014-062d-46dc-8fea-48b4b4497c51-en"
    },
    "languages": ["de"],
    "versionDetails": {
      "versionSelector": "versionAsOfDate",
      "version": "2025-12-05T10:30:00+01:30"
    }
  },
  "filterDetails": [
    { "name": "referenceType", "values": [] },
    { "name": "fileType", "values": [] },
    { "name": "documentState", "values": [] },
    { "name": "translationStatus", "values": [] }
  ]
}
```

### Toevoegen aan bestaand project met basislijn

```json
{
  "title": "Add to existin project Project with baseline",
  "type": "addToExistingProject",
  "path": "/content/projects/existing_project_path",
  "translationDetails": {
    "map": {
      "id": "GUID-06527014-062d-46dc-8fea-48b4b4497c51-en"
    },
    "languages": ["de"],
    "versionDetails": {
      "versionSelector": "baseline",
      "version": "test1"
    }
  },
  "filterDetails": [
    { "name": "referenceType", "values": ["Direct"] },
    { "name": "fileType", "values": [] },
    { "name": "documentState", "values": [] },
    { "name": "translationStatus", "values": [] }
  ]
}
```

## Status van creatie van vertaalproject

Een GET API die de vertaalstatus voor een nieuw vertaalproject bijhoudt.

## Aanvraag-URL

`http://<aem-guides-server>:<port-number>/bin/guides/v1/translation/project/creationstatus`

## Type aanvraag

GET

## Parameters aanvragen

| Naam | Type | Beschrijving |
|----|----|-----------|
| `path` | String | Pad van het project |
| `languageStatusMap` | String | Retourneert voor elke aangevraagde taal de voltooiingsstatus: Bezig, Voltooid, Mislukt, Overgeslagen |


## Voorbeeld aanvragen

```json
{
  "path": "/content/projects/test_project_1_ondec5",
  "languageStatusMap": {
    "de": "Completed"
  }
}
```



