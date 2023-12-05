---
title: Geldige bestandsnamen voor AEM Site-uitvoer configureren
description: Leer hoe u geldige bestandsnamen voor AEM Site-uitvoer kunt configureren
exl-id: 1e69d6f8-7baf-4189-bbbd-34cd0fec6634
source-git-commit: 5e0584f1bf0216b8b00f00b9fe46fa682c244e08
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# Geldige bestandsnamen voor AEM Site-uitvoer configureren {#id214GK0X0KXA}

Net als de lijst met geldige bestandsnaamtekens die zijn toegestaan voor DITA-onderwerpen, kunt u ook een lijst met geldige bestandsnaamtekens configureren voor AEM Site-uitvoer. Enkele bekende tekens die niet in een URL zijn toegestaan, zijn: ```'<>`@$```. Deze tekens zijn geconfigureerd om automatisch om te zetten in een onderstrepingsteken &quot;_&quot; wanneer ze worden gevonden tijdens het genereren van AEM naam voor uitvoerbestanden van de site. De configuratie die u toestaat om geldige karakters in AEM output van de Plaats te plaatsen is aanwezig in `com.adobe.fmdita.common.SanitizeNodeNameImpl` bundel. **De niet-toegestane tekenset voor publicatie instellen op AEM Sites** het plaatsen om karakters op te nemen die u met een onderstrepingsteken in de AEM de dossiernamen van de output van de Plaats wilt vervangen.

**Bovenliggend onderwerp:**[ Bestandsnamen configureren](conf-file-names.md)
