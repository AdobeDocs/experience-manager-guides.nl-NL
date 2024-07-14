---
title: REST API om een gegevensbronschakelaar te registreren
description: Meer informatie over de REST API om een gegevensbronaansluiting te registreren
exl-id: e2811892-c3cf-41f5-94d8-c2b37823a53a
feature: Rest API Data Source
role: Developer
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# REST API om een gegevensbronschakelaar te registreren {#id236LG0Y0CXA}

Met de volgende REST API kunt u een gegevensbronaansluiting registreren.

## Een gegevensbronaansluiting registreren

Een methode van GET die een gegevensbronschakelaar registreert.

**Verzoek URL**:
`http://server:port/bin/guides/v1/konnect/config/register?path=<uploaded file path>`

**Parameter**:
|Naam|Type|Vereist|Beschrijving|
|—|—|—|—|
|`path`|String|Yes|A string which points to a path in the AEM repository. Het kan een pad zijn in de `/content/dam or /var/dxml` .|

**Voorbeeld**:\
`http://host:4502/bin/guides/v1/konnect/config/register?path=/var/dxml/konnect/jira.json`
