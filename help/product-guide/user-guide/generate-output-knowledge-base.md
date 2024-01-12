---
title: Kennisbank
description: Leer hoe u een Knowledge Base-voorinstelling maakt in de webeditor en het kaartdashboard. Configureer de uitvoervoorinstelling van de Knowledge Base in AEM hulplijnen.
feature: Publishing
role: User
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '1158'
ht-degree: 0%

---

# Kennisbank {#knowledge-base}

U kunt de **Kennisbank** voorinstelling in de webeditor:

Open het DITA-kaartbestand in het deelvenster Opslagplaats **Kaartweergave** en vervolgens in de **Uitvoer** , selecteert u het plus-pictogram om een uitvoervoorinstelling te maken en selecteert u vervolgens **Kennisbank** van de **Type** vervolgkeuzelijst **Nieuwe uitvoervoorinstelling** in. U kunt de voorinstelling een naam geven en het doel kiezen om het uitvoerbestand te genereren met de opdracht **Adobe Experience Manager**, **Salesforce**, of **ServiceNow**.




## Configuratie van Knowledge Base{#knowledge-base-configuration}


In de redacteur van het Web, zijn de volgende configuraties georganiseerd onder **Algemeen** en **Artikelen** tabs. U kunt ook de instellingen configureren voor de specifieke **Kennisbank** u als doel hebt geselecteerd, **Adobe Experience Manager**, **Salesforce**, of **ServiceNow**.


### Algemeen

| Opties in de Knowledge Base | Beschrijving |
| --- | --- |
| Voorwaarden toepassen met | Selecteer een van de volgende opties:<br><br>* **Niets toegepast**: Selecteer deze optie als u geen voorwaarde wilt toepassen op de gepubliceerde uitvoer.<br>* **DITAVAL-bestand**: Selecteer DITAVAL-bestand(en) om gepersonaliseerde inhoud te genereren. U kunt meerdere DITAVAL-bestanden selecteren via het dialoogvenster Bladeren of door het bestandspad te typen. Gebruik het kruispictogram bij de bestandsnaam om het te verwijderen. DITAVAL-bestanden worden in de opgegeven volgorde geëvalueerd, zodat de voorwaarden die in het eerste bestand zijn opgegeven voorrang hebben op de voorwaarden die in latere bestanden worden vermeld. U kunt de bestandsvolgorde behouden door bestanden toe te voegen of te verwijderen. Als het DITAVAL-bestand naar een andere locatie wordt verplaatst of wordt verwijderd, wordt het niet automatisch uit de voorinstelling verwijderd. U moet de locatie bijwerken als bestanden worden verplaatst of verwijderd. U kunt de muisaanwijzer boven de bestandsnaam plaatsen om het pad weer te geven in de Adobe Experience Manager-opslagplaats waar het bestand is opgeslagen. U kunt alleen DITAVAL-bestanden selecteren en er wordt een fout weergegeven als u een ander bestandstype selecteert.<br>* **Voorinstelling voorwaarde**: Selecteer een voorinstelling voor de voorwaarde in het vervolgkeuzemenu om een voorwaarde toe te passen tijdens het publiceren van de uitvoer. De optie is zichtbaar als u een voorwaarde hebt toegevoegd op het tabblad Voorinstellingen voorwaarde van de DITA-kaartconsole. Meer informatie over voorinstellingen voor voorwaarden vindt u in de weergave [Voorinstellingen voor voorwaarden gebruiken](generate-output-use-condition-presets.md#id1825FL004PN). |
| Basislijn gebruiken | Als u een basislijn voor de geselecteerde kaart hebt gecreeerd DITA, selecteer deze optie om de versie te specificeren die u wilt publiceren.<br><br>Weergave [Werken met basislijn](generate-output-use-baseline-for-publishing.md#id1825FI0J0PF) voor meer informatie . |
| Workflow na generatie | Als u deze optie kiest, wordt een nieuwe vervolgkeuzelijst Workflow na generatie weergegeven met alle workflows die in Adobe Experience Manager zijn geconfigureerd. U moet een werkstroom selecteren die u wilt uitvoeren nadat de uitvoergeneratie is voltooid.<br><br>**Opmerking**: Meer informatie over hoe u [workflow voor genereren na uitvoer aanpassen](../cs-install-guide/customize-workflows.md#id17A6GI004Y4) in de Installatie- en configuratiehandleiding voor Cloud Servicen. |

### ServiceNow

| Opties voor ServiceNow | Beschrijving |
| --- | --- |
| Profiel publiceren | Gebruik dropdown om van de de verbindingsprofielen te selecteren ServiceNow uw beheerder vormt. Als u meer wilt weten over de manier waarop uw beheerder een publicatieprofiel kan maken, raadpleegt u de **Editor-instellingen** functiebeschrijving in het dialoogvenster [Linkerdeelvenster](./web-editor-features.md#id2051EA0M0HS) sectie. |
| Kennisbank | Gebruik dit gebied om de vereiste Kennisbank te selecteren ServiceNow. U kunt kennisbases in de plaats vormen ServiceNow om de inhoud op te slaan die op de toestemmingen wordt gebaseerd. De artikelen van deze DITA-kaart kunnen op deze kennisbanken worden gepubliceerd. |
| Categorie en subcategorie | Categorieën zijn als hiërarchische bomen die worden gebruikt om de artikelen van de Kennisbank te vinden en te classificeren ServiceNow. Voeg een categorie en een subcategorie toe om de onderwerpen en subonderwerpen van TOC aan die categorie en subcategorie op de plaats ServiceNow te publiceren. |

### Salesforce

| Salesforce-opties | Beschrijving |
| --- | --- |
| Profiel publiceren | Gebruik drop-down om van de de verbindingsprofielen te selecteren Salesforce uw beheerder vormt. Als u meer wilt weten over de manier waarop uw beheerder een publicatieprofiel kan maken, raadpleegt u de **Editor-instellingen** functiebeschrijving in het dialoogvenster [Linkerdeelvenster](./web-editor-features.md#id2051EA0M0HS) sectie. |
| Recordtype | Gebruik de vervolgkeuzelijst om de recordtypen te selecteren die in Salesforce zijn ingesteld op basis van de zichtbaarheidsinstellingen die zijn gebaseerd op uw gebruikersprofiel. Met Salesforce-recordtypen kunt u vele records van één type voor dat object groeperen. Ze bepalen hoe uw publicatie wordt georganiseerd. U kunt bijvoorbeeld Type veelgestelde record selecteren en publiceren volgens de pagina-indeling en velden van de veelgestelde vragen. |
| Veld voor artikelinhoud | U kunt verschillende velden en een unieke indeling voor elke recordtypesjabloon hebben. Gebruik deze velden om specifieke informatie in te voeren, afhankelijk van het type artikel. U kunt bijvoorbeeld de titel, het antwoord en de vergelijking van een artikel met veelgestelde vragen weergeven. |
| Categorieën | Selecteer een categorie in het vervolgkeuzemenu om de onderwerpen van de inhoudsopgave in die categorie te publiceren op de Salesforce-site. |

U kunt de volgende opties in Salesforce en ServiceNow ook bekijken vooraf instelt: | Opties | Beschrijving | | — | — | |Verwijder de koptekst van het onderwerp uit de tekst van het artikel.|Selecteer deze optie om de onderwerpkop uit het artikel in de gepubliceerde uitvoer te verwijderen. | |Uploaden als concept | Selecteer deze optie om het onderwerp te uploaden om het als ontwerp te delen alvorens het ter beschikking te stellen van de gebruikers.| |Afbeeldingen uploaden| Selecteer deze optie als u afbeeldingen in onderwerpen wilt opnemen in de gepubliceerde uitvoer.| |Gekoppelde documenten uploaden| Selecteer deze optie om de documenten verbonden in onderwerpen in de gepubliceerde output op te nemen.|


### Adobe Experience Manager

>[!NOTE]
>
>U kunt de Adobe Experience Manager Knowledge Base-voorinstelling gebruiken als uw beheerder deze heeft geconfigureerd. Voor meer informatie, bekijkt u [Publiceren op basis van artikelen vanuit de webeditor](../install-guide/configure-article-based-publishing.md) in de installatie- en configuratiehandleiding.

| Adobe Experience Manager-opties | Beschrijving |
| --- | --- |
| Artikelpad gebruiken | Selecteer deze optie om de **Artikel pad** van de map die de sjablonen van de Knowledge Base bevat. |
| Artikel pad | Dit veld wordt weergegeven als u de optie selecteert **Artikelpad gebruiken**. Blader naar de Knowledge Base-site in uw Adobe Experience Manager-opslagplaats waar de uitvoer wordt opgeslagen. |
| Site | Gebruik dit veld om de vereiste Adobe Experience Manager Knowledge Base te selecteren. U kunt kennisbanken op de Adobe Experience Manager-site configureren om de inhoud op te slaan op basis van de machtigingen. De artikelen van deze DITA-kaart kunnen op deze kennisbanken worden gepubliceerd. |
| Categorie | Selecteer een categorie in het vervolgkeuzemenu om de onderwerpen van de inhoudsopgave in die categorie te publiceren op de site van de Adobe Experebeheer. |
| Sectiesjabloon en artikelsjabloon | Dit zijn de structurele componenten die worden gebruikt om de inhoud van uw output te organiseren. Deze zijn vooraf gedefinieerd in de Adobe Experience Manager-sitesjabloon. |
| Workflow na generatie | Als u deze optie kiest, wordt een nieuwe vervolgkeuzelijst voor workflow na generatie weergegeven met alle workflows die in Adobe Experience Manager zijn geconfigureerd. U moet een werkstroom selecteren die u wilt uitvoeren nadat de werkstroom van de outputgeneratie is voltooid.<br>Meer informatie over hoe [workflow voor genereren na uitvoer aanpassen](../install-guide/customize-workflows.md#id17A6GI004Y4) in de installatie- en configuratiehandleiding. |
>[!TIP]
> 
>Selecteren **Vernieuwen** ![vernieuwingspictogram](images/navtitle-refresh-icon.svg) om de respectieve malplaatjes op de gebieden volgens het malplaatje van de Kennisbank te bevolken dat u hebt geselecteerd.

### Artikelen

Op dit tabblad wordt de structuur of hiërarchische weergave van de kaart weergegeven. Kies de onderwerpen u aan een kennisbank wilt publiceren. Breid een knoop van TOC uit en kies de onderwerpen die u wilt publiceren.

**Bovenliggend onderwerp:** [Uitvoervoorinstellingen](generate-output-understand-presets.md)
