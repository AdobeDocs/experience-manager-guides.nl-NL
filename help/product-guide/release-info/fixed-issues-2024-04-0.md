---
title: Opmerkingen bij de release | Opgeloste problemen in Adobe Experience Manager Guides, release 2024.4.0
description: Meer informatie over de opgeloste problemen vindt u in de release 2024.04.0 van Adobe Experience Manager Guides as a Cloud Service.
exl-id: 35351d71-7739-4ad3-a063-67adf64906bf
source-git-commit: 5d99274da8fdacbd255d426fa4913b5773ca45f8
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---

# Opgeloste problemen in de release 2024.04.0

Dit artikel heeft betrekking op de fouten die zijn opgelost in verschillende gebieden van de release 2024.04.0 van Adobe Experience Manager Guides as a Cloud Service.

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, mening [ wat in de versie 2024.04.0 ](whats-new-2024-04-0.md) nieuw is.

Leer over [ verbeteringsinstructies voor de versie 2024.04.0 ](upgrade-instructions-2024-04-0.md).

## Authoring

- De **functie van het Exemplaar** ontbreekt om de lege omslagen in Adobe Experience Manager as a Cloud Service te dupliceren. 15353
- De webeditor kan geen .pptx-bestanden uploaden. 14837
- Terwijl het vinden van een tekst in de Redacteur van het Web, keert de curseur aan het eerste voorkomen van de gezochte tekst terug, bij het drukken van de Enter sleutel. 14820
- AutoSave veroorzaakt veelvoudige kwesties, het verplaatst de curseur, en vereist handkliks in het document. 14253
- De onderzoeksresultaten worden onbruikbaar gemaakt na het openen van een dossier dat door globale **wordt gevonden vindt en vervangt**. 12142
- In de bronweergave wordt `</conbody>` soms op onjuiste locaties ingevoegd. 11305
- In de XML-editor kan de knopinfo-functie het Source-veld niet bijwerken. 15847
- De **eigenschap van de Verbinding van UUID van het Aandeel** werkt niet voor de beelden in Adobe Experience Manager. (15598)
- Overlappende tekstproblemen doen zich voor in `<reltable>` - en `<fig>` -tags. 15238
- De het flikkeren kwesties komen in het **paneel van Attributen** voor. 15237
- Wanneer u een teken of woord uit de inhoud verwijdert, springt de cursor tussen de blokelementen. (15224)
- Het **paneel van Attributen** wordt niet getoond in de mening van Source van de Redacteur van het Web. 14387
- Ongewenste, vaste spaties worden toegevoegd tijdens het bewerken aan het einde van een tag in de webeditor. (11786)
- Inhoud wordt verwijderd tijdens het corrigeren van spelfouten in DITA-bestanden. (11610)


## Publiceren

- AEM de productie van de output van de Plaats ontbreekt wanneer de **Schrapping Orphan optie van de Plaats** wordt toegelaten. 15896
- De bewerkingsfunctionaliteit werkt niet wanneer u bestanden toevoegt aan de Kaartverzameling. 15813
- In de JSON-uitvoer worden metagegevens van de DITA-kaart of -onderwerpen niet doorgegeven aan de JSON-uitvoerbestanden. 15713
- Publiceren van eigen PDF mislukt tijdens het wijzigen van de naam van de voorinstelling. (15662)
- Het **sourcePath** bezit is onjuist op de gepubliceerde AEM plaatsuitvoer. 15502
- De taalvariabelen selecteren en aanpassen werken niet goed in de voorinstelling Eigen PDF-uitvoer. (15399)
- Native PDF genereren mislukt bij gebruik van een sjabloon met een grote stijlpagina of lay-out. (15344)
- Inhoud wordt niet correct weergegeven in de gepubliceerde uitvoer als `<conref>` wordt gebruikt met een absoluut pad.
- Een verkorting van de URL van AEM Sites werkt niet vanwege conflicten tussen `fmdita rewriter` en `ResourceResolver` . 14793
- De **verwerking-rol=&quot;middel-slechts&quot;**, **search= &quot;geen&quot;**, en **chunk= &quot;aan-inhoud&quot;** attributen verschijnen ongelijk in de output van AEM Sites. (1442)
- Als een map met 2k-maps wordt ingesteld in het mappad binnen een mapprofiel, mislukken de wijzigingen die op de uitvoervoorinstelling zijn toegepast.14852

## Beheer

- De niet gesloten **Resolvers van het Middel** veroorzaken stijgende zittingstelling en de fouten PathNotFoundException na de versie van Oktober 2023 van Experience Manager Guides as a Cloud Service. 15604
- De eigenschapvlag **fmdita.useApproval** werkt niet zoals verwacht. 15310
- Het maken van een basislijn met de Java API werkt niet met de release van Experience Manager Guides as a Cloud Service in juni 2023. 14787
- De API van `/bin/fmdita/import` blijft permanent vastzitten in een aanvraag die in behandeling is wanneer de uploadmiddelen meer dan 500 MB bedragen. 14743

## Controleren

- Als revisieknooppunten worden verwijderd, kan het bestand niet meer worden geopend en kunnen opmerkingen niet meer worden weergegeven in Adobe Experience Manager Guides. (15366)
- In de webeditor wordt het deelvenster Revisie langzaam geladen. 14680

## Vertaling

- **keur Vertaling** niet goed om de vertaling van tijdelijke dossiers te voltooien. (14665)
