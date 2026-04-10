---
title: Vraag configureren om een bestand bij sluiten in te checken
description: Leer hoe u de vraag om een bestand bij het sluiten in te checken configureert
exl-id: 5b09ec46-aea4-4a3f-8bab-42414e31e37d
feature: Web Editor Configuration
role: Admin
level: Experienced
hidefromtoc: true
source-git-commit: 564ee1731be2378744ffd2ed54a2fd423901a0b3
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# Vraag configureren om een bestand bij sluiten in te checken {#id222HC040PE8}

Wanneer de gebruiker probeert om een dossier te sluiten dat in de Redacteur van het Web gebruikend **dicht** knoop op het lusje van het dossier of **dicht** optie in het menu van Opties wordt geopend, verschijnt een dialoog als het dossier unsaved gegevens of een niet bewaarde versie heeft. De gebruiker wordt gevraagd het bestand te ontgrendelen als het is vergrendeld.

Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om een vraag te configureren om een bestand bij het sluiten in te checken:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.checkin` | Boolean \( true/ false\).<br> **Standaardwaarde**: vals |

Wanneer deze configuratie wordt toegelaten, **ontgrendel checkbox van het Dossier** door gebrek in de dialoogdoos wordt geselecteerd.

Voor meer details, zie *Dossier sluiten en sparen scenario&#39;s* sectie in de Gebruikende gids van Adobe Experience Manager Guides as a Cloud Service.

**Bovenliggend onderwerp:**&#x200B;[&#x200B; pas de Redacteur van het Web &#x200B;](conf-web-editor.md) aan
