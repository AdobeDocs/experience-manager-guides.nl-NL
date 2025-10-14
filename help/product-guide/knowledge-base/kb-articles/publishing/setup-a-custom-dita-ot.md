---
title: Aangepaste DITA-OT instellen in  [!DNL AEM Guides]
description: Leer hoe te opstelling douane DITA-OT in  [!DNL Adobe Experience Manager Guides]
role: Admin
exl-id: f479c2cf-5b8b-4517-be97-81303468007a
feature: DITA-OT Configuration
source-git-commit: be06612d832785a91a3b2a89b84e0c2438ba30f2
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---

# Aangepaste DITA-OT instellen in [!DNL AEM Guides] voor AEM

De stappen om een douane DITA-OT toe te voegen worden gedocumenteerd in de sectie _douane DITA-OT stop-ins van het Gebruik_ van de _Gids van de Installatie en van de Configuratie_.

Op hoog niveau zijn de volgende stappen:

+ Krijg de basisDITA-OT
   + Als u een kopie van de DITA-OT buiten de box wilt verkrijgen vanuit [!DNL AEM Guides] , downloadt u deze van het pad `/etc/fmdita/dita_resources/DITA-OT.zip`
   + Als u een verschillende versie wilt verkrijgen dan kunt u van [&#x200B; dita-te repo &#x200B;](https://www.dita-ot.org/download) downloaden
+ Breng veranderingen in DITA-OT als [&#x200B; het toevoegen van nieuwe stop &#x200B;](https://www.dita-ot.org/dev/topics/plugins-installing.html) aan, of het aanpassen van bestaande stoppen (verwijs voorbeeld in verwante verbindingssectie hieronder)
+ Uploaden `DITA-OT.zip` ontvangen naar `/apps/<project-folder>/dita_resources` (een aangepaste projectmap maken wordt aanbevolen)
+ DITA-profiel toevoegen via **[!UICONTROL Tools]** > **[!UICONTROL Guides]** > **[!UICONTROL DITA Profiles]** (gebruik het DITA-OT-pad waar de aangepaste DITA-OT wordt geüpload, raadpleeg de onderstaande schermafbeelding)
  ![&#x200B; Profielen DITA &#x200B;](assets/dita-profile.png)

>[!MORELIKETHIS]
>
>+ [&#x200B; het Aanpassen van DITA-OT steekproeven van de insteekmodule &#x200B;](https://www.dita-ot.org/dev/topics/pdf-customization.html)
