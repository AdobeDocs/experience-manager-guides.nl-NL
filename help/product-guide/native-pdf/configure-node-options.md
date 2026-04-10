---
title: Native PDF | Node-proces configureren voor native PDF-publicatie
description: Leer hoe u het Node-proces configureert voor systeemeigen PDF-publicatie
feature: Output Generation
role: Admin
level: Experienced
hidefromtoc: true
source-git-commit: 564ee1731be2378744ffd2ed54a2fd423901a0b3
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---

# Node-proces configureren voor native PDF-publicatie voor Cloud Service

Native PDF-publicaties starten een afzonderlijk NodeJs-proces om de bestanden die tijdens het publicatieproces worden gegenereerd, om te zetten in een definitieve PDF. Mogelijk moet u de configuraties van dit Node-proces aanpassen en Native PDF-publicaties uitvoeren om verschillende scenario&#39;s te ondersteunen. Als u bijvoorbeeld grotere werklasten wilt uitvoeren, vergroot u de maximale heapgrootte die beschikbaar is voor het paaide NodeJs-proces.

Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](../install-conf-guide/download-install-config-override.md) om het configuratiedossier.In het configuratiedossier tot stand te brengen, verstrek de volgende (bezit) details:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|---|---|
| `com.adobe.fmdita.config.ConfigManager` | `native.pdf.node.opts` | Tekenreekswaarde om een willekeurige standaard in te stellen `NODE_OPTIONS` .<BR> Standaardwaarde: &quot;&quot; |
