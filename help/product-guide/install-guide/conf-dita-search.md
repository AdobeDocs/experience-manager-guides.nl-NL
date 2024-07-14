---
title: Zoeken naar gebruikersinterface van AEM Assets configureren
description: Leer hoe u zoekopdrachten voor de gebruikersinterface van AEM Assets kunt configureren
exl-id: b920ba7f-e8fc-4af6-aa8a-b8516b1cffc0
feature: Search Configuration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '1695'
ht-degree: 0%

---

# Zoeken naar gebruikersinterface van AEM Assets configureren {#id192SC800MY4}

AEM herkent standaard geen DITA-inhoud, waardoor het geen mechanisme biedt om DITA-inhoud in de opslagplaats te doorzoeken. Met AEM Guides kunt u de zoekfunctie voor DITA-inhoud toevoegen aan AEM opslagplaats.

AEM herkent standaard geen DITA-inhoud, waardoor het geen mechanisme biedt om DITA-inhoud in de opslagplaats te doorzoeken. Er is ook geen OOTB-mogelijkheid om inhoud te zoeken op basis van hun UUID. Met AEM Guides kunt u de zoekfunctie voor DITA-inhoud en zoekmogelijkheden op basis van UUID toevoegen aan de AEM-opslagplaats.

Het vormen van DITA inhoudsonderzoek impliceert de volgende taken:

1. [DITA Element-zoekcomponent toevoegen in Assets UI](#id192SF0F50HS)
1. [Op UUID gebaseerde zoekcomponent toevoegen in gebruikersinterface van Assets](#id2034F04K05Z)
1. [Rechten aan gebruikers opgeven](#id192SF0G0RUI)
1. [Aangepaste elementen of kenmerken toevoegen in zoekopdracht](#id192SF0G10YK)
1. [Metagegevens uit bestaande inhoud extraheren](#id192SF0GA0HT)

Naast het toevoegen van onderzoeksvermogen, kunt u de omslagen ook vormen die niet in het onderzoek zouden moeten worden omvat. Voor meer details, zie [ Tijdelijke dossiers van onderzoeksresultaten uitsluiten ](#id197AHI0035Z).

## DITA Element-zoekcomponent toevoegen in Assets UI {#id192SF0F50HS}

Ga als volgt te werk om een zoekcomponent voor DITA-inhoud toe te voegen in de gebruikersinterface van AEM Assets:

1. Meld u als beheerder aan bij Adobe Experience Manager.

1. Klik op de **verbinding van Adobe Experience Manager** bij de bovenkant en kies **Hulpmiddelen**.

1. Selecteer **Algemeen** van de lijst van hulpmiddelen en klik op de **tegel van Forms van het Onderzoek**.

1. In de **lijst van het Onderzoek Forms**, selecteer de **Spoorweg van het Onderzoek van Admin van Assets**.

1. Klik **uitgeven**.
1. In **Uitgezochte Predicate** tabel, rol aan het eind van de lijst.

1. De belemmering-en-daling **Predicate van het Element DITA** bij de vereiste plaats in de onderzoeksvorm.

   ![](assets/drag-search-predicate.png){width="650" align="left"}

1. Klik **Gedaan** om uw veranderingen te bewaren.

   Wanneer u tot de optie van Filters in Assets UI toegang hebt, zult u de het onderzoek het filtreren optie van het Element DITA krijgen.

   ![](assets/search-filter-asset-console.png){width="350" align="left"}


## Op UUID gebaseerde zoekcomponent toevoegen in gebruikersinterface van Assets {#id2034F04K05Z}

Voer het volgende uit om op UUID-Gebaseerde onderzoekscomponent in AEM Assets UI toe te voegen:

1. Meld u als beheerder aan bij Adobe Experience Manager.

1. Klik op de **verbinding van Adobe Experience Manager** bij de bovenkant en kies **Hulpmiddelen**.

1. Selecteer **Algemeen** van de lijst van hulpmiddelen en klik op de **tegel van Forms van het Onderzoek**.

1. In de **lijst van het Onderzoek Forms**, selecteer de **Spoorweg van het Onderzoek van Admin van Assets**.

1. Klik **uitgeven**.
1. In **Uitgezochte Predicate** lusje, kies **Voorkeur van het Bezit** en belemmering-en-daling het bij de vereiste plaats in de onderzoeksvorm.

1. In het **lusje van Montages**, verstrek de volgende details voor de onlangs toegevoegde **Predicate** component van het Bezit:

   - **Etiket van het Gebied**: UUID
   - **Naam van het Bezit**: jcr:content/fmUuid
1. Klik **Gedaan** om uw veranderingen te bewaren.

   Wanneer u de optie Filters opent in de gebruikersinterface van Assets, krijgt u de optie voor het filteren van UIS-zoekopdrachten.


## Rechten aan gebruikers opgeven {#id192SF0G0RUI}

Auteurs en uitgevers moeten expliciete machtigingen krijgen om toegang te krijgen tot de zoekmogelijkheden via de gebruikersinterface van Assets. Als u deze toestemmingen niet verleent, dan zullen uw gebruikers niet inhoud kunnen zoeken DITA die op hun element/attributenwaarden of UUID wordt gebaseerd.

Voer de volgende stappen uit om toegang tot de eigenschap van het Onderzoek te verlenen DITA:

1. Open de pagina met gebruikers- en groepsmachtigingen. De standaard-URL voor toegang tot de pagina is:

   `http://<server name>:<port>/useradmin.html`

1. Zoek naar de gebruikersgroep of een individuele gebruiker aan wie u toegang wilt verlenen. Bijvoorbeeld, om toegang tot alle gebruikers in auteursgroep te verlenen, ga auteurs op het **gebied van de Vraag van de Filter** in en druk **binnengaan**.

   ![](assets/authors-group-permission.png){width="350" align="left"}

1. Selecteer de **auteurs** groep.

1. In de juiste ruit, selecteer de **Toestemmingen** tabel.

1. Navigeer naar de volgende maplocatie:

   /conf/global/settings/dam/search

1. Geef **Gelezen** toestemming op de onderzoeksomslag.

   ![](assets/read-permission-authors.png){width="650" align="left"}

1. Klik **sparen**.


De geselecteerde gebruiker of gebruikersgroep heeft nu toegang tot de zoekfunctie voor DITA-inhoud in de gebruikersinterface van Assets.

## Aangepaste elementen of kenmerken toevoegen in zoekopdracht {#id192SF0G10YK}

De DITA-zoekopdracht werkt alleen als de DITA-inhoud vooraf is verwerkt. Deze preprocessing stap haalt selectieve inhoud uit individuele kaarten DITA en onderwerpen zodat het voor sneller het zoeken kan worden geïndexeerd. Intern, wordt dit proces genoemd *Rangschikking*. Serienummering van DITA-bestanden vindt plaats tijdens het uploaden van inhoud of kan ook op aanvraag worden uitgevoerd. Het gebruikt een configuratiedossier om te bepalen hoeveel inhoud van elk DITA- dossier zou moeten worden geïndexeerd. De standaardlocatie van het serialisatiebestand is:

/libs/fmdita/config/serializationconfig.xml

De standaardonderzoeksconfiguratie staat u toe om naar alle elementen en attributen binnen het element te zoeken DITA `prolog`. Als u op basis van andere elementen of attributen wilt zoeken, dan moet u het dossier van de onderzoeksrangschikking vormen.

>[!NOTE]
>
> Als u met de standaardonderzoeksconfiguratie binnen het `prolog` element wilt gaan, dan kunt u dit proces overslaan.

Dit bestand bevat twee hoofdsecties: een kenmerkset en een regelset. Hieronder ziet u een fragment van de sectie voor regelsets:

```XML
<ruleset filetypes="xml dita"><!-- Element rules --><rule xpath="//[contains(@class, 'topic/topic')]/[contains(@class, 'topic/prolog')]//*[not(*)]" text="yes" attributeset="all-attrs" /><!-- Attribute rules --><rule xpath="//[contains(@class, 'topic/topic')]/[contains(@class, 'topic/prolog')]///@[local-name() != 'class']" /></ruleset>
```

In het gedeelte Regelset kunt u het volgende opgeven:

- Regels om de elementen te extraheren

- Regels voor het uitnemen van kenmerken


Een regel bestaat uit het volgende:

xpath
:   Dit is de vraag van XPath die de elementen of de attributen van DITA- dossiers terugwint. De standaardconfiguratie voor de elementregel haalt alle `prolog` -elementen op. En de standaardconfiguratie voor de kenmerkregel haalt alle kenmerken van `prolog` -elementen op. U kunt een vraag van XPath specificeren om de elementen of de attributen in series te vervaardigen die u wilt zoeken.

De XPath-query bevat de klassenaam van het documenttype. De `topic/topic` -klasse wordt gebruikt voor DITA-onderwerpdocumenten. Als u een regel wilt maken voor andere DITA-documenten, moet u de volgende klassenamen gebruiken:

| Documenttype | Klassenaam |
|-------------|----------|
| Onderwerp | - onderwerp/onderwerp |
| Taak | - onderwerp/onderwerp/taak |
| Concept | - onderwerp/onderwerp/concept |
| Referentie | - onderwerp/onderwerpverwijzing/verwijzing |
| Kaart | - kaart/kaart |

text
:   Als u naar de tekst binnen het gespecificeerde element wilt zoeken, dan specificeer ja waarde. Als u geen waarde opgeeft, worden alleen de kenmerken in het element geserialiseerd. De kenmerken waarnaar u wilt zoeken, moeten worden opgegeven in de sectie voor kenmerksets.

attributeset
:   Geef de id op van de kenmerkset die u aan deze regel wilt koppelen. De waarde alle-attrs is een speciaal geval om erop te wijzen dat alle attributen voor deze regel in series moeten worden vervaardigd.

Een kenmerkset bevat een lijst met kenmerken die u wilt zoeken binnen DITA-inhoud. De kenmerkenreeks bevat het volgende:

id
:   Een unieke id voor de kenmerkset. Deze id wordt opgegeven in de parameter attributeset van een regelset.

attribute
:   Een lijst met kenmerken die u wilt doorzoeken. Voor elk kenmerk moet u een afzonderlijk item maken in het element `attribute` .

Voer de volgende stappen uit om aangepaste DITA-elementen of -kenmerken toe te voegen in het bestand met zoekserienummering:

1. Meld u aan bij AEM en open de modus CRXDE Lite.

1. Navigeer naar het configuratiebestand voor serienummering dat beschikbaar is op de volgende locatie:

   /libs/fmdita/config/serializationconfig.xml

1. Maak een overlayknooppunt van de map `config` in het knooppunt `apps` .

1. Navigeer naar het configuratiebestand dat beschikbaar is in het knooppunt `apps` :

   `/apps/fmdita/config/serializationconfig.xml`

1. Voeg de vereiste element- of kenmerkregelsets toe.

1. Sla het bestand op.

1. Open de Adobe Experience Manager Web Console Configuration-pagina. De standaard-URL voor toegang tot de configuratiepagina is:

   http://&lt;servernaam\>:&lt;poort\>/system/console/configMgr

1. Onderzoek naar en klik op *com.adobe.fmdita.config.ConfigManager* bundel.

1. Klik **sparen**.


De nieuwe rangschikkingsinformatie wordt opgeslagen en geactiveerd voor onderzoek. U moet de metagegevens echter extraheren uit uw bestaande DITA-inhoud om deze beschikbaar te maken voor zoekopdrachten.

## Metagegevens uit bestaande inhoud extraheren {#id192SF0GA0HT}

Zodra u om het even welke verandering in het standaard dossier van de onderzoeksrangschikking hebt aangebracht, moet u de optie van de Extractie van Meta-gegevens DITA in de {*bundel 0} toelaten com.adobe.fmdita.config.ConfigManager en dan het werkschema in werking stellen om meta-gegevens te halen.* Hiermee haalt u de vereiste metagegevens uit de bestaande DITA-bestanden en wordt hetzelfde vervolgens beschikbaar gesteld voor zoekopdrachten.

Als u nieuwe bestanden maakt of een bestand bewerkt nadat u het serialisatiebestand hebt bijgewerkt, worden de metagegevens automatisch uit dergelijke bestanden geëxtraheerd. Het uitpakken van metagegevens is alleen vereist voor bestanden die al in de AEM opslagplaats bestaan.

Het uitpakken van meta-gegevens uit bestaande DITA- dossiers impliceert twee taken:

1. De optie voor het extraheren van metagegevens inschakelen in configMgr
1. De workflow voor het uitnemen van metagegevens uitvoeren

Voer de volgende stappen uit om de optie van de meta-gegevensextractie in configMgr toe te laten:

1. Open de Adobe Experience Manager Web Console Configuration-pagina. De standaard-URL voor toegang tot de configuratiepagina is:

   http://&lt;servernaam\>:&lt;poort\>/system/console/configMgr

1. Onderzoek naar en klik op *com.adobe.fmdita.config.ConfigManager* bundel.

1. Selecteer **toelaten de optie van de Meta-gegevens van DITA van de Extractie**.

1. Klik **sparen**.


Voer de volgende stappen uit om de workflow voor het uitnemen van metagegevens uit te voeren:

1. Meld u als beheerder aan bij Adobe Experience Manager.

1. Klik op de **verbinding van Adobe Experience Manager** bij de bovenkant en kies **Hulpmiddelen**.

1. Selecteer **Gidsen** van de lijst van hulpmiddelen en klik de **3} tegel van de Extractie van Metagegevens DITA {.**

1. Als u meta-gegevens uit één enkel dossier en zijn gebiedsdelen wilt halen, klik **Uitgezocht een verbinding van het Dossier** en doorblader voor een dossier.

1. Als u meta-gegevens van veelvoudige dossiers binnen een omslag wilt halen, klik **Uitgezochte Omslag \(s \)** verbinding, doorblader en selecteer de vereiste omslag. Klik **toevoegen** knoop om de omslag aan de lijst van de serialisatietaak toe te voegen.

   >[!NOTE]
   >
   > U kunt meerdere mappen selecteren en toevoegen aan een serialisatietaak.

1. Klik **Begin**.

1. In de Bevestig de dialoog van de Extractie van Meta-gegevens, klik **O.K.**.


## Tijdelijke bestanden uitsluiten van zoekresultaten {#id197AHI0035Z}

Standaard wordt de zoekopdracht uitgevoerd op de gehele opslagplaats van AEM. Er kunnen locaties zijn die u wilt uitsluiten van de zoekopdracht. Wanneer u bijvoorbeeld de workflow voor het vertalen van inhoud start, blijven de niet-goedgekeurde bestanden op een tijdelijke maplocatie staan. Wanneer u de zoekopdracht uitvoert, worden ook bestanden van deze tijdelijke locatie geretourneerd in de zoekresultaten.

Als u wilt voorkomen dat AEM Guides de locatie van de tijdelijke vertaalmap doorzoekt, moet u een tijdelijke maplocatie toevoegen aan de lijst met uitsluitingen.

Voer de volgende stappen uit om de tijdelijke vertaalmap uit te sluiten van de zoekopdracht:

>[!NOTE]
>
> Met deze procedure kunt u elke andere maplocatie aan de lijst met uitsluitingen toevoegen.

1. Meld u aan bij AEM en open de modus CRXDE Lite.

1. Navigeer naar de damAssetLucene-node die beschikbaar is op de volgende locatie:

   /eak:index/damAssetLucene

1. Voeg de volgende eigenschap toe aan het knooppunt damAssetLucene:

   | Eigenschapnaam | Type | Waarde |
   |-------------|----|-----|
   | excludePaths | Tekenreeks\[\] | Voeg de volgende waarde toe aan deze eigenschap: <br> /content/dam/projects/conversion\_output |

1. Navigeer naar het lucene knooppunt dat beschikbaar is op de volgende locatie:

   /oak:index/lucene

1. Voeg de volgende eigenschap toe aan het knooppunt lucene:

   | Eigenschapnaam | Type | Waarde |
   |-------------|----|-----|
   | excludePaths | Tekenreeks\[\] | Voeg de volgende waarden toe aan deze eigenschap: <br><ul><li>/var/dxml</li><li>/content/dam/projects/vertaling\_output</li></ul> |
