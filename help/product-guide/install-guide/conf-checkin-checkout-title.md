---
title: Titel configureren voor inchecken en uitchecken van pictogrammen
description: Leer hoe u de titel voor de pictogrammen Inchecken en Uitchecken configureert
exl-id: a8888a17-e819-4fa2-bb6f-cafe1002803a
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# De titel configureren voor de pictogrammen Inchecken en Uitchecken

Met AEM Guides kunt u de titel configureren voor de pictogrammen Inchecken en Uitchecken in de webeditor. Voer de volgende stappen uit om de titel voor de pictogrammen Inchecken en Uitchecken te configureren:

1. Download het UI-configuratiebestand door u als beheerder aan te melden bij Adobe Experience Manager.
1. Klik op de verbinding van Adobe Experience Manager bij de bovenkant en kies **Hulpmiddelen**.
1. Selecteer **Gidsen** van de lijst van hulpmiddelen en klik de **Profielen van de Omslag**.
1. Klik op de **Globale tegel van het Profiel**.
1. Selecteer het **lusje van de Configuratie van de Redacteur van XML** en klik **uitgeven** pictogram op de bovenkant.
1. In de **UI van de Redacteur van XML configuratie** sectie, klik het **3&rbrace; pictogram van de Download &lbrace;om het `ui_config.json` dossier op uw lokaal systeem te downloaden.**
1. Wijzig in het bestand `ui_config.json` de titel in de sectie &quot;bovenste balk&quot;. U kunt de volgende waarden wijzigen:

   ```json
   //Change title to "Check out" instead of "Lock"
           "title": "Check out"
   
   //Change title to "Check in" instead of "@checkOutBy
            "title": "Check in"
   ```

1. Sla het bestand op en upload het.
