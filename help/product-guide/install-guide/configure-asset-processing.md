---
title: Asset-verwerking configureren voor services op locatie
description: Asset-verwerking configureren voor services op locatie
feature: Output Generation
role: Admin
level: Experienced
exl-id: 9d771bba-aa90-4726-a75f-1cb7b804a192
hidefromtoc: true
source-git-commit: 3aadc59f5034828cf319992b7acb32d5a88eaf93
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
