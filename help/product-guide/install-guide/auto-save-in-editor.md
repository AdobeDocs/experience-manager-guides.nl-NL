---
title: Bestanden automatisch opslaan in de webeditor configureren
description: Leer hoe te om dossier te vormen automatisch sparen in de Redacteur van het Web
exl-id: 23fe404c-c76d-43ba-9b28-c49ab1e524de
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---

# Bestanden automatisch opslaan in de webeditor configureren {#id199CC0J0M5Z}

Een van de meest gebruikte functies in de op een browser gebaseerde editor is de mogelijkheid om gegevens na een bepaalde tijdsperiode op te slaan. De Redacteur van het Web van AEM Guides steunt ook auto-sparen van onderwerp en kaartdossiers bij het gespecificeerde tijdinterval. Wanneer deze eigenschap wordt teweeggebracht, wordt het werkende exemplaar van het onderwerp of de kaart bewaard. Er wordt geen nieuwe versie van het onderwerp of de kaart gemaakt. Als u een nieuwe versie wilt maken, klikt u op het pictogram Revisie opslaan op de werkbalk van de webeditor.

De auto-sparen eigenschap wordt niet toegelaten door gebrek en u moet dit van configMgr toelaten. Voer de volgende stappen uit om de auto-sparen eigenschap in de Redacteur van het Web toe te laten:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.xmleditor.config.XmlEditorConfig** bundel.

1. In de *montages 0} XmlEditorConfig, selecteer **Auto sparen**optie.*

1. Op het **Auto sparen het gebied van het Interval**, specificeer het tijdinterval in seconden om de auto-sparen eigenschap teweeg te brengen.

1. Klik **sparen**.


**Bovenliggend onderwerp:**[ pas de Redacteur van het Web ](conf-web-editor.md) aan
