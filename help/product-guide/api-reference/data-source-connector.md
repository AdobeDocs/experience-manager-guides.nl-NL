---
title: REST API om een gegevensbronschakelaar te registreren
description: Meer informatie over de REST API om een gegevensbronaansluiting te registreren
exl-id: e2811892-c3cf-41f5-94d8-c2b37823a53a
feature: Rest API Data Source
role: Developer
level: Experienced
source-git-commit: b4762314ec5269abe62b622184f1724762a6cfa0
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 1%

---

# REST API om een gegevensbronschakelaar te registreren {#id236LG0Y0CXA}

Met de volgende REST API kunt u een gegevensbronaansluiting registreren.

## Een gegevensbronaansluiting registreren

Een methode van GET die een gegevensbronschakelaar registreert.

**Verzoek URL**:
`http://server:port/bin/guides/v1/konnect/config/register?path=<uploaded file path>`

**Parameter**:

| Naam | Type | Vereist | Beschrijving |
|----|----|--------|-----------|
| `path` | String | Ja | Een tekenreeks die naar een pad in de AEM opslagplaats wijst. Dit kan een pad zijn in de `/content/dam or /var/dxml` . |

**Voorbeeld**:\
`http://host:4502/bin/guides/v1/konnect/config/register?path=/var/dxml/konnect/jira.json`
