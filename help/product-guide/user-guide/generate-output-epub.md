---
title: EPUB-voorinstelling
description: Leer hoe u een EPUB-voorinstelling maakt via het kaartdashboard. EPub-uitvoervoorinstelling configureren in Experience Manager Guides.
exl-id: b6fb5483-064e-4552-84c7-b6723b79d8c5
feature: Publishing
role: User
source-git-commit: a953de289530457b257259bda3d9af2b68790592
workflow-type: tm+mt
source-wordcount: '896'
ht-degree: 0%

---

# EPUB {#id205BED020YT}

U kunt de EPUB-voorinstelling maken via het kaartdashboard.

>[!NOTE]
>
> U kunt de methode kiezen om EPUB te genereren met de DITA-OT of FMPS \(als uw systeembeheerder deze heeft geconfigureerd).

Voer de volgende stappen uit om de EPUB-voorinstelling te maken via het kaartdashboard:

1. In Assets UI, navigeer aan en selecteer de kaart DITA om het in kaartdashboard te openen.
1. Zorg ervoor dat de **Output vooraf instelt** tabel wordt geselecteerd.
1. Selecteer **creeer** in de toolbar.

   Er wordt een nieuw, vooraf ingesteld formulier voor het maken van uitvoerbestanden weergegeven.

1. Voer de vereiste configuratiegegevens voor de EPUB-voorinstelling in.
1. Selecteer **Gedaan** om de vooraf ingestelde montages te bewaren.

De volgende configuratieopties zijn beschikbaar voor de EPUB-voorinstelling:

| EPUB-opties | Beschrijving |
| --- | --- |
| Uitvoertype | Het type uitvoer dat u wilt genereren. Als u EPUB-uitvoer wilt genereren, kiest u de optie EPUB. |
| Naam instellen | Geef een beschrijvende naam voor de EPUB-uitvoerinstellingen die u maakt. Bijvoorbeeld, kunt u _Interne klantenoutput_ of _eind-gebruikers output_ specificeren. |
| Argumenten DITA-OT-opdrachtregel | Geef de aanvullende argumenten op die u tijdens het genereren van uitvoer wilt laten verwerken door DITA-OT. Voor details over de bevel-lijn argumenten die in DITA-OT worden gesteund, mening [ DITA-OT documentatie ](https://www.dita-ot.org/). |
| EPub genereren met | Selecteer DITA-OT om de EPUB-uitvoer te genereren. |
| Voorwaarden toepassen met | Selecteer één van de volgende opties:<br><br>* **toegepaste niets**: Selecteer deze optie als u geen voorwaarde op de gepubliceerde output wilt toepassen.<br>* **DITAVAL dossier**: Selecteer DITAVAL dossier(s) om gepersonaliseerde inhoud te produceren. U kunt meerdere DITAVAL-bestanden selecteren via het dialoogvenster Bladeren of door een bestandspad te typen. Gebruik het kruispictogram bij de bestandsnaam om het te verwijderen. DITAVAL-bestanden worden in de opgegeven volgorde geëvalueerd, zodat de voorwaarden die in het eerste bestand zijn opgegeven voorrang hebben op de voorwaarden die in latere bestanden worden vermeld. U kunt de bestandsvolgorde behouden door bestanden toe te voegen of te verwijderen. Als het DITAVAL-bestand naar een andere locatie wordt verplaatst of wordt verwijderd, wordt het niet automatisch verwijderd van het kaartdashboard. U moet de locatie bijwerken als bestanden worden verplaatst of verwijderd. U kunt de muisaanwijzer boven de bestandsnaam plaatsen om het pad weer te geven in de AEM-opslagplaats waar het bestand is opgeslagen. U kunt alleen DITAVAL-bestanden selecteren en er wordt een fout weergegeven als u een ander bestandstype hebt geselecteerd. FrameMaker Publishing Server ondersteunt geen meerdere DITAVAL-bestanden.<br>* **Vooraf ingestelde Voorwaarde**: Selecteer een voorwaarde vooraf ingesteld van drop-down om een voorwaarde toe te passen terwijl het publiceren van de output. De optie is zichtbaar als u een voorwaarde hebt toegevoegd op het tabblad Voorinstellingen voorwaarde van de DITA-kaartconsole. Meer over voorwaarde vooraf ingesteld, mening [ vooraf instelt van het Gebruik van de voorwaarde ](generate-output-use-condition-presets.md#id1825FL004PN). |
| Doelpad | Het pad in uw AEM-opslagplaats waar de EPUB-uitvoer wordt opgeslagen. Het uitvoerpad wordt ingesteld via de variabele `${base_output_path}` , die wordt geconfigureerd door de beheerder. Om de weg van de Output te vormen, vormt de mening [ de Plaats van de Output van de Basis voor de diensten van de Wolk ](../native-pdf/configure-base-location-cs.md) of [ vormt de Plaats van de Output van de Basis voor de diensten On-Prem ](../native-pdf/configure-base-output-location.md) die op de diensten worden gebaseerd u gebruikt. |
| Bestandsnaam | Geef de bestandsnaam op waarmee u de EPUB-uitvoer wilt opslaan.<br><br>**Nota**: Als u geen dossier verstrekt - noem, dan wordt de titel van de kaart DITA gebruikt om de definitieve naam van het de outputdossier van EPUB te produceren. Als de kaart geen titel heeft, wordt de bestandsnaam van de DITA-kaart gebruikt om de uiteindelijke EPUB-uitvoer een naam te geven. De bestandsnaam wordt ontsmet volgens de regels die in het systeem zijn geconfigureerd voor het verwerken van elk ongeldig teken. |
| Transformatienaam | Geef het type uitvoer op dat u wilt genereren. Dit is vereist als u uitvoer wilt genereren met uw eigen aangepaste plug-in, die is geïntegreerd in de DITA-OT-plug-in. Als u bijvoorbeeld XHTML-uitvoer wilt genereren, geeft u `xhtml` op. Voor een lijst van transformaties beschikbaar in DITA-OT, mening [ DITA-OT transformaties (outputformaten) ](http://www.dita-ot.org/2.3/user-guide/AvailableTransforms.md) in de Gids van de Gebruiker van OASIS DITA-OT. |
| Tijdelijke DITA-OT-bestanden opschonen | Selecteer deze optie als u de tijdelijke bestanden die door DITA-OT worden gegenereerd, wilt opschonen. De plaats waar DITA-OT tijdelijke dossiers opslaat kan in het logboek van de outputgeneratie worden gevonden.<br><br> als u fouten terwijl het produceren van output door DITA-OT ervaart, kunt u deze optie schrappen om de tijdelijke dossiers te behouden. Vervolgens kunt u deze bestanden gebruiken om fouten met uitvoergeneratie op te lossen. |
| Workflow na generatie uitvoeren | Als u deze optie kiest, wordt een nieuwe vervolgkeuzelijst Werkstroom na generatie weergegeven met alle werkstromen die in AEM zijn geconfigureerd. U moet een werkstroom selecteren die u wilt uitvoeren nadat de werkstroom van de outputgeneratie is voltooid.<br><br>**Nota**: Voor meer informatie over het creëren van een douane post-output het werkschema van de productiegeneratie, mening _aanpassen post-output werkschema_ in installeer en vorm Adobe Experience Manager Guides as a Cloud Service. |
| Basislijn gebruiken | Als u een basislijn voor de geselecteerde kaart hebt gecreeerd DITA, selecteer deze optie om de versie te specificeren die u wilt publiceren.<br><br> het Werk van de Mening [ met Basislijn ](generate-output-use-baseline-for-publishing.md#id1825FI0J0PF) voor meer detail. |
| Eigenschappen | Selecteer de eigenschappen die u als metagegevens wilt verwerken. Deze eigenschappen worden ingesteld op de pagina Eigenschappen van de DITA-kaart of het bladwijzerbestand. De eigenschappen die u in de vervolgkeuzelijst selecteert, worden onder het veld Eigenschappen weergegeven en uit de vervolgkeuzelijst verwijderd. Zodra reeks, worden deze eigenschappen ook gekopieerd in de onderwerpen binnen de kaart.<br><br>**Nota**: U kunt de meta-gegevens tot de output ook overgaan gebruikend DITA-OT het publiceren. Voor meer detailmening, [ pas op de meta-gegevens aan de output over gebruikend DITA-OT ](pass-metadata-dita-ot.md#id21BJ00QD0XA). |

**Bovenliggend onderwerp:**&#x200B;[ Begrijpend de output stelt ](generate-output-understand-presets.md) vooraf in
