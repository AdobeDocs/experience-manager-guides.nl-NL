---
title: Instellingen voor uitvoergeneratie configureren
description: Leer hoe u instellingen voor uitvoergeneratie configureert
exl-id: 6df31e3c-683c-4188-b917-9c1855d9b95b
feature: Output Generation
role: Admin
level: Experienced
source-git-commit: 6e23f52fc9124d0f07f8108da1b5fe574f553469
workflow-type: tm+mt
source-wordcount: '5756'
ht-degree: 0%

---

# Instellingen voor uitvoergeneratie configureren {#id181AI0B0E30}

AEM Guides wordt geleverd met veel configuratieopties waarmee u het productieproces voor uitvoer kunt aanpassen. Dit onderwerp behandelt alle configuraties en aanpassingen die u aan opstelling uw proces van de outputgeneratie zouden helpen.

## Het tabblad Basislijn op het dashboard voor de DITA-kaart configureren {#id223MD0D0YRM}

U kunt het tabblad Basislijn dat beschikbaar is op het dashboard voor de kaart configureren en verbergen.

De **optie van het Lusje van de Basislijn van de Verbergen** wordt niet toegelaten door gebrek en u moet dit van configMgr toelaten. Voer de volgende stappen uit om de optie door gebrek in de Redacteur van het Web toe te laten:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.config.ConfigManager** bundel.

1. Selecteer de **optie van het Lusje van de Basislijn van de Verbergen**.

1. Klik **sparen**.

   >[!NOTE]
   >
   > Deze configuratie is standaard uitgeschakeld en het tabblad Basislijn is beschikbaar op het kaartdashboard.


## FrameMaker Publishing Server configureren {#id1678G0Z0TN6}

U kunt FrameMaker Publishing Server \(FMPS\) gebruiken om uitvoer voor uw DITA-inhoud te genereren. Als u FMPS configureert, kunt u uitvoer genereren in meerdere indelingen die worden ondersteund door FMPS.

>[!NOTE]
>
> Als u uitvoer wilt genereren met FMPS, moet u de FMPS-server hebben ingesteld. Zie de FrameMaker Publishing Server User Guide (Handleiding voor) voor installatie- en configuratiegegevens.

Als u AEM Guides wilt configureren voor het gebruik van FMPS, werkt u de volgende eigenschappen van de `com.adobe.fmdita.config.ConfigManager` -bundel bij in de webconsole.

>[!NOTE]
>
> Ga naar http://&lt;servernaam\>:&lt;poort\>/system/console/configMgr URL om de webconsole te openen.

| Eigenschap | Beschrijving |
|--------|-----------|
| FrameMaker Publishing Server-aanmeldingsdomein | Geef de domeinnaam of de naam van de werkgroep op waarop de FrameMaker Publishing Server wordt gehost. Op basis van de FMPS-versie geeft u de domeinnaam op als :-   **FMPS 2020**: IP adres als 192.168.1.101 <br> - **FMPS 2019 en vroeger**: IP adres of de domeinnaam |
| FRAMEMAKER PUBLISHING SERVER URL | Geef de URL van de FrameMaker Publishing Server op. Gebaseerd op de versie FMPS, verstrek FMPS URL als:<br> - **FMPS 2020**: `http://<fmps_ip>:<port>` \ (http://192.168.1.101:7000 \) <br> - **FMPS 2019 en vroeger**: `http://<fmps_ip>:<port>/fmserver/v1/` |
| FMPS-versie | Geef het versienummer van de FrameMaker Publishing Server op. Gebaseerd op de versie FMPS, verstrek de versieinformatie als: <br> - **FMPS 2020**: 2020 <br> - **FMPS 2019 en vroeger**: 2019 of 2017 |
| FrameMaker Publishing Server gebruikersnaam en wachtwoord | Geef de gebruikersnaam en het wachtwoord op voor toegang tot de FrameMaker Publishing Server. |
| FMPS-timeout | \ (*Facultatief* \) specificeer de tijd \ (in seconden \) waarvoor AEM Guides op een reactie van FrameMaker Publishing Server wacht. Als er geen reactie is ontvangen binnen de opgegeven tijd, wordt de publicatietaak beëindigd en wordt de taak gemarkeerd als mislukt. <br> Standaardwaarde: 300 seconden \(5 minuten\) |
| Externe AEM URL | *\(Optioneel\)* De AEM-URL waar de FrameMaker Publishing Server de gegenereerde uitvoerbestanden plaatst. Bijvoorbeeld `http://<server-name>:<port>/` . |
| AEM Admin-gebruikersnaam en -wachtwoord | *\(Optioneel\)* De gebruikersnaam en het wachtwoord voor een beheerder van uw AEM-instelling. Dit wordt door FrameMaker Publishing Server gebruikt om te communiceren met AEM. |
| Time-out voor FMPS-taakuitvoering | Deze instelling is alleen van toepassing voor FMPS 2020. Geef de tijd op \(in seconden\) waarna FMPS stopt met wachten tot dit proces wordt uitgevoerd. |

## Overvloeien publiceren configureren binnen een bestaande AEM-site {#id1691I0V0MGR}

Als u een AEM-site hebt die DITA-inhoud bevat, kunt u uw AEM-site-uitvoer zo configureren dat DITA-inhoud wordt gepubliceerd naar een vooraf gedefinieerde locatie op uw site. In de volgende schermafbeelding van een AEM Site-pagina is het knooppunt `ditacontent` bijvoorbeeld gereserveerd voor het opslaan van DITA-inhoud:

![](assets/publish-in-aem-site.png){width="300" align="left"}

De resterende knooppunten op de pagina worden rechtstreeks vanuit de AEM Site-editor gemaakt. Als u de publicatie-instelling configureert voor het publiceren van DITA-inhoud op een vooraf gedefinieerde locatie, weet u zeker dat geen van uw bestaande niet-DITA-inhoud wordt gewijzigd door het AEM Guides-publicatieproces.

U moet de volgende configuraties op uw bestaande plaats uitvoeren om het publiceren van inhoud DITA aan een vooraf bepaalde knoop toe te staan:

- De sjablooneigenschappen van uw site configureren

- Knooppunten op uw site toevoegen om DITA-inhoud te publiceren


Voer de volgende stappen uit om de sjablooneigenschappen van uw bestaande site te configureren:

1. Meld u aan bij AEM en open de CRXDE Lite-modus.

1. Navigeer naar het sjabloonconfiguratieknooppunt van uw site. AEM Guides slaat bijvoorbeeld de standaardsjabloonconfiguraties op in het volgende knooppunt:

   `/libs/fmdita/config/templates/default`

   >[!NOTE]
   >
   > Breng geen aanpassingen aan in de standaardconfiguratiebestanden in het knooppunt `libs` . U moet een overlay van het knooppunt `libs` in het knooppunt `apps` maken en de vereiste bestanden alleen in het knooppunt `apps` bijwerken.

1. Voeg de volgende eigenschappen toe:

   | Eigenschapnaam | Type | Waarde |
   |-------------|----|-----|
   | `topicContentNode` | String | Geef de knooppuntnaam op waar u de DITA-inhoud wilt publiceren. Het standaardknooppunt waarin AEM Guides DITA-inhoud publiceert, is bijvoorbeeld: <br>`jcr:content/contentnode` |
   | `topicHeadNode` | String | Geef de knooppuntnaam op waarin u de metagegevens van uw DITA-inhoud wilt opslaan. Het standaardknooppunt waarin AEM Guides metagegevens opslaat, is bijvoorbeeld: <br>`jcr:content/headnode` |


In de volgende schermafbeelding worden de eigenschappen weergegeven die in het standaardsjabloonknooppunt van AEM Guides zijn toegevoegd:

![](assets/add-content-node.png){width="800" align="left"}

De volgende keer dat u DITA-inhoud publiceert met behulp van de sjabloonconfiguraties van uw site, wordt de inhoud gepubliceerd in de knooppunten die zijn opgegeven in de eigenschappen `topicContentNode` en `topicHeadNode` .

Voor bestaande sites moet u echter handmatig de knooppunten `topicContentNode` en `topicHeadNode` toevoegen.

Voer de volgende stappen uit om de vereiste knooppunten aan uw bestaande site toe te voegen:

1. Meld u aan bij AEM en open de CRXDE Lite-modus.

1. Zoek `jcr:content` in het siteknooppunt.

1. Voeg `topicContentNode` - en `topicHeadNode` -knooppunten toe met dezelfde naam als u hebt opgegeven in de sjabloonconfiguraties van de site.


## Uitvoer van AEM-site aanpassen {#id166TG0B30WR}

AEM Guides ondersteunt het maken van uitvoerbestanden in de volgende indelingen:

- AEM-site

- PDF

- HTML5
- EPUB
- Aangepaste uitvoer via DITA-OT

Voor de uitvoer van de AEM-site kunt u verschillende ontwerpsjablonen met verschillende uitvoertaken toewijzen. Deze ontwerpsjablonen kunnen de DITA-inhoud in verschillende lay-outs renderen. U kunt bijvoorbeeld verschillende ontwerpsjablonen opgeven voor een intern en extern publiek.

U kunt ook aangepaste DITA Open Toolkit \(DITA-OT\)-plug-ins met AEM Guides gebruiken. U kunt deze aangepaste DITA-OT-plug-ins uploaden om PDF-uitvoer op een specifieke manier te genereren.

>[!TIP]
>
> Zie de *het publiceren van de Plaats van AEM* sectie in de gids van Beste praktijken [&#x200B; appendix.md \#](appendix.md#) voor beste praktijken rond het creëren van de output van de Plaats van AEM.

### Ontwerpsjabloon aanpassen voor het genereren van uitvoer {#customize_xml-add-on}

AEM Guides gebruikt een set vooraf gedefinieerde ontwerpsjablonen om AEM Site-uitvoer te genereren. U kunt de ontwerpsjablonen van AEM Guides aanpassen om de uitvoer te genereren die voldoet aan uw bedrijfsbranding. Een ontwerpsjabloon is een verzameling van verschillende stijlen \(CSS\), scripts \(zowel server- als client-side\), bronnen \(afbeeldingen, logo&#39;s en andere elementen\) en JCR-knooppunten die al deze bronnen aan elkaar koppelen. Een ontwerpsjabloon kan zo eenvoudig zijn als één serverscript met slechts een paar JCR-knooppunten of een complexe combinatie van stijlen, bronnen en JCR-knooppunten. De malplaatjes van het ontwerp worden gebruikt door het publiceren subsysteem van AEM Guides terwijl het produceren van de output van de Plaats van AEM en zij controleren de structuur, de blik en het gevoel van de geproduceerde output.

Er is geen beperking ten aanzien van waar de middelen van het ontwerpmalplaatje op de server zouden moeten worden gevestigd, maar zij zijn gewoonlijk logisch georganiseerd volgens hun functie. In de standaardsjabloon worden bijvoorbeeld alle JavaScript- en CSS-bestanden opgeslagen in de map `/etc/designs/fmdita/clientlibs/siteoutput/default` . Waar deze bestanden zich bevinden, worden ze aan elkaar gekoppeld door een verzameling JCR-knooppunten. Samen vormen deze JCR-knooppunten en de bestanden de hele ontwerpsjabloon.

Het standaardontwerpmalplaatje dat met AEM Guides wordt verscheept staat u toe om het landen, het onderwerp, en de componenten van de onderzoekspagina aan te passen. U kunt een kopie maken van het standaardontwerp en de bijbehorende verwijzingssjablonen en verschillende componenten opgeven om de gewenste uitvoer te genereren.

Voer de volgende stappen uit om uw eigen ontwerpsjabloon op te geven die moet worden gebruikt voor het genereren van AEM Site-uitvoer:

1. Meld u aan bij AEM en open de CRXDE Lite-modus.

1. Navigeer naar het standaardontwerpsjabloonknooppunt. De locatie van het standaardontwerpsjabloonknooppunt is:

   `/libs/fmdita/config/templates/`

   ![](assets/templates-node.png){width="300" align="left"}

   >[!NOTE]
   >
   > Maak een kopie van de standaardontwerpsjablonen vanuit de map `libs` naar de map `apps` en breng wijzigingen aan in de map `apps` . U moet ook wijzigingen aanbrengen in de sjablonen waarnaar wordt verwezen vanuit het standaardsjabloonknooppunt. De sjablonen waarnaar wordt verwezen, worden onder het knooppunt `/libs/fmdita/templates/default/cqtemplates` geplaatst. Maak een kopie van de sjablonen waarnaar wordt verwezen in de map `apps` voordat u wijzigingen aanbrengt.

1. Klik de *standaard* component in de *malplaatjes* knoop om tot zijn eigenschappen toegang te hebben.

   De eigenschappen van AEM Guides&#39;s ontwerpsjablonen worden in de volgende tabel beschreven.

   | Eigenschap | Beschrijving |
   |--------|-----------|
   | `landingPageTemplate`, `searchPageTemplate`, `topicPageTemplate`, `shadowPageTemplate` | Geef het knooppunt `cq:Template` voor deze overeenkomende pagina&#39;s op \(landen, zoeken en onderwerpen\). Standaard is het knooppunt `cq:Template` voor deze pagina&#39;s te vinden in het knooppunt `/libs/fmdita/templates/default/cqtemplates` . Dit knooppunt definieert de structuur en eigenschappen van de bestemmings-, zoek- en onderwerppagina&#39;s. <br> `shadowPageTemplate` wordt gebruikt om de afgekapte inhoud te optimaliseren. U moet de waarde van deze eigenschap instellen op: <br> `fmdita/templates/default/cqtemplates/shadowpage` <br> **Nota** u moet een waarde voor `topicPageTemplate` specificeren. De eigenschappen `landingPageTemplate` en `searchPageTemplate` zijn optioneel. Geef deze eigenschappen niet op als u niet wilt dat de zoek- en bestemmingspagina&#39;s worden gegenereerd. |
   | `title` | Een beschrijvende naam van de ontwerpsjabloon. |
   | `topicContentNode` | De plaats van de knoop die de inhoud DITA in een onderwerppagina zal bevatten. Het pad is relatief ten opzichte van de onderwerppagina. |
   | `topicHeadNode` | De locatie van het knooppunt dat de hoofdwaarden \(of metagegevens\) bevat die zijn afgeleid van de DITA-inhoud. Pad is relatief ten opzichte van onderwerppagina. |
   | `tocNode` | De locatie van het knooppunt dat de inhoudsopgave zal bevatten. Het pad is relatief ten opzichte van de bestemmingspagina of het bestemmingspad. |
   | `basePathProp` | De eigenschapnaam voor het opslaan van het pad van de hoofdmap van de gepubliceerde site. |
   | `indexPathProp` | De eigenschapsnaam voor het opslaan van het pad van de bestemmings-/indexpagina van de gepubliceerde site. |
   | `pdfPathProp` | De bezitsnaam voor het opslaan van de weg van onderwerpPDF, als de generatie van onderwerpPDF wordt toegelaten. |
   | `pdfTypeProp` | De eigenschapsnaam voor het opslaan van het type van de PDF-generatie. Momenteel bevat deze eigenschap altijd &quot;Onderwerp&quot;. |
   | `searchPathProp` | De eigenschapsnaam voor het opslaan van het pad van de zoekpagina als de sjabloon een zoekpagina bevat. |
   | `siteTitleProp` | De eigenschapsnaam voor het opslaan van de titel van de site die wordt gepubliceerd. Deze titel is meestal dezelfde als de titel van de kaart die wordt gepubliceerd. |
   | `sourcePathProp` | De bezitsnaam voor het opslaan van de weg van het bronDITA onderwerp voor de huidige pagina. |
   | `tocPathProp` | De eigenschapnaam voor het opslaan van het pad van de inhoudsopgave-hoofdmap voor de gepubliceerde site. |


>[!NOTE]
>
> Nadat u een aangepaste ontwerpsjabloonnode hebt gemaakt, moet u de optie Ontwerpen in de uitvoervoorinstellingen van de AEM-site bijwerken om het aangepaste ontwerpsjabloonknooppunt te kunnen gebruiken.

Voor meer informatie, zie [&#x200B; Creërend uw Eerste Adobe Experience Manager 6.3 website &#x200B;](https://helpx.adobe.com/experience-manager/using/first_aem63_website.html) en [&#x200B; de Grondbeginselen &#x200B;](https://helpx.adobe.com/nl/experience-manager/6-3/sites/developing/using/the-basics.html) van het ontwikkelen van uw eigen website op AEM.

### Documenttitel gebruiken om uitvoer van AEM-sites te genereren

Bij het genereren van de uitvoer van de AEM-site speelt de manier waarop URL&#39;s worden gegenereerd een belangrijke rol bij de detecteerbaarheid van uw inhoud. Als u op UUID gebaseerde bestandsnamen gebruikt, is het genereren van URL&#39;s op basis van UUID van uw bestanden niet zoekvriendelijk. Als Beheerder of Uitgever, hebt u de controle over hoe u URLs voor uw uitvoer van de Plaats van AEM wilt produceren. AEM Guides biedt u een configuratie waarmee u URL&#39;s van AEM Site-uitvoer kunt genereren met de bestandstitel in plaats van de op UUID gebaseerde bestandsnamen. Voor op UUID gebaseerde bestandssystemen is deze optie standaard ingeschakeld. Dit impliceerde dat wanneer u de output van de Plaats van AEM voor op UUID-Gebaseerde dossiersystemen produceert, de titels van het dossier worden gebruikt om URLs en niet UUIDs van de dossiers te produceren.

Bij het genereren van de uitvoer van de AEM-site speelt de manier waarop URL&#39;s worden gegenereerd een belangrijke rol bij de detecteerbaarheid van uw inhoud. Bij niet-UUID-bestandssystemen wordt de uitvoer van de AEM-site gegenereerd met de bestandsnamen en niet met de titels van het bestand. Als Beheerder of Uitgever, hebt u de controle over hoe u URLs voor uw uitvoer van de Plaats van AEM wilt produceren. AEM Guides biedt u een configuratie waarmee u URL&#39;s van AEM Site-uitvoer kunt genereren met de bestandstitel en niet met de bestandsnamen. Deze optie is standaard uitgeschakeld. Dit impliceerde dat wanneer u de output van de Plaats van AEM produceert, de dossiernamen worden gebruikt om URLs en niet de titel van het dossier te produceren. U kunt ervoor kiezen de URL&#39;s te genereren op basis van de bestandstitels door deze optie in te schakelen.

>[!NOTE]
>
> U kunt regels verder configureren om alleen een set tekens toe te staan in de URL&#39;s van een AEM-site-uitvoer. Voor meer details, zie [&#x200B; filename ontsmettingsregels voor het creëren van onderwerpen en het publiceren van de output van de Plaats van AEM &#x200B;](#id2164D0KD0XA) vormen.

Voer de volgende stappen uit om het genereren van URL&#39;s in AEM Site-uitvoer te configureren:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.config.ConfigManager** bundel.

1. Selecteer de **Titel van het Gebruik voor de Namen van de Pagina van de Plaats van AEM** optie.

   >[!NOTE]
   >
   > Als u uitvoer wilt genereren met de bestandsnamen, schakelt u deze optie uit.

1. Klik **sparen**.


### Configureer de regels voor bestandsontsmetting voor het maken van onderwerpen en het publiceren van de uitvoer van de AEM-site {#id2164D0KD0XA}

Als beheerder kunt u een lijst definiëren met geldige speciale tekens die zijn toegestaan in bestandsnamen. Deze tekens vormen uiteindelijk de URL van een AEM Site-uitvoer. In eerdere versies mochten gebruikers bestandsnamen definiëren die speciale tekens bevatten, zoals `@` , `$` , `>` en meer. Deze speciale tekens resulteerden in gecodeerde URL bij het genereren van AEM Site-pagina&#39;s.

Vanaf de release 3.8 zijn configuraties toegevoegd om een lijst met speciale tekens te definiëren die zijn toegestaan in de bestandsnamen. Door gebrek, bevat de geldige filename configuratie &quot;`a-z A-Z 0-9 - _`&quot;. Dit houdt in dat u tijdens het maken van een bestand elk speciaal teken in de bestandstitel kunt hebben, maar dat het intern wordt vervangen door een afbreekstreepje \(`-`\) in de bestandsnaam. U kunt bijvoorbeeld de bestandstitel Introduction 1 of Introduction@1 hebben. De overeenkomstige bestandsnaam die voor beide gevallen wordt gegenereerd, is Introduction-1.

Wanneer u een lijst van geldige karakters bepaalt, herinner dat deze karakters &quot;`*/:[\]|#%{}?&<>"/+`&quot;en `a space` altijd met een koppelteken \ (`-` \) zullen worden vervangen.

>[!NOTE]
>
> Als u de geldige lijst met speciale tekens niet configureert, kan het maken van bestanden onverwachte resultaten opleveren.

Voer de volgende stappen uit om de geldige speciale tekens in bestandsnamen en AEM Site-uitvoer te configureren:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op *com.adobe.fmdita.common.SanitizeNodeNameImpl* bundel.

1. In **Geweigerd Geplaatst Karakter voor het Publiceren aan het bezit van AEM Sites**, zorg ervoor dat het bezit aan ```'<>`@$``` wordt geplaatst. U kunt meer speciale tekens aan deze lijst toevoegen, maar deze moeten de vereiste speciale tekens bevatten.

   >[!NOTE]
   >
   > U kunt de andere eigenschappen zoals **Kleine Geval van het Gebruik** in filenames, **Scheiding** ook vormen om ongeldige karakters te behandelen, en **Maximum Aantal Karakters** toegestaan in filenames.

1. Klik **sparen**.

1. Onderzoek naar en klik op **com.adobe.fmdita.config.ConfigManager** bundel.

1. In **Regex voor Geldige het bezit van Karakters**, zorg ervoor dat het bezit aan `[-a-zA-Z0-9_]` wordt geplaatst. U kunt meer tekens aan deze lijst toevoegen, maar deze moeten de basistekens hebben en de lijst moet beginnen met een koppelteken \(`-`\).

   >[!NOTE]
   >
   > Deze eigenschap definieert de lijst met geldige tekens die wordt gebruikt om een nieuw bestand te maken.

1. Klik **sparen**.


### Samenvoegen van de structuur van AEM-siteknooppunten configureren

Wanneer u de output van de Plaats van AEM produceert, wordt een knoop voor elk element in de onderwerpen intern gecreeerd. Voor een kaart DITA met duizenden onderwerpen, kan deze knoopstructuur te diep worden. Dit type van diep genestelde knoopstructuur kan prestatieskwesties voor grotere plaatsen hebben. De volgende momentopname toont diep genestelde knoopstructuur voor een output van de Plaats van AEM:

![](assets/deep-nested-aem-site-node-structure.png){width="300" align="left"}

In de bovenstaande momentopname, merk op dat er een knoop voor elk `p` element en zijn verdere sub-elementen is gecreeerd en een gelijkaardige structuur wordt gecreeerd voor elk ander element dat in het onderwerp wordt gebruikt.

Met AEM Guides kunt u configureren hoe de knooppuntstructuur van de AEM Site-uitvoer intern wordt gemaakt. U kunt de nodestructuur bij gespecificeerde elementen afvlakken, zo betekent het dat u een element kunt bepalen dat als belangrijkste element zal worden beschouwd en alle sub-elementen binnen het zullen met het belangrijkste element worden samengevoegd. Als u bijvoorbeeld besluit het element `p` af te vlakken, worden alle elementen die in het element `p` worden weergegeven, samengevoegd met het element main `p` . Er wordt geen aparte notitie gemaakt voor een subelement binnen het element `p` . In de volgende momentopname wordt de nodestructuur afgevlakt op het element `p` weergegeven:

![](assets/flattened-aem-site-node-structure.png){width="300" align="left"}

Voer de volgende stappen uit om de nodestructuur van de AEM-site af te vlakken:

1. Geef het element op waarop u de nodestructuur wilt afvlakken.

   1. Bedekking van het knooppunt `libs` in het knooppunt `apps` en open het bestand elementmapping.xml.

   1. Voeg de eigenschap `<flatten>true</flatten>` toe in de definitie van het element waar u de nodestructuur wilt afvlakken. Als u bijvoorbeeld de nodestructuur bij het `p` -element wilt afvlakken, voegt u het afgevlakte kenmerk toe aan de definitie van `p` -element, zoals hieronder wordt getoond:

      ```XML
      <ditaelement>
          <name>p</name>
          <class>- topic/p</class>
          <componentpath>fmdita/components/dita/wrapper</componentpath>
          <type>COMPOSITE</type>
          <target>para</target>
          <flatten>true</flatten>
          <wrapelement>div</wrapelement>
      </ditaelement>
      ```

      >[!NOTE]
      >
      > Standaard is de eigenschap voor samenvoegen van knooppunten geconfigureerd in het element `p` .

1. Schakel de configuratie voor het afvlakken van siteknooppunten in configMgr in.

   1. Open de Adobe Experience Manager Web Console Configuration-pagina.

      De standaard-URL voor toegang tot de configuratiepagina is:

      ```http
      http://<server name>:<port>/system/console/configMgr
      ```

   1. Onderzoek naar en klik op *com.adobe.dxml.flattening.FlatteningConfigurationService* bundel.

   1. Selecteer het {**optie 0} van het Bezit flattening.enabled.**

   1. Klik **sparen**.


>[!IMPORTANT]
>
> Als u om het even welke verandering in het elementmapping.xml- dossier hebt aangebracht, zorg ervoor dat u configMgr opent en om het even welke bundel voor veranderingen opslaat om in werking te treden.

Wanneer u nu de AEM Site-uitvoer genereert, worden de knooppunten in het `p` -element samengevoegd en opgeslagen in het `p` -element zelf. U kunt de nieuwe afvlakkingseigenschappen voor het element `p` vinden in CRXDE.

![](assets/flatten-aem-site-note-props-crxde.png){width="650" align="left"}

**verhinderen afvlakking van de het notitiestructuur van de Plaats van AEM**

Net als het opgeven van het knooppunt dat moet worden samengevoegd in de uitvoer van de AEM-site, kunt u ook een element opgeven dat u wilt uitsluiten van deze configuratie. Als u bijvoorbeeld knooppunten wilt afvlakken op het element `body` , maar geen `table` element `body` wilt afvlakken, kunt u de eigenschap exclude toevoegen binnen de definitie van het element `table` .

Als u het element `table` wilt uitsluiten van afvlakking, voegt u de volgende eigenschap toe aan de definitie van het element `table` :

`<preventancestorflattening>true|false</preventancestorflattening>`

### De versie voor verwijderde pagina&#39;s configureren in AEM Site-uitvoer

Wanneer u de output van de Plaats van AEM met **schrapping en** creeert **&#x200B;**&#x200B;optie die voor het Bestaande plaatsen van de Pagina&#39;s van de Output wordt geselecteerd, wordt een versie gecreeerd voor pagina \(s \) die worden geschrapt. U kunt het systeem vormen om de verwezenlijking van een versie vóór schrapping tegen te houden.

Voer de volgende stappen uit om te stoppen met het maken van een versie voor de pagina\(s\) die wordt verwijderd:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op *com.adobe.fmdita.config.ConfigManager* bundel.

1. Selecteer **creeer geen Versie voor Geschrapte Pagina&#39;s** optie.

   >[!NOTE]
   >
   > Als deze optie is geselecteerd, kunnen gebruikers elke pagina\(s\) rechtstreeks verwijderen zonder daarvoor een versie te maken. Als de optie niet is geselecteerd, wordt een versie gemaakt voordat de pagina\(s\) worden verwijderd.

1. Klik **sparen**.

## Metagegevens gebruiken bij het publiceren van uitvoer via DITA-OT {#id191LF0U0TY4}

AEM Guides biedt een manier om aangepaste metagegevens door te geven tijdens het publiceren van uitvoer met DITA-OT. Als beheerder en uitgever zou u de volgende taken moeten uitvoeren om douanemetagegevens in de gepubliceerde output te vormen en te gebruiken:

- Als beheerder, voeg de vereiste meta-gegevens in het systeem toe zodat het op de pagina van Eigenschappen van de kaart DITA ter beschikking wordt gesteld.

- Als beheerder, voeg de douanemetagegevens in de meta-gegevenslijst toe zodat het in de DITA kaartconsole verschijnt.

- Als Uitgever, vorm en voeg de douanemetagegevens met de kaart DITA toe en produceer de vereiste output.


Voer de volgende stappen uit om de vereiste metagegevens in het systeem toe te voegen:

1. Meld u als beheerder aan bij Adobe Experience Manager.

1. Klik op de verbinding van Adobe Experience Manager bij de bovenkant en kies **Hulpmiddelen**.

1. Selecteer **Assets** van de lijst van hulpmiddelen.

1. Klik op de **Schema&#39;s van Meta-gegevens** tegel.

   De pagina Metadata Schema Forms wordt weergegeven.

1. Selecteer de **standaard** vorm van de lijst.

   >[!NOTE]
   >
   > De eigenschappen die op de pagina Eigenschappen voor een DITA-kaart worden weergegeven, zijn afkomstig uit dit formulier.

1. Klik **uitgeven**.

1. Voeg de aangepaste metagegevens toe die u in de gepubliceerde uitvoer wilt gebruiken. We voegen bijvoorbeeld metagegevens voor het publiek toe door de volgende stappen uit te voeren:

   1. Van **bouwt de de componentenlijst van de Vorm**, belemmering-en-daling **Enige component van de Tekst van de Lijn** op de vorm.

   1. Selecteer het nieuwe gebied om de **Montages** van het gebied te openen.

   1. In het **Etiket van het Gebied**, ga de meta-gegevensnaam— Publiek in.

   1. In de **Kaart aan Bezit** het plaatsen, specificeer./jcr:content/metadata/&lt;name of the metadata\>. We zullen het bijvoorbeeld instellen op ./jcr:content /metadata/publiek.

   Voeg met deze stappen alle vereiste metagegevensparameters toe.

1. Klik **sparen**.


De nieuwe parameter verschijnt nu op de pagina van Eigenschappen voor alle kaarten DITA.

![](assets/properties-page-custom-metadata.PNG){width="650" align="left"}

Vervolgens moet u de aangepaste metagegevens beschikbaar stellen in de DITA-kaartconsole. Voer de volgende stappen uit om de aangepaste metagegevens beschikbaar te maken op het dashboard voor de DITA-kaart:

1. Meld u aan bij AEM en open de CRXDE Lite-modus.

1. Open het bestand metadataList dat beschikbaar is op de volgende locatie:

   /libs/fmdita/config/metadataList

   >[!NOTE]
   >
   > Het metadataList dossier bevat een lijst van eigenschappen die in de **drop-down lijst van Eigenschappen** van een kaart DITA in het kaartdashboard worden getoond. Door gebrek, zijn er vier eigenschappen die in dit dossier worden vermeld— docstate, dc :language, dc :description, en dc :title.

1. Voeg de aangepaste metagegevens toe die u hebt toegevoegd aan de pagina Forms van het metagegevensschema. Voeg voor ons voorbeeld publieksparameter toe aan het einde van de standaardlijst.

1. Klik **sparen allen**.


Nu zullen de douanemetagegevens omhoog in de DITA kaartconsole **Eigenschappen** drop-down lijst van Eigenschappen verschijnen.

Ten slotte moet u als uitgever de aangepaste metagegevens opnemen in de gepubliceerde uitvoer. Voer de volgende stappen uit om de aangepaste metagegevens te verwerken tijdens het genereren van de uitvoer:

1. Navigeer in de gebruikersinterface van Assets naar de DITA-kaart die u wilt publiceren.

1. Selecteer het DITA-kaartbestand en open de eigenschappenpagina.

1. Geef op de pagina Eigenschappen de waarde voor de aangepaste metagegevens op. In ons voorbeeld hebben we een waarde van External opgegeven voor de publieksparameter.

   ![](assets/properties-page-custom-metadata-value.png){width="650" align="left"}

1. Klik **sparen &amp; Sluiten**.

1. Klik op het DITA kaartdossier om de DITA kaartconsole te openen.

1. In de **Output stelt** lusje vooraf in, selecteer de output vooraf ingesteld die u wilt gebruiken om de output te produceren.

1. Klik **uitgeven**.

1. Van de **drop-down lijst van Eigenschappen**, selecteer de eigenschappen die u aan het het publiceren proces wilt overgaan.

   ![](assets/props-in-publish-output.PNG){width="650" align="left"}


De geselecteerde eigenschappen/metagegevens worden doorgegeven aan het publicatieproces en beschikbaar gesteld in de uiteindelijke uitvoer.

## DITA-elementtoewijzing aanpassen met AEM-componenten {#id1679J600HEL}

DITA-elementen in AEM Guides worden toegewezen aan hun overeenkomstige AEM-componenten. AEM Guides gebruikt deze toewijzing in workflows, zoals publiceren en reviseren, om DITA-elementen om te zetten in een corresponderende AEM-component. De toewijzing wordt gedefinieerd in het `elementmapping.xml` -bestand, dat toegankelijk is vanuit de CRXDE Lite-modus. Open de volgende URL in de CRXDE Lite-modus:

`/libs/fmdita/config/elementmapping.xml`

>[!NOTE]
>
> Breng geen aanpassingen aan in de standaardconfiguratiebestanden in het knooppunt ``libs`` . U moet een overlay van het knooppunt ``libs`` in het knooppunt ``apps`` maken en de vereiste bestanden alleen in het knooppunt ``apps`` bijwerken.

U kunt de vooraf gedefinieerde DITA-elementtoewijzingen gebruiken of u kunt DITA-elementen toewijzen aan uw aangepaste AEM-componenten. Als u uw aangepaste AEM-componenten wilt gebruiken, moet u de structuur van het `elementmapping.xml` -bestand begrijpen.

### elementmapping.xml-structuur

Hieronder vindt u een overzicht op hoog niveau van de `elementmapping.xml` -structuur:

1. Elk element DITA wordt eerst gezocht naar een overeenkomstige componentenafbeelding die op de elementnaam wordt gebaseerd. Bijvoorbeeld:

   ```XML
   <ditaelement>     
      <name>**substeps**</name>  
      <class>- topic/ol task/substeps</class>  
      <componentpath>dita/components/ditaolist</componentpath>  
      <type>COMPOSITE</type>  
      <target>para</target>
   </ditaelement>
   ```

   In het bovenstaande voorbeeld worden alle `substeps` DITA-elementen gerenderd met de `dita/components/ditaolist` -component.

1. Als een element DITA geen gelijke vindt die op de naam wordt gebaseerd, dan wordt een gelijke op de basis van `class` gedaan. Bijvoorbeeld:

   ```XML
   <ditaelement>  
      <name>topic</name>  
      <class>**- topic/topic**</class>  
      <componentpath>fmdita/components/dita/topic</componentpath>  
      <type>COMPOSITE</type>  
      <target>para</target>  
      <attributemap> 
         <attribute from="id" to="id" />  
      </attributemap>
   </ditaelement>
   ```

   Als er in het bovenstaande voorbeeld geen toewijzing is gedefinieerd voor het element `task` , wordt het element `task` toegewezen aan de bovenstaande component omdat `task` wordt overgeërfd van de component `topic` .

1. Wanneer een element een overeenkomstige componentenafbeelding heeft, dan wordt de verdere verwerking van zijn kindelementen bepaald door `type`. Bijvoorbeeld:

   ```XML
   <ditaelement>  
      <name>title</name>  
      <class>- topic/title</class>  
      <componentpath>foundation/components/title</componentpath>  
      <type>**STANDALONE**</type>  
      <target>para</target>  
      <textprop>jcr:title</textprop>
   </ditaelement>
   ```

   `type` gebruikt de volgende waarden:

   - COMPOSITE: element aan component *afbeelding gaat ook voor kindelementen* verder.

   - STANDALONE: De kindelementen van het huidige element worden *niet verder in kaart gebracht*.

   In het bovenstaande voorbeeld, als het `<title>` -element onderliggende elementen bevat, worden deze niet toegewezen aan een andere component. De component voor `<title>` -element is verantwoordelijk voor het renderen van alle onderliggende elementen binnen het `<title>` -element.

1. Als er meerdere componenten zijn toegewezen aan één DITA-element, wordt de beste overeenkomst voor het element geselecteerd. Om de beste overeenkomende component te selecteren, worden het domein en de structurele specialisatie van elementen DITA overwogen.

   Als er elementen DITA met domeinspecialisatie zijn en een component voor domeinspecialisatie in kaart wordt gebracht, dan wordt die component hoge prioriteit gegeven.

   Op dezelfde manier als er elementen DITA met structurele specialisatie zijn en een component voor structurele specialisatie in kaart wordt gebracht, dan wordt die component hoge prioriteit gegeven.

1. U kunt `<attributemap>` gebruiken in elementtoewijzing om kenmerkwaarden toe te wijzen aan de overeenkomstige knoopeigenschappen.

1. `textprop` kan worden gebruikt voor het serialiseren van de tekstinhoud van een DITA-element naar een node-eigenschap. Bovendien kan de klasse meerdere keren worden gebruikt in een elementtag om de tekstinhoud op meerdere locaties in de gepubliceerde hiërarchie te serialiseren. U kunt ook de locatie en naam van de eigenschap target aanpassen. Bijvoorbeeld:

   ```XML
   <ditaelement> 
       <name>title</name> 
       <class>- topic/title</class> 
       <componentpath>foundation/components/title</componentpath> 
       <type>STANDALONE</type> 
       <target>para</target> 
       <textprop>**jcr:title**</textprop>
   </ditaelement>
   ```

   In de bovenstaande elementtoewijzing wordt opgegeven dat de tekstinhoud van het element `<title>` wordt opgeslagen als waarde van een eigenschap met de naam `jcr:title` op het uitvoerknooppunt.

1. `xmlprop` kan worden gebruikt voor het serialiseren van de volledige XML voor een bepaald element aan een knoopbezit. De component kan deze knoopeigenschap vervolgens lezen en aangepaste rendering uitvoeren. Bijvoorbeeld:

   ```XML
   <ditaelement> 
       <name>svg-container</name> 
       <class>+ topic/foreign svg-d/svg-container</class> 
       <componentpath>fmdita/components/dita/svg</componentpath> 
       <type>STANDALONE</type> 
       <target>para</target> 
       <xmlprop>**data**</xmlprop>
   </ditaelement>
   ```

   In de bovenstaande elementtoewijzing wordt opgegeven dat de volledige XML-opmaak voor element `<svg-container>` wordt opgeslagen als waarde van een eigenschap met de naam `data` op het uitvoerknooppunt.

1. Er is een speciale kenmerktoewijzing om wegresolutie in het proces van de outputgeneratie te behandelen. Bijvoorbeeld:

   ```XML
   <attributemap> 
       <attribute from="href" to="fileReference" ispath="true" rel="source" /> 
       <attribute from="height" to="height" /> 
       <attribute from="width" to="width" />
   </attributemap>
   ```

   Voor het bovenstaande `attributemap` wordt het kenmerk `href` in het DITA-element toegewezen aan een knoopeigenschap met de naam `fileReference` . Nu `ispath` is ingesteld op `true` , wordt dit pad door het productieproces van de uitvoer omgezet en vervolgens ingesteld in de eigenschap node `fileReference` .

   Hoe deze resolutie gebeurt, wordt bepaald op basis van de waarde van het kenmerk `rel` in de kenmerktoewijzing.

   - Als `rel=source` , wordt de waarde van `href` omgezet met betrekking tot het DITA-bronbestand dat momenteel wordt verwerkt. De waarde van `href` wordt omgezet en in de waarde van `fileReference` -eigenschap geplaatst.

   - Als `rel=target` , wordt de waarde van `href` omgezet met betrekking tot de hoofdpublicatielocatie. De waarde van `href` wordt omgezet en in de waarde van `fileReference` -eigenschap geplaatst.

   Als u geen voorbewerking of resolutie wilt toepassen op padkenmerken, hoeft u het kenmerk `ispath` niet op te geven. De waarde wordt ongewijzigd gekopieerd en de component kan de vereiste resolutie uitvoeren.


### DITA-elementschema

Hieronder ziet u een voorbeeld van het DITA-elementschema in het bestand `elementmapping.xml` :

```XML
<ditaelement>         
    <name>element_name</name>     
    <class>element_class</class>     
    <componentpath>fmdita/components/dita/component_name</componentpath>     
    <type>COMPOSITE|STANDALONE</type>      
    <attributeprop>propname_a</attributeprop>       
    <textprop>propname_t</textprop>     
    <xmlprop>propname_x</xmlprop>      
    <xpath>xpath expression string</xpath>      
    <target>head|para</target>      
    <wrapelement>div</wrapelement>      
    <wrapclass>class_name</wrapclass>      
    <attributemap>           
    <attribute from="attrname" to="propname" ispath="true|false" rel="source|target" />     
    </attributemap>     
    <skip>true|false</skip> 
</ditaelement>
```

De volgende lijst beschrijft de elementen in het DITA elementenschema:

| Element | Beschrijving |
|-------|-----------|
| `<ditaelement>` | The top-level node for each mapping element. |
| `<class>` | Het klassenkenmerk van het doel-DITA-element waarvoor u de component schrijft. <br> Bijvoorbeeld, is de klassenattributen voor het onderwerp DITA: <br>`topic/topic` |
| `<componentpath>` | Het CRXDE-pad van de toegewezen AEM-component. |
| `<type>` | Mogelijke waarden: <br> - **COMPOSITE**: Proces kindelementen eveneens <br> - **STANDALONE**: Overslaat verwerking van kindelementen |
| `<attributeprop>` | Wordt gebruikt voor het toewijzen van geserialiseerde DITA-kenmerken en -waarden aan AEM-knooppunten als eigenschap. Als u bijvoorbeeld `<note type="Caution">` -element hebt en de component die voor dit element is toegewezen, `<attributeprop>attr_t</ attributeprop>` heeft, worden het kenmerk en de waarde van het knooppunt geserialiseerd naar de eigenschap `attr_t` van het corresponderende AEM-knooppunt \( `attr_t->type="caution"`\). |
| `<textprop>propname_t</textprop>` | Sparen `getTextContent()` output aan bezit door `propname_t.` wordt bepaald **Nota:** dit is een geoptimaliseerd bezit dat. |
| `<xmlprop>propname_x </xmlprop>` | Sparen geserialiseerde XML van deze knoop aan bezit dat door `propname_x.` wordt bepaald **Nota:** Dit is een geoptimaliseerd bezit. |
| `<xpath>` | Als het element van XPath in de elementenafbeelding wordt verstrekt, dan samen met elementnaam en klasse zou de voorwaarde van XPath ook voor de componentenafbeelding moeten worden voldaan om te worden gebruikt. |
| `<target>` | Plaats voor het element DITA in de crx bewaarplaats op gespecificeerde plaats. <br> Mogelijke waarden:<br> - **hoofd**: Onder de hoofdknoop <br> - **tekst**: Onder de paragraafknoop |
| `<wrapelement>` | Het HTML-element waarin de inhoud moet worden verpakt. |
| `<wrapclass>` | De elementwaarde voor de eigenschap `wrapclass.` |
| `<attributemap>` | Containerknooppunt met een of meer `<attribute>` knooppunten. |
| `<attribute from="attrname" to="propname" ispath="true\|false" rel="source\|target" />` | Wijst de attributen DITA aan de eigenschappen van AEM toe:<br> - **`from`**: DITA kenmerknaam <br> - **`to`**: de naam van het de componentenbezit van AEM <br> - **`ispath`**: Als de attributen een wegwaarde \ (bijvoorbeeld: *beeld* \) <br> - **`rel`** is: Als de weg de bron of doel <br>**Nota is:** als `attrname`  met `%` en wijst u vervolgens `attrname minus '%'` toe aan de eigenschap &#39; `propname`&#39;. |

**Extra nota&#39;s**

- Als u de standaardelement-toewijzing wilt overschrijven, wordt u aangeraden de wijzigingen in het standaard `elementmapping.xml` -bestand niet aan te brengen. Maak een nieuw XML-toewijzingsbestand en plaats het bestand op een andere locatie, bij voorkeur in de aangepaste map voor apps die u maakt.

- In het `elementmapping.xml` -bestand zijn er veel toewijzingsitems die verwijzen naar de component fmdita/components/dita/wrapper. Wrapper is een generische component die relatief eenvoudige concepten DITA gebruikend eigenschappen op hun plaatsknoop teruggeeft om relevante HTML te produceren. De eigenschap `wrapelement` wordt gebruikt om omsluitende tags te genereren en de onderliggende rendering wordt gedelegeerd aan de corresponderende componenten. Dit is handig wanneer u alleen een containercomponent wilt. In plaats van een nieuwe component te maken die een specifieke containertag zoals `div` of `p` rendert, kunt u de component Wrapper met de eigenschappen `wrapelement` en `wrapclass` gebruiken om hetzelfde effect te bereiken.

- Het wordt niet aanbevolen grote hoeveelheden tekst op te slaan in JCR-eigenschappen van String. De geoptimaliseerde berekening van het eigenschapstype bij het genereren van de uitvoer zorgt ervoor dat grote tekstinhoud niet wordt opgeslagen als tekenreekstype. In plaats daarvan, wanneer de inhoud groter dan een bepaalde drempel moet worden bewaard, wordt het type van het bezit veranderd in binair. Door gebrek, wordt deze drempel gevormd aan 512 bytes, maar kan in de Manager van de Configuratie \ (*worden veranderd com.adobe.fmdita.config.ConfigManager* \) door **te veranderen sparen als Binaire Drempel** het plaatsen.

- Als u een deel van \(en niet alle\) van de elementtoewijzingen wilt overschrijven, hoeft u niet het gehele `elementmapping.xml` -bestand te repliceren. U moet een nieuw XML-toewijzingsbestand maken en alleen de elementen definiëren die u overschrijft.

- Nadat u het XML-bestand op de aangepaste locatie hebt gemaakt, werkt u de instelling `Override Element Mapping` in de `com.adobe.fmdita.config.ConfigManager` -bundel bij.


## DITA-kaartconsole aanpassen {#id188HC08M0CZ}

AEM Guides biedt u de flexibiliteit om de mogelijkheden van de DITA kaartconsole uit te breiden. Als u bijvoorbeeld een set rapporten hebt die afwijken van wat er in AEM Guides beschikbaar is, kunt u dergelijke rapporten toevoegen aan de kaartconsole. Als u de kaartconsole wilt aanpassen, moet u een AEM Client Library \(of ClientLib\) maken die de code bevat om de vereiste functionaliteit uit te voeren.

>[!NOTE]
>
> Directe aanpassing aan pagina-onderdelen wordt niet aanbevolen, omdat deze wordt overschreven door nieuwe versies van het product.

AEM Guides biedt de categorie `apps.fmdita.dashboard-extn` voor het aanpassen van de kaartconsole. Wanneer de kaartconsole wordt geladen, wordt de functionaliteit die onder de categorie `apps.fmdita.dashboard-extn` wordt gemaakt, uitgevoerd en geladen.

>[!NOTE]
>
> Voor meer informatie over het creëren van de Bibliotheek van de Cliënt van AEM, zie [&#x200B; Gebruikend cliënt-Kant Bibliotheken &#x200B;](https://helpx.adobe.com/nl/experience-manager/6-4/sites/developing/using/clientlibs.html).

## Afbeeldingsuitvoering afhandelen tijdens het genereren van de uitvoer {#id177BF0G0VY4}

AEM wordt geleverd met een set standaardworkflows en mediapandgrepen voor het verwerken van middelen. In AEM zijn er vooraf gedefinieerde workflows voor het verwerken van elementen voor de meest gangbare MIME-typen. Doorgaans maakt AEM voor elke afbeelding die u uploadt, meerdere uitvoeringen van dezelfde indeling in binaire indeling. Deze vertoningen kunnen van verschillende grootte, met een verschillende resolutie, met een toegevoegd watermerk, of één of andere andere veranderde eigenschap zijn. Voor meer informatie over hoe AEM activa behandelt, zie [&#x200B; Assets die de Handlers en de Werkschema&#39;s van Media van de Verwerking gebruikt &#x200B;](https://helpx.adobe.com/nl/experience-manager/6-5/assets/using/media-handlers.html) in de documentatie van AEM.

Met AEM Guides kunt u configureren welke afbeeldingsuitvoering moet worden gebruikt wanneer uitvoer voor uw documenten wordt gegenereerd. U kunt bijvoorbeeld kiezen uit een van de standaardafbeeldingsuitvoeringen of een uitvoering maken en hetzelfde gebruiken om uw documenten te publiceren. Toewijzing van afbeeldingsuitvoering voor het publiceren van uw documenten wordt opgeslagen in het `/libs/fmdita/config/ **renditionmap.xml**` -bestand. Een fragment van het bestand `renditionmap.xml` ziet er als volgt uit:

>[!NOTE]
>
> Het wordt aanbevolen een kopie van het bestand `renditionmap.xml` in de map `apps` te maken voor alle aanpassingen.

```XML
<renditionmap>
   <mapelement>
      <mimetype>image/png</mimetype>
      <rendition output="AEMSITE">cq5dam.web.1280.1280.jpeg</rendition>
      <rendition output="PDF">original</rendition>
      <rendition output="HTML5">cq5dam.web.1280.1280.jpeg</rendition>
      <rendition output="EPUB">cq5dam.web.1280.1280.jpeg</rendition>
      <rendition output="CUSTOM">cq5dam.web.1280.1280.jpeg</rendition>
   </mapelement>
...
</renditionmap>
```

Het element `mimetype` geeft het MIME-type van de bestandsindeling aan. Het element `rendition output` geeft het type uitvoerindeling en de naam van de uitvoering \(bijvoorbeeld `cq5dam.web.1280.1280.jpeg`\) aan die moet worden gebruikt voor het publiceren van de opgegeven uitvoer. U kunt de afbeeldingsuitvoeringen opgeven die moeten worden gebruikt voor alle ondersteunde uitvoerindelingen: AEMSITE, PDF, HTML5, EPUB en CUSTOM.

Als de opgegeven vertoning niet aanwezig is, zoekt het AEM Guides-publicatieproces eerst naar de webuitvoering van de opgegeven afbeelding. Als zelfs de webuitvoering niet wordt gevonden, wordt de oorspronkelijke uitvoering van de afbeelding gebruikt.

>[!NOTE]
>
> Deze afbeeldingsuitvoeringen bepalen alleen de uitvoergeneratie. De webuitvoering van een afbeelding wordt gebruikt wanneer u een document opent voor voorvertoning of revisie.

## Automatische herstelperiode voor uitvoergeschiedenis configureren {#id19AAI070V8Q}

Wanneer u een uitvoer genereert, wordt de uitvoer samen met de uitvoerlogboeken gemaakt. Voor grote DITA-kaarten nemen deze logboeken veel ruimte in uw opslagplaats in beslag. De logbestanden worden standaard opgeslagen op de volgende locatie in de opslagplaats:

/var/dxml/metadata/outputHistory/

Over een periode, kon de collectieve grootte van alle logboekdossiers in GBs lopen. Met AEM Guides kunt u een tijdsperiode configureren om deze logbestanden in de opslagplaats te bewaren. Na de opgegeven tijdsperiode worden de logbestanden samen met de productiegeschiedenis van de uitvoer verwijderd uit de opslagplaats.

>[!NOTE]
>
> De geschiedenis van de outputgeneratie is de logboekingang in de Gegenereerde lijst van Output op het lusje van Output.

Het configureren van de functie voor het opschonen van historie heeft invloed op de uitvoergeneratie voor alle DITA-kaarten in de opslagplaats. Op het lusje van Output van een kaart DITA, wordt de geschiedenis gezuiverd na het gespecificeerde aantal dagen en op de tijd die in het plaatsen wordt gespecificeerd.

>[!NOTE]
>
> Het verwijderen van de logbestanden en de productiegeschiedenis van de uitvoer heeft geen invloed op de gegenereerde uitvoer.

Voer de volgende stappen uit om een dag en tijd in te stellen voor het wissen van de uitvoergeschiedenis en logboeken:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.config.ConfigManager** bundel.

1. In het **bezit van de Aanzuivering van de Geschiedenis van de Output van 0&rbrace; &lbrace;het aantal dagen waarna de outputgeschiedenis samen met outputlogboeken wordt gezuiverd.** De standaardwaarde is 5 dagen. Als u deze functie wilt uitschakelen, stelt u deze eigenschap in op 0.

1. In het **bezit van de Opschoontijd van de Geschiedenis van de Output 0&rbrace; &lbrace;de tijd specificeren wanneer het het zuiveren proces in werking wordt gesteld.** Door gebrek, wordt het geplaatst aan 0 :00 \ (of 12 :00 middernacht \). Elke dag op dit ogenblik, wordt het het zuiveren proces uitgevoerd op output die vóór het aantal dagen wordt geproduceerd in het **Periode van de Aanzuivering van de Geschiedenis van de Output** bezit wordt gespecificeerd.

   >[!NOTE]
   >
   > Standaard wordt de functie voor leegmaken elke middernacht uitgevoerd op uitvoerbestanden ouder dan 5 dagen.

1. Klik **sparen**.


## De onlangs gegenereerde limieten in de lijst met uitvoerbestanden wijzigen {#id1679JH0H0O2}

U kunt het maximumaantal geproduceerde output veranderen die in het lusje van Output voor een kaart DITA wordt getoond. Standaard wordt een lijst met de laatste 25 gegenereerde uitvoerbestanden weergegeven. Om het aantal output te veranderen om in de lijst te tonen, werk de **Limiet van de Lijst van Output** het plaatsen in de `com.adobe.fmdita.config.ConfigManager` bundel bij.

>[!TIP]
>
> Zie de *de geschiedenissectie van de Output* in de gids van Beste praktijken [&#x200B; appendix.md \#](appendix.md#) voor beste praktijken rond het werken met outputgeschiedenis.

## Optimalisatie van uitvoerprestaties {#id176LB050VUI}

AEM Guides staat u toe om de grootte van de de generatieprocessen van de outputproductie te vormen die het aantal processen van de outputgeneratie controleert die gelijktijdig lopen. Standaard is de grootte van de procespool ingesteld op het aantal verwerkingskernen dat beschikbaar is in uw systeem plus één. U kunt deze waarde wijzigen in 1 als u opeenvolgende publicaties wilt. In dit geval wordt de eerste publicatietaak uitgevoerd en wordt de volgende publicatietaak opgeslagen in de publicatiereeks.

Om de grootte van de de verwerkingspool van de outputgeneratie te veranderen, werk de **het plaatsen van de Grootte van de Pool van de 1&rbrace; generatie in de** bundel bij.`com.adobe.fmdita.publish.manager.PublishThreadManagerImpl`
