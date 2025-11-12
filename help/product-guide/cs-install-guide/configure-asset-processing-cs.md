---
title: Asset-verwerking voor Cloud-service configureren
description: Meer informatie over het configureren van Asset Processing for Cloud-service
feature: Output Generation
role: Admin
level: Experienced
source-git-commit: 5b29b2b5f725b5d9a2029fb232e62f387a5338fd
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
