---
title: DITA Assets Replication for Cloud Service configureren
description: Leer hoe u replicatie van dita-middelen voor de cloudservice configureert
feature: Output Generation
role: Admin
level: Experienced
source-git-commit: 356ea6edd5e688fb1f77e737c705ed0bd4d2e7f0
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 0%

---

# Replicatie van DITA-elementen configureren

Voer de volgende stappen uit om de functie voor elementverwerking te configureren:

1. Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](../cs-install-guide/download-install-additional-config-override.md) om het configuratiedossier tot stand te brengen.

1. Geef in het configuratiebestand de volgende gegevens (eigenschap) op:

   | PID | Eigenschappensleutel | Waarde van eigenschap |
   |---|---|---|
   | `com.adobe.fmdita.config.ConfigManager` | `publish.replicate` | **Standaardwaarde:** &quot;waar&quot; |
