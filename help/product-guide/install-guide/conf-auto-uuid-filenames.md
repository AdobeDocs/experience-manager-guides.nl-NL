---
title: Automatische bestandsnamen configureren op basis van UUID
description: Leer hoe u automatische bestandsnamen kunt configureren op basis van UUID
exl-id: 2a599228-6d46-494f-a57a-96c3f30e073a
feature: Filename Configuration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# Automatische bestandsnamen configureren op basis van UUID {#id205QG070D5Z}

Wanneer een onderwerp- of kaartbestand wordt gemaakt, krijgen auteurs standaard de mogelijkheid om ook de bestandsnaam op te geven. Auteurs kunnen de bestandsnamen naar wens toewijzen. Dit kan echter leiden tot inconsistentie en een groot aantal bestanden kan in een groot documentatiesysteem worden weergegeven. Als beheerder kunt u de auteurs beperken in het toewijzen van bestandsnamen voor de bestanden die ze in uw systeem maken. Voor elk nieuw onderwerp of kaartdossier, kunt u verkiezen om op UUID-Gebaseerde dossiernamen automatisch toe te wijzen.

Voer de volgende stappen uit om automatisch de op UUID gebaseerde bestandsnaam toe te wijzen voor alle nieuwe bestanden die in het systeem zijn gemaakt:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op *com.adobe.fmdita.xmleditor.config.XmlEditorConfig* bundel.

1. Selecteer de **optie van de Bestandsnamen van het Systeem UUID Gebaseerde van het Gebruik**.

1. Klik **sparen**.


>[!NOTE]
>
> Deze optie is standaard uitgeschakeld. Als deze optie is ingeschakeld, zien auteurs niet de optie om de bestandsnaam op te geven tijdens het maken van een nieuw onderwerp- of kaartbestand. Een nieuw onderwerp of kaartdossier kan van Assets UI en de Redacteur van het Web worden gecreeerd.

**Bovenliggend onderwerp:**&#x200B;[ vorm filenames ](conf-file-names.md)
