---
title: PDF genereren met DITA-OT
description: Leer hoe u een PDF-voorinstelling maakt met DITA-OT vanuit de kaartconsole en het kaartdashboard. PDF-uitvoervoorinstelling configureren in AEM Guides.
feature: Publishing
role: User
exl-id: 6ac82dad-34af-4f9e-8b52-4e4f2eb982a4
source-git-commit: 6e23f52fc9124d0f07f8108da1b5fe574f553469
workflow-type: tm+mt
source-wordcount: '1447'
ht-degree: 0%

---

# DITA-OT PDF-uitvoervoorinstelling maken {#id205BE600HAH}

U kunt de DITA-OT PDF-uitvoervoorinstelling op twee manieren maken:

- [De DITA-OT PDF-voorinstelling maken via de kaartconsole](#create-the-dita-ot-pdf-preset-from-the-map-console)
- [De DITA-OT PDF-voorinstelling maken via het kaartdashboard](#create-the-dita-ot-pdf-preset-from-the-map-dashboard)

## De DITA-OT PDF-voorinstelling maken via de kaartconsole

Voer de volgende stappen uit om de PDF-voorinstelling te maken vanaf de kaartconsole:

1. [ open een DITA kaartdossier in de console van de Kaart ](./open-files-map-console.md).

   U kunt tot het kaartdossier van de **Recente dossiers** widget in de [ sectie van het Overzicht ](./intro-home-page.md#overview) ook toegang hebben. Het geselecteerde kaartbestand wordt geopend in de kaartconsole.
1. In **vooraf instelt van de Output** lusje, selecteer + pictogram om tot een output vooraf ingesteld te leiden.
1. Selecteer **PDF** van het drop-down Type in **Nieuwe output vooraf ingestelde** dialoogdoos.
1. Op het **gebied van de Naam**, verstrek een naam aan dit vooraf ingesteld.
1. Op **produceer PDF Gebruikend** gebied, uitgezochte **DITA-OT**.
1. Selecteer **toevoegen aan huidige omslagprofiel** optie om een output tot stand te brengen die binnen het huidige omslagprofiel vooraf in wordt gesteld. Het ![ pictogram van het omslagprofiel ](images/global-preset-icon.svg) wijst op een omslag-profiel-niveau vooraf ingesteld.

   Leer meer over [ beheer Globale en de profieloutput van de Omslag vooraf instelt ](./web-editor-manage-output-presets.md).

1. Selecteer **toevoegen**.

   De voorinstelling voor PDF wordt gemaakt.

   ![](./images/pdf-preset-map-console.png){width="350" align="left"}

In de console van de Kaart, worden de vooraf ingestelde configuratieopties voor DITA-OT georganiseerd onder de **Algemene** en **Geavanceerde** lusjes in de console van de Kaart.

![](./images/dita-ot-preset-config-new.png){width="350" align="left"}

**Algemeen**

Het **Algemene** lusje bevat de volgende configuratieopties:

- Uitvoerpad
- DITA-OT opdrachtregelargumenten
- PDF-bestandsnaam
- Voorwaardelijk filteren \(als de voorwaarden voor een kaart zijn gedefinieerd\)
- Basislijn gebruiken \(als een basislijn is gemaakt voor een kaart\)
- Workflow na generatie

**Geavanceerd**

Het **Geavanceerde** lusje bevat de volgende configuratieopties:

- Versie inschakelen
- Tijdelijke bestanden behouden
- Bestandseigenschappen

Voor details op vooraf ingestelde configuratieopties, verwijs naar de [ vooraf ingestelde de configuratiesectie van PDF ](#pdf-preset-configuration).


## De DITA-OT PDF-voorinstelling maken via het kaartdashboard

Voer de volgende stappen uit om de PDF-voorinstelling te maken via het kaartdashboard:

1. In Assets UI, navigeer aan en selecteer de kaart DITA om het in kaartdashboard te openen.
1. Zorg ervoor dat de **Output vooraf instelt** tabel wordt geselecteerd.
1. Selecteer **creeer** in de toolbar.

   Er wordt een nieuw, vooraf ingesteld formulier voor het maken van uitvoerbestanden weergegeven.

1. Voer de vereiste configuratiegegevens voor de PDF-voorinstelling in.
1. Selecteer **Gedaan** om de vooraf ingestelde montages te bewaren.

## Configuratie PDF-voorinstelling

De configuratieopties variëren enigszins, afhankelijk van of u de voorinstelling configureert via de kaartconsole of het kaartdashboard. Sommige opties zijn alleen van toepassing op het dashboard Kaart, andere op beide.

Wanneer dezelfde configuratie twee verschillende veldlabels heeft, scheidt a **/** deze in de onderstaande tabel. Het eerste vertegenwoordigt het label in de kaartconsole en het tweede vertegenwoordigt het label in het kaartdashboard.

Bijvoorbeeld, **weg van de Output/Bestemming** - hier, **weg van de Output** is het etiket dat in de console van de Kaart wordt gebruikt, terwijl **Weg van de Bestemming** het etiket is dat in het dashboard van de Kaart voor de zelfde configuratie wordt gebruikt.

| PDF-opties | Beschrijving |
| --- | --- |
| Het Type van output (*Toepasselijk voor het dashboard van de Kaart slechts*) | Het type uitvoer dat u wilt genereren. Als u PDF-uitvoer wilt genereren, kiest u de optie PDF. |
| Plaatsende Naam (*Toepasselijk voor het dashboard van de Kaart slechts*) | Geef een beschrijvende naam voor de PDF-uitvoerinstellingen die u maakt. Bijvoorbeeld, kunt u _Interne klantenoutput_ of _eind-gebruikers output_ specificeren. |
| Produceer PDF Gebruikend (*Toepasselijk voor het dashboard van de Kaart slechts*) | Selecteer **DITA-OT** om de output van PDF te produceren. Selecteer **FrameMaker Publishing Server** als uw beheerder deze optie heeft gevormd. Sommige configuratieopties variëren wanneer FMPS wordt geselecteerd. Bovendien is de FMPS-configuratieoptie alleen beschikbaar in het kaartdashboard. |
| Uitvoerpad/bestemmingspad | Het pad in uw AEM-opslagplaats waar de PDF is opgeslagen.<br> de weg van de Output wordt geplaatst door veranderlijke `${base_output_path}`, die door de Beheerder wordt gevormd. Om de weg van de Output te vormen, vormt de mening [ de Plaats van de Output van de Basis voor de diensten van de Wolk ](../native-pdf/configure-base-location-cs.md) of [ vormt de Plaats van de Output van de Basis voor de diensten On-Prem ](../native-pdf/configure-base-output-location.md) die op de diensten worden gebaseerd u gebruikt.<br> u kunt sommige uit-van-doos variabelen ook gebruiken om de weg van de Output te bepalen, de variabelen van het 1} Gebruik van de mening voor het plaatsen van de Weg van de Bestemming, de Naam van de Plaats, of de opties van de Naam van het Dossier [.](generate-output-use-variables.md#id18BUG70K05Z) |
| Argumenten DITA-OT-opdrachtregel | Geef de aanvullende argumenten op die u tijdens het genereren van uitvoer wilt laten verwerken door DITA-OT. Voor details over de bevel-lijn argumenten die in DITA-OT worden gesteund, mening [ DITA-OT documentatie ](https://www.dita-ot.org/). |
| Transformatienaam | Geef het type uitvoer op dat u wilt genereren. Dit is vereist als u uitvoer wilt genereren met uw eigen aangepaste plug-in, die is geïntegreerd in de DITA-OT-plug-in. Als u bijvoorbeeld XHTML-uitvoer wilt genereren, geeft u `xhtml` op. Voor een lijst van transformaties beschikbaar in DITA-OT, mening [ DITA-OT transformaties (outputformaten) ](http://www.dita-ot.org/2.3/user-guide/AvailableTransforms.html) in de Gids van de Gebruiker van OASIS DITA-OT. |
| PDF-bestandsnaam/bestandsnaam | Geef de bestandsnaam op waarmee u de PDF wilt opslaan.<br><br> u kunt variabelen ook gebruiken terwijl het plaatsen van de Naam van het Dossier van PDF. Voor meer details over het gebruiken van variabelen, mening [ variabelen van het Gebruik voor het plaatsen van de Weg van de Bestemming, de Naam van de Plaats, of de opties van de Naam van het Dossier ](generate-output-use-variables.md#id18BUG70K05Z).<br><br>**Nota**: Als u geen dossier verstrekt - noem, dan wordt de titel van de kaart DITA gebruikt om de definitieve het dossiernaam van PDF te produceren. Als de kaart geen titel heeft, wordt de bestandsnaam van de DITA-kaart gebruikt om de uiteindelijke PDF te noemen. De bestandsnaam wordt ontsmet volgens de regels die in het systeem zijn geconfigureerd voor het verwerken van elk ongeldig teken. |
| Voorwaardelijk filteren/Voorwaarden toepassen met | Selecteer één van de volgende opties:<br><br>* **toegepaste niets**: Selecteer deze optie als u geen voorwaarde op de gepubliceerde output wilt toepassen.<br>* **DITAVAL dossier**: Selecteer DITAVAL dossier(s) om gepersonaliseerde inhoud te produceren. U kunt meerdere DITAVAL-bestanden selecteren via het dialoogvenster Bladeren of door een bestandspad te typen. Gebruik het kruispictogram bij de bestandsnaam om het te verwijderen. DITAVAL-bestanden worden in de opgegeven volgorde geëvalueerd, zodat de voorwaarden die in het eerste bestand zijn opgegeven voorrang hebben op de voorwaarden die in latere bestanden worden vermeld. U kunt de bestandsvolgorde behouden door bestanden toe te voegen of te verwijderen. <br> u kunt vlaggen binnen een DITAVAL dossier ook toepassen om inhoud visueel te merken. Elke markering kan een afbeelding bevatten en worden opgemaakt met opmaak zoals vet of cursief. Voor meer details bij het aanpassen van het vlaggen stijlen of het oplossen van het formatteren conflicten, mening [ Gebruik de redacteur DITAVAL ](../user-guide/ditaval-editor.md). Als het DITAVAL-bestand naar een andere locatie wordt verplaatst of wordt verwijderd, wordt het niet automatisch verwijderd van het kaartdashboard. U moet de locatie bijwerken als bestanden worden verplaatst of verwijderd. U kunt de muisaanwijzer boven de bestandsnaam plaatsen om het pad weer te geven in de AEM-opslagplaats waar het bestand is opgeslagen. U kunt alleen DITAVAL-bestanden selecteren en er wordt een fout weergegeven als u een ander bestandstype hebt geselecteerd. FrameMaker Publishing Server ondersteunt geen meerdere DITAVAL-bestanden.<br>* **Vooraf ingestelde Voorwaarde**: Selecteer een voorwaarde vooraf ingesteld van drop-down om een voorwaarde toe te passen terwijl het publiceren van de output. De optie is zichtbaar als u een voorwaarde hebt toegevoegd op het tabblad Voorinstellingen voorwaarde van de DITA-kaartconsole. Meer over voorwaarde vooraf ingesteld, mening [ vooraf instelt van het Gebruik van de voorwaarde ](generate-output-use-condition-presets.md#id1825FL004PN). |
| Workflow na generatie uitvoeren | Als u deze optie kiest, wordt een nieuwe vervolgkeuzelijst Werkstroom na generatie weergegeven met alle werkstromen die in AEM zijn geconfigureerd. U moet een werkstroom selecteren die u wilt uitvoeren nadat de werkstroom van de outputgeneratie is voltooid.<br><br>**Nota**: Voor meer informatie over het creëren van een douanewerkschema van de post-output generatie, de mening past post-output het productiewerkschema in installeert aan en vormt Adobe Experience Manager Guides as a Cloud Service. |
| Basislijn gebruiken | Als u een basislijn voor de geselecteerde kaart hebt gecreeerd DITA, selecteer deze optie om de versie te specificeren die u wilt publiceren.<br><br> het Werk van de Mening [ met Basislijn ](generate-output-use-baseline-for-publishing.md#id1825FI0J0PF) voor meer detail. |
| Tijdelijke bestanden behouden | Selecteer deze optie om de tijdelijke bestanden te behouden die door DITA-OT worden gegenereerd. Als er fouten optreden bij het genereren van uitvoer via DITA-OT, selecteert u deze optie om de tijdelijke bestanden te behouden. U kunt die dossiers dan gebruiken om de fouten van de outputgeneratie problemen op te lossen.<br> <br> Na het produceren van de output, selecteer het **tijdelijke dossiers van de Download** ![ pictogram van de download tijdelijke dossiers ](images/download-temp-files-icon.png) om de omslag te downloaden van het PIT die de tijdelijke dossiers bevat. De gedownloade bestanden bevatten ook `system_config.xml` -bestand dat u informatie geeft over de URL van de auteur, de lokale URL en de publicatie-URL. Deze URL&#39;s worden geconfigureerd in de AEM-instellingen voor extern maken en worden weergegeven in het `system_config.xml` -bestand.<br><br> **Nota**: Als de dossiereigenschappen tijdens generatie worden toegevoegd, omvatten de output tijdelijke dossiers ook a *metadata.xml* dossier die die eigenschappen bevatten. |
| Bestandseigenschappen | Selecteer de eigenschappen die u als metagegevens wilt verwerken. Deze eigenschappen worden ingesteld op de pagina Eigenschappen van de DITA-kaart of het bladwijzerbestand. De eigenschappen u van de dropdown lijst selecteert verschijnen onder het **gebied van de Eigenschappen van het Dossier 0} {.** Selecteer het kruispictogram naast de eigenschap om deze te verwijderen. <br><br> Nota: U kunt de meta-gegevens tot de output ook overgaan gebruikend DITA-OT het publiceren. Voor meer detailmening, [ pas op de meta-gegevens aan de output over gebruikend DITA-OT ](pass-metadata-dita-ot.md#id21BJ00QD0XA). |


**Bovenliggend onderwerp:**[ Begrijpend de output stelt ](generate-output-understand-presets.md) vooraf in
