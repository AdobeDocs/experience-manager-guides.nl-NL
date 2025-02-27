---
title: Kennisbank
description: Leer hoe u een Knowledge Base-voorinstelling maakt in de webeditor en het kaartdashboard. Configureer de Knowledge Base-uitvoervoorinstelling in AEM Guides.
feature: Publishing
role: User
hide: true
exl-id: 5fc81de9-9ae0-4cd4-a7ef-b52eed2479f7
source-git-commit: 1426cdaecdd358f06e76908b09330e65997e8452
workflow-type: tm+mt
source-wordcount: '1158'
ht-degree: 0%

---

# Kennisbank {#knowledge-base}

U kunt tot de **vooraf ingestelde Kennisbank** van de Redacteur van het Web leiden:

In het paneel van de Bewaarplaats, open het DITA kaartdossier in **Mening van de Kaart**, dan in het **lusje van de Output**, selecteer + pictogram om een output vooraf ingesteld tot stand te brengen, en selecteer dan **Kennisbank** van **Type** dropdown in de **Nieuwe output vooraf ingestelde** dialoog. U kunt vooraf ingesteld noemen en het doel kiezen om de output te produceren gebruikend **Adobe Experience Manager**, **Salesforce**, of **ServiceNow**.




## Configuratie van Knowledge Base{#knowledge-base-configuration}


In de redacteur van het Web, zijn de volgende configuraties georganiseerd onder **Algemene** en **de lusjes van Artikelen**. U kunt de montages voor de specifieke **Kennisbank** ook vormen u als doel, **Adobe Experience Manager**, **Salesforce**, of **ServiceNow** hebt geselecteerd.


### Algemeen

| Opties in de Knowledge Base | Beschrijving |
| --- | --- |
| Voorwaarden toepassen met | Selecteer één van de volgende opties:<br><br>* **toegepaste niets**: Selecteer deze optie als u geen voorwaarde op de gepubliceerde output wilt toepassen.<br>* **DITAVAL dossier**: Selecteer DITAVAL dossier(s) om gepersonaliseerde inhoud te produceren. U kunt meerdere DITAVAL-bestanden selecteren via het dialoogvenster Bladeren of door het bestandspad te typen. Gebruik het kruispictogram bij de bestandsnaam om het te verwijderen. DITAVAL-bestanden worden in de opgegeven volgorde geëvalueerd, zodat de voorwaarden die in het eerste bestand zijn opgegeven voorrang hebben op de voorwaarden die in latere bestanden worden vermeld. U kunt de bestandsvolgorde behouden door bestanden toe te voegen of te verwijderen. Als het DITAVAL-bestand naar een andere locatie wordt verplaatst of wordt verwijderd, wordt het niet automatisch uit de voorinstelling verwijderd. U moet de locatie bijwerken als bestanden worden verplaatst of verwijderd. U kunt de muisaanwijzer boven de bestandsnaam plaatsen om het pad weer te geven in de Adobe Experience Manager-opslagplaats waar het bestand is opgeslagen. U kunt alleen DITAVAL-bestanden selecteren en er wordt een fout weergegeven als u een ander bestandstype selecteert.<br>* **Vooraf ingestelde Voorwaarde**: Selecteer een voorwaarde vooraf ingesteld van dropdown om een voorwaarde toe te passen terwijl het publiceren van de output. De optie is zichtbaar als u een voorwaarde hebt toegevoegd op het tabblad Voorinstellingen voorwaarde van de DITA-kaartconsole. Meer over voorwaarde vooraf instelt, mening [ vooraf instelt van het Gebruik ](generate-output-use-condition-presets.md#id1825FL004PN) vooraf in. |
| Basislijn gebruiken | Als u een basislijn voor de geselecteerde kaart hebt gecreeerd DITA, selecteer deze optie om de versie te specificeren die u wilt publiceren.<br><br> het Werk van de Mening [ met Basislijn ](generate-output-use-baseline-for-publishing.md#id1825FI0J0PF) voor meer details. |
| Workflow na generatie | Als u deze optie kiest, wordt een nieuwe vervolgkeuzelijst Workflow na generatie weergegeven met alle workflows die in Adobe Experience Manager zijn geconfigureerd. U moet een werkstroom selecteren die u wilt uitvoeren nadat de uitvoergeneratie is voltooid.<br><br>**Nota**: Leer meer over hoe te [ het werkschema van de post-outputgeneratie ](/help/product-guide/cs-install-guide/customize-workflows.md#id17A6GI004Y4) sectie in de Gids van de Installatie en van de Configuratie voor de Diensten van de Wolk aanpassen. |

### ServiceNow

| Opties voor ServiceNow | Beschrijving |
| --- | --- |
| Profiel publiceren | Gebruik dropdown om van de de verbindingsprofielen te selecteren ServiceNow uw beheerder vormt. Meer over leren hoe uw beheerder een publicatieprofiel kan tot stand brengen, bekijk de **eigenschapbeschrijving van de Montages van de Redacteur** {in de [ Linkerpaneel ](./web-editor-features.md#id2051EA0M0HS) sectie. |
| Kennisbank | Gebruik dit gebied om de vereiste Kennisbank te selecteren ServiceNow. U kunt kennisbases in de plaats vormen ServiceNow om de inhoud op te slaan die op de toestemmingen wordt gebaseerd. De artikelen van deze DITA-kaart kunnen op deze kennisbanken worden gepubliceerd. |
| Categorie en subcategorie | Categorieën zijn als hiërarchische bomen die worden gebruikt om de artikelen van de Kennisbank te vinden en te classificeren ServiceNow. Voeg een categorie en een subcategorie toe om de onderwerpen en subonderwerpen van TOC aan die categorie en subcategorie op de plaats ServiceNow te publiceren. |

### Salesforce

| Salesforce-opties | Beschrijving |
| --- | --- |
| Profiel publiceren | Gebruik de drop-down om van de de verbindingsprofielen te selecteren van Salesforce uw beheerder vormt. Meer over leren hoe uw beheerder een publicatieprofiel kan tot stand brengen, bekijk de **eigenschapbeschrijving van de Montages van de Redacteur** {in de [ Linkerpaneel ](./web-editor-features.md#id2051EA0M0HS) sectie. |
| Recordtype | Gebruik het vervolgkeuzemenu om een van de recordtypen te selecteren die in Salesforce zijn ingesteld op basis van de zichtbaarheidsinstellingen die zijn gebaseerd op uw gebruikersprofiel. Met Salesforce-recordtypen kunt u vele records van één type voor dat object groeperen. Ze bepalen hoe uw publicatie wordt georganiseerd. U kunt bijvoorbeeld Type veelgestelde record selecteren en publiceren volgens de pagina-indeling en velden van de veelgestelde vragen. |
| Veld voor artikelinhoud | U kunt verschillende velden en een unieke indeling voor elke recordtypesjabloon hebben. Gebruik deze velden om specifieke informatie in te voeren, afhankelijk van het type artikel. U kunt bijvoorbeeld de titel, het antwoord en de vergelijking van een artikel met veelgestelde vragen weergeven. |
| Categorieën | Selecteer een categorie in het vervolgkeuzemenu om de onderwerpen van de inhoudsopgave in die categorie op de Salesforce-site te publiceren. |

U kunt ook de volgende opties weergeven in de voorinstellingen Salesforce en ServiceNow:

| Opties | Beschrijving |
| --- | --- |
| Verwijder de onderwerpkop uit de artikelhoofdtekst. | Selecteer deze optie om de onderwerpkop uit het artikel in de gepubliceerde uitvoer te verwijderen. |
| Uploaden als concept | Selecteer deze optie om het onderwerp te uploaden om het als ontwerp te delen alvorens het ter beschikking te stellen van de gebruikers. |
| Afbeeldingen uploaden | Selecteer deze optie als u afbeeldingen in onderwerpen wilt opnemen in de gepubliceerde uitvoer. |
| Gekoppelde documenten uploaden | Selecteer deze optie om de documenten verbonden in onderwerpen in de gepubliceerde output op te nemen. |


### Adobe Experience Manager

>[!NOTE]
>
>U kunt de Adobe Experience Manager Knowledge Base-voorinstelling gebruiken als uw beheerder deze heeft geconfigureerd. Voor meer details, mening [ op artikel-gebaseerde het publiceren van de sectie van de Redacteur van het Web ](/help/product-guide/install-guide/configure-article-based-publishing.md) in de Gids van de Installatie en van de Configuratie.

| Adobe Experience Manager-opties | Beschrijving |
| --- | --- |
| Artikelpad gebruiken | Selecteer deze optie om de **weg van het Artikel** van de omslag te bekijken die de malplaatjes van de Kennisbank bevat. |
| Artikel pad | Dit gebied verschijnt als u de optie **het artikelweg van het Gebruik** selecteert. Blader naar de Knowledge Base-site in uw Adobe Experience Manager-opslagplaats waar de uitvoer wordt opgeslagen. |
| Site | Gebruik dit veld om de vereiste Adobe Experience Manager Knowledge Base te selecteren. U kunt kennisbanken op de Adobe Experience Manager-site configureren om de inhoud op te slaan op basis van de machtigingen. De artikelen van deze DITA-kaart kunnen op deze kennisbanken worden gepubliceerd. |
| Categorie | Selecteer een categorie in het vervolgkeuzemenu om de onderwerpen van de inhoudsopgave in die categorie te publiceren op de site van Adobe Experebeheer. |
| Sectiesjabloon en artikelsjabloon | Dit zijn de structurele componenten die worden gebruikt om de inhoud van uw output te organiseren. Deze zijn vooraf gedefinieerd in de Adobe Experience Manager-sitesjabloon. |
| Workflow na generatie | Als u deze optie kiest, wordt een nieuwe vervolgkeuzelijst voor workflow na generatie weergegeven met alle workflows die in Adobe Experience Manager zijn geconfigureerd. U moet een werkstroom selecteren die u wilt uitvoeren nadat de werkstroom van de outputgeneratie is voltooid.<br> Leer meer over hoe te [ het werkschema van de post-outputgeneratie ](/help/product-guide/install-guide/customize-workflows.md#id17A6GI004Y4) sectie in de Gids van de Installatie en van de Configuratie aanpassen. |

>[!TIP]
> 
>Selecteer **verfrissen zich** ![ pictogram ](images/navtitle-refresh-icon.svg) verfrist om de respectieve malplaatjes op de gebieden volgens het malplaatje van de Kennisbank te bevolken dat u hebt geselecteerd.

### Artikelen

Op dit tabblad wordt de structuur of hiërarchische weergave van de kaart weergegeven. Kies de onderwerpen u aan een kennisbank wilt publiceren. Breid een knoop van TOC uit en kies de onderwerpen die u wilt publiceren.

**Bovenliggend onderwerp:** [ Begrijpend de output stelt ](generate-output-understand-presets.md) vooraf in
