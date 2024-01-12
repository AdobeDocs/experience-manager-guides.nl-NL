---
title: De installatie van AEM hulplijnen controleren
description: Leer hoe u de installatie van AEM hulplijnen kunt controleren
exl-id: 8e0afe18-5675-4c7e-b216-6de1a752bd01
feature: Installation
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---

# De installatie van AEM hulplijnen controleren {#id213BD030FBE}

Nadat u AEM hulplijnen hebt geïnstalleerd, moet u controleren of de installatie is gelukt of niet. Voer de volgende stappen uit om het installatieproces te controleren:

1. Meld u aan bij uw AEM en navigeer naar de pagina AEM webconsolegronnen. De standaard-URL voor toegang tot de bundelpagina is:

   ```http
   http://<server name>:<port>/system/console/bundles
   ```

   Er wordt een lijst met bundels weergegeven.

1. Filter de lijst met bundels door fmdita in te voeren in het filtertekstvak en druk op **Enter**.

   De lijst met bundels wordt gefilterd om de bundels weer te geven die door AEM hulplijnen zijn geïnstalleerd. Als de installatie is gelukt, hebben alle geïnstalleerde bundels een **Status** van **Actief**.

   Als een van de bundels geen **Actief** status, controleer dan de AEM logboeken om de installatiekwestie problemen op te lossen.


>[!IMPORTANT]
>
> Er zijn een aantal aanbevelingen voor het optimaliseren van de prestaties die u kunt overwegen om de systeemprestaties te verbeteren. Zie [Recommendations for performance optimization](download-install-recommend-perf-optimiz.md#) voor meer informatie.

**Bovenliggend onderwerp:**[ Downloaden en installeren](download-install.md)
