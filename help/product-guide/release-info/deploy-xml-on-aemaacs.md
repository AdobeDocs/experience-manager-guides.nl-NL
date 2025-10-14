---
title: Hoe te  [!DNL Experience Manager Guides]  aan uw  [!DNL Experience Manager as a Cloud Service]  milieu toevoegen
description: Leer hoe te  [!DNL AEM Guides]  aan uw  [!DNL AEM as a Cloud Service]  milieu toevoegen
exl-id: a1e020c2-360c-4d71-b5fd-8179d9ceacda
feature: Installation
role: Leader
source-git-commit: 1b25f1df67fa2442ab79830dc2ac5a6eabd0394c
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---

# [!DNL Adobe Experience Manager Guides] as a Cloud Service implementatie

Leer hoe u [!DNL Experience Manager Guides] toevoegt aan uw [!DNL Experience Manager as a Cloud Service] -omgeving.


>[!NOTE]
>
> Vanaf release 2024.2.0 is Experience Manager Guides alleen beschikbaar als een geautomatiseerde invoegtoepassing voor Experience Manager as a Cloud Service. Als u handmatige implementaties voor Experience Manager Guides gebruikt, verwijdert u eerst de regel `<module>dox.installer</module> from file dox/pom.xml` in uw codebase voor kleurbeheer in de cloud voordat u Experience Manager Guides voor uw programma inschakelt.

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
