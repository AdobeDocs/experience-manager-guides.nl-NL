---
title: Aangepaste implementatie voor indexering voor on-premisse installatie
description: Leer hoe te om indexinhoud voor de opstelling op-gebouw aan te passen
feature: Web Editor Configuration
role: Admin
level: Experienced
exl-id: 5b9e4936-f674-41d3-a7b2-3d42a2523693
hidefromtoc: true
source-git-commit: 3aadc59f5034828cf319992b7acb32d5a88eaf93
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
