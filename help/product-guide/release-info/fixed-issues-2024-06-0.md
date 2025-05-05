---
title: Opmerkingen bij de release | Opgeloste problemen in Adobe Experience Manager Guides, release 2024.06.0
description: Meer informatie over de opgeloste problemen vindt u in de release 2024.06.0 van Adobe Experience Manager Guides as a Cloud Service.
exl-id: 608e5b2c-72af-4498-9b63-935e698231d4
source-git-commit: d525775afeeb89754762ff514126b1c3a3307b3f
workflow-type: tm+mt
source-wordcount: '784'
ht-degree: 0%

---

# Opgeloste problemen in de release 2024.06.0

Dit artikel heeft betrekking op de fouten die zijn opgelost in verschillende gebieden van de release 2024.06.0 van Adobe Experience Manager Guides as a Cloud Service.

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, mening [ wat in de versie 2024.06.0 ](whats-new-2024-06-0.md) nieuw is.

Leer over [ verbeteringsinstructies voor de versie 2024.06.0 ](upgrade-instructions-2024-06-0.md).

## Authoring

- De kopiëren en deegverrichting van onderwerpen groter dan 15KB ontbreekt met een onverwachte fout. 17171
- De functionaliteit om de documentstaat van het **paneel van de Eigenschappen van het Dossier te veranderen** werkt niet correct en verandert in de *3&rbrace; staat van het Ontwerp &lbrace;.* (17088)
- Wanneer u de instellingen van de XML-editor wijzigt met behulp van een aangepast mapprofiel, wordt de `ui_config.json` bijgewerkt met een onjuist bestand. (17011)
- In het **paneel van de Bewaarplaats**, behoudt het **3&rbrace; onderzoek van de Filter &lbrace;niet de waarde van** Uitgecheckt door **gebied wanneer het opnieuw openen van het** Geavanceerde de filterdoos **van de filterdialoog.** 16935
- Gekoppelde afbeeldingen van de onderwerpen worden niet weergegeven in de basislijn na het maken van de versie. 16931
- De herbruikbare inhoudspanelen maken geen lijst van elementen wanneer de **voorkeur van de Gebruiker** aan meningsdossiers door **Filename** wordt geplaatst. 16896
- De subelementen binnen het element van de lijsttitel kunnen niet op de **1&rbrace; wijze van de Voorproef &lbrace;van Experience Manager Guides teruggeven.** (16691)
- De uitvoering van postprocess manuscript ontbreekt toe te schrijven aan **FileNotFoundException** uitzondering. 16517
- Vimeo-video&#39;s bieden geen ondersteuning voor schermvullende functies in Experience Manager Guides. (15996)
- Als u lange vooraf opgemaakte tekstreeksen in `<pre>` - of `<codeblock>` -elementen plakt, wordt de tekst afgebroken. 15859
- De schrapping van de inhoud komt toe te schrijven aan dubbele GUIDs wanneer de malplaatjes via code worden geïnstalleerd maar onverwerkt blijven. 15858
- Experience Manager Guides slaagt er niet in om aan het **attribuut van de Rol van de 0&rbrace; Verwerking {in** 3} wijze van de Voorproef te houden. **&#x200B;**&#x200B;15787
- De Editor verwijdert periodiek extra tekst buiten het geselecteerde gebied.  15708
- Kan grote tabellen niet kopiëren en plakken vanuit Word-documenten of HTML naar de webeditor. (15369)
- De **functie van het Exemplaar** ontbreekt voor lege omslagen in Experience Manager Guides as a Cloud Service. 15353
- Geen API&#39;s of gebeurtenissen om kenmerktoevoeging aan een element of invoeging van een nieuw element vast te leggen. 15351
- Kan tag `<data>` niet toevoegen binnen tag `<ol>` in de webeditor. 15161
- Wanneer Verenigde Shell wordt toegelaten, toont de **dialoogdoos van het Beheer van het Etiket van de Versie** verkeerd **Belangrijkste Inhoud** voor versies zonder etiketten. 15039
- Grote bestanden worden langzaam geladen in de webeditor, met een vertraging van enkele seconden. 14958
- Het drukken van **gaat** sleutel in een lijstcel binnen de tekst binnen niet de paragraaf in zoals verwacht. 14251
- De Gids van DITA van de Experience Manager ontbreekt om **te teweegbrengen sparen** functie na het gebruiken van de auto-karteleigenschap. 16482
- De onderwerpen van het overzicht verschijnen niet in de correcte orde. (16319)
- In de **mening van de Auteur**, komt een exemplaar-en-deegkwestie bij het gebruiken van vaste ruimten voor en resulteert in het overstromen van tekst. 15541

- In `<othermeta>` -element binnen `<topicmeta>` wordt bij het toevoegen van a `<conref>` aan een andere DITA-kaart de kaart-id ook toegevoegd samen met de id van het element. (15226)
- `<conref>` kan niet van het **paneel van Attributen** worden bijgewerkt wanneer het aanbrengen van veranderingen. (15209)
- Wanneer u een afbeelding binnen een tabelcel selecteert, wordt de gehele cel geselecteerd. (15188)

## Publiceren


- Gekruist koppelen mislukt om alle bovenliggende maps weer te geven in de context-instellingen voor publicatie voor een koppeling met de `peer @scope` . (16700)
- Bij het toevoegen van om het even welke nieuwe of het verwijderen van om het even welke bestaande attributen, worden de oude attributen behouden in de **Vooraf ingestelde Voorwaarde**. 15890
- De RTL-taalinhoud wordt niet correct verwerkt in de publicatie-uitvoer van Native PDF. 15709
- De eerste PDF wordt niet versioned wanneer een inheemse output van PDF wordt geproduceerd. 10305
- In Eigen PDF, worden de genestelde onderwerpen DITA verkeerd getoond in de Inhoudslijst (TOC). 16742
- Miniaturen die door Dynamic Media voor videobestanden worden gegenereerd, blijven niet aanwezig in de gepubliceerde uitvoer. 15656
- Uitvoergeneratie mislukt voor native PDF-publicatie op een ARM64-processor. (16968)

## Beheer

- Als u een bestaande basislijn bewerkt en een specifieke versie selecteert, treden toepassingsfouten op. (14451)

## Vertaling

- Met de release van Experience Manager Guides van oktober 2023 kunnen vertaalprojecten geen nieuwe taaltaken toevoegen aan Adobe Experience Manager 6.5 SP18. 15398

## Cloud Service

- Navigatie met Adobe Experience Manager Tools reageert niet. (1718)
- De fase van de Transformatie van de bouw binnen de plaatsing van Cloud Servicen ontbreekt met fouten van de DITA codebase. (14432)

## Rapporten

- De onnauwkeurige **tellingen van de Lijst van het Onderwerp** &lbrace;in Experience Manager Guides UI toe te schrijven aan unpatched eigenschappen wanneer het kopiëren van activa DITA de rapporten beïnvloedt die voor een kaart DTIA worden geproduceerd. (15529)
- Onderwerpen met externe verwijzingen met *%20* in de URL tonen verbroken bestandsverwijzingen. 15347


## Bekende problemen

Adobe heeft de volgende bekende problemen voor de release 2024.06.0 geïdentificeerd:

- Het publiceren van de inheemse PDF ontbreekt wanneer de inhoud van Vimeo aan het onderwerp wordt toegevoegd.
- De **eigenschappen van het Onderwerp** worden niet getoond zoals per het geselecteerde formaat op de meta-gegevensgebieden van een paginalay-out.
- `xrefs` zijn niet klikbaar in de **Assets** mening wanneer Dynamic Media wordt toegelaten.
