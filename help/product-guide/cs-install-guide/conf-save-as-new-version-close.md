---
title: Vraag configureren om bij het sluiten als een nieuwe versie op te slaan
description: Leer hoe te Vorm herinnering om als nieuwe versie bij dicht te bewaren
exl-id: 9029b671-8ff8-45eb-b27e-ab89bd09e7ed
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 0%

---

# Vraag configureren om bij het sluiten als een nieuwe versie op te slaan {#id222HBI00XXA}

Wanneer de gebruiker probeert om een dossier te sluiten dat in de Redacteur van het Web gebruikend **dicht** knoop op het lusje van het dossier of **dicht** optie in het menu van Opties wordt geopend, verschijnt een dialoog als het dossier unsaved gegevens of een niet bewaarde versie heeft. De gebruiker wordt gevraagd het bestand op te slaan als een nieuwe versie als de versie niet is opgeslagen.

Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om een vraag te configureren om bij het sluiten als een nieuwe versie op te slaan:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.savenewversion` | Boolean \( true/ false\). <br>  **Standaardwaarde**: waar |

Wanneer deze configuratie wordt toegelaten, **sparen als Nieuwe 1&rbrace; checkbox van de Versie &lbrace;door gebrek in de dialoogdoos wordt geselecteerd.**

Voor meer details, zie *Dossier sluiten en sparen scenario&#39;s* sectie in de Gebruikende as a Cloud Service gids van Adobe Experience Manager Guides.

**Bovenliggend onderwerp:**&#x200B;[ pas de Redacteur van het Web ](conf-web-editor.md) aan
