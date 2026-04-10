---
title: Vorm het aantal LimitReads voor een vraag
description: Leer hoe te om het aantal LimitReads voor een vraag te vormen
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 6f3f05419f4f5cdd45ab580cdee6fa869f20f01d
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# Vorm het aantal LimitReads voor een vraag voor Op-Premise

Voer de volgende stappen uit om het aantal knooppunten dat een query tegelijkertijd kan lezen, te verhogen:

1. Open de JMX-pagina van de Adobe Experience Manager-webconsole.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/jmx
   ```

1. Onderzoek naar en klik op **QueryEngineSettings**.

1. De attributenwaarde van de verandering voor het **LimitReads** attribuut.

1. Klik **sparen**.


Wanneer u deze kenmerkwaarde verhoogt, helpt het u het rapport voor grotere kaarten te produceren DITA.

**Bovenliggend onderwerp:**[ pas de Redacteur van het Web ](customize-overview.md) aan
