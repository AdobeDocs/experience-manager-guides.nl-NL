---
title: Native PDF | JVM-vlaggen configureren voor Native PDF Publishing
description: JVM-vlaggen configureren voor Native PDF Publishing
exl-id: d5432913-4b5a-48e7-9467-7f6c6e0adbe4
feature: Output Generation
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# JVM-vlaggen configureren voor Native PDF Publishing

Native PDF-publicaties starten een apart JVM-proces om een PDF te genereren. Mogelijk moet u de configuraties van deze JVM aanpassen om verschillende scenario&#39;s te ondersteunen. Als u bijvoorbeeld grotere werklasten wilt uitvoeren, moet u de maximale heapgrootte verhogen die beschikbaar is voor het gepaaide JVM-proces.

Voer de volgende stappen uit om JVM-vlaggen voor AEM Guides Native PDF publiceren te configureren:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en selecteer *com.adobe.fmdita.config.ConfigManager* bundel.

1. Werk het bezit **de lijnopties van het Bevel van Java voor inheemse pdf** (*native.pdf.java.opts*) bij om het even welke standaardvlaggen over te gaan JVM.



1. Klik **sparen**.
