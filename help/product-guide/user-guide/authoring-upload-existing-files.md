---
title: Bestanden uploaden
description: Leer hoe u uw bestanden uploadt naar de AEM-opslagplaats en fouten verwerkt. Gebruikerinterface van de console met bekende middelen, AEM-bureaubladtoepassing, assetbulk ingestor en gebruik FrameMaker voor bulkupload.
exl-id: b5430242-1122-43df-a0b2-275b1dea33f2
feature: Content Management
role: User
source-git-commit: 0259c0c0b7270d860198f17e6ea5f5829df038d5
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 0%

---

# Bestanden uploaden {#id176FF000JUI}

U hebt waarschijnlijk een opslagplaats voor bestaande DITA-inhoud die u met Adobe Experience Manager Guides wilt gebruiken. Voor dergelijke bestaande inhoud kunt u een van de volgende methoden gebruiken om uw inhoud in bulk te uploaden naar de Adobe Experience Manager-opslagplaats.

>[!IMPORTANT]
>
> De mening [&#x200B; voegt digitale activa aan Adobe Experience Manager as a Cloud Service Assets &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/add-assets.html?lang=nl-NL) voor gedetailleerde informatie in de gesteunde inhoud toe uploadt methodes in Adobe Experience Manager.

## Assets Console-gebruikersinterface

Om [&#x200B; digitale activa aan Adobe Experience Manager as a Cloud Service Assets &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/add-assets.html?lang=nl-NL#filename-handling?lang=nl-NL#upload-assets) toe te voegen gebruikend het gebruikersinterface van de Console van Assets, selecteer het vereiste middel op uw Desktop en sleep op het gebruikersinterface van Adobe Experience Manager \ (Webbrowser \) aan de bestemmingsomslag. Zorg er bij het uploaden van elementen voor dat de bestandsnamen geen niet-ondersteunde of verboden tekens bevatten.

Voor meer details, mening [&#x200B; bestandsnaam behandeling en verboden karakters &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/add-assets.html?lang=nl-NL#filename-handling) sectie in de documentatie van Adobe Experience Manager.

## Adobe Experience Manager-bureaubladtoepassing

Gebruik de Adobe Experience Manager-bureaubladtoepassing als u een creatieve professional bent en de middelen op uw lokale bureaublad wilt beheren. U kunt deze elementen openen en bewerken met uw bureaubladtoepassingen. U kunt ook versies bijhouden en uw bestanden delen met andere gebruikers. Voor meer details, bekijk [&#x200B; Desktop app van Adobe Experience Manager &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-desktop-app/using/using.html?lang=nl-NL).

## Bulkingestor

Als u grootschalige migraties en soms grote hoeveelheden inneemt, kunt u de inhoud uploaden met Asset bulksgewijs inslikken. Met dit hulpprogramma kunt u bulkinhoud uploaden uit ondersteunde datastores zoals Azure of S3. Voor meer details, mening [&#x200B; bulkingestor van Activa &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/add-assets.html?lang=nl-NL#asset-bulk-ingestor).

## FrameMaker gebruiken voor bulkupload

Adobe FrameMaker wordt geleverd met een krachtige Adobe Experience Manager-connector waarmee u uw bestaande DITA en andere FrameMaker-documenten \(`.book` en `.fm`\) eenvoudig kunt uploaden naar Adobe Experience Manager. U kunt verschillende functies voor het uploaden van bestanden gebruiken, zoals het uploaden van één bestand, het uploaden van een volledige map met of zonder afhankelijkheden \(zoals inhoudsverwijzingen, kruisverwijzingen en afbeeldingen\).

Voor meer details over het gebruiken van bulkupload eigenschap in FrameMaker, bekijk de sectie *creeer een omslag van CRX en upload dossiers* in de Gids van de Gebruiker van FrameMaker.

## Foutafhandeling tijdens het uploaden van inhoud {#id201MI0I04Y4}

Als het uploaden van een of meer bestanden mislukt, wordt er een vraag weergegeven aan het einde van het uploadproces met een lijst met bestanden die niet zijn geüpload, zoals in het onderstaande fragment wordt getoond.

![](images/uuid-files-failed-to-upload_cs.png){width="650" align="center"}

Voor meer details over hoe de diverse dossier uploadende scenario&#39;s functioneren, mening [&#x200B; leidt dossiers en omslagen &#x200B;](authoring-file-management.md#).

Als u een hulpprogramma zoals een Adobe Experience Manager-bureaubladtoepassing of het bulksgewijs invoegen van middelen gebruikt, wordt de handeling die op een gedupliceerd bestand wordt uitgevoerd, bepaald door een instelling op de Adobe Experience Manager-server. Neem contact op met de systeembeheerder voor informatie over deze configuratie.

**Bovenliggend onderwerp:**&#x200B;[&#x200B; beheert inhoud &#x200B;](authoring.md)
