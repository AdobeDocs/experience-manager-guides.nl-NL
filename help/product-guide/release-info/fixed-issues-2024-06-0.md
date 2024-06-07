---
title: Opmerkingen bij de release | Opgeloste problemen in Adobe Experience Manager Guides, release 2024.06.0
description: Meer informatie over de opgeloste problemen vindt u in de 2024.06.0-release van Adobe Experience Manager Guides as a Cloud Service.
source-git-commit: dff625a841ea9fc758de83b1d830ddffa15646cd
workflow-type: tm+mt
source-wordcount: '784'
ht-degree: 0%

---


# Opgeloste problemen in de release 2024.06.0

In dit artikel worden de bugs beschreven die zijn gecorrigeerd in verschillende gebieden van de release 2024.06.0 van Adobe Experience Manager Guides as a Cloud Service.

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, mening [Nieuwe functies in de release van 2024.06.0](whats-new-2024-06-0.md).

Meer informatie over [instructies voor de upgrade van 2024.06.0](upgrade-instructions-2024-06-0.md).

## Authoring

- De kopiëren en deegverrichting van onderwerpen groter dan 15KB ontbreekt met een onverwachte fout. 17171
- De functionaliteit waarmee u de documentstatus wilt wijzigen in het menu  **Bestandseigenschappen** werkt niet correct en verandert in het dialoogvenster *Concept* status. (17088)
- Wanneer u de instellingen van de XML-editor wijzigt met behulp van een aangepast mapprofiel, kunt u `ui_config.json` wordt bijgewerkt met een onjuist bestand. (17011)
- In de **Bewaarplaats** in het **Filter** zoekopdracht behoudt niet de waarde van **Uitgecheckt door** veld bij opnieuw openen van het dialoogvenster **Geavanceerd filter** in. 16935
- Gekoppelde afbeeldingen van de onderwerpen worden niet weergegeven in de basislijn na het maken van de versie. 16931
- Herbruikbare inhoudspanelen maken geen lijst van elementen wanneer **Gebruikersvoorkeuren** zijn ingesteld op het weergeven van bestanden door **Bestandsnaam**. 16896
- Subelementen in het tabeltitelelement kunnen niet worden weergegeven in het dialoogvenster **Voorvertoning** wijze van de Gidsen van de Experience Manager. (16691)
- Uitvoering van postprocess-script mislukt vanwege **FileNotFoundException** uitzondering. 16517
- Vimeo-video&#39;s bieden geen ondersteuning voor schermvullende functies in de hulplijnen voor Experience Managers. (15996)
- Lange vooraf opgemaakte tekstreeksen plakken in `<pre>` of `<codeblock>` elementen leiden tot afgekapte tekst. 15859
- De schrapping van de inhoud komt toe te schrijven aan dubbele GUIDs wanneer de malplaatjes via code worden geïnstalleerd maar onverwerkt blijven. 15858
- De hulplijnen voor Experience Managers houden zich niet aan de **Verwerkingsrol** kenmerk in **Voorvertoning** -modus. 15787
- De Editor verwijdert periodiek extra tekst buiten het geselecteerde gebied.  15708
- Kan grote tabellen niet kopiëren en plakken vanuit Word-documenten of HTML naar de webeditor. (15369)
- De **Kopiëren** functie mislukt voor lege mappen in as a Cloud Service hulplijnen voor Experience Managers. 15353
- Geen API&#39;s of gebeurtenissen om kenmerktoevoeging aan een element of invoeging van een nieuw element vast te leggen. 15351
- Kan niet toevoegen `<data>` tag binnen `<ol>` tag in de webeditor. 15161
- Wanneer Verenigde Shell wordt toegelaten, **Versielabelbeheer** onjuist weergegeven dialoogvenster **Hoofdinhoud** voor versies zonder labels. 15039
- Grote bestanden worden langzaam geladen in de webeditor, met een vertraging van enkele seconden. 14958
- Druk op de knop **Enter** in een tabelcel in de tekst wordt de alinea niet zoals verwacht gesplitst. 14251
- De Experience Manager DITA Guide kan de **Opslaan** na gebruik van de functie voor automatisch inspringen. 16482
- De onderwerpen van het overzicht verschijnen niet in de correcte orde. (16319)
- In de **Auteur** Er treedt een fout met kopiëren en plakken op bij het gebruik van vaste spaties. Dit leidt tot overloop van tekst. 15541

- In `<othermeta>` element binnen `<topicmeta>`, bij het toevoegen van een `<conref>`aan een andere kaart DITA, wordt kaartidentiteitskaart ook toegevoegd samen met identiteitskaart van het element. (15226)
- De `<conref>` kan niet worden bijgewerkt via de **Attributen** wanneer u wijzigingen aanbrengt. (15209)
- Wanneer u een afbeelding binnen een tabelcel selecteert, wordt de gehele cel geselecteerd. (15188)

## Publiceren


- Gekruist koppelen mislukt. Alle bovenliggende kaarten worden niet weergegeven in de context-instellingen voor publicatie voor een koppeling met de `peer @scope`. (16700)
- Wanneer u nieuwe kenmerken toevoegt of bestaande kenmerken verwijdert, blijven de oude kenmerken behouden in het dialoogvenster **Voorinstellingen voorwaarde**. 15890
- De RTL-taalinhoud wordt niet correct verwerkt in de publicatie-uitvoer van Native PDF. 15709
- De eerste PDF wordt niet versioned wanneer een inheemse output van PDF wordt geproduceerd. 10305
- In Eigen PDF, worden de genestelde onderwerpen DITA verkeerd getoond in de Inhoudslijst (TOC). 16742
- Miniaturen die door Dynamic Media voor videobestanden worden gegenereerd, blijven niet aanwezig in de gepubliceerde uitvoer. 15656
- Uitvoergeneratie mislukt voor native PDF-publicatie op een ARM64-processor. (16968)

## Beheer

- Als u een bestaande basislijn bewerkt en een specifieke versie selecteert, treden toepassingsfouten op. (14451)

## Vertaling

- In vertaalprojecten worden geen nieuwe taaltaken toegevoegd aan Adobe Experience Manager 6.5 SP18 met de release van de Experience Manager Guides van oktober 2023. 15398

## Cloud Service

- Navigatie met Adobe Experience Manager Tools reageert niet. (1718)
- De fase van de Transformatie van de bouw binnen de plaatsing van Cloud Servicen ontbreekt met fouten van de DITA codebase. (14432)

## Rapporten

- De onnauwkeurige **Lijst met onderwerpen** tellingen in de Gidsen UI van de Experience Manager toe te schrijven aan unpatched eigenschappen wanneer het kopiëren van activa DITA de rapporten beïnvloedt die voor een kaart DTIA worden geproduceerd. (15529)
- Onderwerpen die externe verwijzingen bevatten met *%20* in de URL-weergave verbroken bestandsverwijzingen. 15347


## Bekende problemen

Adobe heeft de volgende bekende problemen voor de release 2024.06.0 geïdentificeerd:

- Het publiceren van de inheemse PDF ontbreekt wanneer de inhoud van Vimeo aan het onderwerp wordt toegevoegd.
- De **Eigenschappen van onderwerp** niet worden weergegeven volgens de geselecteerde indeling in de metagegevensvelden van een pagina-indeling.
- `xrefs` kan niet worden geklikt in het dialoogvenster **Activa** weergeven wanneer Dynamic Media is ingeschakeld.
