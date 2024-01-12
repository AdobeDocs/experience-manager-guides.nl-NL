---
title: REST API voor werken met voorwaardelijke kenmerken
description: Meer informatie over de REST API om met voorwaardelijke kenmerken te werken
exl-id: 1f0e023a-422c-47b9-917f-b0d80090471c
feature: Rest API Conditional Attributes
role: Developer
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# REST API voor werken met voorwaardelijke kenmerken {#id175UB30E05Z}

Met de volgende REST API kunt u voorwaardelijke kenmerken toevoegen aan een mappenprofiel.

## Voorwaardelijk kenmerk toevoegen in een profiel op mapniveau

Een methode van de POST die voorwaardelijke attributen aan een bepaald omslag-vlakke profiel toevoegt.

**Aanvraag-URL**:\
http://*&lt;aem-guides-server>*: *&lt;port-number>*/bin/fmdita/folderprofiles

**Parameters**:\
|Naam|Type|Vereist|Beschrijving| |—|—|—|—| |`:operation`|String|Ja|Naam van de bewerking die wordt aangeroepen. De waarde van deze parameter is ``ADDATTRIBUTEPROFILES``. <br> **Opmerking:** De waarde is niet hoofdlettergevoelig.| |`profilename`|Tekenreeks|Ja|Naam weergeven van het profiel op mapniveau waarin de voorwaardelijke kenmerken moeten worden toegevoegd.| |`conditionalprofiles`|JSON-array|Yes|A JSON-array bestaande uit de voorwaardelijke kenmerknaam en -waarden. Het volgende codefragment van het voorbeeld toont de serie JSON met twee attributen - `platform` en `product` waarbij er meerdere waarden aan zijn toegewezen.|

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

**Responswaarden**:\
Retourneert een HTTP 200 \(Successful\) reactie.
