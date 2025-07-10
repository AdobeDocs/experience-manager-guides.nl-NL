---
title: AEM Sites
description: Maak en configureer de AEM Sites-voorinstelling in de module Kaart met behulp van de samengestelde componenttoewijzing en de oudere componenttoewijzing.
feature: Publishing
role: User
exl-id: f3657268-9dee-43af-b643-499dbc3ca948
source-git-commit: 8f2658bd3a724ff375d6d1a9b4474a5cdd8ce270
workflow-type: tm+mt
source-wordcount: '3534'
ht-degree: 0%

---

# AEM Sites-voorinstelling in de kaartconsole

U kunt een AEM Sites-voorinstelling maken via de Kaartenconsole en deze configureren om de AEM Sites-uitvoer te genereren. Er zijn twee manieren om de AEM Sites-uitvoer te maken:

- [ samengestelde componentenafbeelding van het Gebruik ](#use-composite-component-mapping)
- [Koppeling met oudere componenten gebruiken](#use-legacy-component-mapping)

>[!TIP]
>
> Het wordt aanbevolen om de samengestelde componenttoewijzing, beschikbaar in de Experience Manager Guides 2502-release, en nieuwere versies te gebruiken voor betere prestaties.

## Samengestelde componenttoewijzing gebruiken

De samengestelde componenttoewijzing biedt sneller en schaalbaar publiceren naar AEM Sites in vergelijking met het toewijzen van oudere componenten. De sjabloon wordt geleverd met bewerkbare sjablonen die naar wens kunnen worden aangepast met de AEM Template Editor. De sjablonen gebruiken een combinatie van WCM-kerncomponenten en gespecialiseerde `guides-components` om ervoor te zorgen dat eindgebruikers de beste ervaring op uw AEM Sites-pagina&#39;s hebben. U kunt uw bestaande sjablonen ook aanpassen met de samengestelde componenttoewijzingsmethode.

Experience Manager Guides biedt vooraf gedefinieerde sjablonen voor het maken van AEM Sites. Met deze sjablonen kunt u zorgen voor consistentie in de indeling en structuur van de inhoud.
- [ creeer homepages ](../cs-install-guide/download-install-aem-sites-templates-cs.md#create-a-home-page-using-the-template) die op deze vooraf bepaalde malplaatjes worden gebaseerd.
- U kunt [ onderwerpmalplaatjes ](../cs-install-guide/download-install-aem-sites-templates-cs.md#package-installation) uitgeven en stijlen volgens uw vereisten toepassen.
- U kunt [ bestaande malplaatjes van AEM Sites ](../cs-install-guide/download-install-aem-sites-templates-cs.md#customize-existing-aem-sites-templates) ook aanpassen.


**creeer AEM Sites Vooraf ingesteld**

Voer de volgende stappen uit om de AEM Sites-voorinstelling te maken met samengestelde componenttoewijzing:

1. [ open het DITA kaartdossier in kaartconsole ](./open-files-map-console.md).
1. In het **vooraf instelt van de Output** paneel, selecteer + pictogram om tot een output vooraf ingesteld te leiden.
1. Selecteer **AEM Sites** van het **Type** drop-down in de **Nieuwe output vooraf ingestelde** dialoogdoos.
1. Deselecteer de **optie van de de erfeniscomponentenafbeelding van het Gebruik**.
1. Selecteer **toevoegen aan huidige omslagprofiel** optie om een output tot stand te brengen die binnen het huidige omslagprofiel vooraf in wordt gesteld. Het ![ pictogram van het omslagprofiel ](images/global-preset-icon.svg) wijst op een omslag-profiel-niveau vooraf ingesteld.

   Leer meer over [ beheer Globale en de profieloutput van de Omslag vooraf instelt ](./web-editor-manage-output-presets.md).

1. Selecteer **toevoegen**.

   De voorinstelling voor AEM Sites wordt gemaakt.


   ![ Nieuw ](images/new-aem-sites-dialog-box.png){width="300" align="left"}

<!-----------------------
### Generate the AEM Sites output using the templates

Once, the preset is created, you can configure the various options available for AEM Sites output generation. Experience Manager Guides allows you to use the out of the box templates or add your own AEM Sites templates.

You can configure the Out-of-the-box Sites template  in two ways:

- In the **Sites** field, select the AEM sites where you want to publish your output.  For example, `AEMG Docs`.

    The **Publish path** and the **Topic page template** options are automatically set in the dropdown.  For example,  `AEMG-Docs-Site/en/docs/product1` and `Topic page` are set respectively. You can also choose the other options from the dropdown.

- Or, Select the **Use Sites path** option to select the complete Sites path, and then select a **Map page template**. 

    You can browse a predefined Sites path or specify a custom path even if the specified path has not been pre-created within the AEM Sites structure. In such cases, the system creates the necessary structure during the publishing process by using the selected map homepage template.

   For example, you can specify the path `/content/AEMG-Docs-Site/en/docs/product4` where the `product4`does not exist in the strcuture. In this case, the system automatically creates `product4` using the selected **Map page template** and publish the output within this newly created page. 
   
   The **Topic page template** is automatically set as `Topic Page`. However, you can choose to select other available options in the dropdown.

--->

### AEM Sites-configuratie met voorinstellingen voor samengestelde componenttoewijzing

>[!NOTE]
>
> Voordat u de AEM Sites-voorinstelling voor Experience Manager Guides kunt configureren, moet uw beheerder een AEM Sites-structuur maken met de sjablonen.

- **Op-gebouwSoftware**: Leer meer over hoe te [ download en installeer de malplaatjes van AEM Sites ](../install-guide/download-install-aem-sites-templates.md) voor Software op-gebouw.
- **Cloud Service**: Leer meer over hoe te [ download en installeer de malplaatjes van AEM Sites ](../cs-install-guide/download-install-aem-sites-templates-cs.md) voor Cloud Service.

In de console van de Kaart, worden de vooraf ingestelde configuratieopties voor samengestelde componentenafbeelding georganiseerd onder de volgende lusjes:

- Algemeen
- Inhoud
- Lijst met onderwerpen
- Kruisverwijzingen

![ Nieuw ](images/aem-sites-new-config.png){width="650" align="left"}

**Algemeen**

Het **Algemene** lusje bevat de volgende configuratieopties:

| AEM Sites-opties | Beschrijving |
| --- | --- |
| Sitepad gebruiken | Gebruik deze optie om uw inhoud naar een Experience Manager-site te publiceren. |
| Sitepad | **Deze optie verschijnt als u** de optie van de de plaatsweg van het Gebruik **** selecteert. Blader door het vooraf gedefinieerde pad voor de Experience Manager-site of geef een aangepast pad op waar u de uitvoer wilt publiceren. De **optie van de Plaatsen van het Gebruik** staat u toe om de volledige het publiceren weg te specificeren zelfs als de gespecificeerde weg niet vooraf binnen de structuur van AEM Sites is gecreeerd. In dergelijke gevallen creëert het systeem de noodzakelijke structuur tijdens het publicatieproces met behulp van de geselecteerde sjabloon voor kaarthomepage. |
| Paginasjabloon toewijzen | **Deze optie verschijnt als u** de optie van de de plaatsweg van het Gebruik **** selecteert. Selecteer een sjabloon die u wilt toepassen op homepages van kaarten. |
| Site | Naam van de Experience Manager Sites waarnaar u de inhoud wilt publiceren. De opties in het vervolgkeuzemenu worden gevuld op basis van de lijst met sites die beschikbaar zijn in AEM Sites. <br> Uitgezochte **verfrist zich** ![ refreseh pictogram ](images/navtitle-refresh-icon.svg) om een nieuwe lijst van opties te halen en op de bijgewerkte gegevens te wijzen. |
| Pad publiceren | Het pad in de AEM-opslagplaats waar de uitvoer wordt opgeslagen. Het publicatiepad wordt gevuld met alle paden die pagina&#39;s bevatten die op de sjabloon Startpagina zijn gemaakt. De AEM Sites-uitvoer van de DITA-kaart wordt gegenereerd onder dit pad.  Als u bijvoorbeeld de Site opgeeft als `AEMG-Docs` en het publicatiepad als `aemg-docs-en/docs/product-abc.` , wordt de AEM Sites-uitvoer gegenereerd onder het knooppunt `aemg-docs-en/docs/product-abc/` in `crx/de` . |
| Sjabloon voor onderwerppagina | Selecteer het malplaatje u op alle outputonderwerpen wilt toepassen. |
| Paginanamen genereren op basis van | **filename van het Onderwerp**: Gebruikt het dossier van het onderwerp DITA naam om de Plaats URL tot stand te brengen. <br> **Titel van het Onderwerp**: Gebruikt de titel van het onderwerp DITA om de namen van de Plaats van Experience Manager tot stand te brengen. |
| Eerder gegenereerde pagina&#39;s opschonen | - **schrapping eerder geproduceerde pagina&#39;s voor onderwerp dat van de kaart** wordt verwijderd: Als de structuur van de kaart DTIA verandert, kunt u deze optie gebruiken om de eerder geproduceerde pagina&#39;s voor de verwijderde onderwerpen te verwijderen. Deze functie is alleen beschikbaar voor volledige publicatie op de kaart.<br><br> zegt u een kaart DITA hebt gepubliceerd, die onderwerpen a.dita, b.dita, en c.dita bevat. Alvorens de kaart opnieuw te publiceren, verwijderde u b.dita onderwerp van de kaart. Als u deze optie hebt geselecteerd, wordt alle inhoud met betrekking tot b.dita verwijderd uit de AEM Sites-uitvoer en worden alleen a.dita en c.dita gepubliceerd.<br><br>**Nota**: De informatie over geschrapte pagina&#39;s wordt ook gevangen in de logboeken van de outputgeneratie. Voor meer informatie over de toegang tot van de logboekdossiers, [ Mening en controleer het logboekdossier ](generate-output-basic-troubleshooting.md#id1821I0Y0G0A__id1822G0P0CHS). <br><br>**Voorzichtigheid**: Bij het schrappen van de onderwerpen, worden de pagina&#39;s niet beschikbaar van de gepubliceerde plaats. Dus voordat de onderwerpen worden verwijderd, verschijnt er een waarschuwing. U moet bevestigen om hen te schrappen.<br><br> - **schrap alle pagina&#39;s die door andere bronnen bij deze weg** worden gecreeerd: Als u deze optie selecteert, worden alle pagina&#39;s die op deze weg van andere kaarten, individuele onderwerpen, of een andere bron worden gepubliceerd geschrapt. De pagina&#39;s zijn ook niet meer beschikbaar op de gepubliceerde site. Dus voordat de onderwerpen worden verwijderd, verschijnt er een waarschuwing. U moet bevestigen om hen te schrappen. |
| Workflow na generatie | Als u deze optie kiest, wordt een nieuwe vervolgkeuzelijst Werkstroom na generatie weergegeven met alle werkstromen die in AEM zijn geconfigureerd. U moet een werkstroom selecteren die u wilt uitvoeren nadat de werkstroom van de outputgeneratie is voltooid. |

**Inhoud**

Het **lusje van de Inhoud** bevat de volgende configuratieopties:

| AEM Sites-opties | Beschrijving |
| --- | --- |
| Basislijn gebruiken | Als u een basislijn voor de geselecteerde kaart hebt gecreeerd DITA, selecteer deze optie om de versie te specificeren die u wilt publiceren.<br><br> het Werk van de Mening [ met Basislijn ](generate-output-use-baseline-for-publishing.md#id1825FI0J0PF) voor meer details. |
| Voorwaardelijk filteren | Selecteer één van de volgende opties:<br><br>**niets**: Selecteer deze optie als u geen voorwaarde op de gepubliceerde output wilt toepassen.<br>**Gebruikend DITAVAL**: Selecteer DITAVal dossier(s) om geconditionaliseerde inhoud te produceren. U kunt meerdere DITAVal-bestanden selecteren via het dialoogvenster Bladeren of door een bestandspad te typen. Gebruik het kruispictogram bij de bestandsnaam om het te verwijderen. DITAVal-bestanden worden in de opgegeven volgorde geëvalueerd, zodat de voorwaarden die in het eerste bestand zijn opgegeven voorrang hebben op de voorwaarden die in latere bestanden worden vermeld. U kunt de bestandsvolgorde behouden door bestanden toe te voegen of te verwijderen. Als het DITAVal-bestand naar een andere locatie wordt verplaatst of wordt verwijderd, wordt het niet automatisch verwijderd van het kaartdashboard. U moet de locatie bijwerken als bestanden worden verplaatst of verwijderd. U kunt de muisaanwijzer boven de bestandsnaam plaatsen om het pad weer te geven in de AEM-opslagplaats waar het bestand is opgeslagen. U kunt alleen DITAVal-bestanden selecteren en er wordt een fout weergegeven als u een ander bestandstype selecteert.<br>**Vooraf ingestelde Voorwaarde**: Selecteer een voorwaarde vooraf ingesteld van drop-down om een voorwaarde toe te passen terwijl het publiceren van de output. Deze optie is zichtbaar als u een voorwaarde voor het DITA kaartdossier hebt toegevoegd. De voorwaardelijke instellingen zijn beschikbaar op het tabblad Voorinstellingen voorwaarde van de DITA-kaartconsole. Meer over voorwaarde vooraf ingesteld, mening [ vooraf instelt van het Gebruik van de voorwaarde ](generate-output-use-condition-presets.md#id1825FL004PN). |
| Aanvullende DITA-OT opdrachtregelargumenten | Geef de aanvullende argumenten op die u tijdens het genereren van uitvoer wilt laten verwerken door DITA-OT. Voor details over de bevel-lijn argumenten die in DITA-OT worden gesteund, mening [ DITA-OT documentatie ](https://www.dita-ot.org/). |
| Metagegevens <br> <br> Dossier (Assets) Eigenschappen | Selecteer de eigenschappen die u als metagegevens wilt verwerken. Deze eigenschappen worden ingesteld op de pagina Eigenschappen van de DITA-kaart of het bladwijzerbestand. De eigenschappen u van de dropdown lijst selecteert verschijnen onder het **gebied van de Eigenschappen van het Dossier 0} {.** Selecteer het kruispictogram naast de eigenschap om deze te verwijderen. <br><br>**Nota**: De meta-gegevenseigenschappen zijn case-sensitive.<br><br>*als u een Basislijn hebt geselecteerd, dan zijn de waarden voor de eigenschappen gebaseerd op de versie van de geselecteerde Basislijn.<br>* Als u geen basislijn hebt geselecteerd, zijn de waarden voor de eigenschappen gebaseerd op de meest recente versie.<br><br> u kunt de meta-gegevens tot de output ook overgaan gebruikend DITA-OT het publiceren. Voor meer detailmening, [ pas op de meta-gegevens aan de output over gebruikend DITA-OT ](pass-metadata-dita-ot.md#id21BJ00QD0XA).<br><br>**Nota**: Als u niet `cq:tags` in de optie van Eigenschappen hebt bepaald, dan worden de waarden voor `cq:tags` genomen van het huidige het werk exemplaar zelfs als u een Basislijn voor het publiceren hebt geselecteerd. |
| Metagegevens <br> <br> Kaarteigenschappen gebruiken als fallback | Als deze optie is geselecteerd, worden de eigenschappen die voor het kaartbestand zijn gedefinieerd, ook gekopieerd naar de onderwerpen waar deze eigenschappen niet zijn gedefinieerd. Overweeg de volgende punten terwijl het gebruiken van deze optie:<br><br>*slechts Koord, Datum, of Lange (enige en multi-getaxeerde) eigenschappen kunnen tot de pagina&#39;s van de Plaats van AEM worden overgegaan.<br>* De metagegevenswaarden voor een eigenschap van het type String ondersteunen geen speciale tekens (zoals `@, #, " "` ).<br>* Deze optie moet samen met de optie `Properties` worden gebruikt. |

**Lijst van het Onderwerp**

Het **lijst van het Onderwerp** lusje toont de lijst van onderwerpen aanwezig in het huidige werkende exemplaar van de kaart DITA. Standaard worden alle onderwerpen opgenomen. U kunt specifieke onderwerpen selecteren en de output van AEM Sites slechts voor hen produceren. Bijvoorbeeld, hebt u sommige onderwerpen bijgewerkt zodat kunt u slechts die onderwerpen publiceren in plaats van de volledige kaart DITA publiceren.

![ het onderwerpenlijst van plaatsen ](images/aem-presets-topic-list.png) {align="left"}


>[!NOTE]
>
> Wanneer een Basislijn in het **lusje van de Inhoud** wordt geselecteerd, toont de lijst van het Onderwerp onderwerpen en hun versies van de Basislijn in bijlage. Bovendien zou het stijgende publiceren van de lijst van Onderwerpen slechts moeten worden gebruikt wanneer er geen verandering in de structuur van de kaart is. Als er een verandering in de kaartstructuur/TOC is, dan zou de volledige kaart eens moeten worden gepubliceerd om TOC bij te werken.

**de verwijzingen van de Cross-map**

Deze lijst bevat onderwerpen met verwijzingen naar andere mappen met `scope ="peer"` . U kunt de publicatiecontext voor een lijst van verwijzingen naar cross-maps met `scope="peer"` aan onderwerpen specificeren beschikbaar in andere kaarten DITA. Dit tabblad wordt weergegeven als u de Experience Manager Guides-versie (UUID) gebruikt.

Voor meer details, verwijs naar [ het Werken met verbonden onderwerpen ](#working-with-linked-topics) hieronder sectie.

Zodra gevormd, sparen de veranderingen aan vooraf ingesteld, en uitgezocht **produceren** om AEM Sites voor de overeenkomstige kaart te produceren.

>[!NOTE]
>
> Als u voor het eerst inhoud publiceert naar AEM-sites, is het raadzaam de pagina&#39;s op siteniveau te publiceren. Dit verzekert de output correct op **wordt getoond publiceert** instantie zonder enige CSS verstoring.

## Koppeling met oudere componenten gebruiken

De stappen om AEM Sites tot stand te brengen vooraf ingesteld gebruikend erfeniscomponentenafbeelding zijn het zelfde als die geschetst in [ Samengestelde componentenafbeelding ](#use-composite-component-mapping) sectie hierboven. Nochtans, terwijl het creëren van vooraf ingesteld, zorg ervoor dat u de **optie van de afbeelding van de erfeniscomponent van het Gebruik** in de **Nieuwe output vooraf ingestelde** dialoog selecteert.

![](images/aem-sites-output-legacy.png) {width="300" align="left"}

In de console van de Kaart, worden de vooraf ingestelde configuratieopties voor erfeniscomponentenafbeelding georganiseerd onder de volgende lusjes:

- Algemeen
- Inhoud
- Kruisverwijzingen

![ Nieuw ](images/aem-sites-preset-legacy-config.png){width="500" align="left"}

**Algemeen**

Het **Algemene** lusje bevat de volgende configuratieopties:

| AEM Sites-opties | Beschrijving |
| --- | --- |
| Sitenaam | Een sitenaam waar de uitvoer wordt opgeslagen in uw AEM-opslagplaats.<br><br> een knoop in de bewaarplaats van AEM wordt gecreeerd met de hier gespecificeerde naam. Als u de Sitenaam niet opgeeft, wordt het siteknooppunt gemaakt met de naam van het DITA-toewijzingsbestand.<br><br> de Naam van de Plaats u hier specificeert wordt ook gebruikt als titel in browser tabel.<br><br> u kunt variabelen ook gebruiken terwijl het plaatsen van de Naam van de Plaats. |
| Uitvoerpad | Het pad in de AEM-opslagplaats waar de uitvoer wordt opgeslagen. Bij het genereren van de uiteindelijke uitvoer worden de naam en het uitvoerpad van de site gecombineerd. Als u bijvoorbeeld de naam van de site opgeeft als `user-guide` en het uitvoerpad als `/content/output/aem-guides` , wordt de uiteindelijke uitvoer gegenereerd onder het knooppunt `/content/output/aem-guides/user-guide` .<br><br> u kunt variabelen ook gebruiken terwijl het plaatsen van de outputweg. |
| Bestaande uitvoerpagina&#39;s | Selecteer de **optie van de Overschrijf Inhoud** om inhoud in de bestaande pagina&#39;s te beschrijven. Met deze optie overschrijft u alleen de inhoud onder de inhoud en de kopknooppunten van de pagina. Met deze optie schakelt u het gezamenlijk publiceren van inhoud in. Als u deze optie selecteert, kunt u het verwijderen van weespagina&#39;s uit de gepubliceerde uitvoer selecteren. Dit is ook de *standaard* optie voor het creëren van de output van AEM Sites.<br><br> selecteer de **Schrapping en creeer** optie om het even welke bestaande pagina&#39;s tijdens het publiceren te dwingen. Met deze optie verwijdert u het paginaknooppunt samen met de inhoud ervan en alle onderliggende pagina&#39;s eronder. Gebruik deze optie als u de ontwerpsjabloon van de uitvoervoorinstelling hebt gewijzigd of als u extra pagina&#39;s wilt verwijderen die zich al in het doel bevinden. |
| Eerder gegenereerde pagina&#39;s verwijderen voor onderwerpen die van de kaart zijn verwijderd | Als de structuur van de kaart DTIA verandert, kunt u deze optie gebruiken om de eerder geproduceerde pagina&#39;s voor de verwijderde onderwerpen te verwijderen. Deze functie is alleen beschikbaar voor volledige publicatie op de kaart.<br><br> zegt u een kaart DITA hebt gepubliceerd, die onderwerpen a.dita, b.dita, en c.dita bevat. Alvorens de kaart opnieuw te publiceren, verwijderde u b.dita onderwerp van de kaart. Als u deze optie hebt geselecteerd, wordt alle inhoud met betrekking tot b.dita verwijderd uit de AEM Sites-uitvoer en worden alleen a.dita en c.dita gepubliceerd.<br><br>**Nota**: De informatie over geschrapte pagina&#39;s wordt ook gevangen in de logboeken van de outputgeneratie. Voor meer informatie over de toegang tot van de logboekdossiers, [ Mening en controleer het logboekdossier ](generate-output-basic-troubleshooting.md#id1821I0Y0G0A__id1822G0P0CHS). <br><br>**Voorzichtigheid**: Bij het schrappen van de onderwerpen, worden de pagina&#39;s niet beschikbaar van de gepubliceerde plaats. Dus voordat de onderwerpen worden verwijderd, verschijnt er een waarschuwing. U moet bevestigen om hen te schrappen. |
| Ontwerp | Selecteer het ontwerpmalplaatje dat u wilt gebruiken om de output te produceren.<br><br> voor details over hoe te om de malplaatjes van het douaneontwerp te gebruiken om output te produceren, contacteer uw het publiceren beheerder. |
| Workflow na generatie | Als u deze optie kiest, wordt een nieuwe vervolgkeuzelijst Werkstroom na generatie weergegeven met alle werkstromen die in AEM zijn geconfigureerd. U moet een werkstroom selecteren die u wilt uitvoeren nadat de werkstroom van de outputgeneratie is voltooid. |
| Tijdelijke bestanden behouden | Selecteer deze optie om de tijdelijke bestanden te behouden die door DITA-OT worden gegenereerd. Als er fouten optreden bij het genereren van uitvoer via DITA-OT, selecteert u deze optie om de tijdelijke bestanden te behouden. U kunt die dossiers dan gebruiken om de fouten van de outputgeneratie problemen op te lossen.<br> <br> Na het produceren van de output, selecteer het **tijdelijke dossiers van de Download** ![ pictogram van de download tijdelijke dossiers ](images/download-temp-files-icon.svg) om de omslag te downloaden van het PIT die de tijdelijke dossiers bevat. <br><br> **Nota**: Als de dossiereigenschappen tijdens generatie worden toegevoegd, omvatten de output tijdelijke dossiers ook a *metadata.xml* dossier die die eigenschappen bevatten. |

**Inhoud**

![ Nieuw ](images/aem-sites-content-tab.png){width="650" align="left"}

Het **lusje van de Inhoud** bevat de volgende configuratieopties:

| AEM Sites-opties | Beschrijving |
| --- | --- |
| Basislijn gebruiken | Als u een basislijn voor de geselecteerde kaart hebt gecreeerd DITA, selecteer deze optie om de versie te specificeren die u wilt publiceren.<br><br> het Werk van de Mening [ met Basislijn ](./web-editor-baseline.md) voor meer details. |
| Voorwaardelijk filteren | Selecteer één van de volgende opties:<br><br>**niets**: Selecteer deze optie als u geen voorwaarde op de gepubliceerde output wilt toepassen.<br>**Gebruikend DITAVAL**: Selecteer DITAVal dossier(s) om geconditionaliseerde inhoud te produceren. U kunt meerdere DITAVal-bestanden selecteren via het dialoogvenster Bladeren of door een bestandspad te typen. Gebruik het kruispictogram bij de bestandsnaam om het te verwijderen. DITAVal-bestanden worden in de opgegeven volgorde geëvalueerd, zodat de voorwaarden die in het eerste bestand zijn opgegeven voorrang hebben op de voorwaarden die in latere bestanden worden vermeld. U kunt de bestandsvolgorde behouden door bestanden toe te voegen of te verwijderen. Als het DITAVal-bestand naar een andere locatie wordt verplaatst of wordt verwijderd, wordt het niet automatisch verwijderd van het kaartdashboard. U moet de locatie bijwerken als bestanden worden verplaatst of verwijderd. U kunt de muisaanwijzer boven de bestandsnaam plaatsen om het pad weer te geven in de AEM-opslagplaats waar het bestand is opgeslagen. U kunt alleen DITAVal-bestanden selecteren en er wordt een fout weergegeven als u een ander bestandstype selecteert.<br>**Vooraf ingestelde Voorwaarde**: Selecteer een voorwaarde vooraf ingesteld van drop-down om een voorwaarde toe te passen terwijl het publiceren van de output. Deze optie is zichtbaar als u een voorwaarde voor het DITA kaartdossier hebt toegevoegd. De voorwaardelijke instellingen zijn beschikbaar op het tabblad Voorinstellingen voorwaarde van de DITA-kaartconsole. Meer over voorwaarde vooraf ingesteld, mening [ vooraf instelt van het Gebruik van de voorwaarde ](generate-output-use-condition-presets.md#id1825FL004PN). |
| Metagegevens <br> <br> Dossier (Assets) Eigenschappen | Selecteer de eigenschappen die u als metagegevens wilt verwerken. Deze eigenschappen worden ingesteld op de pagina Eigenschappen van de DITA-kaart of het bladwijzerbestand. De eigenschappen u van de dropdown lijst selecteert verschijnen onder het **gebied van de Eigenschappen van het Dossier 0} {.** Selecteer het kruispictogram naast de eigenschap om deze te verwijderen. <br><br>**Nota**: De meta-gegevenseigenschappen zijn case-sensitive.<br><br>*als u een Basislijn hebt geselecteerd, dan zijn de waarden voor de eigenschappen gebaseerd op de versie van de geselecteerde Basislijn.<br>* Als u geen basislijn hebt geselecteerd, zijn de waarden voor de eigenschappen gebaseerd op de meest recente versie.<br><br> u kunt de meta-gegevens tot de output ook overgaan gebruikend DITA-OT het publiceren. Voor meer detailmening, [ pas op de meta-gegevens aan de output over gebruikend DITA-OT ](pass-metadata-dita-ot.md#id21BJ00QD0XA).<br><br>**Nota**: Als u niet `cq:tags` in de optie van Eigenschappen hebt bepaald, dan worden de waarden voor `cq:tags` genomen van het huidige het werk exemplaar zelfs als u een Basislijn voor het publiceren hebt geselecteerd. |
| Metagegevens <br> <br> Kaarteigenschappen gebruiken als fallback | Als deze optie is geselecteerd, worden de eigenschappen die voor het kaartbestand zijn gedefinieerd, ook gekopieerd naar de onderwerpen waar deze eigenschappen niet zijn gedefinieerd. Overweeg de volgende punten terwijl het gebruiken van deze optie:<br><br>*slechts Koord, Datum, of Lange (enige en multi-getaxeerde) eigenschappen kunnen tot de pagina&#39;s van de Plaats van AEM worden overgegaan.<br>* De metagegevenswaarden voor een eigenschap van het type String ondersteunen geen speciale tekens (zoals `@, #, " "` ).<br>* Deze optie moet samen met de optie `Properties` worden gebruikt. |

**de verwijzingen van de Cross-map**

Deze lijst bevat onderwerpen met verwijzingen naar andere mappen met `scope ="peer"` . U kunt de publicatiecontext voor een lijst van verwijzingen naar cross-maps met `scope="peer"` aan onderwerpen specificeren beschikbaar in andere kaarten DITA. Dit tabblad wordt weergegeven als u de Experience Manager Guides-versie (UUID) gebruikt.

Voor meer details, verwijs naar [ het Werken met verbonden onderwerpen ](#working-with-linked-topics) hieronder sectie.

## Werken met gekoppelde onderwerpen

Met Experience Manager Guides kunt u onderwerpverwijzingen maken met de `peer @scope` . Vervolgens kunt u de publicatiecontext van deze verwijzingen definiëren in de AEM Sites-voorinstellingen en ten slotte de uitvoer van de gekoppelde onderwerpen genereren.

Voor meer details, produceren de mening [ output van het verbinden onderwerpen van andere kaarten ](../user-guide/generate-output-aem-site.md#generate-output-linking-topics-from-other-maps).


Voer de volgende stappen uit om de publicatiecontext voor cross-linked bestanden op te geven:

1. Open de **verwijzingen van de Cross-map** tabel. Zorg ervoor dat de `<xrefs>` unieke id&#39;s hebben om dit tabblad weer te geven. Unieke id&#39;s voor `<xrefs>` worden automatisch gegenereerd bij het bewerken/opslaan van de oudere inhoud als de id er niet is.

   In de volgende gevallen kunt u de cross-map link niet bekijken:
   - Voor vooraf instelt die vóór 4.6 versie worden gecreeerd, is het lusje van de Verwijzingen gehandicapt en een hulpmiddeluiteinde, **verwijst naar het dashboard van de Kaart**, verschijnt.
   - Voor vooraf instelt die van het kaartdashboard worden gecreeerd, **verwijs naar het dashboard van de Kaart** tooltip verschijnt.
   - Voor OTB vooraf instelt, **verwijs naar het dashboard van de Kaart** tooltip verschijnt.
   - Voor algemene voorinstellingen maakt u een lokale kopie van deze algemene voorinstelling om verwijzingen naar kruismappen in te stellen.


1. Een lijst met onderwerpen en hun verwijzingen wordt weergegeven

   >[!NOTE]
   >
   >Het **lusje van de Verwijzingen van de Cross-map** toont onderwerpen die het gebruiken van slechts `scope="peer"` verbonden zijn. Voor koppelingen met `scope="local"` hoeft u de publicatiecontext niet op te geven.

   Voor alle gekoppelde onderwerpen is de laatste uitvoervoorinstelling en de kaart standaard geselecteerd. De publicatiecontext voor alle gekoppelde onderwerpen wordt standaard ingesteld op `<Most recently generated>` mapping.

   ![ de verwijzingen van de Cross-map ](images/aem-sites-preset-cross-map-references.png)

1. Als u de onlangs gepubliceerde output van elk afhankelijk dossier in de kaart wilt gebruiken, selecteert het uitgezochte **Gebruik onlangs geproduceerd** publiceer context voor alle afhankelijke onderwerpen.
U zou de kaart moeten publiceren die als ouderkaart wordt geselecteerd alvorens de kaart te publiceren die verbonden onderwerpen bevat. Als de kaart met verbonden onderwerpen niet wordt gepubliceerd, verschijnen de verbindingen als normale teksten in plaats van hyperlinks in de output van AEM Sites.
U moet hetzelfde type AEM Sites-voorinstelling selecteren voor het gekoppelde onderwerp. Als de huidige AEM Sites-voorinstelling bijvoorbeeld gebruikmaakt van oudere componenttoewijzing, selecteert u een vergelijkbare AEM Sites-voorinstelling van het gekoppelde onderwerp.
1. Selecteer in de vervolgkeuzelijst Bovenliggende kaart het kaartbestand met de uitvoer die u wilt koppelen aan de uitvoer van de huidige kaart.
Als u een kaartbestand selecteert, wordt de UUID van de kaart weergegeven in de kolom UUID van bovenliggende kaart. De uitvoervoorinstellingen die aan de gekozen kaart zijn gekoppeld, worden vermeld in de lijst Voorinstellingen bovenliggende kaart. Bijvoorbeeld, bevat Onderwerp 1 in Kaart A een verwijzing naar Onderwerp 2. Onderwerp 2 kan aanwezig zijn in enige of veelvoudige kaarten. U kunt de bovenliggende kaart en een specifieke voorinstelling selecteren of de meest recente gepubliceerde uitvoer voor elke koppeling.

1. Als het zelfde onderwerp naar meer dan eens in een dossier wordt verwezen, dan kunt u een verschillende het publiceren context voor elke instantie toevoegen. Dit biedt meer flexibiliteit en controle over de inhoud ervan. Bijvoorbeeld, is Onderwerp 3 aanwezig in zowel Kaart B als Kaart C. Onderwerp 1 bevat twee verwijzingen naar Onderwerp 3. U kunt Kaart B als ouderkaart voor de eerste verbinding en Kaart C als ouder voor de tweede verbinding kiezen.

1. Selecteer in de vervolgkeuzelijst Voorinstelling bovenliggende kaart de uitvoervoorinstelling waarmee u de uitvoer van de huidige kaart wilt koppelen.
   >[!NOTE]
   >
   > De verschillende AEM Sites-voorinstellingen van de huidige kaart worden weergegeven in de vervolgkeuzelijst. Als u geen voorinstelling selecteert, wordt een waarschuwingspictogram weergegeven en mislukt het genereren van de uitvoer.

1. Selecteer de vereiste kaart en zijn output vooraf instelt voor alle brononderwerpen en uitgezocht **produceert**.




**Bovenliggend onderwerp:** [ Begrijpend de output stelt ](generate-output-understand-presets.md) vooraf in