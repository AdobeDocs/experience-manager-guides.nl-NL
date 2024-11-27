---
title: Bestanden uploaden
description: Leer hoe u uw bestanden uploadt naar de AEM opslagplaats en fouten verwerkt. De middelen van de console van kennis gebruikersinterface, AEM Desktop app, activa bulkingestor, en gebruiken FrameMaker voor bulkupload.
exl-id: b5430242-1122-43df-a0b2-275b1dea33f2
feature: Content Management
role: User
source-git-commit: 7db3df07fd17eecae1c502554118ca12f95fb5ab
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# Bestanden uploaden {#id176FF000JUI}

U hebt waarschijnlijk een opslagplaats voor bestaande DITA-inhoud die u met AEM Guides wilt gebruiken. Voor dergelijke bestaande inhoud kunt u de volgende methoden gebruiken om uw inhoud in bulk te uploaden naar AEM opslagplaats:

>[!IMPORTANT]
>
> Zie [ digitale activa toevoegen aan Adobe Experience Manager as a Cloud Service Assets ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/add-assets.html) voor gedetailleerde informatie in de gesteunde inhoud uploadt methodes in AEM.

## Assets Console-gebruikersinterface

U kunt inhoud op uw bureaublad selecteren en in de AEM gebruikersinterface \(webbrowser\) naar de doelmap slepen. Voor meer details, zie [ activa ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/add-assets.html#upload-assets) in AEM documentatie uploaden.

## Bureaubladapp AEM

Gebruik AEM bureaubladtoepassing als u een creatieve professional bent en de middelen op uw lokale bureaublad wilt beheren. U kunt deze elementen openen en bewerken met uw bureaubladtoepassingen. U kunt ook versies bijhouden en uw bestanden delen met andere gebruikers. Voor meer details, zie [ Desktop app ](https://experienceleague.adobe.com/docs/experience-manager-desktop-app/using/using.html) AEM.

## Bulkingestor

Als u grootschalige migraties en soms grote hoeveelheden inneemt, kunt u de inhoud uploaden met Asset bulksgewijs inslikken. Met dit hulpprogramma kunt u bulkinhoud uploaden uit ondersteunde datastores zoals Azure of S3. Voor meer details, zie [ bulkingestor van Activa ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/add-assets.html?lang=en#asset-bulk-ingestor).

## FrameMaker gebruiken voor bulkupload

Adobe FrameMaker wordt geleverd met een krachtige AEM-aansluiting waarmee u uw bestaande DITA en andere FrameMaker documenten \(`.book` en `.fm`\) eenvoudig kunt uploaden naar AEM. U kunt verschillende functies voor het uploaden van bestanden gebruiken, zoals het uploaden van één bestand, het uploaden van een volledige map met of zonder afhankelijkheden \(zoals inhoudsverwijzingen, kruisverwijzingen en afbeeldingen\).

Voor meer details over het gebruiken van bulkupload eigenschap in FrameMaker, zie de sectie *een omslag van CRX creëren en dossiers* in de Gids van de Gebruiker van de FrameMaker uploaden.

## Foutafhandeling tijdens het uploaden van inhoud {#id201MI0I04Y4}

Als een of meer bestanden niet kunnen worden geüpload, wordt na het uploadproces een vraag weergegeven met een lijst bestanden die niet zijn geüpload:

![](images/uuid-files-failed-to-upload_cs.png){width="650" align="center"}

Voor meer details over hoe de diverse dossier het uploaden scenario&#39;s, [ zien uploaden inhoud DITA ](authoring-file-management.md#).

Als u een gereedschap gebruikt, zoals AEM bureaubladtoepassing of het bulksgewijs invoegen van middelen, wordt de handeling die op een gedupliceerd bestand wordt uitgevoerd, bepaald door een instelling op de AEM server. Neem contact op met de systeembeheerder voor informatie over deze configuratie.

**Bovenliggend onderwerp:**[ beheert inhoud ](authoring.md)
