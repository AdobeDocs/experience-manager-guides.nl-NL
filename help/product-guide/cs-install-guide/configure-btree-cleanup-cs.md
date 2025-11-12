---
title: Opschoontaak voor B-boomstructuur configureren voor Cloud-services
description: Opschoontaak voor B-boomstructuur configureren voor Cloud-services
feature: Output Generation
role: Admin
level: Experienced
source-git-commit: 5b29b2b5f725b5d9a2029fb232e62f387a5338fd
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# B-boomstructuur opschonen configureren

Stel de opschoontaak van de B-boomstructuur in en beheer de instelling `Guides BTree deletion` om uw systeem te optimaliseren en de opslag schoon te houden.

## B-boomstructuuropschoontaak configureren

Voer de volgende stappen uit om B-boom schoonmaakbaan te vormen:

1. Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](../cs-install-guide/download-install-additional-config-override.md) om het configuratiedossier tot stand te brengen.

1. Geef in het configuratiebestand de volgende gegevens (eigenschap) op:

   | PID | Eigenschappensleutel | Waarde van eigenschap |
   |---|---|---|
   | `com.adobe.guides.utils.schedulers.GuidesBTreesCleanupSchedulerJob` | `cronExpression` | **Standaardwaarde:** &quot;0 0 * *?&quot; |


## Vorm de Schrapping van de Gidsen B-boom toelaten plaatsen

Voer de volgende stappen uit om de instelling in te schakelen:

1. Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](../cs-install-guide/download-install-additional-config-override.md) om het configuratiedossier tot stand te brengen.

1. Geef in het configuratiebestand de volgende gegevens (eigenschap) op:

   | PID | Eigenschappensleutel | Waarde van eigenschap |
   |---|---|---|
   | `com.adobe.fmdita.config.ConfigManager` | `btree.deletion.enabled` | **Standaardwaarde:** &quot;Waar&quot; |