---
title: Bestanden uploaden
description: Leer hoe u uw bestanden uploadt naar de AEM-opslagplaats en fouten verwerkt. Gebruikerinterface van de console met bekende middelen, AEM-bureaubladtoepassing, assetbulk ingestor en gebruik FrameMaker voor bulkupload.
exl-id: b5430242-1122-43df-a0b2-275b1dea33f2
feature: Content Management
role: User
source-git-commit: f3858b1694837c7a3fa7bb222ed8ff31ce7103f8
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 0%

---

# Bestanden uploaden {#id176FF000JUI}

U hebt waarschijnlijk een opslagplaats voor bestaande DITA-inhoud die u met Adobe Experience Manager Guides wilt gebruiken. Voor dergelijke bestaande inhoud kunt u een van de volgende methoden gebruiken om uw inhoud in bulk te uploaden naar de Adobe Experience Manager-opslagplaats.

>[!IMPORTANT]
>
> De mening [ voegt digitale activa aan Adobe Experience Manager as a Cloud Service Assets ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/add-assets.html?lang=nl-NL) voor gedetailleerde informatie in de gesteunde inhoud toe uploadt methodes in Adobe Experience Manager.

## Assets Console-gebruikersinterface

U kunt inhoud op uw bureaublad selecteren en in de Adobe Experience Manager-gebruikersinterface \(webbrowser\) naar de doelmap slepen. Voor meer details, mening [ uploadt activa ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/add-assets.html?lang=nl-NL#upload-assets) in de documentatie van Adobe Experience Manager.

## Adobe Experience Manager-bureaubladtoepassing

Gebruik de Adobe Experience Manager-bureaubladtoepassing als u een creatieve professional bent en de middelen op uw lokale bureaublad wilt beheren. U kunt deze elementen openen en bewerken met uw bureaubladtoepassingen. U kunt ook versies bijhouden en uw bestanden delen met andere gebruikers. Voor meer details, bekijk [ Desktop app van Adobe Experience Manager ](https://experienceleague.adobe.com/docs/experience-manager-desktop-app/using/using.html?lang=nl-NL).

## Bulkingestor

Als u grootschalige migraties en soms grote hoeveelheden inneemt, kunt u de inhoud uploaden met Asset bulksgewijs inslikken. Met dit hulpprogramma kunt u bulkinhoud uploaden uit ondersteunde datastores zoals Azure of S3. Voor meer details, mening [ bulkingestor van Activa ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/add-assets.html?lang=nl-NL#asset-bulk-ingestor).

## FrameMaker gebruiken voor bulkupload

Adobe FrameMaker wordt geleverd met een krachtige Adobe Experience Manager-connector waarmee u uw bestaande DITA en andere FrameMaker-documenten \(`.book` en `.fm`\) eenvoudig kunt uploaden naar Adobe Experience Manager. U kunt verschillende functies voor het uploaden van bestanden gebruiken, zoals het uploaden van één bestand, het uploaden van een volledige map met of zonder afhankelijkheden \(zoals inhoudsverwijzingen, kruisverwijzingen en afbeeldingen\).

Voor meer details over het gebruiken van bulkupload eigenschap in FrameMaker, bekijk de sectie *creeer een omslag van CRX en upload dossiers* in de Gids van de Gebruiker van FrameMaker.

## Foutafhandeling tijdens het uploaden van inhoud {#id201MI0I04Y4}

Als het uploaden van een of meer bestanden mislukt, wordt er een vraag weergegeven aan het einde van het uploadproces met een lijst met bestanden die niet zijn geüpload, zoals in het onderstaande fragment wordt getoond.

![](images/uuid-files-failed-to-upload_cs.png){width="650" align="center"}

Voor meer details over hoe de diverse dossier uploadende scenario&#39;s functioneren, mening [ leidt dossiers en omslagen ](authoring-file-management.md#).

Als u een hulpprogramma zoals een Adobe Experience Manager-bureaubladtoepassing of het bulksgewijs invoegen van middelen gebruikt, wordt de handeling die op een gedupliceerd bestand wordt uitgevoerd, bepaald door een instelling op de Adobe Experience Manager-server. Neem contact op met de systeembeheerder voor informatie over deze configuratie.

**Bovenliggend onderwerp:**&#x200B;[ beheert inhoud ](authoring.md)
