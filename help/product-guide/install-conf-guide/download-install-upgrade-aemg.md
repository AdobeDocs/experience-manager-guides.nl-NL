---
title: Upgrade uitvoeren van AEM Guides voor Cloud Service
description: Meer informatie over het upgraden van AEM Guides
feature: Installation
role: Admin
level: Experienced
source-git-commit: b416334318a83e882c32318bc4769d24268cdd1c
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---

# Upgrade uitvoeren van AEM Guides voor Cloud Service {#id213BD050YPH}

Voer de volgende stappen uit voor het upgraden van AEM Guides:

1. Open de Cloud Manager Git-opslagplaats.

1. Werk het `dox/dox.installer/pom.xml` bestand bij.

1. Werk de waarde van `dox.version` variabele bij naar de versiedetails die door Adobe worden geleverd.

1. Leg de wijzigingen vast en voer de Cloud Manager-pijplijn uit om het geüpgrade pakket te implementeren.


>[!NOTE]
>
> Voor meer details over het gebruiken van CI/CD pijpleiding, zie [&#x200B; Gebruik CI/CD Pijpleiding in Adobe Cloud Manager &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/cloud-manager/use-the-cicd-pipeline-in-cloud-manager-for-aem.html).

## Browser-cache wissen

Na het upgradeproces moeten alle gebruikers het cachegeheugen van de browser wissen voordat ze de geüpgrade versie van AEM Guides gebruiken.
