---
title: Aanbevelingen voor optimalisatie van prestaties voor Cloud Service
description: Meer informatie over aanbevelingen voor optimalisatie van prestaties
feature: Performance Optimization
role: Admin
level: Experienced
source-git-commit: 834959a6a0e22cd5d2b2c5d0e57ceb6d45c0c666
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# Aanbevelingen voor optimalisatie van prestaties voor Cloud Service {#id213BD0JG0XA}

Houd rekening met de volgende punten voor het optimaliseren van prestaties:

- Om inhoud en het indexeren ervaring te optimaliseren, zie [&#x200B; het Onderzoek en het Indexeren van de Inhoud &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html?lang=nl-NL) in de documentatie van AEM optimaliseren.

- Reparatie Xerces Jar bij gebruik van aangepaste DITA-OT voor publicatie. Dit is een verplichte configuratie, afhankelijk van uw gebruiksgeval. Deze wijziging is alleen vereist als u aangepaste DITA-OT gebruikt voor het publiceren van uitvoer.

  *Vereiste configuratie*: Vervang het Jar van Xerces dossier in uw douaneDITA-OT pakket met één verscheepte OTB. Het standaard OOTB `xercesImpl-2.11.0.jar` -bestand is beschikbaar in het `/libs/fmdita/dita\_resources/DITA-OT.zip` -bestand. Zorg ervoor dat de naam van het `xercesImpl-2.11.0.jar` -bestand overeenkomt met het oude Xerces Jar-bestand dat wordt vervangen. Dit kan tijdens runtime worden gedaan.

  Deze verandering vermindert de het publiceren tijd en geheugengebruik terwijl het publiceren van kaarten DITA met een groot aantal onderwerpen.

