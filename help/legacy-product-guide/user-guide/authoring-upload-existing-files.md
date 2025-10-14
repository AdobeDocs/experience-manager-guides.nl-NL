---
title: Bestanden uploaden
description: Leer hoe u uw bestanden uploadt naar de AEM-opslagplaats en fouten verwerkt. Gebruikerinterface van de console met bekende middelen, AEM-bureaubladtoepassing, assetbulk ingestor en gebruik FrameMaker voor bulkupload.
feature: Content Management
role: User
hide: true
exl-id: fcb2cc43-6a36-42f2-a695-7a50ae1031a0
source-git-commit: 7286c3fb36695caa08157296fd6e0de722078c2b
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# Bestanden uploaden {#id176FF000JUI}

U hebt waarschijnlijk een opslagplaats voor bestaande DITA-inhoud die u met AEM Guides wilt gebruiken. Voor dergelijke bestaande inhoud kunt u een van de volgende methoden gebruiken om uw inhoud in een AEM-opslagplaats te bulksgewijs te uploaden:

>[!IMPORTANT]
>
> Zie [&#x200B; digitale activa toevoegen aan Adobe Experience Manager as a Cloud Service Assets &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/add-assets.html?lang=nl-NL) voor gedetailleerde informatie in de gesteunde inhoud uploadt methodes in AEM.

## Assets Console-gebruikersinterface

U kunt inhoud op uw bureaublad selecteren en in de AEM-gebruikersinterface \(webbrowser\) naar de doelmap slepen. Voor meer details, zie [&#x200B; activa &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/add-assets.html?lang=nl-NL#upload-assets) in de documentatie van AEM uploaden.

## AEM-bureaubladtoepassing

Gebruik de AEM-bureaubladtoepassing als u een creatieve professional bent en de middelen op uw lokale bureaublad wilt beheren. U kunt deze elementen openen en bewerken met uw bureaubladtoepassingen. U kunt ook versies bijhouden en uw bestanden delen met andere gebruikers. Voor meer details, zie [&#x200B; Desktop app van AEM &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-desktop-app/using/using.html?lang=nl-NL).

## Bulkingestor

Als u grootschalige migraties en soms grote hoeveelheden inneemt, kunt u de inhoud uploaden met Asset bulksgewijs inslikken. Met dit hulpprogramma kunt u bulkinhoud uploaden uit ondersteunde datastores zoals Azure of S3. Voor meer details, zie [&#x200B; bulkingestor van Activa &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/add-assets.html?lang=nl-NL#asset-bulk-ingestor).

## FrameMaker gebruiken voor bulkupload

Adobe FrameMaker wordt geleverd met een krachtige AEM-connector waarmee u uw bestaande DITA en andere FrameMaker-documenten \(`.book` en `.fm`\) eenvoudig kunt uploaden naar AEM. U kunt verschillende functies voor het uploaden van bestanden gebruiken, zoals het uploaden van één bestand, het uploaden van een volledige map met of zonder afhankelijkheden \(zoals inhoudsverwijzingen, kruisverwijzingen en afbeeldingen\).

Voor meer details over het gebruiken van bulkupload eigenschap in FrameMaker, zie de sectie *een omslag van CRX creëren en dossiers* in de Gids van de Gebruiker van FrameMaker uploaden.

## Foutafhandeling tijdens het uploaden van inhoud {#id201MI0I04Y4}

Als een of meer bestanden niet kunnen worden geüpload, wordt na het uploadproces een vraag weergegeven met een lijst bestanden die niet zijn geüpload:

![](images/uuid-files-failed-to-upload_cs.png){width="650" align="center"}

Voor meer details over hoe de diverse dossier het uploaden scenario&#39;s, [&#x200B; zien uploaden inhoud DITA &#x200B;](authoring-file-management.md#).

Als u een hulpprogramma zoals een AEM-bureaubladtoepassing of het bulksgewijs invoegen van middelen gebruikt, wordt de handeling die op een gedupliceerd bestand wordt uitgevoerd, bepaald door een instelling op de AEM-server. Neem contact op met de systeembeheerder voor informatie over deze configuratie.

**Bovenliggend onderwerp:**&#x200B;[&#x200B; beheert inhoud &#x200B;](authoring.md)
