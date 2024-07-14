---
title: Recommendations for performance optimization
description: Meer informatie over Recommendations voor optimalisatie van prestaties
exl-id: 92ac1f81-2f51-44b0-82c3-56b39e8f3027
feature: Performance Optimization
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# Recommendations for performance optimization {#id213BD0JG0XA}

Houd rekening met de volgende punten voor het optimaliseren van prestaties:

- Om inhoud en het indexeren ervaring te optimaliseren, zie [ het Onderzoek en het Indexeren van de Inhoud ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html) in AEM documentatie optimaliseren.

- Reparatie Xerces Jar bij gebruik van aangepaste DITA-OT voor publicatie. Dit is een verplichte configuratie, afhankelijk van uw gebruiksgeval. Deze wijziging is alleen vereist als u aangepaste DITA-OT gebruikt voor het publiceren van uitvoer.

  *Vereiste configuratie*: Vervang het Jar van Xerces dossier in uw douaneDITA-OT pakket met één verscheepte OTB. Het standaard OOTB xercesImpl-2.11.0.jar- dossier is beschikbaar binnen /libs/fmdita/dita \ _resources/DITA-OT.zip. Zorg ervoor dat u de naam van het bestand xercesImpl-2.11.0.jar wijzigt zodat dit overeenkomt met het oude bestand Xerces Jar dat wordt vervangen. Dit kan tijdens runtime worden gedaan.

  Deze verandering vermindert de het publiceren tijd en geheugengebruik terwijl het publiceren van kaarten DITA met een groot aantal onderwerpen.


**Bovenliggend onderwerp:**[ Download en installeer ](download-install.md)
