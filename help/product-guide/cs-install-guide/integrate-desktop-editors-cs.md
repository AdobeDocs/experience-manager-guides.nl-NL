---
title: XML-editors die zijn gebaseerd op een desktopcomputer integreren
description: Leer hoe u op bureaublad gebaseerde XML-editors kunt integreren
feature: Publishing FrameMaker Documents
role: Admin
level: Experienced
source-git-commit: b3ae1c02d3055fe15257d5de0365d30e7af21afb
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# XML-editors die zijn gebaseerd op een desktopcomputer integreren

Er zijn veel XML-editors beschikbaar op de markt en u kunt er al een gebruiken. Adobe FrameMaker is een van de krachtigste XML-editors en wordt geleverd met AEM connector. Met de AEM-connector in FrameMaker kunt u eenvoudig verbinding maken met de AEM opslagplaats, bestanden voor uitchecken en inchecken en bestanden rechtstreeks in FrameMaker bewerken. U kunt Experience Manager Guides ook configureren om FrameMaker te starten vanuit de webeditor. Nadat u het bestand in de FrameMaker hebt geopend, kunt u het bestand bewerken en terugcontroleren in de AEM.

## Bestandsbewerking in FrameMaker inschakelen vanuit de webeditor

U kunt FrameMaker of een andere redacteur gebruiken DITA om inhoud tot stand te brengen en bij te werken DITA. Nochtans, als uw organisatie FrameMaker als redacteur DITA gebruikt, dan kunt u uw gebruikers een optie geven om documenten DITA direct in FrameMaker van AEM te openen.


Door gebrek, zien uw gebruikers niet **Open in FrameMaker** knoop op de AEM toolbar. Voer de volgende stappen uit om deze knop toe te voegen aan de werkbalk AEM:

Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\) gegevens op om deze knop op de werkbalk AEM toe te voegen:


| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.openinframebuttonshow` | Boolean \(true/false\). Als u **Open in FrameMaker** knoop wilt tonen, dan plaats dit bezit aan waar. <br> **Standaardwaarde**: vals |



Als u versie 2409 en FrameMaker versie 2022 September - Update 3 gebruikt, moet u **Versie 2022 Update 3 van de FrameMaker of hierboven** config voor uw gebruikers toelaten om op de de serverdetails van Experience Manager Guides tot FrameMaker over te gaan.  Standaard is dit uitgeschakeld.


| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.openinframe2022above` | Boolean \(true/false\). Als u FrameMaker 2022 de versie van September - Update 3 gebruikt, dan plaats dit bezit aan waar. <br> **Standaardwaarde**: vals |



Wanneer u *openinframebuttonshow* bezit aan waar plaatst, dan wordt **Open in FrameMaker** knoop getoond bij het selecteren van om het even welk DITA- dossier in de AEM bewaarplaats. Wanneer dit bezit niet aan *waar* wordt geplaatst, wordt **Open in FrameMaker** knoop getoond slechts wanneer u .fm of een .book dossier in de bewaarplaats selecteert.



