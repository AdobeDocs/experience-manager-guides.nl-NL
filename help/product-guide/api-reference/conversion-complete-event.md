---
title: Omzetproces, gebeurtenishandler
description: Meer informatie over de gebeurtenishandler voor het conversieproces
exl-id: 8033935d-2113-4e39-ab74-b7431b89f948
feature: Conversion Process Event Handler
role: Developer
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# Omzetproces, gebeurtenishandler {#id175UB30E05Z}

AEM Guides stelt de gebeurtenis com/adobe/fmdita/conversion/complete beschikbaar die wordt gebruikt om naverwerkingen uit te voeren nadat een documentconversieproces is voltooid. Deze gebeurtenis wordt geactiveerd wanneer een niet-DITA-document wordt gemigreerd naar de DITA-bestandsindeling. Als u bijvoorbeeld een Word naar DITA-conversie of een InDesign naar DITA-conversieproces uitvoert, wordt deze gebeurtenis aangeroepen nadat het conversieproces is beëindigd.

U moet een AEM gebeurtenishandler maken om de eigenschappen te lezen die beschikbaar zijn in deze gebeurtenis en verdere verwerking uit te voeren.

De gebeurtenisdetails worden hieronder uitgelegd:

**naam van de Gebeurtenis**:

```HTTP
com/adobe/fmdita/conversion/complete 
```

**Parameters**:\
|Naam|Type|Omschrijving|
|—|—|—|
|`status`|String|De geretourneerde status voor de uitgevoerde bewerking. De mogelijke opties zijn: -   SUCCESS: het conversieproces is voltooid. <br> -   VOLTOOID MET FOUTEN: het conversieproces is voltooid, maar met enkele fouten. <br>-   MISLUKT: het conversieproces is mislukt door een fatale fout.|
|`filePath`|String|Absoluut pad van het bronbestand \(om te converteren\) in AEM opslagplaats.|
|`outputPath`|String|Absoluut pad van de doellocatie waar de geconverteerde DITA-bestanden worden opgeslagen.|
|`logPath`|String|Absoluut pad van het knooppunt waar het conversielogbestand wordt opgeslagen.|
