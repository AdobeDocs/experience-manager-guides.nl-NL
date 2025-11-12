---
title: B-boomstructuuropruimtaak configureren voor services op locatie
description: B-boomstructuuropruimtaak configureren voor services op locatie
feature: Output Generation
role: Admin
level: Experienced
source-git-commit: e1b332b100cc8e3937557e4617d66352c1a0dc3c
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# B-boomstructuur opschonen configureren

Stel de opschoontaak van de B-boomstructuur in en beheer de instelling `Guides B-tree deletion` om uw systeem te optimaliseren en de opslag schoon te houden.

## B-boomstructuuropschoontaak configureren

Voer de volgende stappen uit om B-boom schoonmaakbaan te vormen:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en selecteer *com.adobe.guides.utils.planners.GuidesBTreesCleanupSchedulerJob* bundel.

1. Werk de cron uitdrukking bij aan opstelling de de dienstloopfrequentie van de opschoonplanner van de B-boom.

1. Vorm de B-boom schoonmaakplanner zoals hieronder getoond.

   ![](assets/btree-cleanup-config.png){align="left"}

1. Selecteer **sparen**.


## Vorm de Schrapping van de Gidsen B-boom toelaten plaatsen

Voer de volgende stappen uit om de instelling in te schakelen:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en selecteer *com.adobe.fmdita.config.ConfigManager* bundel.
1. Schakel de instelling `Guides btree deletion enabled` in.

   ![](assets/btree-cleanup-setting.png){align="left"}

1. Selecteer **sparen**.

