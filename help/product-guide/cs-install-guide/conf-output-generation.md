---
title: Instellingen voor uitvoergeneratie configureren
description: Leer hoe u instellingen voor uitvoergeneratie configureert
exl-id: b5cf4f6c-dc56-428e-a514-6c9f879ac03d
feature: Output Generation
role: Admin
level: Experienced
source-git-commit: a2e52572edf0915c1701a384d396a32de2429f53
workflow-type: tm+mt
source-wordcount: '5620'
ht-degree: 0%

---

# Instellingen voor uitvoergeneratie configureren {#id181AI0B0E30}

AEM Guides wordt geleverd met veel configuratieopties waarmee u het productieproces voor uitvoer kunt aanpassen. Dit onderwerp behandelt alle configuraties en aanpassingen die u aan opstelling uw proces van de outputgeneratie zouden helpen.

## Het tabblad Basislijn op het dashboard voor de DITA-kaart configureren {#id223MD0D0YRM}

Voer de volgende stappen uit om het tabblad Basislijn op het dashboard voor de DITA-kaart te verbergen:

1. Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen.
1. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om het basislijntabblad op het kaartdashboard te configureren.

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `hide.tabs.baseline` | Boolean\(`true/false`\).**Standaardwaarde**: `true` |

>[!NOTE]
>
> Deze configuratie is standaard ingeschakeld en het tabblad Basislijn is niet beschikbaar op het kaartdashboard.

## Overvloeien publiceren configureren binnen een bestaande AEM-site {#id1691I0V0MGR}

Als u een AEM-site hebt die DITA-inhoud bevat, kunt u uw AEM-site-uitvoer zo configureren dat DITA-inhoud wordt gepubliceerd naar een vooraf gedefinieerde locatie op uw site. In de volgende schermafbeelding van een AEM Site-pagina is het knooppunt `ditacontent` bijvoorbeeld gereserveerd voor het opslaan van DITA-inhoud:

![](assets/publish-in-aem-site.png)

De resterende knooppunten op de pagina worden rechtstreeks vanuit de AEM Site-editor gemaakt. Als u de publicatie-instelling configureert voor het publiceren van DITA-inhoud op een vooraf gedefinieerde locatie, weet u zeker dat geen van uw bestaande niet-DITA-inhoud wordt gewijzigd door het AEM Guides-publicatieproces.

U moet de volgende configuraties op uw bestaande plaats uitvoeren om het publiceren van inhoud DITA aan een vooraf bepaalde knoop toe te staan:

- De sjablooneigenschappen van uw site configureren

- Knooppunten op uw site toevoegen om DITA-inhoud te publiceren


Voer de volgende stappen uit om de sjablooneigenschappen van uw bestaande site te configureren:

1. Gebruik de Manager van het Pakket om /libs/fmdita/config/templates/default dossier te downloaden.

   >[!NOTE]
   >
   > Breng geen aanpassingen aan in de standaardconfiguratiebestanden in het knooppunt `libs` . U moet een overlay van het knooppunt `libs` in het knooppunt `apps` maken en de vereiste bestanden alleen in het knooppunt `apps` bijwerken.

1. Voeg de volgende eigenschappen toe:

   | Eigenschapnaam | Type | Waarde |
   |-------------|----|-----|
   | `topicContentNode` | String | Geef de knooppuntnaam op waar u de DITA-inhoud wilt publiceren. Het standaardknooppunt waarin AEM Guides DITA-inhoud publiceert, is bijvoorbeeld: <br> `jcr:content/contentnode` |
   | `topicHeadNode` | String | Geef de knooppuntnaam op waarin u de metagegevens van uw DITA-inhoud wilt opslaan. Het standaardknooppunt waarin AEM Guides metagegevens opslaat, is bijvoorbeeld: <br> `jcr:content/headnode` |


De volgende keer dat u DITA-inhoud publiceert met behulp van de sjabloonconfiguraties van uw site, wordt de inhoud gepubliceerd in de knooppunten die zijn opgegeven in de eigenschappen `topicContentNode` en `topicHeadNode` .

## Uitvoer van AEM-site aanpassen {#id166TG0B30WR}

De AEM Guides ondersteunt het maken van uitvoerbestanden in de volgende indelingen:

- AEM-site
- PDF
- HTML5
- EPUB
- Aangepaste uitvoer via DITA-OT

Voor de uitvoer van de AEM-site kunt u verschillende ontwerpsjablonen met verschillende uitvoertaken toewijzen. Deze ontwerpsjablonen kunnen de DITA-inhoud in verschillende lay-outs renderen. U kunt bijvoorbeeld verschillende ontwerpsjablonen opgeven voor een intern en extern publiek.

U kunt ook aangepaste DITA Open Toolkit \(DITA-OT\)-plug-ins gebruiken met de AEM Guides. U kunt deze aangepaste DITA-OT-plug-ins uploaden om PDF-uitvoer op een specifieke manier te genereren.

>[!TIP]
>
> Zie de *het publiceren van de Plaats van AEM* sectie in de Beste praktijken gids voor beste praktijken rond het creëren van de output van de Plaats van AEM.


### Ontwerpsjabloon aanpassen voor het genereren van uitvoer {#customize_xml-add-on}

De AEM Guides gebruikt een set vooraf gedefinieerde ontwerpsjablonen om AEM Site-uitvoer te genereren. U kunt de AEM Guides-ontwerpsjablonen aanpassen om de uitvoer te genereren die in overeenstemming is met uw bedrijfsbranding. Een ontwerpsjabloon is een verzameling van verschillende stijlen \(CSS\), scripts \(zowel server- als client-side\), bronnen \(afbeeldingen, logo&#39;s en andere elementen\) en JCR-knooppunten die al deze bronnen aan elkaar koppelen. Een ontwerpsjabloon kan zo eenvoudig zijn als één serverscript met slechts een paar JCR-knooppunten of een complexe combinatie van stijlen, bronnen en JCR-knooppunten. De malplaatjes van het ontwerp worden gebruikt door het publiceren subsysteem van AEM Guides terwijl het produceren van de output van de Plaats van AEM en zij controleren de structuur, de blik en het gevoel van de geproduceerde output.

Er is geen beperking ten aanzien van waar de middelen van het ontwerpmalplaatje op de server zouden moeten worden gevestigd, maar zij zijn gewoonlijk logisch georganiseerd volgens hun functie. In de standaardsjabloon worden bijvoorbeeld alle JavaScript- en CSS-bestanden opgeslagen in de map `/etc/designs/fmdita/clientlibs/siteoutput/default` . Waar deze bestanden zich bevinden, worden ze aan elkaar gekoppeld door een verzameling JCR-knooppunten. Samen vormen deze JCR-knooppunten en de bestanden de hele ontwerpsjabloon.

Het standaardontwerpmalplaatje dat met AEM Guides wordt verscheept staat u toe om het landen, het onderwerp, en de componenten van de onderzoekspagina aan te passen. U kunt een kopie maken van het standaardontwerp en de bijbehorende verwijzingssjablonen en verschillende componenten opgeven om de gewenste uitvoer te genereren.

Voer de volgende stappen uit om uw eigen ontwerpsjabloon op te geven die moet worden gebruikt voor het genereren van AEM Site-uitvoer:

1. Gebruik de Manager van het Pakket om het standaardontwerpmalplaatje van de volgende plaats te downloaden:

   /libs/fmdita/config/templates

1. Maak een kopie van de gedownloade bestanden op de volgende locatie in de Cloud Manager Git-opslagplaats:

   /apps/fmdita/config/templates

1. U moet ook de sjablonen downloaden en kopiëren waarnaar wordt verwezen vanuit het standaardsjabloonknooppunt. De sjablonen waarnaar wordt verwezen worden onder:

   /libs/fmdita/templates/default/cqtemplates

   De eigenschappen van de AEM Guides-ontwerpsjabloon worden in de volgende tabel beschreven.

   | Eigenschap | Beschrijving |
   |--------|-----------|
   | `landingPageTemplate`, `searchPageTemplate`, `topicPageTemplate`, `shadowPageTemplate` | Geef het knooppunt `cq:Template` voor deze overeenkomende pagina&#39;s op \(landen, zoeken en onderwerpen\). Standaard is het knooppunt `cq:Template` voor deze pagina&#39;s te vinden in het knooppunt `/libs/fmdita/templates/default/cqtemplates` . Dit knooppunt definieert de structuur en eigenschappen van de bestemmings-, zoek- en onderwerppagina&#39;s.<br> De lus `shadowPageTemplate` wordt gebruikt om de inhoud die u hebt afgekapt, te optimaliseren. U moet de waarde van deze eigenschap instellen op: `fmdita/templates/default/cqtemplates/shadowpage` <br> **Nota:** u moet een waarde voor `topicPageTemplate` specificeren. De eigenschappen `landingPageTemplate` en `searchPageTemplate` zijn optioneel. Geef deze eigenschappen niet op als u niet wilt dat de zoek- en bestemmingspagina&#39;s worden gegenereerd. |
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

Voor meer informatie, zie [ Creërend uw eerste website van Adobe Experience Manager ](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html?lang=nl-NL) en [ de Grondbeginselen ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/develop-wknd-tutorial.html?lang=nl-NL) van het ontwikkelen van uw eigen website op AEM.

### Documenttitel gebruiken om uitvoer van AEM-sites te genereren

Bij het genereren van de uitvoer van de AEM-site speelt de manier waarop URL&#39;s worden gegenereerd een belangrijke rol bij de detecteerbaarheid van uw inhoud. Als u op UUID gebaseerde bestandsnamen gebruikt, is het genereren van URL&#39;s op basis van UUID van uw bestanden niet zoekvriendelijk. Als Beheerder of Uitgever, hebt u de controle over hoe u URLs voor uw uitvoer van de Plaats van AEM wilt produceren. AEM Guides biedt u een configuratie waarmee u URL&#39;s van AEM Site-uitvoer kunt genereren met de bestandstitel in plaats van de op UUID gebaseerde bestandsnamen. Voor op UUID gebaseerde bestandssystemen is deze optie standaard ingeschakeld. Dit impliceerde dat wanneer u de output van de Plaats van AEM voor op UUID-Gebaseerde dossiersystemen produceert, de titels van het dossier worden gebruikt om URLs en niet UUIDs van de dossiers te produceren.

>[!NOTE]
>
> U kunt regels verder configureren om alleen een set tekens toe te staan in de URL&#39;s van een AEM-site-uitvoer. Voor meer details, zie [ filename ontsmettingsregels voor het creëren van onderwerpen en het publiceren van de output van de Plaats van AEM ](#id2164D0KD0XA) vormen.

Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om de URL&#39;s te configureren die worden gegenereerd in AEM Site-uitvoer:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `aemsite.pagetitle` | Boolean \(true/false\). Als u uitvoer wilt genereren met de paginatitel, stelt u deze eigenschap in op true. Standaard, wordt het geplaatst om het dossier te gebruiken - noem.<br> **Standaardwaarde**: vals |

### De URL van de AEM-site-uitvoer configureren om de documenttitel te gebruiken

U kunt de documenttitels in URL van de output van de Plaats van AEM gebruiken. Als de bestandsnaam niet bestaat of niet alle speciale tekens bevat, kunt u het systeem zo configureren dat de speciale tekens worden vervangen door een scheidingsteken in de URL van de AEM-site-uitvoer. U kunt het ook vormen om hen met de naam van het eerste kindonderwerp te vervangen.


Voer de volgende stappen uit om de paginanamen te configureren:

1. Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen.
1. In het configuratiedossier, verstrek de volgende (bezit) details om de paginanamen voor de onderwerpen te vormen.

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.common.SanitizeNodeName` | `nodename.systemDefinedPageName` | Boolean (`true/false`). **Standaardwaarde**: `false` |

Als de eigenschap *@navtitle* in `<topichead>` bijvoorbeeld alle speciale tekens bevat en u de eigenschap `aemsite.pagetitle` instelt op true, wordt standaard een scheidingsteken gebruikt. Als u de eigenschap `nodename.systemDefinedPageName` instelt op true, wordt de naam van het eerste onderliggende onderwerp weergegeven.


### Configureer de regels voor bestandsontsmetting voor het maken van onderwerpen en het publiceren van uitvoer in AEM Sites en andere indelingen {#id2164D0KD0XA}

Als beheerder kunt u een lijst definiëren met geldige speciale tekens die zijn toegestaan in bestandsnamen. Deze tekens vormen uiteindelijk de URL van een AEM Site-uitvoer. In eerdere versies mochten gebruikers bestandsnamen definiëren die speciale tekens bevatten, zoals `@` , `$` , `>` en meer. Deze speciale tekens resulteerden in gecodeerde URL bij het genereren van AEM Site-pagina&#39;s.

Vanaf de release 3.8 zijn configuraties toegevoegd om een lijst met speciale tekens te definiëren die zijn toegestaan in de bestandsnamen. Door gebrek, bevat de geldige filename configuratie &quot;`a-z A-Z 0-9 - _`&quot;. Dit houdt in dat u tijdens het maken van een bestand elk speciaal teken in de bestandstitel kunt hebben, maar dat het intern wordt vervangen door een afbreekstreepje \(`-`\) in de bestandsnaam. U kunt bijvoorbeeld de bestandstitel Introduction 1 of Introduction@1 hebben. De overeenkomstige bestandsnaam die voor beide gevallen wordt gegenereerd, is Introduction-1.

Wanneer u een lijst van geldige karakters bepaalt, herinner dat deze karakters &quot;`*/:[\]|#%{}?&<>"/+`&quot;en `a space` altijd met een koppelteken \ (`-` \) zullen worden vervangen.

>[!NOTE]
>
> Als u de geldige lijst met speciale tekens niet configureert, kan het maken van bestanden onverwachte resultaten opleveren.

Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\) gegevens op om de geldige speciale tekens in bestandsnamen en uitvoer van AEM-site te configureren:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.common.SanitizeNodeNameImpl` | `aemsite.DisallowedFileNameChars` | Controleer of de eigenschap is ingesteld op ``'<>`@$`` . U kunt meer speciale tekens aan deze lijst toevoegen. |

>[!NOTE]
> 
> De bovenstaande configuratie geldt voor alle uitvoerindelingen. Dit betekent dat bij het genereren van een PDF-, HTML- of aangepaste uitvoer de uiteindelijke uitvoer de geconfigureerde regels voor bestandsontsmetting volgt.

U kunt ook andere eigenschappen configureren, zoals kleine letters gebruiken in bestandsnamen, scheidingstekens voor het verwerken van ongeldige tekens en het maximum aantal tekens dat is toegestaan in de bestandsnamen. Om deze eigenschappen te vormen, voeg de volgende zeer belangrijke waardeparen in het configuratiedossier toe:

| Eigenschappensleutel | Waarde van eigenschap |
|------------|--------------|
| `nodename.uselower` | Boolean \(true/false\).<br> **Standaardwaarde**: waar |
| `nodename.separator` | Elk teken. <br> **Standaardwaarde**: \_ *\ (onderstrepingsteken \)* |
| `nodename.maxlength` | Waarde van gehele getallen.<br> **Standaardwaarde**: 50 |

### Samenvoegen van de structuur van AEM-siteknooppunten configureren

Wanneer u de output van de Plaats van AEM produceert, wordt een knoop voor elk element in de onderwerpen intern gecreeerd. Voor een kaart DITA met duizenden onderwerpen, kan deze knoopstructuur te diep worden. Dit type van diep genestelde knoopstructuur kan prestatieskwesties voor grotere plaatsen hebben. De volgende momentopname toont diep genestelde knoopstructuur voor een output van de Plaats van AEM:

![](assets/deep-nested-aem-site-node-structure.png)

In de bovenstaande momentopname, merk op dat er een knoop voor elk `p` element en zijn verdere sub-elementen is gecreeerd en een gelijkaardige structuur wordt gecreeerd voor elk ander element dat in het onderwerp wordt gebruikt.

Met AEM Guides kunt u configureren hoe de knooppuntstructuur van de AEM Site-uitvoer intern wordt gemaakt. U kunt de nodestructuur bij gespecificeerde elementen afvlakken, zo betekent het dat u een element kunt bepalen dat als belangrijkste element zal worden beschouwd en alle sub-elementen binnen het zullen met het belangrijkste element worden samengevoegd. Als u bijvoorbeeld besluit het element `p` af te vlakken, worden alle elementen die in het element `p` worden weergegeven, samengevoegd met het element main `p` . Er wordt geen aparte notitie gemaakt voor een subelement binnen het element `p` . In de volgende momentopname wordt de nodestructuur afgevlakt op het element `p` weergegeven:

![](assets/flattened-aem-site-node-structure.png)

Voer de volgende stappen uit om de nodestructuur van de AEM-site af te vlakken:

1. Identificeer het element\(en\) waarop u de nodestructuur wilt afvlakken:

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

1. Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen.
1. Geef in het configuratiebestand de volgende \(eigenschap\)-details op:

   | PID | Eigenschappensleutel | Waarde van eigenschap |
   |---|------------|--------------|
   | `com.adobe.dxml.flattening.FlatteningConfigurationService` | `flattening.enabled` | Boolean \(true/false\).<br> **Standaardwaarde**: `false` |


Wanneer u nu de AEM Site-uitvoer genereert, worden de knooppunten in het `p` -element samengevoegd en opgeslagen in het `p` -element zelf. U kunt de nieuwe afvlakkingseigenschappen voor het element `p` vinden in CRXDE.

![](assets/flatten-aem-site-note-props-crxde.png)

**Onderzoek een koord binnen de inhoud in de output van de Plaats van AEM**

Standaard kunt u alleen in de AEM Site-uitvoer naar een tekenreeks in de titels zoeken. U kunt het systeem zodanig configureren dat wordt gezocht naar een tekenreeks in zowel de titels als de inhoud of de hoofdtekst van de AEM Site-uitvoer.

>[!NOTE]
>
> Soms werkt uw zoekopdracht mogelijk voor bepaalde elementen in de inhoud, maar u kunt de zoekopdracht zo configureren dat deze voor de gehele inhoud werkt.

![](assets/flatten-aem-site-note-props-crxde-search.png)

Om het onderzoek toe te laten, zou u de afvlakking van de de knoopstructuur van de Plaats van AEM moeten vormen.

VOORZIENING:

U kunt zoeken naar maximaal 1 MB samengevoegde inhoud. In de vorige schermafbeelding kunt u bijvoorbeeld zoeken of de inhoud onder de tag &lt;p\> &lt;= 1Mb is.

>[!NOTE]
>
> Het onderzoek werkt op de elementen slechts als het `<flatten>` attribuut aan waar wordt geplaatst. Standaard is in AEM Guides het kenmerk `<flatten>` ingesteld op true voor veelgebruikte tekstelementen, zoals &lt;p\> &lt;ul\> &lt;lI\>. Als u echter enkele aangepaste elementen hebt gemaakt, moet u het kenmerk `<flatten>` instellen op true in het bestand elementmapping.xml.

**verhinderen afvlakking van de de knoopstructuur van de Plaats van AEM**

Net als het opgeven van het knooppunt dat moet worden samengevoegd in de uitvoer van de AEM-site, kunt u ook een element opgeven dat u wilt uitsluiten van deze configuratie. Als u bijvoorbeeld knooppunten wilt afvlakken op het element `body` , maar geen `table` element `body` wilt afvlakken, kunt u de eigenschap exclude toevoegen binnen de definitie van het element `table` .

Als u het element `table` wilt uitsluiten van afvlakking, voegt u de volgende eigenschap toe aan de definitie van het element `table` :

`<preventancestorflattening>true|false</preventancestorflattening>`

### De versie voor verwijderde pagina&#39;s configureren in AEM Site-uitvoer

Wanneer u de output van de Plaats van AEM met **schrapping en** creeert **&#x200B;**&#x200B;optie die voor het Bestaande plaatsen van de Pagina&#39;s van de Output wordt geselecteerd, wordt een versie gecreeerd voor pagina \(s \) die worden geschrapt. U kunt het systeem vormen om de verwezenlijking van een versie vóór schrapping tegen te houden.

Voer de volgende stappen uit om te stoppen met het maken van een versie voor de pagina\(s\) die wordt verwijderd:

1. Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen.
1. In het configuratiedossier, verstrek de volgende \(bezit \) details om **te vormen creeer geen Versie voor Geschrapte Pagina&#39;s** optie:

   | PID | Eigenschappensleutel | Waarde van eigenschap |
   |---|------------|--------------|
   | `com.adobe.fmdita.confi g.ConfigManager` | `no.version.creation.on.deletion` | Boolean \(true/false\).<br> **Standaardwaarde**: `true` |

   >[!NOTE]
   >
   > Als deze optie is geselecteerd, kunnen gebruikers elke pagina\(s\) rechtstreeks verwijderen zonder daarvoor een versie te maken. Als de optie niet is geselecteerd, wordt een versie gemaakt voordat de pagina\(s\) worden verwijderd.

### Aangepaste rewriter instellen met Experience Manager Guides {#custom-rewriter}

Experience Manager Guides heeft een douane die [**herschrijver** ](https://sling.apache.org/documentation/bundles/output-rewriting-pipelines-org-apache-sling-rewriter.html) module leest voor de behandeling van de verbindingen in het geval van dwars-kaarten (verbindingen tussen de onderwerpen van twee verschillende kaarten) worden geproduceerd. Deze herschrijfconfiguratie is geïnstalleerd op het volgende pad: <br> `/apps/fmdita/config/rewriter/fmdita-crossmap-link-patcher`.

Als u nog een aangepaste schrijfbewerking voor tekenreeksen in uw codebase hebt, gebruikt u een `'order'` -waarde groter dan 50, omdat Experience Manager Guides anders `'order'` 50 gebruikt.  Als u dit wilt overschrijven, hebt u een waarde > 50 nodig. Voor meer details, mening [ Output die pijplijnen herschrijft ](https://sling.apache.org/documentation/bundles/output-rewriting-pipelines-org-apache-sling-rewriter.html).


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

   2. Selecteer het nieuwe gebied om de **Montages** van het gebied te openen.

   3. In het **Etiket van het Gebied**, ga de meta-gegevensnaam— Publiek in.

   4. In de **Kaart aan Bezit** het plaatsen, specificeer./jcr:content/metadata/&lt;naam van de metagegevens\>. We zullen het bijvoorbeeld instellen op ./jcr:content/metadata/publiek.

   Voeg met deze stappen alle vereiste metagegevensparameters toe.

1. Klik **sparen**.


De nieuwe parameter verschijnt nu op de pagina van Eigenschappen voor alle kaarten DITA.

![](assets/properties-page-custom-metadata.PNG)

Vervolgens moet u de aangepaste metagegevens beschikbaar stellen in de DITA-kaartconsole. Voer de volgende stappen uit om de aangepaste metagegevens beschikbaar te maken op het dashboard voor de DITA-kaart:

1. Gebruik pakketbeheer om toegang te krijgen tot het bestand metadataList dat beschikbaar is op de volgende locatie in de Cloud Manager Git-opslagplaats:

   /libs/fmdita/config/metadataList

   >[!NOTE]
   >
   > Het metadataList dossier bevat een lijst van eigenschappen die in de **drop-down lijst van Eigenschappen** van een kaart DITA in het kaartdashboard worden getoond. Standaard worden in dit bestand vier eigenschappen vermeld: docstate, dc:language, dc:description en dc:title.

1. Voeg de aangepaste metagegevens toe die u hebt toegevoegd aan de pagina Forms van het metagegevensschema. Voeg voor ons voorbeeld publieksparameter toe aan het einde van de standaardlijst.


Nu zullen de douanemetagegevens omhoog in de DITA kaartconsole **Eigenschappen** drop-down lijst van Eigenschappen verschijnen.

Ten slotte moet u als uitgever de aangepaste metagegevens opnemen in de gepubliceerde uitvoer. Voer de volgende stappen uit om de aangepaste metagegevens te verwerken tijdens het genereren van de uitvoer:

1. Navigeer in de gebruikersinterface van Assets naar de DITA-kaart die u wilt publiceren.

1. Selecteer het DITA-kaartbestand en open de eigenschappenpagina.

1. Geef op de pagina Eigenschappen de waarde voor de aangepaste metagegevens op. In ons voorbeeld hebben we een waarde van External opgegeven voor de publieksparameter.

   ![](assets/properties-page-custom-metadata-value.png)

1. Klik **sparen &amp; Sluiten**.

1. Klik op het DITA kaartdossier om de DITA kaartconsole te openen.

1. In de **Output stelt** lusje vooraf in, selecteer de output vooraf ingesteld die u wilt gebruiken om de output te produceren.

1. Klik **uitgeven**.

1. Van de **drop-down lijst van Eigenschappen**, selecteer de eigenschappen die u aan het het publiceren proces wilt overgaan.

   ![](assets/props-in-publish-output.PNG)


De geselecteerde eigenschappen/metagegevens worden doorgegeven aan het publicatieproces en beschikbaar gesteld in de uiteindelijke uitvoer.

### Metagegevens valideren die worden doorgegeven aan de DITA-OT voor verwerking

Voor het valideren van de metagegevenswaarden die aan de DITA-OT worden doorgegeven, kan een lokale omgeving worden gebruikt met een pot die klaar is voor de cloud. Omdat we geen toegang hebben tot het lokale bestandssysteem in de cloud, is de enige manier om het metagegevensbestand te valideren via de voor de cloud geschikte poort.

- Bestandsnaam: metadata.xml
- Bestandslocatie: crx-quickstart/profiles/ditamaps/&lt;ditamap-1234\>

  Toegang krijgen tot metadata.xml:

   - Meld u aan bij de serverlocatie waar de AEM-instantie wordt uitgevoerd.
   - Migreren naar crx-quickstart/profiles/ditamaps/&lt;recent-created-directory-name\>/metadata.xml.
- Voorbeeld van bestandsindeling:

  **metadata.xml**

  ```XML
  <?xml version="1.0" encoding="UTF-8" standalone="no"?>
  <root>
     <Path id="/absolutePath/sampleMap.ditamap">
        <metadata>
           <meta isArray="false" key="dc:description">This is a file</meta>
           <meta isArray="false" key="dc:title">Myfile</meta>
           <meta isArray="true" key="multivalueText">One;Two;Three</meta>
        </metadata>
     </Path>
     <Path id="/absolutePath/sampleTopic.dita">
        <metadata>
           <meta isArray="false" key="dc:description">description for the accountability</meta>
           <meta isArray="false" key="dc:title">accountability title</meta>
           <meta isArray="true" key="multivalueText">value1</meta>
        </metadata>
     </Path>
  </root>
  ```


- isArray: een Booleaans kenmerk dat definieert of de metagegevens een meerwaarde \(Array\) zijn of niet. De waarden worden gescheiden door een puntkomma.
- Pad-id: absoluut pad naar het bestand dat is opgeslagen in de tijdelijke map.

>[!NOTE]
>
> Als het bestand geen specifieke metagegevens bevat, wordt &lt;meta\>-tag met de sleutel niet weergegeven als eigenschap voor dat bestand in het bestand metadata.xml.

## Vorm het DITA-OT gebied van de bevellijn argument om wortelkaartmeta-gegevens goed te keuren

Voer de volgende stappen uit om het argumentveld voor de opdrachtregel DITA-OT te gebruiken om metagegevens voor hoofdmapmappen door te geven:

1. Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen.
1. In het configuratiedossier, verstrek de volgende \(bezit \) details om het DITA-OT gebied van het bevellijn argument in Vooraf ingesteld te vormen:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `pass.metadata.args.cmd.line` | Boolean\(`true/false`\).**Standaardwaarde**: `true` |

- Het plaatsen van de bezitswaarde aan **waar** laat de DITA-OT functionaliteit van de bevellijn toe, toestaand u om de meta-gegevens door DITA-OT bevellijn over te gaan.
- Het plaatsen van de bezitswaarde aan **vals** maakt de DITA-OT functionaliteit van de bevellijn onbruikbaar. Vervolgens kunt u het veld Eigenschappen in de voorinstelling gebruiken om de metagegevens door te geven.



## DITA-elementtoewijzing aanpassen met AEM-componenten {#id1679J600HEL}

DITA-elementen in de AEM Guides worden toegewezen aan hun overeenkomstige AEM-componenten. AEM Guides gebruikt deze toewijzing in workflows, zoals publiceren en reviseren, om DITA-elementen om te zetten in een corresponderende AEM-component. De toewijzing wordt gedefinieerd in het `elementmapping.xml` -bestand, dat kan worden geopend met pakketbeheer.

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
        <attribute from="attrname"         to="propname"         ispath="true|false"         rel="source|target" />    
    </attributemap>    
    <skip>true|false</skip> 
</ditaelement>
```

De volgende lijst beschrijft de elementen in het DITA elementenschema:

| Element | Beschrijving |
|-------|-----------|
| `<ditaelement>` | The top-level node for each mapping element. |
| `<class>` | Het klassenkenmerk van het doel-DITA-element waarvoor u de component schrijft.<br> Het klassenkenmerk voor het DITA-onderwerp is bijvoorbeeld: <br> `- topic/topic` |
| `<componentpath>` | Het CRXDE-pad van de toegewezen AEM-component. |
| `<type>` | Mogelijke waarden:<br> -   **COMPOSITE**: Proces de kindelementen eveneens <br> -   **STANDALONE**: Overslaat verwerking van kindelementen |
| `<attributeprop>` | Wordt gebruikt voor het toewijzen van geserialiseerde DITA-kenmerken en -waarden aan AEM-knooppunten als eigenschap. Als u bijvoorbeeld `<note type="Caution">` -element hebt en de component die voor dit element is toegewezen, `<attributeprop>attr_t</ attributeprop>` heeft, worden het kenmerk en de waarde van het knooppunt geserialiseerd naar de eigenschap `attr_t` van het corresponderende AEM-knooppunt \( `attr_t->type="caution"`\). |
| `<textprop>propname_t</textprop>` | De uitvoer van `getTextContent()` opslaan naar de eigenschap die wordt gedefinieerd door `propname_t.` <br> **Nota:** dit is een geoptimaliseerd bezit. |
| `<xmlprop>propname_x </xmlprop>` | Sparen geserialiseerde XML van deze knoop aan bezit dat door `propname_x.<br> `**wordt bepaald Nota:** Dit is een geoptimaliseerd bezit. |
| `<xpath>` | Als het element van XPath in de elementenafbeelding wordt verstrekt, dan samen met elementnaam en klasse zou de voorwaarde van XPath ook voor de componentenafbeelding moeten worden voldaan om te worden gebruikt. |
| `<target>` | Plaats voor het element DITA in de crx bewaarplaats op gespecificeerde plaats.<br> Mogelijke waarden: <br> - **hoofd**: Onder de hoofdknoop <br> - **tekst**: Onder de paragraafknoop |
| `<wrapelement>` | Het HTML-element waarin de inhoud moet worden verpakt. |
| `<wrapclass>` | De elementwaarde voor de eigenschap `wrapclass.` |
| `<attributemap>` | Containerknooppunt met een of meer `<attribute>` knooppunten. |
| `<attribute from="attrname" to="propname" ispath="true|false" rel="source|target" />` | Wijst de DITA-kenmerken toe aan AEM-eigenschappen: <br> -   **`from`**: DITA-kenmerknaam <br> -   **`to`**: AEM-componenteigenschap name <br> -   **`ispath`**: Als het attribuut een wegwaarde \ is (bijvoorbeeld: *beeld* \) <br> -   **`rel`**: als het pad de bron of het doel is <br> **Nota:** als `attrname` met `%` begint, dan kaart `attrname minus '%'` aan steun &#39; `propname`&#39;. |

**Extra nota&#39;s**

- Als u de standaardelement-toewijzing wilt overschrijven, wordt u aangeraden de wijzigingen in het standaard `elementmapping.xml` -bestand niet aan te brengen. Maak een nieuw XML-toewijzingsbestand en plaats het bestand op een andere locatie, bij voorkeur in de aangepaste map voor apps die u maakt.

- In het `elementmapping.xml` -bestand zijn er veel toewijzingsitems die verwijzen naar de component fmdita/components/dita/wrapper. Wrapper is een generische component die relatief eenvoudige concepten DITA gebruikend eigenschappen op hun plaatsknoop teruggeeft om relevante HTML te produceren. De eigenschap `wrapelement` wordt gebruikt om omsluitende tags te genereren en de onderliggende rendering wordt gedelegeerd aan de corresponderende componenten. Dit is handig wanneer u alleen een containercomponent wilt. In plaats van een nieuwe component te maken die een specifieke containertag zoals `div` of `p` rendert, kunt u de component Wrapper met de eigenschappen `wrapelement` en `wrapclass` gebruiken om hetzelfde effect te bereiken.

- Het wordt niet aanbevolen grote hoeveelheden tekst op te slaan in JCR-eigenschappen van String. De geoptimaliseerde berekening van het eigenschapstype bij het genereren van de uitvoer zorgt ervoor dat grote tekstinhoud niet wordt opgeslagen als tekenreekstype. In plaats daarvan, wanneer de inhoud groter dan een bepaalde drempel moet worden bewaard, wordt het type van het bezit veranderd in binair. Door gebrek, wordt deze drempel gevormd aan 512 bytes, maar kan in de Manager van de Configuratie \ (*worden veranderd com.adobe.fmdita.config.ConfigManager* \) door **te veranderen sparen als Binaire Drempel** het plaatsen.

- Als u een deel van \(en niet alle\) van de elementtoewijzingen wilt overschrijven, hoeft u niet het gehele `elementmapping.xml` -bestand te repliceren. U moet een nieuw XML-toewijzingsbestand maken en alleen de elementen definiëren die u overschrijft.

- Nadat u het XML-bestand op de aangepaste locatie hebt gemaakt, werkt u de instelling `Override Element Mapping` in de `com.adobe.fmdita.config.ConfigManager` -bundel bij.


## DITA-kaartconsole aanpassen {#id188HC08M0CZ}

AEM Guides biedt u de flexibiliteit om de mogelijkheden van de DITA kaartconsole uit te breiden. Als u bijvoorbeeld een set rapporten hebt die afwijkt van de beschikbare rapporten in de AEM Guides, kunt u dergelijke rapporten toevoegen aan de kaartconsole. Als u de kaartconsole wilt aanpassen, moet u een AEM Client Library \(of ClientLib\) maken die de code bevat om de vereiste functionaliteit uit te voeren.

>[!NOTE]
>
> Directe aanpassing aan pagina-onderdelen wordt niet aanbevolen, omdat deze wordt overschreven door nieuwe versies van het product.

AEM Guides biedt de categorie `apps.fmdita.dashboard-extn` voor het aanpassen van de kaartconsole. Wanneer de kaartconsole wordt geladen, wordt de functionaliteit die onder de categorie `apps.fmdita.dashboard-extn` wordt gemaakt, uitgevoerd en geladen.

>[!NOTE]
>
> Voor meer informatie over het creëren van de Bibliotheek van de Cliënt van AEM, zie [ Gebruikend cliënt-Kant Bibliotheken ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html?lang=nl-NL).

## Afbeeldingsuitvoering afhandelen tijdens het genereren van de uitvoer {#id177BF0G0VY4}

AEM wordt geleverd met een set standaardworkflows en mediapandgrepen voor het verwerken van middelen. In AEM zijn er vooraf gedefinieerde workflows voor het verwerken van elementen voor de meest gangbare MIME-typen. Doorgaans maakt AEM voor elke afbeelding die u uploadt, meerdere uitvoeringen van dezelfde indeling in binaire indeling. Deze vertoningen kunnen van verschillende grootte, met een verschillende resolutie, met een toegevoegd watermerk, of één of andere andere veranderde eigenschap zijn. Voor meer informatie over hoe AEM activa behandelt, zie [ Assets die de Handlers en de Werkschema&#39;s van Media van de Verwerking gebruikt ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html?lang=nl-NL) in de documentatie van AEM.

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

`/var/dxml/metadata/outputHistory`

Over een periode, kon de collectieve grootte van alle logboekdossiers in GBs lopen. Met AEM Guides kunt u een tijdsperiode configureren om deze logbestanden in de opslagplaats te bewaren. Na de opgegeven tijdsperiode worden de logbestanden samen met de productiegeschiedenis van de uitvoer verwijderd uit de opslagplaats.

>[!NOTE]
>
> De geschiedenis van de outputgeneratie is de logboekingang in de Gegenereerde lijst van Output op het lusje van Output.

Het configureren van de functie voor het opschonen van historie heeft invloed op de uitvoergeneratie voor alle DITA-kaarten in de opslagplaats. Op het lusje van Output van een kaart DITA, wordt de geschiedenis gezuiverd na het gespecificeerde aantal dagen en op de tijd die in het plaatsen wordt gespecificeerd.

>[!NOTE]
>
> Het verwijderen van de logbestanden en de productiegeschiedenis van de uitvoer heeft geen invloed op de gegenereerde uitvoer.

Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om een dag en tijd in te stellen voor het wissen van de uitvoergeschiedenis en logboeken:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `output.history.purgeperiod` | Geef het aantal dagen op waarna de uitvoergeschiedenis en de uitvoerlogboeken worden gewist. Als u deze functie wilt uitschakelen, stelt u deze eigenschap in op 0.Elke dag op het opgegeven tijdstip dat het leegmaken wordt uitgevoerd op uitvoerbestanden die worden gegenereerd vóór het aantal dagen dat in deze eigenschap is opgegeven. <br> **Standaardwaarde**: 5 |
| `output.history.purgetime` | Geef de tijd op waarop het zuiveringsproces wordt gestart. <br> **Standaardwaarde**: 0:00 \ (of 12:00 middernacht\) |

## De onlangs gegenereerde limieten in de lijst met uitvoerbestanden wijzigen {#id1679JH0H0O2}

U kunt het maximumaantal geproduceerde output veranderen die in het lusje van Output voor een kaart DITA wordt getoond.

Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om het aantal uitvoerbestanden te wijzigen dat in de lijst moet worden weergegeven:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `output.historylimit` | Waarde van gehele getallen.<br> **Standaardwaarde**: 25 |

>[!TIP]
>
> Zie de *de geschiedenissectie van de Output* in de gids van Beste praktijken voor beste praktijken rond het werken met outputgeschiedenis.

