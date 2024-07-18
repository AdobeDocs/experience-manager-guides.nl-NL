---
title: REST API voor werken met voorwaardelijke kenmerken
description: Meer informatie over de REST API om met voorwaardelijke kenmerken te werken
exl-id: 1f0e023a-422c-47b9-917f-b0d80090471c
feature: Rest API Conditional Attributes
role: Developer
level: Experienced
source-git-commit: 6184bb98c9897e980a6fba2f97476570228188af
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# REST API voor werken met voorwaardelijke kenmerken {#id175UB30E05Z}

Met de volgende REST API kunt u voorwaardelijke kenmerken toevoegen aan een mappenprofiel.

## Voorwaardelijk kenmerk toevoegen in een profiel op mapniveau

Een methode van de POST die voorwaardelijke attributen aan een bepaald omslag-vlakke profiel toevoegt.

**Verzoek URL**:\
http://*&lt;aem-guides-server\>*: *&lt;port-number\>*/bin/fmdita/folderProfile

**Parameters**:

| Naam | Type | Vereist | Beschrijving |
|----|----|--------|-----------|
| `:operation` | String | Ja | Naam van de bewerking die wordt aangeroepen. De waarde van deze parameter is ``ADDATTRIBUTEPROFILES`` . <br> **Nota:** de waarde is case-insensitive. |
| `profilename` | String | Ja | De naam van de vertoning van het omslag-vlakke profiel waarin de voorwaardelijke attributen moeten worden toegevoegd. |
| `conditionalprofiles` | JSON-array | Ja | Een JSON-array die bestaat uit de voorwaardelijke kenmerknaam en -waarden. Het volgende codefragment uit het voorbeeld toont de JSON-array met twee kenmerken - `platform` en `product` waarbij meerdere waarden aan deze kenmerken zijn toegewezen. |

```JSON
[  {    name: "platform",    
        values: [       
                {value: "win", label: "Windows"},       
                {value: "mac", label: "Mac OS"}    
                ]},
                {    
                    name: "product",    
                    values: [      
                        {value: "aem_1", label: "AEM 6.1"},     
                        {value: "aem_4,  label: "AEM 6.4"}  
                        ]  
                }]
```

**waarden van de Reactie**:\
Retourneert een HTTP 200 \(Successful\) reactie.
