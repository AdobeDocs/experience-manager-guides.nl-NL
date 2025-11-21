---
title: Kennisbank
description: Leer hoe u een Knowledge Base-voorinstelling maakt via de kaartconsole. Configureer de Knowledge Base-uitvoervoorinstelling in AEM Guides.
feature: Publishing
role: User
exl-id: 31fdfd96-377c-406b-96ed-59a80bf6e03e
source-git-commit: 6e23f52fc9124d0f07f8108da1b5fe574f553469
workflow-type: tm+mt
source-wordcount: '1322'
ht-degree: 0%

---

# Kennisbank {#knowledge-base}

Voer de volgende stappen uit om tot de **vooraf ingestelde Kennisbank** van de console van de Kaart te leiden:

1. [ open een DITA kaartdossier in de console van de Kaart ](./open-files-map-console.md).

   U kunt tot het kaartdossier van de **Recente dossiers** widget in de [ sectie van het Overzicht ](./intro-home-page.md#overview) ook toegang hebben. Het geselecteerde kaartbestand wordt geopend in de kaartconsole.
1. In **vooraf instelt van de Output** lusje, selecteer + pictogram om tot een output vooraf ingesteld te leiden.
1. Selecteer **Kennisbank** van het drop-down Type in de **Nieuwe output vooraf ingestelde** dialoogdoos.
1. Op het **gebied van het Doel**, selecteer een doel voor de geproduceerde output. De beschikbare opties zijn; **Adobe Experience Manager**, **Salesforce**, en **ServiceNow**.

   ![](./images/knowledge-base-preset-dialog-box.png){width="350" align="left"}

1. Selecteer **toevoegen aan huidige omslagprofiel** optie om een output tot stand te brengen die binnen het huidige omslagprofiel vooraf in wordt gesteld. Het ![ pictogram van het omslagprofiel ](images/global-preset-icon.svg) wijst op een omslag-profiel-niveau vooraf ingesteld.

   Leer meer over [ beheer Globale en de profieloutput van de Omslag vooraf instelt ](./web-editor-manage-output-presets.md).

1. Selecteer **toevoegen**.

   De voorinstelling voor de Knowledge Base wordt gemaakt.

## Configuratie van Knowledge Base{#knowledge-base-configuration}


De vooraf ingestelde de configuratieopties van de Kennisbank worden georganiseerd onder de **Algemene**, **artikelen**, en het geselecteerde doel (**AEM**/ **ServerNow**/ **Salesforce**) lusjes.

![](./images/kb-aem-preset.png){width="550" align="left"}

### Algemeen

De volgende configuratieopties zijn beschikbaar onder het **Algemene** lusje:

| Opties in de Knowledge Base | Beschrijving |
| --- | --- |
| Voorwaarden toepassen met | Selecteer één van de volgende opties:<br><br>* **toegepaste niets**: Selecteer deze optie als u geen voorwaarde op de gepubliceerde output wilt toepassen.<br>* **DITAVAL dossier**: Selecteer DITAVAL dossier(s) om gepersonaliseerde inhoud te produceren. U kunt meerdere DITAVAL-bestanden selecteren via het dialoogvenster Bladeren of door het bestandspad te typen. Gebruik het kruispictogram bij de bestandsnaam om het te verwijderen. DITAVAL-bestanden worden in de opgegeven volgorde geëvalueerd, zodat de voorwaarden die in het eerste bestand zijn opgegeven voorrang hebben op de voorwaarden die in latere bestanden worden vermeld. U kunt de bestandsvolgorde behouden door bestanden toe te voegen of te verwijderen. Als het DITAVAL-bestand naar een andere locatie wordt verplaatst of wordt verwijderd, wordt het niet automatisch uit de voorinstelling verwijderd. U moet de locatie bijwerken als bestanden worden verplaatst of verwijderd. U kunt de muisaanwijzer boven de bestandsnaam plaatsen om het pad weer te geven in de Adobe Experience Manager-opslagplaats waar het bestand is opgeslagen. U kunt alleen DITAVAL-bestanden selecteren en er wordt een fout weergegeven als u een ander bestandstype selecteert.<br><br> **Nota**: Overweeg het volgende wanneer het gebruiken van het filtreren van DITAVAL voor **publiceren Salesforce**: <br> - slechts `Include` en `Exclude` acties worden gesteund voor elk bezit DITAVAL.<br> - Het aanbrengen van markeringen om voorwaardelijke inhoud in de uitvoer visueel te markeren of te markeren, wordt niet ondersteund.<br> - In de uitvoervoorinstellingen kan slechts één DITAVAL-bestand worden geselecteerd voor publicatie. Meerdere DITAVAL-bestandsselecties worden niet ondersteund voor Salesforce-publicatie. <br> - `ditavalref` verwijzingen binnen de inhoud worden niet ondersteund. <br><br> **Vooraf ingestelde Voorwaarde**: Selecteer een voorwaarde vooraf ingesteld van dropdown om een voorwaarde toe te passen terwijl het publiceren van de output. De optie is zichtbaar als u een voorwaarde hebt toegevoegd op het tabblad Voorinstellingen voorwaarde van de DITA-kaartconsole. Meer over voorwaarde vooraf instelt, mening [ vooraf instelt van het Gebruik ](generate-output-use-condition-presets.md#id1825FL004PN) vooraf in. |
| Basislijn gebruiken | Als u een basislijn voor de geselecteerde kaart hebt gecreeerd DITA, selecteer deze optie om de versie te specificeren die u wilt publiceren.<br><br> het Werk van de Mening [ met Basislijn ](generate-output-use-baseline-for-publishing.md#id1825FI0J0PF) voor meer details. |
| Workflow na generatie | Als u deze optie kiest, wordt een nieuwe vervolgkeuzelijst Workflow na generatie weergegeven met alle workflows die in Adobe Experience Manager zijn geconfigureerd. U moet een werkstroom selecteren die u wilt uitvoeren nadat de uitvoergeneratie is voltooid.<br><br>**Nota**: Leer meer over hoe te [ het werkschema van de post-outputgeneratie ](../cs-install-guide/customize-workflows.md#id17A6GI004Y4) sectie in de Gids van de Installatie en van de Configuratie voor de Diensten van de Wolk aanpassen. |

### Artikelen

Op dit tabblad wordt de structuur of hiërarchische weergave van de kaart weergegeven. Kies de onderwerpen u aan een kennisbank wilt publiceren. Breid een knoop van TOC uit en kies de onderwerpen die u wilt publiceren.

### Doel - Adobe Experience Manager/ServiceNow/Salesforce

De configuratieopties veranderen op basis van het doel dat u selecteert.


**Adobe Experience Manager**

De volgende configuratieopties worden getoond voor **Adobe Experience Manager** als doel:


>[!NOTE]
>
>U kunt de Adobe Experience Manager Knowledge Base-voorinstelling alleen gebruiken als uw beheerder deze heeft geconfigureerd.

| Adobe Experience Manager-opties | Beschrijving |
| --- | --- |
| Artikelpad gebruiken | Selecteer deze optie om de **weg van het Artikel** van de omslag te bekijken die de malplaatjes van de Kennisbank bevat. |
| Artikel pad | Dit gebied verschijnt als u de optie **het artikelweg van het Gebruik** selecteert. Blader naar de Knowledge Base-site in uw Adobe Experience Manager-opslagplaats waar de uitvoer wordt opgeslagen. |
| Site | Gebruik dit veld om de vereiste Adobe Experience Manager Knowledge Base te selecteren. U kunt kennisbanken op de Adobe Experience Manager-site configureren om de inhoud op te slaan op basis van de machtigingen. De artikelen van deze DITA-kaart kunnen op deze kennisbanken worden gepubliceerd. |
| Categorie | Selecteer een categorie in het vervolgkeuzemenu om de onderwerpen van de inhoudsopgave in die categorie op de Adobe Experience Manager-site te publiceren. |
| Sectiesjabloon en artikelsjabloon | Dit zijn de structurele componenten die worden gebruikt om de inhoud van uw output te organiseren. Deze zijn vooraf gedefinieerd in de Adobe Experience Manager-sitesjabloon. |
| Workflow na generatie | Als u deze optie kiest, wordt een nieuwe vervolgkeuzelijst voor workflow na generatie weergegeven met alle workflows die in Adobe Experience Manager zijn geconfigureerd. U moet een werkstroom selecteren die u wilt uitvoeren nadat de werkstroom van de outputgeneratie is voltooid.<br> Leer meer over hoe te [ het werkschema van de post-outputgeneratie ](../install-guide/customize-workflows.md#id17A6GI004Y4) sectie in de Gids van de Installatie en van de Configuratie aanpassen. |

>[!TIP]
> 
>Selecteer **verfrissen** pictogram om de respectieve malplaatjes op de gebieden volgens het malplaatje van de Kennisbank te bevolken dat u hebt geselecteerd.

**ServiceNow**

De volgende configuratieopties worden getoond voor **ServiceNow** als doel:

| Opties voor ServiceNow | Beschrijving |
| --- | --- |
| Profiel publiceren | Gebruik dropdown om van de de verbindingsprofielen te selecteren ServiceNow uw beheerder vormt. Meer over leren hoe uw beheerder een publicatieprofiel kan tot stand brengen, bekijk de **montages van Workspace** (die als **Montages** voor **op-Prem** verschijnen) eigenschapbeschrijving in de [ Linkerpaneel ](./web-editor-features.md#id2051EA0M0HS) sectie. |
| Kennisbank | Gebruik dit gebied om de vereiste Kennisbank te selecteren ServiceNow. U kunt kennisbases in de plaats vormen ServiceNow om de inhoud op te slaan die op de toestemmingen wordt gebaseerd. De artikelen van deze DITA-kaart kunnen op deze kennisbanken worden gepubliceerd. |
| Categorie en subcategorie | Categorieën zijn als hiërarchische bomen die worden gebruikt om de artikelen van de Kennisbank te vinden en te classificeren ServiceNow. Voeg een categorie en een subcategorie toe om de onderwerpen en subonderwerpen van TOC aan die categorie en subcategorie op de plaats ServiceNow te publiceren. |

**Salesforce**

De volgende configuratieopties worden getoond voor **Salesforce** als doel:

| Salesforce-opties | Beschrijving |
| --- | --- |
| Profiel publiceren | Gebruik de drop-down om van de de verbindingsprofielen te selecteren van Salesforce uw beheerder vormt. Meer over leren hoe uw beheerder een publicatieprofiel kan tot stand brengen, bekijk de **montages van Workspace** (die als **Montages** voor **op-Prem** verschijnen) eigenschapbeschrijving in [ bar van het Lusje ](./web-editor-tab-bar.md). |
| Recordtype | Gebruik het vervolgkeuzemenu om een van de recordtypen te selecteren die in Salesforce zijn ingesteld op basis van de zichtbaarheidsinstellingen die zijn gebaseerd op uw gebruikersprofiel. Met Salesforce-recordtypen kunt u vele records van één type voor dat object groeperen. Ze bepalen hoe uw publicatie wordt georganiseerd. U kunt bijvoorbeeld Type veelgestelde record selecteren en publiceren volgens de pagina-indeling en velden van de veelgestelde vragen. |
| Veld voor artikelinhoud | U kunt verschillende velden en een unieke indeling voor elke recordtypesjabloon hebben. Gebruik deze velden om specifieke informatie in te voeren, afhankelijk van het type artikel. U kunt bijvoorbeeld de titel, het antwoord en de vergelijking van een artikel met veelgestelde vragen weergeven. |
| Categorieën | Selecteer een categorie in het vervolgkeuzemenu om de onderwerpen van de inhoudsopgave in die categorie op de Salesforce-site te publiceren. |

**wat meer opties**

U kunt ook de volgende opties weergeven in de voorinstellingen Salesforce en ServiceNow:

| Opties | Beschrijving |
| --- | --- |
| Verwijder de onderwerpkop uit de artikelhoofdtekst. | Selecteer deze optie om de onderwerpkop uit het artikel in de gepubliceerde uitvoer te verwijderen. |
| Uploaden als concept | Selecteer deze optie om het onderwerp te uploaden om het als ontwerp te delen alvorens het ter beschikking te stellen van de gebruikers. |
| Afbeeldingen uploaden | Selecteer deze optie als u afbeeldingen in onderwerpen wilt opnemen in de gepubliceerde uitvoer. |
| Gekoppelde documenten uploaden | Selecteer deze optie om de documenten verbonden in onderwerpen in de gepubliceerde output op te nemen. |





**Bovenliggend onderwerp:** [ Begrijpend de output stelt ](generate-output-understand-presets.md) vooraf in
