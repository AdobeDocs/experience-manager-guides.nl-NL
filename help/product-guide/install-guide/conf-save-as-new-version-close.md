---
title: Vraag configureren om bij het sluiten als een nieuwe versie op te slaan
description: Leer hoe te Vorm herinnering om als nieuwe versie bij dicht te bewaren
exl-id: 1b8c3eaa-a654-4563-9541-18a59b7d306c
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# Vraag configureren om bij het sluiten als een nieuwe versie op te slaan {#id222HBI00XXA}

Wanneer de gebruiker probeert om een dossier te sluiten dat in de Redacteur van het Web gebruikend **dicht** knoop op het lusje van het dossier of **dicht** optie in het menu van Opties wordt geopend, verschijnt een dialoog als het dossier unsaved gegevens of een niet bewaarde versie heeft. De gebruiker wordt gevraagd het bestand op te slaan als een nieuwe versie als de versie niet is opgeslagen.

**sparen als Nieuwe 1} checkbox van de Versie {wordt niet toegelaten door gebrek en u moet dit van configMgr toelaten.** Voer de volgende stappen uit om de optie door gebrek in de Redacteur van het Web toe te laten:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.xmleditor.config.XmlEditorConfig** bundel.

1. Selecteer **vragen om nieuwe versie op dichte** optie.

1. Klik **sparen**.


Wanneer deze optie wordt geselecteerd, **sparen als Nieuwe 1} checkbox van de Versie wordt geselecteerd door gebrek in de dialoogdoos.**

Voor meer details, zie *Dossier sluiten en sparen scenario&#39;s* sectie in de Gebruikende as a Cloud Service gids van Adobe Experience Manager Guides.

**Bovenliggend onderwerp:**[ pas de Redacteur van het Web ](conf-web-editor.md) aan
