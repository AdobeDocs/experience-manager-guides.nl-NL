---
title: Geldige bestandsnamen voor AEM Site-uitvoer configureren
description: Leer hoe u geldige bestandsnamen voor AEM Site-uitvoer configureert
exl-id: 05215bec-653b-4563-83c6-a1bb16200469
feature: Filename Configuration
role: Admin
level: Experienced
hidefromtoc: true
source-git-commit: 564ee1731be2378744ffd2ed54a2fd423901a0b3
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# Geldige bestandsnamen voor AEM Site-uitvoer configureren {#id214GK0X0KXA}

Net als bij de lijst met geldige bestandsnaamtekens die zijn toegestaan voor DITA-onderwerpen, kunt u ook een lijst met geldige bestandsnaamtekens configureren voor AEM Site-uitvoer. Enkele bekende tekens die niet in een URL zijn toegestaan, zijn: ``'<>`@$`` . Deze karakters worden gevormd om automatisch in een onderstrepingsteken &quot;`_`&quot;om te zetten wanneer zij terwijl het produceren van de namen van het de outputdossier van de Plaats van AEM worden gevonden.

Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om geldige tekens in te stellen in de uitvoer van de AEM-site:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.common.SanitizeNodeNameImpl` | `aemsite.DisallowedFileNameChars` | Voeg tekens toe die u wilt vervangen door een onderstrepingsteken in de namen van de uitvoerbestanden van de AEM-site. <br> **Standaardwaarde**: ``'<\>\`@$`` |

**Bovenliggend onderwerp:**[ vorm filenames ](conf-file-names.md)
