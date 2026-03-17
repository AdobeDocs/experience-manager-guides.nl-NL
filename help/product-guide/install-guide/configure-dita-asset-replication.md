---
title: DITA Assets Replication configureren voor services op locatie
description: Leer hoe te om dita activa replicatie voor de diensten op locatie te vormen
feature: Output Generation
role: Admin
level: Experienced
source-git-commit: 356ea6edd5e688fb1f77e737c705ed0bd4d2e7f0
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
