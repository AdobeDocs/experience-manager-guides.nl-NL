---
title: Aangepaste implementatie voor indexering voor on-premisse installatie
description: Leer hoe te om indexinhoud voor de opstelling op-gebouw aan te passen
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 8a9a82e79c757e403141e853aafbc64e1618c30a
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# Opnieuw indexeren voor de functie Zoeken en vervangen (Source-weergave)

Het opnieuw indexeren wordt vereist om de **Vondst toe te laten en te vervangen (de mening van Source)** eigenschap, die u toestaat om de volledige inhoud zichtbaar in de mening van de Auteur en ook de onderliggende inhoud van Source (de structuur van XML, met inbegrip van elementen, markeringen, en attributenwaarden) voor het gezochte koord af te tasten.

## Opnieuw indexeren

Voor instellingen op locatie wordt de indexdefinitie opgenomen in het pakket. Als u de functie wilt inschakelen, moet u de inhoud opnieuw indexeren.

Begin opnieuw indexeren door de eigenschap `reindex=true (Boolean)` op het knooppunt in te stellen: ` /oak:index/guidesAssetLucene` om eerder vastgelegde inhoud opnieuw te indexeren.

Het herindexeringsproces wordt voortgezet totdat het systeem deze eigenschap automatisch terugzet op false. U kunt de voortgang van het opnieuw indexeren in de systeemlogboeken controleren.