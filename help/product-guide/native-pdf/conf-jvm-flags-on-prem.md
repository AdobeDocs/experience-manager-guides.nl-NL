---
title: Native PDF | JVM-vlaggen configureren voor native PDF-publicatie
description: JVM-vlaggen configureren voor native PDF-publicatie
feature: Output Generation
role: Admin
level: Experienced
source-git-commit: 834959a6a0e22cd5d2b2c5d0e57ceb6d45c0c666
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---

# JVM-vlaggen configureren voor Native PDF Publishing for On-Premise

Native PDF-publicaties starten een apart JVM-proces om een PDF te genereren. Mogelijk moet u de configuraties van deze JVM aanpassen om verschillende scenario&#39;s te ondersteunen. Als u bijvoorbeeld grotere werklasten wilt uitvoeren, moet u de maximale heapgrootte verhogen die beschikbaar is voor het gepaaide JVM-proces.

Voer de volgende stappen uit om JVM-vlaggen voor AEM Guides Native PDF Publishing te configureren:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en selecteer *com.adobe.fmdita.config.ConfigManager* bundel.

1. Werk het bezit **de lijnopties van het Bevel van Java voor inheemse pdf** (*native.pdf.java.opts*) bij om het even welke standaardvlaggen over te gaan JVM.



1. Klik **sparen**.
