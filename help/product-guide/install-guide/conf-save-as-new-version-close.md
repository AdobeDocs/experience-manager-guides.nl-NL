---
title: Vraag configureren om bij het sluiten als een nieuwe versie op te slaan
description: Leer hoe te Vorm herinnering om als nieuwe versie bij dicht te bewaren
exl-id: 1b8c3eaa-a654-4563-9541-18a59b7d306c
source-git-commit: 5e0584f1bf0216b8b00f00b9fe46fa682c244e08
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# Vraag configureren om bij het sluiten als een nieuwe versie op te slaan {#id222HBI00XXA}

Wanneer de gebruiker een dossier probeert te sluiten dat in de Redacteur van het Web gebruikend **Sluiten** op het tabblad van het bestand of op de knop **Sluiten** in het menu Opties wordt een dialoogvenster weergegeven als het bestand niet-opgeslagen gegevens of een niet-opgeslagen versie heeft. De gebruiker wordt gevraagd het bestand op te slaan als een nieuwe versie als de versie niet is opgeslagen.

De **Opslaan als nieuwe versie** checkbox wordt niet toegelaten door gebrek en u moet dit van configMgr toelaten. Voer de volgende stappen uit om de optie door gebrek in de Redacteur van het Web toe te laten:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Zoeken naar en klikken op de knop **com.adobe.fmdita.xmleditor.config.XmlEditorConfig** bundel.

1. Selecteer de **Nieuwe versie aanvragen bij sluiten** -optie.

1. Klikken **Opslaan**.


Als deze optie is geselecteerd, wordt **Opslaan als nieuwe versie** Selectievakje is standaard geselecteerd in het dialoogvenster.

Zie voor meer informatie *Bestanden sluiten en scenario&#39;s opslaan* in de as a Cloud Service handleiding Adobe Experience Manager-hulplijnen gebruiken.

**Bovenliggend onderwerp:**[ Webeditor aanpassen](conf-web-editor.md)
