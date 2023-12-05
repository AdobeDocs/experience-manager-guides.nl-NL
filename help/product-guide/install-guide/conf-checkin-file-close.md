---
title: Vraag configureren om een bestand bij sluiten in te checken
description: Leer hoe u de vraag om een bestand bij het sluiten in te checken configureert
exl-id: d184c97f-8405-4bcd-963d-635f17584897
source-git-commit: 5e0584f1bf0216b8b00f00b9fe46fa682c244e08
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---

# Vraag configureren om een bestand bij sluiten in te checken {#id222HC040PE8}

Wanneer de gebruiker een dossier probeert te sluiten dat in de Redacteur van het Web gebruikend **Sluiten** op het tabblad van het bestand of op de knop **Sluiten** in het menu Opties wordt een dialoogvenster weergegeven als het bestand niet-opgeslagen gegevens of een niet-opgeslagen versie heeft. De gebruiker wordt gevraagd het bestand te ontgrendelen als het is vergrendeld.

De **Het bestand ontgrendelen** checkbox wordt niet toegelaten door gebrek en u moet dit van configMgr toelaten. Voer de volgende stappen uit om de optie door gebrek in de Redacteur van het Web toe te laten:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Zoeken naar en klikken op de knop **com.adobe.fmdita.xmleditor.config.XmlEditorConfig** bundel.

1. Selecteer de **Inchecken bij sluiten aanvragen** -optie.

1. Klikken **Opslaan**.


Wanneer deze configuratie wordt toegelaten, **Het bestand ontgrendelen** Selectievakje is standaard geselecteerd in het dialoogvenster.

Zie voor meer informatie *Bestanden sluiten en scenario&#39;s opslaan* in de as a Cloud Service handleiding Adobe Experience Manager-hulplijnen gebruiken.

**Bovenliggend onderwerp:**[ Webeditor aanpassen](conf-web-editor.md)
