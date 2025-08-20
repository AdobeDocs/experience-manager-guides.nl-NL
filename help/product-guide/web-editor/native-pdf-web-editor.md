---
title: Oorspronkelijke PDF | PDF-uitvoergeneratie
description: Leer hoe u het publiceren van een eigen PDF-bestand kunt gebruiken, een PDF-uitvoervoorinstelling kunt maken en genereren, tijdelijke bestanden kunt downloaden nadat u de eigen PDF-uitvoer hebt gegenereerd en taalvariabelen in Adobe Experience Manager Guides kunt gebruiken.
exl-id: ec3d59b7-1dda-4fd1-848e-21d8a36ff5e4
feature: Publishing, Native PDF Output
role: User
source-git-commit: e722ba35e27599566140709e060f3b391d50b4db
workflow-type: tm+mt
source-wordcount: '3232'
ht-degree: 0%

---

# Systeemeigen PDF-uitvoervoorinstelling

Bij het ontwerpen van inhoud wordt het van essentieel belang dat de inhoud is geoptimaliseerd voor weergave, bewerking en afdrukken. Met standaarden zoals W3C CSS3 voor inhoudsopmaak en CSS-normen voor gepagineerde media voor eigenschappen van paginadefinities, zoals grootte, marges, afdrukstand, pagina-einden, kop- en voetteksten en paginanummering, kunt u de weergave en lay-out voor uw PDF-document instellen, zodat u verzekerd bent van consistentie en bruikbaarheid. De publicatiefunctie Native PDF gebruikt deze standaarden om een PDF te genereren.

Met de native PDF-publicatie kunt u vooraf gedefinieerde sjablonen gebruiken om consistentie in de indeling en structuur van de inhoud te garanderen, stijlpagina&#39;s toepassen om de vormgeving van uw uitvoer te wijzigen, PDF optimaliseren, drukkermarkeringen instellen, ondersteuning voor schermlezers toestaan, PDF-conformiteit instellen, lettertypen insluiten en nog veel meer.

Het genereren van een PDF met behulp van Native PDF-publicaties heeft twee aspecten:

* Gebruik sjablonen om stijlen toe te passen op inhoud, paginalay-outs en verschillende instellingen in te stellen om de PDF te verfijnen. Auteurs kunnen de voorbeeldsjablonen gebruiken of wijzigen of aangepaste sjablonen maken en geavanceerde configuratieopties instellen die door uitgevers en ontwikkelaars worden gebruikt.

* Een PDF-uitvoervoorinstelling maken of configureren om de PDF-instellingen te beheren. Nadat u een PDF-uitvoervoorinstelling hebt gemaakt, kunt u de PDF genereren.

## Een uitvoervoorinstelling maken

Voer de volgende stappen uit om de PDF-voorinstelling te maken vanaf de kaartconsole:

1. [ open een DITA kaartdossier in de console van de Kaart ](../user-guide/open-files-map-console.md).

   U kunt tot het kaartdossier van de **Recente dossiers** widget in de [ sectie van het Overzicht ](../user-guide/intro-home-page.md#overview) ook toegang hebben. Het geselecteerde kaartbestand wordt geopend in de kaartconsole.
1. In **vooraf instelt van de Output** lusje, selecteer + pictogram om tot een output vooraf ingesteld te leiden.
1. Selecteer **PDF** van het drop-down Type in **Nieuwe output vooraf ingestelde** dialoogdoos.
1. Op het **gebied van de Naam**, verstrek een naam aan dit vooraf ingesteld.
1. Op **produceer PDF Gebruikend** gebied, uitgezochte **Native-PDF**.
1. Selecteer **toevoegen aan huidige omslagprofiel** optie om een output tot stand te brengen die binnen het huidige omslagprofiel vooraf in wordt gesteld. Het ![ pictogram van het omslagprofiel ](./assets/global-preset-icon.svg) wijst op een omslag-profiel-niveau vooraf ingesteld.

   Leer meer over [ beheer Globale en de profieloutput van de Omslag vooraf instelt ](../user-guide/web-editor-manage-output-presets.md).

1. Selecteer **toevoegen**.

   De voorinstelling voor PDF wordt gemaakt.

## Systeemeigen configuratie van PDF-voorinstellingen

Nadat de voorinstelling is gemaakt, configureert u de instellingen voor de eigen PDF-voorinstelling. De vooraf ingestelde configuratieopties voor DITA-OT worden georganiseerd onder **Algemeen**, **Meta-gegevens**, **Lay-out**, **Veiligheid**, **Druk**, en **Geavanceerde** lusjes.

<img src="assets/preset-panel-new.png" alt="deelvenster met voorinstellingen" width="800">

**Algemeen**

Hiermee kunt u basisuitvoerinstellingen opgeven, zoals een uitvoerpad, PDF-bestandsnaam en meer.

| Instelling | Beschrijving |
| --- | --- |
| **Pad van de Output** | Het pad in de AEM-opslagplaats waar de PDF-uitvoer wordt opgeslagen. Zorg ervoor dat het uitvoerpad zich niet in de projectmap bevindt. Het uitvoerpad wordt ingesteld via de variabele `${base_output_path}` , die wordt geconfigureerd door Beheerder. Om de weg van de Output te vormen, vormt de mening [ de Plaats van de Output van de Basis voor de diensten van de Wolk ](../native-pdf/configure-base-location-cs.md) of [ vormt de Plaats van de Output van de Basis voor de diensten On-Prem ](../native-pdf/configure-base-output-location.md) die op de dienst worden gebaseerd u gebruikt. <br> u kunt de volgende uit-van-doos variabelen ook gebruiken om de Weg van de Output te bepalen. U kunt een enkele of een combinatie van variabelen gebruiken om deze optie te definiëren. <br> `${map_filename}`: gebruikt de naam van de DITA-kaartbestanden om het doelpad te maken. <br> `${map_title}`: gebruikt de DITA-maptitel om het doelpad te maken. <br>`${preset_name}`: gebruikt de naam van de uitvoervoorinstelling om het doelpad te maken. <br> `${language_code}`: gebruikt de taalcode waar het kaartbestand zich bevindt om het doelpad te maken. <br> `${map_parentpath}`: gebruikt het volledige pad van het kaartbestand om het doelpad te maken.  <br>`${path_after_langfolder}`: gebruikt het pad van het kaartbestand na de taalmap om het doelpad te maken. |
| **het Dossier van PDF** | Geef een bestandsnaam op om de PDF op te slaan. Standaard wordt bij de naam van het PDF-bestand de DITA-mapnaam en de naam van de voorinstelling toegevoegd. ditamap is bijvoorbeeld &#39;TestMap&#39; en de naam van de voorinstelling is &#39;preset1&#39;. De standaardnaam van de pdf is &#39;TestMap_preset1.pdf&#39;. <br> u kunt de volgende uit-van-doos variabelen ook gebruiken om het Dossier van PDF te bepalen. U kunt een enkele of een combinatie van variabelen gebruiken om deze optie te definiëren. <br>`${map_filename}`<br>`${map_title}`<br>`${preset_name}` <br> `${language_code}`. |
| **pas Voorwaarden toe gebruikend** | Kies voor geconditioneerde inhoud een van de onderstaande opties om een PDF-uitvoer te genereren op basis van deze voorwaarden: <br><ul> <li> **Geen Toegepaste** Selecteer deze optie als u geen voorwaarde op de kaart en broninhoud wilt toepassen. <br><li> **DITAVAL dossier** Selecteer een DITAVAL dossier om voorwaardelijke inhoud te produceren. U kunt meerdere DITAVAL-bestanden selecteren via het dialoogvenster Bladeren of door het bestandspad handmatig in te voeren. Als u een geselecteerd bestand wilt verwijderen, klikt u op het kruispictogram naast de naam ervan. Als een ongeldig dossier wordt geselecteerd, wordt een foutenmelding getoond verklarend **Ongeldig DITAVAL dossier wordt geselecteerd**. <br> <br> Elk DITAVAL dossier kan een waaier van eigenschappen, zoals het filtreren voorwaarden en het vlaggen stijlen bevatten. Door tags toe te wijzen kunt u inhoud visueel markeren met begin- en eindmarkeringen, die afbeeldingen of tekstopmaak zoals vet of cursief kunnen bevatten. In geval van overlappende voorwaarden of stijlconflicten kunt u een achtergrondkleur definiëren met de conflictopties voor Stijl. Voor meer details, bekijk [ Gebruik de redacteur DITAVAL ](../user-guide/ditaval-editor.md).<br><li> **Vooraf ingestelde Voorwaarde van de Voorwaarde** Selecteer een voorwaarde vooraf ingesteld van drop-down om een voorwaarde toe te passen terwijl het publiceren van de output. Deze optie is zichtbaar als u een voorwaarde voor het DITA kaartdossier hebt toegevoegd. De voorwaardelijke instellingen zijn beschikbaar op het tabblad Voorinstellingen voorwaarde van de DITA-kaartconsole. Om meer over voorwaarde vooraf ingesteld te weten, mening [ vooraf instelt van het Gebruik ](https://help.adobe.com/en_US/xml-documentation-for-adobe-experience-manager/index.html#t=DXML-master-map%2Fgenerate-output-use-condition-presets.html). <br> </ul> |
| **Basislijn van het Gebruik** | Als u een basislijn voor de geselecteerde kaart hebt gecreeerd DITA, selecteer deze optie om de versie te specificeren die u wilt publiceren. Het Werk van de mening [ met Basislijn ](https://help.adobe.com/en_US/xml-documentation-for-adobe-experience-manager/index.html#t=DXML-master-map%2Fgenerate-output-use-baseline-for-publishing.html) voor meer details. |
| **creeer PDF met de Bar van de Verandering tussen Gepubliceerde Versies** | Gebruik de volgende opties om een PDF te maken die de verschillen in inhoud tussen twee versies weergeeft met wijzigingsbalken:   <br><ul><li> **Basislijn van de Vorige Versie** kiest de basislijnversie die u met de huidige versie of een andere basislijn wilt vergelijken. In de PDF wordt een wijzigingsbalk weergegeven om de gewijzigde inhoud aan te geven. Een wijzigingsbalk is een verticale lijn die nieuwe of herziene inhoud visueel identificeert. De wijzigingsbalk verschijnt links van de inhoud die is ingevoegd, gewijzigd of verwijderd. <br> **Nota**: Als u **Basislijn van het Gebruik** selecteert en een basislijn kiest om te publiceren, zal de vergelijking tussen de twee geselecteerde basislijnversies worden gedaan. Bijvoorbeeld, als u basislijnversie 1.3 onder **Basislijn van het Gebruik** kiest, en Versie 1.1 onder **Basislijn van de Vorige Versie**, zal de vergelijking tussen basislijnversie 1.1 en basislijnversie 1.3 worden gedaan. <br><li> **toon Toegevoegde Tekst** Uitgezocht om de opgenomen tekst in groene kleur en onderstreept te tonen. Deze optie is standaard ingeschakeld. <br> <li> **toon Geschrapte Tekst** Uitgezocht om de geschrapte tekst in rode kleur en duidelijk met een doorhaling te tonen. Deze optie is standaard ingeschakeld. <br>**Nota** U kunt het stileren van de veranderingsbar, opgenomen inhoud, of geschrapte inhoud ook aanpassen gebruikend stylesheet.<br></ul> |
| **Werkschema van de Post van de Generatie** | Selecteer deze optie om een vervolgkeuzelijst weer te geven met alle workflows die in AEM zijn geconfigureerd. U kunt de workflow selecteren die u wilt uitvoeren nadat de PDF-generatieworkflow is voltooid. |

**Metagegevens**

Metagegevens zijn de beschrijving of definitie van de inhoud. Metagegevens helpen bij inhoudsbeheer en helpen bij het zoeken naar bestanden op internet.

Gebruik het tabblad Metagegevens om de metagegevensvelden in te stellen, zoals de naam van de auteur, de documenttitel, trefwoorden, copyrightinformatie en andere gegevensvelden voor de PDF-uitvoer. U kunt ook aangepaste metagegevens toevoegen voor uw PDF-uitvoer.

Deze meta-gegevens wordt in kaart gebracht aan de meta-gegevens in het **1&rbrace; lusje van de Beschrijving &lbrace;binnen de** Eigenschappen van het Document **van uw output PDF.**



<img src="assets/pdf-metadata.png" alt="tabblad Metagegevens" width="600">

Van de Output stelt vooraf in, selecteert **PDF** > **Native-PDF** > **Meta-gegevens** om meta-gegevensopties toe te voegen en aan te passen.
* **Metagegevens van het Gebruik die in topicmeta** worden toegevoegd

  Deze optie is standaard ingeschakeld. U kunt de meta-gegevens gebruiken die u in het topicmeta element van de kaart DITA hebt toegevoegd om de meta-gegevensgebieden van de output van PDF te bevolken.

* **verstrek XMP dossier**

  U kunt de meta-gegevensgebieden ook direct bevolken door [ XMP ](https://www.adobe.com/products/xmp.html) (het Verlengbare Platform van Meta-gegevens) dossier in te voeren. U kunt hier een voorbeeld-XMP-bestand downloaden.

[Downloaden](assets/SampleXMP.xmp)

  U kunt ook een XMP-bestand genereren met Adobe Acrobat.
   1. Selecteer **Dossier** > **Eigenschappen** in Acrobat.
   1. Onder **Beschrijving**, uitgezochte **Extra Meta-gegevens**.
   1. Van het linkerpaneel, uitgezochte **Geavanceerd**.
   1. Selecteer **sparen**.

  XMP-bestand wordt opgeslagen op het apparaat.

* **verstrekt meta-gegevensnamen en waarden**

   1. Voeg naam toe door uit de drop-down te selecteren of een douanemetagegevens toe door direct op het naamgebied te typen.
   1. Voer de waarde voor de metagegevens in en selecteer het plusteken (+).
De metagegevens worden toegevoegd aan de lijst met metagegevens voor de PDF.

U kunt ook variabelen gebruiken om de waarden van metagegevens te definiëren.  U kunt de metagegevens die voor de DITA-kaart of het bladwijzerbestand zijn gedefinieerd, als variabelen gebruiken. De metagegevens vindt u onder het knooppunt `/jcr:content/metadata` van de DITA-kaart of het bladwijzerbestand.
Wanneer u een variabele gebruikt, wordt de waarde ervan gekozen uit de eigenschappen van metagegevens.

Als u een variabele wilt gebruiken, moet u deze definiëren in de `${<variable>}` -indeling.

Een van de metagegevenseigenschappen die bijvoorbeeld in het knooppunt /`jcr:content/metadata` zijn gedefinieerd, is
`dc:title` . U kunt `${dc:title}` specificeren, en de titelwaarde wordt gebruikt in de definitieve output.

U kunt een enkele of een combinatie van variabelen gebruiken om de metagegevens te definiëren. Bijvoorbeeld `${dc:title} ${dc:docstate}` . U kunt ook de combinatie van een variabele en een tekenreeks gebruiken.  Bijvoorbeeld `View ${dc:title} in ${dc:language}` .

Taalvariabelen gebruiken om de gelokaliseerde waarde van eigenschappen van metagegevens te definiëren. Afhankelijk van uw gekozen taal wordt de gelokaliseerde waarde automatisch gekozen in de PDF-uitvoer. U kunt bijvoorbeeld &quot;Auteur&quot; afdrukken als de metagegevenswaarde in het Engels en &quot;Autorin&quot; in het Duits.

Indeling: `${lng:<variable name>}`. `${lng:author-label}` waarbij `author-label` bijvoorbeeld een taalvariabele is.

Overslaan <img src="./assets/info-details.svg" alt= "info icon" width="25"> in de buurt van de optie voor meer informatie over de optie.


**Lay-out**

Hiermee kunt u paginalay-outs instellen en paginaweergaveopties opgeven voor PDF-uitvoer, zoals Paginaweergave en Zoomniveaus instellen.

| Instelling | Beschrijving |
| --- | --- |
| **Malplaatje van PDF** | PDF-sjablonen bieden een duidelijke structuur voor het definiëren van paginalay-outs, het opmaken van inhoud en het toepassen van verschillende instellingen op uw PDF-uitvoer. Selecteer in de vervolgkeuzelijst PDF-sjabloon de gewenste sjabloon. <br> u kunt **ook selecteren doorbladert Malplaatje** <img src="./assets/browse-templates-icon.svg"  alt= "bladersjablonen, pictogram" width="25"> om een sjabloon te kiezen. In de **Uitgezochte het malplaatje van PDF** dialoog kunt u de duimnagel en de titel en de beschrijving voor het geselecteerde malplaatje ook voorproef bekijken. |
| **Vertoning van de Pagina** | Gebruik de paginaweergave voor de paginaweergave waarin wordt getoond hoe de PDF wordt weergegeven wanneer deze wordt geopend. Selecteer een optie in het keuzemenu Paginaweergave om een voorkeursweergave te kiezen. <br><ul><li> **Gebrek** Vertoningen zoals op het gebrek dat van de kijker van PDF op de machine van een gebruiker plaatst.  <br> <li> **Enige Mening van de Pagina** toont één pagina tegelijkertijd.   <br> <li> **Enige Pagina die** scrolt toont één enkele pagina in een ononderbroken verticale kolom.  <br> <li> **Twee Mening van de Pagina** toont twee-pagina uitgespreid zij aan zij tegelijkertijd. .<br> <li> **Twee het Schuiven van de Pagina** toont twee-pagina uitgespreid zij aan zij met ononderbroken het scrollen. </ul> |
| **Gezoem** | Selecteer deze optie om het formaat te wijzigen van de paginaweergave waarin wordt getoond hoe de PDF wordt weergegeven wanneer deze wordt geopend.  <br><ul><li> **Gebrek** Vertoningen zoals per het gebrek dat van de kijker van PDF op de machine van een gebruiker plaatst    <br> <li> **100%** maakt de pagina in zijn daadwerkelijke grootte verschijnen.     <br> <li> **Passend Pagina** maakt de paginabreedte en de hoogte om binnen de documentruit te passen.   .<br> <li> **Passend de Breedte van de Pagina** maakt de breedte van de pagina de breedte van de documentruit vullen.  <br> <li> **de Hoogte van de Pagina van de Passende** maakt de hoogte van de pagina de hoogte van de documentruit vullen. </ul> |

**Veiligheid**

Bescherm uw PDF door beperkingen toe te voegen aan het openen en lezen van het bestand. Gebruik de onderstaande opties om ongeoorloofde toegang te voorkomen.

| Instelling | Beschrijving |
| --- | --- |
| **plaats wachtwoord om het document** te openen | Selecteer deze optie om een beveiligd wachtwoord toe te voegen om uw PDF-bestand weer te geven. Specificeer een wachtwoord op het **gebied van het wachtwoord van de Gebruiker 0&rbrace;.** Gebruikers kunnen de PDF alleen openen door het wachtwoord in te voeren dat in dit veld is opgegeven. |
| **plaats de documentbeperkingen** | Selecteer deze optie om de interactie tussen gebruikers en uw PDF te beperken. Specificeer een wachtwoord op het **gebied van het Wachtwoord van de Eigenaar 0&rbrace; &lbrace;voor de hieronder beperkingsmontages te werken.**<br><ul><li> **het Druk** Uitgezocht om een gebruiker toe te staan om PDF te drukken. <br> <li> **de kwaliteit van het Ontwerp druk** Uitgezocht om een gebruiker toe te staan om PDF in een lagere resolutie te drukken.  <br> <li> **Inhoud het kopiëren** Uitgezocht om een gebruiker toe te staan om inhoud van PDF te kopiëren.   <br> <li> **Annotaties** Uitgezocht om een gebruiker toe te staan om een nota of een commentaar in PDF toe te voegen. <br> <li> **de wijzigingen van de Inhoud** Uitgezocht om een gebruiker toe te staan om de inhoud in PDF te veranderen. <br> <li> **Inhoud het kopiëren voor toegankelijkheid** Uitgezocht om het schermlezers toe te staan om inhoud in PDF te lezen en te navigeren. <br>  **de assemblage van het Document** Uitgezocht om gebruikers toe te staan om pagina&#39;s in PDF op te nemen. <br> **Nota**: De gebruikers moeten het eigenaarwachtwoord ingaan om het even welke beperkingen van het Dossier te veranderen > Eigenschappen in Adobe Acrobat. |

**Druk**

>[!NOTE]
>
> Beginnend met Experience Manager Guides 5.0/2025.02.0 versie, is de sectie van de Druk nu deel van de **Eigen vooraf ingestelde Output van PDF**. Voor de bestaande sjablonen met opgeslagen afdrukinstellingen blijven de afdrukgegevens intact, maar worden deze niet meer weergegeven in de gebruikersinterface of worden deze tijdens de uitvoer toegepast. Als u deze instellingen wilt blijven gebruiken, moet u ze opnieuw configureren in de eigen PDF-uitvoervoorinstelling.

Configureer de afdrukproductie-instellingen om drukkermarkeringen toe te wijzen, kleurmodellen te selecteren en eigenschappen voor het afdrukken van de PDF-uitvoer op te geven.

* **de Tekens van de Printer**: Wanneer u een document voor drukproductie voorbereidt, worden de drukkermarkeringen toegevoegd aan de paginagrenzen om in juiste groepering, het in orde maken, en kleurenselectie tijdens druk bij te staan. Door een drukkermarkering te selecteren, wordt de paginagrens uitgebreid om de markering aan te passen, die tijdens het afdrukken wordt bijgesneden. U kunt de volgende drukkermarkeringen weergeven in de PDF-uitvoer:
   * **de Tekens van de Versiering**: Selecteer de optie om een teken bij elke hoek van het versieringsgebied te plaatsen om erop te wijzen waar het document na druk moet worden bijgesneden.
   * **Aflooptekens**: Selecteer om een markering bij elke hoek van het afloopvak te plaatsen om op het bijsnijdgebied voor de uitgebreide afbeelding te wijzen.
   * **de Tekens van de Registratie**: Uitgezocht om een teken buiten het gewassengebied voor het richten van de verschillende scheidingen in een kleurendocument te plaatsen.
   * **de Bars van de Kleur**: Uitgezocht om een strook kleuren buiten het trimgebied toe te voegen om kleurenconsistentie te handhaven en inktdichtheid aan te passen wanneer het drukken.

  De vastgestelde afmetingen voor de geselecteerde drukkermarkeringen gebruiken de **Breedte van de Lijn**, **Kleur van de Lijn**, en **Bleed de Breedte van de Doos** opties.

* **Grootte van de Doos van Media**: Dit is de algemene paginagrootte met inbegrip van het uitgebreide gebied bezet door drukkermarkeringen. Gebruik de vervolgkeuzelijst om het paginaformaat te selecteren voor uw PDF-uitvoer of om uw eigen aangepaste formaat te maken.

* **Ruimte van de Kleur**: U krijgt een optie om van RGB of CMYK kleurenruimten te kiezen om uw document van PDF te drukken. Kies RGB om de gegenereerde PDF digitaal en CMYK weer te geven voor fysiek afdrukken. Kleuren die in het document zijn gedefinieerd, worden omgezet in de gekozen kleurruimte.

* **ICC profiel**: Hier, kunt u kleurennauwkeurigheid over apparaten beheren door een ICC profiel te specificeren. Dit zorgt voor consistente kleurweergave in de afgedrukte uitvoer.

Als u deze instelling wilt configureren, geeft u het pad naar het ICC-profielbestand op de server op en geeft u de naam van het ICC-profiel op voor eenvoudige identificatie. Als het ICC-profiel echter online is opgeslagen, kunt u de URL opgeven in plaats van het bestandspad.

>[!NOTE]
>
> Als u CMYK-kleurruimte gebruikt, is een ICC-kleurprofiel vereist voor het maken van PDF/A.

<!--For more information on applying these print settings, see *Printing preferences*.-->

**Geavanceerd**

Gebruik de volgende opties om geavanceerde instellingen op te geven voor het samenvoegen van PDF&#39;s, compressie gebruiken, compatibiliteitsnorm selecteren en meer.

| Instelling | Beschrijving |
| --- | --- |
| **creeer toegankelijke (geëtiketteerde) PDF** | Selecteer deze optie als u een PDF met tags wilt genereren. Met een gelabelde PDF kunnen schermlezers gemakkelijker inhoud, hyperlinks, bladwijzers enzovoort lezen en navigeren. Als een tabel bijvoorbeeld is gecodeerd, weet de schermlezer dat deze de tabel leest en niet alleen regels en tekst. |
| **Fusie PDFs inbegrepen in TOC** | Selecteer deze optie als u bestaande PDF&#39;s wilt samenvoegen in de uitvoer door deze als resourcebestand toe te voegen aan uw DITA-kaart. De PDF&#39;s worden ingevoegd op de locatie die op de kaart wordt weergegeven en de pagina&#39;s worden dienovereenkomstig verhoogd. |
| **bed gebruikte doopvonten** in | Selecteer deze optie als u lettertypen gebruikt die mogelijk niet op de computer van de eindgebruiker zijn geïnstalleerd. Als deze optie is ingeschakeld, worden de gebruikte lettertypen ingesloten in de PDF. Zo weet u zeker dat de gebruiker de PDF naar behoren kan weergeven, zelfs als de lettertypen niet op hun computer zijn geïnstalleerd. <br> **Nota**: Een doopvont kan worden ingebed slechts als het het plaatsen door de doopvontverkoper bevat die het om toelaat worden ingebed. Zorg ervoor dat u de vereiste instelling of licentie hebt voordat u een lettertype insluit. |
| **gebruik automatische woordafbreking** | Als automatische woordafbreking is ingeschakeld, worden woorden aan het einde van regels op grammaticaal correcte plaatsen afgebroken met een afbreekstreepje. |
| **laat JavaScript** toe | Schakel deze optie in als u een JavaScript-code hebt waarmee u de inhoud dynamisch wilt transformeren voordat u een PDF genereert. |
| **bed de dossiers van multimedia** in | Selecteer deze optie als u alle audio, video en interactieve inhoud naar de PDF wilt opnemen. |
| **volledige compressie van het Gebruik om de grootte van PDF te optimaliseren** | Selecteer deze optie als u een grote PDF wilt comprimeren of verkleinen. Houd er rekening mee dat het comprimeren van de PDF de bestandskwaliteit kan verminderen. |
| **de beeldcompressie van het Gebruik om de grootte van PDF te optimaliseren** | Selecteer deze optie als u de gebruikte afbeeldingen in uw PDF wilt comprimeren of verkleinen. Houd er rekening mee dat het comprimeren van een afbeelding de afbeeldingskwaliteit kan verminderen. |
| **de douaneresolutie van het Gebruik (pixel per duim)** | Dit is de resolutie van de paginaweergave bij pixels per inch. Voer in het veld een voorkeurswaarde in die wordt weergegeven wanneer deze optie wordt geselecteerd. De standaardwaarde is 96 pixels per inch. Stel een hogere waarde in om meer inhoud in een inch te passen en andersom als u een lagere waarde instelt. |
| **toon Watermerk** | Selecteer deze optie als u een watermerk in de uitvoer wilt plaatsen. U kunt een nieuwe tekstreeks in het tekstvak invoeren met de tekenbehuizing zoals u wilt. <br><br> de statische tekst of taalvariabelen van het Gebruik om de gelokaliseerde versie van het watermerk te publiceren.  Afhankelijk van uw gekozen taal wordt de gelokaliseerde waarde automatisch gekozen in de PDF-uitvoer. U kunt &#39;Publisher&#39; bijvoorbeeld afdrukken als een watermerk in het Engels en &#39;Auteure&#39; in het Frans.  <br> Indeling: `${lng:<variable name>}` . `$ {lng:publisher-label}` waarbij `publisher-label` bijvoorbeeld een taalvariabele is. <br> Houd de cursor boven <img src="./assets/info-details.svg" alt= "info icon" width="25"> in de buurt van de optie voor meer informatie over de optie. |
| **laat de vergelijkingen van MathML** toe | Selecteer deze optie om MathML-vergelijkingen in uw inhoud te renderen. De vergelijkingen worden anders standaard genegeerd. |
| **creeer interactieve vorm van PDF** | Selecteer deze optie als u interactieve en aanpasbare PDF-formuliervelden wilt opnemen voor verbeterde gebruikersinvoer in gegenereerde PDF-uitvoerbestanden. |
| **omvat spoorveranderingen** | Selecteer deze optie als u bijgehouden wijzigingen in de gegenereerde PDF wilt opnemen, zodat u deze gemakkelijk kunt bekijken en vergelijken. |
| **behoud tijdelijke dossiers** | Selecteer deze optie als u de tussentijdse HTML-bestanden die zijn gemaakt tijdens het genereren van de eigen PDF-uitvoer wilt behouden. U kunt de tijdelijke bestanden later downloaden nadat u de uitvoer hebt gegenereerd. De gedownloade bestanden bevatten ook `system_config.xml` -bestand dat u informatie geeft over de URL van de auteur, de lokale URL en de publicatie-URL. Deze URL&#39;s worden geconfigureerd in de AEM-instellingen voor extern maken en worden weergegeven in het `system_config.xml` -bestand. |
| **conformiteit van PDF** | Dit is de standaard waarmee u uw PDF wilt opslaan om ervoor te zorgen dat deze voldoet. Selecteer in het vervolgkeuzemenu een optie in de lijst met beschikbare PDF-standaarden. Voor meer details over de gesteunde normen, mening [ Ongeveer PDF normen ](https://helpx.adobe.com/acrobat/using/pdf-conversion-settings.html#about_pdf_x_pdf_e_and_pdf_a_standards). |
| **eigenschappen van het Dossier** | Selecteer de metagegevens die u wilt doorgeven aan eigen PDF-publicaties. In het vervolgkeuzemenu worden zowel de aangepaste als de standaardeigenschappen weergegeven. `dc:description`, `dc:language`, `dc:title` en `docstate` zijn bijvoorbeeld de standaardeigenschappen, terwijl u `author` als de aangepaste eigenschap kunt hebben. De geselecteerde eigenschappen van metagegevens worden doorgegeven aan het PDF-bestand dat is gegenereerd met Native PDF. <br> Deze eigenschappen worden gekozen uit het `metadataList` dossier beschikbaar bij:`/libs/fmdita/config/metadataList`. <br> Dit dossier kan bij worden bedekt: `/apps/fmdita/config/metadataList`. |



<!--------------


### Additional notes for PDF output

**Download temporary files after generating the Native PDF output**

If you select the **Download temporary files** option in the Advanced settings, you can also download the interim HTML files created while generating the Native PDF output. Once you've generated the output, you can download the temporary files using the **Download temporary files** ![download temporary files](assets/native-pdf-download-temporary-files-icon.svg)icon on the top bar. This feature helps you view your interim HTML styles and layouts and helps you correct or change your CSS styles according to your requirements.


>[!NOTE]
>
> The **Download temporary files**  ![download temporary files](assets/native-pdf-download-temporary-files-icon.svg) icon appears only if you have generated the last PDF output using the preset wherein you have selected the option in the **Advanced** tab. 


**Use language variables**

AEM Guides also provides the support for language variables. Select **Language Variables** <img src="assets/language-variables.svg" width="25">  in the left panel to define a localized version of the out-of-the-box labels like Note, Caution, and Warning or static text in the PDF output. For more details, view [Support for language variables](../native-pdf/native-pdf-language-variables.md).


**Support for Markdown documents**

Experience Manager Guides also provides support for your Markdown documents.  Markdown files are easy to author and also provide a variety of formatting options. Learn how to [author Markdown documents from the Editor](../user-guide/web-editor-markdown-topic.md). 

You can add the Markdown topics to your DITA map and generate the PDF output using the Native PDF output presets.  Learn how to configure or [create a PDF output preset](#create-a-pdf-output-preset-create-output-preset). 

--------------->