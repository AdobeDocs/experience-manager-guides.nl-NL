---
title: Alinea's in een onderwerp uitsluiten van vertaling
description: Hoe te om paragrafen binnen een onderwerp van vertaling uit te sluiten
feature: Translation
role: User
exl-id: 21e41bb4-52f3-4352-92d9-4a60f636de99
source-git-commit: 5e0584f1bf0216b8b00f00b9fe46fa682c244e08
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# Hoe te om paragrafen binnen een onderwerp van vertaling uit te sluiten

De eenvoudigste manier is om het kenmerk translatie=no te gebruiken.

+ De auteurs kunnen de extra attributen als **vertaling=no** op de paragrafen opnemen die zij niet willen vertalen. De vertaalleverancier moet worden geïnformeerd en zij kunnen configuratie aan hun eind doen om de tekst met dit attribuut te negeren.
+ De machinevertaling OOTB (met de proefschakelaar van Microsoft Translation) vertoont hetzelfde gedrag.
+ Testen met de Vertaling van Microsoft: als u **translate=no** attributen op paragraafniveau bepaalt dan vertaalt het niet de volledige paragraaf. Dit kenmerk kan op elk element worden gedefinieerd en de inhoud binnen dat element wordt niet vertaald.


Hier volgen enkele schermafbeeldingen die dit nader verklaren:

**Inhoud Source**

![ Inhoud Source ](assets/source-content.jpg)

**Vertaalde Inhoud in Spaans**

![ Vertaalde Inhoud in Spaans ](assets/trans-content.jpg)
