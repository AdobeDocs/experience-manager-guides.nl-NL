---
title: AEM Guides-installatie verifiëren
description: Meer informatie over het verifiëren van AEM Guides-installatie
exl-id: 4e566c57-a522-4605-bc70-47155f20b429
feature: Installation
role: Admin
level: Experienced
hidefromtoc: true
source-git-commit: 564ee1731be2378744ffd2ed54a2fd423901a0b3
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# AEM Guides-installatie verifiëren {#id213BD030FBE}

Nadat u AEM Guides hebt geïnstalleerd, moet u controleren of de installatie is gelukt of niet. Voer de volgende stappen uit om de installatie te verifiëren:

1. Open de Developer Console van je Cloud Service.

   Voor details om tot Developer Console toegang te hebben, zie {de toegang van 0} Developer Console [&#x200B; in de documentatie van AEM.](https://experienceleague.adobe.com/docs/experience-manager-learn/cloud-service/debugging/debugging-aem-as-a-cloud-service/developer-console.html?lang=nl-NL)

1. Open de lijst met OSGi-bundels in AEM.

   Voor details om tot Bundels toegang te hebben, zie [&#x200B; Bundels &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-learn/cloud-service/debugging/debugging-aem-as-a-cloud-service/developer-console.html?lang=nl-NL#bundles) in de documentatie van AEM.

1. Zoek naar fmdita in de lijst van bundels en controleer zijn status.

   De status zou *Actief* voor met succes opgestelde bundels moeten tonen. Als een van de pakketten geen actieve status heeft, controleert u de AEM-logboeken om het installatieprobleem op te lossen.


**Bovenliggend onderwerp:**&#x200B;[&#x200B; Download en installeer &#x200B;](download-install.md)
