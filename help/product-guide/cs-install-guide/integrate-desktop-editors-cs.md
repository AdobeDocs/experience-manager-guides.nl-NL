---
title: XML-editors die zijn gebaseerd op een desktopcomputer integreren
description: Leer hoe u op bureaublad gebaseerde XML-editors kunt integreren
feature: Publishing FrameMaker Documents
role: Admin
level: Experienced
exl-id: 86ba53fa-0e08-4791-9018-09fe974691da
hidefromtoc: true
source-git-commit: 564ee1731be2378744ffd2ed54a2fd423901a0b3
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# XML-editors die zijn gebaseerd op een desktopcomputer integreren

Er zijn veel XML-editors beschikbaar op de markt en u kunt er al een gebruiken. Adobe FrameMaker is een van de krachtigste XML-editors, die wordt geleverd met AEM-connector. Met de AEM-connector in FrameMaker kunt u eenvoudig verbinding maken met de AEM-opslagplaats, bestanden voor uitchecken en inchecken en bestanden rechtstreeks in FrameMaker bewerken. U kunt Experience Manager Guides ook configureren om FrameMaker te starten vanuit de webeditor. Als u het bestand hebt geopend in FrameMaker, kunt u het bestand bewerken en terugcontroleren in de AEM-opslagplaats.

## Bestanden bewerken in FrameMaker inschakelen vanuit de webeditor

Met FrameMaker of een andere DITA-editor kunt u DITA-inhoud maken en bijwerken. Als uw organisatie FrameMaker echter als DITA-editor gebruikt, kunt u uw gebruikers de optie geven om DITA-documenten rechtstreeks vanuit AEM te openen in FrameMaker.


Door gebrek, zien uw gebruikers niet **Open in FrameMaker** knoop op de toolbar van AEM. Voer de volgende stappen uit om deze knop toe te voegen op de werkbalk van AEM:

Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\) gegevens op om deze knop toe te voegen op de werkbalk van AEM:


| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.openinframebuttonshow` | Boolean \(true/false\). Als u **Open in FrameMaker** knoop wilt tonen, dan plaats dit bezit aan waar. <br> **Standaardwaarde**: vals |



Als u versie 2409 en de versie van FrameMaker 2022 September - Update 3 gebruikt, moet u **Versie van FrameMaker 2022 Update 3 of hierboven** config voor uw gebruikers toelaten om de de serverdetails van Experience Manager Guides tot FrameMaker over te gaan.  Standaard is dit uitgeschakeld.


| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.openinframe2022above` | Boolean \(true/false\). Als u FrameMaker 2022 September release - Update 3 gebruikt, dan plaats dit bezit aan waar. <br> **Standaardwaarde**: vals |



Wanneer u *openinframebuttonshow* bezit aan waar plaatst, dan wordt de **Open in FrameMaker** knoop getoond bij het selecteren van om het even welk DITA- dossier in de bewaarplaats van AEM. Wanneer dit bezit niet aan *waar* wordt geplaatst, wordt **Open in FrameMaker** knoop getoond slechts wanneer u .fm of een .book dossier in de bewaarplaats selecteert.
