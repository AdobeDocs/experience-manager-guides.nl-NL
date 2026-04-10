---
title: Configuratieoverschrijvingen voor Cloud Service
description: Leer hoe te om met voeten te treden van de Configuratie
feature: Installation
role: Admin
level: Experienced
source-git-commit: 834959a6a0e22cd5d2b2c5d0e57ceb6d45c0c666
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# Configuratieoverschrijvingen voor Cloud Service {#id216IFC003XA}

Voor het uitvoeren van configuratieupdates in Experience Manager Guides as a Cloud Service moet de volgende algemene aanpak worden gebruikt:

1. Open de Cloud Manager Git-opslagplaats.

1. Maak een nieuw JSON-bestand op de volgende locatie:

   `src/main/content/jcr\_root/apps/fmditaCustom/config/`

1. Geef het bestand een naam in de volgende indeling:

   `$\{PID\}.cfg.json`

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

