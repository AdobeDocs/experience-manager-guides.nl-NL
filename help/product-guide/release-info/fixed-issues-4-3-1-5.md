---
title: Opmerkingen bij de release | Adobe Experience Manager-hulplijnen 4.3.1.5. Opgeloste problemen
description: Meer informatie over de opgeloste problemen in de 4.3.1.5-release van Adobe Experience Manager Guides
role: Leader
source-git-commit: 485f88e2e8724d1dc28deac13d677734fcc15c25
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---


# 4.3.1.5. Opgeloste problemen


In dit artikel worden de bugs beschreven die zijn gecorrigeerd in verschillende gebieden van de release van Adobe Experience Manager Guides in 4.3.1.5.



Meer informatie over [upgrade-instructies voor de 4.3.1.5-release](../release-info/upgrade-instructions-4-3-1-5.md).


## Authoring

- Spaties toevoegen tussen inline-elementen binnen `<codeblock>` veroorzaakt een lijnonderbreking in de geproduceerde output. 15247
- Er doen zich problemen voor bij het toevoegen van elementen uit het dialoogvenster Element invoegen. 15108

## Publiceren

- Foutlogboeken geven onjuiste informatie weer over het publiceren van inhoud met een extern bereik. 15242
- Interne koppelingen naar DITA-bestanden die beginnen met `HTTP` worden behandeld als externe koppelingen en veroorzaken bereikfouten. 15155
- AEM Site-regeneratie mislukt voor DITA-kaarten. 14369

## Beheer

- **fmditaTopicrefs** in plaats van absolute paden worden relatieve paden weergegeven. 15341

