---
title: Geldige bestandsnamen voor AEM Site-uitvoer configureren
description: Leer hoe u geldige bestandsnamen voor AEM Site-uitvoer kunt configureren
exl-id: 05215bec-653b-4563-83c6-a1bb16200469
source-git-commit: 5e0584f1bf0216b8b00f00b9fe46fa682c244e08
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# Geldige bestandsnamen voor AEM Site-uitvoer configureren {#id214GK0X0KXA}

Net als de lijst met geldige bestandsnaamtekens die zijn toegestaan voor DITA-onderwerpen, kunt u ook een lijst met geldige bestandsnaamtekens configureren voor AEM Site-uitvoer. Enkele bekende tekens die niet in een URL zijn toegestaan, zijn: ``'<>`@$``. Deze tekens zijn zo geconfigureerd dat ze automatisch worden omgezet in een onderstrepingsteken &quot;`_`&quot; wanneer deze worden gevonden tijdens het genereren van AEM namen voor uitvoerbestanden van de site.

Gebruik de instructies die worden gegeven in [Configuratieoverschrijvingen](download-install-additional-config-override.md#) om het configuratiebestand te maken. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om geldige tekens in te stellen in AEM Site-uitvoer:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.common.SanitizeNodeNameImpl` | `aemsite.DisallowedFileNameChars` | Voeg tekens toe die u wilt vervangen door een onderstrepingsteken in de namen van de uitvoerbestanden van de AEM. <br> **Standaardwaarde**: ``'<\>\`@$`` |

**Bovenliggend onderwerp:**[ Bestandsnamen configureren](conf-file-names.md)
