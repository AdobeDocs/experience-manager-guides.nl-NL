---
title: Vraag configureren om een bestand bij sluiten in te checken
description: Leer hoe u de vraag om een bestand bij het sluiten in te checken configureert
exl-id: d184c97f-8405-4bcd-963d-635f17584897
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---

# Vraag configureren om een bestand bij sluiten in te checken {#id222HC040PE8}

Wanneer de gebruiker probeert om een dossier te sluiten dat in de Redacteur van het Web gebruikend **dicht** knoop op het lusje van het dossier of **dicht** optie in het menu van Opties wordt geopend, verschijnt een dialoog als het dossier unsaved gegevens of een niet bewaarde versie heeft. De gebruiker wordt gevraagd het bestand te ontgrendelen als het is vergrendeld.

**ontgrendel checkbox van het Dossier** niet door gebrek wordt toegelaten en u moet dit van configMgr toelaten. Voer de volgende stappen uit om de optie door gebrek in de Redacteur van het Web toe te laten:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.xmleditor.config.XmlEditorConfig** bundel.

1. Selecteer **vragen om controle-binnen op dichte** optie.

1. Klik **sparen**.


Wanneer deze configuratie wordt toegelaten, **ontgrendel checkbox van het Dossier** door gebrek in de dialoogdoos wordt geselecteerd.

Voor meer details, zie *Dossier sluiten en sparen scenario&#39;s* sectie in de Gebruikende as a Cloud Service gids van Adobe Experience Manager Guides.

**Bovenliggend onderwerp:**[ pas de Redacteur van het Web ](conf-web-editor.md) aan
