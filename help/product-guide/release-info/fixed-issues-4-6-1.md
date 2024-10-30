---
title: Opmerkingen bij de release | Opgeloste problemen in de Adobe Experience Manager-handleidingen 4.6.1-versie
description: Meer informatie over de opgeloste problemen in de 4.6.1-versie van Adobe Experience Manager Guides
role: Leader
source-git-commit: 3547eb43977f31dae297ca5cb1f1ab53f7f2b067
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 0%

---


# Opgeloste problemen in versie 4.6.1 (oktober 2024)


In dit artikel worden de bugs beschreven die zijn gecorrigeerd in verschillende gebieden van release 4.6.1 van Adobe Experience Manager Guides.

Leer over [ verbeteringsinstructies voor de versie 4.6.1 ](upgrade-instructions-4-6-1.md).

## Ontwerpen

- Het maken van een DITA-kaart op een UUID-instantie mislukt wanneer `xmleditor.uniquefilenames` is ingeschakeld in `XMLEditorConfig` . (21201)
- Wanneer het sluiten van een dossier, worden de commentaren en de etiketten die in **worden toegevoegd sparen Veranderingen en de de dialoogdoos van het Ontgrendelen van het Dossier** niet bewaard in de Geschiedenis van de Versie met de nieuwe versie. Dit is specifiek voor een gebruiksgeval waar **vraagt om Controle-binnen op Sluiten** of **vraagt om Nieuwe Versie op Sluiten** binnen `XMLEditorConfig` wordt toegelaten. (20065)
- De als **Gemarkeerde Staat van het Document** keert aan **Ontwerp** terug alvorens een nieuwe versie op te slaan, resulterend in de **Gedaane** staat die niet in enige documentversies voortduurt. (2006)
- Kan geen PDF-bestand als afbeeldingsverwijzing toevoegen aan een onderwerp in de webeditor. (21206)
- Het selecteren van een DITA dossier in de Activa UI toont **Open in FrameMaker** optie, zelfs wanneer onbruikbaar gemaakt in de configuratie. (2008)


## Publiceren

- Het uploaden van bijlagen naar Salesforce mislukt als het bijlagepad de toegestane lengte overschrijdt. (19420)
- Bij het publiceren van een onderwerp naar Salesforce kunnen de koppelingen naar het PDF-bestand niet worden opgelost. (19304)
- De fout `DUPLICATE_VALUE` treedt af en toe op wanneer wordt geprobeerd een bestaand artikel opnieuw te publiceren in Salesforce. (17932)
- In de uitvoer van de native PDF ontbreken hoofdstuktitels in de inhoudsopgave. Dit leidt tot een onjuiste hiërarchie. 21840
- Bij het publiceren van AEM Sites is er slechts een beperkt aantal kenmerken beschikbaar voor opname in de inhoudsopgave. 7483

## Management

- De lekken van het middel komen toe te schrijven aan unclosed **fouten ResourceResolver in logboeken.** (18488)
- Wanneer u een nieuwe of gedupliceerde basislijn maakt, worden labels in willekeurige volgorde weergegeven. (19307)









