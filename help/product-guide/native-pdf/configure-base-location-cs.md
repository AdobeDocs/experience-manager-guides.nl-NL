---
title: Native PDF | Basisuitvoerlocatie configureren voor het publiceren van PDF for Cloud-services
description: Basisuitvoerlocatie configureren voor het publiceren van PDF for Cloud-services
feature: Output Generation
role: Admin
level: Experienced
exl-id: d79085d6-938a-4e80-84a2-03562e6b76e0
hidefromtoc: true
source-git-commit: 564ee1731be2378744ffd2ed54a2fd423901a0b3
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---

# Basisuitvoerlocatie configureren voor het publiceren van uitvoer voor cloudservices

Voer de volgende stappen uit om de basisuitvoerlocatie te configureren:

1. Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](../cs-install-guide/download-install-additional-config-override.md) om het configuratiedossier tot stand te brengen.

1. In het configuratiedossier, verstrek de volgende (bezit) details om de plaats van de basisoutput te vormen:

   | PID | Eigenschappensleutel | Waarde van eigenschap |
   |---|---|---|
   | `com.adobe.fmdita.config.ConfigManager` | `base.output.path` | **Standaardwaarde:** &quot;/content/dam/fmdita-outputs&quot; |
