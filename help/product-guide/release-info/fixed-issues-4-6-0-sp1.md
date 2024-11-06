---
title: Opmerkingen bij de release | Adobe Experience Manager Guides 4.6.0 Service Pack 1-release heeft problemen opgelost.
description: Meer informatie over de opgeloste problemen vindt u in de 4.6.0 Service Pack 1-release van Adobe Experience Manager Guides
role: Leader
source-git-commit: 2362870e0e3e6c08df03e8c547bb77de7faa0a02
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---


# Oplossingen voor problemen in de 4.6.0 Service Pack 1-release (oktober 2024)


Dit artikel behandelt de fouten die in diverse gebieden van versie 4.6.0 Service Pack 1 van Adobe Experience Manager Guides worden opgelost.

Leer over [ verbeteringsinstructies voor 4.6.0 Service Pack 1 versie ](upgrade-instructions-4-6-0-sp1.md).

## Authoring

- Het maken van een DITA-kaart op een UUID-instantie mislukt wanneer `xmleditor.uniquefilenames` is ingeschakeld in `XMLEditorConfig` . (21201)
- Wanneer het sluiten van een dossier, worden de commentaren en de etiketten die in **worden toegevoegd sparen Veranderingen en ontgrendelen van het Dossier** dialoogdoos niet bewaard in de Geschiedenis van de Versie met de nieuwe versie. Dit is specifiek voor een gebruiksgeval waar **om Controle-binnen op Sluiten** vraagt of **vraagt om Nieuwe Versie op Sluiten** binnen `XMLEditorConfig` wordt toegelaten. (2006)
- De staat van het Document die als **wordt gemerkt Gedaan** keert aan **Ontwerp** terug alvorens een nieuwe versie op te slaan, resulterend in de **Gedaan** staat die niet in enige documentversies voortduurt. (2006)
- Unable to add a PDF file as an image reference in a topic in the Web Editor. (21206)
- Het selecteren van een DITA- dossier in Assets UI toont **Open in FrameMaker** optie, zelfs wanneer onbruikbaar gemaakt in de configuratie. (2008)


## Publiceren

- Het uploaden van bijlagen naar Salesforce mislukt als het bijlagepad de toegestane lengte overschrijdt. (19420)
- Wanneer u een onderwerp naar Salesforce publiceert, kunnen de koppelingen naar het PDF-bestand niet worden opgelost. (19304)
- De fout `DUPLICATE_VALUE` treedt soms op wanneer u probeert een bestaand artikel opnieuw te publiceren in Salesforce. 17932
- In de uitvoer Native PDF ontbreken hoofdstuktitels in de inhoudsopgave. Dit leidt tot een onjuiste hiërarchie. 21840
- Bij het publiceren van AEM Sites zijn slechts een beperkt aantal kenmerken beschikbaar voor opname in de inhoudsopgave. 7483

## Beheer

- De lekken van het middel komen toe te schrijven aan Unclosed **fouten ResourceResolver in logboeken.** (18488)
- Wanneer u een nieuwe of gedupliceerde basislijn maakt, worden labels in willekeurige volgorde weergegeven. (19307)









