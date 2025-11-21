---
title: AEM-site
description: Maak en configureer AEM-sites met voorinstelling in AEM Guides vanaf het kaartdashboard. Met AEM-sites kunt u op artikelen gebaseerde uitvoer genereren, gekoppelde onderwerpen publiceren, conref gebruiken en een tekenreeks in de inhoud zoeken.
feature: Publishing
role: User
hide: true
exl-id: 41c0d4d5-5c46-4d2b-90b3-8c441fee8e99
source-git-commit: 6e23f52fc9124d0f07f8108da1b5fe574f553469
workflow-type: tm+mt
source-wordcount: '2404'
ht-degree: 0%

---

# AEM Sites-voorinstellingen op het kaartdashboard {#id205BE3008SW}

U kunt AEM Sites-voorinstellingen maken van het dashboard voor de kaart en deze configureren om de AEM Sites-uitvoer te genereren.


De volgende opties zijn beschikbaar voor de AEM Sites-uitvoer:

| AEM Sites-opties | Beschrijving |
| --- | --- |
| Uitvoertype | Het type uitvoer dat u wilt genereren. Als u responsieve AEM Sites-uitvoer wilt genereren, kiest u de optie AEM Sites. |
| Naam instellen | Geef een beschrijvende naam op voor de AEM Sites-instellingen die u maakt. Bijvoorbeeld, kunt u *Interne klantenoutput* of *eind-gebruikers output* specificeren. |
| Sitenaam | Een sitenaam waar de uitvoer wordt opgeslagen in uw AEM-opslagplaats.<br><br> een knoop in de bewaarplaats van AEM wordt gecreeerd met de hier gespecificeerde naam. Als u de Sitenaam niet opgeeft, wordt het siteknooppunt gemaakt met de naam van het DITA-toewijzingsbestand.<br><br> de Naam van de Plaats u hier specificeert wordt ook gebruikt als titel in browser tabel.<br><br> u kunt variabelen ook gebruiken terwijl het plaatsen van de Naam van de Plaats. Voor meer details over het gebruiken van variabelen, zie [&#x200B; variabelen van het Gebruik voor het plaatsen van de Weg van de Bestemming, de Naam van de Plaats, of de opties van de Naam van het Dossier &#x200B;](generate-output-use-variables.md#id18BUG70K05Z). |
| Ontwerp | Selecteer het ontwerpmalplaatje dat u wilt gebruiken om de output te produceren.<br><br> voor details over hoe te om de malplaatjes van het douaneontwerp te gebruiken om output te produceren, contacteer uw het publiceren beheerder. |
| Doelpad | Het pad in de AEM-opslagplaats waar de uitvoer wordt opgeslagen. Bij het genereren van de uiteindelijke uitvoer worden de sitenaam en het bestemmingspad gecombineerd. Als u bijvoorbeeld Sitenaam opgeeft als `user-guide` en Doelpad als `/content/output/aem-guides` , wordt de uiteindelijke uitvoer gegenereerd onder het knooppunt `/content/output/aem-guides/user-guide` .<br><br> u kunt variabelen ook gebruiken terwijl het plaatsen van de Weg van de Bestemming. Voor meer details over het gebruiken van variabelen, zie [&#x200B; variabelen van het Gebruik voor het plaatsen van de Weg van de Bestemming, de Naam van de Plaats, of de opties van de Naam van het Dossier &#x200B;](generate-output-use-variables.md#id18BUG70K05Z). |
| Voorwaarden toepassen met | Selecteer één van de volgende opties:<br><br>**Geen Toegepast**: Selecteer deze optie als u geen voorwaarde op de gepubliceerde output wilt toepassen.<br>**DITAVal dossier**: Selecteer DITAVal dossier(s) om geconditionaliseerde inhoud te produceren. U kunt meerdere DITAVal-bestanden selecteren via het dialoogvenster Bladeren of door een bestandspad te typen. Gebruik het kruispictogram bij de bestandsnaam om het te verwijderen. DITAVal-bestanden worden in de opgegeven volgorde geëvalueerd, zodat de voorwaarden die in het eerste bestand zijn opgegeven voorrang hebben op de voorwaarden die in latere bestanden worden vermeld. U kunt de bestandsvolgorde behouden door bestanden toe te voegen of te verwijderen. Als het DITAVal-bestand naar een andere locatie wordt verplaatst of wordt verwijderd, wordt het niet automatisch verwijderd van het kaartdashboard. U moet de locatie bijwerken als bestanden worden verplaatst of verwijderd. U kunt de muisaanwijzer boven de bestandsnaam plaatsen om het pad te zien in de AEM-opslagplaats waar het bestand is opgeslagen. U kunt alleen DITAVal-bestanden selecteren en er wordt een fout weergegeven als u een ander bestandstype selecteert.<br>**Vooraf ingestelde Voorwaarde**: Selecteer een voorwaarde vooraf ingesteld van drop-down om een voorwaarde toe te passen terwijl het publiceren van de output. Deze optie is zichtbaar als u een voorwaarde voor het DITA kaartdossier hebt toegevoegd. De voorwaardelijke instellingen zijn beschikbaar op het tabblad Voorinstellingen voorwaarde van de DITA-kaartconsole. Om meer over vooraf ingestelde voorwaarde te weten, zie [&#x200B; Voorinstellingen van het Gebruik &#x200B;](generate-output-use-condition-presets.md#id1825FL004PN). |
| Bestaande uitvoerpagina&#39;s | Selecteer de **optie van de Overschrijf Inhoud** om inhoud in de bestaande pagina&#39;s te beschrijven. Met deze optie overschrijft u alleen de inhoud onder de inhoud en de kopknooppunten van de pagina. Met deze optie schakelt u het gezamenlijk publiceren van inhoud in. Als u deze optie selecteert, kunt u het verwijderen van weespagina&#39;s uit de gepubliceerde uitvoer selecteren. Dit is ook de *standaard* optie voor het creëren van de output van AEM Sites.<br><br> selecteer de **Schrapping en creeer** optie om het even welke bestaande pagina&#39;s tijdens het publiceren te dwingen. Met deze optie verwijdert u het paginaknooppunt samen met de inhoud ervan en alle onderliggende pagina&#39;s eronder. Gebruik deze optie als u de ontwerpsjabloon van de uitvoervoorinstelling hebt gewijzigd of als u extra pagina&#39;s wilt verwijderen die zich al in het doel bevinden. |
| Orphan-sitepagina&#39;s verwijderen | Het selecteren van **overschrijft Inhoud** in het **Bestaande plaatsen van de Pagina&#39;s van de Output** deze optie. Als u deze optie selecteert, worden alle wezen pagina&#39;s verwijderd van de gepubliceerde AEM-site. Deze functie kan alleen worden uitgevoerd als u de volledige DITA-kaart publiceert en niet de incrementele publicatie gebruikt.<br><br> zegt u een kaart DITA hebt gepubliceerd, die onderwerpen a.dita, b.dita, en c.dita bevat. Alvorens de kaart opnieuw te publiceren, verwijderde u b.dita onderwerp van de kaart. Als u deze optie hebt geselecteerd, wordt alle inhoud met betrekking tot b.dita verwijderd uit de AEM Sites-uitvoer en worden alleen a.dita en c.dita gepubliceerd.<br><br> Deze eigenschap verwijdert geen gepubliceerde kindkaart. Bijvoorbeeld, als uw ouderkaart een kindkaart bevat, en u de volledige kindkaart verwijdert, dan wordt de inhoud van de kindkaart niet geschrapt van de gepubliceerde output. Nochtans, als u om het even welk onderwerp uit een kindkaart verwijdert en opnieuw publiceert, dan wordt de inhoud van het verwijderde onderwerp geschrapt van de plaatsuitvoer.<br><br> ook, als er om het even welke referenced inhoud is, en die inhoud wordt verwijderd alvorens opnieuw te publiceren, dan worden de gegevens van de referenced inhoud niet verwijderd.<br><br>**Nota**: De informatie over geschrapte weespagina&#39;s wordt ook gevangen in de logboeken van de outputgeneratie. Voor meer informatie over de toegang tot van de logboekdossiers, zie [&#x200B; Mening en controleer het logboekdossier &#x200B;](generate-output-basic-troubleshooting.md#id1821I0Y0G0A__id1822G0P0CHS). |
| Tijdelijke bestanden behouden | Selecteer deze optie om de tijdelijke bestanden te behouden die door DITA-OT worden gegenereerd. Als er fouten optreden bij het genereren van uitvoer via DITA-OT, selecteert u deze optie om de tijdelijke bestanden te behouden. U kunt die dossiers dan gebruiken om de fouten van de outputgeneratie problemen op te lossen.<br> <br> Na het produceren van de output, selecteer het **tijdelijke dossiers van de Download** ![&#x200B; pictogram van de download tijdelijke dossiers &#x200B;](images/download-temp-files-icon.png) om de omslag te downloaden van het PIT die de tijdelijke dossiers bevat. <br><br> **Nota**: Als de dossiereigenschappen tijdens generatie worden toegevoegd, omvatten de output tijdelijke dossiers ook a *metadata.xml* dossier die die eigenschappen bevatten. |
| Afzonderlijke PDF genereren voor elk onderwerp | Indien geselecteerd, wordt een PDF ook gecreeerd voor elk onderwerp in de kaart DITA. Als u deze optie kiest, wordt een nieuwe optie PDF-pad splitsen weergegeven.<br><br> op het Gesplitste gebied van de Weg van PDF, specificeer de weg om PDFs op te slaan die voor elk onderwerp wordt geproduceerd.<br><br>**Nota**: AEM Guides gebruikt het elektrisch toestel DITA-OT genoemd pdfx om PDF voor elk onderwerp te produceren. Deze plug-in is gebundeld met het DITA-OT-pakket dat buiten de box wordt geleverd. U kunt deze insteekmodule aanpassen om PDF te genereren naar wens. Als u een aangepaste insteekmodule DITA-OT gebruikt, moet u de insteekmodule pdfx integreren voor PDF-generatiefuncties op onderwerpniveau. |
| Workflow na generatie uitvoeren | Als u deze optie kiest, wordt een nieuwe vervolgkeuzelijst Werkstroom na generatie weergegeven met alle werkstromen die in AEM zijn geconfigureerd. U moet een werkstroom selecteren die u wilt uitvoeren nadat de werkstroom van de outputgeneratie is voltooid. |
| Basislijn gebruiken | Als u een basislijn voor de geselecteerde kaart hebt gecreeerd DITA, selecteer deze optie om de versie te specificeren die u wilt publiceren.<br><br>**Belangrijk**: Wanneer u stijgende output voor de Plaats van AEM produceert, dan wordt de output gecreeerd gebruikend de huidige versie van de dossiers en niet de in bijlage Basislijn.<br><br> zie [&#x200B; Werk met Basislijn &#x200B;](generate-output-use-baseline-for-publishing.md#id1825FI0J0PF) voor meer detail. |
| Eigenschappen | Selecteer de eigenschappen die u als metagegevens wilt verwerken. Deze eigenschappen worden ingesteld op de pagina Eigenschappen van de DITA-kaart of het bladwijzerbestand. De eigenschappen u van de dropdown lijst selecteert verschijnen onder het **gebied van de Eigenschappen van het Dossier 0&rbrace; &lbrace;.** Selecteer het kruispictogram naast de eigenschap om deze te verwijderen. <br><br>**Nota**: De meta-gegevenseigenschappen zijn case-sensitive.<br><br>*als u een Basislijn hebt geselecteerd, dan zijn de waarden voor de eigenschappen gebaseerd op de versie van de geselecteerde Basislijn.<br>* Als u geen basislijn hebt geselecteerd, zijn de waarden voor de eigenschappen gebaseerd op de meest recente versie.<br><br> u kunt de meta-gegevens tot de output ook overgaan gebruikend DITA-OT het publiceren. Voor meer details zie, [&#x200B; pas op de meta-gegevens aan de output over gebruikend DITA-OT &#x200B;](pass-metadata-dita-ot.md#id21BJ00QD0XA).<br><br>**Nota**: Als u niet `cq:tags` in de optie van Eigenschappen hebt bepaald, dan worden de waarden voor `cq:tags` genomen van het huidige het werk exemplaar zelfs als u een Basislijn voor het publiceren hebt geselecteerd. |
| Kaarteigenschappen als standaard gebruiken | Als deze optie is geselecteerd, worden de eigenschappen die voor het kaartbestand zijn gedefinieerd, ook gekopieerd naar de onderwerpen waar deze eigenschappen niet zijn gedefinieerd. Overweeg de volgende punten terwijl het gebruiken van deze optie:<br><br>*slechts Koord, Datum, of Lange (enige en multi-getaxeerde) eigenschappen kunnen tot de pagina&#39;s van AEM Sites worden overgegaan.<br>* De metagegevenswaarden voor een eigenschap van het type String ondersteunen geen speciale tekens (zoals `@, #, " "` ).<br>* Deze optie moet samen met de optie `Properties` worden gebruikt. |

## Aanvullende opmerking over AEM Sites

### Op artikel gebaseerde uitvoer genereren vanuit de webeditor

U kunt de output van AEM Sites voor één of meerdere onderwerpen, of de volledige kaart DITA van de Redacteur van het Web produceren. U moet uitvoervoorinstellingen maken voor uw DITA-kaart en vervolgens kunt u eenvoudig de AEM Sites-uitvoer voor uw kaart genereren. Als u een paar onderwerpen in uw kaart hebt bijgewerkt, kunt u de output van AEM Sites slechts voor die onderwerpen van de Redacteur van het Web ook produceren. Voor meer details, zie [&#x200B; Op artikel-gebaseerde het publiceren van de Redacteur van het Web &#x200B;](web-editor-article-publishing.md#id218CK0U019I).

### Produceer output van het verbinden onderwerpen van andere kaarten

Het is een zeer gemeenschappelijk scenario om een grote reeks documentatie te hebben die zich over veelvoudige omslagen en kaarten DITA uitgespreid. Het wordt bijzonder ingewikkeld om inhoud te publiceren die van diverse plaatsen verbonden is. Standaard worden alle koppelingen `<xref>` gemaakt met de lus `local` `@scope` . Het publiceren van dergelijke onderwerpen impliceert geen uitdaging, aangezien het directe verbinding aan het onderwerp gebruikt. Als het onderwerp buiten de huidige kaart DITA is, toont de verbinding niet de verbonden inhoud.

Een andere manier om inhoud te koppelen, is het maken van een koppeling met de `peer` `@scope` . Voor dergelijke inhoud, wordt de verbinding opgelost in runtime door de titel van het dossier en de gevormde context voor het verbonden onderwerp van de DITA kaart te kiezen publiceert context. In de volgende schermafbeelding ziet u het deelvenster Eigenschappen voor een koppeling met de naam `peer` `@scope` :

![](images/peer-link-scope-link.png){width="800" align="left"}

Om het publiceren van complexe kaarten en onderwerpen te vereenvoudigen die met andere onderwerpen in andere kaarten verbinden, staat AEM Guides u toe om de het publiceren context voor elke output vooraf ingesteld te plaatsen.

De het publiceren context staat u toe om te specificeren welk onderwerp moet worden gebruikt waarvan kaart voor het publiceren van een specifieke output. Laten we dit begrijpen met behulp van een voorbeeld — laten we zeggen dat u vier mappen hebt: voorbeeld a, monster b, monster c en monster d. Elke omslag bevat een kaart DITA — kaart A DITA, kaart B DITA, kaart C DITA, en kaart D DITA. De kaart D van DITA dwars-kaart zal verbinden gebeuren wanneer een onderwerp in kaartA van DITA met een onderwerp in kaart B DITA, C, of D. verbindt. In het volgende schermafbeelding bevat een onderwerp met voorbeeldconcepten koppelingen \(of verwijzingen\) naar bestanden die deel uitmaken van andere DITA-kaarten.

![](images/sample-concept-link-to-other.png){width="350" align="left"}

Wanneer u nu de AEM Sites-publicatie-instellingen configureert voor het kaartbestand dat dit onderwerp bevat, kunt u selecteren welke publicatiecontext voor de gekoppelde inhoud wordt gebruikt tijdens het publiceren. Een publicatiecontext is een combinatie van een DITA-kaart en de bijbehorende uitvoervoorinstelling. De uitvoervoorinstelling bevat op zijn beurt een specifieke versie van de inhoud en voorwaardelijke voorinstellingen. Deze volledige combinatie van de DITA-kaart, de uitvoervoorinstelling, de versie \(bestanden\) en de voorwaarden definiëren de publicatiecontext voor een gekoppelde kaart.

Voer de volgende stappen uit om de publicatiecontext voor cross-linked bestanden op te geven:

1. Open de **Output vooraf instelt** lusje van de kaart DITA u wilt publiceren.

1. Selecteer de **vooraf ingestelde uitvoer van de Plaats van AEM**.

   De tabbladen Instellingen voorinstellingen AEM en Context publiceren worden weergegeven.

   ![](images/aem-site-publish-settings.png){width="800" align="left"}

1. Open **publiceer Context** tabel.

   U wordt getoond een lijst van afhankelijke onderwerpen. Dit zijn de onderwerpen die van één of ander onderwerp in de huidige kaart verbonden zijn, maar zij zijn beschikbaar in sommige andere kaarten DITA.

   >[!NOTE]
   >
   > Op het tabblad Publicatie worden onderwerpen weergegeven die alleen via `peer` `@scope` zijn gekoppeld. Voor koppelingen met `local` `@scope` hoeft u de publicatiecontext niet op te geven.

   Standaard zijn voor alle gekoppelde onderwerpen de meest recente uitvoervoorinstelling en -toewijzing geselecteerd.

   ![](images/default-publish-context.png){width="800" align="left"}

1. Om de standaardselectie van kaart te veranderen DITA en vooraf ingesteld, geeft de klik **&#x200B;**&#x200B;\ uit (in de belangrijkste toolbar \).

1. Als u de onlangs gepubliceerde output van elk afhankelijk dossier in de kaart wilt gebruiken, selecteert het uitgezochte **Gebruik onlangs geproduceerde publiceer context voor alle afhankelijke onderwerpen**.

1. In de **drop-down lijst van de Kaart van de Ouder 1&rbrace;, selecteer het kaartdossier met de waarvan output u de output van de huidige kaart wilt verbinden.**

   Bij het selecteren van een kaartdossier, wordt UUID van de kaart getoond in de Ouderlijke kolom van UUID van de Kaart. De uitvoervoorinstellingen die aan de geselecteerde kaart zijn gekoppeld, worden vermeld in de lijst Voorinstellingen bovenliggende kaart.

1. In de **drop-down lijst van de Vooraf ingestelde Kaart van de Ouder**, selecteer de output vooraf ingesteld die u de output van de huidige kaart met wilt verbinden.

1. Selecteer de vereiste kaart en zijn output vooraf instelt voor alle afhankelijke onderwerpen en klik **Gedaan**.

   De context voor de afhankelijke onderwerpen is nu ingesteld. U kunt de uitvoer voor de huidige kaart genereren. Voor meer informatie over het produceren van output, zie [&#x200B; output voor een kaart DITA van de kaartconsole &#x200B;](generate-output-for-a-dita-map.md#) produceren.

### Overvloeien van publicaties

AEM Guides ondersteunt het publiceren van DITA-inhoud binnen uw bestaande AEM-site. Als u bijvoorbeeld een bestaande site hebt, kunt u de AEM Sites-uitvoer gebruiken om alleen de DITA-inhoud op die site te publiceren. In dit proces wordt de bestaande niet-DITA-inhoud niet gewijzigd door het publicatieproces. Neem contact op met de publicatiebeheerder voor meer informatie over het instellen van uw site om alleen DITA-inhoud te publiceren.

### Publiceren `conref`

Als u `conref` in uw inhoud gebruikt, wordt het gepubliceerd als normale of ingebedde inhoud samen met de inhoud in het bron \(of verwijzend\) onderwerp. De `conref` -inhoud wordt samen met de hoofdinhoud gerenderd en er wordt geen aparte sitepagina voor dezelfde inhoud gemaakt. Wanneer u de inhoud zoekt waarnaar wordt verwezen in `conref` , wordt alleen het hoofdonderwerp of de pagina met de `conref` -inhoud weergegeven in de zoekresultaten.

>[!NOTE]
>
>Als u afzonderlijke pagina&#39;s voor de `conref` inhoud gebruikend versie 3.5 van AEM Guides of vroeger hebt geproduceerd, dan wordt het geadviseerd om die pagina&#39;s schoon te maken/te schrappen door de [&#x200B; Schrapping te gebruiken de Orphan optie van de Pagina&#39;s van de Plaats &#x200B;](#delete-orphan-page-aem-site).


### Zoeken in een tekenreeks binnen de inhoud

U kunt zoeken naar een tekenreeks in de AEM Sites-uitvoer. Standaard kunt u alleen in de titels naar de tekenreeks zoeken. Als u naar de tekenreeks in de inhoud of de hoofdtekst van de AEM Sites-uitvoer wilt zoeken, neemt u contact op met de systeembeheerder om de eigenschap flattening.enabled in te schakelen.

![&#x200B; Uitvoer van AEM Sites van het Onderzoek &#x200B;](images/aem-output-search.png){width="650" align="left"}

Voor meer details zie *afvlakking van de de knoopstructuur van de Plaats van AEM* sectie in installeren en vormen de gids van Adobe Experience Manager Guides.

**Bovenliggend onderwerp:**&#x200B;[&#x200B; Begrijpend de output stelt &#x200B;](generate-output-understand-presets.md) vooraf in
