---
title: Opmerkingen bij de release | Adobe Experience Manager Guides 4.6.0 Service Pack 3-release heeft problemen opgelost.
description: Meer informatie over de opgeloste problemen vindt u in de 4.6.0 Service Pack 3-release van Adobe Experience Manager Guides
role: Leader
source-git-commit: d60fea16831af458c479df24c877ef7095b2fd15
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%

---

# Oplossingen voor problemen in de 4.6.0 Service Pack 3-release (januari 2025)


Dit artikel behandelt de fouten die in diverse gebieden van versie 4.6.0 Service Pack 3 van Adobe Experience Manager Guides worden opgelost.

Leer over [ verbeteringsinstructies voor 4.6.0 Service Pack 3 versie ](upgrade-instructions-4-6-0-sp2.md).

## Authoring

- Alle voorwaardengroepen gaan verloren en de voorwaarden worden afgevlakt bij het bijwerken van de voorwaarden van het omslagprofiel. (23526)
- Het veranderen van de waarde van kopbalrijen voor een lijst in het **eigenschappen van de Inhoud** paneel past niet de bijgewerkte waarde toe. (23213)
- Wanneer het toevoegen van nieuwe onderwerpverwijzingen in kaart DITA gebruikend **het elementendialoog van de verwijzing van 0&rbrace; Onderwerp &lbrace;in de lay-outweergave, worden de toegevoegde verwijzingen getoond als gebroken verbinding.** (22859)
- Wanneer het toevoegen van onderwerpen in kaart DITA gebruikend **het elementendialoog van de Verwijzing van 0&rbrace; Onderwerp &lbrace;in de auteursmening, worden de geselecteerde onderwerpen opgenomen in omgekeerde orde van wordt geselecteerd.** (22858)
- Wanneer u een afbeelding uit een extern product kopieert (bijvoorbeeld MS PowerPoint) en deze in hulplijnen plakt, wordt de functionaliteit voor het uploaden van het element direct voor gebruik in het bestand verbroken. 24983
- Wanneer het zoeken van dossiers in de bewaarplaats gebruikend **Onderzoek &amp; filter** functionaliteit, kunnen de veelvoudige dossiers niet worden geselecteerd. 25104

## Publiceren

- Publiceren naar Salesforce mislukt wanneer inhoud vaste spaties bevat. (23664)
- Voor onderwerpen met fouten zoals verbroken koppelingen mislukt het publiceren van de Salesforce en wordt de voortgangsbalk voor onbepaalde tijd weergegeven. (2985)
- Voor kaarten met verbroken koppelingen mislukt het publiceren van de Salesforce en wordt de voortgangsbalk voor onbepaalde tijd weergegeven. 24963
- Als een externe koppeling een UUID bevat, gaat deze na de verwerking en wordt de externe koppeling naar de UUID-koppeling omgezet, waardoor de koppeling in de webeditor en ook op de publicatiesites wordt verbroken. (22574)
- `xref` zet in relatieve verbinding zelfs om wanneer het **werkingsgebied** van verbinding aan **extern** wordt geplaatst. (23059)
- De inheemse generatie van PDF ontbreekt voor inhoud met **brok** attributen die aan **worden geplaatst aan-inhoud**. (21772)
- Het **geeft eigenschappen** dialoog voor een basislijn uit toont niet de eerder bewaarde criteria voor dynamische basislijn. (23964)


## Vertaling

- Voor niet-verouderde vertaling (voor niet-UUID), leidt het bewegen van een onderwerp in de bronweg aan een verschillende omslag tot gebroken verwijzingen in de doelscène. 24152
