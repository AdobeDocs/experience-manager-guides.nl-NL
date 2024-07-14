---
title: Opmerkingen bij de release | Opgeloste problemen in Adobe Experience Manager Guides 4.3.1.5-release
description: Meer informatie over de opgeloste problemen in de 4.3.1.5-release van Adobe Experience Manager Guides
role: Leader
exl-id: 082dca28-15da-417c-b511-74eb5ac68078
source-git-commit: e40ebf4122decc431d0abb2cdf1794ea704e5496
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---

# 4.3.1.5. Opgeloste problemen


In dit artikel worden de bugs beschreven die zijn gecorrigeerd in verschillende gebieden van de release van Adobe Experience Manager Guides van 4.3.1.5.



Leer over [ verbeteringsinstructies voor de versie 4.3.1.5 ](../release-info/upgrade-instructions-4-3-1-5.md).


## Authoring

- Als u spaties toevoegt tussen inline-elementen in `<codeblock>` , wordt er een regeleinde ingevoegd in de gegenereerde uitvoer. 15247
- Er doen zich problemen voor bij het toevoegen van elementen uit het dialoogvenster Element invoegen. 15108

## Publiceren

- Foutlogboeken geven onjuiste informatie weer over het publiceren van inhoud met een extern bereik. 15242
- Interne koppelingen naar DITA-bestanden die beginnen met `HTTP` worden behandeld als externe koppelingen en veroorzaken bereikfouten. 15155
- AEM Site-regeneratie mislukt voor DITA-kaarten. 14369

## Beheer

- **fmditaTopicrefs** bezit toont relatieve wegen in plaats van absolute wegen. 15341
