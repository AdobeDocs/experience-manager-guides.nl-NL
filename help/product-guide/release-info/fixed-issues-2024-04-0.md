---
title: Opmerkingen bij de release | Opgeloste problemen in Adobe Experience Manager Guides, release 2024.4.0
description: Meer informatie over de opgeloste problemen vindt u in de 2024.04.0-release van Adobe Experience Manager Guides as a Cloud Service.
source-git-commit: 4c7421391922d276ef82515fb4b1cbdc2397e4ce
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---


# Opgeloste problemen in de release 2024.04.0

In dit artikel worden de bugs beschreven die zijn gecorrigeerd in verschillende gebieden van de release 2024.04.0 van Adobe Experience Manager Guides as a Cloud Service.

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, mening [Nieuwe functies in de release van 2024.04.0](whats-new-2024-04-0.md).

Meer informatie over [upgradeinstructies voor de release van 2024.04.0](upgrade-instructions-2024-04-0.md).

## Authoring

- De **Kopiëren** kan de lege mappen in Adobe Experience Manager as a Cloud Service niet dupliceren. 15353
- De webeditor kan geen .pptx-bestanden uploaden. 14837
- Terwijl het vinden van een tekst in de Redacteur van het Web, keert de curseur aan het eerste voorkomen van de gezochte tekst terug, bij het drukken van de Enter sleutel. 14820
- AutoSave veroorzaakt veelvoudige kwesties, het verplaatst de curseur, en vereist handkliks in het document. 14253
- De zoekresultaten worden uitgeschakeld nadat een bestand is geopend dat via algemene **Zoeken en vervangen**. 12142
- In de bronweergave `</conbody>` wordt soms op onjuiste locaties ingevoegd. 11305
- In de XML-editor kan het veld Bron niet worden bijgewerkt met de knopinfo-functie. 15847
- De **UUID-koppeling delen** werkt niet voor de afbeeldingen in Adobe Experience Manager. (15598)
- Overlappende tekstproblemen doen zich voor in `<reltable>` en `<fig>` -tags. 15238
- Flickingproblemen doen zich voor in de **Attributen** deelvenster. 15237
- Wanneer u een teken of woord uit de inhoud verwijdert, springt de cursor tussen de blokelementen. (15224)
- De **Attributen** wordt niet weergegeven in de bronweergave van de webeditor. 14387
- Ongewenste, vaste spaties worden toegevoegd tijdens het bewerken aan het einde van een tag in de webeditor. (11786)
- Inhoud wordt verwijderd tijdens het corrigeren van spelfouten in DITA-bestanden. (11610)


## Publiceren

- AEM genereren van Site-uitvoer mislukt als de **Orphan-site verwijderen** is ingeschakeld. 15896
- De bewerkingsfunctionaliteit werkt niet wanneer u bestanden toevoegt aan de Kaartverzameling. 15813
- In de JSON-uitvoer worden metagegevens van de DITA-kaart of -onderwerpen niet doorgegeven aan de JSON-uitvoerbestanden. 15713
- Publiceren van eigen PDF mislukt tijdens het wijzigen van de naam van de voorinstelling. (15662)
- De **sourcePath** De eigenschap is onjuist op de gepubliceerde AEM-site-uitvoer. 15502
- De taalvariabelen selecteren en aanpassen werken niet goed in de voorinstelling Eigen PDF-uitvoer. (15399)
- Native PDF genereren mislukt bij gebruik van een sjabloon met een grote stijlpagina of lay-out. (15344)
- Inhoud wordt niet correct weergegeven in de gepubliceerde uitvoer als `<conref>` wordt gebruikt met een absoluut pad.
- De verkorting van AEM Sites URL werkt niet wegens conflicten tussen `fmdita rewriter` en `ResourceResolver`. 14793
- De **processing-rol=&quot;resource-only&quot;**, **search=&quot;no&quot;**, en **chunk=&quot;to-content&quot;** kenmerken worden in AEM Sites-uitvoer ongelijk weergegeven. (1442)
- Als een map met 2k-maps wordt ingesteld in het mappad binnen een mapprofiel, mislukken de wijzigingen die op de uitvoervoorinstelling zijn toegepast.14852

## Beheer

- Niet gesloten **Resolvers van bronnen** veroorzaken stijgende zittingstelling en PathNotFoundException fouten na de as a Cloud Service versie van de Gidsen van de Experience Manager van oktober 2023. 15604
- De functiemarkering **fmdita.useapproval** werkt niet zoals verwacht. 15310
- Het maken van een basislijn met de Java API werkt niet met de release van juni 2023 van Experience Manager Guides as a Cloud Service. 14787
- De `/bin/fmdita/import` API blijft in aanvraag voor onbepaalde tijd vastzitten wanneer de uploadmiddelen meer dan 500 MB bedragen. 14743

## Controleren

- Als revisieknooppunten worden verwijderd, kan het venster met Adobe Experience Manager-hulplijnen niet meer worden geopend en weergegeven. (15366)
- In de webeditor wordt het deelvenster Revisie langzaam geladen. 14680

## Vertaling

- **Vertaling accepteren** kan de vertaling van tijdelijke bestanden niet voltooien. (14665)


