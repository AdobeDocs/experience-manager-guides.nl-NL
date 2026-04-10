---
title: Basisuitvoerlocatie configureren voor publicatie-uitvoer voor services op locatie
description: Basisuitvoerlocatie configureren voor publicatie-uitvoer voor services op locatie
feature: Output Generation
role: Admin
level: Experienced
exl-id: ae1d805a-7b79-4b76-8be2-a19c5552530c
hidefromtoc: true
source-git-commit: 3aadc59f5034828cf319992b7acb32d5a88eaf93
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 0%

---

# Vorm de Plaats van de Output van de Basis voor het publiceren output voor de diensten op locatie

Voer de volgende stappen uit om de basisuitvoerlocatie te configureren:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en selecteer *com.adobe.fmdita.config.ConfigManager* bundel.

1. Werk het bezit **Plaats van de Output van de Basis** bij om de standaardweg in de bewaarplaats van AEM te specificeren waar PDF na het publiceren zal worden bewaard. Bovendien, als een ongeldig weg is ingegaan, zal het automatisch aan de standaardweg terugkeren: /content/dam/fmdita-output.

1. Klik **sparen**.
