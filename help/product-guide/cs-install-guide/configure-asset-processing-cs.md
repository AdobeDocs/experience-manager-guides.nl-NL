---
title: Asset-verwerking voor Cloud-service configureren
description: Meer informatie over het configureren van Asset Processing for Cloud-service
feature: Output Generation
role: Admin
level: Experienced
exl-id: 219a096f-4087-489f-9b3b-104864817198
hidefromtoc: true
source-git-commit: 564ee1731be2378744ffd2ed54a2fd423901a0b3
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 0%

---

# Functie voor middelenverwerking configureren

Voer de volgende stappen uit om de functie voor elementverwerking te configureren:

1. Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](../cs-install-guide/download-install-additional-config-override.md) om het configuratiedossier tot stand te brengen.

1. Geef in het configuratiebestand de volgende gegevens (eigenschap) op:

   | PID | Eigenschappensleutel | Waarde van eigenschap |
   |---|---|---|
   | `com.adobe.fmdita.config.ConfigManager` | `enable.asset.processing.scheduler` | **Standaardwaarde:** &quot;waar&quot; |
