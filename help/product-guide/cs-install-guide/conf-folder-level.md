---
title: Profielen op algemeen niveau of mapniveau configureren
description: Leer hoe u algemene profielen of mapprofielen configureert
exl-id: 19f63d67-89ef-4c5e-bc9a-cf40dd8d7979
feature: Profiles
role: Admin
level: Experienced
source-git-commit: 1b25f1df67fa2442ab79830dc2ac5a6eabd0394c
workflow-type: tm+mt
source-wordcount: '4285'
ht-degree: 0%

---

# Profielen op algemeen niveau of mapniveau configureren {#id181AH2003PF}

In een onderneming, kunnen de verschillende groepen of de producten verschillende auteursmalplaatjes, outputmalplaatjes, voorwaardelijke attributenprofielen \ (of onderwerpregelingen \), en de configuraties van de Redacteur van het Web gebruiken. Als u deze alleen op ondernemingsniveau \(of algemeen\) configureert, kunnen auteurs problemen ondervinden omdat ze sjablonen of profielen zien die voor hen niet relevant zijn.

Met AEM hulplijnen kunt u ontwerpsjablonen \(onderwerp of kaart\), uitvoersjablonen, voorwaardelijke kenmerken en webeditorconfiguraties op ondernemingsniveau \(algemeen\) en op mapniveau configureren. Op deze manier kunt u de configuraties voor verschillende afdelingen of producten in uw onderneming van elkaar scheiden.

Ook, kunt u de omslag-specifieke configuraties aan een afdeling of productbeheerders delegeren om het beleid te decentraliseren.

Met de tegel Mapprofielen in de instellingen voor hulplijnen kunt u instellingen configureren onder de volgende tabbladen:

![](assets/folder-profile-tabs.png){width="800" align="left"}

- **Algemeen**: Het algemene tabblad is alleen beschikbaar wanneer u instellingen op mapniveau \(of project/product\) configureert. U kunt instellingen configureren, zoals de mappaden waarop de instellingen van toepassing zijn en gebruikers die beheerdersrechten hebben om configuraties te maken of bij te werken.

- **Voorwaardelijke kenmerken**: Gebruik dit tabblad om voorwaardelijke kenmerken op algemeen of mapniveau te configureren. Een voorwaardelijk kenmerk is een combinatie van de naam en de waarde van het kenmerk en u kunt er ook een label voor definiëren. U kunt de standaard attributen DITA of uw eigen douanekenmerken gebruiken. De voorwaardelijke attributen die u op het globale niveau bepaalt worden ter beschikking gesteld aan alle gebruikers over projecten. Als u voorwaardelijke kenmerken op mapniveau hebt gedefinieerd, worden deze samengevoegd met de algemeen gedefinieerde voorwaardelijke kenmerken.

- **Sjablonen**: Gebruik dit tabblad om de sjablonen te configureren die uw auteurs zullen gebruiken om DITA-inhoud te maken of te publiceren. De volgende onderwerpmalplaatjes zijn beschikbaar uit-van-de-doos:

   - Verklarende woordenlijst

   - Referentie

   - Onderwerp

   - Concept

   - Taak

   - Problemen oplossen

   - Leeg

   - DITAVAL

  >[!NOTE]
  >
  > U kunt alle bestaande sjablonen als basis gebruiken om nieuwe sjablonen te maken. De lege DITA-sjabloon bevat geen structuur of elementen zoals de andere sjablonen. U kunt om het even welke malplaatjes OOTB DITA als basis gebruiken, wijzigingen aanbrengen aan het, en het bewaren met een verschillende naam. Nadat u de vereiste wijzigingen hebt aangebracht, voegt u de bijgewerkte sjabloon toe aan de configuratie van de algemene ontwerpsjablonen of de ontwerpsjablonen op mapniveau en wordt deze vervolgens beschikbaar voor ontwerpen.

  Samen met onderwerpmalplaatjes, kunt u de kaartmalplaatjes ook bepalen die aan auteurs ter beschikking zullen worden gesteld. De volgende kaartsjablonen zijn beschikbaar buiten de box:

   - Kaart

   - Bladwijzer

- **Uitvoervoorinstelling**: Net als sjablonen zijn er vijf vooraf geconfigureerde uitvoervoorinstellingen:

   - Site AEM

   - PDF

   - HTML 5

   - EPUB

   - Aangepast

  Uitgevers kunnen deze voorinstellingen voor uitvoer buiten de doos gebruiken om inhoud te publiceren. Deze voorinstellingen kunnen worden geconfigureerd door een beheerder van het algemene profiel of het mapprofiel. Zodra gevormd, worden de het publiceren voorinstellingen beschikbaar aan de uitgevers voor pas gecreëerde kaarten DITA. U kunt ook publicatievoorinstellingen toepassen op bestaande DITA-kaarten. Zie [Vooraf ingestelde wijzigingen toepassen](#id18AGD0K0OHS) voor meer informatie .

- **Configuraties in XML-editor**: Gebruik dit tabblad om de vormgeving en verschillende functies van de webeditor aan te passen. De volgende configureerbare montages zijn beschikbaar voor de Redacteur van het Web:

   - UI-configuratie XML-editor
   - CSS-sjabloonlay-out
   - XML-editorfragmenten
   - Versielabels voor XML-inhoud
   - Rootmap \(alleen op mapniveau\)

U kunt beide configureren: algemeen profiel en mapprofiel. In een profiel op mapniveau kunt u de mappen definiëren waarop de instellingen van toepassing zijn. Deze instellingen zijn onder andere de voorwaardelijke kenmerken, sjablonen, uitvoervoorinstellingen en de instellingen in de XML-editor. De voorwaardelijke voorinstellingen, sjablonen en configuraties van de XML-editor worden vervolgens beschikbaar gesteld aan auteurs die in de geconfigureerde mappen werken. Op dezelfde manier hebben uitgevers toegang tot de geconfigureerde uitvoervoorinstellingen die in de geconfigureerde mappen zijn gedefinieerd.

Een profiel op mapniveau overschrijft de instellingen die in het algemene profiel zijn geconfigureerd. Met andere woorden, als een omslag een omslag-vlakke profiel heeft, dan zal het de malplaatjes, outputmalplaatjes, en montages van de Redacteur van XML tonen die in zijn overeenkomstig omslagprofiel worden gevormd. De instellingen die in het algemene profiel zijn geconfigureerd, worden niet weergegeven. Dit geldt echter niet voor de voorwaardelijke kenmerken. In het geval van voorwaardelijke kenmerken worden de voorwaardelijke kenmerken samengevoegd op algemeen niveau en mapniveau.

In de volgende secties wordt u door het proces geleid voor het configureren van algemene profiel- en mapprofielen.

## Globaal profiel configureren

Voer de volgende stappen uit om het algemene profiel te configureren:

1. Meld u als beheerder aan bij Adobe Experience Manager.

1. Klik op de Adobe Experience Manager-koppeling bovenaan en kies **Gereedschappen**.

1. Selecteren **Hulplijnen** in de lijst met gereedschappen en klik op de knop **Mapprofielen**.

   Voor het eerst wordt op de pagina Mapprofielen alleen de algemene profieltegel weergegeven.

   ![](assets/folder-profile-global.png){width="800" align="left"}

1. Klik op de knop **Globaal profiel** tegel.

1. Om te vormen **Voorwaardelijke kenmerken**, zie [Voorwaardelijke kenmerken voor algemene profielen of mapprofielen configureren](#id1889D0I305Z).

1. Om te vormen **Sjablonen**, zie [Ontwerpsjablonen configureren](#id1889D0IL0Y4).

1. Om te vormen **Voorinstellingen uitvoer**, zie [Uitvoervoorinstellingen configureren](#id18AGD0IH0Y4).

1. Zie voor informatie over het configureren van XML Editor [De XML-webeditor configureren en aanpassen](#id2065G300O5Z).

1. Nadat u alle vereiste updates hebt uitgevoerd, slaat u het bestand op en sluit u het **Globaal profiel**.


## Een profiel op mapniveau maken en configureren

Voer de volgende stappen uit om een profiel op mapniveau te configureren:

1. Meld u als beheerder aan bij Adobe Experience Manager.

1. Klik op de Adobe Experience Manager-koppeling bovenaan en kies **Gereedschappen**.

1. Selecteren **Hulplijnen** in de lijst met gereedschappen en klik op de knop **Mapprofielen** tegel.

   Voor het eerst wordt de pagina Mapprofielen alleen weergegeven met de standaardtegel Globaal profiel.

1. Klikken **Maken**.

   ![](assets/create-folder-profile.png){width="300" align="left"}

1. Voer de volgende gegevens in het dialoogvenster **Mapprofiel maken** dialoogvenster:
   - Naam van het mapprofiel.
   - Pad van de map waarin het profiel van toepassing is.

     >[!NOTE]
     >
     > U kunt geen meerdere mapprofielen toepassen op een map. Controleer of er geen ander profiel is toegepast op de map die u hier selecteert. In het geval van bovenliggende en onderliggende mappen met hun eigen specifieke profielen gebruikt de onderliggende map de configuraties van het eigen profiel. De configuraties in de bovenliggende map overschrijven de configuraties van een onderliggende map niet.

1. Klikken **Maken**.

   Er wordt een nieuwe tegel met de naam van het mapprofiel gemaakt op de pagina Mapprofielen

1. Klik op de tegel voor het mapprofiel die u wilt bewerken.

   Er wordt een tabblad Algemeen weergegeven met de naam van het mapprofiel en de geconfigureerde mapgegevens.

1. Klikken **Bewerken** om meerdere mappen en gebruikers toe te voegen die beheerrechten hebben om het mapprofiel te wijzigen.

   >[!NOTE]
   >
   > Gebruikers die u hier toevoegt, hebben de beheerdersrechten om de voorwaardelijke kenmerken, sjablonen en uitvoervoorinstellingen die voor dit mapprofiel zijn geconfigureerd, bij te werken.

1. Als u een map wilt toevoegen, klikt u op het pictogram Bladeren in het mappad, navigeert u naar een map en selecteert u deze. Klik vervolgens op Toevoegen om de map aan dit profiel toe te voegen.

   >[!NOTE]
   >
   > Controleer of aan de map die u hier kiest, geen ander mapprofiel is gekoppeld.

1. Om een gebruiker toe te voegen, selecteer een gebruiker van **Admin-gebruikers** vervolgkeuzelijst en klikken **Toevoegen**.

   >[!NOTE]
   >
   > U kunt vanuit de vervolgkeuzelijst meerdere gebruikers aan het mappenprofiel toevoegen. U kunt ook een bestaande beheerder uit de lijst verwijderen door op het pictogram Verwijderen naast de gebruikersnaam te klikken.

1. Nadat u alle vereiste mappen en gebruikers aan het mappenprofiel hebt toegevoegd, klikt u op **Opslaan**.


Nu kunt u de voorwaardelijke kenmerken, sjablonen, uitvoervoorinstellingen en de XML-editor configureren.

>[!IMPORTANT]
>
> Wanneer u een omslagprofiel creeert, door gebrek bevat het geen malplaatjes. U moet de vereiste sjablonen toevoegen aan het mappenprofiel om deze beschikbaar te maken voor de auteurs.

## Voorwaardelijke kenmerken voor algemene profielen of mapprofielen configureren {#id1889D0I305Z}

Voer de volgende stappen uit om standaard door DITA ondersteunde voorwaardelijke attributen op globaal of mapniveau te configureren:

1. Meld u aan bij Adobe Experience Manager als beheerder of als de gebruiker beheerdersrechten heeft voor een profiel op mapniveau.

1. Klik op de Adobe Experience Manager-koppeling bovenaan en kies **Gereedschappen**.

1. Selecteren **Hulplijnen** in de lijst met gereedschappen en klik op de knop **Mapprofielen** tegel.

1. Klik op de profieltegel die u wilt vormen.

   >[!NOTE]
   >
   > U kunt voorwaardelijke kenmerken configureren in het algemene profiel of in een mapprofiel.

1. Klik op de profielpagina op de knop **Voorwaardelijke kenmerken** tab.

1. Klikken **Bewerken**.

1. Klikken **Toevoegen**.

1. Voer de **Naam**, **Waarde** en **Label** voor het voorwaardelijke kenmerk.

   U kunt een profiel opslaan met alleen de kenmerknaam. Een kenmerk kan echter alleen worden gebruikt als er een waarde aan is opgegeven. Als u zowel - waarde als etiket voor een attribuut specificeert, toont de Redacteur van het Web het etiket van de voorwaardelijke attributen. Het label wordt ook weergegeven aan de publicatiebeheerder op het moment dat u een voorwaardelijke voorinstelling maakt.

   De volgende schermafbeelding toont de definitie voor de `platform` met mogelijke waarden en labels.

   ![](assets/add_profile.png)

1. Als u meer waarden voor hetzelfde kenmerk wilt toevoegen, klikt u op de knop **+** en voert u de extra waarde en het label in.

1. Klik op **Toevoegen**.

1. Klikken **Opslaan**.


Als u een aangepast kenmerk gebruikt, moet dit een geldig DITA-kenmerk zijn dat door het DTD-bestand wordt ondersteund. Als u om het even welk attribuut wilt gebruiken, dat geen standaardDITA attribuut is, dan voer de volgende extra stappen uit:

1. Voeg het aangepaste kenmerk toe aan het DTD-bestand. Als uw DTD-bestand bijvoorbeeld commonElements.mod is, moet u dit bestand zoeken in de map DTD. Het standaardpad van het systeem-DTD-bestand is:

   /libs/fmdita/dita\_resources/DITA-1.3/dtd/base/dtd/commonElements.mod

   >[!IMPORTANT]
   >
   > Het gespecialiseerde DTD-bestand moet onderdeel zijn van de implementatie van aangepaste code. DTD&#39;s onder /apps maken deel uit van de productimplementatie en worden daarom overschreven door de installatie van nieuwe releases. Het wordt aanbevolen gespecialiseerde DTD toe te voegen onder /var/dxml/dita\_resources in de projectmap en het pad DTD/catalogus op te nemen in het DITA-profiel.Voor meer informatie raadpleegt u [DITA-specialisatie integreren](dita-ot-specialization.md#id211MB0E00XA).

1. Gebruik Pakketbeheer om het bestand /libs/fmdita/config/condAttrList.xml te downloaden:

1. Maak een kopie van het bestand condAttrList.xml op de volgende locatie in de Git-opslagplaats van uw Cloud Manager:

   `/apps/fmdfmdita/config/condAttrList.xml`

1. Sla het bestand op.

1. Voeg aangepaste kenmerken toe aan het algemene profiel of aan het mapprofiel.


## Sjablonen configureren {#id1889D0IL0Y4}

AEM de Gidsen komen met 7 uit-van-de-doos onderwerpmalplaatjes, 2 DITA kaartmalplaatjes, en 3 malplaatjes van PDF. U kunt ervoor kiezen om slechts een paar sjablonen beschikbaar te hebben voor uw auteurs en uitgevers. Als u een douanemalplaatje gebruikt, kan het zelfde worden gevormd en ter beschikking gesteld voor creatie en het publiceren. U gebruikt de **Sjablonen** in de configuratie Mapprofielen om onderwerp-, kaart- of PDF-sjablonen toe te voegen aan of te verwijderen uit algemene profielen of uit profielen op mapniveau.

Zelfs alvorens het onderwerp, de kaart, of de malplaatjes van PDF op globaal of omslag-niveau te vormen, kunt u een plaats ook bepalen om uw douanesjablonen op te slaan. Om een douaneplaats te vormen om de malplaatjes op te slaan, zie [Aangepast pad voor DITA-sjabloonmap configureren](conf-template-tags-custom-dita-topic-template.md#id191LCF0095Z).

Voer de volgende stappen uit om het onderwerp, de kaart, of de malplaatjes van de PDF in een omslagprofiel toe te voegen:

1. Meld u aan bij Adobe Experience Manager als beheerder of als de gebruiker beheerdersrechten heeft voor een profiel op mapniveau.

1. Klik op de Adobe Experience Manager-koppeling bovenaan en kies **Gereedschappen**.

1. Selecteren **Hulplijnen** in de lijst met gereedschappen en klik op de knop **Mapprofielen** tegel.

1. Klik op de profieltegel die u wilt vormen.

   >[!NOTE]
   >
   > U kunt een sjabloon configureren in het algemene profiel of in een mapprofiel.

1. Klik op de profielpagina op de knop **Sjablonen** tab.
1. Klikken **Bewerken**.

   U krijgt de opties om de malplaatjes van het Onderwerp, van de Kaart, en van de PDF toe te voegen door van de standaardplaats te zoeken of te doorbladeren voor het.

   >[!NOTE]
   >
   > Door gebrek, worden alle malplaatjes opgeslagen in /content/dam/dita-templates omslag. De `dita-templates` map bevat `topics`, `maps`, en `PDF` submappen voor het opslaan van het onderwerp, de kaart en de sjablonen PDF. U kunt uw aangepaste sjablonen \(.dita, .xml of .ditamapfiles\) toevoegen in de standaardsjabloonmappen. Nadat u de sjabloon in de standaardmap hebt toegevoegd, kunt u deze toevoegen in het algemene profiel of in het mappenprofiel. Voor meer informatie over het creëren van douanesjablonen die de Redacteur van het Web gebruiken, zie [Aangepaste ontwerpsjabloon maken](#id1917D0EG0HJ).

   ![](assets/search-author-temp.png){width="800" align="left"}

1. Voeg het vereiste onderwerp, de kaart, en de malplaatjes van PDF aan uw profiel toe.

   Voer een van de volgende handelingen uit om een sjabloon toe te voegen:

   - Kies **Zoeken of typen** en voert u de naam van een sjabloon in of selecteert u deze in de vervolgkeuzelijst. De vervolgkeuzelijst bestaat uit alle standaardsjablonen en alle nieuwe sjablonen die u hebt gemaakt.

     ![](assets/default-template-list.png){width="800" align="left"}

   - Klikken **Bladeren** en selecteer een sjabloon van DAM.

1. Klikken **Toevoegen**.

   De geselecteerde sjablonen worden toegevoegd aan de sjabloonlijst.

   ![](assets/author-templ-added-list.png){width="800" align="left"}

   >[!NOTE]
   >
   > U kunt de volgorde van sjablonen wijzigen door deze naar de gewenste positie in de lijst te slepen. De positie van malplaatjes controleert de orde waarin zij in de pagina van de Vervaging in het onderwerp of de werkschema van de kaartverwezenlijking tonen.

1. Om de vertaalregels te plaatsen, doorblader de plaats SRX om de omslag te vinden die de SRX dossiers bevat. De indeling SRX \(Segmentation Rules eXchange\) is een standaard voor het uitwisselen van segmentatieregels tussen verschillende gebruikers en verschillende vertaalomgevingen. U kunt een map maken en uw aangepaste SRX-bestanden eraan toevoegen.

   Als u de map hebt gemaakt die de SRX-bestanden bevat, kunt u het mappad toevoegen aan het dialoogvenster **SRX-locatie voor vertaling** in uw mapprofiel.

   AEM de Gidsen kiezen de regels SRX volgens de brontaal van het vertaalproject. Het zoekt een douaneSRX dossier voor een taal, en als u geen douaneSRX dossier bepaalt, dan plukt het de regels zoals per uit de doos vertaalregels.

1. Klikken **Opslaan**.


Als u de sjablonen op een mapniveau-profiel hebt geconfigureerd, worden de geconfigureerde sjablonen gekoppeld aan de geconfigureerde map. Alle projecten die onder de gevormde omslag worden gecreeerd zullen toegang tot slechts die malplaatjes hebben die onder het omslag-vlakke profiel worden gevormd.

## Aangepaste ontwerpsjabloon maken {#id1917D0EG0HJ}

Met AEM hulplijnen kunt u eenvoudig ontwerpsjablonen maken. Als systeembeheerder, kunt u de Redacteur van het Web gebruiken om auteursmalplaatjes van kras tot stand te brengen. Vervolgens kunt u de nieuwe sjabloon toevoegen aan het algemene profiel of deze toewijzen aan een specifieke map met behulp van het mapspecifieke profiel.

Voer de volgende stappen uit om een aangepaste ontwerpsjabloon te maken:

1. Meld u als beheerder aan bij Adobe Experience Manager.

1. Navigeer in de interface Middelen naar de map die is geconfigureerd voor het opslaan van de sjabloonbestanden. Door gebrek, worden alle onderwerpmalplaatjes opgeslagen in /content/dam/dita-templates/topics omslag.

   >[!NOTE]
   >
   > Om een douaneplaats te vormen om onderwerp of kaartmalplaatjes op te slaan, zie [Aangepast pad voor DITA-sjabloonmap configureren](conf-template-tags-custom-dita-topic-template.md#id191LCF0095Z)

1. Klikken **Maken** \> **DITA-sjabloon**.

1. Voor de pagina van de Vervaging, selecteer het type van het DITA onderwerpmalplaatje dat u wilt tot stand brengen.

   >[!NOTE]
   >
   > U kunt de sjabloon Blanco gebruiken om helemaal opnieuw te beginnen. De lege sjabloon bevat geen structuur of elementen.

1. Klik op **Next**.

1. Voer op de nieuwe pagina Sjablooneigenschappen een **Titel**, **Naam**, en **Beschrijving** voor de sjabloon.

   >[!NOTE]
   >
   > De naam wordt automatisch voorgesteld gebaseerd op de Titel van uw malplaatje. Als u de naam handmatig wilt opgeven, dient u ervoor te zorgen dat de naam geen spaties, apostrof of accolades bevat en eindigt met .dita.

1. *\(Optioneel\)* Klik op de knop **Miniatuur toevoegen** naar de browser en selecteer een miniatuur die aan de sjabloon moet worden gekoppeld.

1. Klikken **Maken**.

   Het bericht Gemaakt onderwerp wordt weergegeven.

   U kunt verkiezen om het malplaatje voor het uitgeven in de Redacteur van het Web te openen, of het malplaatjedossier in de plaats van de malplaatjeopslag op te slaan. Zodra het malplaatje wordt gecreeerd, kunt u de Redacteur van het Web gebruiken om het malplaatje volgens uw auteursbehoeften aan te passen. Als een sjabloon eenmaal is ingesteld, moet u deze koppelen aan een algemeen profiel of aan een mapprofiel.


## Uitvoervoorinstellingen configureren {#id18AGD0IH0Y4}

In een typisch ondernemingsopstelling, zouden de verschillende outputmalplaatjes voor verschillende producten of gebruikersgidsen kunnen worden gebruikt. Ook kunnen er enkele gangbare productieproductieprocessen zijn die door alle uitgevers moeten worden gebruikt en een reeks specifieke productieprocessen voor een specifieke groep uitgevers of projecten.

Met AEM hulplijnen kan de beheerder uitvoervoorinstellingen maken met specifieke instellingen die vervolgens door alle of een specifieke set uitgevers kunnen worden gebruikt om uitvoer te genereren. De beheerder kan bijvoorbeeld één uitvoervoorinstelling maken om een gebruikershandleiding te genereren die voor alle uitgevers hetzelfde is. Een andere manier om de programmeergebruikershandleidingen te maken die specifiek zijn voor een aantal uitgevers. Beide voorinstellingen kunnen worden geconfigureerd voor het gebruik van verschillende uitvoersjablonen. In dit voorbeeld kan de algemene publicatievoorinstelling voor het genereren van de gebruikershandleiding op algemeen niveau worden geconfigureerd. En de uitvoervoorinstelling voor het genereren van de gebruikershandleiding voor programmering kan op mapniveau worden geconfigureerd.

Nadat de standaarduitvoervoorinstellingen in het systeem zijn gemaakt, worden voor alle DITA-kaarten die daarna worden gemaakt, de standaardvoorinstellingen gebruikt om uitvoer te genereren. Nochtans, zouden alle bestaande kaarten DITA de outputvoorinstellingen blijven gebruiken die vroeger met hen werden gevormd. Als u de nieuwe uitvoervoorinstelling wilt toepassen op alle bestaande DITA-toewijzingen, moet u de workflow voor het toepassen van vooraf ingestelde wijzigingen uitvoeren.

Naast de voorinstellingen die op algemeen of ondernemingsniveau zijn geconfigureerd, heeft een uitgever nog steeds de rechten om meer uitvoervoorinstellingen te maken. Deze voorinstellingen zijn echter gekoppeld aan de DITA-kaart waarvoor ze zijn gemaakt. Zie voor meer informatie over het maken van reguliere uitvoervoorinstellingen voor een DITA-kaart *Een uitvoervoorinstelling maken, bewerken, dupliceren of verwijderen* in de as a Cloud Service handleiding Adobe Experience Manager-hulplijnen gebruiken.

Voer de volgende stappen uit om algemene of mapspecifieke uitvoervoorinstellingen te configureren:

1. Meld u aan bij Adobe Experience Manager als beheerder of als de gebruiker beheerdersrechten heeft voor een mapspecifiek profiel.

1. Klik op de Adobe Experience Manager-koppeling bovenaan en kies **Gereedschappen**.

1. Selecteren **Hulplijnen** in de lijst met gereedschappen en klik op de knop **Mapprofielen** tegel.

1. Klik op de profieltegel die u wilt vormen.

   >[!NOTE]
   >
   > U kunt uitvoervoorinstellingen configureren in het algemene profiel of in een mapspecifiek profiel.

1. Op de profielpagina. klik op de **Voorinstellingen uitvoer** tab.

   Er wordt een lijst weergegeven met uitvoervoorinstellingen die buiten de doos vallen, waaronder Site, PDF, HTML5, EPUB en AANGEPAST.

1. Voer een van de volgende handelingen uit om een uitvoervoorinstelling te maken of te bewerken:

   - Klikken **Maken** om een nieuwe voorinstelling voor de uitvoer te maken.
   - Klik op Dupliceren om een kopie van de geselecteerde uitvoervoorinstelling te maken. U kunt wijzigingen aanbrengen in de gedupliceerde voorinstelling en deze opslaan.

   - Klikken **Bewerken** om de configuratie van de geselecteerde voorinstelling te openen en te bewerken.

     Zie voor informatie over instellingen van uitvoervoorinstellingen *Uitvoervoorinstellingen* in de as a Cloud Service handleiding Adobe Experience Manager-hulplijnen gebruiken.

1. Klikken **Opslaan** om de voorinstellingen op te slaan.


Alle DITA-kaarten die u daarna maakt of uploadt, hebben de nieuwe of bijgewerkte uitvoervoorinstelling.

## Vooraf ingestelde wijzigingen toepassen {#id18AGD0K0OHS}

Een nieuwe uitvoervoorinstelling die op algemeen niveau wordt gemaakt, wordt beschikbaar gesteld voor alle nieuwe DITA-kaarten die u in de toekomst maakt. Als er een nieuwe uitvoervoorinstelling wordt gemaakt op mapniveau, wordt die voorinstelling beschikbaar gemaakt voor alle mappen die worden gemaakt in de geconfigureerde map. Standaard wordt een nieuwe voorinstelling voor uitvoer niet beschikbaar gemaakt voor bestaande DITA-kaarten.

Als u een bestaande uitvoervoorinstelling hebt bijgewerkt of als u een nieuwe uitvoervoorinstelling beschikbaar wilt maken voor bestaande DITA-kaarten, voert u de volgende stappen uit:

1. Meld u aan bij Adobe Experience Manager als beheerder of als de gebruiker beheerdersrechten heeft voor een mapspecifiek profiel.

1. Klik op de Adobe Experience Manager-koppeling bovenaan en kies **Gereedschappen**.

1. Selecteren **Hulplijnen** in de lijst met gereedschappen en klik op de knop **Mapprofielen** tegel.

1. Klik op de profieltegel die u wilt vormen.

   >[!NOTE]
   >
   > U kunt uitvoervoorinstellingen configureren in het algemene profiel of in een mapspecifiek profiel.

1. Op de profielpagina. klik op de **Voorinstellingen uitvoer** tab.

   Er wordt een lijst weergegeven met uitvoervoorinstellingen die buiten de doos vallen, waaronder Site, PDF, HTML5, EPUB en AANGEPAST.

1. Selecteer de uitvoervoorinstelling die u wilt toepassen op bestaande DITA-maps.

1. Klikken **Wijzigingen voorinstelling toepassen** in de hoofdwerkbalk.

1. In het dialoogvenster Wijzigingen voorinstelling toepassen kunt u kiezen uit:

   - **De optie Bestaande voorinstelling overschrijven selecteren**: Als u deze optie selecteert, worden de instellingen in alle bestaande DITA-kaarten waarin de voorinstelling wordt gebruikt, overschreven door updates die u hebt gemaakt in de bestaande uitvoervoorinstellingen. Dit leidt echter tot het verlies van bestaande voorwaardelijke voorinstellingen en basislijngegevens die bij de kaart horen.

   - **De optie Bestaande voorinstelling overschrijven niet selecteren**: Als u deze optie niet selecteert, hebben updates die u hebt gemaakt in de bestaande uitvoervoorinstellingen geen invloed op de bestaande DITA-kaarten. Alleen de zojuist toegevoegde voorinstellingen worden toegevoegd aan de bestaande DITA-kaarten. De nieuwe DITA-kaart krijgt beide functies: de bijgewerkte uitvoervoorinstellingen en de nieuw toegevoegde voorinstellingen.

1. Klikken **OK** om wijzigingen toe te passen uit de geselecteerde uitvoervoorinstellingen op alle bestaande DITA-kaarten.



## Slimme suggesties op basis van AI configureren in de webeditor {#conf-ai-smart-suggestions}

Voor ![AEM ](assets/aem-cloud-icon.svg) Experience Manager-hulplijnen as a Cloud Service.

U kunt de op AI-Gebaseerde Slimme Suggesties vormen en de auteurs helpen de bestaande inhoud hergebruiken en gemakkelijk correcte en verenigbare inhoudsverwijzingen creëren. De **AI-configuratie** kunt u de instellingen van het deelvenster Slimme suggesties in de webeditor bepalen.

Voer de volgende stappen uit om standaardAI configuratie op het globale of omslag-vlakke profiel te vormen:
1. Meld u aan bij Adobe Experience Manager als beheerder of gebruiker met beheerdersrechten voor een profiel op mapniveau.
1. Selecteer de **Adobe Experience Manager** koppeling bovenaan en kies **Gereedschappen**.
1. Selecteren **Hulplijnen** in de lijst met gereedschappen en selecteer de **Mapprofielen** tegel.
1. Selecteer de profieltegel die u wilt vormen.

   >[!NOTE]
   >
   >U kunt op AI gebaseerde slimme suggesties aan het globale of een omslag-niveau profiel vormen.

1. Selecteer op de profielpagina de optie **AI-configuratie** tab.
   ![Tabblad AI-configuratie in algemeen profiel](assets/global-profile-AI-configuration-cs.png) {width="800" align="left"}

1. Klikken **Bewerken**.
1. Als beheerder kunt u de volgende instellingen configureren:

   **Minimum aantal tekens**: Voer het minimale aantal tekens in dat de auteurs moeten invoeren om de suggesties te krijgen. Als dit getal bijvoorbeeld 7 is, moet de auteur ten minste 7 tekens toevoegen om een slimme suggestie weer te geven.

   **Maximumaantal suggesties**: Voer het maximum aantal suggesties in dat de auteurs kunnen ophalen tijdens het ontwerpen van de inhoud. Als dit getal bijvoorbeeld 5 is, kan de auteur maximaal vijf slimme suggesties weergeven.

   **Bestanden en mappen**: Selecteer de bestanden of mappen waaruit de slimme suggesties moeten worden weergegeven. *Voor de consistentie van de inhoud is het raadzaam dat er geen twee items in de lijst gemeenschappelijke bestanden hebben*. Nadat u de bestanden en mappen hebt geselecteerd, worden deze weergegeven.

1. Klikken **Opslaan**.

   >[!NOTE]
   >
   > De laatste geïndexeerde statusdetails worden bovenaan weergegeven nadat u het bestand hebt opgeslagen.

Meer informatie over weergeven en toevoegen [Slimme suggesties op basis van AI](../user-guide/authoring-ai-based-smart-suggestions.md) om inhoudsverwijzingen toe te voegen terwijl het ontwerpen in de Redacteur van het Web.

## De XML-webeditor configureren en aanpassen {#id2065G300O5Z}

Door gebrek, komt de Redacteur van het Web van XML met veel eigenschappen om uw auteurs te helpen DITA documenten tot stand brengen. Als u in een restrictieve omgeving werkt, kunt u kiezen welke functies aan uw auteurs worden blootgesteld. Het lusje van de Configuratie van de Redacteur van XML staat u toe om de eigenschappen gemakkelijk te controleren en ook het blik-en-gevoel van uw Redacteur van het Web te veranderen. Als beheerder, kunt u de volgende componenten van de Redacteur van het Web aanpassen:

**UI-configuratie XML-editor**

Deze instelling bepaalt de werkbalk en de andere gebruikersinterface-elementen van de webeditor. Klik op het pictogram Downloaden om het bestand ui\_config.json op uw lokale systeem te downloaden. Vervolgens kunt u het bestand wijzigen en het bestand uploaden. Afhankelijk van de plaats waar u het bestand uploadt op, algemeen profiel of mapniveau, worden de wijzigingen dienovereenkomstig toegepast. Voor meer informatie over hoe u de XML-editor kunt aanpassen met het bestand ui\_config.json raadpleegt u [Werkbalk Aanpassen](conf-web-editor-customize-toolbar.md#).

**CSS-sjabloonlay-out**

Download het bestand dat in deze sectie beschikbaar is om de vormgeving van uw document aan te passen wanneer een voorvertoning van het document wordt weergegeven of wanneer het document wordt geopend voor bewerking in de webeditor. Het standaard CSS-bestand dat kan worden gedownload, is slechts een testbestand dat niet mag worden gebruikt voor aanpassing. U kunt een CSS dossier met aanpassingen voor de Redacteur van het Web tot stand brengen en het zelfde uploaden. U kunt bijvoorbeeld een CSS-bestand maken met de volgende code:

```
.title {    font-size: 9em;}
```

Sla dit bestand op en upload het in de sectie CSS-sjabloonlay-out. De volgende keer dat u het bestand downloadt, wordt het meest recente CSS-bestand gebruikt in de webeditor.

**XML-editorfragmenten**

Met behulp van het configuratiebestand in deze sectie kunt u enkele standaardfragmenten maken en deze delen met uw auteurs. De standaardstructuur van het bestand wordt hieronder gegeven:

```
{
   "snippetID": {
      "name": "snippet Name",
      "description": "snippet Description",
      "value": "<i>this is snippet value</i>"
  }
}
```

U moet de volgende gegevens opgeven om een fragment te maken:

snippetID : Een unieke id voor het fragment. Dit kan een alfanumerieke waarde hebben.

name : Een beschrijvende naam om het fragment te identificeren. Deze naam wordt weergegeven in het paneel Fragmenten.

beschrijving: voeg een beschrijvende informatie voor het fragment toe.

value : geef de XML-code van het fragment op.

>[!NOTE]
>
> U kunt meer fragmenten toevoegen door een komma \(,\) aan het einde van de fragmentdefinitie toe te voegen en dezelfde structuur voor het volgende fragment te herhalen.

**Versielabels voor XML-inhoud**

Auteurs kunnen standaard zelf labels maken en deze koppelen aan hun onderwerpbestanden. Nochtans, kan dit tot vele variaties van het zelfde etiket leiden, bijvoorbeeld zou &quot;Versie 1.0&quot;, &quot;Versie-1.0&quot;, &quot;versie 1&quot;etiketten voor het identificeren van het zelfde stadium van een onderwerp kunnen hebben. Om dergelijke inconsistente etikettering in het systeem te voorkomen, kunt u een vooraf gedefinieerde lijst met labels maken waaruit auteurs kunnen kiezen. Dankzij consistente labels kunt u bestanden beter beheren in uw systeem.

Met de configuratie van het versielabel kunt u een lijst met geldige labels voor uw organisatie uploaden. Download het standaard label.json-bestand en wijzig het bestand zoals hieronder wordt weergegeven:

```
{
"label1":"Draft",
"label2":"PM-Review",
"label3":"Engg-Review",
"label4":"QE-Review",
"label5":"Ready for Loc",
"label6":"Ready for Publish"
}
```

In het bovenstaande voorbeeld is &quot;label1&quot; de id voor de labelvolgorde en wordt het toegevoegd door het label dat wordt weergegeven aan de auteurs waar een label is vereist. Sla dit bestand op en upload het in de sectie Labels voor XML-inhoudsversie.

>[!IMPORTANT]
>
> Gebruikers moeten het profiel selecteren onder hun gebruikersvoorkeuren in de webeditor om configuraties op mapniveau van kracht te laten worden.

**Rootmap**

Als uw auteurs met een specifieke wortelkaart werken, dan kunt u doorbladeren aan en die rootmap hier selecteren. U kunt de routekaart alleen definiëren voor een mapprofiel.
