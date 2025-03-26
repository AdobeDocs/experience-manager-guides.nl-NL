---
title: JSON
description: Leer hoe u een JSON-voorinstelling maakt via de Kaartconsole. Configureer de JSON-uitvoervoorinstelling in Experience Manager Guides.
exl-id: 9eb426fc-ca0a-4932-8a55-fea731281a0a
feature: Publishing
role: User
source-git-commit: ac83f613d87547fc7f6a18070545e40ad4963616
workflow-type: tm+mt
source-wordcount: '794'
ht-degree: 0%

---

# JSON {#id231KK0180T4}

Voer de volgende stappen uit om de JSON-voorinstelling te maken vanaf de kaartconsole:

1. [ open een DITA kaartdossier in de console van de Kaart ](./open-files-map-console.md).

   U kunt tot het kaartdossier van de **Recente dossiers** widget in de [ sectie van het Overzicht ](./intro-home-page.md#overview) ook toegang hebben. Het geselecteerde kaartbestand wordt geopend in de kaartconsole.
1. In **vooraf instelt van de Output** lusje, selecteer + pictogram om tot een output vooraf ingesteld te leiden.
1. Selecteer **JSON** van het drop-down Type in **Nieuwe output vooraf ingestelde** dialoogdoos.
1. Op het **gebied van de Naam**, verstrek een naam aan dit vooraf ingesteld.
1. Selecteer **toevoegen aan huidige omslagprofiel** optie om een output tot stand te brengen die binnen het huidige omslagprofiel vooraf in wordt gesteld. Het ![ pictogram van het omslagprofiel ](images/global-preset-icon.svg) wijst op een omslag-profiel-niveau vooraf ingesteld.

   Leer meer over [ beheer Globale en de profieloutput van de Omslag vooraf instelt ](./web-editor-manage-output-presets.md).

1. Selecteer **toevoegen**.

   De JSON-voorinstelling wordt gemaakt.

   ![](images/json-preset-dialog-new.png){width="300" align="left"}

Nadat de voorinstelling is gemaakt, kunt u de volgende vooraf ingestelde configuraties configureren die beschikbaar zijn op het tabblad Algemeen.

- Uitvoerpad
- Indexbestand
- Voorwaarden toepassen met \(als de voorwaarden voor een kaart zijn gedefinieerd\)
- Basislijn gebruiken \(als een basislijn is gemaakt voor een kaart\)
- Tijdelijke bestanden behouden
- Eigenschappen die in de uitvoer moeten worden doorgegeven
- Workflow na generatie

Voor details, verwijs naar [ configuratie JSON ](#json-configuration).

![](images/json-preset-config.png){align="left"}

## JSON-configuratie

De volgende opties zijn beschikbaar voor de JSON-voorinstelling:

>[!NOTE]
>
> U kunt het JSON-bestand ook bewerken in de Editor.

| JSON-opties | Beschrijving |
| --- | --- |
| Uitvoerpad | Het pad in uw AEM-opslagplaats waar de JSON-uitvoer wordt opgeslagen. |
| Indexbestand | U kunt een naam geven voor het indexbestand dat u maakt voor de JSON-uitvoer. Standaard wordt de bestandsnaam van de DITA-kaart gekozen en wordt een achtervoegsel toegevoegd (zoals `map_filename_index.json` ).<br><br> u kunt variabelen ook gebruiken terwijl het plaatsen van het Dossier van de Index. Voor meer details over het gebruiken van variabelen, mening [ variabelen van het Gebruik voor het plaatsen van de Weg van de Bestemming, de Naam van de Plaats, of de opties van de Naam van het Dossier ](generate-output-use-variables.md#id18BUG70K05Z). |
| Voorwaarden toepassen met | Selecteer één van de volgende opties:<br><br>* **toegepaste niets**: Selecteer deze optie als u geen voorwaarde op de gepubliceerde output wilt toepassen.<br>* **DITAVAL dossier**: Selecteer DITAVAL dossier(s) om gepersonaliseerde inhoud te produceren. U kunt meerdere DITAVAL-bestanden selecteren via het dialoogvenster Bladeren of door een bestandspad te typen. Gebruik het kruispictogram bij de bestandsnaam om het te verwijderen. DITAVAL-bestanden worden in de opgegeven volgorde geëvalueerd, zodat de voorwaarden die in het eerste bestand zijn opgegeven voorrang hebben op de voorwaarden die in latere bestanden worden vermeld. U kunt de bestandsvolgorde behouden door bestanden toe te voegen of te verwijderen. Als het DITAVAL-bestand naar een andere locatie wordt verplaatst of wordt verwijderd, wordt het niet automatisch verwijderd van het kaartdashboard. U moet de locatie bijwerken als bestanden worden verplaatst of verwijderd. U kunt de muisaanwijzer boven de bestandsnaam plaatsen om het pad weer te geven in de AEM-opslagplaats waar het bestand is opgeslagen. U kunt alleen DITAVAL-bestanden selecteren en er wordt een fout weergegeven als u een ander bestandstype hebt geselecteerd.<br>* **Vooraf ingestelde Voorwaarde**: Selecteer een voorwaarde vooraf ingesteld van drop-down om een voorwaarde toe te passen terwijl het publiceren van de output. De optie is zichtbaar als u een voorwaarde hebt toegevoegd op het tabblad Voorinstellingen voorwaarde van de DITA-kaartconsole. Meer over voorwaarde vooraf ingesteld, mening [ vooraf instelt van het Gebruik van de voorwaarde ](generate-output-use-condition-presets.md#id1825FL004PN). |
| Basislijn gebruiken | Als u een basislijn voor de geselecteerde kaart hebt gecreeerd DITA, selecteer deze optie om de versie te specificeren die u wilt publiceren.<br><br> het Werk van de Mening [ met Basislijn ](generate-output-use-baseline-for-publishing.md#id1825FI0J0PF) voor meer detail. |
| Tijdelijke bestanden behouden | Selecteer deze optie om de tijdelijke bestanden te behouden die door DITA-OT worden gegenereerd. Als er fouten optreden bij het genereren van uitvoer via DITA-OT, selecteert u deze optie om de tijdelijke bestanden te behouden. U kunt die dossiers dan gebruiken om de fouten van de outputgeneratie problemen op te lossen.<br> <br> Na het produceren van de output, selecteer het **tijdelijke dossiers van de Download** ![ pictogram van de download tijdelijke dossiers ](images/download-temp-files-icon.svg) om de omslag te downloaden van het PIT die de tijdelijke dossiers bevat. <br><br> **Nota**: Als de dossiereigenschappen tijdens generatie worden toegevoegd, omvatten de output tijdelijke dossiers ook a *metadata.xml* dossier die die eigenschappen bevatten. |
| Eigenschappen die in de uitvoer moeten worden doorgegeven | Selecteer de eigenschappen die u als metagegevens wilt verwerken. Deze eigenschappen worden ingesteld op de pagina Eigenschappen van de DITA-kaart of het bladwijzerbestand. De eigenschappen die u selecteert in de vervolgkeuzelijst, worden weergegeven onder het veld Eigenschappen.<br><br>**Nota**: U kunt douaneeigenschappen ook bepalen en de meta-gegevens tot de output overgaan gebruikend DITA-OT het publiceren. Voor meer detailmening, [ Werk met meta-gegevens ](metadata-dita.md#id21BJ00QD0XA). |
| Workflow na generatie | Als u deze optie kiest, wordt een nieuwe vervolgkeuzelijst Werkstroom na generatie weergegeven met alle werkstromen die in AEM zijn geconfigureerd. U moet een werkstroom selecteren die u wilt uitvoeren nadat de werkstroom van de outputgeneratie is voltooid.<br><br>**Nota**: Voor meer informatie over het creëren van een douane post-output het werkschema van de productiegeneratie, mening _aanpassen post-output werkschema_ in installeer en vorm de gids van Adobe Experience Manager Guides as a Cloud Service. |

**Bovenliggend onderwerp:**[ Begrijpend de output stelt ](generate-output-understand-presets.md) vooraf in
