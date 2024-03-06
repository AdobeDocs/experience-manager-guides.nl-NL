---
title: Toevoegen [!DNL Experience Manager Guides] aan uw [!DNL Experience Manager as a Cloud Service] milieu
description: Meer informatie over toevoegen [!DNL AEM Guides] aan uw [!DNL AEM as a Cloud Service] milieu
exl-id: a1e020c2-360c-4d71-b5fd-8179d9ceacda
feature: Installation
role: Leader
source-git-commit: 1b25f1df67fa2442ab79830dc2ac5a6eabd0394c
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---

# [!DNL Adobe Experience Manager Guides] as a Cloud Service implementatie

Meer informatie over toevoegen [!DNL Experience Manager Guides] aan uw [!DNL Experience Manager as a Cloud Service] milieu.


>[!NOTE]
>
> Vanaf versie 2024.2.0, zijn de Gidsen van de Experience Manager slechts beschikbaar als geautomatiseerde toe:voegen-op voor as a Cloud Service Experience Manager. Als u handmatige implementaties voor hulplijnen voor Experience Managers gebruikt, verwijdert u de regel `<module>dox.installer</module> from file dox/pom.xml` in uw cloud manage it codebase voordat u Experience Manager Guides inschakelt voor uw programma.

1. Aanmelden bij [!UICONTROL Cloud Manager].

1. Bewerk het programma waarvoor u wilt configureren [!DNL Experience Manager Guides].

1. Overschakelen op **[!UICONTROL Solutions and Add-ons]** tab.

1. In de **[!UICONTROL Solutions and Add-ons]** tabel, klik op **[!UICONTROL Assets]**.

1. Selecteren **[!UICONTROL Guides]** en selecteert u **[!UICONTROL Save]**.

U hebt met succes uw programma voor automatische levering van de oplossing van de Gidsen van de Experience Manager gevormd.

![Oplossing voor het configureren van hulplijnen voor Experience Managers](assets/addon-configuration.png)

>[!NOTE]
>
>Om te installeren [!DNL Experience Manager Guides] op elk milieu in het kader van het geïntegreerde programma moet u de pijpleiding voor het milieu in werking stellen . Er is geen aanvullende configuratie vereist in uw CM-it-codebase voor installatie [!DNL Experience Manager Guides].
