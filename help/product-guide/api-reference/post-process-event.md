---
title: Gebeurtenishandler voor nabewerking
description: Meer informatie over de gebeurtenishandler Nabewerking
exl-id: 3b105ff5-02d4-40e3-a713-206a7fcf18b2
feature: Post-Processing Event Handler
role: Developer
level: Experienced
source-git-commit: 83966cc9187b13dd3b5956821e0aa038b41db28e
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 0%

---

# Gebeurtenishandler voor nabewerking {#id175UB30E05Z}

AEM Guides stelt de gebeurtenis com/adobe/fmdita/postprocess/complete beschikbaar die wordt gebruikt om naverwerkingen uit te voeren. Deze gebeurtenis wordt geactiveerd wanneer een bewerking op een DITA-bestand wordt uitgevoerd. De volgende bewerkingen op een DITA-bestand activeren deze gebeurtenis:

>[!NOTE]
>
> Deze gebeurtenis wordt niet geactiveerd voor het verwijderen in AEM 6.1.

- Uploaden
- Maken
- Wijziging
- Verwijderen

U moet een AEM gebeurtenishandler maken om de eigenschappen te lezen die beschikbaar zijn in deze gebeurtenis en verdere verwerking uit te voeren.

De gebeurtenisdetails worden hieronder uitgelegd:

**naam van de Gebeurtenis**:

```
com/adobe/fmdita/postprocess/complete 
```

**Parameters**:

| Naam | Type | Beschrijving |
|----|----|-----------|
| `path` | String | Het pad van het bestand dat deze gebeurtenis heeft geactiveerd. Dit is doorgaans het bestand waarop een bewerking is uitgevoerd. |
| `status` | String | De geretourneerde status voor de uitgevoerde bewerking. De mogelijke opties zijn: - <br> - SUCCESS: de naverwerkingbewerking is voltooid. <br> - IS VOLTOOID MET FOUTEN: de naverwerkingsbewerking is voltooid, maar met enkele fouten. <br> - MISLUKT: de naverwerkingshandeling is mislukt als gevolg van een fatale fout. |
| `message` | String | Als de status IS VOLTOOID MET FOUTEN of MISLUKT, bevat deze parameter de details over de fout of de oorzaak van de fout. |
| `operation` | String | De nabewerking die op het bestand is uitgevoerd. De mogelijke opties zijn:<br> - Toevoeging <br> - Bijwerken <br> - Verwijderen |
