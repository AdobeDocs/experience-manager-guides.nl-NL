---
title: DITA Assets Replication configureren voor services op locatie
description: Leer hoe te om dita activa replicatie voor de diensten op locatie te vormen
feature: Output Generation
role: Admin
level: Experienced
exl-id: 49fd9dfe-e1a5-4388-abbd-ec5d45669b45
hidefromtoc: true
source-git-commit: 3aadc59f5034828cf319992b7acb32d5a88eaf93
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 0%

---

# Replicatie van DITA-elementen configureren

Voer de volgende stappen uit om de functie voor middelenverwerking te configureren:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en selecteer *com.adobe.fmdita.config.ConfigManager* bundel.

1. Configureer de instelling `Replicate DITA assets` naar wens. De instelling wordt standaard ingeschakeld.


   ![](assets/dita-assets-replication.png){width="350" align="left"}


1. Selecteer **sparen**.
