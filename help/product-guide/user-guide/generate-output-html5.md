---
title: HTML5 gebruiken
description: Leer hoe u een HTML5-voorinstelling maakt via de kaartconsole en het kaartdashboard. Configureer de HTML5-uitvoervoorinstelling in AEM Guides.
exl-id: b54bf3a0-7a13-41a0-ae72-cdf2caf8d974
feature: Publishing
role: User
source-git-commit: e1d6123991ddd8d25f76ee03befeb95f020a9834
workflow-type: tm+mt
source-wordcount: '1509'
ht-degree: 0%

---

# HTML5 {#id205BE700XO1}

U kunt de HTML5-uitvoervoorinstelling maken om uitvoer te publiceren met DITA-OT en FMPS (indien geconfigureerd door uw beheerder).

U kunt de HTML5-voorinstelling op twee manieren maken:

- [HTML5-uitvoervoorinstelling maken via de kaartconsole](#create-html5-output-preset-from-the-map-console)
- [HTML5-uitvoervoorinstelling maken via het kaartdashboard](#create-html5-output-preset-from-the-map-dashboard)

## HTML5-uitvoervoorinstelling maken via de kaartconsole

Voer de volgende stappen uit om de HTML5-voorinstelling te maken vanaf de kaartconsole:

1. [ open een DITA kaartdossier in de console van de Kaart ](./open-files-map-console.md).

   U kunt tot het kaartdossier van de **Recente dossiers** widget in de [ sectie van het Overzicht ](./intro-home-page.md#overview) ook toegang hebben. Het geselecteerde kaartbestand wordt geopend in de kaartconsole.
1. In **vooraf instelt van de Output** lusje, selecteer + pictogram om tot een output vooraf ingesteld te leiden.
1. Selecteer **HTML5** van het drop-down Type in **Nieuwe vooraf ingestelde output** dialoogdoos.
1. Op het **gebied van de Naam**, verstrek een naam aan dit vooraf ingesteld.
1. Op **produceer HTML Gebruikend** gebied, uitgezochte DITA-OT.
1. Selecteer **toevoegen aan huidige omslagprofiel** optie om een output tot stand te brengen die binnen het huidige omslagprofiel vooraf in wordt gesteld. Het ![ pictogram van het omslagprofiel ](images/global-preset-icon.svg) wijst op een omslag-profiel-niveau vooraf ingesteld.

   Leer meer over [ beheer Globale en de profieloutput van de Omslag vooraf instelt ](./web-editor-manage-output-presets.md).

1. Selecteer **toevoegen**.

   De voorinstelling voor HTML5 wordt gemaakt.

   ![](images/html5-preset-dialog-new.png){width="300" align="left"}

In de console van de Kaart, worden de vooraf ingestelde configuratieopties georganiseerd onder de **Algemene** en **Geavanceerde** lusjes.

Het **Algemene** lusje bevat de volgende configuratieopties:

- Uitvoerpad
- DITA-OT opdrachtregelargumenten
- Bestandsnaam
- Voorwaardelijk filteren \(als de voorwaarden voor een kaart zijn gedefinieerd\)
- Basislijn gebruiken \(als een basislijn is gemaakt voor een kaart\)
- Workflow na generatie

**Geavanceerd**

Het tabblad Geavanceerd bevat de volgende configuratieopties:

- Transformatienaam
- Tijdelijke bestanden behouden
- Bestandshiërarchie afvlakken
- Bestandseigenschappen

Voor details op vooraf ingestelde configuratieopties, verwijs naar [ HTML5 vooraf ingestelde configuratie ](#html5-preset-configuration) sectie.

## HTML5-uitvoervoorinstelling maken via het kaartdashboard

Voer de volgende stappen uit om de HTML5-voorinstelling te maken vanaf het dashboard Kaart:

1. In Assets UI, navigeer aan en selecteer de kaart DITA om het in het dashboard van de Kaart te openen.
1. Zorg ervoor dat de **Output vooraf instelt** tabel wordt geselecteerd.
1. Selecteer **creeer** in de toolbar.

   Er wordt een nieuw, vooraf ingesteld formulier voor het maken van uitvoerbestanden weergegeven.

1. Voer de vereiste configuratiegegevens in voor de HTML5-voorinstelling.
1. Selecteer **Gedaan** om de vooraf ingestelde montages te bewaren.

Voor details op vooraf ingestelde configuratieopties, verwijs naar [ HTML5 vooraf ingestelde configuratie ](#html5-preset-configuration) sectie.

## Configuratie van HTML5-voorinstellingen

De configuratieopties variëren enigszins, afhankelijk van of u de voorinstelling configureert via de kaartconsole of het kaartdashboard. Sommige opties zijn alleen van toepassing op het dashboard Kaart, andere op beide.

Wanneer dezelfde configuratie twee verschillende veldlabels heeft, scheidt a **/** deze in de onderstaande tabel. Het eerste vertegenwoordigt het label in de kaartconsole en het tweede vertegenwoordigt het label in het kaartdashboard.

Bijvoorbeeld, **weg van de Output/Bestemming** - hier, **weg van de Output** is het etiket dat in de console van de Kaart wordt gebruikt, terwijl **Weg van de Bestemming** het etiket is dat in het dashboard van de Kaart voor de zelfde configuratie wordt gebruikt.

| HTML5-opties | Beschrijving |
| --- | --- |
| Het Type van output (*Toepasselijk voor het dashboard van de Kaart slechts*) | Het type uitvoer dat u wilt genereren. Kies de optie HTML5 om HTML5-uitvoer te genereren. |
| Plaatsende Naam (*Toepasselijk voor het dashboard van de Kaart slechts*) | Geef een beschrijvende naam voor de HTML5-uitvoerinstellingen die u maakt. Bijvoorbeeld, kunt u _Interne klantenoutput_ of _eind-gebruikers output_ specificeren. |
| Produceer het Responsieve Gebruiken (*Toepasselijk voor het dashboard van de Kaart slechts*) | Selecteer **DITA-OT** om de output te produceren HTML5. Selecteer **FrameMaker Publishing Server** als uw beheerder deze optie heeft gevormd. Sommige configuratieopties variëren wanneer FMPS wordt geselecteerd. |
| Uitvoerpad/bestemmingspad | Het pad in uw AEM-opslagplaats waar de HTML5-uitvoer wordt opgeslagen. |
| DITA-OT opdrachtregelargumenten | Geef de aanvullende argumenten op die u tijdens het genereren van uitvoer wilt laten verwerken door DITA-OT. <br><br> OPMERKING: vanaf de release 2502 van Experience Manager Guides wordt de parameter `generate.copy.outer` niet meer intern beheerd. Deze verandering betekent dat als uw inhoud HTML5 buiten de kaartfolder verblijft, u de parameter `-Dgenerate.copy.outer=3` in het **moet uitdrukkelijk plaatsen DITA-OT gebied van de Regelargumenten van het Bevel**. Zo weet u zeker dat de inhoud correct wordt verwerkt en in de uitvoer wordt opgenomen. Voor meer details bij de behandeling van inhoud buiten de kaartfolder, mening [ DITA-OT documentatie ](https://www.dita-ot.org/dev/parameters/generate-copy-outer#:~:text=The%20generate.,located%20outside%20the%20map%20directory/). |
| Bestandsnaam | Geef de bestandsnaam op waarmee u de HTML5-uitvoer wilt opslaan.<br><br>**Nota**: Als u geen dossier verstrekt - noem, dan wordt de titel van de kaart DITA gebruikt om de definitieve naam van het HTML5- outputdossier te produceren. Als de kaart geen titel heeft, wordt de bestandsnaam van de DITA-kaart gebruikt om de uiteindelijke HTML5-uitvoer een naam te geven. De bestandsnaam wordt ontsmet volgens de regels die in het systeem zijn geconfigureerd voor het verwerken van elk ongeldig teken. |
| Filteren en/of voorwaarden toepassen met behulp van conditionering | Selecteer één van de volgende opties:<br><br>* **toegepaste niets**: Selecteer deze optie als u geen voorwaarde op de gepubliceerde output wilt toepassen.<br>* **DITAVal dossier**: Selecteer DITAVal dossier(s) om gepersonaliseerde inhoud te produceren. U kunt meerdere DITAVal-bestanden selecteren via het dialoogvenster Bladeren of door een bestandspad te typen. Gebruik het kruispictogram bij de bestandsnaam om het te verwijderen. DITAVal-bestanden worden in de opgegeven volgorde geëvalueerd, zodat de voorwaarden die in het eerste bestand zijn opgegeven voorrang hebben op de voorwaarden die in latere bestanden worden vermeld. U kunt de bestandsvolgorde behouden door bestanden toe te voegen of te verwijderen. Als het DITAVal-bestand naar een andere locatie wordt verplaatst of wordt verwijderd, wordt het niet automatisch verwijderd van het kaartdashboard. U moet de locatie bijwerken als bestanden worden verplaatst of verwijderd. U kunt de muisaanwijzer boven de bestandsnaam plaatsen om het pad weer te geven in de AEM-opslagplaats waar het bestand is opgeslagen. U kunt alleen DITAVal-bestanden selecteren en er wordt een fout weergegeven als u een ander bestandstype hebt geselecteerd. FrameMaker Publishing Server ondersteunt geen meerdere DITAVAL-bestanden.<br>* **Vooraf ingestelde Voorwaarde**: Selecteer een voorwaarde vooraf ingesteld van drop-down om een voorwaarde toe te passen terwijl het publiceren van de output. De optie is zichtbaar als u een voorwaarde hebt toegevoegd op het tabblad Voorinstellingen voorwaarde van de DITA-kaartconsole. Meer over voorwaarde vooraf ingesteld, mening [ vooraf instelt van het Gebruik van de voorwaarde ](generate-output-use-condition-presets.md#id1825FL004PN).<br><br> u kunt veelvoudige DITAVAL dossiers selecteren gebruikend doorbladerdialoog of door dossierweg te typen. Gebruik het kruispictogram bij de bestandsnaam om het te verwijderen. DITAVAL-bestanden worden in de opgegeven volgorde geëvalueerd, zodat de voorwaarden die in het eerste bestand zijn opgegeven voorrang hebben op de voorwaarden die in latere bestanden worden vermeld. U kunt de bestandsvolgorde behouden door bestanden toe te voegen of te verwijderen. U moet de locatie bijwerken als bestanden worden verplaatst of verwijderd. U kunt de muisaanwijzer boven de bestandsnaam plaatsen om het pad weer te geven in de AEM-opslagplaats waar het bestand is opgeslagen. U kunt alleen DITAVAL-bestanden opslaan. Er wordt een fout weergegeven als u een ander bestand hebt geselecteerd.<br><br>**Nota**: FrameMaker Publishing Server steunt geen veelvoudige DITAVAL dossiers. |
| Workflow na generatie | Als u deze optie kiest, wordt een nieuwe vervolgkeuzelijst Werkstroom na generatie weergegeven met alle werkstromen die in AEM zijn geconfigureerd. U moet een werkstroom selecteren die u wilt uitvoeren nadat de werkstroom van de outputgeneratie is voltooid.<br><br>**Nota**:Voor meer informatie over het creëren van een douane post-output het werkschema van de productiegeneratie, mening _aanpassen post-output werkschema_ in installeer en vorm Adobe Experience Manager Guides as a Cloud Service. |
| Transformatienaam | Geef het type uitvoer op dat u wilt genereren. Dit is vereist als u uitvoer wilt genereren met uw eigen aangepaste plug-in, die is geïntegreerd in de DITA-OT-plug-in. Als u bijvoorbeeld XHTML-uitvoer wilt genereren, geeft u `xhtml` op. Voor een lijst van transformaties beschikbaar in DITA-OT, mening [ DITA-OT transformaties (outputformaten) ](http://www.dita-ot.org/2.3/user-guide/AvailableTransforms.html) in de Gids van de Gebruiker van OASIS DITA-OT. |
| Tijdelijke bestanden behouden | Selecteer deze optie om de tijdelijke bestanden te behouden die door DITA-OT worden gegenereerd. Als er fouten optreden bij het genereren van uitvoer via DITA-OT, selecteert u deze optie om de tijdelijke bestanden te behouden. U kunt die dossiers dan gebruiken om de fouten van de outputgeneratie problemen op te lossen.<br> <br> Na het produceren van de output, selecteer het **tijdelijke dossiers van de Download** ![ pictogram van de download tijdelijke dossiers ](images/download-temp-files-icon.svg) om de omslag te downloaden van het PIT die de tijdelijke dossiers bevat. <br><br> **Nota**: Als de dossiereigenschappen tijdens generatie worden toegevoegd, omvatten de output tijdelijke dossiers ook a *metadata.xml* dossier die die eigenschappen bevatten. |
| Basislijn gebruiken | Als u een basislijn voor de geselecteerde kaart hebt gecreeerd DITA, selecteer deze optie om de versie te specificeren die u wilt publiceren.<br><br> het Werk van de Mening [ met Basislijn ](generate-output-use-baseline-for-publishing.md#id1825FI0J0PF) voor meer detail. |
| Bestandshiërarchie afvlakken | Selecteer de optie om de HTML5-uitvoer te genereren in een platte maphiërarchie. De volledige inhoud wordt gepubliceerd in de HTML5-uitvoerindeling in een platte bestandshiërarchie en wordt in één map opgeslagen. <br> Als u deze optie uitschakelt, wordt de uitvoer gegenereerd in een geneste maphiërarchie en wordt de volledige mapstructuur gerepliceerd. |
| Bestandseigenschappen | Selecteer de eigenschappen die u als metagegevens wilt verwerken. Deze eigenschappen worden ingesteld op de pagina Eigenschappen van de DITA-kaart of het bladwijzerbestand. De eigenschappen u van de dropdown lijst selecteert verschijnen onder het **gebied van de Eigenschappen van het Dossier 0&rbrace; &lbrace;.** Selecteer het kruispictogram naast de eigenschap om deze te verwijderen. <br><br>**Nota**: U kunt de meta-gegevens tot de output ook overgaan gebruikend DITA-OT het publiceren. Voor meer detailmening, [ pas op de meta-gegevens aan de output over gebruikend DITA-OT ](pass-metadata-dita-ot.md#id21BJ00QD0XA). |







**Bovenliggend onderwerp:**&#x200B;[ Begrijpend de output stelt ](generate-output-understand-presets.md) vooraf in
