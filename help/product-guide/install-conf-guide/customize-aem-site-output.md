---
title: Instellingen voor uitvoergeneratie configureren
description: Leer hoe u instellingen voor uitvoergeneratie configureert
feature: Output Generation
role: Admin
level: Experienced
exl-id: 0849544d-fa7b-4c66-b418-1ffcd1ca09df
source-git-commit: d5dbd67ba44735cf1545291e9a03e3096acd8166
workflow-type: tm+mt
source-wordcount: '3190'
ht-degree: 0%

---

# Bestaande AEM-site-uitvoer aanpassen {#id166TG0B30WR}

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
> Zie de *AEM Plaats het publiceren* sectie in de [&#x200B; gids van Beste praktijken &#x200B;](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/cs-mar-22/Adobe-Experience-Manager-Guides_Best-Practices_EN.pdf) voor beste praktijken rond het creëren van de output van de Plaats van AEM.


## Ontwerpsjabloon aanpassen voor het genereren van uitvoer {#customize_xml-add-on}

De AEM Guides gebruikt een set vooraf gedefinieerde ontwerpsjablonen om AEM Site-uitvoer te genereren. U kunt de AEM Guides-ontwerpsjablonen aanpassen om de uitvoer te genereren die in overeenstemming is met uw bedrijfsbranding. Een ontwerpsjabloon is een verzameling van verschillende stijlen \(CSS\), scripts \(zowel server- als client-side\), bronnen \(afbeeldingen, logo&#39;s en andere elementen\) en JCR-knooppunten die al deze bronnen aan elkaar koppelen. Een ontwerpsjabloon kan zo eenvoudig zijn als één serverscript met slechts een paar JCR-knooppunten of een complexe combinatie van stijlen, bronnen en JCR-knooppunten. De malplaatjes van het ontwerp worden gebruikt door het publiceren subsysteem van AEM Guides terwijl het produceren van de output van de Plaats van AEM en zij controleren de structuur, de blik en het gevoel van de geproduceerde output.

Er is geen beperking ten aanzien van waar de middelen van het ontwerpmalplaatje op de server zouden moeten worden gevestigd, maar zij zijn gewoonlijk logisch georganiseerd volgens hun functie. In de standaardsjabloon worden bijvoorbeeld alle JavaScript- en CSS-bestanden opgeslagen in de map `/etc/designs/fmdita/clientlibs/siteoutput/default` . Waar deze bestanden zich bevinden, worden ze aan elkaar gekoppeld door een verzameling JCR-knooppunten. Samen vormen deze JCR-knooppunten en de bestanden de hele ontwerpsjabloon.

Het standaardontwerpmalplaatje dat met AEM Guides wordt verscheept staat u toe om het landen, het onderwerp, en de componenten van de onderzoekspagina aan te passen. U kunt een kopie maken van het standaardontwerp en de bijbehorende verwijzingssjablonen en verschillende componenten opgeven om de gewenste uitvoer te genereren.

Op de volgende tabbladen vindt u instructies voor het opgeven van uw eigen ontwerpsjabloon voor het genereren van de AEM-site-uitvoer op basis van uw Experience Manager Guides-instelling: Cloud Service of On-Premise.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

1. Gebruik de Manager van het Pakket om het standaardontwerpmalplaatje van de volgende plaats te downloaden:

   /libs/fmdita/config/templates

1. Maak een kopie van de gedownloade bestanden op de volgende locatie in de Cloud Manager Git-opslagplaats:

   /apps/fmdita/config/templates

1. U moet ook de sjablonen downloaden en kopiëren waarnaar wordt verwezen vanuit het standaardsjabloonknooppunt. De sjablonen waarnaar wordt verwezen worden onder:

   /libs/fmdita/templates/default/cqtemplates

>[!TAB  Op locatie ]

1. Meld u aan bij AEM en open de CRXDE Lite-modus.

1. Navigeer naar het standaardontwerpsjabloonknooppunt. De locatie van het standaardontwerpsjabloonknooppunt is:

   `/libs/fmdita/config/templates/`

   ![](assets/templates-node.png){width="300" align="left"}

   >[!NOTE]
   >
   > Maak een kopie van de standaardontwerpsjablonen vanuit de map `libs` naar de map `apps` en breng wijzigingen aan in de map `apps` . U moet ook wijzigingen aanbrengen in de sjablonen waarnaar wordt verwezen vanuit het standaardsjabloonknooppunt. De sjablonen waarnaar wordt verwezen, worden onder het knooppunt `/libs/fmdita/templates/default/cqtemplates` geplaatst. Maak een kopie van de sjablonen waarnaar wordt verwezen in de map `apps` voordat u wijzigingen aanbrengt.

1. Klik de *standaard* component in de *malplaatjes* knoop om tot zijn eigenschappen toegang te hebben.

>[!ENDTABS]

De eigenschappen van de AEM Guides-ontwerpsjabloon worden in de volgende tabel beschreven.

| Eigenschap | Beschrijving |
|--------|-----------|
| `landingPageTemplate`, `searchPageTemplate`, `topicPageTemplate`, `shadowPageTemplate` | Geef het knooppunt `cq:Template` voor deze overeenkomende pagina&#39;s op \(landen, zoeken en onderwerpen\). Standaard is het knooppunt `cq:Template` voor deze pagina&#39;s te vinden in het knooppunt `/libs/fmdita/templates/default/cqtemplates` . Deze knoop bepaalt de structuur en de eigenschappen van het landen, het onderzoek, en onderwerppagina&#39;s.<br> De `shadowPageTemplate` wordt gebruikt om de inhoud die is afgekapt te optimaliseren. U moet de waarde van deze eigenschap instellen op: `fmdita/templates/default/cqtemplates/shadowpage` <br> **Nota:** u moet een waarde voor `topicPageTemplate` specificeren. De eigenschappen `landingPageTemplate` en `searchPageTemplate` zijn optioneel. Geef deze eigenschappen niet op als u niet wilt dat de zoek- en bestemmingspagina&#39;s worden gegenereerd. |
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

Voor meer informatie, zie [&#x200B; Creërend uw eerste website van Adobe Experience Manager &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html?lang=nl-NL) en [&#x200B; de Grondbeginselen &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/develop-wknd-tutorial.html?lang=nl-NL) van het ontwikkelen van uw eigen website op AEM.

## Documenttitel gebruiken om uitvoer van AEM-sites te genereren

Bij het genereren van de uitvoer van de AEM-site speelt de manier waarop URL&#39;s worden gegenereerd een belangrijke rol bij de detecteerbaarheid van uw inhoud. Als u op UUID gebaseerde bestandsnamen gebruikt, is het genereren van URL&#39;s op basis van UUID van uw bestanden niet zoekvriendelijk. Als Beheerder of Uitgever, hebt u de controle over hoe u URLs voor uw uitvoer van de Plaats van AEM wilt produceren. AEM Guides biedt u een configuratie waarmee u URL&#39;s van AEM Site-uitvoer kunt genereren met de bestandstitel in plaats van de op UUID gebaseerde bestandsnamen. Voor op UUID gebaseerde bestandssystemen is deze optie standaard ingeschakeld. Dit impliceerde dat wanneer u de output van de Plaats van AEM voor op UUID-Gebaseerde dossiersystemen produceert, de titels van het dossier worden gebruikt om URLs en niet UUIDs van de dossiers te produceren.

Voor installatie op locatie met niet-UUID-gebaseerde bestandssystemen wordt de uitvoer van de AEM-site gegenereerd met de bestandsnamen en niet met de titels van het bestand. Deze optie is standaard uitgeschakeld. Dit impliceerde dat wanneer u de output van de Plaats van AEM produceert, de dossiernamen worden gebruikt om URLs en niet de titel van het dossier te produceren. U kunt ervoor kiezen de URL&#39;s te genereren op basis van de bestandstitels door deze optie in te schakelen.

Op de volgende tabbladen vindt u instructies voor het configureren van het genereren van URL&#39;s in AEM Site-uitvoer op basis van uw Experience Manager Guides-instellingen: Cloud Service of On-Premise.

>[!NOTE]
>
> U kunt regels verder configureren om alleen een set tekens toe te staan in de URL&#39;s van een AEM-site-uitvoer. Voor meer details, zie [&#x200B; filename ontsmettingsregels voor het creëren van onderwerpen en het publiceren van de output van de Plaats van AEM &#x200B;](#id2164D0KD0XA) vormen.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om de URL&#39;s te configureren die worden gegenereerd in AEM Site-uitvoer:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `aemsite.pagetitle` | Boolean \(true/false\). Als u uitvoer wilt genereren met de paginatitel, stelt u deze eigenschap in op true. Standaard, wordt het geplaatst om het dossier te gebruiken - noem.<br> **Standaardwaarde**: vals |


>[!TAB  Op locatie ]

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

>[!ENDTABS]

## De URL van de AEM Site-uitvoer configureren om de documenttitel te gebruiken (alleen voor Cloud Service)

U kunt de documenttitels in URL van de output van de Plaats van AEM gebruiken. Als de bestandsnaam niet bestaat of alle speciale tekens bevat, kunt u het systeem zo configureren dat de speciale tekens worden vervangen door een scheidingsteken in de URL van de AEM-site-uitvoer. U kunt het ook vormen om hen met de naam van het eerste kindonderwerp te vervangen.


Voer de volgende stappen uit om de paginanamen te configureren:

1. Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-config-override.md#) om het configuratiedossier tot stand te brengen.
1. In het configuratiedossier, verstrek de volgende (bezit) details om de paginanamen voor de onderwerpen te vormen.

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.common.SanitizeNodeName` | `nodename.systemDefinedPageName` | Boolean (`true/false`). **Standaardwaarde**: `false` |

Als de eigenschap *@navtitle* in `<topichead>` bijvoorbeeld alle speciale tekens bevat en u de eigenschap `aemsite.pagetitle` instelt op true, wordt standaard een scheidingsteken gebruikt. Als u de eigenschap `nodename.systemDefinedPageName` instelt op true, wordt de naam van het eerste onderliggende onderwerp weergegeven.


## Configureer de regels voor bestandsontsmetting voor het maken van onderwerpen en het publiceren van uitvoer in AEM Sites en andere indelingen {#id2164D0KD0XA}

Als beheerder kunt u een lijst definiëren met geldige speciale tekens die zijn toegestaan in bestandsnamen. Deze tekens vormen uiteindelijk de URL van een AEM Site-uitvoer. In eerdere versies mochten gebruikers bestandsnamen definiëren die speciale tekens bevatten, zoals `@` , `$` , `>` en meer. Deze speciale tekens resulteerden in gecodeerde URL bij het genereren van AEM Site-pagina&#39;s.

Vanaf de release 3.8 zijn configuraties toegevoegd om een lijst met speciale tekens te definiëren die zijn toegestaan in de bestandsnamen. Door gebrek, bevat de geldige filename configuratie &quot;`a-z A-Z 0-9 - _`&quot;. Dit houdt in dat u tijdens het maken van een bestand elk speciaal teken in de bestandstitel kunt hebben, maar dat het intern wordt vervangen door een afbreekstreepje \(`-`\) in de bestandsnaam. U kunt bijvoorbeeld de bestandstitel Introduction 1 of Introduction@1 hebben. De overeenkomstige bestandsnaam die voor beide gevallen wordt gegenereerd, is Introduction-1.

Wanneer u een lijst van geldige karakters bepaalt, herinner dat deze karakters &quot;`*/:[\]|#%{}?&<>"/+`&quot;en `a space` altijd met een koppelteken \ (`-` \) zullen worden vervangen.

>[!NOTE]
>
> Als u de geldige lijst met speciale tekens niet configureert, kan het maken van bestanden onverwachte resultaten opleveren.

Op de volgende tabbladen vindt u instructies voor het configureren van de geldige speciale tekens in bestandsnamen en uitvoer van de AEM-site op basis van uw Experience Manager Guides-instellingen: Cloud Service of On-Premise.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\) gegevens op om de geldige speciale tekens in bestandsnamen en uitvoer van AEM-site te configureren:

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

>[!TAB  Op locatie ]

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

>[!ENDTABS]

## Samenvoegen van de structuur van AEM-siteknooppunten configureren

Wanneer u de output van de Plaats van AEM produceert, wordt een knoop voor elk element in de onderwerpen intern gecreeerd. Voor een kaart DITA met duizenden onderwerpen, kan deze knoopstructuur te diep worden. Dit type van diep genestelde knoopstructuur kan prestatieskwesties voor grotere plaatsen hebben. De volgende momentopname toont diep genestelde knoopstructuur voor een output van de Plaats van AEM:

![](assets/deep-nested-aem-site-node-structure.png)

In de bovenstaande momentopname, merk op dat er een knoop voor elk `p` element en zijn verdere sub-elementen is gecreeerd en een gelijkaardige structuur wordt gecreeerd voor elk ander element dat in het onderwerp wordt gebruikt.

Met AEM Guides kunt u configureren hoe de knooppuntstructuur van de AEM Site-uitvoer intern wordt gemaakt. U kunt de nodestructuur bij gespecificeerde elementen afvlakken, zo betekent het dat u een element kunt bepalen dat als belangrijkste element zal worden beschouwd en alle sub-elementen binnen het zullen met het belangrijkste element worden samengevoegd. Als u bijvoorbeeld besluit het element `p` af te vlakken, worden alle elementen die in het element `p` worden weergegeven, samengevoegd met het element main `p` . Er wordt geen aparte notitie gemaakt voor een subelement binnen het element `p` . In de volgende momentopname wordt de nodestructuur afgevlakt op het element `p` weergegeven:

![](assets/flattened-aem-site-node-structure.png)

Op de volgende tabbladen vindt u instructies voor het afvlakken van de nodestructuur van de AEM-site op basis van uw Experience Manager Guides-instellingen: Cloud Service of On-Premise.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

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

1. Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-config-override.md#) om het configuratiedossier tot stand te brengen.
1. Geef in het configuratiebestand de volgende \(eigenschap\)-details op:

   | PID | Eigenschappensleutel | Waarde van eigenschap |
   |---|------------|--------------|
   | `com.adobe.dxml.flattening.FlatteningConfigurationService` | `flattening.enabled` | Boolean \(true/false\).<br> **Standaardwaarde**: `false` |


Wanneer u nu de AEM Site-uitvoer genereert, worden de knooppunten in het `p` -element samengevoegd en opgeslagen in het `p` -element zelf. U kunt de nieuwe afvlakkingseigenschappen voor het element `p` vinden in CRXDE.

![](assets/flatten-aem-site-note-props-crxde.png)

>[!TAB  Op locatie ]

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

>[!ENDTABS]

**Onderzoek een koord binnen de inhoud in de output van de Plaats van AEM (slechts voor Cloud Service)**

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

## De versie voor verwijderde pagina&#39;s configureren in AEM Site-uitvoer

Wanneer u de output van de Plaats van AEM met **schrapping en** creeert **&#x200B;**&#x200B;optie die voor het Bestaande plaatsen van de Pagina&#39;s van de Output wordt geselecteerd, wordt een versie gecreeerd voor pagina \(s \) die worden geschrapt. U kunt het systeem vormen om de verwezenlijking van een versie vóór schrapping tegen te houden.

Op de volgende tabbladen vindt u instructies om te voorkomen dat er een versie voor de pagina\(s\) wordt gemaakt die wordt verwijderd op basis van de Experience Manager Guides-instellingen: Cloud Service of On-Premise.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

1. Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-config-override.md#) om het configuratiedossier tot stand te brengen.
1. In het configuratiedossier, verstrek de volgende \(bezit \) details om **te vormen creeer geen Versie voor Geschrapte Pagina&#39;s** optie:

   | PID | Eigenschappensleutel | Waarde van eigenschap |
   |---|------------|--------------|
   | `com.adobe.fmdita.confi g.ConfigManager` | `no.version.creation.on.deletion` | Boolean \(true/false\).<br> **Standaardwaarde**: `true` |

   >[!NOTE]
   >
   > Als deze optie is geselecteerd, kunnen gebruikers elke pagina\(s\) rechtstreeks verwijderen zonder daarvoor een versie te maken. Als de optie niet is geselecteerd, wordt een versie gemaakt voordat de pagina\(s\) worden verwijderd.

>[!TAB  Op locatie ]

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

>[!ENDTABS]

## Aangepaste rewriter instellen met Experience Manager Guides (alleen voor Cloud Service) {#custom-rewriter}

Experience Manager Guides heeft een douane die [**herschrijver** &#x200B;](https://sling.apache.org/documentation/bundles/output-rewriting-pipelines-org-apache-sling-rewriter.html) module leest voor de behandeling van de verbindingen in het geval van dwars-kaarten (verbindingen tussen de onderwerpen van twee verschillende kaarten) worden geproduceerd. Deze herschrijfconfiguratie is geïnstalleerd op het volgende pad: <br> `/apps/fmdita/config/rewriter/fmdita-crossmap-link-patcher`.

Als u nog een aangepaste schrijfbewerking voor tekenreeksen in uw codebase hebt, gebruikt u een `'order'` -waarde groter dan 50, omdat Experience Manager Guides anders `'order'` 50 gebruikt.  Als u dit wilt overschrijven, hebt u een waarde > 50 nodig. Voor meer details, mening [&#x200B; Output die pijplijnen herschrijft &#x200B;](https://sling.apache.org/documentation/bundles/output-rewriting-pipelines-org-apache-sling-rewriter.html).
