---
title: Geldige bestandsnamen voor AEM Site-uitvoer configureren
description: Leer hoe u geldige bestandsnamen voor AEM Site-uitvoer kunt configureren
exl-id: 05215bec-653b-4563-83c6-a1bb16200469
feature: Filename Configuration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# Geldige bestandsnamen voor AEM Site-uitvoer configureren {#id214GK0X0KXA}

Net als de lijst met geldige bestandsnaamtekens die zijn toegestaan voor DITA-onderwerpen, kunt u ook een lijst met geldige bestandsnaamtekens configureren voor AEM Site-uitvoer. Enkele bekende tekens die niet in een URL zijn toegestaan, zijn: ``'<>`@$`` . Deze karakters worden gevormd om automatisch in een onderstrepingsteken &quot;`_`&quot;om te zetten wanneer zij terwijl het produceren van AEM de namen van het de outputdossier van de Plaats worden gevonden.

Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om geldige tekens in te stellen in AEM Site-uitvoer:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.common.SanitizeNodeNameImpl` | `aemsite.DisallowedFileNameChars` | Voeg tekens toe die u wilt vervangen door een onderstrepingsteken in de namen van de uitvoerbestanden van de AEM. <br> **Standaardwaarde**: ``'<\>\`@$`` |

**Bovenliggend onderwerp:**&#x200B;[ vorm filenames ](conf-file-names.md)
