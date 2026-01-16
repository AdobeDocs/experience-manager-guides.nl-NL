---
title: Opmerkingen bij de release | Problemen met Adobe Experience Manager Guides 5.1.0 Service Pack 3-release opgelost.
description: Meer informatie over de opgeloste problemen vindt u in de 5.1.0 Service Pack 3-release van Adobe Experience Manager Guides
role: Leader
source-git-commit: 82eb0e18eb285006c66b1fe2b6ecc3ca86fefe61
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# Oplossingen voor problemen in de 5.1.0 Service Pack 3-release (december 2025)


Dit artikel behandelt de fouten die in diverse gebieden van 5.1.0 Service Pack 3 versie van Adobe Experience Manager Guides worden opgelost.

Leer over [ verbeteringsinstructies voor 5.1.0 Service Pack 3 versie ](upgrade-instructions-5-1-0-sp3.md).


## Authoring

- Aangepaste CSS die wordt toegepast in een mapprofiel voor onderwerpen of mappen, wordt teruggezet naar de standaardstijl in de modus Voorbeeld wanneer de browser wordt vernieuwd. (GUIDEN-31098)
- Onbekwaam om de veelvoudige **etiketten van de Versie** aan een onderwerp van **toe te voegen sparen als nieuwe versie** dialoog. (GUIDEN-32716)


## Beheer van bedrijfsmiddelen

- Onbekwaam om de etiketten van de Versie uit **geschiedenis van de Versie** paneel in Assets UI te verwijderen. (GUIDEN-38276)


## Controleren

- Wanneer een revisor een revisietaak voltooit of een aanvrager een revisietaak bijwerkt zonder opmerkingen in te voeren, wordt in het e-mailbericht dat wordt verzonden de meest recente vorige opmerking weergegeven. (HIDEN-33590)

## Publiceren

- Wanneer u AEM Sites-uitvoer genereert met behulp van oude componenttoewijzing, worden onderwerpen die het kenmerk `copy-to` gebruiken, gepubliceerd met de naam van het `copy-from` -onderwerp in plaats van de naam die is ingesteld in het kenmerk `copy-to` . (HULPLIJNEN-22155)
- Wanneer de Inheemse output van PDF gebruikend een dynamische basislijn wordt geproduceerd, wordt de termijn **PDFProject** getoond als titel van PDF in plaats van de daadwerkelijke kaarttitel. (GIDS-31102)

## Platform

- Als u `scope="external"` gebruikt voor een verwijzing naar DAM-inhoud binnen een onderwerp of kaart, wordt het relatieve pad van het element vervangen door een GUID. (HIDEN-35605)

## Bekend probleem

Adobe heeft het volgende bekende probleem voor de 5.1.0 Service Pack 3-release geïdentificeerd:

- Wanneer u een overzichtstaak zoals volledig van de pagina van taakdetails merkt, wordt de taak voltooid en gesloten; nochtans, blijft zijn status tonen zoals **Bezig** op het dashboard van het Overzicht. (GUIDEN-39375)




