---
title: REST API om een gegevensbronschakelaar te registreren
description: Meer informatie over de REST API om een gegevensbronaansluiting te registreren
exl-id: e2811892-c3cf-41f5-94d8-c2b37823a53a
source-git-commit: 5e0584f1bf0216b8b00f00b9fe46fa682c244e08
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# REST API om een gegevensbronschakelaar te registreren {#id236LG0Y0CXA}

Met de volgende REST API kunt u een gegevensbronaansluiting registreren.

## Een gegevensbronaansluiting registreren

Een methode van GET die een gegevensbronschakelaar registreert.

**Aanvraag-URL**:
`http://server:port/bin/guides/v1/konnect/config/register?path=<uploaded file path>`

**Parameter**: |Naam|Type|Vereist|Beschrijving| |—|—|—|—| |`path`|String|Yes|A string which points to a path in the AEM repository. Het kan een pad zijn in de `/content/dam or /var/dxml`.|

**Voorbeeld**:\
`http://host:4502/bin/guides/v1/konnect/config/register?path=/var/dxml/konnect/jira.json`
