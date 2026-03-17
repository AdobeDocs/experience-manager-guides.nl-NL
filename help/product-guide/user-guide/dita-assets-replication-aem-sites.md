---
title: Replicatie van DITA-bronelementen beheren
description: Leer hoe u replicatie van DITA-bronelementen uitvoert
feature: Publishing
role: User
source-git-commit: 52921a33d30817434424772ff32b1b31d4878497
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---

# Replicatie van DITA-bronelementen beheren

Wanneer de output die van inhoud DITA wordt geproduceerd gebruikend **Snelle publiceer** of **leidt Publicatie** op sommige publiceert milieu, probeert AEM ook om de bijbehorende DITA bronactiva, zoals kaarten DITA en, in sommige gevallen, onderwerpen DITA te publiceren. Dit gebeurt omdat AEM DITA-elementen behandelt als afhankelijkheden van de gegenereerde sitepagina&#39;s.

![](images/quick-publish-site-instance.png){width="350" align="left"}

Om de onbedoelde replicatie van DITA-inhoud naar het publicatiemilieu te verhinderen en prestatiesproblemen te vermijden, moeten de beheerders DITA activa-replicatie expliciet beheren via de Manager van de Configuratie. Deze configuratie laat beheerders toe om de replicatie van gesteunde activa te controleren DITA, met inbegrip van kaarten DITA, onderwerpen DITA, de dossiers van XML, en Prijsvermindering (.md) dossiers.

Om de eigenschap van de DITA activa replicatie te vormen, vormt de mening [ DITA activa replicatie voor Cloud Service ](../cs-install-guide/configure-dita-assets-replication.md) of [ DITA activa replicatie voor On-Premise ](../install-guide/configure-dita-asset-replication.md) afhankelijk van de opstelling u gebruikt

