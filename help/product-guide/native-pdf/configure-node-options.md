---
title: Native PDF | Het Node-proces configureren voor Native PDF Publishing
description: Leer hoe u het Node-proces configureert voor Native PDF Publishing
exl-id: f470939b-a5cb-4d28-92d1-7a0a52c4c637
source-git-commit: 5e0584f1bf0216b8b00f00b9fe46fa682c244e08
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# Knooppuntproces configureren voor publicatie op eigen PDF

Native PDF-publicatie start een afzonderlijk NodeJs-proces om de bestanden die in het publicatieproces worden gegenereerd, om te zetten in een definitieve PDF. U zou de configuraties van dit proces van Node kunnen moeten aanpassen die het Native publiceren van PDF in werking stellen om verschillende scenario&#39;s te steunen. Als u bijvoorbeeld grotere werklasten wilt uitvoeren, vergroot u de maximale heapgrootte die beschikbaar is voor het paaide NodeJs-proces.

Gebruik de instructies die worden gegeven in [Configuratieoverschrijvingen](../cs-install-guide/download-install-additional-config-override.md) om het configuratiedossier.In het configuratiedossier tot stand te brengen, verstrek de volgende (bezit) details:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|---|---|
| `com.adobe.fmdita.config.ConfigManager` | `native.pdf.node.opts` | Tekenreekswaarde voor het instellen van een willekeurige standaard `NODE_OPTIONS`.<BR> Standaardwaarde: &quot;&quot; |
