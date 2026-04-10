---
title: Opschoontaak voor B-boomstructuur configureren voor Cloud-services
description: Opschoontaak voor B-boomstructuur configureren voor Cloud-services
feature: Output Generation
role: Admin
level: Experienced
source-git-commit: 6f3f05419f4f5cdd45ab580cdee6fa869f20f01d
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# B-boomstructuur opschonen configureren

Stel de opschoontaak van de B-boomstructuur in en beheer de instelling `Guides BTree deletion` om uw systeem te optimaliseren en de opslag schoon te houden.

## B-boomstructuuropschoontaak configureren

Op de volgende tabbladen vindt u instructies voor het configureren van een opschoontaak in de B-structuur op basis van uw Experience Manager Guides-instellingen: Cloud Service of On-Premise.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

1. Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-config-override.md) om het configuratiedossier tot stand te brengen.

1. Geef in het configuratiebestand de volgende gegevens (eigenschap) op:

   | PID | Eigenschappensleutel | Waarde van eigenschap |
   |---|---|---|
   | `com.adobe.guides.utils.schedulers.GuidesBTreesCleanupSchedulerJob` | `cronExpression` | **Standaardwaarde:** &quot;0 0 * *?&quot; |

>[!TAB  Op locatie ]

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

>[!ENDTABS]

## Vorm de Schrapping van de Gidsen B-boom toelaten plaatsen

Op de volgende tabbladen vindt u instructies voor het inschakelen van de instelling op basis van de Experience Manager Guides-instellingen: Cloud Service of On-Premise.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

1. Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-config-override.md) om het configuratiedossier tot stand te brengen.

1. Geef in het configuratiebestand de volgende gegevens (eigenschap) op:

   | PID | Eigenschappensleutel | Waarde van eigenschap |
   |---|---|---|
   | `com.adobe.fmdita.config.ConfigManager` | `btree.deletion.enabled` | **Standaardwaarde:** &quot;Waar&quot; |

>[!TAB  Op locatie ]

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en selecteer *com.adobe.fmdita.config.ConfigManager* bundel.
1. Schakel de instelling `Guides btree deletion enabled` in.

   ![](assets/btree-cleanup-setting.png){align="left"}

1. Selecteer **sparen**.

>[!ENDTABS]