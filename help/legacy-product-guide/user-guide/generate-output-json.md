---
title: JSON
description: Leer hoe u een JSON-voorinstelling maakt in de webeditor en het kaartdashboard. Configureer de JSON-uitvoervoorinstelling in AEM Guides.
feature: Publishing
role: User
hide: true
exl-id: dbc082e9-e75e-414d-a1d1-41f919b345af
source-git-commit: 6e23f52fc9124d0f07f8108da1b5fe574f553469
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 0%

---

# JSON {#id231KK0180T4}

U kunt de JSON-voorinstelling maken in de webeditor:

Open in het deelvenster Opslagplaats het DITA-toewijzingsbestand in de Kaartweergave en selecteer vervolgens op het tabblad Uitvoer het pictogram + om een uitvoervoorinstelling te maken. Selecteer vervolgens JSON in het keuzemenu Type in het dialoogvenster Voorinstelling toevoegen.

In de redacteur van het Web, zijn de volgende configuraties georganiseerd onder het **Algemene** lusje:

- Uitvoerpad
- Indexbestand
- Voorwaarden toepassen met \(als de voorwaarden voor een kaart zijn gedefinieerd\)
- Basislijn gebruiken \(als een basislijn is gemaakt voor een kaart\)
- Tijdelijke bestanden behouden
- Eigenschappen die in de uitvoer moeten worden doorgevoerd
- Workflow na generatie

Voor details, verwijs naar [&#x200B; configuratie JSON &#x200B;](#id231KJA00REJ).


**configuratie JSON**

De volgende opties zijn beschikbaar voor de JSON-voorinstelling:

>[!NOTE]
>
> U kunt het JSON-bestand ook bewerken in de webeditor.

| JSON-opties | Beschrijving |
| --- | --- |
| Uitvoerpad | Het pad in uw AEM-opslagplaats waar de JSON-uitvoer wordt opgeslagen. |
| Indexbestand | U kunt een naam geven voor het indexbestand dat u maakt voor de JSON-uitvoer. Standaard wordt de bestandsnaam van de DITA-kaart gekozen en wordt een achtervoegsel toegevoegd (zoals `map_filename_index.json` ).<br><br> u kunt variabelen ook gebruiken terwijl het plaatsen van het Dossier van de Index. Voor meer details over het gebruiken van variabelen, zie [&#x200B; variabelen van het Gebruik voor het plaatsen van de Weg van de Bestemming, de Naam van de Plaats, of de opties van de Naam van het Dossier &#x200B;](generate-output-use-variables.md#id18BUG70K05Z). |
| Voorwaarden toepassen met | Selecteer één van de volgende opties:<br><br>* **toegepaste niets**: Selecteer deze optie als u geen voorwaarde op de gepubliceerde output wilt toepassen.<br>* **DITAVAL dossier**: Selecteer DITAVAL dossier(s) om gepersonaliseerde inhoud te produceren. U kunt meerdere DITAVAL-bestanden selecteren via het dialoogvenster Bladeren of door een bestandspad te typen. Gebruik het kruispictogram bij de bestandsnaam om het te verwijderen. DITAVAL-bestanden worden in de opgegeven volgorde geëvalueerd, zodat de voorwaarden die in het eerste bestand zijn opgegeven voorrang hebben op de voorwaarden die in latere bestanden worden vermeld. U kunt de bestandsvolgorde behouden door bestanden toe te voegen of te verwijderen. Als het DITAVAL-bestand naar een andere locatie wordt verplaatst of wordt verwijderd, wordt het niet automatisch verwijderd van het kaartdashboard. U moet de locatie bijwerken als bestanden worden verplaatst of verwijderd. U kunt de muisaanwijzer boven de bestandsnaam plaatsen om het pad te zien in de AEM-opslagplaats waar het bestand is opgeslagen. U kunt alleen DITAVAL-bestanden selecteren en er wordt een fout weergegeven als u een ander bestandstype hebt geselecteerd.<br>* **Vooraf ingestelde Voorwaarde**: Selecteer een voorwaarde vooraf ingesteld van drop-down om een voorwaarde toe te passen terwijl het publiceren van de output. De optie is zichtbaar als u een voorwaarde hebt toegevoegd op het tabblad Voorinstellingen voorwaarde van de DITA-kaartconsole. Om meer over vooraf ingestelde voorwaarde te weten, zie [&#x200B; Voorinstellingen van het Gebruik &#x200B;](generate-output-use-condition-presets.md#id1825FL004PN). |
| Basislijn gebruiken | Als u een basislijn voor de geselecteerde kaart hebt gecreeerd DITA, selecteer deze optie om de versie te specificeren die u wilt publiceren.<br><br> zie [&#x200B; Werk met Basislijn &#x200B;](generate-output-use-baseline-for-publishing.md#id1825FI0J0PF) voor meer detail. |
| Tijdelijke bestanden behouden | Selecteer deze optie om de tijdelijke bestanden te behouden die door DITA-OT worden gegenereerd. Als er fouten optreden bij het genereren van uitvoer via DITA-OT, selecteert u deze optie om de tijdelijke bestanden te behouden. U kunt die dossiers dan gebruiken om de fouten van de outputgeneratie problemen op te lossen.<br> <br> Na het produceren van de output, selecteer het **tijdelijke dossiers van de Download** ![&#x200B; pictogram van de download tijdelijke dossiers &#x200B;](images/download-temp-files-icon.png) om de omslag te downloaden van het PIT die de tijdelijke dossiers bevat. <br><br> **Nota**: Als de dossiereigenschappen tijdens generatie worden toegevoegd, omvatten de output tijdelijke dossiers ook a *metadata.xml* dossier die die eigenschappen bevatten. |
| Eigenschappen die in de uitvoer moeten worden doorgevoerd | Selecteer de eigenschappen die u als metagegevens wilt verwerken. Deze eigenschappen worden ingesteld op de pagina Eigenschappen van de DITA-kaart of het bladwijzerbestand. De eigenschappen die u selecteert in de vervolgkeuzelijst, worden weergegeven onder het veld Eigenschappen.<br><br>**Nota**: U kunt douaneeigenschappen ook bepalen en de meta-gegevens tot de output overgaan gebruikend DITA-OT het publiceren. Voor meer details zie, [&#x200B; Werk met meta-gegevens &#x200B;](metadata-dita.md#id21BJ00QD0XA). |
| Workflow na generatie | Als u deze optie kiest, wordt een nieuwe vervolgkeuzelijst Werkstroom na generatie weergegeven met alle werkstromen die in AEM zijn geconfigureerd. U moet een werkstroom selecteren die u wilt uitvoeren nadat de werkstroom van de outputgeneratie is voltooid.<br><br>**Nota**: Voor meer informatie over het creëren van een werkschema van de douanepost-output generatie, zie _werkschema van de post-outputgeneratie_ aanpassen in installeer en vorm de gids van Adobe Experience Manager Guides as a Cloud Service. |

**Bovenliggend onderwerp:**&#x200B;[&#x200B; Begrijpend de output stelt &#x200B;](generate-output-understand-presets.md) vooraf in
