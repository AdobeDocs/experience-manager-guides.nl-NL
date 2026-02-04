---
title: Opmerkingen bij de release | Nieuwe functies in de Adobe Experience Manager Guides 2026.01.0-release
description: Meer informatie over de nieuwe en verbeterde functies in de 2026.01.0-release van Adobe Experience Manager Guides
role: Leader
source-git-commit: cb3b06e18391fdfc53eb5abd4096553781eab0b8
workflow-type: tm+mt
source-wordcount: '1551'
ht-degree: 0%

---

# Nieuwe functies in de release 2026.01.0 (februari 2026)

Dit artikel behandelt de nieuwe en verbeterde functies die zijn geïntroduceerd met de release 2026.01.0 van Adobe Experience Manager Guides as a Cloud Service.

Voor de lijst van kwesties die in deze versie worden bevestigd, mening [&#x200B; Vaste kwesties in de 2026.01.0 versie &#x200B;](fixed-issues-2026-01-0.md).

Leer over [&#x200B; verbeteringsinstructies voor de versie 2026.01.0 &#x200B;](../release-info/upgrade-instructions-2026-01-0.md).


## Maak kennis met zoeken in Source-modus in Zoeken en vervangen

Experience Manager Guides heeft verschillende verbeteringen aangebracht in de functie Zoeken en vervangen in het linkerdeelvenster van de Editor-interface. Samen met betere UI voor betere bruikbaarheid, introduceert deze versie een nieuwe **bron van het Gebruik wijze** knevel in **Vondst en vervangt** paneel.

Als u deze modus inschakelt, kunt u niet alleen een algemene zoekopdracht uitvoeren op de zichtbare inhoud, maar ook op de onderliggende broninhoud (XML-structuur, inclusief elementen, tags en kenmerkwaarden) voor de gezochte tekenreeks. Deze modus zorgt voor een uitgebreide zoekopdracht in de gehele inhoud.

![](assets/map-find-replace-with-source-mode.png){width="650" align="left"}

In deze modus kunt u filters toepassen om de zoekopdracht te beperken tot bestandstype, documentstatus, datum van laatste wijziging en meer. U kunt ook een gedetailleerd CSV-rapport downloaden nadat u de bewerking Alle vervangen hebt uitgevoerd. Hiermee wordt een momentopname gegeven van alle vervangacties die samen met hun status van succes en mislukking zijn uitgevoerd.

Voor meer details, mening [&#x200B; vind en vervang &#x200B;](../user-guide/web-editor-left-panel.md#find-and-replace) sectie in _Linkerpaneel in Redacteur_.

>[!NOTE]
>
> Voor **het bronwijze van het Gebruik** eigenschap in het paneel van de Vondst en vervangt, moet een plaatsing van de douaneindex eerst worden voltooid. Nadat de indexering op zijn plaats is, contacteer uw team van het Succes van de Klant om deze eigenschap toe te laten.

## Verbeterde bladerervaring voor bestanden en mappen

Deze release introduceert een schonere, intuïtievere interface voor het bladeren in bestanden en mappaden in Experience Manager Guides.

Wanneer het doorbladeren van dossiers, kenmerkt de vernieuwde **Uitgezochte dossier** dialoog nu een van labels voorzien lay-out met twee meningen - **Bewaarplaats** voor het navigeren van de volledige inhoudsbewaarplaats in een in tabelvorm formaat, en **Inzamelingen** voor snelle toegang tot vaak gebruikte onderwerpen, kaarten, en beelden.

![](assets/select-file.png){width="650" align="left"}

Belangrijke verbeteringen zijn:

- Tabellarische weergave van bestanden en mappen voor georganiseerde navigatie.
- Broodkruimels en het navigatievenster van de omslag om zich gemakkelijk door de omslagen te bewegen.
- Ondersteuning voor bestandsselectie voor herbruikbare inhoud, onderwerpverwijzingen, Schematron, Uitvoervoorinstellingen (met DITAVAL) en Workfront.
- Geef een voorvertoning van de geselecteerde bestanden weer zodat u ze gemakkelijk kunt bekijken. Geef voor meerdere selecties een voorvertoning van alle bestanden weer en verwijder de bestanden zo nodig uit het deelvenster Voorvertoning.
- Zoek- en filteropties om de resultaten te beperken op naam, titel, bestandstype, documentstatus en codes.

De **Uitgezochte weg** dialoog kenmerkt ook een betere boom-gestructureerde mening voor omslagnavigatie, die een meer georganiseerde en efficiënte manier verzekert om wegen over de inhoudsbewaarplaats te selecteren.

![](assets/select-path-dialog-new.png){width="350" align="left"}

Voor meer details, bekijk [&#x200B; het Bladeren dossiers en omslagen in Experience Manager Guides &#x200B;](../user-guide/web-editor-other-features.md#browse-files-and-folders-in-experience-manager-guides) sectie in _Andere eigenschappen in de Redacteur_.

## Verbeteringen voor Zoeken en filteren in opslagplaats

### Ondersteuning voor het statusfilter Document

Nu filtert u de zoekresultaten voor de opslagplaats op basis van de huidige documentstatus van de bestanden. Met het nieuwe **de staatfilter van het Document**, kunt u onderaan uw onderzoek beperken gebruikend de beschikbare die filterwaarden in het `ui_config.json` dossier binnen uw profiel van de Omslag worden bepaald.

![](assets/document-state-filter-repository.png){align="left"}

De standaardfilterwaarden die beschikbaar zijn voor de documentstatus zijn: Concept, Bewerken, In-Review, Goedgekeurd, Reviewed en Done. Voor details bij het aanpassen van de waarden van de standaarddocumentstaatsfilters, vormt de mening [&#x200B; de filters van de documentstaat &#x200B;](../cs-install-guide/config-doc-state-filters.md).

>[!NOTE]
>
> Als u aangepaste instellingen gebruikt voor `ui_config.json` , moet u een back-up van deze instellingen maken voordat u de upgrade uitvoert. Nadat u de update hebt uitgevoerd, kunt u de instellingen controleren en aanpassen en deze aanpassen aan de wijzigingen die u in de nieuwste versie hebt aangebracht.

### Miniatuurpictogram voor multimedia

Alle dossiers van verschillende media worden nu getoond met duimnagelpictogrammen, die het gemakkelijker maken om beelden binnen de **Bewaarplaats** visueel te identificeren en van de plaats te bepalen. Deze verhoging is ook van toepassing wanneer het zoeken naar dossiers in het **paneel van het Onderzoek**, die u helpen snel de activa van verschillende media van andere dossiertypes onderscheiden.

![](assets/thumbnail-repository.png){align="left"}

## Verbeteringen in de Editor

De volgende Editor-verbeteringen zijn doorgevoerd in deze versie:

### Onderwerpen of kaart vernieuwen in de modus Voorbeeld

Introducerend nieuw **&#x200B;**&#x200B;functionaliteit voor kaarten vernieuwen die reeds op de wijze van de Voorproef worden geopend. Met deze nieuwe eigenschap, kunt u de inhoud van de volledige kaart of individuele onderwerpen gemakkelijk verfrissen huidig binnen het.

- Om de volledige kaart (met inbegrip van alle onderwerpen) te verfrissen, verfrist een nieuwe **&#x200B;**&#x200B;knoop wordt geïntroduceerd op de hoogste linkerhoek van de Redacteur.

  ![](assets/refresh-map.png){width="600" align="left"}

- Om de inhoud van individuele onderwerpen te verfrissen, verfrist een nieuwe **onderwerp** optie wordt geïntroduceerd in het contextmenu.

  ![](assets/refresh-topic.png){width="600" align="left"}

Voor meer details, de redacteurseigenschappen van de Kaart van de mening [&#x200B; &#x200B;](../user-guide/map-editor-advanced-map-editor.md).

### Indicator voor werkkopie voor wijzigingen in metagegevens

Om het even welke veranderingen in de meta-gegevensgebieden beschikbaar onder **eigenschappen van het Dossier** zullen nu de werkende exemplaarindicator teweegbrengen. Een documentversie wordt duidelijk als _vuil (*)_ wanneer u toevoegt, schrapt, of om het even welke gebrek of gebieden van douanemetagegevens wijzigt. Deze verbetering zorgt ervoor dat alle meta-gegevensveranderingen correct worden gevolgd, die grotere zichtbaarheid en controle over documentversies verstrekken.

### Aantal woorden voor onderwerpen en kaarten

U kunt het woordaantal nu volgen aanwezig binnen een kaart of onderwerpdossier. Het nieuwe **gebied van de Telling van 0&rbrace; Word in het Juiste paneel zou het totale aantal woorden tonen huidig binnen een onderwerp (of kaart), waar de woorden die door ruimten worden gescheiden als individuele woorden worden geteld.** Deze wordt automatisch vernieuwd wanneer u wijzigingen opslaat. Voor kruisverwijzingen wordt alleen de weergavetekst opgenomen, terwijl toetsen worden uitgesloten.

![](assets/file-properties-new.png){width="350" align="left"}

Voor details, mening [&#x200B; Juiste paneel in Redacteur &#x200B;](../user-guide/web-editor-right-panel.md#file-properties).

### Verbeterde verwerking voor alleen-lezen bestanden

Het uitgeven van de eigenschappen van het Dossier is nu beperkt voor dossiers die op **Gelezen slechts** wijze zijn. Als een dossier door een andere gebruiker (beschikbaar op Gelezen slechts wijze) wordt gesloten, kunt u geen meta-gegevensbezit veranderen, of van het [&#x200B; Juiste paneel &#x200B;](../user-guide/web-editor-right-panel.md#file-properties), de **3&rbrace; optie van Eigenschappen &lbrace;in het** contextmenu van een dossier [, of het &#x200B;](../user-guide/web-editor-other-features.md#context-menu-functions-on-a-files-tab) Rapport van Meta-gegevens [. &#x200B;](../user-guide/reports-web-editor.md#metadata-report) Zo voorkomt u onbedoelde wijzigingen in alleen-lezen bestanden.

## Verbeteringen voor revisie

### Onderwerpen toevoegen aan of verwijderen uit een lopende revisietaak

Nu, kunt u nieuwe onderwerpen aan een aan de gang zijnde overzichtstaak toevoegen (als zij niet eerder voor overzicht) werden verzonden of onderwerpen uit een aan de gang zijnde overzichtstaak verwijderen zonder het overzichtswerkschema te beïnvloeden.

Op de **pagina van de Details van de Taak**, kunt u eenvoudig selecteren of onderwerpen losmaken om de onderwerpenlijst te wijzigen. Revisoren worden via AEM en e-mailberichten op de hoogte gesteld (via AEM en e-mail) van wijzigingen in hun toegewezen onderwerpen. Voor meer details, verzendt de mening [&#x200B; onderwerpen voor overzicht &#x200B;](../user-guide/review-send-topics-for-review.md).

![](assets/modify-review-topics.png){width="650" align="left"}

## Verbeterde vertaling

### Indicator voor niet-geversificeerde activa verzonden voor vertaling

Wanneer u vertalingen beheert, is het belangrijk ervoor te zorgen dat er een versienummer wordt ingesteld voor alle inhoud voordat deze ter verwerking wordt verzonden. Om dit te helpen, verstrekt Experience Manager Guides nu een duidelijke indicator voor onderwerpen die veranderingen hebben bewaard maar nog niet versioned.

Als een dossier unversioned veranderingen (niet opgeslagen als nieuwe versie in uw kaart) bevat, verschijnt een _info_ pictogram naast het dossier, erop wijzend dat de updates bestaan. Om zich snel op deze dossiers te concentreren, laat **activa met unversioned veranderingen slechts** optie in het paneel van Filters toe.

Voor meer details, mening [&#x200B; vertaal documenten van de Console van de Kaart &#x200B;](../user-guide/translate-documents-web-editor.md).

![](assets/unversioned-changes-translation.png){width="650" align="left"}

## Verbeteringen voor publiceren

### Aangepaste afbeeldingsuitvoeringen voor specifieke uitvoervoorinstellingen

U kunt nu verschillende afbeeldingsuitvoeringen configureren voor afzonderlijke uitvoervoorinstellingen onder hetzelfde uitvoertype door het kenmerk `outputName` in `renditionmapping.xml` te gebruiken. Deze verbetering geeft u meer flexibiliteit wanneer het publiceren van inhoud die verschillende beeldresoluties voor verschillende scenario&#39;s vereist. U wilt bijvoorbeeld een afbeelding met hoge resolutie voor de HTML5-hoofduitvoer terwijl u een kleinere miniatuur voor een lichtgewichtvoorinstelling gebruikt.

Voor meer details, bekijk [&#x200B; de afbeeldingsvertoning van de Handle in outputgeneratie &#x200B;](../cs-install-guide/conf-output-generation.md#handle-image-rendition-during-output-generation).


### Logboeken downloaden voor gegenereerde uitvoer

Wanneer het produceren van output door Assets UI, is een nieuwe **Logboeken van de Download** knoop nu beschikbaar die u toestaat om logboek aan uw lokaal apparaat voor gemakkelijkere toegang en overzicht te downloaden.


### Taalvariabelen voor kruisverwijzingen in native PDF-uitvoer

Wanneer het publiceren van Inheemse output van PDF, kunt u [&#x200B; taalvariabelen &#x200B;](../native-pdf/native-pdf-language-variables.md) gebruiken om statische verwijzingstekst als _te vertalen zie in hoofdstuk_ of _zie op pagina_. De variabele gebruikt de taal die in het onderwerp door het `xml:lang` attribuut wordt bepaald.

Voor details bij het vormen van Inheemse vooraf ingestelde output van PDF en verwijzingsmontages, mening [&#x200B; Inheemse vooraf ingestelde output van PDF &#x200B;](../web-editor/native-pdf-web-editor.md).


### Ondersteuning voor componenttoewijzing op elementniveau in New AEM Sites (met samengestelde componenttoewijzing)-publicaties

Experience Manager Guides ondersteunt nu componenttoewijzing op elementniveau in de AEM Sites-uitvoer (met samengestelde componenttoewijzing), waardoor teams exact kunnen bepalen hoe DITA-elementen worden gerenderd met `componentmapping.json` . Als u `topicref` , titels, afbeeldingen, tabellen en meer toewijst aan de juiste AEM Core-componenten, krijgt u een schonere structuur in plaats van alles wat standaard aan de Text-component wordt toegewezen. Dit resulteert in betere prestaties en ontgrendelt rijkere, modernere Sites-ervaringen.

Voor meer details, bekijk [&#x200B; afbeelding van de Component in AEM Sites &#x200B;](../cs-install-guide/component-mapping.md).

## Verbeteringen voor middelenverwerking

Deze release introduceert de volgende verbeteringen voor de verwerking van bedrijfsmiddelen:

- Middelen verwerken op zowel map- als bestandsniveau
- U kunt elementen filteren door specifieke elementtypen te kiezen, zoals onderwerpen, kaarten, markeringen, HTML/CSS, DITAVAL of andere ondersteunde bestanden, zodat alleen de bestanden worden verwerkt die u nodig hebt.
- Pas op datum gebaseerde filters toe om het verwerkingsbereik voor een bepaald tijdsbestek te beperken.
- De activa van het herproces direct gebruikend de nieuwe optie (**verwerkt activa**) beschikbaar in het contextmenu van dossiers en omslagen binnen de mening van de Bewaarplaats en het paneel van de Ontdekkingsreiziger.

Voor meer details op verwerkingsactiva, mening [&#x200B; activa van het Proces &#x200B;](../user-guide/asset-processor.md).

## API-verbeteringen

De volgende API-verbeteringen zijn doorgevoerd in deze release:

- Nieuwe API&#39;s worden geïntroduceerd om een nieuw vertaalproject te maken en de status ervan te volgen. Deze API&#39;s helpen het vertaalproces te automatiseren, verminderen handmatige inspanningen en verbeteren de efficiëntie. Voor details, mening [&#x200B; creeer vertaalproject &#x200B;](../api-reference/translation-project.md)
- Verbeterde API&#39;s voor middelenverwerking met verbeterde filtermogelijkheden voor bestanden en mappen. Voor details, mening [&#x200B; activa van het Proces &#x200B;](../api-reference/bulk-assets-processing.md).
















