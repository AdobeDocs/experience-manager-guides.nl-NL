---
title: XML-editors die zijn gebaseerd op een desktopcomputer integreren
description: Leer hoe u op bureaublad gebaseerde XML-editors kunt integreren
exl-id: 268e8613-bb3b-4577-96fb-a588dabfd834
feature: Publishing FrameMaker Documents
role: Admin
level: Experienced
source-git-commit: 82c7feab6599440c52ecbec845b5e3b8bb4a5046
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# XML-editors die zijn gebaseerd op een desktopcomputer integreren {#id181GB01G0HS}

Er zijn veel XML-editors beschikbaar op de markt en u kunt er al een gebruiken. Adobe FrameMaker is een van de krachtigste XML-editors en wordt geleverd met AEM connector. Met de AEM-connector in FrameMaker kunt u eenvoudig verbinding maken met de AEM opslagplaats, bestanden voor uitchecken en inchecken en bestanden rechtstreeks in FrameMaker bewerken. U kunt AEM Guides ook configureren om FrameMaker te starten vanuit de webeditor. Nadat u het bestand in de FrameMaker hebt geopend, kunt u het bestand bewerken en terugcontroleren in de AEM.

## Bestandsbewerking in FrameMaker inschakelen vanuit de webeditor

U kunt FrameMaker of een andere redacteur gebruiken DITA om inhoud tot stand te brengen en bij te werken DITA. Nochtans, als uw organisatie FrameMaker als redacteur DITA gebruikt, dan kunt u uw gebruikers een optie geven om documenten DITA direct in FrameMaker van AEM te openen.

Door gebrek, zien uw gebruikers niet **Open in FrameMaker** knoop op de AEM toolbar. Voer de volgende stappen uit om deze knop toe te voegen aan de werkbalk AEM:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.xmleditor.config.XmlEditorConfig** bundel.

   ![](assets/open-in-fm-toolbar.png){width="550" align="left"}

1. Selecteer **tonen Open in de FrameMaker** optie van de Knoop.

1. Klik **sparen**.


Wanneer u **opent toont Open in de FrameMakerKnoop** optie, dan wordt **Open in FrameMaker** knoop getoond bij het selecteren van om het even welk DITA- dossier in de AEM bewaarplaats. Wanneer deze optie *niet* wordt toegelaten, **Open in FrameMaker** knoop wordt getoond slechts wanneer u een .fm of een .book dossier in de bewaarplaats selecteert.
