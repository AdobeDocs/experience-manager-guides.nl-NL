---
title: XML-editors die zijn gebaseerd op een desktopcomputer integreren
description: Leer hoe u op bureaublad gebaseerde XML-editors kunt integreren
exl-id: 268e8613-bb3b-4577-96fb-a588dabfd834
feature: Publishing FrameMaker Documents
role: Admin
level: Experienced
hidefromtoc: true
source-git-commit: 3aadc59f5034828cf319992b7acb32d5a88eaf93
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 0%

---

# XML-editors die zijn gebaseerd op een desktopcomputer integreren {#id181GB01G0HS}

Er zijn veel XML-editors beschikbaar op de markt en u kunt er al een gebruiken. Adobe FrameMaker is een van de krachtigste XML-editors, die wordt geleverd met AEM-connector. Met de AEM-connector in FrameMaker kunt u eenvoudig verbinding maken met de AEM-opslagplaats, bestanden voor uitchecken en inchecken en bestanden rechtstreeks in FrameMaker bewerken. U kunt Experience Manager Guides ook configureren om FrameMaker te starten vanuit de webeditor. Als u het bestand hebt geopend in FrameMaker, kunt u het bestand bewerken en terugcontroleren in de AEM-opslagplaats.

## Bestanden bewerken in FrameMaker inschakelen vanuit de webeditor

Met FrameMaker of een andere DITA-editor kunt u DITA-inhoud maken en bijwerken. Als uw organisatie FrameMaker echter als DITA-editor gebruikt, kunt u uw gebruikers de optie geven om DITA-documenten rechtstreeks vanuit AEM te openen in FrameMaker.

Door gebrek, zien uw gebruikers niet **Open in FrameMaker** knoop op de toolbar van AEM. Voer de volgende stappen uit om deze knop toe te voegen op de werkbalk van AEM:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.xmleditor.config.XmlEditorConfig** bundel.
   ![](assets/open-in-fm-config.png)

1. Selecteer **tonen Open in de Knoop van FrameMaker** optie.

1. Als u versie 4.6 en de versie van FrameMaker 2022 September - Update 3 gebruikt, moet u **Versie van FrameMaker 2022 Update 3 of hierboven** config voor uw gebruikers toelaten om de de serverdetails van Experience Manager Guides tot FrameMaker over te gaan. Standaard is dit uitgeschakeld.


1. Klik **sparen**.


Wanneer u **opent toont Open in de Knoop van FrameMaker** optie, dan wordt **Open in FrameMaker** knoop getoond bij het selecteren van om het even welk DITA- dossier in de bewaarplaats van AEM. Wanneer deze optie *niet* wordt toegelaten, **Open in FrameMaker** knoop wordt getoond slechts wanneer u een .fm of een .book dossier in de bewaarplaats selecteert.



