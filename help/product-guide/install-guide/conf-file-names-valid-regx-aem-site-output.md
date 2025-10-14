---
title: Geldige bestandsnamen voor AEM Site-uitvoer configureren
description: Leer hoe u geldige bestandsnamen voor AEM Site-uitvoer kunt configureren
exl-id: 1e69d6f8-7baf-4189-bbbd-34cd0fec6634
feature: Filename Configuration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# Geldige bestandsnamen voor AEM Site-uitvoer configureren {#id214GK0X0KXA}

Net als de lijst met geldige bestandsnaamtekens die zijn toegestaan voor DITA-onderwerpen, kunt u ook een lijst met geldige bestandsnaamtekens configureren voor AEM Site-uitvoer. Enkele bekende tekens die niet in een URL zijn toegestaan, zijn: ```'<>`@$``` . Deze tekens zijn geconfigureerd om automatisch om te zetten in een onderstrepingsteken &quot;_&quot; wanneer ze worden gevonden tijdens het genereren van AEM naam voor uitvoerbestanden van de site. De configuratie waarmee u geldige tekens kunt instellen in AEM site-uitvoer is aanwezig in de `com.adobe.fmdita.common.SanitizeNodeNameImpl` -bundel. **plaats het Geweigerde Karakter dat voor het Publiceren aan AEM Sites** wordt geplaatst om karakters te omvatten die u met een onderstrepingsteken in de het outputdossiernamen van de AEM Plaats wilt vervangen.

**Bovenliggend onderwerp:**&#x200B;[&#x200B; vorm filenames &#x200B;](conf-file-names.md)
