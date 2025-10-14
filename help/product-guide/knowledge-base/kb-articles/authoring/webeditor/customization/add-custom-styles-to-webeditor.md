---
title: Aangepaste stijlen toevoegen aan webeditor van hulplijnen
description: Leer hoe u aangepaste stijlen toevoegt om de vormgeving van de gulden-webeditor te wijzigen.
exl-id: 03143fb2-d05d-4103-b172-8b91880b7f9e
feature: Web Editor
role: User, Admin
source-git-commit: be06612d832785a91a3b2a89b84e0c2438ba30f2
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---

# Aangepaste stijlen toevoegen aan webeditor van hulplijnen

In dit artikel leert u hoe u aangepaste stijlen kunt toevoegen om de standaardweergave en het standaarduiterlijk van de spaander te wijzigen.

Dit omvat de volgende stappen:
- Aangepaste stijlen toevoegen via Configuratie XML-editor voor mapprofiel
- Het respectievelijke mapprofiel kiezen in de webbrowser en de wijzigingen testen


## Implementeren door een voorbeeld te nemen

Laten we dit begrijpen met een voorbeeld waarin we de korte beschrijving en titel als een apart blok willen weergeven met bepaalde stijlaspecten in de redactie.

![&#x200B; Previewing webeditor met douanestijlen &#x200B;](../../../assets/authoring/webeditor-customstyles-preview.png)


## Dit implementeren


### De aangepaste CSS toevoegen aan het mappenprofiel

Gebruik de omslagprofielen om *css_layout.css* onder het lusje van de Configuratie van de Redacteur van &quot;XML&quot;te controleren en CSS toe te voegen die douanestijlen heeft

[&#x200B; gebruik deze verbinding om meer over het profiel van de Omslag te leren en CSS malplaatjelay-out te vormen &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/videos/advanced-user-guide/editor-configuration.html?lang=nl-NL#customize-the-css-template-layout)

Gebruik het volgende om bovenstaande stijl in uw webeditor in te stellen:
- Gebruik [&#x200B; css_layout.css &#x200B;](../../../assets/authoring/webeditor-customstyles-css_layout.css) en upload het aan het omslagprofiel van uw keus
- Installeer het pakket in bijlage [&#x200B; webeditor-styles-resources.zip &#x200B;](../../../assets/authoring/webeditor-styles-resources.zip) gebruikend AEM pakketmanager om de middelen te installeren die in het bovengenoemde CSS dossier worden gebruikt

```
This will install the resources at path "/content/dam/resources" which will include sub-folders "fonts" and "images"
```


### Testen

- Webeditor openen
- Kies in de gebruikersvoorkeuren het mapprofiel waaraan u de aangepaste stijlen hebt toegevoegd. Als u het aan het Globale Profiel hebt toegevoegd, dan gebruikt u waarschijnlijk reeds dat.
- Open een onderwerp, zult u merken dat het het uitgeven gebied aangepaste UI zou moeten hebben

```
Please note this is compatible to AEM Guides version 4.2 and AEM Guides cloud version 2303 (March)
```


## Verwijzingen

U kunt ook in de deskundige zitting rond webeditor configuraties en aanpassing geinteresseerd zijn die in [&#x200B; worden behandeld Deskundige zitting op webeditor &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/tutorials/knowledge-base/expert-session/webbased-authoring-jan2023.html?lang=nl-NL)
