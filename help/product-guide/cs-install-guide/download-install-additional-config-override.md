---
title: Configuratieoverschrijvingen
description: Leer hoe te om met voeten te treden van de Configuratie
exl-id: dc5f81f7-5b0a-4d12-a944-ba66b0239d5c
source-git-commit: 5e0584f1bf0216b8b00f00b9fe46fa682c244e08
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---

# Configuratieoverschrijvingen {#id216IFC003XA}

Voor het maken van om het even welke configuratieupdates, zou de volgende generische benadering moeten worden gebruikt:

1. Open de Git-opslagplaats van uw Cloud Manager.

1. Maak een nieuw JSON-bestand op de volgende locatie:

   src/main/content/jcr\_root/apps/fmditaCustom/config/

1. Geef het bestand een naam in de volgende indeling:

   $\{PID\}.cfg.json

   Hier, is PID procesidentiteitskaart van de configuratie.

1. Voeg eigenschappen in het JSON-bestand toe in de volgende indeling:

   ```
   {
      "aem.adminuname": "updatedUserjson",
      "valid.characters": "[-a-zA-Z0-9_@$]",
      "dita.serialization": true
   }
   ```

1. Leg de wijzigingen vast en voer de Cloud Manager-pijplijn uit om de bijgewerkte configuratie te implementeren.


**Bovenliggend onderwerp:**[ Downloaden en installeren](download-install.md)
