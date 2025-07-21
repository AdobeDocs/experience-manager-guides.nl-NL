---
title: Opmerkingen bij de release | Opgeloste problemen in Adobe Experience Manager Guides, release 2025.07.0
description: Meer informatie over de opgeloste problemen vindt u in de release 2025.07.0 van Adobe Experience Manager Guides as a Cloud Service.
exl-id: 0744e821-5aee-432b-a6c8-7ed6538935db
source-git-commit: c4d3cdd2a0a98b7c9c937c66c5c3130bf4c5c164
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 0%

---

# Opgeloste problemen in de release 2025.07.0

Dit artikel heeft betrekking op de fouten die zijn opgelost in verschillende gebieden van de release 2025.07.0 van Adobe Experience Manager Guides as a Cloud Service.

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, mening [ wat in de versie 2025.07.0 ](whats-new-2025-07-0.md) nieuw is.

Leer over [ verbeteringsinstructies voor de versie 2025.07.0 ](upgrade-instructions-2025-07-0.md).

## Authoring

- Wanneer een XML-opmerking wordt toegevoegd binnen een element in de Source-weergave, gaan de spaties aan het begin en aan het einde van de opmerking verloren bij het schakelen tussen weergaven. (GUIDEN-29781)
- Multimedia de opties werken niet wanneer huidig binnen het ellipspictogram (**Meer** menu) in de toolbar. (GUIDEN-29583)
- Wanneer u een nieuw onderwerp maakt via de gebruikersinterface van Assets of de Editor, wordt het onderwerp niet automatisch geopend in de Editor als de instelling `xmleditor.uniquefilenames` is ingesteld op true in `XMLEditorConfig` . (HIDEN-28171)
- Spaties die in een MathML-vergelijking in de Source-weergave worden toegevoegd, blijven niet behouden wanneer de Editor-weergave wordt gewijzigd. (HULPLIJNEN-26111)

## Beheer van bedrijfsmiddelen

- Wanneer u een onderwerp opent in de weergave Auteur nadat de browser is vernieuwd, blijven eerder toegepaste tags in het deelvenster Bestandseigenschappen niet behouden en wanneer u nieuwe tags toevoegt, worden de bestaande tags overschreven, met name wanneer een groot aantal tags beschikbaar is voor selectie. (HIDEN-29078)
- Wanneer het produceren van een rapport van Meta-gegevens voor een kaart DITA die een groot aantal activa bevat, leidt **** knoop wordt unresponsief of toont een vertraagde reactie. (HULPLIJNEN-2843)

## Controleren

- Pogingen om overzichtstaken tot stand te brengen door het werkschema van AEM ontbreken constant omdat de overzichtsknoop niet wordt gecreeerd. (HIDEN-28214)

## Publiceren

- Er treedt een fout in de codekwaliteit op bij de implementatie van het AEM Sites-pakket met publicatiecomponenten `guides-components.all-1.3.0.zip` via Cloud Manager. (GUIDEN-28873)
- Als u een DITA-kaart met het kenmerk `chunk=to-content` publiceert, worden dubbele JCR-knooppunten in de nieuwe AEM Sites-uitvoer gemaakt, wat tot een redundante inhoudsstructuur in AEM Sites leidt. (HULPLIJNEN-28104)
- Wanneer het publiceren van een kaart DITA gebruikend de nieuwe output van AEM Sites, als een onderwerp het `chunk =to-content` attribuut heeft en de output wordt geplaatst om onderwerptitels als paginanamen te gebruiken, toont de geproduceerde paginanaam verkeerd het woord **brok** in plaats van het behouden van de originele onderwerpnaam. (HIDEN-28102)
- De eigenschap `cq:template` die is ingesteld in de AEM Guides-onderwerpsjabloon voor nieuwe publicaties in AEM Sites, geeft een onjuiste waarde weer, die de sjabloonstructuur en de rendering van inhoud beïnvloedt. (HULPLIJNEN-27789)


## Platform

- Prestatieproblemen zoals langere laadtijden en intermitterende onderbrekingen worden waargenomen wanneer u werkt met grote verzamelingen. (HIDEN-29065, HULPLIJNEN-28793)
- De kwetsbaarheden die samenhangen met het gebruik van de vervangen Guava-bibliotheek in de AEM Guides-componenten die zijn geüpload op Experience Manager Guides.(HIDEN-27402)

## Bekende problemen

Adobe heeft de volgende bekende problemen vastgesteld voor de release 2025.07.0:

- Wanneer het werken met de onderwerpen van de Prijsverhoging, de de verwijzings **knoop van het a** Onderwerp verschijnt in de toolbar van de Redacteur, maar het werkt niet. (GIDS-31038)
- Namen van mapknooppunten worden onjuist weergegeven in plaats van maptitels in de Editor. (GUIDEN-30909)
- In de **dialoog van de Fusie**, toont de dropdown lijst verkeerd **Belangrijkste inhoud** in plaats van het tonen van de beschikbare versies van het geselecteerde onderwerp. (GUIDEN-30820)
- Wanneer het openen van een kaart DITA met verenigde toegelaten shell, verandert de redacteur af en toe.(GUIDEN-26919)
