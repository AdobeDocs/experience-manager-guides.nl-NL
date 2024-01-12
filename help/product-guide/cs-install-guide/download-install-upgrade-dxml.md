---
title: Upgrade uitvoeren AEM hulplijnen
description: Leer hoe u AEM hulplijnen kunt bijwerken
exl-id: 57ae906f-69e3-4319-89f6-0fa9ddb7a3ff
feature: Installation
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---

# Upgrade uitvoeren AEM hulplijnen {#id213BD050YPH}

1. Open de Git-opslagplaats van uw Cloud Manager.

1. Werk het bestand dox/dox.installer/pom.xml bij.

1. Werk de waarde van de variabele dox.version bij tot de versiedetails die door Adobe worden verstrekt.

1. Leg de wijzigingen vast en voer de Cloud Manager-pijplijn uit om het geüpgrade pakket te implementeren.


>[!NOTE]
>
> Voor meer details over het gebruiken van pijpleiding CI/CD, zie [De CI/CD-pijpleiding gebruiken in Adobe Cloud Manager](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/cloud-manager/use-the-cicd-pipeline-in-cloud-manager-for-aem.html).

## Browser-cache wissen

Na het verbeteringsproces, moeten alle gebruikers het browser geheime voorgeheugen ontruimen alvorens de promotieversie van AEMGidsen te gebruiken.

**Bovenliggend onderwerp:**[ Downloaden en installeren](download-install.md)
