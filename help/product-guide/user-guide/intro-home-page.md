---
title: Ervaring met homepage van Adobe Experience Manager Guides
description: Meer weten over de startpagina van de Adobe Experience Manager Guides.
feature: Authoring
role: User
exl-id: 4e6e40ba-277b-43d5-a2a9-665f4586c7e3
source-git-commit: ac83f613d87547fc7f6a18070545e40ad4963616
workflow-type: tm+mt
source-wordcount: '1853'
ht-degree: 0%

---

# Ervaring met homepage van Experience Manager Guides

De startpagina is het eerste scherm dat u weergeeft wanneer u zich aanmeldt bij Experience Manager Guides. Het biedt u een verenigde en intuïtieve welkomstschermbeleving, die een snelle weergave omvat van de bestanden die u onlangs hebt geopend, verzamelingen en meer.

![](images/aem-home-page.png){align="left"}

De startpagina van Experience Manager Guides is onderverdeeld in de volgende secties:

- Kopbalk
- Navigatiebalk
- Deelvenster Links

## Kopbalk

De kopbalbar is de hoogste bar van de pagina van het Huis die het embleem van Adobe Experience Manager (of verenigde Shell toont als u Verenigde Shell als uw Experience Manager Guides UI gebruikt). Wanneer u het logo selecteert, wordt u naar de Experience Manager-navigatiepagina geleid.

![](images/aem-home-header.png){align="left"}

## Navigatiebalk

Met de gereedschappen voor navigatiebalkoppervlakken kunt u van navigatie wisselen, de overzichtslay-out aanpassen en de paginaweergave aanpassen. Het toont ook het huidige omslagprofiel in gebruik.

>[!NOTE]
>
> Als het gebruiken van Adobe Experience Manager Guides as a Cloud Service, wordt een extra eigenschap geëtiketteerd als **AI Medewerker** getoond in de navigatiebar.

![](images/aem-home-nav-bar.png){align="left"}

De functies in de navigatiebalk worden als volgt uitgelegd:

- **de schakelaars van de Navigatie**: Staat naadloze navigatie aan andere pagina&#39;s toe:
   - **Huis**: De standaardpagina die u wanneer het registreren in Experience Manager Guides bekijkt.
   - **Redacteur**: Een makkelijk te gebruiken web-based Redacteur die u toestaat om gestructureerde documenten in Experience Manager Guides tot stand te brengen en te beheren. [ krijgt om de interface van de Redacteur ](./web-editor.md) te kennen.
   - **console van de Kaart**: Verstrekt u een specifieke werkruimte om alle aspecten van kaartbeheer en het publiceren te behandelen. [ krijgt om de de consoleinterface van de Kaart te kennen ](./map-console-overview.md).
- **AI Medewerker**: Een krachtig, AI-gedreven hulpmiddel dat wordt ontworpen om uw productiviteit door slimme hulpeigenschappen te verbeteren. Als u werkt in de Editor-interface, kunt u bovendien gebruikmaken van de slimme ontwerpmogelijkheden van AI Assistant die het ontwerpproces slimmer en sneller maken door intelligente suggesties voor hergebruik en optimalisatie van inhoud.

  De [ AI Medewerker ](./ai-assistant.md) eigenschap is momenteel slechts beschikbaar voor Adobe Experience Manager als Cloud Service.
- **pas overzichtssectie** aan: Staat u toe om widgets in de sectie te verbergen of te tonen Widgets.
- **profiel van de Omslag in gebruik**: Toont het omslagprofiel dat momenteel wordt gebruikt.
- **breid mening** uit: Staat u toe om de paginamening uit te breiden gebruikend **breid** pictogram uit. In deze weergave is de kopbalk verborgen en wordt de ruimte van de inhoud gemaximaliseerd. Om aan de standaardmening terug te keren, gebruik **Uitgang het uitgebreide meningspictogram**.

## Deelvenster Links

In het linkerdeelvenster hebt u snel toegang tot de functies Overzicht, Kaarten, Bulk publiceren, Wachtrij publiceren en Gebruikersvoorkeuren. U kunt het paneel uitbreiden door **te selecteren breid** pictogram uit dat bij de bodem-linkerhoek van de interface wordt geplaatst. Zodra uitgevouwen, gebruik het **Samenvouwen** pictogram om het paneel samen te vouwen.

![](images/aem-home-left-panel.png){width="300" align="left"}

Wat u in dit deelvenster weergeeft, is afhankelijk van uw gebruikersrol. De volgende tabel bevat een lijst met de rollen en de respectieve secties die in het linkerdeelvenster worden weergegeven.

- **Admin &amp; Uitgever**: De capaciteit om alle secties in het paneel te bekijken.
- **Auteur**: De capaciteit om alle secties behalve het publiceren te bekijken. Auteurs hebben geen toegang tot de inzamelingen van de Kaart, publiceer rij, en Bulk publiceer sectie.
- **Recensent**: De capaciteit om de sectie van het Overzicht slechts te bekijken. Als u de sectie Overzicht selecteert, wordt een standaardbericht met een lege status of de widget Workfront-taken weergegeven, afhankelijk van of Adobe Workfront is geconfigureerd.


De functies in het linkerdeelvenster worden als volgt uitgelegd:

- [Overzicht](#overview)
- [ Verzamelingen van de Kaart ](#map-collections)
- [Bulk publiceren](#bulk-publish)
- [Wachtrij publiceren](#publish-queue)
- [ Voorkeur van de Gebruiker ](#user-preferences)

>[!NOTE]
>
> Bovendien als uw beheerder de integratie van Adobe Workfront in het systeem heeft gevormd, dan wordt de optie van a **Workfront** ook getoond in het linkerpaneel. Leer over [ integratie van Adobe Workfront ](./workfront-integration.md) in Experience Manager Guides.


### Overzicht

**Overzicht** handelt als een gepersonaliseerd dashboard dat wordt ontworpen om productiviteit te verbeteren. Het heeft verschillende widgets die u helpen georganiseerd en gefocust te blijven.

De widgets bieden u ook opties om kolommen te sorteren en te vergroten of te verkleinen. Als u deze opties wilt weergeven, selecteert u de kolomkop en geeft u de opties weer in een lijst.


De volgende widgets zijn aanwezig in de sectie Widgets:

- **Recente Dossiers**: widget voorziet u van een momentopname van onlangs geopende dossiers (een lijst van dossiers die u in de Redacteur) samen met de belangrijkste dossierdetails met inbegrip van Titel, de naam van het Dossier, het type van Dossier, de weg van het Dossier, en Toegelaten op data.

  ![](images/aem-home-recent-files.png){align="left"}

  U kunt de kolommen sorteren en het formaat ervan wijzigen door opties te selecteren in het vervolgkeuzemenu van de kolom. Standaard worden de gegevens gesorteerd op basis van de datum en tijd die het laatst zijn geopend.

  ![](images/aem-home-recent-files-sort-resize-options.png){align="left"}


  Van [ Voorkeur van de Gebruiker ](#user-preferences), kunt u het maximumaantal dossiers plaatsen die in deze widget kunnen worden getoond. Door gebrek, wordt deze grens geplaatst aan **20**.

  De volgende opties zijn beschikbaar wanneer u de muisaanwijzer op een bestand plaatst:

   - **Open in redacteur**: Staat u toe om het dossier in de Redacteur te openen. U kunt een bestand ook openen door het te selecteren.
   - **Vastzetten/unpin**: Staat u toe om één of meerdere dossiers aan Recente dossiers widget vast te zetten. Vastgezette bestanden worden bovenaan in de widgetlijst weergegeven. Om een dossier los te maken, gebruik **&#x200B;**&#x200B;optie vrijmaken.
   - **verwijder**: Staat u toe om het dossier uit Recente dossiers widget te verwijderen.

  **creeer nieuw dossier van het Nieuwe dossier dropdown menu**

  Het **Nieuwe dossier** dropdown menu staat u toe om een onderwerp of een kaart DITA recht van de **Recente dossiers** widget tot stand te brengen. Wanneer het bestand is gemaakt, wordt u omgeleid naar de Editor-interface waar u aan het bestand kunt werken.

- **Inzamelingen**: Als u aan een reeks dossiers of omslagen werkt, kunt u hen aan deze widget toevoegen om tot hen snel toegang te hebben. Nadat u de bestanden hebt toegevoegd, kunt u de bestanden op Titel weergeven, samen met andere belangrijke gegevens, zoals Eigenaar en Gemaakt op-datums. Terwijl u het vervolgkeuzemenu met kolommen selecteert, kunt u de opties voor het sorteren en vergroten of verkleinen van de kolom weergeven.


  ![](images/aem-home-collections.png){align="left"}

  De broodkruimels van de geselecteerde inzameling worden getoond bij de bovenkant van widget van de Inzameling. U kunt deze selecteren om terug te keren naar een specifieke map in de hiërarchie.

  ![](images/aem-home-collections-breadcrumbs.png){align="left"}

  De volgende opties zijn beschikbaar wanneer u de muisaanwijzer op een verzameling plaatst en het pictogram Meer ![](images/Smock_MoreSmallList_18_N.svg) selecteert:

   - **anders noemen**: Staat u toe om de inzameling anders te noemen.
   - **Schrapping**: Staat u toe om de inzameling te schrappen.
   - **Mening in Assets UI**: Staat u toe om de inzameling in Assets UI te openen.

  U kunt een verzameling openen door de titel van de verzameling te selecteren. De volgende opties zijn beschikbaar wanneer u de muisaanwijzer op een verzamelingsbestand plaatst en het pictogram Meer ![](images/Smock_MoreSmallList_18_N.svg) selecteert:

   - **Open in redacteur**: Staat u toe om het dossier in de Redacteur te openen. U kunt ook de bestandstitel selecteren om het bestand te openen.
   - **Open in kaartconsole**: Staat u toe om het kaartdossier in de kaartconsole te openen. (Alleen beschikbaar voor een DITA-kaartbestand).
   - **voeg aan inzamelingen** toe: Staat u toe om het dossier aan een nieuwe of bestaande inzameling toe te voegen.
   - **verwijder uit inzamelingen**: Staat u toe om het dossier uit de inzamelingslijst te verwijderen.
   - **Mening in Assets UI**: Staat u toe om van het dossier in Assets UI de plaats te bepalen.

  **creeer nieuwe inzameling van het Nieuwe inzamelingsdropdown menu**

  Het **Nieuwe inzameling** dropdown menu staat u toe om een nieuwe inzameling tot stand te brengen en het toe te voegen aan **Inzamelingen** widget.

>[!NOTE]
>
> Bovendien als uw beheerder de integratie van Adobe Workfront in het systeem heeft gevormd, dan **wordt Uw taken** widget ook getoond in de sectie Widgets. Leer meer over [ integratie van Adobe Workfront ](./workfront-integration.md#working-with-the-your-tasks-widget) in Experience Manager Guides.

### Kaartverzamelingen

Experience Manager Guides voorziet u van de capaciteit om uw inhoud voor het publiceren te organiseren door een dashboard te gebruiken genoemd **inzamelingen van de Kaart**. Om deze eigenschap te gebruiken, selecteer **inzamelingen van de Kaart** van het linkerpaneel. Het neemt u aan de pagina van de inzamelingen van de Kaart in **Assets UI** waar u kaartinzameling voor outputgeneratie kunt [ gebruiken.](./generate-output-use-map-collection-output-generation.md)

### Bulkpublicatie

Met de functie Bulk activeren kunt u uw inhoud snel en eenvoudig activeren, van ontwerpen tot publicatie-instantie. Om deze eigenschap te gebruiken, uitgezocht **Bulk publiceert** van het linkerpaneel. Het neemt u aan de Bulk pagina van de Inzamelingen van de Activering in Assets UI waar u [ Bulk activering van gepubliceerde inhoud ](./conf-bulk-activation.md) kunt tot stand brengen en beheren.

### Wachtrij publiceren

Wanneer u een grote reeks het publiceren taken hebt die op uw systeem lopen, wordt het praktisch onmogelijk om elke kaart afzonderlijk te controleren DITA om zijn het publiceren taak te controleren. Experience Manager Guides geeft de beheerders en uitgevers één enkele mening van alle het publiceren taken die in het systeem lopen.

Om deze eigenschap te gebruiken, uitgezocht **publiceer rij** van het linkerpaneel. Het neemt u aan de Publish dashboardpagina in Assets UI waar u kunt [ leiden publiceer taken gebruikend het publiceer dashboard ](./generate-output-publish-dashboard.md).

### Gebruikersvoorkeuren

De gebruikersvoorkeuren zijn beschikbaar voor alle auteurs. Met de voorkeuren kunt u de volgende instellingen configureren:

- **Algemeen**: Het Algemene lusje staat u toe om de volgende montages te vormen:

  ![](images/user_preference_editor.PNG){align="left"}

   - **het profiel van de Omslag**: Het profiel van de Omslag controleert diverse configuraties met betrekking tot voorwaardelijke attributen, auteursmalplaatjes, output stelt vooraf in en de configuraties van de Redacteur. Het profiel Algemeen wordt standaard weergegeven. Als uw beheerder mapprofielen heeft geconfigureerd in het systeem, worden deze mapprofielen ook weergegeven in de lijst Mapprofielen.
   - **de weg van de Basis**: Door gebrek, wanneer u tot de bewaarplaats van Experience Manager Guides van de Redacteur toegang hebt, wordt u getoond activa van de /content/dam plaats. De werkmap bevat hoogstwaarschijnlijk enkele mappen in de map /content/dam/. U kunt het basispad instellen op de werkmap en in de weergave Opslagplaats geeft u de inhoud van die locatie vooraf weer. Hierdoor neemt de tijd voor toegang tot uw werkmap af. Wanneer u een referentie- of mediabestand invoegt in uw onderwerp, begint de locatie van het bestand bovendien met de map die is ingesteld in het basispad.
      - **Uitgezochte Kaart van de Wortel**: Selecteer een DITA kaartdossier om zeer belangrijke verwijzingen of verklarende woordenlijstingangen op te lossen. De geselecteerde hoofdmap heeft de hoogste prioriteit om toetsverwijzingen op te lossen. Voor meer details, lost de mening [ zeer belangrijke verwijzingen ](./map-editor-other-features.md) op.
      - **Maximum aantal recente dossiers**: Gebruik dit gebied, om een maximumgrens op de dossiers te plaatsen die in Recente dossiers widget worden getoond.
      - **plaats standaard kaart het openen gedrag**: Hier, kunt u een standaardgedrag selecteren het systeem tijdens het openen van een DITA kaartdossier zal volgen.

- **Verschijning**: Het lusje van de Verschijning voorziet u van de opties om de thema&#39;s voor de toepassing en de bronmening van het inhoudsuitgevende gebied te selecteren. Op dit tabblad kunt u de volgende instellingen configureren:

  ![](images/user_preference_editor_appearance.png){align="left"}

   - **de vertoningsconfiguratie van de dossiers van de Redacteur**: Selecteer de standaardmanier om de dossiers in de Redacteur te bekijken. U kunt de bestandenlijst weergeven op titel of bestandsnaam in de verschillende deelvensters van de weergave Auteur. Standaard worden de bestanden op titel weergegeven in de Editor.
   - **het thema van de Toepassing en de mening van Source**: U kunt van de Lichte of Donkere thema&#39;s voor de toepassing en bronmening kiezen. In het geval van het thema Licht gebruiken de werkbalken en deelvensters een lichtgrijze achtergrond. In het geval van het thema Donker gebruiken de werkbalken en deelvensters een achtergrond met een zwarte kleur. Selecteer **thema van het apparaat van 0&rbrace; Gebruik &lbrace;om Experience Manager Guides toe te staan om de lichte en donkere thema&#39;s te selecteren die op het thema van uw apparaat worden gebaseerd.**

     In alle thema&#39;s wordt het bewerkingsgebied van de inhoud weergegeven in een witte-kleurenachtergrond in de weergave Auteur.

   - **bepaal altijd de plaats van dossiers in de bewaarplaats**: Selecteer deze optie om de plaats van een dossier in de bewaarplaats te tonen terwijl het uitgeven van het in de Redacteur.
   - **toon non-breaking ruimteindicator op de auteurswijze**: Selecteer deze optie om een indicator voor de vaste ruimten te tonen terwijl het uitgeven van het in de Redacteur. Deze optie is standaard ingeschakeld.
