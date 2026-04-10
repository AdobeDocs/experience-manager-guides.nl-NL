---
title: DITA Assets Replication for Cloud Service configureren
description: Leer hoe u replicatie van dita-middelen voor de cloudservice configureert
feature: Output Generation
role: Admin
level: Experienced
exl-id: 1eafc6b2-2b85-486a-bb2c-0038fae1fef9
hidefromtoc: true
source-git-commit: 564ee1731be2378744ffd2ed54a2fd423901a0b3
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 0%

---

# Replicatie van DITA-elementen configureren

Voer de volgende stappen uit om de functie voor elementverwerking te configureren:

1. Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](../cs-install-guide/download-install-additional-config-override.md) om het configuratiedossier tot stand te brengen.

1. Geef in het configuratiebestand de volgende gegevens (eigenschap) op:

   | PID | Eigenschappensleutel | Waarde van eigenschap |
   |---|---|---|
   | `com.adobe.fmdita.config.ConfigManager` | `publish.replicate` | **Standaardwaarde:** &quot;waar&quot; |
