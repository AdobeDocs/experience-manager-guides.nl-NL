---
title: AEM Guides-installatie verifiëren
description: Meer informatie over het verifiëren van AEM Guides-installatie
feature: Installation
role: Admin
level: Experienced
source-git-commit: 6f3f05419f4f5cdd45ab580cdee6fa869f20f01d
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---

# AEM Guides-installatie verifiëren {#id213BD030FBE}

Nadat u AEM Guides hebt geïnstalleerd, moet u controleren of de installatie is gelukt of niet.

Op de volgende tabbladen vindt u instructies voor het controleren van de AEM Guides-installatie op basis van uw Experience Manager Guides-installatie: Cloud Service of On-Premise.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

Voer de volgende stappen uit om de installatie te verifiëren:

1. Open de Developer Console van je Cloud Service.

   Voor details om tot Developer Console toegang te hebben, zie {de toegang van 0} Developer Console [&#x200B; in de documentatie van AEM.](https://experienceleague.adobe.com/docs/experience-manager-learn/cloud-service/debugging/debugging-aem-as-a-cloud-service/developer-console.html)

1. Open de lijst met OSGi-bundels in AEM.

   Voor details om tot Bundels toegang te hebben, zie [&#x200B; Bundels &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-learn/cloud-service/debugging/debugging-aem-as-a-cloud-service/developer-console.html?lang=en#bundles) in de documentatie van AEM.

1. Zoek naar fmdita in de lijst van bundels en controleer zijn status.

   De status zou *Actief* voor met succes opgestelde bundels moeten tonen. Als een van de pakketten geen actieve status heeft, controleert u de AEM-logboeken om het installatieprobleem op te lossen.

>[!TAB  Op locatie ]

Voer de volgende stappen uit om de installatie te verifiëren:

1. Meld u aan bij uw AEM-exemplaar en navigeer naar de pagina AEM Web Console Bundles. De standaard-URL voor toegang tot de bundelpagina is:

   ```http
   http://<server name>:<port>/system/console/bundles
   ```

   Er wordt een lijst met bundels weergegeven.

1. Filter de lijst van bundels door fmdita in het filtrerende tekstvakje in te gaan en **te drukken gaat** binnen.

   De lijst met bundels wordt gefilterd om de bundels weer te geven die door AEM Guides zijn geïnstalleerd. Als de installatie succesvol was, dan zullen alle geïnstalleerde bundels a **Status** van **Actieve** hebben.

   Als om het even welke bundels geen **Actieve** status heeft, dan controleer de logboeken van AEM om de installatiekwestie problemen op te lossen.


>[!IMPORTANT]
>
> Er zijn een aantal aanbevelingen voor het optimaliseren van de prestaties die u kunt overwegen om de systeemprestaties te verbeteren. Zie [&#x200B; Aanbevelingen voor prestatiesoptimalisering &#x200B;](perf-optimization-on-prem.md#) voor details.

>[!ENDTABS]


