---
title: Instellingen voor uitvoergeneratie configureren
description: Leer hoe u instellingen voor uitvoergeneratie configureert
feature: Output Generation
role: Admin
level: Experienced
source-git-commit: 6f3f05419f4f5cdd45ab580cdee6fa869f20f01d
workflow-type: tm+mt
source-wordcount: '3314'
ht-degree: 0%

---

# Instellingen voor uitvoergeneratie configureren {#id181AI0B0E30}

AEM Guides wordt geleverd met veel configuratieopties waarmee u het productieproces voor uitvoer kunt aanpassen. Dit onderwerp behandelt alle configuraties en aanpassingen die u aan opstelling uw proces van de outputgeneratie zouden helpen.

## Het tabblad Basislijn op het dashboard voor de DITA-kaart configureren {#id223MD0D0YRM}

Op de volgende tabbladen vindt u instructies voor het verbergen van het tabblad Basislijn op het dashboard voor de DITA-kaart op basis van uw Experience Manager Guides-instellingen: Cloud Service of Op locatie.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

1. Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-config-override.md#) om het configuratiedossier tot stand te brengen.
1. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om het basislijntabblad op het kaartdashboard te configureren.

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `hide.tabs.baseline` | Boolean\(`true/false`\).**Standaardwaarde**: `true` |

>[!NOTE]
>
> Deze configuratie is standaard ingeschakeld en het tabblad Basislijn is niet beschikbaar op het kaartdashboard.

>[!TAB  Op locatie ]

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

>[!ENDTABS]


## Overvloeien publiceren configureren binnen een bestaande AEM-site {#id1691I0V0MGR}

Als u een AEM-site hebt die DITA-inhoud bevat, kunt u uw AEM-site-uitvoer zo configureren dat DITA-inhoud wordt gepubliceerd naar een vooraf gedefinieerde locatie op uw site. In de volgende schermafbeelding van een AEM Site-pagina is het knooppunt `ditacontent` bijvoorbeeld gereserveerd voor het opslaan van DITA-inhoud:

![](assets/publish-in-aem-site.png)

De resterende knooppunten op de pagina worden rechtstreeks vanuit de AEM Site-editor gemaakt. Als u de publicatie-instelling configureert voor het publiceren van DITA-inhoud op een vooraf gedefinieerde locatie, weet u zeker dat geen van uw bestaande niet-DITA-inhoud wordt gewijzigd door het AEM Guides-publicatieproces.

U moet de volgende configuraties op uw bestaande plaats uitvoeren om het publiceren van inhoud DITA aan een vooraf bepaalde knoop toe te staan:

- De sjablooneigenschappen van uw site configureren

- Knooppunten op uw site toevoegen om DITA-inhoud te publiceren


Op de volgende tabbladen vindt u instructies voor het configureren van de sjablooneigenschappen van uw bestaande site op basis van uw Experience Manager Guides-instellingen: Cloud Service of On-Premise.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

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

>[!TAB  Op locatie ]

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

>[!ENDTABS]

## Basisuitvoerlocatie voor publicatie configureren

Op de volgende tabbladen vindt u instructies voor het configureren van de basisuitvoerlocatie op basis van uw Experience Manager Guides-configuratie: Cloud Service of On-Premise.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

1. Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-config-override.md) om het configuratiedossier tot stand te brengen.

1. In het configuratiedossier, verstrek de volgende (bezit) details om de plaats van de basisoutput te vormen:

   | PID | Eigenschappensleutel | Waarde van eigenschap |
   |---|---|---|
   | `com.adobe.fmdita.config.ConfigManager` | `base.output.path` | **Standaardwaarde:** &quot;/content/dam/fmdita-outputs&quot; |

>[!TAB  Op locatie ]

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en selecteer *com.adobe.fmdita.config.ConfigManager* bundel.

1. Werk het bezit **Plaats van de Output van de Basis** bij om de standaardweg in de bewaarplaats van AEM te specificeren waar PDF na het publiceren zal worden bewaard. Als er een ongeldig pad wordt ingevoerd, wordt bovendien automatisch het standaardpad `/content/dam/fmdita-outputs` gebruikt.

1. Klik **sparen**.

>[!ENDTABS]

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

   4. In de **Kaart aan Bezit** het plaatsen, specificeer./jcr:content/metadata/&lt;name of the metadata\>. We zullen het bijvoorbeeld instellen op ./jcr:content /metadata/publiek.

   Voeg met deze stappen alle vereiste metagegevensparameters toe.

1. Klik **sparen**.


De nieuwe parameter verschijnt nu op de pagina van Eigenschappen voor alle kaarten DITA.

![](assets/properties-page-custom-metadata.PNG)

Vervolgens moet u de aangepaste metagegevens beschikbaar stellen in de DITA-kaartconsole. Op de volgende tabbladen vindt u instructies voor het beschikbaar maken van de aangepaste metagegevens op het dashboard voor de DITA-kaart op basis van uw Experience Manager Guides-instellingen: Cloud Service of On-Premise.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

1. Gebruik pakketbeheer om toegang te krijgen tot het bestand metadataList dat beschikbaar is op de volgende locatie in de Cloud Manager Git-opslagplaats:

   /libs/fmdita/config/metadataList

   >[!NOTE]
   >
   > Het metadataList dossier bevat een lijst van eigenschappen die in de **drop-down lijst van Eigenschappen** van een kaart DITA in het kaartdashboard worden getoond. Door gebrek, zijn er vier eigenschappen die in dit dossier worden vermeld— docstate, dc :language, dc :description, en dc :title.

1. Voeg de aangepaste metagegevens toe die u hebt toegevoegd aan de pagina Forms van het metagegevensschema. Voeg voor ons voorbeeld publieksparameter toe aan het einde van de standaardlijst.

>[!TAB  Op locatie ]

1. Meld u aan bij AEM en open de CRXDE Lite-modus.

1. Open het bestand metadataList dat beschikbaar is op de volgende locatie:

   /libs/fmdita/config/metadataList

   >[!NOTE]
   >
   > Het metadataList dossier bevat een lijst van eigenschappen die in de **drop-down lijst van Eigenschappen** van een kaart DITA in het kaartdashboard worden getoond. Door gebrek, zijn er vier eigenschappen die in dit dossier worden vermeld— docstate, dc :language, dc :description, en dc :title.

1. Voeg de aangepaste metagegevens toe die u hebt toegevoegd aan de pagina Forms van het metagegevensschema. Voeg voor ons voorbeeld publieksparameter toe aan het einde van de standaardlijst.

1. Klik **sparen allen**.

>[!ENDTABS]

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

### Metagegevens valideren die worden doorgegeven aan de DITA-OT voor verwerking (alleen voor Cloud Service)

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

## Vorm het DITA-OT gebied van de bevellijn argument om wortelkaartmeta-gegevens (slechts voor Cloud Service) goed te keuren

Voer de volgende stappen uit om het argumentveld voor de opdrachtregel DITA-OT te gebruiken om metagegevens voor hoofdmapmappen door te geven:

1. Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-config-override.md#) om het configuratiedossier tot stand te brengen.
1. In het configuratiedossier, verstrek de volgende \(bezit \) details om het DITA-OT gebied van het bevellijn argument in Vooraf ingesteld te vormen:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `pass.metadata.args.cmd.line` | Boolean\(`true/false`\).**Standaardwaarde**: `true` |

- Het plaatsen van de bezitswaarde aan **waar** laat de DITA-OT functionaliteit van de bevellijn toe, toestaand u om de meta-gegevens door DITA-OT bevellijn over te gaan.
- Het plaatsen van de bezitswaarde aan **vals** maakt de DITA-OT functionaliteit van de bevellijn onbruikbaar. Vervolgens kunt u het veld Eigenschappen in de voorinstelling gebruiken om de metagegevens door te geven.

## DITA-kaartconsole aanpassen {#id188HC08M0CZ}

AEM Guides biedt u de flexibiliteit om de mogelijkheden van de DITA kaartconsole uit te breiden. Als u bijvoorbeeld een set rapporten hebt die afwijkt van de beschikbare rapporten in de AEM Guides, kunt u dergelijke rapporten toevoegen aan de kaartconsole. Als u de kaartconsole wilt aanpassen, moet u een AEM Client Library \(of ClientLib\) maken die de code bevat om de vereiste functionaliteit uit te voeren.

>[!NOTE]
>
> Directe aanpassing aan pagina-onderdelen wordt niet aanbevolen, omdat deze wordt overschreven door nieuwe versies van het product.

AEM Guides biedt de categorie `apps.fmdita.dashboard-extn` voor het aanpassen van de kaartconsole. Wanneer de kaartconsole wordt geladen, wordt de functionaliteit die onder de categorie `apps.fmdita.dashboard-extn` wordt gemaakt, uitgevoerd en geladen.

>[!NOTE]
>
> Voor meer informatie over het creëren van de Bibliotheek van de Cliënt van AEM, zie [&#x200B; Gebruikend cliënt-Kant Bibliotheken &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html?lang=en).

## Afbeeldingsuitvoering afhandelen tijdens het genereren van de uitvoer {#id177BF0G0VY4}

AEM wordt geleverd met een set standaardworkflows en mediapandgrepen voor het verwerken van middelen. In AEM zijn er vooraf gedefinieerde workflows voor het verwerken van elementen voor de meest gangbare MIME-typen. Doorgaans maakt AEM voor elke afbeelding die u uploadt, meerdere uitvoeringen van dezelfde indeling in binaire indeling. Deze vertoningen kunnen van verschillende grootte, met een verschillende resolutie, met een toegevoegd watermerk, of één of andere andere veranderde eigenschap zijn. Voor meer informatie over hoe AEM activa behandelt, zie [&#x200B; Assets die de Handlers en de Werkschema&#39;s van Media van de Verwerking gebruikt &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html?lang=en) in de documentatie van AEM.

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
      <rendition output="HTML5" outputName="ditahtml5">cq5dam.thumbnail.319.319.png</rendition>
      <rendition output="EPUB">cq5dam.web.1280.1280.jpeg</rendition>
      <rendition output="CUSTOM">cq5dam.web.1280.1280.jpeg</rendition>
   </mapelement>
...
</renditionmap>
```

Het element `mimetype` geeft het MIME-type van de bestandsindeling aan. Het element `rendition output` geeft het type uitvoerindeling en de naam van de uitvoering \(bijvoorbeeld `cq5dam.web.1280.1280.jpeg`\) aan die moet worden gebruikt voor het publiceren van de opgegeven uitvoer. U kunt de afbeeldingsuitvoeringen opgeven die moeten worden gebruikt voor alle ondersteunde uitvoerindelingen: AEMSITE, PDF, HTML5, EPUB en CUSTOM.

Als u verschillende afbeeldingsuitvoeringen wilt opgeven voor een uitvoervoorinstelling, kunt u het kenmerk `outputName` met de waarde ingesteld op de titel van de voorinstelling gebruiken om aangepaste uitvoeringen te definiëren voor specifieke uitvoervoorinstellingen onder hetzelfde uitvoertype. Dit is handig wanneer u verschillende afbeeldingsgrootten of indelingen voor verschillende publicatiescenario&#39;s nodig hebt.

Bijvoorbeeld:


```XML
<renditionmap>
   <mapelement>
      <mimetype>image/png</mimetype>
      
      <rendition output="HTML5">cq5dam.web.1280.1280.jpeg</rendition>
      <rendition output="HTML5" outputName="ditahtml5">cq5dam.thumbnail.319.319.png</rendition>
      
   </mapelement>
...
</renditionmap>
```

Wanneer in de bovenstaande uitvoeringen het kenmerk `outputName` is ingesteld op `ditahtml5` (titel van voorinstelling), gebruikt de voorinstelling `ditahtml5` de miniatuurafbeelding `cq5dam.thumbnail.319.319.png` . Als het kenmerk `outputName` niet is opgegeven, gebruiken alle HTML5-uitvoerbestanden de grotere afbeelding `cq5dam.web.1280.1280.jpeg` .

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

Op de volgende tabbladen vindt u instructies voor het instellen van een dag en tijd voor het wissen van de uitvoergeschiedenis en de logbestanden op basis van de Experience Manager Guides-instellingen: Cloud Service of On-Premise.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om een dag en tijd in te stellen voor het wissen van de uitvoergeschiedenis en logboeken:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager\|output.history.purgeperiod` | Geef het aantal dagen op waarna de uitvoergeschiedenis en de uitvoerlogboeken worden gewist. Als u deze functie wilt uitschakelen, stelt u deze eigenschap in op 0.Elke dag op het opgegeven tijdstip dat het leegmaken wordt uitgevoerd op uitvoerbestanden die worden gegenereerd vóór het aantal dagen dat in deze eigenschap is opgegeven. | **Standaardwaarde**: 5 |
| `output.history.purgetime` | Geef de tijd op waarop het zuiveringsproces wordt gestart. | **Standaardwaarde**: 0 :00 \ (of 12 :00 middernacht \) |

>[!TAB  Op locatie ]

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

>[!ENDTABS]

## De onlangs gegenereerde limieten in de lijst met uitvoerbestanden wijzigen {#id1679JH0H0O2}

U kunt het maximumaantal geproduceerde output veranderen die in het lusje van Output voor een kaart DITA wordt getoond.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om het aantal uitvoerbestanden te wijzigen dat in de lijst moet worden weergegeven:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `output.historylimit` | Waarde van gehele getallen.<br> **Standaardwaarde**: 25 |

>[!TAB  Op locatie ]

Standaard wordt een lijst met de laatste 25 gegenereerde uitvoerbestanden weergegeven. Om het aantal output te veranderen om in de lijst te tonen, werk de **Limiet van de Lijst van Output** het plaatsen in de `com.adobe.fmdita.config.ConfigManager` bundel bij.

>[!ENDTABS]

>[!TIP]
>
> Zie de *de geschiedenissectie van de Output* in de [&#x200B; gids van Beste praktijken &#x200B;](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/cs-mar-22/Adobe-Experience-Manager-Guides_Best-Practices_EN.pdf) voor beste praktijken rond het werken met outputgeschiedenis.

## Optimalisatie van uitvoergeneratieprestaties (alleen voor op locatie) {#id176LB050VUI}

AEM Guides staat u toe om de grootte van de de generatieprocessen van de outputproductie te vormen die het aantal processen van de outputgeneratie controleert die gelijktijdig lopen. Standaard is de grootte van de procespool ingesteld op het aantal verwerkingskernen dat beschikbaar is in uw systeem plus één. U kunt deze waarde wijzigen in 1 als u opeenvolgende publicaties wilt. In dit geval wordt de eerste publicatietaak uitgevoerd en wordt de volgende publicatietaak opgeslagen in de publicatiereeks.

Om de grootte van de de verwerkingspool van de outputgeneratie te veranderen, werk de **het plaatsen van de Grootte van de Pool van de 1&rbrace; generatie in de** bundel bij.`com.adobe.fmdita.publish.manager.PublishThreadManagerImpl`

## FrameMaker Publishing Server configureren (alleen voor op locatie) {#id1678G0Z0TN6}

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


