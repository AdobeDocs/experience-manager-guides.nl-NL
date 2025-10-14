---
title: AEM Guides-installatie verifiëren
description: Meer informatie over het verifiëren van AEM Guides-installatie
exl-id: 4e566c57-a522-4605-bc70-47155f20b429
feature: Installation
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# AEM Guides-installatie verifiëren {#id213BD030FBE}

Nadat u AEM Guides hebt geïnstalleerd, moet u controleren of de installatie is gelukt of niet. Voer de volgende stappen uit om de installatie te verifiëren:

1. Open de Developer Console van je Cloud Service.

   Voor details om tot Developer Console toegang te hebben, zie {de toegang van 0} Developer Console [&#128279;](https://experienceleague.adobe.com/docs/experience-manager-learn/cloud-service/debugging/debugging-aem-as-a-cloud-service/developer-console.html?lang=nl-NL) in AEM documentatie.

1. Open de lijst met OSGi-bundels in AEM.

   Voor details om tot Bundels toegang te hebben, zie [&#x200B; Bundels &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-learn/cloud-service/debugging/debugging-aem-as-a-cloud-service/developer-console.html?lang=nl-NL#bundles) in AEM documentatie.

1. Zoek naar fmdita in de lijst van bundels en controleer zijn status.

   De status zou *Actief* voor met succes opgestelde bundels moeten tonen. Als om het even welke bundel geen Actieve status heeft, dan controleer de AEM logboeken om de installatiekwestie problemen op te lossen.


**Bovenliggend onderwerp:**&#x200B;[&#x200B; Download en installeer &#x200B;](download-install.md)
