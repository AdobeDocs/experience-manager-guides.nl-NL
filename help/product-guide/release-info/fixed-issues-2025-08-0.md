---
title: Opmerkingen bij de release | Opgeloste problemen in Adobe Experience Manager Guides, release 2025.08.0
description: Meer informatie over de opgeloste problemen vindt u in de release 2025.08.0 van Adobe Experience Manager Guides as a Cloud Service.
source-git-commit: 5abe5c153d8cedc7b555d6ca82709557cc38d28f
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 0%

---

# Opgeloste problemen in de release 2025.08.0

Dit artikel heeft betrekking op de fouten die zijn opgelost in verschillende gebieden van de release 2025.08.0 van Adobe Experience Manager Guides as a Cloud Service.

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, mening [&#x200B; wat in de versie 2025.08.0 &#x200B;](whats-new-2025-08-0.md) nieuw is.

Leer over [&#x200B; verbeteringsinstructies voor de versie 2025.08.0 &#x200B;](upgrade-instructions-2025-08-0.md).

## Authoring

- **CSS** en **de lay-out van de Pagina** dossiers in de Inheemse malplaatjes van PDF tonen inconsequent gedrag van het dossiersluiten, toestaand geeft zelfs wanneer de dossiers worden gesloten uit. (GUIDEN-26688)
- Als u de pagina vernieuwt nadat u aangepaste knoppen aan het linkerdeelvenster hebt toegevoegd, worden dubbele tabbladen gemaakt. (GUIDEN-30899)
- Wanneer XML-inhoud met hoekhaken (zoals &lt;/ of />) wordt toegevoegd binnen een `code block` -element in een onderwerp, wordt het codeblokelelement leeg weergegeven in de uiteindelijke uitvoer. (GIDS-31007)
- De waarden van algemene variabelen `canCheckIn` en `canCheckOut` worden niet correct ingesteld wanneer een bestand wordt uitgecheckt en ingecheckt op de werkbalk van de Editor.(GUIDES-29890)
- Wanneer het openen van een kaart DITA met verenigde toegelaten shell, de Redacteur met tussenpozen verfrist.(GUIDEN-26919)
- Wanneer een DITA-kaart is geselecteerd in de Kaartweergave, wordt het aantal selecties in eerste instantie onjuist weergegeven omdat de onderliggende knooppunten van de kaart niet zijn geselecteerd. De juiste selectie en opname van alle onderliggende knooppunten wordt alleen weergegeven als u de selectie daarna wijzigt. (HULPLIJNEN-2563)
- De dossiers van de prijsverhoging worden niet teruggewonnen wanneer gezocht in het paneel van de Bewaarplaats gebruikend het **DITA onderwerp** filter. Ook, **vindt en vervangt** werkt niet voor de dossiers van de Prijsverhoging en verwante inhoud. (HULPLIJNEN-27133)
- Onbekwaam om het **drop-down van het Menu** van de toolbar van de Redacteur aan te passen gebruikend het uitbreidingskader. Het resultaat is dat u geen bestaande knoppen kunt weergeven of verbergen of nieuwe knoppen kunt toevoegen in het vervolgkeuzemenu Menu. (HULPLIJNEN-28748)

## Beheer van bedrijfsmiddelen

- Het kopiëren van een map met een groot aantal elementen uit de gebruikersinterface van Assets leidt tot een API-time-out. De verrichting blijft in het achterste eind lopen en voltooit na wat tijd, maar geen succes of mislukkingsbericht, of bericht wordt getoond in UI. (GIDS-30900)
- Kopiëren en plakken in een map in de gebruikersinterface van Assets mislukt als gevolg van naverwerkingsfouten. (GUIDEN-30840)
- Kopiëren en plakken mislukt voor mappen met samengestelde elementen (elementen met subelementen) in de gebruikersinterface van Assets. (28107)
- Mappen met een groot aantal elementen worden niet correct geladen in de opslagplaats. (GIDS-32500)
- Namen van mapknooppunten worden onjuist weergegeven in plaats van maptitels in de Editor. (GUIDEN-32402)
- Er treedt een fout op bij het uploaden van elementen met niet-ondersteunde of verboden tekens in de bestandsnamen. (HIDEN-28845)

## Publiceren

- In de native PDF-uitvoer wordt de lijst met indexen (LOI) weergegeven in een niet-alfabetische volgorde en worden geneste indextermen niet op de juiste wijze gegroepeerd, waardoor het moeilijk wordt om te navigeren in de index. (HIDEN-29090)
- Het **paginamalplaatje van de Kaart** en **de paginamalplaatje van het Onderwerp** dropdown lijst in de vooraf ingestelde pagina van de componentenafbeelding van AEM Sites verschijnt leeg wanneer de bestemmingspad een variabele met een dubbelepunt bevat. (HULPLIJNEN-2819)
- Wanneer een kaart DITA verschillende types van onderwerpverwijzingen zoals Concept, Verwijzing of Taak bevat, en het gebruikend het `chunk=to-content` attribuut wordt samengevoegd om enige paginaoutput op AEM Sites met componentenafbeelding te produceren, wordt de inhoud niet behoorlijk gepubliceerd toe te schrijven aan publicatiefouten. (HULPLIJNEN-2818)

## Basislijn

- Het kopiëren van een kaart DITA van Assets UI kopieert ook zijn in bijlage Basislijn aan de nieuwe kaart. (GUIDEN-11227)

## Homepage

- De homepage gaat leeg wanneer één van de dossiers die in **worden vermeld Recente dossiers** widget gebaseerd is op een malplaatje de waarvan bronmalplaatje geen duimnagel omvat. (GIDS-31506)

## Bekende problemen

Adobe heeft de volgende bekende problemen vastgesteld voor de release 2025.08.0:

- Wanneer een dossier dat in Redacteur wordt geopend anders wordt genoemd of bewogen, verandert het schakelen tussen de wijzen (zoals **Auteur**, **Voorproef**, en meer) de inhoud op het het uitgeven gebied maar benadrukt visueel niet de actieve wijze bij de bodem-juiste hoek. (HULPLIJNEN-32719) <br> **Oplossing**: Vernieuw de pagina om de kwestie op te lossen.
- Afbeeldingen met spaties in bestandsnamen worden niet in de uitvoer weergegeven wanneer ze worden gemarkeerd met voorwaardelijke kenmerken. (GUIDEN-33858)
- In het **Eigenschappen van de Inhoud** paneel, sluit het gebied van Attributen automatisch wanneer u probeert om een verwijzing van de **verbinding van de Update** dialoog bij te werken, verhinderend de verbinding wordt bijgewerkt. (GUIDEN-17767)



