---
title: Upgrade uitvoeren voor AEM Guides
description: Meer informatie over het upgraden van AEM Guides
exl-id: 57ae906f-69e3-4319-89f6-0fa9ddb7a3ff
feature: Installation
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---

# Upgrade uitvoeren voor AEM Guides {#id213BD050YPH}

1. Open de Cloud Manager Git-opslagplaats.

1. Werk het bestand dox/dox.installer/pom.xml bij.

1. Werk de waarde van de variabele dox.version bij tot de versiedetails die door Adobe worden verstrekt.

1. Leg de wijzigingen vast en voer de Cloud Manager-pijplijn uit om het geüpgrade pakket te implementeren.


>[!NOTE]
>
> Voor meer details over het gebruiken van CI/CD pijpleiding, zie [&#x200B; Gebruik CI/CD Pijpleiding in Adobe Cloud Manager &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/cloud-manager/use-the-cicd-pipeline-in-cloud-manager-for-aem.html?lang=nl-NL).

## Browser-cache wissen

Na het upgradeproces moeten alle gebruikers het cachegeheugen van de browser wissen voordat ze de geüpgrade versie van AEM Guides gebruiken.

**Bovenliggend onderwerp:**&#x200B;[&#x200B; Download en installeer &#x200B;](download-install.md)
