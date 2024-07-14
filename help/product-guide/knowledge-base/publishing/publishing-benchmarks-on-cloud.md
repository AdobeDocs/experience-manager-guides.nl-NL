---
title: Gidsen die Benchmarks op AEMaaCS publiceren
description: Begrijp systeembeperkingen bij het publiceren op AEM Cloud.
exl-id: 2cb4dfa4-dafc-409a-8d29-dbb00fabeae5
feature: Publishing
role: User, Admin
source-git-commit: be06612d832785a91a3b2a89b84e0c2438ba30f2
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 4%

---

# AEM Guides Publishing Benchmarks op AEMaaCS

De AEM Guides-cloudservice kent momenteel enkele limieten voor het publiceren van kaartgrootten die het team van hulplijnen actief probeert op te lossen.

Het team van gidsen heeft een scalable het publiceren microservice geïntroduceerd om grote kaarten en veelvoudige gezamenlijke het publiceren te steunen. Meer over nieuw leren publiceert microservice verwijs [ het publiceren microservice architectuur ](publish-microservice-architecture-and-performance.md)

Om de nieuwe het publiceren dienst voor om het even welk AEM wolkenmilieu te vormen verwijs [ nieuwe op microservice-gebaseerde het publiceren ](configure-microservices.md) vormen


## Uitvoeromgeving

     AEM Versie: 2023.5.11983.20230511T173830Z 
     Gids voegt op Versie toe: 2023.6.0 
     AEM het Malplaatje van de Plaats: AEM Guides OTB malplaatje 
     DITA-OT versie: 3.5.5 4 
     het Type van Werkschema van Publish: Splitste Publish Werkschema 
     Output die door microservice wordt gesteund: Inheemse PDF, PDF (Dita-OT) 

## Productienummers uitvoer

| Uitvoertype | Kaartgrootte (onderwerpverwijzingen) | Uitvoeringstijd (in seconden) | Publishing Microservice |
|---------------|------------------------------|----------------------------|-----------------------|
| Site AEM | 3500 | 5220 | Nee |
| Native PDF | 3500 | 780 | Ja |
| PDF (DITA-OT) | 11000 | 960 | Ja |
| HTML 5 | 3500 | 240 | Nee |
| Aangepast | 300 | 300 | Nee |

## Belangrijkste punten om te onthouden

- AEM Site maakt veel cq:paginaknooppunten en voegt deze af door ze tijdens de generatie afzonderlijk weer te geven. Daarom is het aan te raden om grote, meerdere gelijktijdige AEM Sitepublicaties niet uit te voeren, aangezien dit het systeem kan overbelasten.
- AEM de tijd van de Plaatsgeneratie hangt van het gebruikte malplaatje af. De uitvoeringstijd kan toenemen als een complexe sjabloon wordt gebruikt.
- De uitvoeringstijd voor aangepaste publicatie is voor een voorbeelduitvoer. Aangepaste publicatietijd is uitsluitend afhankelijk van de eigen transformatielogica van de klant.
