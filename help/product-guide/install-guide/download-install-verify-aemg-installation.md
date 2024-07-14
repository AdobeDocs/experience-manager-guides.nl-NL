---
title: AEM Guides-installatie verifiëren
description: Meer informatie over het verifiëren van AEM Guides-installatie
exl-id: 8e0afe18-5675-4c7e-b216-6de1a752bd01
feature: Installation
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---

# AEM Guides-installatie verifiëren {#id213BD030FBE}

Nadat u AEM Guides hebt geïnstalleerd, moet u controleren of de installatie is gelukt of niet. Voer de volgende stappen uit om het installatieproces te controleren:

1. Meld u aan bij uw AEM en navigeer naar de pagina AEM webconsolegronnen. De standaard-URL voor toegang tot de bundelpagina is:

   ```http
   http://<server name>:<port>/system/console/bundles
   ```

   Er wordt een lijst met bundels weergegeven.

1. Filter de lijst van bundels door fmdita in het filtrerende tekstvakje in te gaan en **te drukken gaat** binnen.

   De lijst met bundels wordt gefilterd om de bundels weer te geven die door AEM Guides zijn geïnstalleerd. Als de installatie succesvol was, dan zullen alle geïnstalleerde bundels a **Status** van **Actieve** hebben.

   Als om het even welke bundels geen **Actieve** status heeft, dan controleer de AEM logboeken om de installatiekwestie problemen op te lossen.


>[!IMPORTANT]
>
> Er zijn een aantal aanbevelingen voor het optimaliseren van de prestaties die u kunt overwegen om de systeemprestaties te verbeteren. Zie [ Recommendations voor prestatiesoptimalisering ](download-install-recommend-perf-optimiz.md#) voor details.

**Bovenliggend onderwerp:**[ Download en installeer ](download-install.md)
