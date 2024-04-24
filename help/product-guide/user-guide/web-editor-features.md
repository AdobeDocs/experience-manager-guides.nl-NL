---
title: De functies van de webeditor kennen
description: Ontdek functies van de webeditor in AEM hulplijnen. Zorg dat u de interface van de webeditor kent, zoals de hoofdwerkbalk, de secundaire werkbalk, het linkerdeelvenster, het bewerkingsgebied van inhoud en het rechterdeelvenster.
exl-id: 340cf72e-e44d-4df2-8312-50d00ac651b7
feature: Authoring, Features of Web Editor
role: User
source-git-commit: 4c7421391922d276ef82515fb4b1cbdc2397e4ce
workflow-type: tm+mt
source-wordcount: '18678'
ht-degree: 0%

---

# De functies van de webeditor kennen {#id176NC500V5Z}

Deze sectie begeleidt u door de diverse eigenschappen die in de Redacteur van het Web beschikbaar zijn. Wij kunnen de Redacteur van het Web in de volgende secties of gebieden verdelen:

- [Hoofdwerkbalk](#id2051EA0G05Z)
- [Secundaire werkbalk](#id2051EA0J0Y4)
- [Deelvenster Links](#id2051EA0M0HS)
- [Inhoudsbewerkingsgebied](#id2051EB000UI)
- [Rechterdeelvenster](#id2051EB003YK)

De volgende subsectie behandelt in detail de diverse secties van de Redacteur van het Web.

## Hoofdwerkbalk {#id2051EA0G05Z}

De belangrijkste toolbar is bij de bovenkant van de interface van de Redacteur van het Web en het verstrekt dossier-vlakke eigenschappen en diverse auteurswijzen beschikbaar in de Redacteur van het Web. De functies in de bovenste werkbalk worden als volgt uitgelegd:

**Alles opslaan** - ![](images/SaveFloppy_icon.svg)

Hiermee slaat u de wijzigingen op die u in alle geopende onderwerpen hebt aangebracht. Als u veelvoudige onderwerpen hebt die in de Redacteur van het Web worden geopend, klikt het klikken **Alles opslaan** of door **Crtl**+**S** Met sneltoetsen worden alle documenten met één klik opgeslagen. U hoeft niet elk document afzonderlijk op te slaan.

>[!NOTE]
>
> Met Opslaan wordt geen nieuwe versie van uw onderwerpen gemaakt. Kies Opslaan als nieuwe versie als u een nieuwe versie wilt maken.

**Opslaan als nieuwe versie** - ![](images/save-revision-icon.png)

Slaat de veranderingen op u in uw onderwerp hebt aangebracht en leidt ook tot een nieuwe versie van uw onderwerp. Als u aan een nieuw gecreeerd onderwerp werkt, wordt de versieinformatie getoond zoals **none**.

![](images/save-all-first-version-none_cs.png){width="800" align="left"}

Het versieaantal verandert met elke nieuwe versie die voor het onderwerp of kaartdossier wordt gecreeerd.

Wanneer u een onderwerp of kaart opslaat met **Opslaan als nieuwe versie** wordt het volgende dialoogvenster weergegeven:

![](images/save-as-new-version-dialog.PNG){width="300" align="left"}

Voer opmerkingen en versielabels in om de wijzigingen te identificeren en klik op **Opslaan** om een nieuwe versie van uw bestand te maken.

Wanneer u *Opslaan als nieuwe versie*, wordt de eerste versie van het onderwerp gecreeerd in DAM, die ook de momenteel actieve versie van uw onderwerp wordt. Later, als u aan een oudere versie van het onderwerp terugkeert, dan wordt dat uw huidige actieve versie van het onderwerp.

Als uw beheerder pre-gevormde versielabels heeft, dan zult u die etiketten in een drop-down lijst zien. U kunt een label kiezen in de lijst met beschikbare labels en het document opslaan.

![](images/web-editor-pre-defined-labels.PNG){width="300" align="left"}

Wanneer u een onderwerp opslaat, kunt u een opmerking toevoegen die de wijzigingen opgeeft die u in het onderwerp hebt aangebracht. Deze opmerking wordt getoond in de Geschiedenis van de Versie van het onderwerp.

Als uw onderwerp wordt gecontroleerd, zullen uw recensenten een bericht krijgen die zeggen dat een nieuwere versie van het onderwerp beschikbaar is. Ze hebben eenvoudig toegang tot de nieuwste revisie van uw document en kunnen de nieuwste versie van uw onderwerp blijven bekijken.

Wanneer u de aanwijzer boven de titel van een onderwerp plaatst, worden het bestandspad en het versienummer weergegeven.

![](images/mouse-hover-on-title_cs.png){width="800" align="left"}

>[!NOTE]
>
> Zodra een versie van uw onderwerp beschikbaar is, kunt u etiketten aan uw onderwerp ook toevoegen. Deze labels kunnen vervolgens worden gebruikt om een basislijn te maken voor het publiceren van een specifieke versie van uw document. Voor meer informatie over het gebruiken van etiketten in uw onderwerpen, zie [Labels gebruiken](web-editor-use-label.md#).

**Ongedaan maken en Opnieuw** - ![](images/Undo_icon.svg) / ![](images/Redo_icon.svg)

De laatste handeling ongedaan maken of opnieuw uitvoeren.

**Element verwijderen** - ![](images/Delete_icon.svg)

Verwijdert het momenteel geselecteerde element of het element waar de cursor is geplaatst.

**Zoeken en vervangen** - ![](images/FindAndReplace_icon.svg)

De functie Zoeken en vervangen is beschikbaar in de modus Auteur en de modus Bronweergave. De de tekstbar van de Vondst en van de Vervanging verschijnt bij de bodem van het onderwerp het uitgeven gebied. U kunt de sneltoetsen gebruiken **CTRL**+**F** om de balk Zoeken en vervangen aan te roepen.

![](images/find-replace-bar.png){width="800" align="left"}

Het instellingenpictogram gebruiken \(![](images/settings-find-replace-icon.svg)\), kunt u schakelen tussen **Hoofdlettergebruik negeren** en **Alleen hele woorden** zoekopties. Als u de niet-hoofdlettergevoelige zoekopdracht wilt uitvoeren, schakelt u \(of selecteert\) de optie **Hoofdlettergebruik negeren** -optie. Als u anders de hoofdlettergevoelige zoekopdracht wilt uitvoeren, schakelt u \(of deselecteert\) de optie **Hoofdlettergebruik negeren** -optie. U kunt ook een heel woord zoeken.

De zoekopdracht is onmiddellijk, wat betekent dat u de zoekuitdrukking of het woord in het dialoogvenster **Zoeken** wordt de term onmiddellijk doorzocht en geselecteerd in het onderwerp. Op dezelfde manier voor het vervangen van een tekst in uw onderwerp, ga de onderzoekstermijn en zijn vervanging op de respectieve gebieden in en klik **Vervangen** of **Alles vervangen** knop.

In de Bronmening, is de Vondst en vervangt uiterst nuttig voor het zoeken naar een specifiek element of een attribuut. Als u bijvoorbeeld de waarde van de optie `@product` kan dit gemakkelijk worden gedaan vanuit de bronweergave. In de weergave Auteur kunt u niet zoeken op basis van een kenmerk of element. U moet echter voorzichtig zijn met het gebruik van de **Alles vervangen** gebruiken, aangezien het de code van XML zou kunnen beschrijven.

**Editor-instellingen** - ![](images/editor_settings_icon.svg)

De Editor-instellingen zijn alleen beschikbaar voor gebruikers met administratieve bevoegdheden. Met behulp van de voorkeuren kan een beheerder de volgende instellingen configureren:

>[!NOTE]
>
> Als u standaardinstellingen bijwerkt, moet u documenten opnieuw openen om de wijzigingen van kracht te laten worden.

- **Algemeen**: Met de algemene instellingen kunt u het woordenboek configureren dat u wilt gebruiken met de webeditor. Dit tabblad bevat drie secties: **Spellingcontrole**, **Voorwaarde**, en **Authoring**.

  ![](images/editor-setting-general.png){width="650" align="left"}

   - **Spellingcontrole**: Er zijn twee opties — **Spellingcontrole AEM** en **Spellingcontrole browser**. Standaard gebruikt de editor de functie Spellingcontrole in browser, waarbij de spellingcontrole wordt uitgevoerd met behulp van het ingebouwde woordenboek van de browser. U kunt overschakelen op AEM spellingcontrole om AEM woordenboek te gebruiken, dat ook kan worden aangepast om uw lijst met aangepaste woorden toe te voegen. Ga voor meer informatie over het aanpassen van AEM woordenboek naar *Standaardwoordenboek AEM aanpassen* in de sectie Adobe Experience Manager-hulplijnen installeren en configureren as a Cloud Service.


   - **Voorwaarde**

      - **Voorwaardelijke tekst markeren in de weergave Auteur**: Selecteer deze optie om de voorwaardelijke tekst te markeren in de ontwerpweergave. De voorwaardelijke inhoud wordt gemarkeerd met de kleur die voor de voorwaarde is gedefinieerd.

      - **Valideren met Condition-kenmerken**: Selecteer deze optie als u de gedefinieerde waarden voor de kenmerken wilt valideren. Hierdoor kunt u geen onjuiste waarde toevoegen.

      - **Toon de Sleutel met de Titel in het paneel van het Onderwerp**: Selecteer deze optie om de sleutels samen met titels in het onderwerpschema weer te geven. Als u deze optie niet selecteert, worden alleen de titels weergegeven. Hier worden bijvoorbeeld de toetsen &#39;os&#39;, &#39;publiek&#39; en &#39;ander&#39; ook samen met titels weergegeven.

        ![](images/subject-scheme-title.png){width="550" align="left"}

      - **Onderwerpregeling tonen in het deelvenster Voorwaarden**: Selecteer deze optie om een onderwerpschema weer te geven in het deelvenster Voorwaarden. Als u deze optie uitschakelt, worden de gedefinieerde voorwaarden weergegeven in het deelvenster Voorwaarden.

   - **Authoring**

      - **Alles vervangen inschakelen**: Selecteer deze optie om het pictogram Alles vervangen in het deelvenster Zoeken en vervangen weer te geven.


   - **Kaarten**
Wijzig de stijl van de citaten. Kies de citaatstijl van drop-down u in uw project wilt gebruiken. Zie voor meer informatie [Aanhalingsstijlen wijzigen](./web-editor-apply-citations.md#change-citation-style).


**Deelvensters**: Deze instelling bepaalt de deelvensters die worden weergegeven in het linkerdeelvenster van de editor. U kunt schakelen tussen het tonen of verbergen van het gewenste deelvenster.

![](images/editor-setting-panel.png){width="650" align="left"}

>[!NOTE]
>
> Als er een aangepast deelvenster is geconfigureerd, wordt dit ook weergegeven in de lijst met deelvensters. U kunt schakelen tussen het weergeven of verbergen van het aangepaste deelvenster. Voor meer details over de configuratie, zie *Een aangepast deelvenster configureren in het linkerdeelvenster* in de sectie Adobe Experience Manager-hulplijnen installeren en configureren as a Cloud Service.

- **Elements List**: Als beheerder kunt u de lijst met elementen beheren die een auteur kan invoegen met de opdracht [Element invoegen](#id204SG30105Z) en definieert ook de weergavenaam voor het element. Met de instelling Elements List kunt u de naam van het element opgeven volgens de DITA-specificaties en een label dat u wilt gebruiken in plaats van de door DITA gedefinieerde elementnaam:

  ![](images/editor-setting-element-list.png){width="650" align="left"}

In de bovenstaande schermafbeelding `b` element heeft een etiket van Vet gekregen; `codeblock` krijgt samen met enkele andere elementen een label van Codeblok. Als u **Alleen boven elementen gebruiken** en worden alleen de geldige elementen \(op het huidige invoegpunt\) uit deze lijst weergegeven in het pop-upmenu Element invoegen.

In het volgende schermafbeelding worden slechts 3 van de 4 geconfigureerde elementen van de vorige schermafbeelding weergegeven bij de huidige context:

![](images/editor-setting-insert-element-list.PNG){width="300" align="left"}

- **Lijst met kenmerken**: Net als in de lijst met elementen kunt u de lijst met kenmerken en hun weergavenamen instellen die in de lijst met kenmerken van een element moet worden weergegeven. In het volgende schermschot, slechts zijn 3 attributen gevormd om in de de attributenlijst van een element te worden getoond:

  ![](images/editor-setting-attributes-list.png){width="650" align="left"}

  Met dit het plaatsen, wanneer u probeert om een attribuut aan een element toe te voegen, ziet u slechts de lijst van attributen die in de lijst worden gevormd.

  ![](images/editor-setting-add-attributes-list.png-to-element.PNG){width="300" align="left"}

- **Profiel publiceren**: Dit bevat de publicatieprofielen die kunnen worden gebruikt om de **Kennisbank** uitvoer. U kunt een nieuw profiel voor een doelkennisbasis tot stand brengen. Bijvoorbeeld Salesforce of ServiceNow.

   - **Een Salesforce-publicatieprofiel maken**

     **Vereisten**

      - Maak een verbonden app voor Salesforce. Raadpleeg voor meer informatie [OAuth-instellingen inschakelen voor API-integratie](https://help.salesforce.com/s/articleView?id=sf.connected_app_create_api_integration.htm&amp;type=5).

      - Zorg tijdens het configureren van de verbonden app voor het volgende:

         - Geef de callback op.

           `URL: http://<server name>:<port>/bin/dxml/thirdparty/callback/salesforce`

         - Selecteer de volgende OAuth-bereiken:
            - Volledige toegang (volledig)
            - Selecteer Gebruikersgegevens beheren via API&#39;s (api)

  Als de app eenmaal is geconfigureerd, biedt Salesforce een **Consumentencode** en **Consumentengeheim**.

  Deze kunnen worden gebruikt om het Salesforce-publicatieprofiel te maken.


   - Als u een Salesforce-publicatieprofiel wilt maken, selecteert u de optie **Salesforce** Kennisbasis van de **Servertype** vervolgkeuzelijst. Voer een profielnaam in. In de **Site-URL** voert u de consumentensite in die u wilt gebruiken om de uitvoer te publiceren en voegt u vervolgens de **Consumentencode** en **Consumentengeheim** verstrekt door de consumentenwebsite van Salesforce. Dan, **Valideren** en **Opslaan** het nieuwe profiel.
     ![salesforce publicatieprofiel in editorinstellingen](./images/salesforce-publish-profile.png){width="550" align="left"}

     >[!NOTE]
     >
     >Om een volmacht voor Salesforce in de Gidsen van de Experience Manager te vormen, gebruik Apache de Configuratie van de Volmacht van HTTP Componenten in AEM. Leer hoe u [vorm volmacht voor de Controle van de Verbinding AEM](https://helpx.adobe.com/experience-manager/kb/How-to-configure-proxy-for-the-AEM-Link-Checker-AEM.html).


   - **Een ServiceNow-publicatieprofiel maken**

     **Vereisten**

     Vorm de server ServiceNow om de activa te uploaden.
      - Verbinding maken met de **ServiceNow** server.
      - Navigeren naar **Systeemeigenschappen** > **Beveiliging**.
      - Schakel de volgende optie uit:

        **Deze eigenschap moet worden ingesteld om MIME-typecontrole te activeren voor uploads (alle versies Eureka en up). Schakelt mime-validatie (true) of uit (false) voor de bestandsbijlagen. Bestandsextensies die zijn geconfigureerd via glide.gehechtheid.extensions worden tijdens het uploaden gecontroleerd op het MIME-type.**

      - Klikken **Opslaan**.

     Als u de app hebt geconfigureerd, maakt u de **ServiceNow** Profiel publiceren.
   - Om een Publish Profiel tot stand te brengen, selecteer de Kennisbank ServiceNow van **Servertype** vervolgkeuzelijst. Een profiel invoeren **Naam**. In de **ServiceNow URL** voert u de consumentensite in die u voor het publiceren van de uitvoer wilt gebruiken en voegt u vervolgens de **Gebruikersnaam** en **Wachtwoord** verstrekt door de de consument ServiceNow plaats. Dan, **Valideren** en **Opslaan** het nieuwe profiel.

     ![ServiceNow-publicatieprofiel](./images/service-now-publish-profile.png){width="550" align="left"}

  Nadat u hebt gevalideerd, kunt u het publicatieprofiel selecteren in de uitvoervoorinstellingen van een DITA-kaart en deze gebruiken om de uitvoer naar de  **Salesforce** of **ServiceNow** server die u hebt gekozen.

  Meer informatie over de [Kennisbank](../user-guide/generate-output-knowledge-base.md) uitvoervoorinstelling.


- **Validatie**: Dit lusje bevat opties om de Bevestigingen van het Schema in de redacteur van het Web te vormen. U kunt de volgende functies inschakelen:

   - **Validatiecontrole uitvoeren voordat het bestand wordt opgeslagen**: Selecteer deze optie om Schematron-validaties uit te voeren met behulp van de geselecteerde Schematron-bestanden voordat u een opslagbewerking uitvoert. U kunt een Schematron-bestand toevoegen door op het pictogram + te klikken. De geselecteerde Schematron-bestanden worden weergegeven.

     >[!NOTE]
     >Het geselecteerde schemabestand of de geselecteerde schemabestanden blijven aanwezig voor het geselecteerde mapprofiel.

     ![Validatie in editorinstellingen](./images/editor-setting-validation.png){width="550" align="left"}
Hiermee voorkomt u dat gebruikers een bestand opslaan dat een regel verbreekt die is gedefinieerd in de geselecteerde Schema-bestanden. Als u deze optie niet selecteert, wordt het bestand niet gevalideerd voordat de wijzigingen worden opgeslagen.

   - **Laat alle gebruikers schemabestanden toevoegen in het validatievenster**: Selecteer deze optie als u wilt dat gebruikers een willekeurig schemabestand kunnen toevoegen in het deelvenster Validatie van de webeditor. Dit staat de gebruikers toe om dossiers Schematron toe te voegen en dan de onderwerpen tegen het dossier van Schematron te bevestigen. Als deze optie niet is geselecteerd, **Schematron-bestand toevoegen** is niet beschikbaar voor de gebruikers in het dialoogvenster **Deelvenster Validatie** van de webeditor.


- **Weergavekenmerken**: Net als in de lijst Kenmerken kunt u de lijst met kenmerken instellen die in de lijst met kenmerken van een element moet worden weergegeven. Standaard vier **Weergavekenmerken** — het publiek, het platform, het product, en de steunen zijn gevormd om in de attributenlijst van een element worden getoond. U kunt ook een weergavekenmerk toevoegen met de opdracht **Toevoegen** bovenaan. U kunt ook alle weergavekenmerken verwijderen met de opdracht **Verwijderen** pictogram.

  De kenmerken die voor een element zijn gedefinieerd, worden weergegeven in de layoutweergave en in de contourweergave.

  ![](images/editor-settings-display-attributes.png){width="550" align="left"}

- **Vertaling**: Dit lusje bevat de opties om taalgroepen tot stand te brengen, de bronetiketten aan de doelversie te verspreiden, en het vertaalproject schoon te maken.
  ![](images/editor-setting-translation.png){width="550" align="left"}

   - **Taalgroepen**: Als beheerder kunt u een groep talen maken en deze gebruiken als een set om de inhoud te vertalen.\
     Voer de volgende stappen uit om een nieuwe taalgroep te maken:
      1. Selecteer Toevoegen ![pictogram toevoegen](images/Add_icon.svg) pictogram.
      1. Voer de naam van de taalgroep in. Elke taal moet een unieke naam hebben. U kunt een fout weergeven als het naamveld leeg is of als de naam niet uniek is.
      1. Selecteer de talen in het vervolgkeuzemenu. U kunt meerdere talen selecteren.

     Typ de eerste paar tekens van de taal of de taalcode om de gewenste talen te filteren. Typ bijvoorbeeld &#39;en&#39; om alle talen te filteren die &#39;en&#39; bevatten aan het begin van hun naam of code.
      1. Selecteren **Gereed** om de geselecteerde talen toe te voegen aan de groep. De talen worden weergegeven. Wanneer u drie of meer talen toevoegt, **Meer weergeven** worden weergegeven. U kunt **Meer weergeven** om alle talen in de groep weer te geven.
         >[!TIP]
         >
         > Schakelen **Meer weergeven** tot **Minder tonen** en bekijk slechts een paar talen.

      1. Houd de muis boven de talen in een groep die u wilt bewerken ![bewerkingspictogram](images/edit_pencil_icon.svg) of verwijderen ![delete](images/Delete_icon.svg) de taalgroepen.
      1. Sla de **Editor-instellingen**.

         >[!NOTE]
         >
         >Als gebruiker, kunt u de taalgroepen bekijken die aan uw omslagprofiel worden gevormd.

   - **Bronversielabels doorgeven aan de doelversie**: Selecteer deze optie om het label van de versie van het bronbestand aan het vertaalde bestand door te geven. Deze optie is standaard uitgeschakeld.
   - **Overdrachtsproject opschonen na voltooiing**: Selecteer deze optie om de vertaalprojecten te vormen die na de vertaling moeten worden onbruikbaar gemaakt of automatisch worden geschrapt. Standaard, **Geen** is geselecteerd, dus het project bestaat na vertaling.

     U kunt de vertaalprojecten onbruikbaar maken als u hen later wilt gebruiken. Als u een project verwijdert, worden alle bestanden en mappen in het project permanent verwijderd.


- **Metagegevens**: U kunt de versiemetagegevens van het onderwerp en hun waarden controleren die in worden getoond **Versiehistorie** in.  Geef in het pad naar de metagegevens de locatie op van de knooppunten waaruit u de metagegevens wilt kiezen. U kunt ook een aangepaste naam voor de metagegevens definiëren als label. De standaardeigenschappen zijn Titel, Documentstatus en Labels.

  De metagegevens kunnen worden gekozen uit elke eigenschap onder de `/jcr:content` knooppunt van het element, zodat u het pad van de eigenschap kunt toevoegen als het pad naar metagegevens.


  Er wordt een fout weergegeven als het pad naar de metagegevens leeg is. Als u het label leeg laat, wordt het laatste element als label gekozen.




  ![tabblad Metagegevens in de editorinstellingen](images/editor-setting-metadata.png){width="550" align="left"}

  *De metagegevens voor de **Versiehistorie**in.*




  U kunt ook de volgorde definiëren waarin deze metagegevenstags worden weergegeven. Als u de standaardvolgorde van deze tags wilt wijzigen, selecteert u de stippelbalken om de tags naar de gewenste locatie te slepen.
De metagegevenslabels worden in dezelfde volgorde in de **Versiehistorie** van de webeditor.



**Gebruikersvoorkeuren** - ![pictogram met gebruikersvoorkeuren](images/user_preference_editor_icon.svg)

De gebruikersvoorkeuren zijn beschikbaar voor alle auteurs. Met de voorkeuren kan een auteur de volgende instellingen configureren:



- **Algemeen**: Op het tabblad Algemeen kunt u de volgende instellingen configureren:

  ![Tabblad Algemeen voor gebruikersvoorkeuren](images/user_preference_editor.PNG){width="550" align="left"}

   - **Mapprofielen**: Het profiel Map bestuurt diverse configuraties met betrekking tot voorwaardelijke kenmerken, ontwerpsjablonen, uitvoervoorinstellingen en de configuraties van de webeditor. Het algemene profiel wordt standaard weergegeven. Als uw beheerder mapprofielen heeft geconfigureerd in het systeem, worden deze mapprofielen ook weergegeven in de lijst Mapprofielen.

     De configuraties van de Redacteur van het Web die een beheerder in het omslagprofiel kan bepalen omvatten: het aanpassen van gebruikersinterface met inbegrip van de toolbarpictogrammen, de lay-out van de Redacteur van het Web, fragmenten, en wortelkaart. Zie voor meer informatie *Profielen op algemeen niveau of mapniveau configureren* in de as a Cloud Service Adobe Experience Manager-hulplijnen installeren en configureren.

     >[!NOTE]
     >
     > De naam van het huidige mapprofiel wordt weergegeven als een label voor het pictogram Gebruikersvoorkeuren op de hoofdwerkbalk.

   - **Basispad**: Door gebrek, wanneer u tot de AEM bewaarplaats van de Redacteur van het Web toegang hebt, wordt u getoond activa van de /content/dam plaats. De werkmap bevat hoogstwaarschijnlijk enkele mappen in de map /content/dam/. Het zou u een paar klikken nemen om de werkende omslag telkens te bereiken. U kunt het Basispad instellen op uw werkmap en vervolgens in de weergave Opslagplaats de inhoud van die locatie vooraf weergeven. Hierdoor neemt de tijd voor toegang tot uw werkmap af. Ook, wanneer u om het even welk verwijzing of media dossier in uw onderwerp opneemt, doorbladert het dossier plaats begint met de omslag die in de Weg van de Basis wordt geplaatst.

   - **Hoofdmap selecteren**: Selecteer een DITA-toewijzingsbestand om sleutelverwijzingen of woordenboekitems op te lossen. De geselecteerde hoofdmap heeft de hoogste prioriteit om toetsverwijzingen op te lossen. Zie voor meer informatie [Belangrijke verwijzingen oplossen](map-editor-other-features.md#id176GD01H05Z).

     >[!NOTE]
     >    
     > Als u geen wortelkaart wilt gebruiken, dan zorg ervoor dat **Hoofdmap selecteren** veld is leeg.

- **Weergave**: Selecteer de thema&#39;s voor de webeditor en de bronweergave van het inhoudsbewerkingsgebied.

  ![tabblad Weergave van gebruikersvoorkeuren](images/user_preference_editor_appearance.png){width="550" align="left"}

   - **Bestanden weergeven op**: Selecteer de standaardmanier om de bestanden weer te geven in de webeditor. U kunt de bestandenlijst weergeven op titel of bestandsnaam in de verschillende deelvensters van het dialoogvenster **Auteur** weergeven.
     >[!NOTE]
     >
     > Standaard worden de bestanden op titel weergegeven in de webeditor.

   - **Toepassingsthema**: U kunt kiezen uit de **Licht** of **Donker** thema&#39;s voor de toepassing. Voor de **Licht** in de werkbalken en deelvensters wordt een lichtgrijze achtergrond gebruikt. Voor de **Donker** in de werkbalken en deelvensters wordt een zwarte achtergrond gebruikt. Selecteren **Apparaatthema gebruiken** om Experience Manager Guides toe te staan de lichte en donkere thema&#39;s te selecteren op basis van het thema van uw apparaat.  In alle thema&#39;s wordt het bewerkingsgebied van de inhoud weergegeven in de witte kleur van de achtergrond in het dialoogvenster **Auteur** weergeven.

   - **Bronweergavethema**: - U kunt kiezen uit de **Licht** of **Donker** thema&#39;s voor het inhoudsbewerkingsgebied in de bronweergave. Voor de **Licht** in het inhoudsbewerkingsgebied wordt een lichtgrijze achtergrond voor de bronweergave gebruikt, terwijl in het geval van **Donker** wordt een achtergrond met een zwarte kleur gebruikt. Selecteren **Apparaatthema gebruiken** om Experience Manager Guides toe te staan de lichte en donkere thema&#39;s te selecteren op basis van het thema van uw apparaat.

   - **Bestanden altijd zoeken in de opslagplaats**: Selecteer deze optie om de locatie van een bestand in de opslagplaats weer te geven terwijl u het bewerkt in de webeditor.

   - **Vaste-spatie-indicator weergeven in de modus Schrijver**: Selecteer deze optie om een indicator voor de vaste spaties te tonen terwijl het uitgeven van het in de Redacteur van het Web. Deze is standaard ingeschakeld.

**De modus Auteur, Bron en Voorvertoning**

Zie voor meer informatie over de verschillende ontwerpmodi en de weergavemodi voor documenten [Weergaven van de webeditor](web-editor-views.md#).

## Secundaire werkbalk {#id2051EA0J0Y4}

De secundaire werkbalk wordt weergegeven wanneer u een onderwerp opent voor bewerking in de webeditor. De functies in de secundaire werkbalk worden als volgt uitgelegd:

**Element invoegen** - ![](images/Add_icon.svg)

Hiermee voegt u een geldig element in op de huidige of volgende geldige locatie. U kunt ook de sneltoets gebruiken ***Alt***+***Enter*** om het pop-upvenster Element invoegen te openen. U bewerkt bijvoorbeeld een alinea en vervolgens in het dialoogvenster **Element invoegen** een lijst met elementen die in de alinea kunnen worden ingevoegd. Selecteer het element dat u wilt invoegen. U kunt het toetsenbord gebruiken om door de lijst met elementen te bladeren en op ***Enter*** om het vereiste element in te voegen.

U kunt twee typen geldige elementen weergeven:

- **Geldige elementen op de huidige locatie**: De lijst bevat de elementen die u op de huidige cursorlocatie zelf kunt invoegen.

- **Geldige elementen buiten de huidige locatie**: De lijst bevat de elementen die u kunt invoegen na een van de bovenliggende elementen voor het huidige element in de elementhiërarchie.



Als u bijvoorbeeld binnen de inline `<b>` element, kunt u elementen invoegen, zoals `<u>`, `<xref>`, `<i>` op de huidige locatie. U kunt daarentegen elementen invoegen, zoals `<table>` en `<topic>` buiten de huidige locatie.

U kunt ook een teken of tekenreeks typen in het zoekvak en zoeken naar de elementen die ermee beginnen.


![element invoegen](images/insert-element.png){width="300" align="left"}

*Voer &#39;t&#39; in om te zoeken naar alle geldige elementen die met &#39;t&#39; beginnen.*

Als u in een blokelement werkt, zoals een `note`gebruikt u vervolgens het pictogram Element invoegen om een nieuw element in te voegen na het pictogram `note` element. In het volgende scherm is een notitie-element ingevoegd in het p \(alinea\)-element:

![Element invoegen in een blokelement](images/note-in-para-insert-element_cs.png){width="800" align="left"}

Als u op Enter drukt in het notitie-element, wordt een nieuwe alinea gemaakt in het notitie-element zelf. Als u een nieuw element buiten de notitie wilt invoegen, klikt u op het p-element \(gemarkeerd in schermafbeelding\) in de elementenbroodkruimel en klikt u op het pictogram Element invoegen of drukt u op ***Alt***+***Enter*** om het pop-upvenster Element invoegen te openen. Selecteer vervolgens het gewenste element en druk op Enter om het geselecteerde element in te voegen na het notitie-element.

U kunt ook een element tussen twee elementen toevoegen wanneer er een knipperende blokcursor verschijnt.

![](images/Block-cursor.png){width="300" align="left"}

Als u bijvoorbeeld aan een DITA-onderwerp werkt en de blokcursor tussen de korte beschrijving en het hoofdgedeelte knippert, kunt u `prolog` en voeg dan auteursrecht, auteur, en andere details toe.

Een andere manier om nieuw element in te voeren is door het contextmenu te gebruiken. Klik met de rechtermuisknop op een willekeurige plaats in het document om het contextmenu aan te roepen. In dit menu kiest u **Element invoegen** om de **Element invoegen** en kiest u het element dat u wilt invoegen.

![](images/insert-element-before-after.png){width="300" align="left"}

**Alinea invoegen** - ![](images/Paragraph_icon.svg)

Voeg alinea-element in op de huidige of volgende geldige locatie.

**Genummerde lijst invoegen/verwijderen** - ![](images/TextNumbered_icon.svg)

Hiermee maakt u een genummerde lijst op de huidige of volgende geldige locatie. Als u in een genummerde lijst op dit pictogram klikt, wordt het item omgezet in een normale alinea.

**Lijst met opsommingstekens invoegen/verwijderen** - ![](images/BulletList_icon.svg)

Hiermee maakt u een lijst met opsommingstekens op de huidige of volgende geldige locatie. Als u op een lijst met opsommingstekens klikt en op dit pictogram klikt, wordt het item omgezet in een normale alinea.

>[!NOTE]
>
>U kunt ook de optie **Gesplitste lijst** in het contextmenu van een lijstitem om de huidige lijst te splitsen en een nieuwe lijst op hetzelfde niveau te beginnen.

**Tabel invoegen** - ![](images/Table_icon.svg)

Hiermee voegt u een tabel in op de huidige of volgende geldige locatie. Klik op het pictogram Tabel invoegen om het dialoogvenster Tabel invoegen te openen:

![](images/table-properties.png){width="550" align="left"}

U kunt opgeven hoeveel rijen en kolommen in de tabel moeten worden opgenomen. Als u de eerste rij als tabelkop wilt behouden, selecteert u de optie Eerste rij als koptekst instellen. Als u een titel aan uw tabel wilt toevoegen, voert u deze in het veld Titel in.

Nadat een tabel is ingevoegd, kunt u de tabel wijzigen met het contextmenu.

![](images/table-context-menu_cs.png){width="550" align="left"}

Met behulp van het contextmenu van de tabel kunt u:

- Cellen, rijen of kolommen invoegen

- Cellen samenvoegen in de richtingen naar rechts en omlaag

- Cellen horizontaal of verticaal splitsen

- Cellen, rijen of kolommen verwijderen

- Een fragment maken van de tabel

- Id&#39;s genereren


U kunt ook kenmerken definiëren voor meerdere cellen, hele rijen of kolommen in een tabel. Als u bijvoorbeeld een tabelcel wilt uitlijnen, sleept u en selecteert u de gewenste cel. In het deelvenster Eigenschappen voor inhoud (aan de rechterkant) geeft u de eigenschap **Type** wijzigingen in **Meerdere items**.

1. In de **Attributen** sectie, klikken **+Toevoegen**.
1. Selecteer de `@valign` kenmerk van de **Kenmerk** vervolgkeuzelijst.
1. Selecteer in de vervolgkeuzelijst Waarde de gewenste tekstuitlijning die u wilt toepassen op de geselecteerde tabelcellen.
1. Klikken **Toevoegen.**

![](images/align-table-cell_cs.png){width="800" align="left"}

**Afbeelding invoegen** - ![](images/Image_icon.svg)

Hiermee voegt u een afbeelding in op de huidige of volgende geldige locatie. Klik op het pictogram Afbeelding invoegen om het dialoogvenster Afbeelding invoegen te openen, zoek en selecteer de afbeelding die u wilt invoegen.

>[!NOTE]
>
> U kunt ook een afbeelding toevoegen door deze van uw lokale systeem naar uw artikel te slepen. In dit geval wordt het afbeeldingsbestand toegevoegd met de opdracht **Elementen uploaden** workflow.  Zie voor meer informatie de **Elementen uploaden** in de [Linkerdeelvenster](web-editor-features.md#id2051EA0M0HS) sectie.


![](images/insert-image.png){width="650" align="left"}

In het dialoogvenster Afbeelding invoegen kunt u afbeeldingen/figuurtitel en Alternatieve tekst voor de afbeelding toevoegen.

U kunt naar het vereiste afbeeldingsbestand zoeken door de bestandsnaam in te voeren in de balk Type naar zoekopdracht bovenaan en de zoekresultaten te filteren op Pad \(om in te zoeken\), Verzamelingen, Bestandstype en Labels. Nadat u het vereiste afbeeldingsbestand hebt gevonden, selecteert u het bestand en klikt u op Selecteren om de afbeelding in het document in te voegen. U kunt verschillende indelingen voor afbeeldingsbestanden invoegen, zoals `.png`, `.svg`, `.gif`, `.jpg`, `.eps`, `.ai`, `.psd`en meer.

Nadat u een afbeelding hebt ingevoegd, kunt u de hoogte, breedte, plaatsing en kenmerken wijzigen in het deelvenster Eigenschappen van inhoud. Klik op een afbeeldingsbestand en breng wijzigingen aan in het deelvenster Eigenschappen van inhoud in de rechtertrack.

![](images/image-properties.png){width="800" align="left"}

In het veld Bron wordt de UUID van het ingevoegde afbeeldingsbestand weergegeven. U kunt het volledige pad van het ingevoegde afbeeldingsbestand vinden door de muisaanwijzer boven het veld Bron te plaatsen. Het pad wordt weergegeven in de knopinfo.

U kunt het formaat van een afbeelding wijzigen door de waarde Hoogte of Breedte voor het afbeeldingsbestand op te geven. De hoogte-breedteverhouding van de afbeelding wordt automatisch behouden. Desgewenst kunt u ook de hoogte-breedteverhouding van het afbeeldingsbestand niet behouden door op het vergrendelingspictogram \(van Hoogte-breedteverhouding behouden\) te klikken en de waarden voor Hoogte en Breedte in te voeren.

U kunt de instelling Placement voor de afbeelding ook opgeven als Inline of Onderbreking. Als u ervoor kiest om de plaatsingsoptie Onderbreking te gebruiken, kunt u kiezen waar u de afbeelding wilt uitlijnen (Links, Midden of Rechts).

U kunt ook andere eigenschappen voor een afbeeldingsbestand toevoegen door de vereiste eigenschappen te selecteren in het dialoogvenster **Attributen** veld.

>[!NOTE]
>
>U kunt ook klikbare gebieden \(afbeelding met hyperlinks\) in uw afbeelding definiëren. Zie voor meer informatie de **Afbeeldingskaart invoegen/bewerken** functiebeschrijving in het dialoogvenster [Linkerdeelvenster](web-editor-features.md#id2051EA0M0HS) sectie.

**Contextmenu voor afbeeldings- of mediabestanden**

U kunt ook bepaalde veelvoorkomende bewerkingen voor afbeeldingen en mediabestanden uitvoeren met het contextmenu. Klik met de rechtermuisknop op een willekeurige plaats in de afbeelding om het contextmenu aan te roepen.

Het contextmenu bevat opties voor het knippen, kopiëren of plakken van de afbeelding of media. U kunt een element invoegen voor of na het geselecteerde element. U kunt een element ook een andere naam geven of de naam ervan opheffen. U kunt de geselecteerde afbeelding of media zoeken in de opslagplaats of de voorvertoning van het bestand bekijken in de interface Middelen.

Met de andere opties in het contextmenu kunt u het pad kopiëren, een afbeelding met hyperlinks bewerken, een fragment maken of id&#39;s voor het geselecteerde element genereren.

**Multimedia invoegen** - ![](images/insert-multimedia-icon.svg)

Hiermee voegt u verschillende typen multimediabestanden in. Klik op het pictogram Multimedia invoegen en kies het type bestand dat u wilt invoegen. De ondersteunde multimedia-indelingen zijn:

- Audiobestand
- Videobestand
- YouTube
- Vimeo

Als u de optie Audio- of Video-bestand selecteert, wordt de dataweergave weergegeven waarin u door het gewenste bestand kunt bladeren en dit kunt selecteren. Als u YouTube of Vimeo kiest, wordt het dialoogvenster Multimedia invoegen weergegeven. Plak de koppeling van het videobestand in het veld Webkoppeling en klik op Invoegen om de video toe te voegen op de huidige of volgende geldige locatie in het document.

>[!NOTE]
>
> Wanneer u een YouTube-videokoppeling toevoegt, moet u de tekenreeks vervangen `watch?v=` with `embed` in de URL. Bijvoorbeeld om een YouTube-videokoppeling toe te voegen: `https://www.youtube.com/**watch?v**=WlIKQOrmZcs`, moet u deze toevoegen als: `https://www.youtube.com/**embed/**WlIKQOrmZcs`. Deze wijziging zorgt ervoor dat de video wordt ingesloten in de AEM Site en PDF-uitvoer.

U kunt het audio- of videobestand ook toevoegen via het dialoogvenster Multimedia invoegen. Selecteer de optie Audio-/videobestand en klik op het bladerpictogram om de weergave in de repository te starten. Selecteer het audio- of videobestand in de gegevensopslagruimte en klik op Selecteren om de koppeling van het bestand toe te voegen in het veld Audio- of videobestand. Als u een videobestand kiest, wordt ook een voorvertoning van het bestand weergegeven in het voorvertoningsgebied. U kunt het videobestand afspelen om de voorvertoning weer te geven.

![](images/insert-multimedia.png){width="650" align="left"}

**Kruisverwijzing invoegen** - ![](images/Reference_icon.svg)

Referenties van het type invoegen: Content Reference, Content Key Reference, Key Reference, File Reference, Web Link of Email Link.

Klik op de knop **Bestand selecteren** pictogram \(voor Content Reference en File Reference\) of **Kaart selecteren** pictogram \(voor Content Key Reference en Key Reference\) en selecteer het gewenste bestand of de gewenste inhoud die u wilt koppelen.

![](images/insert-references.png){width="650" align="left"}

Er wordt een koppeling van de geselecteerde verwijzing toegevoegd aan het document. In het contextmenu op de koppeling hebt u de volgende opties:

- **Element invoegen**: Geeft een lijst met geldige elementen weer die u in de opgegeven context kunt invoegen.
- **UUID kopiëren**: Kopieert de UUID van de ingevoegde verwijzing.
- **Pad kopiëren**: kopieert het volledige pad van de ingevoegde verwijzing.
- **Fragment maken**: Hiermee maakt u een herbruikbaar fragment van de ingevoegde verwijzing.
- **Id&#39;s genereren**: Hiermee genereert u unieke id voor de ingevoegde verwijzing.

U kunt ook zoeken met de UUID van het bestand waarnaar u wilt verwijzen. Voer bij de koppelingen Inhoud en Sleutelverwijzing de UUID in van het bestand waarnaar u een koppeling wilt maken. Het bestand wordt dan automatisch doorzocht en weergegeven in de sectie Voorbeeld. Wanneer u de UUID van het bestand opgeeft, hoeft u niet expliciet de bestandsextensie voor .xml-bestanden te vermelden. De extensie .xml wordt automatisch toegevoegd aan de UUID.

![](images/insert-content-using-uuid-search.png){width="650" align="left"}

Als de beheerder de optie UUID&#39;s heeft ingeschakeld in *XMLEditorConfig*, dan ziet u de UUID van de inhoud waarnaar wordt verwezen in de **Koppeling** eigenschap.

![](images/ref-link-uuid_cs.png){width="800" align="left"}

>[!NOTE]
>
> Als de **UUID&#39;s inschakelen** is niet ingeschakeld, wordt het relatieve pad van de inhoud waarnaar wordt verwezen, weergegeven.

>[!IMPORTANT]
>
> Hoewel het relatieve pad van de inhoud waarnaar wordt verwezen wordt weergegeven in het dialoogvenster **Koppeling** eigenschap, wordt intern de koppeling gemaakt met de UUID van de inhoud waarnaar wordt verwezen.

>[!TIP]
>
> Zie de sectie Referenties in de handleiding met aanbevolen procedures voor tips en trucs voor het verwijzen naar inhoud.

**Filter Zoeken**

U kunt zoeken naar tekst in de bestanden die aanwezig zijn op het geselecteerde pad van de AEM. &#39;Algemeen&#39; wordt bijvoorbeeld gezocht in de onderstaande screenshot. U kunt de zoekopdracht ook verkleinen met behulp van verbeterde filters. U kunt alle DITA- Dossiers zoals Onderwerpen DITA en Kaarten DITA aanwezig op de geselecteerde weg zoeken.

U kunt zoeken naar niet-DITA-bestanden zoals afbeeldingsbestanden, multimedia en documenten in het geselecteerde pad. U kunt ook zoeken naar specifieke waarden in de kenmerken van DITA-elementen. U kunt ook zoeken naar bestanden die door de opgegeven gebruiker zijn uitgecheckt.

![](images/reference-search-filters.png){width="650" align="left"}

>[!NOTE]
>
> Uw systeembeheerder kan de tekstfilters ook vormen en andere filters tonen of verbergen. Zie de sectie Tekstfilters configureren in de as a Cloud Service Adobe Experience Manager-hulplijnen installeren en configureren voor meer informatie.

De lijst met gefilterde bestanden die de gezochte tekst bevatten, wordt weergegeven. In het bovenstaande scherm worden bijvoorbeeld de bestanden met de tekst &#39;algemeen&#39; weergegeven. U kunt ook een voorvertoning van de inhoud van het bestand weergeven.

**Herbruikbare inhoud invoegen** - ![](images/content-reuse-icon.svg)

Inhoud in andere documenten in uw project opnieuw gebruiken. U kunt inhoud invoegen door rechtstreeks een koppeling te maken naar de inhoud in een bestand of door een toetsverwijzing te gebruiken, raadpleegt u [Belangrijke verwijzingen oplossen](map-editor-other-features.md#id176GD01H05Z). Wanneer u op het pictogram Herbruikbare inhoud invoegen klikt, wordt het dialoogvenster Inhoud opnieuw gebruiken weergegeven:

![](images/reuse-content-dialog.png){width="650" align="left"}

Selecteer in het dialoogvenster Inhoud opnieuw gebruiken het DITA-bestand voor bestandsverwijzingen of het DITA-kaartbestand dat de toetsverwijzingen bevat. Als deze optie is geselecteerd, worden het onderwerp of de belangrijkste verwijzingen weergegeven in het dialoogvenster. U kunt identiteitskaart/de sleutel van het onderwerp selecteren dat u en Gedaan wilt opnemen klikken om de inhoud binnen uw onderwerp op te nemen.

Als u Content Reference wilt invoegen, kunt u ook de UUID van het bestand invoeren. De herbruikbare inhoud van dat bestand wordt vermeld in de sectie Voorbeeld.

Gebaseerd op het plaatsen voor het opnemen van verbindingen, kon u of UUID van de opgenomen inhoud of de relatieve weg in het paneel van Eigenschappen of de Broncodemening zien. De koppeling wordt altijd gemaakt met de UUID van de inhoud waarnaar wordt verwezen. Zie Op UUID gebaseerde koppelingen configureren in de as a Cloud Service Adobe Experience Manager-hulplijnen installeren en configureren.

>[!NOTE]
>
> Als u inhoud voor of na de bedoelde inhoud wilt toevoegen, gebruikt u *Alt*+*Links* Pijl of Alt+*Rechts* Pijltoetsen om de cursor naar de gewenste locatie te verplaatsen.

U kunt de doorverwezen inhoud binnen het onderwerp ook insluiten door met de rechtermuisknop op de doorverwezen inhoud te klikken en **Verwijzing door inhoud vervangen** in het contextmenu.

**Speciale tekens invoegen** -  ![](images/insert-special-chars-icon.svg)

Hiermee voegt u speciale tekens in het onderwerp in. Klik op het pictogram Speciaal teken invoegen om het dialoogvenster Speciaal teken invoegen te openen.

>[!NOTE]
>
> AEM Hulplijnen bieden verplaatsbare en aanpasbare dialoogvensters. Dialoogvensters met twee kruislijnen in de rechterbenedenhoek kunnen worden vergroot of verkleind. De kruislijnen in het dialoogvenster Speciaal teken worden hieronder weergegeven.

![](images/insert-special-char.png){width="550" align="left"}

In het dialoogvenster Speciaal teken invoegen kunt u zoeken naar een speciaal teken met de naam ervan. Alle speciale tekens worden in verschillende categorieën opgeslagen. Gebruik de Uitgezochte drop-down lijst van de Categorie en selecteer een categorie. De speciale tekens die beschikbaar zijn in de geselecteerde categorie worden weergegeven. U kunt met de pijltoetsen door de lijst met speciale tekens navigeren of op het gewenste teken klikken dat u wilt invoegen. De naam en de hexadecimale code van het geselecteerde speciale teken worden onder de lijst weergegeven. Klik op Invoegen om het geselecteerde teken in het document in te voegen.

**Trefwoord invoegen** - ![](images/Keyword_icon.svg)

Trefwoord invoegen dat is gedefinieerd in uw DITA-kaart. Klik op het pictogram Trefwoord invoegen om het dialoogvenster Toetsverwijzing te openen.

![](images/insert-keyword.png){width="550" align="left"}

De trefwoorden worden in alfabetische volgorde weergegeven en u kunt ook naar trefwoorden zoeken door een zoektekenreeks te typen in het vak Zoeken. Het zoekresultaat retourneert de trefwoorden met de tekenreeks in ID of Value. De trefwoorden die in de DITA-kaart zijn gedefinieerd, worden in dit dialoogvenster weergegeven. Kies het trefwoord dat u wilt invoegen en klik op **Invoegen**.

U kunt de kenmerken van het ingevoegde trefwoord ook wijzigen door met de rechtermuisknop op het trefwoord te klikken en de optie Kenmerken te selecteren. Het dialoogvenster Kenmerken voor trefwoord wordt geopend:

![](images/attributes-for-keyword.png){width="550" align="left"}

U kunt de kenmerken van het trefwoord wijzigen of een nieuw kenmerk aan het trefwoord toevoegen.

**Fragment invoegen** - ![](images/insert-snippet-icon.svg)

Voeg een fragment in op de huidige of volgende geldige locatie. Deze functie werkt alleen als in uw systeem fragmenten zijn gedefinieerd. Voor meer informatie over het toevoegen van een fragment raadpleegt u de **Fragment** functiebeschrijving in het dialoogvenster [Linkerdeelvenster](web-editor-features.md#id2051EA0M0HS) sectie.

Wanneer u op het pictogram Fragment invoegen klikt, wordt de catalogus Fragment invoegen weergegeven. De catalogus is contextgevoelig, wat aangeeft dat de fragmenten alleen worden weergegeven als ze op de huidige locatie zijn toegestaan.

In het volgende voorbeeld worden twee vooraf geconfigureerde fragmenten getoond - Waarschuwing en Fout die op de huidige locatie in het document kunnen worden ingevoegd.

![](images/insert-snippet.png){width="300" align="left"}

Wanneer u een fragment in de lijst kiest, wordt het ingevoegd op de huidige of volgende geldige locatie in het document. In de volgende schermafbeelding ziet u het fragment Error dat in het document is ingevoegd:

![](images/error-snippet.png){width="400" align="left"}

**Afbeeldingskaart invoegen/bewerken** - ![](images/imagemap-rectangle.svg)

Hiermee voegt u een afbeelding met hyperlinks in de geselecteerde afbeelding. Een afbeelding met klikbare gebieden die aan onderwerpen of webpagina&#39;s zijn gekoppeld, wordt een afbeelding met hyperlinks genoemd.

Selecteer een afbeelding in het huidige onderwerp en klik op het pictogram Afbeeldingskaart invoegen/bewerken om het dialoogvenster Afbeeldingskaart invoegen te openen.

![](images/insert-image-map.png){width="650" align="left"}

De voorkeursvormrechthoek kiezen ![](images/imagemap-rectangle-toolbar.png), cirkel ![](images/imagemap-circle-toolbar.png), of veelhoek ![](images/imagemap-polygon-toolbr.png) Hiermee definieert u een gebied boven een afbeelding dat u als koppeling wilt gebruiken. Nadat u een gebied hebt gedefinieerd, wordt het dialoogvenster Referentie weergegeven waarin u de koppeling naar interne of externe inhoud moet opgeven:

![](images/reference-dialog.png){width="650" align="left"}

Als gebieden elkaar overlappen, kunt u de vorm naar voren halen of terugsturen door op het desbetreffende pictogram op de werkbalk te klikken. U kunt een gebied ook verwijderen door het te selecteren en het pictogram van de Schrapping te klikken. Als u dubbelklikt op een gebied, wordt het dialoogvenster Referentie geopend waarin u de doelkoppeling kunt wijzigen. Als u de vereiste gebieden in de afbeelding hebt gemarkeerd, slaat u de wijzigingen op door op Gereed te klikken.

**Uitchecken/Inchecken** - ![](images/LockClosed_icon.svg)/ ![](images/LockOpen_icon.svg)

Hiermee wordt het huidige bestand uitgecheckt of gecontroleerd. Als u een bestand uitcheckt, heeft de gebruiker exclusief schrijftoegang tot het bestand. Als het bestand is ingecheckt, worden de wijzigingen opgeslagen in de huidige versie van het bestand.

Als u in de Kaartweergave werkt en de bovenliggende kaart uitvouwt, kunt u met één klik alle bestanden op de kaart uitchecken. Vouw gewoon het bovenliggende kaartbestand uit en selecteer het bovenliggende bestand. Dit betekent dat u alle bestanden in de kaart selecteert. Vervolgens kunt u **Uitchecken**  ![](images/LockClosed_icon.svg) om alle bestanden op de kaart te vergrendelen.

>[!NOTE]
>
> Wanneer u een bestand incheckt dat niet-opgeslagen wijzigingen bevat, wordt u gevraagd de wijzigingen op te slaan. Als u uw wijzigingen niet opslaat, wordt alleen het bestand gecontroleerd.

De knopinfo voor In- en uitchecken wordt bepaald door de eigenschap title in het dialoogvenster `ui_config.json` bestand.

Voor meer informatie, bekijkt u [De titel configureren voor de pictogrammen Inchecken en Uitchecken](../install-guide/conf-checkin-checkout-title.md) in de on-premise Gids van de Installatie en van de configuratie.


**Tagweergave in-/uitschakelen** - ![](images/Label_icon.svg)

Tags zijn visuele aanwijzingen die de grenzen van een element aangeven. Een elementgrens geeft het begin en einde van een element aan. Vervolgens kunt u deze grenzen gebruiken als visuele aanwijzing om de invoegpositie te plaatsen of de tekst binnen een grens te selecteren. Als u een ander element voor of na een element in het document wilt invoegen, kunt u de invoegpositie voor of na de openings- of sluitingsgrens van het element plaatsen.

In de volgende schermafbeelding ziet u een document met de weergave Codes ingeschakeld:

![](images/tags-view.png){width="650" align="left"}

De volgende bewerkingen kunnen worden uitgevoerd in een document met de codeweergave op:

- **Een element selecteren**: Klik op de openingstag of de afsluitende tag van een element om de inhoud ervan te selecteren.

- **Tags uitvouwen of samenvouwen**: Klik op + of - teken in een tag om deze uit of samen te vouwen.

- **Het contextmenu gebruiken**: Het contextmenu bevat opties voor het knippen, kopiëren of plakken van het geselecteerde element. U kunt ook een element voor of na het geselecteerde element invoegen. Met de andere opties kunt u een id genereren of het deelvenster Eigenschappen openen voor het geselecteerde element.

- **Elementen slepen en neerzetten**: Selecteer de tag van een element en sleep deze eenvoudig naar het document. Als de neerzetlocatie een geldige locatie is waar het element is toegestaan, wordt het element op de neergezette locatie geplaatst.


>[!NOTE]
>
> Als een gebruiker de Mening van Markeringen van de Redacteur van het Web toelaat, blijft het toegelaten zelfs over de zittingen. Dit betekent dat u niet de Mening van Markeringen moet opnieuw toelaten om tot het later toegang te hebben.De standaardwaarde voor de Mening van Markeringen voor de zitting van een nieuwe gebruiker wordt bepaald door het bezit tagsView in het ui \_config.json- dossier. Zie voor meer informatie de *Standaardwaarde voor weergave Codes configureren* in de sectie Adobe Experience Manager-hulplijnen installeren en configureren as a Cloud Service.

**Wijzigingen bijhouden inschakelen/uitschakelen** ![](images/track-change-icon.svg)

U kunt alle updates die op een document zijn aangebracht bijhouden door de modus Wijzigingen bijhouden in te schakelen. Nadat u wijzigingen in de track hebt ingeschakeld, worden alle invoegingen en verwijderingen vastgelegd in het document. Alle verwijderde inhoud wordt gemarkeerd met Doorhalen en alle invoegingen worden gemarkeerd in groene tekst. Bovendien krijgt u ook de veranderingsbars bij de rand van de onderwerppagina. Ook hier wordt een rode balk weergegeven voor verwijderde inhoud en een groene balk voor toegevoegde inhoud. Als er toevoeging en schrapping op de zelfde lijn is, dan zowel worden de groene als de rode bars getoond.

In de volgende schermafbeelding wordt de verwijderde en ingevoegde inhoud samen met de wijzigingsbalken gemarkeerd:

![](images/track-changes-content.png){width="650" align="left"}

Doorgaans kunnen wijzigingen in een document worden bijgehouden bij collegiale toetsing. U kunt wijzigingen bijhouden inschakelen en uw document delen voor revisie. De controleur brengt vervolgens wijzigingen aan met de functie Wijzigingen bijhouden ingeschakeld. Wanneer u het document ontvangt, hebt u een mechanisme nodig om de voorgestelde updates samen met een handige manier te bekijken om wijzigingen te accepteren of te negeren.

AEM Hulplijnen biedt de functie Bijgehouden wijzigingen die informatie bevat over de updates die in het document zijn aangebracht. De functie Bijgehouden wijzigingen biedt informatie over welke updates zijn uitgevoerd, wie deze heeft aangebracht en op welk moment. Met de functie Bijgehouden wijzigingen kunt u de voorgestelde updates in het document ook gemakkelijk accepteren of negeren.

Klik op het pictogram Bijgehouden wijzigingen in het rechterdeelvenster om de functie te openen.

![](images/changes-panel_cs.png){width="300" align="left"}

Als u op een wijziging klikt, wordt de gewijzigde inhoud in het document geselecteerd. U kunt een wijziging accepteren door het pictogram Wijziging accepteren te selecteren of deze te negeren door Wijzigen negeren te selecteren.

Als u met één klik alle wijzigingen wilt accepteren of negeren, selecteert u **Alles accepteren** of **Alles negeren**.

>[!NOTE]
>
> In de modus Voorvertoning kunt u het document met of zonder de gewijzigde markeringen van de inhoud weergeven. Zie voor meer informatie de [Voorvertoning](web-editor-views.md#preview-mode-id19AAGL00163) -modus.

**Samenvoegen** - ![](images/merge-icon.svg)

Wanneer u in een multi-auteurmilieu werkt, wordt het moeilijk om te volgen welke veranderingen de andere auteurs in een onderwerp of een kaart hebben aangebracht. Met de functie Samenvoegen hebt u meer controle over het weergeven van de wijzigingen, maar ook over de wijzigingen die in de meest recente versie van het document blijven staan.

**Onderwerpbestanden samenvoegen**

Voer de volgende stappen uit om wijzigingen in een onderwerp samen te voegen:

1. Een onderwerp openen in de webeditor.

1. Klikken **Samenvoegen**.

   Het dialoogvenster Samenvoegen wordt weergegeven.

   ![](images/merge-changes-in-topic.png){width="550" align="left"}

1. *\(Optioneel\)* U kunt ook bladeren naar een nieuw bestand en dit selecteren vanuit een andere locatie in de opslagplaats.

1. Selecteer een versie van het bestand waarmee u de huidige versie van het bestand wilt vergelijken.

1. Kies bij Opties de volgende opties:

   - **Wijzigingen bijhouden in geselecteerde versie**: Met deze optie worden alle updates van de inhoud weergegeven in de vorm van wijzigingen in tracks. Vervolgens kunt u kiezen of u de wijzigingen in het document een voor een wilt accepteren of wilt negeren, of in één keer.

   - **Geselecteerde versie herstellen**: Met deze optie wordt de huidige versie van het document hersteld naar de geselecteerde versie. Met deze optie kunt u niet bepalen welke inhoud wordt geaccepteerd of geweigerd.

1. Klikken **Gereed**.

1. Als u **Bijhouden gewijzigd van geselecteerde versie** worden alle wijzigingen van de geselecteerde versie weergegeven in de functie Bijgehouden wijzigingen in het rechterdeelvenster.

   U kunt ervoor kiezen alle opmerkingen in het deelvenster Bijgehouden wijzigingen te accepteren of te negeren, of afzonderlijke opmerkingen te accepteren of te negeren.


**Kaartbestanden samenvoegen**

Voer de volgende stappen uit om wijzigingen in een kaartbestand samen te voegen:

1. Een kaart openen in de webeditor.

1. Klikken **Samenvoegen**.

   Het dialoogvenster Samenvoegen wordt weergegeven.

   ![](images/merge-changes-in-map.png){width="550" align="left"}

1. *\(Optioneel\)* U kunt ook bladeren naar een nieuw bestand en dit selecteren vanuit een andere locatie in de opslagplaats.

1. Selecteer een versie van het bestand waarmee u de huidige versie van het bestand wilt vergelijken.

1. Kies bij Opties de volgende opties:

   - **Wijzigingen bijhouden in geselecteerde versie**: Met deze optie worden alle updates van de inhoud weergegeven in de vorm van wijzigingen in tracks. Vervolgens kunt u kiezen of u de wijzigingen in het document een voor een wilt accepteren of wilt negeren, of in één keer.

   - **Geselecteerde versie herstellen**: Met deze optie wordt de huidige versie van het document hersteld naar de geselecteerde versie. Met deze optie kunt u niet bepalen welke inhoud wordt geaccepteerd of geweigerd.

1. Klikken **Gereed**.

   1. Als u **Bijhouden gewijzigd van geselecteerde versie** worden alle wijzigingen van de geselecteerde versie weergegeven in het deelvenster Bijgehouden wijziging \(rechts\).

      U kunt ervoor kiezen om alle wijzigingen te accepteren of te negeren in het deelvenster Bijgehouden wijzigingen of om afzonderlijke wijzigingen in het kaartbestand te accepteren of te negeren.


**Versiehistorie** - ![](images/version-history-web-editor-ico.svg)


De **Versiehistorie** De eigenschap in de Redacteur van het Web staat u toe om de beschikbare versies van uw DITA- dossiers te controleren, hen te vergelijken, en aan om het even welke versie van de redacteur zelf terug te keren.

In de versiegeschiedenis kunt u de inhoud en metagegevens van de huidige versie (die ook een werkende kopie kan zijn) vergelijken met elke vorige versie van hetzelfde bestand. U kunt ook de labels en opmerkingen voor de vergeleken versies weergeven.

Ga als volgt te werk om de versiegeschiedenis te openen en terug te keren naar een specifieke versie van het onderwerp:

1. Een onderwerp openen in de webeditor.

1. Klikken **Versiehistorie**.

   De **Versiehistorie** wordt weergegeven.

   ![Dialoogvenster Versiehistorie](images/version-history-dialog-web-editor.png){width="550" align="left"}
   *Bekijk een voorvertoning van de wijzigingen in de verschillende versies van een onderwerp.*

1. Kies een versie van het onderwerp dat u wilt vergelijken of waar in terug in **Vergelijken met** vervolgkeuzelijst.

   >[!NOTE]
   >
   > Als er op een versie labels zijn toegepast, worden deze ook tussen haakjes en het versienummer weergegeven.



1. Inschakelen **Labels en opmerkingen weergeven** om de labels en opmerkingen weer te geven die zijn toegepast op de huidige en de vergeleken versies.

1. U kunt ook de volgende informatie weergeven in het dialoogvenster **Versiehistorie** dialoogvenster:

   **Voorvertoning** tab: De toegevoegde inhoud is in een groen lettertype en de verwijderde inhoud in een rood lettertype.

   **Metagegevens** tab: De toegevoegde metagegevens zijn in een groen lettertype en de verwijderde metagegevens in een rood lettertype.
   ![Metagegevensverschil voor versies ](images/metadata-version-diff.png){width="550" align="left"}
   *Vergelijk de metagegevens van verschillende versies in de versiegeschiedenis.*

   >[!NOTE]
   >
   > De systeembeheerder kan de metagegevens wijzigen die moeten worden weergegeven op het tabblad Metagegevens in de Editor-instellingen.

   U kunt ook de gebruikers- en tijdgegevens weergeven van de huidige en de vergeleken versie.



1. Wanneer u een versie in de vervolgkeuzelijst kiest, wordt de **De optie Geselecteerde versie herstellen** beschikbaar gesteld. Het voorproefvenster toont de verschillen tussen de huidige versie en de geselecteerde versie van het onderwerp.


1. Klikken **Geselecteerde versie herstellen** om uw het werk exemplaar met de geselecteerde versie van het onderwerp terug te keren.

   Het dialoogvenster Versie herstellen wordt weergegeven.

   ![](images/version-history-revert-dialog-save-working-copy.png){width="550" align="left"}

1. \(*Optioneel*\) Geef een reden op om terug te keren naar een eerdere versie. U kunt ook een nieuwe versie maken van de actieve werkkopie van het onderwerp.

1. Klikken **Bevestigen.**

   De werkkopie van het bestand wordt teruggezet naar de geselecteerde versie. Als u ervoor kiest een nieuwe versie van de momenteel actieve werkkopie te maken, wordt ook een nieuwe versie van het bestand gemaakt met alle werkwijzigingen.


Wanneer u terugkeert naar een eerdere versie, wordt een visuele aanwijzing getoond die erop wijst dat de versie u momenteel werkt aan niet de recentste versie is.

![](images/older-version-visual-cue.png){width="800" align="left"}

**Versielabelbeheer** -  ![](images/version-label-icon.svg)

Met labels kunt u het werkgebied identificeren waarin een bepaald onderwerp zich in de DDLC \(Levenscyclus voor documentontwikkeling\) bevindt. Wanneer u bijvoorbeeld aan een onderwerp werkt, kunt u het label &quot;Goedgekeurd&quot; instellen. Zodra een onderwerp wordt gepubliceerd en ter beschikking gesteld aan klanten, kunt u &quot;Vrijgegeven&quot;etiket aan dat onderwerp toewijzen.

Met AEM hulplijnen kunt u labels opgeven in een tekstindeling met vrije vorm of een set vooraf gedefinieerde labels gebruiken. Met het aangepaste label kan elke auteur in het systeem naar keuze een label opgeven. Dit geeft flexibiliteit, maar het introduceert inconsistente labels in het systeem. Om dit probleem te verhelpen, kunnen beheerders een set vooraf gedefinieerde labels configureren. Zie voor meer informatie over het configureren van vooraf gedefinieerde labels *De XML-webeditor configureren en aanpassen* in de as a Cloud Service Adobe Experience Manager-hulplijnen installeren en configureren.

Deze labels worden in de vorm van een vervolgkeuzelijst weergegeven aan auteurs, waar ze een label moeten opgeven. Dit zorgt ervoor dat alleen vooraf gedefinieerde, consistente labels in het systeem worden gebruikt.

Er zijn verschillende methoden om labels toe te passen op uw onderwerpen - [Versiehistorie](web-editor-use-label.md) paneel in de interface Elementen, [Basislijnen](/help/product-guide/user-guide/generate-output-use-baseline-for-publishing.md) UI en de Redacteur van het Web. De eigenschap van het Etiket van de Versie in de Redacteur van het Web geeft auteurs snelle en gemakkelijke manier om etiketten aan hun onderwerpen toe te wijzen.

Om etiketten aan uw onderwerp van de Redacteur van het Web toe te voegen, voer de volgende stappen uit:

1. Een onderwerp openen in de webeditor.

1. Klikken **Versielabel**.

   Het dialoogvenster Versielabelbeheer wordt geopend.

   ![](images/version-label-management-dialog.png){width="650" align="left"}

   Het dialoogvenster Versielabelbeheer is opgedeeld in twee delen. Het linkerdeelvenster bevat een lijst met versies die beschikbaar zijn voor het onderwerp, samen met de vervolgkeuzelijst met labels \(of een tekstvak waarin een label\ wordt ingevoerd) en het rechterdeelvenster met een voorvertoning van het onderwerp.

1. Selecteer een versie waarop u labels wilt toepassen.

   Wanneer u een verschillende versie van het onderwerp van de versielijst kiest, dan toont het voorproefpaneel de veranderingen tussen de huidige versie en de geselecteerde versie van het onderwerp

   >[!NOTE]
   >
   > Als een label al op een versie is toegepast, wordt het naast het versienummer weergegeven in de vervolgkeuzelijst en onder de lijst Selecteer versie. U kunt een bestaand label verwijderen door te klikken op \(**x**\) naast het label.

1. Als de beheerder een lijst met labels heeft gedefinieerd, wordt een vervolgkeuzelijst met de labels weergegeven waaruit u de labels kunt kiezen die u wilt toepassen. U kunt meerdere labels selecteren in de vervolgkeuzelijst.

   Anders, wordt u getoond een tekstvakje, waar u de etiketten kunt ingaan die u aan uw onderwerp wilt toevoegen.

   >[!NOTE]
   >
   > U kunt niet het zelfde etiket op veelvoudige versies van een onderwerp toepassen. Als u probeert om een bestaand etiket te associëren, dan krijgt u een optie om het uit de bestaande versie te verwijderen en het op de geselecteerde versie van het onderwerp toe te passen.

1. Klikken **Label toevoegen**.

1. Selecteer in het bevestigingsbericht Label toepassen de optie **Label verplaatsen** om labels van een bestaande versie naar de geselecteerde versie te verplaatsen. Als u deze optie niet selecteert en er etiketten zijn die aan een verschillende versie van het onderwerp worden toegewezen, dan worden zij niet verplaatst naar de geselecteerde versie van het onderwerp. Dergelijke labels worden genegeerd in het labeltoepassingsproces.


**Revisietaak maken** -  ![](images/create-review-task-icon.svg)

U kunt een overzichtstaak van het huidige onderwerp of kaartdossier direct van de Redacteur van het Web tot stand brengen. Open het bestand waarvoor u de revisietaak wilt maken en klik op Revisietaak maken om het proces voor het maken van de revisie te starten.

>[!NOTE]
>
> U kunt ook een revisietaak maken via het deelvenster Revisie \(aan de rechterkant\).

Volg de instructies in de [Onderwerpen of kaarten controleren](review.md#) voor meer informatie .

## Deelvenster Links {#id2051EA0M0HS}

Het linkerdeelvenster is een permanent deelvenster. U kunt het uit- of samenvouwen door te klikken op het pictogram Zijbalk uitvouwen \(![](images/sidebar-expand-icon.svg)\). In de uitgevouwen weergave worden de namen van de pictogrammen weergegeven die als knopinfo worden weergegeven in de samengevouwen weergave.

>[!NOTE]
>
> U kunt het formaat van het linkerdeelvenster wijzigen. Als u de grootte van het deelvenster wilt wijzigen, plaatst u de cursor op de rand van het deelvenster, verandert de cursor in een dubbele pijl, klikt en sleept u om de breedte van het deelvenster aan te passen.

In het linkerdeelvenster hebt u toegang tot de volgende functies:

**Favorieten** -  ![](images/favorite-collections.svg)

Als u werkt aan een set bestanden of mappen, kunt u deze toevoegen aan uw favoriete lijst en ze snel openen. De lijst Favorieten bevat de lijst met documenten die u hebt toegevoegd en andere openbaar toegankelijke lijsten met favoriete documenten van de andere gebruikers.
Standaard kunt u de bestanden op titels weergeven. Terwijl u de cursor op een bestand plaatst, kunt u de bestandstitel en het bestandspad weergeven als knopinfo.
>[!NOTE]
>
> Als beheerder, kunt u ook verkiezen om de lijst van dossiers door filenames in de Redacteur van het Web te bekijken. Selecteer de **Bestandsnaam** van de **Bestanden weergeven op** sectie in **Gebruikersvoorkeuren** ![](images/user_preference_editor_icon.svg).

Als u een favoriete lijst of verzameling wilt maken, klikt u op het pictogram + naast het deelvenster Favorieten om het logboek New Collection Media weer te geven:

![](images/favorite-new-collection.PNG){width="300" align="left"}

Voer een titel en beschrijving in voor de favoriete verzameling die u wilt maken. Als u **Openbaar** Deze favoriet wordt ook aan andere gebruikers getoond.

Als u een bestand aan uw favoriete verzameling wilt toevoegen, gebruikt u een van de volgende methoden:

- Navigeer naar het gewenste bestand of de gewenste map in de weergave Opslag en klik op de knop *Opties* pictogram om het contextmenu te openen en **Toevoegen aan Favorieten**. In het dialoogvenster Toevoegen aan Favorieten kunt u het bestand of de map toevoegen aan een bestaande favoriet of een nieuw bestand maken.

  ![](images/favorite-add-file-folder.png){width="300" align="left"}

- Klik met de rechtermuisknop op het tabblad van een bestand in de editor om het contextmenu te openen. Kies **Toevoegen aan** > **Favorieten** om het bestand toe te voegen aan uw lijst met favorieten.

  ![](images/favorite-add-from-file-context-menu_cs.png){width="400" align="left"}

>[!NOTE]
>
> - Als u een item uit de lijst Favorieten wilt verwijderen, selecteert u het pictogram Opties naast het item in een verzameling Favorieten en kiest u **Verwijderen uit Favorieten**.
> - Als u het bestand wilt bekijken zonder het te openen, selecteert u een bestand en selecteert u vervolgens **Voorvertoning** in het menu Opties.



**Menu Opties voor de verzameling Favroties**\
U kunt ook veel handelingen uitvoeren met het menu Opties dat beschikbaar is voor een verzameling Favorieten:

![](images/favorites-options.png){width="400" align="left"}
- **Naam wijzigen**: Wijzig de naam van de geselecteerde verzameling.
- **Verwijderen**: Verwijder de geselecteerde verzameling.
- **Vernieuwen**: Haal een nieuwe lijst met bestanden en mappen op uit de opslagplaats.
- **Weergeven in interface Elementen**: De inhoud van het bestand of de map weergeven in de interface Middelen.

>[!NOTE]
>
> U kunt de lijst ook vernieuwen met het pictogram Vernieuwen bovenaan.


**Weergave opslagplaats** - ![](images/Repository_icon.svg)

Wanneer u op het pictogram Weergave opslagplaats klikt, wordt een lijst met bestanden en mappen beschikbaar in DAM. Standaard kunt u de bestanden op titels weergeven. Terwijl u de cursor op een bestand plaatst, kunt u de bestandstitel en de bestandsnaam als knopinfo weergeven.

>[!NOTE]
>
> Als beheerder, kunt u ook verkiezen om de lijst van dossiers door filenames in de Redacteur van het Web te bekijken. Selecteer de **Bestandsnaam** van de **Bestanden weergeven op** sectie in **Gebruikersvoorkeuren** ![](images/user_preference_editor_icon.svg).


Er worden 75 bestanden tegelijk geladen. Elke keer dat u klikt **Meer laden**... 75 bestanden worden geladen en de knop wordt niet meer weergegeven wanneer alle bestanden zijn weergegeven. Het laden van deze batch is efficiënt en u hebt sneller toegang tot de bestanden dan tot het laden van alle bestanden in een map.

U kunt gemakkelijk naar het vereiste dossier binnen DAM navigeren en het openen in de Redacteur van het Web. Als u de vereiste toegang hebt om het bestand te bewerken, kunt u dat doen.

U kunt ook op een audio- of videobestand in de webeditor klikken en dit afspelen. U kunt het volume of de weergave van de video wijzigen. In het snelmenu hebt u ook de mogelijkheid om de afspeelsnelheid te downloaden, te wijzigen of de afbeelding in beeld te bekijken.



Selecteer een kaart en druk binnengaan of dubbelklik om het in te openen in **Kaartweergave**. Zie voor meer informatie de **Kaartweergave** functiebeschrijving in het dialoogvenster [Linkerdeelvenster](web-editor-features.md#id2051EA0M0HS) sectie. Selecteer een onderwerp en druk binnengaan of tweemaal klikken om het in te openen in [Inhoudsbewerkingsgebied](#id2051EB000UI). Als u een bestand rechtstreeks vanuit de webeditor kunt openen en er kunt navigeren, bespaart u tijd en verhoogt u de productiviteit.

**Filter Zoeken**

De webeditor biedt verbeterde filters voor het zoeken naar tekst. U kunt zoeken en filteren naar tekst in de bestanden die zich op het geselecteerde pad van de Adobe Experience Manager-opslagplaats bevinden. Deze zoekt in de titel, de bestandsnaam en de inhoud in de bestanden.


![zoekbestanden in de dataweergave](images/repository-filter-search.png){width="300" align="left"}

*Filters toepassen op de zoekopdracht naar de bestanden die de tekst bevatten`general purpose.`*

Selecteer de **Filter Zoeken** \(![Filterpictogram Zoeken](images/filter-search-icon.svg)\) gebruiken om het filter op pop-up te openen.

>[!NOTE]
>
> Wanneer u tekst doorzoekt of bestanden filtert, verschijnt er een blauwe stip op het tabblad **Filter Zoeken**  \(![Filterpictogram Zoeken](images/filter-search-icon.svg)\) om aan te geven dat we in het deelvenster Zoeken staan en dat sommige filters zijn toegepast.


U hebt de volgende opties om de bestanden te filteren en uw zoekopdracht in de Adobe Experience Manager-opslagplaats te beperken:

- **DITA-bestanden**: U kunt alles zoeken **DITA-onderwerpen** en **DITA-kaarten** aanwezig op het geselecteerde pad. Deze zijn standaard geselecteerd.
- **Niet-DITA-bestanden**: U kunt zoeken naar **Ditavale bestanden**,  **Afbeeldingsbestanden**, **Multimedia**, **Documenten**, en **Json** in het geselecteerde pad.

![snelzoekfilter ](images/repository-filter-search-quick.png) {width="300" align="left"}

*Gebruik de snelle filters om naar DITA en niet-DITA dossiers te zoeken.*

**Geavanceerd filteren**

Selecteer de **Geavanceerd filteren** ![pictogram geavanceerd filter](images/advanced-filter-gear-icon.svg)pictogram om het **Geavanceerd filter** in.

U kunt de volgende opties weergeven onder de **Algemeen** en **Geavanceerd** tabs.

![dialoogvenster voor geavanceerd filter](images/repository-filter-search-advanced.png) {width="800" align="left"}


**Algemeen**

- **De zoekresultaten zijn als volgt**: Zoek naar tekst in de bestanden op het geselecteerde pad van de Adobe Experience Manager-opslagplaats. De tekst wordt doorzocht in de titel, de bestandsnaam en de inhoud in de bestanden.

Dit is synchroon met het zoekvak in het venster Opslagplaats. Als u bijvoorbeeld `general purpose` in het zoekvak in het paneel van de repository wordt het ook weergegeven in **Geavanceerd filter** en omgekeerd.

- **Zoeken in**: Selecteer het pad waar u de bestanden in de Adobe Experience Manager-opslagplaats wilt zoeken.

- **Uitgecheckt door**: U kunt zoeken naar bestanden die de opgegeven gebruiker uitcheckt.
- **Laatst gewijzigd**: U kunt zoeken naar bestanden die het laatst zijn gewijzigd na een geselecteerde datum, maar vóór een geselecteerde datum.
- **Gewijzigd vóór**: U kunt zoeken naar bestanden die het laatst zijn gewijzigd vóór een geselecteerde datum.
- **Tijdskader**: U kunt ook zoeken naar bestanden die de laatste twee uur, vorige week, vorige maand of vorig jaar zijn gewijzigd.
- **Tags**: U kunt zoeken naar bestanden waarop specifieke tags zijn toegepast. U kunt de tag typen of deze selecteren in de vervolgkeuzelijst.

**Geavanceerd**

- **DITA-elementen**: U kunt ook zoeken naar specifieke waarden in de kenmerken van de opgegeven DITA-elementen.
   - Selecteren **Element toevoegen** ![pictogram toevoegen](images/Add_icon.svg) om de elementen, kenmerken en waarden toe te voegen.
   - Pas de filters toe die u hebt geselecteerd.

- Selecteren **Alles wissen** om alle toegepaste filters te wissen.


- Selecteer de **Filter sluiten** ![pictogram sluiten](images/close-icon.svg) om het filter te sluiten en terug te keren naar de boomstructuurweergave van de repository.
  >[!NOTE]
  >
  >Uw systeembeheerder kan de tekstfilters ook vormen en andere filters tonen of verbergen. Zie voor meer informatie *Tekstfilters configureren* in de sectie Adobe Experience Manager-hulplijnen installeren en configureren as a Cloud Service.

  De lijst met gefilterde bestanden die de gezochte tekst bevatten, wordt weergegeven. De bestanden met de tekst `general purpose` worden weergegeven in de vorige schermafbeelding. U kunt meerdere bestanden in de gefilterde lijst selecteren en ze naar een kaart slepen die u wilt bewerken.




**Menu Opties**

Naast het openen van bestanden vanuit het linkerdeelvenster kunt u ook een groot aantal handelingen uitvoeren via het menu Opties in de Weergave opslagplaats. U ziet verschillende opties, afhankelijk van of u een omslag, een onderwerpdossier, of een media dossier kiest.

**Opties voor een map**

U kunt de volgende handelingen uitvoeren met het menu Opties van een *map* in de weergave Opslagplaats:

![](images/options-menu-folder_cs.PNG){width="550" align="left"}


- **Maken**: Maak een nieuw DITA-onderwerp, een DITA-kaart of een map. Zie voor meer informatie de  **Onderwerpen maken in de weergave Opslagplaats** in de [Linkerdeelvenster](web-editor-features.md#id2051EA0M0HS) sectie.



- **Elementen uploaden**: Upload een bestand van uw lokale systeem naar de geselecteerde map in de Adobe Experience Manager-opslagplaats. U kunt bestanden ook van uw lokale systeem naar het huidige werkonderwerp slepen. Dit is zeer nuttig als u beelden van uw lokaal systeem in uw onderwerp wilt opnemen.

  ![](images/upload-assets.png){width="550" align="left"}

  U kunt een map selecteren waarin u het bestand wilt uploaden en er wordt ook een voorvertoning van de afbeelding weergegeven. Als u de naam van het bestand wilt wijzigen, kunt u dit doen in het tekstvak Bestandsnaam. Klik op Uploaden om het uploaden van het bestand te voltooien. Als u een afbeeldingsbestand over een onderwerp hebt gesleept en neergezet, wordt het afbeeldingsbestand aan het artikel toegevoegd en wordt het ook geüpload.

  Als de beheerder de optie UUID&#39;s heeft ingeschakeld in *XMLEditorConfig*, dan ziet u de UUID van de geüploade afbeelding in het dialoogvenster **Bron** eigenschap.

  ![](images/uuid-in-source-upload-image_cs.png){width="800" align="left"}

- **Bestanden zoeken in map**: Hiermee verplaatst u de focus naar de zoekopdracht in de repository waarin u de zoekterm kunt invoeren. De zoekopdracht wordt uitgevoerd onder de geselecteerde map in de opslagplaats. U kunt ook een filter toepassen om DITA-bestanden, afbeeldingsbestanden of beide te retourneren.

  ![](images/find-files-in-folders-repo-view_cs.png){width="400" align="left"}

  U kunt ook zoeken met de UUID van een bestand. In dat geval wordt in de zoekresultaten de titel van het DITA/XML-bestand weergegeven. Als het bestand een afbeeldingsbestand is, wordt de UUID van het bestand weergegeven. In het volgende zoekvoorbeeld wordt de UUID van een afbeeldingsbestand doorzocht en worden in de zoekresultaten de UUID van het oorspronkelijke afbeeldingsbestand en de onderwerptitel van het bestand weergegeven waarnaar wordt verwezen.

  ![](images/uuid-repo-search-image-topic-file_cs.png){width="300" align="left"}

- **Alles samenvouwen**: Vouw alle geopende mappen in de opslagplaats samen en geef alleen de mappen op hoofdniveau weer.

  >[!NOTE]
  >
  > Gebruik de **\>** pictogram naast een map om deze uit te vouwen.

- **Toevoegen aan Favorieten**: Voegt de geselecteerde map toe aan de favorieten. U kunt desgewenst toevoegen aan een bestaande of nieuwe favoriete verzameling.

- **Vernieuwen**: Haal een nieuwe lijst met bestanden en mappen op uit de opslagplaats.
- **Weergeven in interface Elementen**: De inhoud van de map weergeven in de interface Middelen.

**Opties voor een bestand**

U ziet verschillende opties in het menu Opties, afhankelijk van het feit of u een mediabestand of een DITA-bestand selecteert. Enkele algemene opties die beschikbaar zijn voor media en DITA-bestanden zijn:

- Dupliceren
- Uitchecken/inchecken
- Voorvertoning
- Verplaatsen naar
- Naam wijzigen
- Verwijderen
- Kopiëren
- Alles samenvouwen
- Toevoegen aan Favorieten
- Eigenschappen
- Weergeven in interface Elementen

![optiemenu van een bestand in de dataweergave](images/options-menu-repo-view-file-level.png){width="550" align="left"}

De verschillende opties in het menu Opties worden hieronder uitgelegd:

- **Bewerken**: Open het bestand voor bewerking. In het geval van een .ditamap/.bookmap-bestand, wordt het geopend in het dialoogvenster [Geavanceerde kaarteditor](map-editor-advanced-map-editor.md#) voor bewerken.

- **Dupliceren**: Gebruik deze optie om een kopie of kopie van het geselecteerde bestand te maken. U kunt de naam van het gedupliceerde bestand ook wijzigen in de vraag Elementen dupliceren. Standaard wordt het bestand gemaakt met het achtervoegsel \(zoals bestandsnaam\_1.extension\). De titel van het bestand blijft dezelfde als het bronbestand en het nieuwe bestand begint met versie 1.0. Alle verwijzingen, markeringen, en meta-gegevens worden gekopieerd terwijl de basislijnen niet in het dubbele dossier worden gekopieerd.
- **Uitchecken**: Vergrendel het geselecteerde bestand om het te bewerken. Voor een vergrendeld bestand verandert deze optie in **Inchecken**.

  >[!NOTE]
  >
  > - Als een bestand is vergrendeld of uitgecheckt door een gebruiker en u de muisaanwijzer boven het vergrendelingspictogram houdt, wordt de gebruiker \(naam\) weergegeven die het bestand heeft vergrendeld.
  > - Wanneer u een bestand incheckt dat niet-opgeslagen wijzigingen bevat, wordt u gevraagd de wijzigingen op te slaan. Als u uw wijzigingen niet opslaat, wordt alleen het bestand gecontroleerd.

- **Voorvertoning**: U kunt een snelle voorvertoning van het bestand (.dita, .xml, audio, video of afbeelding) weergeven zonder het te openen. U kunt het formaat van het voorvertoningsvenster wijzigen. Als de inhoud een `<xref>` of `<conref>`kunt u deze selecteren en openen op een nieuw tabblad. De titel van het bestand wordt weergegeven in het venster. Als er geen titel aanwezig is, wordt de bestandsnaam weergegeven. Als u het dialoogvenster **Voorvertoning** kunt u het sluitingspictogram selecteren of ergens buiten het deelvenster klikken.

  ![](images/quick-preview_cs.png){width="800" align="left"}

- **Naam wijzigen**: Gebruik deze optie om de naam van het geselecteerde bestand te wijzigen. Voer de naam van het nieuwe bestand in het dialoogvenster **Naam element wijzigen** in.
   - U kunt de naam van een bestand van elk type wijzigen.
   - U kunt de extensie van een bestand niet wijzigen.
   - Twee bestanden kunnen niet dezelfde naam hebben. U kunt de naam van een bestand dus niet wijzigen in een bestaande naam. Er wordt een fout weergegeven.

- **Verplaatsen naar**: Gebruik deze optie om het geselecteerde bestand naar een andere map te verplaatsen.
   - U kunt de naam van de doelmap typen of **Pad selecteren** om de doelmap te selecteren.
   - U kunt een bestand van elk type verplaatsen naar een willekeurig doel in de map Inhoud.
   - Twee bestanden kunnen niet dezelfde naam hebben. U kunt een bestand dus niet verplaatsen naar een map waarin al een bestand met dezelfde naam bestaat.

  Als u een bestand probeert te verplaatsen naar een map waarin een bestand met dezelfde naam maar een andere titel bestaat, wordt het dialoogvenster Naam wijzigen en bestand verplaatsen weergegeven en moet u de naam van het bestand wijzigen voordat u het bestand verplaatst. Het verplaatste bestand in de doelmap heeft de nieuwe bestandsnaam.

  ![](images/rename-move-asset.png){width="550" align="left"}

  >[!NOTE]
  > U kunt een bestand ook naar een andere doelmap slepen.

  **Uitsluitingsscenario&#39;s**

  Met AEM hulplijnen kunt u de naam van een bestand niet wijzigen of een bestand verplaatsen in de volgende gevallen:

   - U kunt een bestand niet verplaatsen of de naam ervan wijzigen als het deel uitmaakt van een revisie of een vertaalworkflow.

   - Als een andere gebruiker het bestand uitcheckt, kunt u de naam van het bestand niet wijzigen of het bestand verplaatsen, wordt de optie Naam wijzigen of Verplaatsen naar voor het bestand niet weergegeven.

  >[!NOTE]
  > Als uw beheerder u de toestemmingen op een omslag heeft gegeven, dan slechts **Naam wijzigen** of **Verplaatsen naar** worden weergegeven.

  <details>
    <summary> Cloud Servicen </summary>

  Als u de naam van een bestand wijzigt of een bestand verplaatst, worden bestaande verwijzingen van of naar het bestand niet verbroken, omdat elk bestand een unieke UUID heeft.
  </details>



- **Verwijderen**: Gebruik deze optie om het geselecteerde bestand te verwijderen. Er wordt een bevestigingsbericht weergegeven voordat u het bestand verwijdert.

   - Er wordt een bevestigingsbericht weergegeven voordat u het bestand verwijdert.
   - Als er vanuit een ander bestand niet naar het bestand wordt verwezen, wordt het bestand verwijderd en wordt een succesbericht weergegeven.
   - Als het bestand is uitgecheckt, kunt u het niet verwijderen en wordt een foutbericht weergegeven.

     >[!NOTE]
     >
     > Als uw beheerder het verwijderen van uitgecheckte bestanden heeft verhinderd, wordt alleen het foutbericht weergegeven. Zie voor meer informatie *Verwijderen van uitgecheckte bestanden voorkomen* in de sectie Adobe Experience Manager-hulplijnen installeren en configureren as a Cloud Service.

   - Als het bestand wordt toegevoegd aan een favoriete verzameling, wordt de opdracht **Verwijderen forceren** wordt weergegeven en u kunt dit met kracht verwijderen.
   - Als er vanuit een ander bestand naar het bestand wordt verwezen, dan **Verwijderen forceren** wordt weergegeven en u kunt het bestand met kracht verwijderen:

     ![](images/options-menu-force-delete.png){width="550" align="left"}

     >[!NOTE]
     >
     > Als uw beheerder toestemming heeft gegeven om het bestand te verwijderen, dan **Verwijderen forceren** is ingeschakeld. Anders, **Verwijderen forceren** is uitgeschakeld en er wordt een bericht weergegeven dat u geen toestemming hebt om bestanden waarnaar wordt verwezen, te verwijderen. Zie voor meer informatie *Verwijderen van bestanden waarnaar wordt verwezen voorkomen* in de sectie Adobe Experience Manager-hulplijnen installeren en configureren as a Cloud Service.

   - Als u een onderwerp waarnaar wordt verwezen verwijdert en u het bestand met verwijzingen hebt geopend voor bewerken, wordt de verbroken koppeling voor het bestand waarnaar wordt verwezen, weergegeven.

  >[!NOTE]
  >
  > U kunt het geselecteerde bestand ook verwijderen met de toets Delete van het toetsenbord.

- **Kopiëren**: U kunt uit de volgende opties kiezen:

   - **UUID kopiëren**: Kopieer de UUID van het geselecteerde bestand naar het klembord.

   - **Pad kopiëren**: Kopieer het volledige pad van het geselecteerde bestand naar het klembord.

- **Alles samenvouwen**: Vouw alle bestanden in de opslagplaats samen. Alleen de mappen op het hoogste niveau in de opslagplaats worden weergegeven.
- **Toevoegen aan**: U kunt uit de volgende opties kiezen:
   - **Favorieten**: Voegt het geselecteerde bestand toe aan favorieten. U kunt desgewenst toevoegen aan een bestaande of nieuwe favoriete verzameling.

   - **Herbruikbare inhoud**: Hiermee voegt u het geselecteerde bestand toe aan de lijst Herbruikbare inhoud in het linkerdeelvenster.

- **Eigenschappen**: Gebruik deze optie om de eigenschappenpagina van het geselecteerde bestand te openen. U kunt deze eigenschappenpagina ook openen vanuit de interface Middelen door een bestand te selecteren en op het pictogram Eigenschappen op de werkbalk te klikken.

- **Kaartdashboard openen**: Als het geselecteerde bestand een DITA-kaart is, wordt met deze optie het kaartdashboard geopend.

- **Bewerken in zuurstof**: Selecteer deze optie om het geselecteerde bestand te bewerken in de insteekmodule Zuurstofaansluiting. Het bestand wordt geopend voor bewerking.

  >[!NOTE]
  >
  >Neem contact op met het team voor succes van uw klant om deze functie in de omgeving in te schakelen. Dit wordt niet toegelaten als deel van uit-van-de-doos steun. Voor meer informatie bekijkt u de [De optie configureren om te bewerken in zuurstof](../cs-install-guide/conf-edit-in-oxygen.md) in de installatie- en configuratiehandleiding.


- **Weergeven in interface Elementen**: Gebruik deze optie om een voorbeeld van een .dita/.xml-bestand in de interface Elementen weer te geven. In het geval van een .ditamap/.bookmap- dossier, worden alle onderwerpdossiers binnen de kaart getoond in één enkele verenigde pagina-door-pagina mening.

- **Downloaden als PDF**: Gebruik de optie om de uitvoer van de PDF te genereren en te downloaden.

- **Publiceren als**: Gebruik de optie om een onderwerp of de elementen binnen een onderwerp naar een inhoudsfragment te publiceren.

- **Snel genereren**: Genereer de uitvoer voor het geselecteerde bestand. Uitvoer kan alleen worden gegenereerd voor bestanden die deel uitmaken van een uitvoervoorinstelling. Zie voor meer informatie [Publiceren op basis van artikelen vanuit de webeditor](web-editor-article-publishing.md#id218CK0U019I).


**Onderwerpen maken in de weergave Opslagplaats**

U kunt een nieuw onderwerp, een nieuwe kaart, of een nieuwe omslag van + pictogram naast het paneel van de Bewaarplaats of van het contextmenu van een omslag in de Mening van de Bewaarplaats kiezen.

***Een onderwerp maken***

Wanneer u ervoor kiest *een nieuw onderwerp maken* in het menu krijgt u het volgende dialoogvenster:

![](images/create-topic-dialog.png){width="300" align="left"}

In de **Nieuw onderwerp maken** geeft u de volgende gegevens op:

- Een malplaatje waarop het onderwerp zal worden gebaseerd. Bijvoorbeeld, voor een uit-van-de-doos opstelling, kunt u van Lege, Concept, DITAVAL, Verwijzing, Taak, Onderwerp, en de malplaatjes van het Oplossen van problemen kiezen.

  Als er in uw map een mapprofiel is geconfigureerd, worden alleen de onderwerpsjablonen weergegeven die in het mapprofiel zijn geconfigureerd.

- Pad waar u het onderwerpbestand wilt opslaan. Standaard wordt het pad van de geselecteerde map in de opslagplaats weergegeven in het veld Pad.
- Een titel voor het onderwerp.

- *\(Optioneel\)* De bestandsnaam voor het onderwerp. De bestandsnaam wordt automatisch voorgesteld op basis van de titel van het onderwerp.

  Als uw beheerder automatische bestandsnamen heeft ingeschakeld op basis van de UUID-instelling, ziet u het veld Naam niet zoals in de volgende schermafbeelding wordt getoond:

  ![](images/new-topic-without-filename.PNG){width="300" align="left"}


Wanneer u op **Maken**, wordt het onderwerp gecreeerd bij de gespecificeerde weg. Ook, wordt het onderwerp geopend in de Redacteur van het Web voor het uitgeven.

***Een DITA-kaart maken***

Wanneer u ervoor kiest *een nieuwe DITA-kaart maken* krijgt u het volgende dialoogvenster:

![](images/create-map-dialog.png){width="300" align="left"}

In de **Nieuwe kaart maken** geeft u de volgende gegevens op:

- Een sjabloon waarop de kaart wordt gebaseerd. Bijvoorbeeld, voor een uit-van-de-doos opstelling, kunt u van de de kaartmalplaatjes kiezen van Bookmap of DITA.

- Pad waarin u het kaartbestand wilt opslaan. Standaard wordt het pad van de geselecteerde map in de opslagplaats weergegeven in het veld Pad.
- A **Titel** voor de kaart.

- *\(Optioneel\)* De bestandsnaam voor de kaart. De bestandsnaam wordt automatisch voorgesteld op basis van de maptitel.

  Als de beheerder automatische bestandsnamen heeft ingeschakeld op basis van de UUID-instelling, wordt het veld Naam niet weergegeven.


Wanneer u op **Maken**, wordt de kaart gemaakt en toegevoegd in de map die is opgegeven in het veld Pad. De kaart wordt ook geopend in de Kaartweergave. U kunt het kaartdossier in de Redacteur van de Kaart openen en onderwerp aan het toevoegen. Voor meer informatie over het toevoegen van onderwerpen aan een kaartdossier, zie [Een kaart maken](map-editor-create-map.md#).

***Een map maken***

Wanneer u ervoor kiest *een nieuwe map maken*, krijgt u de **Nieuwe map maken** dialoogvenster:

![](images/new-folder-dialog_cs.png){width="300" align="left"}

Voer een **Titel** voor de map, die automatisch wordt omgezet in de mapnaam. Het pad is het pad waarin u het kaartbestand wilt opslaan. Standaard wordt het pad van de geselecteerde map in de opslagplaats weergegeven in het veld Pad. Wanneer u op **Maken**, wordt de map gemaakt en toegevoegd in de map vanwaar de optie Map maken is uitgevoerd.

**Kaartweergave** -  ![](images/map-view-icon.svg)

Wanneer u op het pictogram Kaartweergave klikt, wordt een lijst met onderwerpen in het kaartbestand weergegeven. Als u geen kaartbestand hebt geopend, wordt de Kaartweergave leeg weergegeven. Als u dubbelklikt op een kaartbestand, wordt het kaartbestand in deze weergave geopend. U kunt op om het even welk dossier binnen de kaart tweemaal klikken om het in de Redacteur van het Web te openen.

Standaard kunt u de bestanden op titels weergeven. Terwijl u de cursor op een bestand plaatst, kunt u de bestandstitel en het bestandspad weergeven als knopinfo.
>[!NOTE]
>
>Als beheerder kunt u ook de bestandsnaam bekijken van de bovenliggende kaart die momenteel is geopend in de kaartweergave. Selecteer de **Bestandsnaam** van de **Bestanden weergeven op** sectie in **Gebruikersvoorkeuren** ![](images/user_preference_editor_icon.svg).


Wanneer u een kaart opent in de kaartweergave, wordt de titel van de huidige kaart weergegeven in het midden van de hoofdwerkbalk. Als de titel te lang is, wordt een ovaal weergegeven en kunt u de muisaanwijzer boven de titel houden om de volledige titel in de knopinfo weer te geven.

Wanneer u zeer belangrijke attributen voor het onderwerp of kaartverwijzingen bepaalt, kunt u de titel, het overeenkomstige pictogram, en de sleutel in het linkerpaneel bekijken. De toets wordt weergegeven als `keys=<key-name>`.

![toetsen in de kaartweergave](images/view-key-title-map-view.png){width="300" align="left"}

Als u bewerkingsrechten hebt voor de kaartbestanden, kunt u de bestanden ook bewerken. Voor meer informatie over het openen en het uitgeven van een onderwerp door kaart DITA, zie [Onderwerpen bewerken via de DITA-kaart](map-editor-advanced-map-editor.md#id17ACJ0F0FHS).


U kunt de volgende handelingen uitvoeren met het menu Opties van het kaartbestand:

![](images/options-menu-map-view_cs.png){width="550" align="left"}

- **Bewerken**: Open het kaartbestand voor bewerking in de Geavanceerde kaarteditor.

- **Alles selecteren**: Selecteer alle bestanden op de kaart.

- **Selectie wissen**: Hef de selectie van de geselecteerde bestanden op de kaart op.

- **Afhandeling en vergrendelen**: Uitchecken en vergrendelen van de geselecteerde bestanden op de kaart.

- **Afhandeling annuleren en ontgrendelen**: Hiermee ontgrendelt u het kaartbestand en maakt u het beschikbaar voor bewerking. De wijzigingen worden niet teruggezet naar de vorige versie.

- **Opslaan als nieuwe versie en ontgrendelen**: Maak een nieuwere versie en laat de vergrendeling van de geselecteerde bestanden op de kaart los.

- **Voorvertoning**: Open een voorvertoning van het kaartbestand. In deze weergave worden alle onderwerpbestanden in de kaart weergegeven in één weergave voor elke pagina.

- **Kopiëren**: U kunt uit de volgende opties kiezen:
   - **UUID kopiëren**: Kopieer de UUID van het kaartbestand naar het klembord.
   - **Pad kopiëren**: Kopieer het volledige pad van het kaartbestand naar het klembord.

- **Zoeken in opslagplaats**: geeft de locatie van het kaartbestand in de opslagplaats \(of DAM\) weer.

- **Toevoegen aan**: U kunt uit de volgende opties kiezen:
   - **Favorieten**: voegt het kaartbestand toe aan de favorieten. U kunt desgewenst toevoegen aan een bestaande of nieuwe favoriete verzameling.

   - **Herbruikbare inhoud**: Voegt het kaartbestand toe aan de lijst Herbruikbare inhoud in het linkerdeelvenster.

- **Eigenschappen**: Gebruik deze optie om de pagina met eigenschappen van het kaartbestand te openen. U kunt deze eigenschappenpagina ook openen vanuit de interface Middelen door een bestand te selecteren en op het pictogram Eigenschappen op de werkbalk te klikken.

- **Kaartdashboard openen**: Open het kaartdashboard.

- **Weergeven in interface Elementen**: Gebruik deze optie om een voorvertoning van het kaartbestand weer te geven in de interface Middelen. In deze weergave worden alle onderwerpbestanden in de kaart weergegeven in één weergave voor elke pagina.
- **Kaart downloaden**: Selecteer deze optie om het dialoogvenster **Kaart downloaden** in.
In de **Kaart downloaden** kunt u de volgende opties kiezen:
   - **Basislijn gebruiken**: Selecteer deze optie om een lijst met basislijnen op te halen die voor de DITA-kaart zijn gemaakt. Als u het kaartbestand en de inhoud ervan wilt downloaden op basis van een specifieke basislijn, selecteert u de basislijn in de vervolgkeuzelijst. Voor meer informatie over het werken met Baselines, bekijkt [Werken met basislijn](./generate-output-use-baseline-for-publishing.md).
   - **Bestandshiërarchie afvlakken**: Selecteer deze optie als u alle onderwerpen en mediabestanden waarnaar wordt verwezen, in één map wilt opslaan.

  U kunt het kaartbestand ook downloaden zonder een optie te selecteren. In dat geval worden de laatste voortgezette versies van de onderwerpen waarnaar wordt verwezen en de mediabestanden gedownload.


  Nadat u op de knop **Downloaden** knoop, wordt het kaartuitvoerpakketverzoek een rij gevormd. De **Succes** wordt weergegeven als het pakket is gemaakt.  U kunt op de knop **Downloaden** van de knop **Succes** in.

  U ontvangt een melding die klaar is voor downloaden op de kaart als de kaart kan worden gedownload. Als het downloaden mislukt, ontvangt u een melding dat het downloaden van de kaart is mislukt.

  U hebt toegang tot de downloadkoppeling via het AEM-meldingsvak. Selecteer het gegenereerde kaartbericht in het Postvak In als u de kaart in de ZIP-indeling wilt downloaden.

  >[!NOTE]
  >
  >  Standaard blijven de gedownloade kaarten vijf dagen in het AEM-vak.

- **Uitvoer genereren**: Genereer de uitvoer voor het geselecteerde kaartbestand. Uitvoer kan alleen worden gegenereerd voor bestanden die deel uitmaken van een uitvoervoorinstelling. Zie voor meer informatie [Publiceren op basis van artikelen vanuit de webeditor](web-editor-article-publishing.md#id218CK0U019I).
- **Sluiten**: Sluit het kaartbestand.



De volgende het schermopname toont het menu van Opties voor een dossier in de Mening van de Kaart DITA:

![](images/options-menu-file_cs.PNG){width="550" align="left"}

U kunt de volgende handelingen uitvoeren met het menu Opties:

- **Bewerken**: Open het bestand voor bewerking. In het geval van een .ditamap/.bookmap-bestand, wordt het geopend in het dialoogvenster [Geavanceerde kaarteditor](map-editor-advanced-map-editor.md#) voor bewerken.

- **Uitchecken**: Check het geselecteerde bestand uit. Voor een uitgecheckt bestand wordt deze optie gewijzigd in **Inchecken**.



  >[!NOTE]
  >
  > - Als een bestand is vergrendeld of uitgecheckt door een gebruiker en u de muisaanwijzer boven het vergrendelingspictogram houdt, wordt de gebruiker \(naam\) weergegeven die het bestand heeft vergrendeld.
  > - Wanneer u een bestand incheckt, wordt u gevraagd de wijzigingen op te slaan. Als u uw wijzigingen niet opslaat, wordt alleen het bestand gecontroleerd.

- **Voorvertoning**: U kunt een snelle voorvertoning van het bestand (.dita, .xml, audio, video of afbeelding) weergeven zonder het te openen. U kunt het formaat van het voorvertoningsvenster wijzigen. Als de inhoud een `<xref>` of `<conref>`kunt u deze selecteren en openen op een nieuw tabblad.  De titel van het bestand wordt weergegeven in het venster. Als er geen titel aanwezig is, wordt de bestandsnaam weergegeven. Als u het dialoogvenster **Voorvertoning** kunt u het sluitingspictogram selecteren of ergens buiten het deelvenster klikken.
- **Kopiëren**: U kunt uit de volgende opties kiezen:
   - **UUID kopiëren**: Kopieer de UUID van het geselecteerde bestand naar het klembord.
   - **Pad kopiëren**: Kopieer het volledige pad van het geselecteerde bestand naar het klembord.


- **Zoeken in opslagplaats**: Geeft de locatie van het geselecteerde bestand in de opslagplaats \(of DAM\) weer.
- **Alles uitbreiden**: Vouw alle onderwerpen in de kaartbestanden uit.

- **Alles samenvouwen**: Vouw alle onderwerpen samen die deel uitmaken van het huidige kaartbestand.

- **Toevoegen aan**: U kunt uit de volgende opties kiezen:
   - **Favorieten**: Voegt het geselecteerde bestand toe aan favorieten. U kunt desgewenst toevoegen aan een bestaande of nieuwe favoriete verzameling.

   - **Herbruikbare inhoud**: Hiermee voegt u het geselecteerde bestand toe aan de lijst Herbruikbare inhoud in het linkerdeelvenster.

- **Eigenschappen**: Gebruik deze optie om de eigenschappenpagina van het geselecteerde bestand te openen. U kunt deze eigenschappenpagina ook openen vanuit de interface Middelen door een bestand te selecteren en op het pictogram Eigenschappen op de werkbalk te klikken.

- **Weergeven in interface Elementen**: Gebruik deze optie om een voorbeeld van een .dita/.xml-bestand in de interface Elementen weer te geven. In het geval van een .ditamap/.bookmap- dossier, worden alle onderwerpdossiers binnen de kaart getoond in één enkele verenigde pagina-door-pagina mening.

- **Snel genereren**: Genereer de uitvoer voor het geselecteerde bestand. Uitvoer kan alleen worden gegenereerd voor bestanden die deel uitmaken van een uitvoervoorinstelling. Zie voor meer informatie [Publiceren op basis van artikelen vanuit de webeditor](web-editor-article-publishing.md#id218CK0U019I).

>[!NOTE]
>
> U kunt de eigenschappen van geselecteerde onderwerpen in een kaart ook openen en uitgeven DITA van het **Meer opties** onder aan de Kaartweergave.

**Omtrekweergave** -  ![](images/outline-icon.svg)

Wanneer u op het pictogram Omtrekweergave klikt, krijgt u de hiërarchische weergave van de elementen die in het document worden gebruikt.

![](images/outline-view_cs.png){width="300" align="left"}

De omtrekweergave biedt de volgende functies:

- Een boomstructuurweergave van alle elementen die in het document worden gebruikt.

- Als een element een id, kenmerk en tekst heeft, kunt u deze samen met het element zien.

- De Mening van het Overzicht van de toegang in zowel auteur als Bronmeningen.

- Gebruik de vervolgkeuzelijst met filters om alle elementen of alleen de verbroken verwijzingen weer te geven:

- Wanneer u op een element in de weergave Omtrek klikt, wordt de inhoud van het element geselecteerd in de weergave Auteur of Bron. De weergave Omtrek blijft synchroon met de weergave Auteur en Bron. Als u wijzigingen aanbrengt in een weergave, kunt u deze weergeven in de weergave Overzicht. Als u bijvoorbeeld een alinea toevoegt of een element bijwerkt in de weergave Auteur, wordt deze weergegeven in de weergave Overzicht.

  ![](images/select-element-content-outline-view_cs.png){width="650" align="left"}

- Elementen slepen en neerzetten. U kunt een element eenvoudig vervangen door er een ander element op neer te zetten. Als u een element over een ander element sleept en u een vierkant vakje rond het element ziet, wijst het erop dat het element zal worden vervangen. Het vervangt het element waarop het element wordt gelaten vallen.

  ![](images/replace-element-outline-view_cs.png){width="300" align="left"}

  Als u een element sleept en neerzet, geeft een onderbroken rechthoek aan dat het element op de huidige locatie kan worden geplaatst. Als het slepen en neerzetten ongeldig is, wordt een foutbericht weergegeven om aan te geven dat de bewerking niet is toegestaan.

  ![](images/drop-element-outline-view_cs.png){width="300" align="left"}

- De **Opties** in het menu *Omtrekweergave* Hiermee kunt u algemene bewerkingen uitvoeren, zoals Knippen, Kopiëren, Verwijderen, Id genereren, Element invoegen voor of na het huidige element, Naam van een element wijzigen of een element vervangen, Een element laten omlopen, een element opheffen en een fragment maken van het geselecteerde element.

>[!NOTE]
>
>Voor meer informatie over Generate ID, het element van het Tussenvoegsel vóór of na het huidige element, en Unwrap een element, zie [Andere functies in de webeditor](web-editor-other-features.md#).

**Weergaveopties voor het deelvenster Omtrekweergave**

Met het vervolgkeuzemenu Weergaveopties kunt u het volgende weergeven als het element deze opties heeft:

- **Id tonen**: geeft de id van het element weer.
- **Kenmerk tonen**: geeft het kenmerk samen met de waarde weer.
- **Tekst tonen**: Geeft de tekst weer. Als de tekst langer is dan 20 tekens, wordt een ovaal weergegeven.

Als een blokelement zijn eigen tekst heeft, wordt het getoond samen met dat blokelement. Als het geen eigen tekst heeft, wordt de tekst van het eerste onderliggende element samen met dat blokelement weergegeven.

![](images/outline-view-block-element.png){width="550" align="left"}

Als uw beheerder een profiel voor attributen heeft gecreeerd, dan zult u die attributen samen met hun gevormde waarden krijgen. U kunt ook weergavekenmerken toewijzen die door de beheerder onder de **Weergavekenmerken** in de editorinstellingen. De kenmerken die voor een element zijn gedefinieerd, worden weergegeven in de layoutweergave en in de contourweergave.


Zie voor meer informatie de *Weergavekenmerken* binnen de *Editor-instellingen* functiebeschrijving in het dialoogvenster [Linkerdeelvenster](web-editor-features.md#id2051EA0M0HS) sectie.

**Zoekfunctie**
Met de zoekfunctie kunt u naar een element zoeken op basis van de naam, id, tekst of kenmerkwaarde.

De zoekopdracht is niet hoofdlettergevoelig en komt exact overeen met de tekenreeks. De zoekresultaten worden gesorteerd op basis van de positie van het element in het document.

U kunt zoeken naar een tekenreeks in het element als deze wordt weergegeven in het deelvenster Omtrekweergave. Als de tekenreeks &quot;Adobe&quot; bijvoorbeeld voorkomt in de tekst van het element en wordt weergegeven in het deelvenster Omtrekweergave (zoals u hebt geselecteerd) **Tekst tonen** in het vervolgkeuzemenu Weergaveopties), wordt het element met deze opties gefilterd. Maar als de tekst niet wordt weergegeven in het deelvenster Omtrekweergave (aangezien u niet hebt geselecteerd **Tekst tonen** in het vervolgkeuzemenu Weergaveopties), wordt het element met deze opties niet gefilterd. Op dezelfde manier vindt u de tekenreeks in de id of kenmerken als u deze hebt geselecteerd.



**Herbruikbare inhoud** -  ![](images/content-reuse-icon.png)

Een van de belangrijkste functies van DITA is de mogelijkheid om inhoud opnieuw te gebruiken. In het deelvenster Herbruikbare inhoud kunt u uw DITA-bestanden opslaan vanwaar u doorgaans herbruikbare inhoud invoegt. Nadat de DITA-bestanden zijn toegevoegd, blijven deze in het deelvenster Herbruikbare inhoud van alle sessies staan. Dit betekent dat u uw DITA dossiers niet moet opnieuw toevoegen om tot hen later toegang te hebben.

U kunt herbruikbare inhoud eenvoudig van het deelvenster naar het huidige onderwerp slepen en deze inhoud snel en eenvoudig invoegen. U kunt ook een voorvertoning van de inhoud weergeven voordat u deze in het document invoegt.

Standaard kunt u de bestanden op titels weergeven. Terwijl u de cursor op een bestand plaatst, kunt u de bestandstitel en het bestandspad weergeven als knopinfo.
>[!NOTE]
>
> Als beheerder, kunt u ook verkiezen om de lijst van dossiers door filenames in de Redacteur van het Web te bekijken. Selecteer de **Bestandsnaam** van de **Bestanden weergeven op** sectie in **Gebruikersvoorkeuren** ![](images/user_preference_editor_icon.svg).

Als u een DITA-bestand wilt toevoegen aan het deelvenster Herbruikbare inhoud, gebruikt u een van de volgende methoden:

- Klik op het pictogram + naast Herbruikbare inhoud om het dialoogvenster Bladeren te openen. Selecteer het bestand dat u wilt toevoegen en klik op **Toevoegen** om het proces te voltooien.

  ![](images/reuse-content-add-dita-file_cs.png){width="650" align="left"}

- Klik in de weergave Opslag op het pictogram Opties van het gewenste bestand en kies **Toevoegen aan herbruikbare inhoud** in het contextmenu.

- Klik met de rechtermuisknop op het tabblad van een bestand in de editor om het contextmenu te openen en kies **Toevoegen aan herbruikbare inhoud**.


Wanneer het bestand is toegevoegd, ziet u alle herbruikbare inhoudselementen uit het bestand in het deelvenster Opnieuw te gebruiken inhoud. Herbruikbare inhoud wordt weergegeven met hun id&#39;s en elementnamen.

Wanneer u een bestand toevoegt aan de lijst Herbruikbare inhoud, wordt de bestandstitel weergegeven in plaats van de UUID van het bestand. Als u de UUID van het bestand wilt controleren, beweegt u de muisaanwijzer over de titel van het bestand en wordt de UUID van het bestand weergegeven in de knopinfo.

![](images/uuid-reusable-content-file-title_cs.png){width="300" align="left"}

>[!NOTE]
>
> U kunt meerdere bestanden toevoegen aan de lijst met herbruikbare inhoud. Vervolgens kunt u de gewenste inhoud vanuit het deelvenster Opnieuw te gebruiken inhoud in het document invoegen.

**Vernieuwen**: controleert opnieuw op alle herbruikbare inhoud en geeft een nieuwe lijst van herbruikbare inhoud weer.

Gebruik een van de volgende methoden om inhoud in te voegen uit het deelvenster Herbruikbare inhoud:

- Houd de muisaanwijzer boven een element dat u wilt invoegen, klik op het pictogram Opties en kies **Herbruikbare inhoud invoegen**.

  ![](images/insert-reusable-content_cs.png){width="400" align="left"}

  >[!NOTE]
  >
  > Selecteer een bestand en selecteer vervolgens **Voorvertoning** van de **Opties** om een voorvertoning van het bestand weer te geven zonder het te openen. U kunt ook een voorvertoning weergeven van de verwijzingen die in een onderwerp aanwezig zijn. De referentie-id wordt weergegeven in het venster.
  >
  > De **Voorvertoning** Deze optie is ook beschikbaar in het dialoogvenster **Opties** menu van een element, dat u een snel voorbeeld van het element geeft alvorens het op te nemen.

- Sleep het herbruikbare inhoudsitem van het deelvenster naar de gewenste locatie in het document.



**Verklarende woordenlijst** -  ![](images/glossary.svg)

Met AEM hulplijnen kunt u eenvoudig documenten van het type verklarende woordenlijst maken en gebruiken. U kunt woordenlijstonderwerpdossiers tot stand brengen en dan hen omvatten in een gemeenschappelijke verklarende woordenlijstkaart. Zodra deze kaart als uw wortelkaart wordt toegevoegd, worden de verklarende woordenlijstingangen dan getoond in het paneel van de Verklarende woordenlijst.

![](images/glossary-panel.png){width="650" align="left"}

Om een termijn van de verklarende woordenlijst op te nemen, eenvoudig sleep-en-dalings de ingang van het paneel aan de gewenste plaats in uw onderwerp. Met het menu Opties van een verklarende woordenlijstterm kunt u snel **Voorvertoning** van de inreistermijn, **Pad kopiëren** van het bestand met de invoertermijn of zoek het bestand met de invoertermijn in de opslagplaats.

Voer de volgende stappen uit om teksttermen te zoeken en deze te vervangen door verklarende woordenlijstafkortingen:

1. Open het DITA-onderwerp of de DITA-kaart waarin u de tekst of termen wilt zoeken en omzetten.
1. Selecteer het verklarende woordenlijstpaneel om de verklarende woordenlijsttermijnen in de wortelkaart te bekijken. U kunt deze termen slepen en neerzetten om ze aan het geopende onderwerp toe te voegen.
1. Selecteer de **Hotspot** gereedschap \( ![](images/hotspot-icon.svg)\) in het deelvenster Verklarende woordenlijst om specifieke teksttermen te zoeken en om te zetten in gekoppelde verklarende woordenlijstafkortingen. En omgekeerd kunt u deze ook gebruiken om te zoeken in afkortingen van woordenlijsten en deze om te zetten in teksttermen.

![](images/glossary-hotspot-tool.png){width="300" align="left"}

U kunt de volgende instellingen configureren voor het gereedschap Hotspot:

![](images/Glossary-search-keys.png){width="300" align="left"}

- **Verklarende sleutels**: Selecteer de verklarende woordenlijstsleutels van de kaart DITA u voor het onderzoek in het geselecteerde onderwerp wilt gebruiken. De geselecteerde toetsen worden hieronder weergegeven. U kunt een geselecteerde toets verwijderen door op de knop **Verwijderen** pictogram.

- **Onderwerpen**: Kies een van de **Huidig onderwerp** geopend in de webeditor, alle **Geopende onderwerpen** in de huidige kaart, of **Huidige kaart** worden bewerkt in de Kaarteditor om de termen te doorzoeken.
- **Onderwerpen filteren op status**: U kunt de zoekopdracht beperken tot onderwerpen die de status van het geselecteerde document hebben. De onderwerpen kunnen in Ontwerp zijn, uitgeven, In-Overzicht, Goedgekeurd, herzien, Klaar status, of in om het even welke staat zoals gevormd door de organisatie.
- **Handeling**: U kunt kiezen of u de woordenlijsttoetsen wilt doorzoeken **Handmatig voor elk onderwerp** of **Automatisch voor alle onderwerpen**. Als u **Handmatig voor elk onderwerp**, zet het u ertoe aan om te bevestigen alvorens elke termijn in elk onderwerp om te zetten. Als u **Automatisch voor alle onderwerpen**, zet het alle termijnen in alle onderwerpen automatisch om.
- **Omzetten**: U kunt een gezochte **Tekst naar verklarende woordenlijstterm** of **Verklarende term voor tekst.**
- **Opties**: U kunt een van de volgende opties selecteren:
   - **Hoofdlettergevoelig**: Zoekt naar een term om de overeenkomst te vinden die de zelfde omhulsel heeft. &#39;USB&#39; komt bijvoorbeeld niet overeen met &#39;usb&#39;.
   - **Alleen de eerste instantie omzetten**: Als een onderwerp meerdere instanties van de gezochte term bevat, wordt alleen de eerste instantie omgezet.
   - **Bestand uitchecken voor conversie**: Het gezochte bestand wordt uitgecheckt voordat de termen worden omgezet.
   - **Nieuwe versie maken na conversie**: Een nieuwe versie van het onderwerp wordt gecreeerd nadat de omzetting van termijnen is voltooid.
- **Volgende** wordt weergegeven als u **Handmatig voor elk onderwerp** -optie. Klikken **Volgende** om de termijnen voor elk onderwerp op basis van de geselecteerde montages om te zetten. Het veroorzaakt voor omzetting van termijnen in elk onderwerp en beweegt zich aan het volgende dossier. U kunt ervoor kiezen een term om te zetten of deze over te slaan en naar de volgende termijn te gaan.

  ![](images/manual-convert-skip.png){width="300" align="left"}

- **Omzetten** wordt weergegeven als u **Automatisch voor alle onderwerpen** -optie. Selecteren **Omzetten** om alle termen in het document te converteren naar gekoppelde woordenboekafkortingen.

Een lijst van de **Onderwerpen bijgewerkt** met de omgezette termen en **Onderwerpen met fout** wordt weergegeven. Houd de muisaanwijzer boven \( ![](images/info-icon.svg)\) pictogram dichtbij Onderwerpen met Fout om de details van de fout te zien.

![](images/glossary-converted-terms-error.png){width="300" align="left"}

>[!NOTE]
>
> Vernieuw het onderwerp om de omgezette termijnen te bekijken.

**Voorwaarden** -  ![](images/conditions-icon.svg)

In het deelvenster Voorwaarden worden de voorwaardelijke kenmerken weergegeven die door de beheerder zijn gedefinieerd in het algemene profiel of het mapprofiel. U kunt voorwaarden aan uw inhoud toevoegen door de gewenste voorwaarde gewoon naar uw inhoud te slepen. De voorwaardelijke inhoud wordt gemarkeerd met de kleur die voor de voorwaarde is gedefinieerd, zodat u deze gemakkelijk kunt herkennen.

U kunt ook meerdere voorwaarden op een element toepassen door meerdere voorwaarden op een element te slepen en neer te zetten. Wanneer u meerdere voorwaarden toepast op een element, worden in het deelvenster Eigenschappen de toegepaste voorwaarden weergegeven, gescheiden met een komma.

![](images/multiple-conditions-applied_cs.png){width="800" align="left"}

In de codeweergave worden de voorwaarden echter gescheiden met een scheidingsteken voor spaties. Wanneer u een voorwaarde toevoegt of bewerkt in de codeweergave, moet u ervoor zorgen dat meerdere voorwaarden worden gescheiden met een spatie.

>[!IMPORTANT]
>
> De volgende schermafbeelding is van een gebruiker met beheerdersrechten. Als gebruiker met beheerdersrechten kunt u voorwaarden toevoegen, bewerken en verwijderen. Anders krijgt u als normale auteur alleen de optie om voorwaarden toe te passen.

![](images/conditional-content-through-panel_cs.png){width="800" align="left"}

Als u een voorwaarde wilt toevoegen of definiëren, klikt u op het pictogram + naast het deelvenster Voorwaarden om het dialoogvenster Voorwaarde definiëren te openen:

![](images/conditional-panel-create-cond.png){width="400" align="left"}

Selecteer in de lijst Kenmerk het voorwaardelijke kenmerk dat u wilt definiëren, voer een waarde voor de voorwaarde in en geef vervolgens het label op dat in het deelvenster Voorwaarden wordt weergegeven. U kunt ook een kleur voor de voorwaarde definiëren. Deze kleur wordt ingesteld als de achtergrondkleur van de inhoud waarop de voorwaarde wordt toegepast

Kies **Bewerken** in het menu Opties. Het dialoogvenster Voorwaarde bewerken wordt geopend:

![](images/conditional-panel-edit-cond.png){width="400" align="left"}

Specificeer de details op de zelfde manier zoals gevormd terwijl het bepalen van een nieuwe voorwaarde.

**Onderwerpregeling** -  ![](images/subject_scheme_panel-icon.svg)

Onderwerpschemakaarten zijn een gespecialiseerde vorm van DITA-kaarten die worden gebruikt om taxonomische onderwerpen en gecontroleerde waarden te definiëren. Afhankelijk van uw vereisten kunt u een overzicht van de onderwerpenregeling maken en ernaar verwijzen in het hoofdmapbestand. Met AEM hulplijnen kunt u de geneste hiërarchie van de onderwerpdefinities in uw onderwerpschema definiëren.

U kunt het onderwerpschema eenvoudig maken en gebruiken in een overzicht van het onderwerpschema. Zodra deze kaart als uw wortelkaart wordt toegevoegd, wordt het onderwerpregeling dan getoond in het paneel van het Programma van het Onderwerp. In het paneel Onderwerpschema wordt het beschikbare onderwerpschema op een geneste of hiërarchische manier weergegeven.

AEM de Gidsen steunen ook genestelde vlakke onderwerpschemakaarten, en u kunt veelvoudige onderwerpregelingen hebben die onder de kaart van de wortelonderwerpregeling worden bepaald.

In het volgende voorbeeld ziet u hoe u het onderwerpschema in AEM hulplijnen kunt gebruiken.

1. Maak een onderwerpschemabestand in een gereedschap van uw keuze. De volgende XML-code maakt een onderwerpschema dat waarden bindt voor de `platform` kenmerk.

   ```XML
   <?xml version="1.0" encoding="UTF-8"?>
   <!DOCTYPE subjectScheme PUBLIC "-//OASIS//DTD DITA Subject Scheme Map//EN" "subjectScheme.dtd">
   <subjectScheme id="GUID-4f942f63-9a20-4355-999f-eab7c6273270">
       <title>rw</title>
       <!-- Define new OS values that are merged with those in the unixOS scheme -->
       <subjectdef keys="os">
           <subjectdef keys="linux">    </subjectdef>
           <subjectdef keys="mswin">    </subjectdef>
           <subjectdef keys="zos">    </subjectdef>
       </subjectdef>
       <!-- Define application values -->
       <subjectdef keys="app" navtitle="Applications">
           <subjectdef keys="apacheserv">    </subjectdef>
           <subjectdef keys="mysql">    </subjectdef>
       </subjectdef>
       <!-- Define an enumeration of the platform attribute, equal to       each value in the OS subject. This makes the following values       valid for the platform attribute: linux, mswin, zos -->
       <enumerationdef>
           <attributedef name="platform">    </attributedef>
           <subjectdef keyref="os">    </subjectdef>
       </enumerationdef>
       <!-- Define an enumeration of the otherprops attribute, equal to       each value in the application subjects.       This makes the following values valid for the otherprops attribute:       apacheserv, mysql -->
       <enumerationdef>
           <attributedef name="otherprops">    </attributedef>
           <subjectdef keyref="app">    </subjectdef>
       </enumerationdef>
   </subjectScheme>
   ```

   ![](images/subject-scheme-panel.png){width="300" align="left"}

1. Sla het bestand op met de extensie a.ditamap en upload het bestand naar een willekeurige map in DAM.

   >[!NOTE]
   >
   > U kunt een verwijzing naar het onderwerpschemabestand toevoegen in de bovenliggende DITA-kaart.

   ![](images/subject-scheme-root-map.png){width="550" align="left"}

1. De bovenliggende kaart instellen als de hoofdmap in het dialoogvenster **Gebruikersvoorkeuren**. Zodra deze kaart als uw wortelkaart wordt toegevoegd, wordt het onderwerpregeling dan getoond in het paneel van het Programma van het Onderwerp.

   ![](images/subject-scheme-user-preferences.png){width="400" align="left"}

1. In de Redacteur van het Web, open het dossier waar u de definities van de onderwerpregeling wilt gebruiken.
1. Pas het onderwerpschema toe op uw inhoud door het gewenste onderwerpschema gewoon naar uw inhoud te slepen. De inhoud wordt vervolgens gemarkeerd in de gedefinieerde kleur.

   ![](images/subject-scheme-apply.png){width="650" align="left"}

**De hiërarchische definities van onderwerpdefinities en opsommingen verwerken**

Naast het verwerken van de opsommingen en de onderwerpdefinities in dezelfde kaart, biedt AEM hulplijnen ook de functie om opsommingen en onderwerpdefinities in twee aparte kaarten te definiëren. U kunt één of meerdere onderwerpdefinities in een kaart en de opsommingsdefinities in een andere kaart bepalen en dan de kaartverwijzing toevoegen. Met de volgende XML-code worden bijvoorbeeld onderwerpdefinities en opsommingsdefinities in twee aparte mappen gemaakt.

De onderwerpdefinities worden gedefinieerd in `subject_scheme_map_1.ditamap`


```XML
  <?xml version="1.0" encoding="UTF-8"?> 
    <!DOCTYPE subjectScheme PUBLIC "-//OASIS//DTD DITA Subject Scheme Map//EN" "../dtd/libs/fmdita/dita_resources/DITA-1.3/dtd/subjectScheme/dtd/subjectScheme.dtd"> 
    <subjectScheme id="subject-scheme.ditamap_f0bfda58-377b-446f-bf49-e31bc87792b3"> 

    <title>subject_scheme_map_1</title> 
    
    <subjectdef keys="os" navtitle="Operating system">
        <subjectdef keys="linux" navtitle="Linux">
        <subjectdef keys="redhat" navtitle="RedHat Linux">
        </subjectdef>
        <subjectdef keys="suse" navtitle="SuSE Linux">
        </subjectdef>
        </subjectdef>
        <subjectdef keys="windows" navtitle="Windows">
        </subjectdef>
        <subjectdef keys="zos" navtitle="z/OS">
        </subjectdef>
        </subjectdef>
        <subjectdef keys="deliveryTargetValues">
        <subjectdef keys="print">
        </subjectdef>
        <subjectdef keys="online">
        </subjectdef>
    </subjectdef>
    <subjectdef keys="mobile" navtitle="Mobile">
        <subjectdef keys="android" navtitle="Android">
        </subjectdef>
        <subjectdef keys="ios" navtitle="iOS">
    </subjectdef>
    </subjectdef>
    <subjectdef keys="cloud" navtitle="Cloud">
        <subjectdef keys="aws" navtitle="Amazon Web Services">
        </subjectdef>
        <subjectdef keys="azure" navtitle="Microsoft Azure">
        </subjectdef>
        <subjectdef keys="gcp" navtitle="Google Cloud Platform">
        </subjectdef>
    </subjectdef>
    </subjectScheme>
```

De opsommingsdefinitie is aanwezig in subject_scheme_map_2.ditamap.

```XML
    ?xml version="1.0" encoding="UTF-8"?> 
        <!DOCTYPE subjectScheme PUBLIC "-//OASIS//DTD DITA Subject Scheme Map//EN" "../dtd/libs/fmdita/dita_resources/DITA-1.3/dtd/subjectScheme/dtd/subjectScheme.dtd"> 
        <subjectScheme id="subject-scheme.ditamap_17c433d9-0558-44d4-826e-3a3373a4c5ae"> 
        <title>subject_scheme_map_2</title> 
        <mapref format="ditamap" href="subject_scheme_map_1.ditamap" type="subjectScheme"> 
        </mapref> 
        <enumerationdef>
        <attributedef name="platform">
        </attributedef>
        <subjectdef keyref="mobile">
        </subjectdef>
        <subjectdef keyref="cloud">
        </subjectdef>
        </enumerationdef>
        </subjectScheme>
```

Hier worden onderwerpdefinities gedefinieerd in `subject_scheme_map_1.ditamap`  terwijl de opsomming def aanwezig is in `subject_scheme_map_2.ditamap`. De verwijzing naar `subject_scheme_map_1.ditamap` wordt ook toegevoegd in `subject_scheme_map_2.ditamap`.

>[!NOTE]
>
> Als de `subject_scheme_map_1.ditamap` en `subject_scheme_map_2.ditamap` er wordt met elkaar gerefereerd en daarom worden de betrokken regelingen opgelost .

De verwijzingen naar onderwerpopsommingen worden in de volgende volgorde van prioriteit opgelost:

1. Zelfde kaart
1. Toegewezen kaart


De verwijzingen worden niet opgelost als de opsomming niet in de zelfde kaart en de referenced kaart wordt gevonden.




**De waarden beperken tot een specifiek element**

U kunt de voorwaarden tot sommige elementen binnen een onderwerp ook beperken. Gebruik de `<elementdef>` -tag om het element en de `<attributedef>` -tag om de voorwaarde te definiëren die op het element kan worden toegepast.  Als u geen `<elementdef>` -tag, kunt u de voorwaarden toepassen op alle elementen.
Gebruik bijvoorbeeld de volgende opsomming om de `@platform` aan de `<shortdesc>` element.  De andere voorwaarden zijn zichtbaar voor alle elementen.

```XML
<enumerationdef>
    <elementdef name="shortdesc">
    </elementdef>
    <attributedef name="platform">
    </attributedef>
    <subjectdef keyref="deliveryTargetValues">
    </subjectdef>
    <subjectdef keyref="os">
    </subjectdef>
  </enumerationdef>
```

</details>


**Attributen** vervolgkeuzelijst

U kunt de waarde van het onderwerpschema ook wijzigen met de optie **Attributen** vervolgkeuzelijst **Eigenschappen van inhoud** in het deelvenster **Auteur** weergeven.
![](images/subject-scheme-attribute-dropdown.png){width="200" align="left"}
Voer de volgende stappen uit om de waarde te wijzigen:

1. Selecteer een kenmerk in het menu **Kenmerk** vervolgkeuzelijst.
1. Selecteren **Bewerken** ![bewerkingspictogram](images/edit_pencil_icon.svg).
1. Selecteer de gewenste waarde in het menu **Waarde** vervolgkeuzelijst.
1. Klikken **Bijwerken**.



U kunt ook waarden voor een kenmerk toepassen door meerdere waarden in het vervolgkeuzemenu te selecteren.

**Bronweergave**

U kunt de waarden van drop-down van de attributen in de Bronmening ook veranderen. De Bronweergave voorkomt ook dat u een onjuiste waarde toevoegt.

![](images/subject-scheme-code-error.png){width="550" align="left"}

**Het onderwerpschema weergeven en toepassen vanuit het deelvenster Voorwaarden**

U kunt het onderwerpschema ook weergeven en toepassen vanuit het deelvenster Voorwaarden.

Als u het onderwerpschema wilt weergeven in het deelvenster Voorwaarden, moet uw systeembeheerder de optie selecteren **Onderwerpregeling tonen in het deelvenster Voorwaarden** onder het tabblad Voorwaarde in Editor-instellingen. Zie voor meer informatie [Tabblad Voorwaarde](#id21BMNE0602V).

In het deelvenster Voorwaarden wordt de vlakke verticale structuur van de onderwerpdefinities in het onderwerpschema weergegeven.

![](images/subject-scheme-condtions-panel.png){width="300" align="left"}

U kunt voorwaarden aan uw inhoud toevoegen door de gewenste voorwaarde naar de inhoud te slepen. De voorwaardelijke inhoud wordt gemarkeerd met de kleur die voor de voorwaarde is gedefinieerd.

**Fragmenten** -  ![](images/insert-snippet-icon.svg)

Fragmenten zijn kleine inhoudsfragmenten die over verschillende onderwerpen in uw documentatieproject opnieuw kunnen worden gebruikt. In het paneel Fragmenten ziet u een verzameling inhoudsfragmenten die u hebt gemaakt. Als u een fragment wilt invoegen, sleept u het fragment van het deelvenster naar de gewenste locatie in het onderwerp. In het paneel Fragmenten kunt u een fragment toevoegen, bewerken, verwijderen, voorvertonen en invoegen.

>[!IMPORTANT]
>
> De volgende schermafbeelding is van een gebruiker met beheerdersrechten. Als gebruiker met beheerdersrechten kunt u fragmenten toevoegen, bewerken en verwijderen. Anders krijgt u als normale auteur alleen de opties om een fragment voor te vertonen en in te voegen.

![](images/snippets-panel_cs.png){width="400" align="left"}

Gebruik een van de volgende methoden om een fragment toe te voegen:

- Klik op het pictogram + naast Fragmenten om het dialoogvenster Nieuw fragment te openen.

  ![](images/snippet-new-dialog.png){width="550" align="left"}

  Geef in het dialoogvenster Nieuw fragment een titel op die wordt weergegeven in het paneel Fragmenten, een beschrijving en XML-code van de fragmentinhoud die u wilt maken. Klikken **Maken** om het fragment op te slaan en te maken.

- Klik in het inhoudsbewerkingsgebied met de rechtermuisknop op de broodkruimel van het element dat u als een fragment wilt gebruiken en kies **Fragment maken** in het contextmenu. Het dialoogvenster Nieuw fragment wordt weergegeven met de XML-code van het geselecteerde element dat is gevuld in het dialoogvenster **Inhoud** veld. Voer de **Titel** en **Beschrijving** voor het fragment en klik **Maken** het fragment opslaan.

- Klik in het inhoudsbewerkingsgebied met de rechtermuisknop ergens op de inhoud die u als fragment wilt gebruiken en kies **Fragment maken** in het contextmenu. Het dialoogvenster Nieuw fragment wordt weergegeven met de XML-code van het geselecteerde element dat is gevuld in het dialoogvenster **Inhoud** veld. Voer de **Titel** en **Beschrijving** voor het fragment en klik **Maken** het fragment opslaan.

  In de volgende schermafbeelding worden de breadcrumb en het inhoudsgebied gemarkeerd waaruit u het contextmenu kunt aanroepen.

  ![](images/snippet-create-from-breadcrumb-content.png){width="350" align="left"}


Gebruik een van de volgende methoden om een fragment in te voegen:

- Selecteer een fragment in het paneel Fragmenten en sleep het naar de gewenste locatie in het onderwerp.

- Plaats de invoegpositie op de plaats waar u het fragment wilt invoegen en kies Fragment invoegen in het menu Opties van het gewenste fragment.


>[!NOTE]
>
> Vanuit het contextmenu van een fragment-item kunt u ook een fragment bewerken, verwijderen, een voorbeeld ophalen of invoegen.

**Sjablonen** -  ![](images/templates-icon.svg)

Het deelvenster Sjablonen is alleen beschikbaar voor beheerders. Met dit deelvenster en de beheerder kunt u eenvoudig sjablonen maken en beheren die vervolgens door de auteurs kunnen worden gebruikt. De sjablonen worden standaard onder *Kaart* en *Onderwerp* typesjablonen.

![](images/templates-panel_cs.png){width="550" align="left"}

Standaard kunt u de bestanden op titels weergeven. Terwijl u de cursor op een sjabloon plaatst, kunt u de bestandstitel en de bestandsnaam als knopinfo weergeven.

>[!NOTE]
>
> Als beheerder, kunt u ook verkiezen om de lijst van dossiers in de Redacteur van het Web te bekijken. Selecteer de **Bestandsnaam** van de **Bestanden weergeven op** sectie in **Gebruikersvoorkeuren** ![](images/user_preference_editor_icon.svg).

Als u een sjabloon wilt maken, klikt u op het pictogram + naast Sjablonen en kiest u een sjabloon die u wilt maken. Als u **Onderwerpsjabloon** verschijnt het dialoogvenster Nieuw onderwerpsjabloon maken:

![](images/create-new-topic-template.PNG){width="400" align="left"}

Kies het type sjabloon dat u wilt maken in het menu **Sjabloon** vervolgkeuzelijst. Geef de **Titel**, die wordt weergegeven in het deelvenster Sjablonen. De **Naam** van de sjabloon wordt automatisch voorgesteld op basis van de titel, maar u kunt een andere bestandsnaam opgeven.

>[!NOTE]
>
> Als de beheerder automatische bestandsnamen heeft ingeschakeld op basis van de UUID-instelling, wordt het veld Naam niet weergegeven.

Nadat u de sjabloon hebt gemaakt, moet u deze toevoegen aan uw algemene profiel of mapprofiel. Nadat het malplaatje wordt toegevoegd, zullen uw auteurs beginnen het nieuwe malplaatje in het onderwerp/kaartcreatieproces te zien.

Met het menu Opties van een bestaande sjabloon kunt u ervoor kiezen **Bewerken** of **Dupliceren** het. In geval van duplicatie blijven de structuur en het type \(van document\) van de sjabloon behouden en kunt u deze opnieuw gebruiken om er een andere sjabloon van te maken.

**Controleren** -  ![](images/active-review-tasklist-icon.svg)

AEM Gidsen verstrekt de eigenschap om alle overzichtstaken in uw projecten te tonen. U kunt alle revisieprojecten en de actieve revisietaken in de revisieprojecten weergeven, waarvan u deel uitmaakt in het dialoogvenster **Controleren** deelvenster.  Vervolgens kunt u de revisietaken openen om de opmerkingen van de verschillende revisoren weer te geven.
De revisietaken worden weergegeven in het deelvenster. Standaard kunt u de bestanden op titels weergeven. Terwijl u de cursor op een bestand plaatst, kunt u de bestandstitel en het bestandspad weergeven als knopinfo.
>[!NOTE]
>
> Als beheerder, kunt u ook verkiezen om de lijst van dossiers door filenames in de Redacteur van het Web te bekijken. Selecteer de **Bestandsnaam** van de **Bestanden weergeven op** sectie in **Gebruikersvoorkeuren** ![](images/user_preference_editor_icon.svg).

Als auteur, kunt u de commentaren in een onderwerp richten gebruikend de Redacteur van het Web.


Voer de volgende stappen uit om de revisieopmerkingen weer te geven in de actieve revisietaken die aanwezig zijn in uw projecten:

1. Revisie selecteren ![](images/active-review-tasklist-icon.svg)   in het linkerdeelvenster. De **Controleren** wordt geopend.  Alle overzichtsprojecten en de actieve overzichtstaken binnen de overzichtsprojecten, die u deel van uitmaken worden getoond.

   ![](images/web-editor-review-panel.png){width="300" align="left"}
1. Selecteer een revisieproject en selecteer vervolgens een revisietaak in de lijst om deze te openen.
1. U kunt uw projecten ook op de volgende manieren filteren:

   - Voer de zoekterm of tekst in die u wilt zoeken in de titel van het project. Druk vervolgens op Enter om de zoekopdracht uit te voeren. U kunt bijvoorbeeld alle projecten doorzoeken met de term &#39;ruimte&#39; in de titel.

   - Selecteren ![](images/filter-search-icon.svg)  om de **Filter** in. U kunt alle of alleen specifieke projecten selecteren. De geselecteerde projecten worden vermeld in **Controleren** deelvenster.
     ![](images/active-review-select-project.png){width="300" align="left"}

     De **Taken die door mij zijn gestart** is standaard ingeschakeld. Het staat u toe om slechts de taken te bekijken die u hebt in werking gesteld.

1. Door gebrek, in uw overzichtsproject zult u een vlakke lijst van onderwerpen bekijken die commentaren verbonden aan hen hebben. Pas de vereiste filters van de linkerspoorstaaf toe om de onderwerpen te filtreren die op de overzichtscommentaren worden gebaseerd in hen:

   - **Alle onderwerpen weergeven**: Hier worden alle onderwerpen weergegeven die in de projecten voorkomen.
   - **Onderwerpen met opmerkingen weergeven**: Alleen de onderwerpen met revisieopmerkingen weergeven.
1. U kunt ook de zoekterm of tekst invoeren die u wilt zoeken in de titel of het bestandspad van het onderwerp. De onderwerpen die de termijn in de titel of de dossierweg bevatten zijn vermeld.
1. Dubbelklik op een onderwerp om het te openen in de weergave Ontwerpen. U kunt de opmerkingen weergeven in het dialoogvenster **Opmerkingen** deelvenster.
   ![](images/active-review-task-comments.png){width="800" align="left"}


   >[!NOTE]
   > 
   > De **Controleren** en de **Opmerkingen** zijn altijd synchroon. In het venster Opmerkingen worden de opmerkingen geladen op basis van de revisietaak die in het deelvenster Revisie is geladen.
   > Voor meer informatie over hoe u de opmerkingen kunt verwerken, bekijkt u [Opmerkingen voor revisie van adres](review-address-review-comments.md#).

**Zoeken en vervangen** -  ![](images/FindAndReplace_icon.svg)

Onder in het linkerdeelvenster vindt u het pictogram Zoeken en vervangen. Met het deelvenster Zoeken en vervangen kunt u zoeken naar tekst in bestanden in een kaart of een map in uw opslagplaats en deze vervangen. U kunt in alle onderwerpen van een kaart evenals onderwerpen vinden en vervangen aanwezig in submaps binnen de kaart.

![](images/map-find-replace.png){width="800" align="left"}

Standaard kunt u de bestanden op titels weergeven. Terwijl u de cursor op een bestand plaatst, kunt u de bestandstitel en het bestandspad weergeven als knopinfo.
>[!NOTE]
>
> Als beheerder, kunt u ook verkiezen om de lijst van filenames in de Redacteur van het Web te bekijken. Selecteer de **Bestandsnaam** van de **Bestanden weergeven op** sectie in **Gebruikersvoorkeuren** ![](images/user_preference_editor_icon.svg).

Voer de volgende stappen uit om de algemene zoek- en vervangactie uit te voeren:

1. De globale **Zoeken en vervangen** deelvenster.
1. Klik op de knop **Zoeken in** selecteert u een van de volgende opties om de zoekopdracht uit te voeren.
   - **Huidige kaart**: Naar de huidige geopende kaart zoeken

     >[!NOTE]
     >
     > Deze optie wordt weergegeven als u al een kaart hebt geopend voor bewerken.

   - **Pad**: Naar het geselecteerde pad zoeken
   - **Kaart selecteren**: Naar de geselecteerde kaart zoeken

1. U kunt op de knop **Opties** en kies een van de volgende opties:

   - **Bestand uitchecken voor vervangen**: Selecteer deze optie als u een bestand automatisch wilt uitchecken voordat u de zoekterm vervangt. Deze instelling is relevanter voor het geval dat de beheerder de configuratie heeft ingeschakeld om een bestand uit te checken voordat het wordt bewerkt. Selecteer deze optie als de instelling Achterkant is ingeschakeld. Zo voorkomt u dat u in het dialoogvenster voor het uitchecken van bestanden wordt gevraagd om elk bestand uit te checken voordat u wijzigingen aanbrengt. Als u deze optie niet selecteert, verschijnt er een vraag voordat een bestand wordt geopend voor bewerking.
   - **Alleen hele woorden**: Selecteer deze optie als u naar de volledige zoekreeks wilt zoeken. Als u bijvoorbeeld een zoekopdracht opgeeft in de zoekreeks, retourneert het zoekresultaat alle bestanden met woorden als over en overzicht. Selecteer deze optie als u de zoekopdracht wilt beperken en de exacte ingevoerde term wilt retourneren.
   - **Nieuwe versie maken na vervangen**: Selecteer deze optie als u een nieuwe versie wilt maken van het onderwerp waarin u de tekst wilt vervangen. U kunt ook versieopmerkingen opgeven die bij elk bijgewerkt bestand worden toegevoegd.

     Als u deze optie niet selecteert, dan worden de veranderingen bewaard in de huidige versie van het onderwerp en geen nieuwe versie wordt gecreeerd.

   - **Inclusief indirecte verwijzing**: Selecteer deze optie als u de tekenreeks ook in de DITA-kaart wilt doorzoeken in de indirecte verwijzingen. Deze optie is standaard uitgeschakeld, zodat de zoekopdracht alleen op de directe referenties wordt uitgevoerd.

1. Voer de zoekterm of tekst in die u wilt zoeken.
1. Voer de tekst in waarmee u de zoekterm wilt vervangen.
1. Druk op Enter of selecteer **Zoeken** pictogram \( ![](images/search-icon.svg)\) om de zoekopdracht uit te voeren.
1. Selecteer een bestand in de lijst met zoekresultaten. Het bestand wordt geopend in het bewerkingsgebied van de inhoud en de gezochte term wordt gemarkeerd in de inhoud.
1. De globale **Zoeken en vervangen** deelvenster.
1. Klik op de knop **Zoeken in** selecteert u een van de volgende opties om de zoekopdracht uit te voeren.

   - **Huidige kaart**: Naar de huidige geopende kaart zoeken

     >[!NOTE]
     >
     > Deze optie wordt weergegeven als u al een kaart hebt geopend voor bewerken.

   - **Pad**: Naar het geselecteerde pad zoeken
   - **Kaart selecteren**: Naar de geselecteerde kaart zoeken

1. U kunt op de knop **Opties** en kies een van de volgende opties:

   - **Bestand uitchecken voor vervangen**: Selecteer deze optie als u een bestand automatisch wilt uitchecken voordat u de zoekterm vervangt. Deze instelling is relevanter voor het geval dat de beheerder de configuratie heeft ingeschakeld om een bestand uit te checken voordat het wordt bewerkt. Selecteer deze optie als de instelling Achterkant is ingeschakeld. Zo voorkomt u dat u in het dialoogvenster voor het uitchecken van bestanden wordt gevraagd om elk bestand uit te checken voordat u wijzigingen aanbrengt. Als u deze optie niet selecteert, verschijnt er een vraag voordat een bestand wordt geopend voor bewerking.

   - **Alleen hele woorden**: Selecteer deze optie als u naar de volledige zoekreeks wilt zoeken. Als u bijvoorbeeld een zoekopdracht opgeeft in de zoekreeks, retourneert het zoekresultaat alle bestanden met woorden als over en overzicht. Selecteer deze optie als u de zoekopdracht wilt beperken en de exacte ingevoerde term wilt retourneren.

   - **Nieuwe versie maken na vervangen**: Selecteer deze optie als u een nieuwe versie wilt maken van het onderwerp waarin u de tekst wilt vervangen. U kunt ook versieopmerkingen opgeven die bij elk bijgewerkt bestand worden toegevoegd.

     Als u deze optie niet selecteert, dan worden de veranderingen bewaard in de huidige versie van het onderwerp en geen nieuwe versie wordt gecreeerd.

   - **Inclusief indirecte verwijzing**: Selecteer deze optie als u de tekenreeks ook in de DITA-kaart wilt doorzoeken in de indirecte verwijzingen. Deze optie is standaard uitgeschakeld, zodat de zoekopdracht alleen op de directe referenties wordt uitgevoerd.

1. Voer de zoekterm of tekst in die u wilt zoeken.

1. Voer de tekst in waarmee u de zoekterm wilt vervangen.

1. Druk op Enter of selecteer **Zoeken** pictogram \( ![](images/search-icon.svg)\) om de zoekopdracht uit te voeren.
1. Selecteer een bestand in de lijst met zoekresultaten. Het bestand wordt geopend in het bewerkingsgebied van de inhoud en de gezochte term wordt gemarkeerd in de inhoud.

1. Klikken **Eén exemplaar vervangen** \( ![](images/replace-icon.svg)\) om de momenteel gemarkeerde zoekterm in het onderwerp te vervangen of op Volgende overeenkomst te klikken ![](images/next-match-in-search.png) of ![](images/previous-match-in-search.png) Vorige overeenkomst om naar de volgende of vorige instantie van de tekst te gaan.

1. Klikken **Alles vervangen in bestand** \( ![](images/replace-all-in-file-icon.svg)\) om alle instanties van de gezochte term in één bestand te vervangen door de vervangterm in één klik. Er wordt een melding weergegeven nadat u alle instanties in het geselecteerde bestand hebt vervangen.

   >[!NOTE]
   >
   > Houd de muisaanwijzer boven een bestand in de lijst met zoekresultaten om alles in het bestandspictogram rechts ervan te zien Vervangen. U kunt ook het pictogram Bestand negeren gebruiken om het bestand uit het zoekresultaat te verwijderen. De bestanden die u negeert, worden uit de lijst verwijderd en de zoekterm wordt in de lijst niet vervangen.

1. Klikken **Alles vervangen** \( ![](images/replace-all-in-file-icon.svg)\) rechts boven aan de lijst om alle gevonden termen in alle bestanden te vervangen door de term &#39;vervangen&#39; met één klik.

   >[!NOTE]
   >
   > Om het **Alles vervangen** pictogram, moet uw systeembeheerder de optie selecteren **Alles vervangen inschakelen** onder de **Algemeen** tab in **Editor-instellingen**.


Slechts één vervang alle verrichting kan tegelijkertijd in het volledige systeem worden uitgevoerd, en tot de tijdverrichting wordt uitgevoerd zult u &quot;vervangt allen lopend&quot;status zien. U kunt ook de vervangingsbewerking afbreken of het lograpport bekijken. Als u de bewerking afbreekt, ontvangt u een melding over de bewerking in het Postvak IN. Er wordt een melding weergegeven als u alle exemplaren in het geselecteerde bestand hebt vervangen.

![](images/replace-all-in-progress.png){width="400" align="left"}

U kunt ook de opdracht **Zoeken op kaart** van de **Opties** menu van een kaart om tekst in een kaart te zoeken en te vervangen. Deze optie wordt weergegeven voor een kaart die is geopend in het paneel van de gegevensopslagruimte of in de kaartweergave.

![](images/map-options-menu.png){width="550" align="left"}

## Inhoudsbewerkingsgebied {#id2051EB000UI}

In het inhoudsbewerkingsgebied wordt de inhoud van het onderwerp of de kaart weergegeven. U kunt alle inhoud in dit gebied bewerken. Het geeft een WYSIWYG-weergave van de inhoud die u bewerkt. U kunt veelvoudige onderwerpen hebben die tezelfdertijd worden geopend, die in hun respectieve lusjes worden getoond.

Standaard kunt u de bestandstitels op de tabbladen weergeven. Terwijl u de cursor op een bestand plaatst, kunt u de bestandstitel en het bestandspad weergeven als knopinfo.
>[!NOTE]
>
> Als beheerder kunt u de lijst met bestanden ook weergeven op bestandsnamen op de tabbladen. Selecteer de **Bestandsnaam** van de **Bestanden weergeven op** sectie in **Gebruikersvoorkeuren** ![](images/user_preference_editor_icon.svg).

Onder het lusje van het dossier, hebt u de broodkruimel van het element bij huidige curseurplaats. In de rechterbovenhoek van het inhoudsbewerkingsgebied wordt het versienummer van het huidige onderwerp weergegeven.

![](images/content-editing-area.png){width="650" align="left"}

## Rechterdeelvenster {#id2051EB003YK}

Het rechterdeelvenster is een permanent deelvenster dat informatie bevat over het momenteel geselecteerde document.

>[!NOTE]
>
> U kunt het formaat van het rechterdeelvenster wijzigen. Als u de grootte van het deelvenster wilt wijzigen, plaatst u de cursor op de rand van het deelvenster, verandert de cursor in een dubbele pijl, klikt en sleept u om de breedte van het deelvenster aan te passen.

In het rechterdeelvenster hebt u toegang tot de volgende functies:

**Eigenschappen van inhoud** -  ![inhoudseigenschappen](images/content-properties-icon.svg)

U hebt toegang tot **Eigenschappen van inhoud** door de **Eigenschappen van inhoud** in het rechterdeelvenster. De **Eigenschappen van inhoud** bevat informatie over het type van het momenteel geselecteerde element in het document en de bijbehorende kenmerken.

**Type**: U kunt de tags in de volledige hiërarchie voor de huidige tag weergeven en selecteren in het vervolgkeuzemenu.

**Attributen**: De **Attributen** het vervolgkeuzevenster is beschikbaar in de weergaven Layout, Auteur en Bron. U kunt de kenmerken eenvoudig toevoegen, bewerken of verwijderen.

1. Klikken **+ Toevoegen**.

   ![kenmerken in eigenschappen van inhoud](images/properties-tab-attributes_cs.png){width="300" align="left"}

1. In de **Kenmerk** selecteert u het kenmerk in de vervolgkeuzelijst en geeft u de waarde van een kenmerk op.  Klik vervolgens op **Toevoegen**.

   ![kenmerkpaneel met meerdere kenmerken ](images/attributes-multiple-properties.png){width="300" align="left"}

1. Als u het kenmerk wilt bewerken, plaatst u de muis erboven en selecteert u **Bewerken** ![bewerkingspictogram](images/edit_pencil_icon.svg).
   ![kenmerken bewerken](images/edit-attributes-content-properties.png){width="300" align="left"}

1. Als u het kenmerk wilt verwijderen, plaatst u de muis erboven en selecteert u **Verwijderen** ![delete-icon](images/Delete_icon.svg).


>[!NOTE]
>
> Zelfs als uw onderwerp inhoud waarnaar wordt verwezen bevat, kunt u er kenmerken aan toevoegen via het deelvenster Eigenschappen.

Als uw beheerder een profiel voor attributen heeft gecreeerd, dan zult u die attributen samen met hun gevormde waarden krijgen. Gebruikend het paneel van inhoudseigenschappen, kunt u die attributen kiezen en hen toewijzen aan relevante inhoud in uw onderwerp. Op deze manier kunt u ook voorwaardelijke inhoud maken, die u vervolgens kunt gebruiken om voorwaardelijke uitvoer te maken. Zie voor meer informatie over het genereren van uitvoer met behulp van voorwaardelijke voorinstellingen [Voorinstellingen voor voorwaarden gebruiken](generate-output-use-condition-presets.md#).



**Bestandseigenschappen** -  ![](images/topic-properties-icon.svg)

De eigenschappen van het geselecteerde bestand weergeven door op Bestandseigenschappen te klikken ![](images/topic-properties-icon.svg) in het rechterdeelvenster. De functie Bestandseigenschappen is beschikbaar in alle vier de modi of weergaven: Indeling, Auteur, Bron en Voorvertoning.

De bestandseigenschappen hebben de volgende twee secties:

**Algemeen**

In het gedeelte Algemeen hebt u toegang tot de volgende functies:

![bestandseigenschappen](images/file-properties-general.png){width="300" align="left"}

- **Naam**: Hiermee geeft u de bestandsnaam van het geselecteerde onderwerp weer. De bestandsnaam is gekoppeld aan de eigenschappenpagina van het geselecteerde bestand.
- **ID**: Toont identiteitskaart van het geselecteerde onderwerp.
- **Tags**: Dit zijn de meta-gegevenstags van het onderwerp. Deze worden ingesteld vanuit het tagveld op de eigenschappenpagina. U kunt deze typen of selecteren in het vervolgkeuzemenu.  De tags worden weergegeven onder de vervolgkeuzelijst. Als u een tag wilt verwijderen, selecteert u het kruispictogram naast de tag.
- **Meer eigenschappen bewerken**: U kunt meer eigenschappen bewerken via de pagina met bestandseigenschappen.
- **Taal**: Toont de taal van het onderwerp. Deze wordt ingesteld vanuit het taalveld op de eigenschappenpagina.
- **Gemaakt op**: De datum en de tijd van vertoningen waarop het onderwerp werd gecreeerd.
- **Uitgecheckt door**: Toont de gebruiker die het onderwerp heeft uitgecheckt.
- **Documentstatus**: U kunt de documentstatus van het momenteel geopende onderwerp selecteren en bijwerken. Zie voor meer informatie [Documentstatus ](web-editor-document-states.md#)*.*

**Opmerking:** U kunt de kenmerkwaarden van de verschillende velden in de bestandseigenschappen naar het klembord kopiëren.

**Verwijzingen**

In het gedeelte Verwijzingen hebt u toegang tot de volgende functies:

![](images/file-properties-references.png){width="300" align="left"}

- **Gebruikt in**: In verwijzingen worden de documenten weergegeven waarnaar het huidige bestand wordt verwezen of gebruikt.
- **Uitgaande koppelingen:** De uitgaande Verbindingen maken een lijst van de documenten waarnaar in het huidige document wordt verwezen.

Standaard kunt u de bestanden op titels weergeven. Terwijl u de cursor op een bestand plaatst, kunt u de bestandstitel en het bestandspad weergeven als knopinfo.
>[!NOTE]
>
> Als beheerder, kunt u ook verkiezen om de lijst van dossiers door filenames in de Redacteur van het Web te bekijken. Selecteer de **Bestandsnaam** van de **Bestanden weergeven op** sectie in **Gebruikersvoorkeuren** ![](images/user_preference_editor_icon.svg).

**Opmerking:** Alle Gebruikte binnen en Uitgaande verwijzingen zijn hyperlinked aan de documenten. U kunt de gekoppelde documenten gemakkelijk openen en bewerken.

Naast het openen van bestanden kunt u ook een groot aantal handelingen uitvoeren met de opdracht **Opties** in de sectie Referenties. Enkele acties die u kunt uitvoeren zijn Bewerken, Voorvertoning, UUID kopiëren, Pad kopiëren, Toevoegen aan Favorieten, Eigenschappen en Kaart openen.

**Controleren** -  ![](images/review-icon.svg)

Als u op het pictogram Revisie klikt, wordt het revisievenster geopend waarin u een revisietaak kunt maken voor het document dat momenteel is geopend.

![](images/review-panel-before-opening.png){width="300" align="left"}

Als u meerdere revisieprojecten hebt gemaakt, kunt u een van de vervolgkeuzelijsten selecteren en de revisieopmerkingen openen.

Met het deelvenster Review kunt u reacties op de opmerkingen over het onderwerp weergeven en posten. U kunt de opmerkingen een voor een accepteren of afwijzen.

Zie voor meer informatie [Opmerkingen voor revisie van adres](review-address-review-comments.md#).

**Bijgehouden wijzigingen** -  ![](images/track-change-icon.svg)

Met de functie Bijgehouden wijzigingen in het rechterdeelvenster kunt u de informatie weergeven van alle updates die in een document zijn aangebracht. U kunt ook zoeken naar specifieke updates van het document.

>[!NOTE]
>
> De functie Bijgehouden wijzigingen toont alle updates die zijn bijgehouden met de functie Wijzigingen bijhouden inschakelen/uitschakelen op de hoofdwerkbalk. Zie voor meer informatie [Wijzigingen bijhouden inschakelen/uitschakelen](#id205DF0203Y4).

**Bovenliggend onderwerp:**[ Werken met de webeditor](web-editor.md)

