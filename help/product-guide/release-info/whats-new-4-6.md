---
title: Opmerkingen bij de release | Nieuwe functies in Adobe Experience Manager Guides 4.4.0-release
description: Meer informatie over de nieuwe en verbeterde functies in de 4.4.0-release van Adobe Experience Manager Guides
role: Leader
source-git-commit: 57c3b39f0ab0fde5b18e4d4ae0e1501738997e68
workflow-type: tm+mt
source-wordcount: '3050'
ht-degree: 0%

---

# Nieuwe functies in de release 4.6.0 (september 2024)

Dit artikel behandelt de nieuwe en verbeterde functies die zijn geïntroduceerd met versie 4.6.0 van Adobe Experience Manager Guides.

Voor de lijst van kwesties die in deze versie zijn bevestigd, mening [ Vaste kwesties in de 4.6.0 versie ](../release-info/fixed-issues-4-6-0.md).

Leer over [ verbeteringsinstructies voor de versie 4.6.0 ](../release-info/upgrade-instructions-4-6-0.md).


## Verbeteringen voor publiceren

De volgende verbeteringen in het publiceren van inhoud zijn aangebracht in de release 4.6.0:



### Een onderwerp of zijn elementen aan een Fragment van de Ervaring Publish

Een ervaringsfragment is een modulaire inhoudseenheid in Adobe Experience Manager waarin inhoud en lay-out worden geïntegreerd. De Fragmenten van de ervaring zijn essentieel voor het creëren van verenigbare en het engageren ervaringen, die verder over veelvoudige kanalen kunnen worden opnieuw gebruikt. U kunt bijvoorbeeld ervaringsfragmenten maken voor kop- of voetteksten met brandingelementen, promotionele banners, getuigenissen van klanten en gebeurtenispromoties.

![ dossier eigenschappen opties tabel ](./assets/file-properties-outputs-4-6.png) {width="300" align="left"}

*Publish en bekijk de Fragmenten van de Ervaring van een onderwerp van de **2&rbrace; sectie van Output &lbrace;in de**&#x200B;Eigenschappen van het Dossier **.***

Met Experience Manager Guides kunt u nu een onderwerp of de bijbehorende elementen publiceren naar een ervaringsfragment. U kunt een op JSON-Gebaseerde afbeelding tussen een onderwerp of zijn elementen en een malplaatje van het Fragment van de Ervaring tot stand brengen. U kunt ook Experience Fragment-variaties maken met behulp van de voorwaardenfilters.

Leer meer over hoe te [ de Fragmenten van de Ervaring van Publish ](../user-guide/publish-experience-fragment.md).



### Verbeteringen in het publiceren van inhoudsfragmenten

Experience Manager Guides biedt ook enkele nuttige verbeteringen in Content Fragments:

- Met Experience Manager Guides kunt u een onderwerp of de elementen ervan publiceren naar een inhoudsfragment.

- U kunt de Fragmenten van de Inhoud van een onderwerp van de **sectie van Output** in de **Eigenschappen van het Dossier** publiceren en bekijken.


- U kunt eenvoudig variaties in inhoudsfragmenten maken door inhoud met voorwaarden te filteren terwijl u publiceert naar een inhoudsfragment.

- Gebruik de nieuwe toewijzingsinterface om de elementen gemakkelijk te selecteren en te publiceren naar een inhoudsfragment.

Bij het publiceren van inhoudsfragmenten wordt alleen de toegewezen inhoud vervangen in plaats van het volledige inhoudsfragment te overschrijven. Met deze functie kan een inhoudsfragment gegevens uit meerdere bronnen bevatten, zoals meerdere onderwerpen of de editor voor inhoudsfragmenten.

![ voeg het fragmentmodel en toewijzingsdetails in Publish toe als de dialoog van het Fragment van de Inhoud ](assets/content-fragment-mapping.png)

Voor meer details, mening [ de Fragmenten van de Inhoud van Publish ](../user-guide/publish-content-fragment.md).

### AEM Sites-voorinstelling opnieuw ingedeeld voor gebruiksgemak

De instellingen zijn opnieuw ingedeeld om u te helpen de uitvoervoorinstelling snel te configureren en de AEM Sites-uitvoer te genereren.
U kunt bestaande AEM Sites tot stand brengen stelt vooraf in door de **optie van de de erfeniscomponentenafbeelding van het Gebruik** in de **Nieuwe output vooraf ingestelde** dialoogdoos te selecteren.

Bekijk de **Algemene**, **Inhoud**, en **de verwijzings** lusjes van de Kaart van de kaart in AEM Sites vooraf instelt:
- **Algemeen**: Bevat de algemene configuraties om de output te produceren. U kunt het site- en uitvoerpad opgeven, bestaande uitvoerpagina&#39;s verwijderen of overschrijven, de eerder gegenereerde pagina&#39;s voor verwijderde onderwerpen verwijderen, de ontwerpsjabloon selecteren, de tijdelijke bestanden behouden en de workflow voor na de generatie opgeven.
- **Inhoud**: Bevat de montages toepasselijk op de inhoud voor outputgeneratie. U kunt de filters, de basislijn van de kaart DITA, en de meta-gegevenseigenschappen voor het publiceren selecteren.
- **verwijzingen van de Steekkaart**: Deze lijst bevat onderwerpen die verwijzingen van de dwars-kaart met werkingsgebied = &quot;peer&quot; bevatten. U kunt de het publiceren context voor een lijst van dwars-kaartverwijzingen met scope= &quot;peer&quot;aan onderwerpen specificeren beschikbaar in andere kaarten DITA. Dit tabblad wordt weergegeven als u de Experience Manager Guides-versie (UUID) gebruikt.



### Kruismapverwijzingen uit AEM Sites-voorinstellingen in de webeditor

De meest recente uitbreiding van Experience Manager Guides introduceert verwijzingen naar kruismappen in de AEM Sites-voorinstellingen van de webeditor.
Kruisverwijzingen in Experience Manager Guides helpen de navigatie van inhoud te verbeteren, het hergebruik van inhoud te vergroten en de gebruikerservaring te verbeteren.


U kunt de het publiceren context voor een lijst van dwars-kaartverwijzingen naar onderwerpen specificeren beschikbaar in andere kaarten DITA met scope= &quot;peer&quot;. Bijvoorbeeld, bevat Onderwerp 1 in Kaart A een verwijzing naar Onderwerp 2. Onderwerp 2 kan aanwezig zijn in enige of veelvoudige kaarten.  U kunt de bovenliggende kaart en een specifieke voorinstelling selecteren of de meest recente gepubliceerde uitvoer voor elke koppeling.

Als het zelfde onderwerp naar meer dan eens in een dossier wordt verwezen, dan kunt u een verschillende het publiceren context voor elke instantie toevoegen. Dit biedt meer flexibiliteit en controle over de inhoud ervan. Bijvoorbeeld, is Onderwerp 3 aanwezig in zowel Kaart B als Kaart C. Onderwerp 1 bevat twee verwijzingen naar Onderwerp 3. U kunt Kaart B als ouderkaart voor de eerste verbinding en Kaart C als ouder voor de tweede verbinding kiezen.

![ Verouderde vooraf ingestelde AEM Sites ](assets/aem-sites-legacy.png)

*specificeer de het publiceren context voor de verbonden onderwerpen van de **Verwijzingen van de kaart**&#x200B;lusje van **AEM Sites**&#x200B;vooraf ingesteld.*






### Mogelijkheid om metagegevens van de eigenschappen van het onderwerpbestand door te geven aan de uitvoer van native PDF

Nu, staat Experience Manager Guides u toe om de meta-gegevens van het dossiereigenschappen van een onderwerp aan de paginalay-outs toe te voegen terwijl het produceren van de Inheemse output van de PDF. Gebruik deze functie om metagegevens voor specifieke onderwerpen, zoals de titel, tags en beschrijving, toe te voegen aan de paginalay-outs. U kunt uw gepubliceerde PDF ook aanpassen die op de meta-gegevens van het onderwerp wordt gebaseerd, zoals het toevoegen van een watermerk aan de achtergrond van het onderwerp die op de het documentstaat van het onderwerp wordt gebaseerd.

![ voeg meta-gegevens inheemse pdf ](./assets/add-metadata-native-pdf.png) toe {width="300" align="left"}

*voeg meta-gegevens aan de gebieden in uw paginalay-outs toe.*

Leer hoe te [ gebieden en meta-gegevens ](../native-pdf/design-page-layout.md#add-fields-metadata) in een paginalay-out toevoegen.





### Ondersteuning voor opmaakdocumenten in publicaties met eigen PDF

Experience Manager Guides ondersteunt ook Markdown-documenten in Native PDF-publicaties. Deze functie is handig en helpt u PDF te genereren voor de Markeringen in uw DITA-kaart.

Voor meer details, mening [ steun voor de documenten van de Prijsverhoging ](../web-editor/native-pdf-web-editor.md#support-for-markdown-documents).


### Download het tijdelijke bestand terwijl u de uitvoer genereert via DITA-OT

U kunt de tijdelijke bestanden ook downloaden die zijn gegenereerd wanneer u de AEM Sites-, HTML-, Aangepast-, JSON- of PDF-uitvoer publiceert via DITA-OT. Met deze functie kunt u eventuele problemen analyseren die zich tijdens het genereren van de uitvoer kunnen voordoen en effectief problemen oplossen.  
U kunt het bestand metadata.xml ook downloaden als u eigenschappen van metagegevens hebt geselecteerd die zijn doorgegeven aan de uitvoer die is gegenereerd met DITA-OT. 

Voor meer details over vooraf instelt, mening [ Begrijpend de output stelt ](../user-guide/generate-output-understand-presets.md) vooraf in.


### Optie voor het kiezen van een platte of geneste bestandshiërarchie voor HTML5-uitvoer

Nu, staat Experience Manager Guides u toe om de vlakke omslaghiërarchie voor de tijdelijke dossiers te behouden waar de volledige inhoud in HTML5 uitvoerformaat wordt gepubliceerd en in één enkele omslag wordt bewaard.
Als u er niet voor kiest om de bestandshiërarchie af te vlakken, wordt de HTML5-uitvoer gegenereerd in een geneste mappenhiërarchie. Dit houdt in dat de oorspronkelijke mapstructuur van de inhoud, met bestanden die in submappen zijn ingedeeld, in de uitvoer wordt gerepliceerd. Deze geneste maphiërarchie maakt een complexere organisatie en categorisering van bestanden mogelijk, waardoor het eenvoudiger wordt om grote gegevensvolumes te beheren en te navigeren.


Leer meer over hoe te [ HTML5 output ](../user-guide/generate-output-html5.md) produceren


## Verbeteringen in de Editor

De volgende redacteursverhogingen zijn toegevoegd in versie 4.6.0:

### Alleen-lezen toegang tot de modus Auteur en Source voor vergrendelde bestanden

Als een DITA- of markeringsbestand is vergrendeld of uitgecheckt door een andere gebruiker, kunt u de inhoud niet bewerken of wijzigen. Naast Voorvertoning kunt u het bestand ook als alleen-lezen bestand weergeven in de modus Auteur of Source.
Op read-only wijze, kunt u de inhoud samen met de markeringen en de attributen binnen de **Auteur** of **Source** wijze bekijken en de dossiereigenschappen uitgeven.

U kunt tot de **mening van de Lay-out** voor read-only kaarten ook toegang hebben DITA.
>[!NOTE]
>
> Uw beheerders van het omslagprofiel moeten *ui_config.json* bijwerken zodat u tot de read-only dossiers in de Auteur, Source, en wijzen van de Lay-out kunt harmonieus toegang hebben.

![ gesloten dossierredacteur ](./assets/locked-file-editor.png)
*Mening de gesloten dossiers op Auteur en de wijze van Source.*


Leer hoe te [ open gesloten dossiers in de wijzen van de Auteur en van Source ](../user-guide/web-editor-edit-topics.md#open-locked-files-in-author-and-source-modes).



### Gedeeltelijke inhoud selecteren voor elementen voor bewerkingen

Experience Manager Guides verbetert het selecteren van de inhoud in de verschillende elementen van de webeditor. U kunt eenvoudig inhoud selecteren in verschillende elementen en bewerkingen uitvoeren, zoals vet, cursief en onderstreept maken.

Met deze functie kunt u de opmaak van gedeeltelijk geselecteerde inhoud naadloos toepassen of verwijderen. U kunt ook snel de inhoud verwijderen die u hebt geselecteerd in de verschillende elementen. Als de inhoud eenmaal is verwijderd, wordt de resterende inhoud indien nodig automatisch samengevoegd met één geldig element. U kunt ook gedeeltelijke inhoud selecteren over elementen en de inhoud omringen onder een geldig element DITA.

Over het algemeen bieden deze verbeteringen een betere ervaring en helpen u uw efficiëntie te verbeteren tijdens het bewerken van uw documenten.
Voor meer details, mening [ Gedeeltelijke selectie van inhoud over element ](../user-guide/web-editor-edit-topics.md#partial-selection-of-content-across-elements).



### Gesegregeerde lijst om geldige elementen weer te geven en in te voegen volgens hun positie

Terwijl het uitgeven van een document in de Redacteur van het Web, kunt u een gescheiden lijst van elementen nu bekijken die bij de huidige plaats en buiten de huidige plaats geldig zijn. Op basis van uw vereisten kiest u een element uit de volgende opties:

- **Geldige elementen bij de huidige plaats** die u bij de huidige cursorplaats zelf kunt opnemen.
- **Geldige elementen buiten de huidige plaats** die u na om het even welke ouders voor het huidige element binnen de elementenhiërarchie kunt opnemen.

![ het elementendialoog van het Tussenvoegsel ](assets/insert-element-dialog.png){width="300" align="left"}

*Mening de gescheiden lijsten van geldige elementen om een element bij de huidige plaats op te nemen.*


Deze gesplitste lijst met geldige elementen helpt u de inhoudsstructuur te behouden en de DITA-standaarden te volgen.

Leer meer over de **eigenschap van het Element van het Tussenvoegsel** in de [ Secundaire toolbar ](../user-guide/web-editor-features.md#2051ea0j0y4) sectie.


### Nieuwe ervaring voor het zoeken en filteren van bestanden in de dataweergave

Nu hebt u een verbeterde ervaring bij het filteren van bestanden. De vernieuwde functionaliteit voor het filteren van bestanden biedt een verbeterde manier om bestanden moeiteloos te doorzoeken en door te bladeren.


![ onderzoeksdossiers in bewaarplaatmening ](assets/repository-filter-search-2404.png){width="300" align="left"}

*Onderzoek naar de dossiers die de tekst bevatten`general purpose.`*

Geniet van voordelen zoals snellere toegang tot relevante bestanden en een intuïtievere gebruikersinterface, waardoor uw zoekervaring vloeiender en efficiënter wordt.

![ snel zoekfilter ](assets/repository-filter-search-quick.png) {width="300" align="left"}

*gebruik de snelle filters om naar DITA en niet-DITA dossiers te zoeken.*


>[!NOTE]
>
> Uw beheerders van het omslagprofiel moeten *ui_config.json* bijwerken zodat u tot deze eigenschap kunt harmonieus toegang hebben.

Leer meer over de **eigenschap van het Onderzoek van de Filter** in de [ Linkerpaneel ](../user-guide/web-editor-features.md#id2051EA0M0HS) sectie.

### Gegroepeerde voorwaarden voor verbeterde inhoudsorganisatie

Met Experience Manager Guides kunt u nu voorwaarden groeperen en presenteren in een geneste hiërarchie, zodat u meerdere voorwaarden aan één groep kunt toevoegen. Door de voorwaarden te groeperen, kunt u hen beter organiseren en toepassen over uw inhoud.

![ voorwaarden die in een genestelde hiërarchie ](assets/conditions-nested-hierarchy.png){width="300" align="left"} worden georganiseerd

Leer meer over de **de eigenschapbeschrijving van de Voorwaarden** in de [ Linkerpaneel ](../user-guide/web-editor-features.md#id2051EA0M0HS) sectie.

### Pas uw ervaring van de Redacteur van het Web met een nieuwe UI van gebruikersvoorkeur aan

Het **de dialoogvakje van de Voorkeur van de Gebruiker** in de Redacteur van het Web omvat nu een nieuwe **Verschijning** tabel. Dit nieuwe lusje staat u toe om de gemeenschappelijkste blik-en-voelen voorkeur in de interface van de Redacteur van het Web gemakkelijk te vormen.

U kunt configureren om de bestanden op titel of bestandsnaam weer te geven en het thema van de toepassing en de bronweergave te wijzigen. Het helpt u ook de montages vormen om van een open dossier in de bewaarplaatmening de plaats te bepalen en de vaste ruimten te behandelen.

![ vormgevingslusje van gebruikersvoorkeur ](assets/user_preference_editor_appearance.png){width="550" align="left"}

*pas de verschijning volgens uw voorkeur aan.*

Leer meer over de **eigenschapbeschrijving van de voorkeur van de Gebruiker** &lbrace;in de [ Linkerpaneel ](../user-guide/web-editor-features.md#id2051EA0M0HS) sectie.


### Een geopend bestand zoeken in de dataweergave van de webeditor

Selecteer **altijd van dossiers in de bewaarplaats** optie in de **Voorkeur van de Gebruiker** de plaats bepalen om snel te navigeren en van uw dossier in de bewaarplaats de plaats te bepalen mening. Je hoeft er niet handmatig naar te zoeken.

Met deze functie kunt u tijdens het bewerken de locatie van het bestand gemakkelijk weergeven in de hiërarchie van opslagruimten.

Voor meer details, bepaal de plaats van mening [ van een open dossier in de bewaarnemermening ](../user-guide/web-editor-edit-topics.md#locate-an-open-file-in-the-repository-view).

### Verbeterde verwerking van vaste spaties in de webeditor

Met Experience Manager Guides kunt u een vaste-spatie-indicator weergeven tijdens het bewerken van documenten in de webeditor. Het verbetert ook de behandeling van vaste ruimten.
Het zet veelvoudige opeenvolgende witte ruimten in één enkele ruimte om om de mening van WYSIWYG van het document in de Redacteur van het Web te bewaren. Deze functie draagt ook bij tot een betere algemene vormgeving en professionaliteit van het document.


Voor meer details, bekijk de [ andere eigenschappen van de Redacteur van het Web ](../user-guide/web-editor-other-features.md).


### De mogelijkheid om eigenschappen van elk element vanuit de elementenhiërarchie weer te geven

Nu, verschijnt het Type van Eigenschappen van de Inhoud **&#x200B;**&#x200B;als dropdown menu. In het vervolgkeuzemenu kunt u de tags van de volledige hiërarchie voor de huidige tag weergeven en selecteren.

Met dit vervolgkeuzemenu hebt u snel toegang tot de eigenschappen van de inhoud van de geselecteerde tag.


![ type dropdown menu in inhoudseigenschappen ](assets/content-properties-type.png){width="300" align="left"}

*selecteer een markering van de hiërarchie voor de huidige markering.*

Leer meer over de **eigenschap van de Eigenschappen van de Inhoud** in de [ Juiste 3&rbrace; sectie van het Comité.](../user-guide/web-editor-features.md#id2051eb003yk)



### Verbeterde prestaties tijdens het bulksgewijs inchecken van de bestanden in de Kaarteditor

Experience Manager Guides verbetert de prestaties en ervaring van de functie Inchecken van grote bestanden in de Kaarteditor. Deze verbetering helpt u de dossiers in bulk sneller controleren.
U kunt de vooruitgang van de controle-binnen verrichting voor de dossiers van **ook bekijken sparen als Nieuwe Versie en ontgrendelen** dialoogdoos. Tot slot verschijnt het succesbericht nadat de bewerking is voltooid en zijn alle geselecteerde uitgecheckte bestanden ingecheckt.

![ sparen als nieuwe versie en open dialoogdoos ](./assets/save-version-lock.png){width="300" align="left"}

*Mening de lijst en de status van de dossiers die in bulk van de Redacteur van de Kaart worden gecontroleerd.*

Leer hoe te [ werken met de Geavanceerde Redacteur van de Kaart ](../user-guide/map-editor-advanced-map-editor.md)





## Verbeteringen voor beheer van de levenscyclus van inhoud

Het beheer van de inhoudslevenscyclus is op de volgende manieren verbeterd:

### Mogelijkheid om inhoud in meerdere talen te vertalen met behulp van vooraf geconfigureerde taalgroepen

Met Experience Manager Guides kunt u nu taalgroepen maken en uw inhoud eenvoudig in meerdere talen vertalen. Met deze functie kunt u vertalingen volgens de behoeften van uw organisatie ordenen en beheren.

Als u bijvoorbeeld uw inhoud voor bepaalde landen in Europa wilt vertalen, kunt u een taalgroep voor Europese talen maken, zoals Engels (EN), Frans (FR), Duits (DE), Spaans (ES) en Italiaans (IT).



![ vertaalpaneel ](assets/translation-languages-2404.png){width="300" align="left"}

*selecteer de taalgroepen of de talen die u uw documenten wilt vertalen.*

>[!NOTE]
>
>Als de doelmap van een taal ontbreekt of als de doeltaal gelijk is aan de bron, wordt deze grijs weergegeven en wordt een waarschuwingsteken weergegeven.

Als beheerder kunt u taalgroepen maken en deze configureren naar meerdere mapprofielen. Als auteur kunt u de taalgroepen weergeven die zijn geconfigureerd in uw mapprofiel.


Het maken van taalgroepen verbetert over het algemeen de efficiëntie en productiviteit van vertaalprojecten en verbetert uiteindelijk het lokalisatieproces in meerdere talen.


Leer hoe te [ documenten van de Redacteur van het Web ](../user-guide/translate-documents-web-editor.md) vertalen.


### Verbeterde prestaties en schaalbaarheid voor grote vertaalprojecten

De vertaalfunctie is sneller en schaalbaarder dan ooit. Het wordt geleverd met een nieuwe architectuur die verbeterde prestaties levert. De projectaanmaaktijd is nu sneller dan eerder en de conflicten tijdens het proces zijn bijna onbestaand. Deze verbeterde prestaties helpen u bij snellere vertalingen, waardoor u ook voor grote vertaalprojecten probleemloos kunt werken.

Deze verbetering is zeer voordelig, aangezien zij de productiviteit en de algemene ervaring verbetert.

Leer meer over hoe te [ documenten van de Redacteur van het Web ](../user-guide/translate-documents-web-editor.md) vertalen.

### Het vertaalproject na de vertaling automatisch verwijderen of uitschakelen

Nu, als beheerder, kunt u de vertaalprojecten vormen om na de voltooiing van de vertaling worden onbruikbaar gemaakt of automatisch worden geschrapt. Met deze functie kunt u efficiënt bronnen gebruiken en bestanden beheren nadat de vertaling is voltooid.

Als u een project verwijdert, worden alle bestanden en mappen in het project permanent verwijderd. Het schrappen van de vertaalprojecten laat u ook toe om de bezette schijfruimte vrij te maken.

U kunt de vertaalprojecten onbruikbaar maken als u hen later wilt gebruiken.

![](assets/editor-setting-translation.png){width="550" align="left"}


*vormt taalgroepen en de schoonmaakmontages voor vertaalprojecten.*


Leer meer over hoe te [ automatisch schrappen of het vertaalproject ](../user-guide/translate-documents-web-editor.md#automatically-delete-or-disable-a-completed-translation-project) onbruikbaar maken.


### Nabewerking voor selectieve mappen op Adobe Experience Manager Assets uitschakelen


Als beheerder kunt u de nabewerking en het genereren van UUID&#39;s voor selectieve mappen op Experience Manager Assets nu uitschakelen. Deze configuratie kan handig zijn, vooral wanneer u werkt met veel elementen of complexe mapstructuren. Bovendien kunnen meerdere gebruikers de elementen snel tegelijk uploaden zonder elkaar te storen.  

Als naverwerking voor een map wordt uitgeschakeld, heeft dit ook invloed op alle onderliggende mappen. Experience Manager Guides biedt nu echter de mogelijkheid om nabewerking selectief in te schakelen voor afzonderlijke onderliggende mappen in de genegeerde map.

Leer hoe te [ postprocessing voor een omslag ](../cs-install-guide/conf-folder-post-processing.md) onbruikbaar maken.


## Verbeteringen in de gegevensbronconnectors

De volgende verbeteringen zijn aangebracht in de gegevensbronconnectors voor de release 2024.4.0:

### Verbind met Salsify, Akeneo, en Microsoft Azure DevOps Boards (ADO) gegevensbronnen

Naast de bestaande out-of-the-box connectors biedt Experience Manager Guides ook connectors voor Salsify-, Akeneo- en Microsoft Azure DevOps Boards (ADO)-gegevensbronnen. Als beheerder kunt u deze connectors downloaden en installeren. Dan, vorm de geïnstalleerde schakelaars.

### Kopieer en plak de voorbeeldquery om een inhoudsfragment of onderwerp te maken

U kunt een vraag van steekproefgegevens in de generator gemakkelijk kopiëren en kleven om een inhoudsfragment of een onderwerp tot stand te brengen. Met deze eigenschap, moet u niet de syntaxis herinneren of een vraag manueel creëren. In plaats van de vraag manueel te typen, kunt u een steekproefvraag kopiëren en kleven, het uitgeven, en het gebruiken om de gegevens volgens uw vereisten te halen.

![ neem de dialoogdoos van het inhoudsfragment op ](assets/insert-content-snippet.png){width="800" align="left"}

*Exemplaar en geef een steekproefvraag uit om het inhoudsfragment tot stand te brengen.*

### Verbinding maken met JSON-gegevensbestanden via een bestandsconnector


Nu, als beheerder, kunt u een JSON dossierschakelaar vormen om JSON- gegevensdossiers als gegevensbron te gebruiken. Gebruik de connector om de JSON-bestanden van uw computer of de Adobe Experience Manager Assets te importeren. Vervolgens kunt u als auteur met behulp van de generatoren inhoudsfragmenten of onderwerpen maken.

Met deze functie kunt u de gegevens die in uw JSON-bestanden zijn opgeslagen, gebruiken en opnieuw gebruiken in verschillende fragmenten. De inhoud wordt ook dynamisch bijgewerkt wanneer u de JSON-bestanden bijwerkt.

### Vorm veelvoudige middel URLs voor een schakelaar om inhoudsfragmenten of onderwerpen te creëren

Als beheerder, kunt u veelvoudige middel URLs voor sommige schakelaars zoals de Generische Cliënt van de REST, Salsify, Akeneo, en Microsoft Azure DevOps Boards (ADO) vormen.

Dan, als auteur, verbind met de gegevensbronnen om inhoudsfragmenten of onderwerpen tot stand te brengen gebruikend de generators. Deze functie is handig omdat u geen gegevensbron hoeft te maken voor elke URL. Het helpt u om gegevens van om het even welke middelen voor een bepaalde gegevensbron in één enkel inhoudsfragment of onderwerp snel te halen.

Bekijk meer details over de gegevensbronschakelaars en hoe te [ een gegevensbronschakelaar van het gebruikersinterface ](../cs-install-guide/conf-data-source-connector-tools.md) vormen.

Leer hoe te [ gegevens van uw gegevensbron ](../user-guide/web-editor-content-snippet.md) gebruiken.

