---
title: Configuratie van implementatie en verzender
description: Meer informatie over de configuratie van Implementatie en verzenders in Experience Manager Guides as a Cloud Service
feature: Introduction, Installation
role: Admin
level: Experienced
source-git-commit: 834959a6a0e22cd5d2b2c5d0e57ceb6d45c0c666
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 3%

---

# Configuratie van implementatie en verzender

Dit artikel bevat informatie over hoe u Experience Manager Guides as a Cloud Service kunt implementeren en dispatcher kunt configureren.

## Experience Manager Guides as a Cloud Service implementeren

U kunt beginnen met het implementeren van Experience Manager Guides via de Cloud Manager. Om de module op te stellen volg de instructies die in [&#x200B; worden vermeld de plaatsing van as a Cloud Service van AEM Guides &#x200B;](../release-info/deploy-xml-on-aemaacs.md).

>[!NOTE]
>
> Vanaf de release 2024.2.0 is Experience Manager Guides alleen beschikbaar als een automatische invoegtoepassing voor Experience Manager as a Cloud Service. Als u de versies van december 2023 of vroeger gebruikt, kunt u Adobe Experience Manager Guides van de bewaarplaats downloaden GitHub en het installeren. Als u handmatige implementaties voor Experience Manager Guides gebruikt, verwijdert u de regel `<module>dox.installer</module> from file dox/pom.xml` in uw Git-codebase voor cloudbeheer voordat u Experience Manager Guides voor uw programma inschakelt.

Voer de volgende stappen uit om de Experience Manager Guides-module te implementeren:

1. Meld u aan bij [!UICONTROL Cloud Manager] .

1. Bewerk het programma waarvoor u [!DNL Experience Manager Guides] wilt configureren.

1. Ga naar **[!UICONTROL Solutions and Add-ons]** tab.

1. Klik in de tabel **[!UICONTROL Solutions and Add-ons]** op **[!UICONTROL Assets]** .

1. Selecteer **[!UICONTROL Guides]** en selecteer **[!UICONTROL Save]** .

U hebt met succes uw programma voor automatische levering van de oplossing van Experience Manager Guides gevormd.

![&#x200B; Vormend de oplossing van Experience Manager Guides &#x200B;](assets/addon-configuration.png)

>[!NOTE]
>
>Als u [!DNL Experience Manager Guides] wilt installeren op een willekeurige omgeving in het kader van het geïntegreerde programma, moet u de pijplijn uitvoeren die is gekoppeld aan de omgeving. Voor de installatie van [!DNL Experience Manager Guides] is geen aanvullende configuratie vereist in uw CM-git-codebase.


## Dispatcher configureren

Dispatcher is de Adobe Experience Manager-tool voor cache- en taakverdelingsbewerkingen. Voor meer details, verwijs naar [&#x200B; Dispatcher in de Wolk &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/content-delivery/disp-overview.html?lang=nl-NL).

1. Voor het migreren van de vraagconfiguratie van AMS aan de wolkendienst, verwijs naar [&#x200B; het Migreren van de configuratie van Dispatcher van AMS aan AEM as a Cloud Service &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/content-delivery/ams-aem.html?lang=nl-NL).
1. Voor details op hoe te om dispatcher te vormen, zie [&#x200B; Vormend Dispatcher &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html?lang=nl-NL).

>[!NOTE]
>
> AEM as a Cloud Service biedt geen ondersteuning voor dispatcher voor de auteur.
