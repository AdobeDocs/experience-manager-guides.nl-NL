---
title: De installatie van AEM hulplijnen controleren
description: Leer hoe u de installatie van AEM hulplijnen kunt controleren
exl-id: 4e566c57-a522-4605-bc70-47155f20b429
source-git-commit: 5e0584f1bf0216b8b00f00b9fe46fa682c244e08
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# De installatie van AEM hulplijnen controleren {#id213BD030FBE}

Nadat u AEM hulplijnen hebt geïnstalleerd, moet u controleren of de installatie is gelukt of niet. Voer de volgende stappen uit om de installatie te verifiëren:

1. Open de Developer Console van uw Cloud Service.

   Ga voor meer informatie over toegang tot de Developer Console naar [Toegang tot ontwikkelconsole](https://experienceleague.adobe.com/docs/experience-manager-learn/cloud-service/debugging/debugging-aem-as-a-cloud-service/developer-console.html) in AEM documentatie.

1. Open de lijst met OSGi-bundels in AEM.

   Voor meer informatie over het openen van bundels raadpleegt u [Bundels](https://experienceleague.adobe.com/docs/experience-manager-learn/cloud-service/debugging/debugging-aem-as-a-cloud-service/developer-console.html?lang=en#bundles) in AEM documentatie.

1. Zoek naar fmdita in de lijst van bundels en controleer zijn status.

   De status moet *Actief* voor correct geïmplementeerde bundels. Als om het even welke bundel geen Actieve status heeft, dan controleer de AEM logboeken om de installatiekwestie problemen op te lossen.


**Bovenliggend onderwerp:**[ Downloaden en installeren](download-install.md)
