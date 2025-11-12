---
title: Asset-verwerking configureren voor services op locatie
description: Asset-verwerking configureren voor services op locatie
feature: Output Generation
role: Admin
level: Experienced
source-git-commit: e1b332b100cc8e3937557e4617d66352c1a0dc3c
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 0%

---

# Functie voor middelenverwerking configureren

Voer de volgende stappen uit om de functie voor middelenverwerking te configureren:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en selecteer *com.adobe.fmdita.config.ConfigManager* bundel.

1. Configureer de instelling `Enable Guides asset processing scheduled job` naar wens. De instelling wordt standaard ingeschakeld.

1. Selecteer **sparen**.
