---
title: Geldige bestandsnamen voor AEM Site-uitvoer configureren
description: Leer hoe u geldige bestandsnamen voor AEM Site-uitvoer configureert
feature: Filename Configuration
role: Admin
level: Experienced
source-git-commit: 6f3f05419f4f5cdd45ab580cdee6fa869f20f01d
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# Geldige bestandsnamen voor AEM Site-uitvoer configureren {#id214GK0X0KXA}

Net als bij de lijst met geldige bestandsnaamtekens die zijn toegestaan voor DITA-onderwerpen, kunt u ook een lijst met geldige bestandsnaamtekens configureren voor AEM Site-uitvoer. Enkele bekende tekens die niet in een URL zijn toegestaan, zijn: ``'<>`@$`` . Deze karakters worden gevormd om automatisch in een onderstrepingsteken &quot;`_`&quot;om te zetten wanneer zij terwijl het produceren van de namen van het de outputdossier van de Plaats van AEM worden gevonden.

Op de volgende tabbladen vindt u instructies voor het configureren van geldige bestandsnamen voor AEM Site-uitvoer op basis van uw Experience Manager Guides-instellingen: Cloud Service of On-Premise.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](download-install-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om geldige tekens in te stellen in de uitvoer van de AEM-site:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.common.SanitizeNodeNameImpl` | `aemsite.DisallowedFileNameChars` | Voeg tekens toe die u wilt vervangen door een onderstrepingsteken in de namen van de uitvoerbestanden van de AEM-site. <br> **Standaardwaarde**: ``'<\>\`@$`` |

>[!TAB  Op locatie ]

De configuratie waarmee u geldige tekens kunt instellen in AEM Site-uitvoer is aanwezig in de `com.adobe.fmdita.common.SanitizeNodeNameImpl` -bundel. **plaats het Geweigerde Karakter voor het Publiceren aan AEM Sites** plaatsen om karakters te omvatten die u met een onderstrepingsteken in de de uitvoerdossiernamen van de Plaats van AEM wilt vervangen.

>[!ENDTABS]
