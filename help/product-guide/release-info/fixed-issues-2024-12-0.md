---
title: Opmerkingen bij de release | Opgeloste problemen in de release 2024.12.0 van Adobe Experience Manager Guides
description: Meer informatie over de opgeloste problemen vindt u in de release 2024.12.0 van Adobe Experience Manager Guides as a Cloud Service.
source-git-commit: f643a4a22151af2ff14288ab3885c1a6657a80ca
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 0%

---

# Opgeloste problemen in de release 2024.12.0

Dit artikel heeft betrekking op de fouten die zijn opgelost in verschillende gebieden van de release 2024.12.0 van Adobe Experience Manager Guides as a Cloud Service.

Leer over [ verbeteringsinstructies voor de versie 2024.12.0 ](./upgrade-instructions-2024-12-0.md).

## Authoring

- Het maken van een DITA-kaart op een UUID-instantie mislukt wanneer `xmleditor.uniquefilenames` is ingeschakeld in `XMLEditorConfig` . (21201)
- Wanneer het sluiten van een dossier, worden de commentaren en de etiketten die in **worden toegevoegd sparen Veranderingen en ontgrendelen van het Dossier** dialoogdoos niet bewaard in de Geschiedenis van de Versie met de nieuwe versie. Dit is specifiek voor een gebruiksgeval waar **om Controle-binnen op Sluiten** vraagt of **vraagt om Nieuwe Versie op Sluiten** binnen `XMLEditorConfig` wordt toegelaten. (2006)
- De staat van het document duidelijk zoals **Gedaan** keert terug naar **Ontwerp** alvorens een nieuwe versie op te slaan, resulterend in de **Gedaan** staat die niet in om het even welke documentversies voortduurt. (2006)
- Unable to add a PDF file as an image reference in a topic in the Web Editor. (21206)
- Het selecteren van een DITA- dossier in Assets UI toont **Open in FrameMaker** optie, zelfs wanneer onbruikbaar gemaakt in de configuratie. (2008)

## Publiceren

- In de uitvoer Native PDF ontbreken hoofdstuktitels in de inhoudsopgave. Dit leidt tot een onjuiste hiërarchie. 21840


## Beheer

- De lekken van het middel komen toe te schrijven aan **Unclosed ResourceResolver** fouten in logboeken. (18488)
- Wanneer u een nieuwe of gedupliceerde basislijn maakt, worden labels in willekeurige volgorde weergegeven. (19307)


## Basislijn

- Het uitgeven en dan het opslaan van een basislijn op een chronologie van de wolkenopstelling na 1 minuut als de basislijn groot aantal onderwerpen of kaarten heeft. (1958)

## Vertaling

- De vertaling van de kaart gebruikend basislijn wordt langzaam en uiteindelijk ontbreekt om de lijst van alle bijbehorende onderwerpen en kaartdossiers te laden. (1973)
