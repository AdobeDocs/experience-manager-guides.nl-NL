---
title: Bestanden automatisch opslaan in de webeditor configureren
description: Leer hoe te om dossier te vormen automatisch sparen in de Redacteur van het Web
exl-id: 23fe404c-c76d-43ba-9b28-c49ab1e524de
source-git-commit: 5e0584f1bf0216b8b00f00b9fe46fa682c244e08
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---

# Bestanden automatisch opslaan in de webeditor configureren {#id199CC0J0M5Z}

Een van de meest gebruikte functies in de op een browser gebaseerde editor is de mogelijkheid om gegevens na een bepaalde tijdsperiode op te slaan. De redacteur van het Web van de Gidsen van de AEM steunt ook auto-sparen van onderwerp en kaartdossiers bij het gespecificeerde tijdinterval. Wanneer deze eigenschap wordt teweeggebracht, wordt het werkende exemplaar van het onderwerp of de kaart bewaard. Er wordt geen nieuwe versie van het onderwerp of de kaart gemaakt. Als u een nieuwe versie wilt maken, klikt u op het pictogram Revisie opslaan op de werkbalk van de webeditor.

De auto-sparen eigenschap wordt niet toegelaten door gebrek en u moet dit van configMgr toelaten. Voer de volgende stappen uit om de auto-sparen eigenschap in de Redacteur van het Web toe te laten:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Zoeken naar en klikken op de knop **com.adobe.fmdita.xmleditor.config.XmlEditorConfig** bundel.

1. In de *XmlEditorConfig* instellingen, selecteert u de **Automatisch opslaan** -optie.

1. In de **Interval automatisch opslaan** geeft u het tijdsinterval in seconden op om de functie voor automatisch opslaan te activeren.

1. Klikken **Opslaan**.


**Bovenliggend onderwerp:**[ Webeditor aanpassen](conf-web-editor.md)
