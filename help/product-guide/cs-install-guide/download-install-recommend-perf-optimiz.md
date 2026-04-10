---
title: Aanbevelingen voor optimalisatie van prestaties
description: Meer informatie over aanbevelingen voor optimalisatie van prestaties
exl-id: 92ac1f81-2f51-44b0-82c3-56b39e8f3027
feature: Performance Optimization
role: Admin
level: Experienced
hidefromtoc: true
source-git-commit: 564ee1731be2378744ffd2ed54a2fd423901a0b3
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# Aanbevelingen voor optimalisatie van prestaties {#id213BD0JG0XA}

Houd rekening met de volgende punten voor het optimaliseren van prestaties:

- Om inhoud en het indexeren ervaring te optimaliseren, zie [&#x200B; het Onderzoek en het Indexeren van de Inhoud &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html?lang=nl-NL) in de documentatie van AEM optimaliseren.

- Reparatie Xerces Jar bij gebruik van aangepaste DITA-OT voor publicatie. Dit is een verplichte configuratie, afhankelijk van uw gebruiksgeval. Deze wijziging is alleen vereist als u aangepaste DITA-OT gebruikt voor het publiceren van uitvoer.

  *Vereiste configuratie*: Vervang het Jar van Xerces dossier in uw douaneDITA-OT pakket met één verscheepte OTB. Het standaard OOTB xercesImpl-2.11.0.jar- dossier is beschikbaar binnen /libs/fmdita/dita \ _resources/DITA-OT.zip. Zorg ervoor dat u de naam van het bestand xercesImpl-2.11.0.jar wijzigt zodat dit overeenkomt met het oude bestand Xerces Jar dat wordt vervangen. Dit kan tijdens runtime worden gedaan.

  Deze verandering vermindert de het publiceren tijd en geheugengebruik terwijl het publiceren van kaarten DITA met een groot aantal onderwerpen.


**Bovenliggend onderwerp:**&#x200B;[&#x200B; Download en installeer &#x200B;](download-install.md)
