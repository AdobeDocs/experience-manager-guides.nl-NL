---
title: Opmerkingen bij de release | Opgeloste problemen in Adobe Experience Manager Guides, release 5.1.0
description: Meer informatie over de opgeloste problemen vindt u in de 5.1.0-release van Adobe Experience Manager Guides.
source-git-commit: 6c29d5540f48c850416db279b4392b6042c8ca2c
workflow-type: tm+mt
source-wordcount: '1789'
ht-degree: 0%

---

# Opgeloste problemen in de 5.1.0-release (september 2025)

In dit artikel worden de bugs beschreven die zijn gecorrigeerd in verschillende gebieden van 5.1.0 release van Adobe Experience Manager Guides.


Voor meer informatie over de nieuwe eigenschappen en de verhogingen, mening [ wat in de 5.1.0 versie ](whats-new-5-1-0.md) nieuw is.

Leer over [ verbeteringsinstructies voor de 5.1.0 versie ](upgrade-instructions-5-1-0.md).


## Authoring

- **CSS** en **de lay-out van de Pagina** dossiers in de Inheemse malplaatjes van PDF tonen inconsequent gedrag van het dossiersluiten, toestaand geeft zelfs wanneer de dossiers worden gesloten uit. (GUIDEN-26688)
- Als u de pagina vernieuwt nadat u aangepaste knoppen aan het linkerdeelvenster hebt toegevoegd, worden dubbele tabbladen gemaakt. (GUIDEN-30899)
- Wanneer XML-inhoud met hoekhaken (zoals &lt;/ of />) wordt toegevoegd binnen een `code block` -element in een onderwerp, wordt het codeblokelelement leeg weergegeven in de uiteindelijke uitvoer. (GIDS-31007)
- De waarden van algemene variabelen `canCheckIn` en `canCheckOut` worden niet correct ingesteld wanneer een bestand wordt uitgecheckt en ingecheckt op de werkbalk van de Editor.(GUIDES-29890)
- Wanneer een DITA-kaart is geselecteerd in de Kaartweergave, wordt het aantal selecties in eerste instantie onjuist weergegeven omdat de onderliggende knooppunten van de kaart niet zijn geselecteerd. De juiste selectie en opname van alle onderliggende knooppunten wordt alleen weergegeven als u de selectie daarna wijzigt. (HULPLIJNEN-2563)
- De dossiers van de prijsverhoging worden niet teruggewonnen wanneer gezocht in het paneel van de Bewaarplaats gebruikend het **DITA onderwerp** filter. Ook, **vindt en vervangt** werkt niet voor de dossiers van de Prijsverhoging en verwante inhoud. (HULPLIJNEN-27133)
- Onbekwaam om het **drop-down van het Menu** van de toolbar van de Redacteur aan te passen gebruikend het uitbreidingskader. Het resultaat is dat u geen bestaande knoppen kunt weergeven of verbergen of nieuwe knoppen kunt toevoegen in het vervolgkeuzemenu Menu. (HULPLIJNEN-28748)
- Wanneer een XML-opmerking wordt toegevoegd binnen een element in de Source-weergave, gaan de spaties aan het begin en aan het einde van de opmerking verloren bij het schakelen tussen weergaven. (GUIDEN-29781)
- Multimedia de opties werken niet wanneer huidig binnen het ellipspictogram (**Meer** menu) in de toolbar. (GUIDEN-29583)
- Wanneer u een nieuw onderwerp maakt via de gebruikersinterface van Assets of de Editor, wordt het onderwerp niet automatisch geopend in de Editor als de instelling `xmleditor.uniquefilenames` is ingesteld op true in `XMLEditorConfig` . (HIDEN-28171)
- Spaties die in een MathML-vergelijking in de Source-weergave worden toegevoegd, blijven niet behouden wanneer de Editor-weergave wordt gewijzigd. (HULPLIJNEN-26111)
- Als u geen JCR-sessieverbindingen sluit tijdens het bijwerken of maken van onderwerpen, resulteert dit in geheugenlekken en downtime van de service. (GUIDEN-26282)
- Als u de kolommen sleept, verandert de breedte van een percentage in pixelwaarden. Dit leidt tot vervormde of onjuist uitgelijnde tabellen.(HIDEN-23128)
- Wanneer inhoud in een `code block` wordt geplakt of wanneer ruimten in `code block` worden toegevoegd en de weergave wordt geschakeld, gaat de afstand verloren. (GUIDEN-27478)
- Wanneer u een kaart toevoegt aan de `bookmap` , wordt deze opgeslagen in `fmditatopicrefs` in plaats van `fmditamaprefs` . (HIDEN-25480)
- Het **beeld van het Tussenvoegsel** dialoog ontbreekt om correct op een hoog-resolutie of gezoomde schermen terug te geven die de beeldtitel en afwisselende tekstgebieden veroorzaken om te verdwijnen. (GUIDEN-26459)
- Het vak voor speciale tekeninvoeging in de Editor kan niet worden geladen voor de landinstelling Duits. (GUIDEN-24537)
- Opmerkingen en labels die zijn toegevoegd tijdens het opslaan van een nieuwe versie van een DITAVAL-bestand, worden niet in de versiegeschiedenis opgeslagen met de nieuwe versie. (GUIDEN-24076)
- De uitgaande en inkomende verwijzingen onder **eigenschappen van het Dossier** in het juiste paneel verfrissen zich niet behoorlijk wanneer het schakelen tussen kaartdossiers. Dit probleem treedt specifiek op wanneer de kaartbestanden een groot aantal verwijzingen bevatten. (HIDEN-23344)
- Het filter Bewaarplaats behoudt niet de volgorde van aangepaste filters die zijn gedefinieerd in de `ui_config.json` . (HULPLIJNEN-2193)
- Als u meerdere tekstregels in een `codeblock` -element verwijdert, wordt een lege ruimte gemaakt die niet uit de weergave Auteur kan worden verwijderd. (GUIDEN-20672)
- Nieuwe ids ontbreekt om voor elementen te produceren wanneer dergelijke elementen via fragmenten worden toegevoegd of via malplaatjes worden gecreeerd, zelfs wanneer **auto produceert identiteitskaart** optie binnen `XMLEditorConfig` wordt toegelaten. (HIDEN-21734)
- Het creëren van een nieuw element DITA van malplaatjes DITA kopieert de replicatie eigenschappen van overeenkomstige malplaatjes DITA. (HIDEN-25145)
- Kan geen toegang krijgen tot bestandseigenschappen vanuit het paneel van de repository als de naam van de bovenliggende map het teken &#39;&amp;&#39; bevat. (GUIDEN-25762)
- Als u een onderwerpbestand sluit, kan dit als een nieuwe versie worden opgeslagen, zelfs als het onderwerp is vergrendeld. Deze kwestie komt specifiek voor wanneer **vraagt om nieuwe versie op dichte** optie binnen `XMLEditorConfig` wordt toegelaten. (GUIDEN-23875)
- De huidige maximumbreedte van het paneel van de bewaarplaats verbergt onderwerp en kaarttitels wanneer de inhoudshiërarchie diep wordt genesteld. (GUIDEN-27751)

## Beheer van bedrijfsmiddelen

- Het kopiëren van een map met een groot aantal elementen uit de gebruikersinterface van Assets leidt tot een API-time-out. De verrichting blijft in het achterste eind lopen en voltooit na wat tijd, maar geen succes of mislukkingsbericht, of bericht wordt getoond in UI. (GIDS-30900)
- Kopiëren en plakken in een map in de gebruikersinterface van Assets mislukt als gevolg van naverwerkingsfouten. (GUIDEN-30840)
- Kopiëren en plakken mislukt voor mappen met samengestelde elementen (elementen met subelementen) in de gebruikersinterface van Assets. (HULPLIJNEN-28107)
- Mappen met een groot aantal elementen worden niet correct geladen in de opslagplaats. (GIDS-32500)
- Namen van mapknooppunten worden onjuist weergegeven in plaats van maptitels in de Editor. (GUIDEN-32402)
- Er treedt een fout op bij het uploaden van elementen met niet-ondersteunde of verboden tekens in de bestandsnamen. (HIDEN-28845)
- Wanneer u een onderwerp opent in de weergave Auteur nadat de browser is vernieuwd, blijven eerder toegepaste tags in het deelvenster Bestandseigenschappen niet behouden en wanneer u nieuwe tags toevoegt, worden de bestaande tags overschreven, met name wanneer een groot aantal tags beschikbaar is voor selectie. (HIDEN-29078)
- Wanneer het produceren van een rapport van Meta-gegevens voor een kaart DITA die een groot aantal activa bevat, leidt **** knoop wordt unresponsief of toont een vertraagde reactie. (HULPLIJNEN-2843)
- De staat van het document van het werkende exemplaar van een onderwerp wordt getoond tegen alle versies van dat onderwerp in de Vertaling en Basislijn UI. (GUIDEN-20674)

## Controleren

- Pogingen om overzichtstaken tot stand te brengen door het werkschema van AEM ontbreken constant omdat de overzichtsknoop niet wordt gecreeerd. (HIDEN-28214)
- In de documentweergave in de revisie-interface wordt de inhoud voor bepaalde schermgrootten niet verpakt. Gebruikers moeten dan horizontaal schuiven om de volledige inhoud weer te geven. (GUIDEN-25292)
- Als u de details van een revisietaak bijwerkt op het dashboard Revisie, wordt niet bevestigd of de update is gelukt of niet. (GUIDEN-8051)

## Vertaling

- De vertalingen die door Experience Manager Guides worden voorgelegd omvatten niet de activa in bijlage, veroorzakend de **knoop van het Begin** voor vertaalbaan om niet aan gebruikers onbeschikbaar te worden. (HIDEN-28237)

## Publiceren

- In de native PDF-uitvoer wordt de lijst met indexen (LOI) weergegeven in een niet-alfabetische volgorde en worden geneste indextermen niet op de juiste wijze gegroepeerd, waardoor het moeilijk wordt om te navigeren in de index. (HIDEN-29090)
- Het **paginamalplaatje van de Kaart** en **de paginamalplaatje van het Onderwerp** dropdown lijst in de vooraf ingestelde pagina van de componentenafbeelding van AEM Sites verschijnt leeg wanneer de bestemmingspad een variabele met een dubbelepunt bevat. (HULPLIJNEN-2819)
- Wanneer een kaart DITA verschillende types van onderwerpverwijzingen zoals Concept, Verwijzing of Taak bevat, en het gebruikend het `chunk=to-content` attribuut wordt samengevoegd om enige paginaoutput op AEM Sites met componentenafbeelding te produceren, wordt de inhoud niet behoorlijk gepubliceerd toe te schrijven aan publicatiefouten. (HULPLIJNEN-2818)
- Als u een DITA-kaart met het kenmerk `chunk=to-content` publiceert, worden dubbele JCR-knooppunten in de nieuwe AEM Sites-uitvoer gemaakt, wat tot een redundante inhoudsstructuur in AEM Sites leidt. (HULPLIJNEN-28104)
- Wanneer het publiceren van een kaart DITA gebruikend de nieuwe output van AEM Sites, als een onderwerp het `chunk =to-content` attribuut heeft en de output wordt geplaatst om onderwerptitels als paginanamen te gebruiken, toont de geproduceerde paginanaam verkeerd het woord **brok** in plaats van het behouden van de originele onderwerpnaam. (HIDEN-28102)
- De eigenschap `cq:template` die is ingesteld in de AEM Guides-onderwerpsjabloon voor nieuwe publicaties in AEM Sites, geeft een onjuiste waarde weer, die de sjabloonstructuur en de rendering van inhoud beïnvloedt. (HULPLIJNEN-27789)
- Native PDF-publicatie gaat eindeloos door als de DITA-inhoud een webkoppeling heeft zonder bereik als `external` . (HIDEN-26434)
- Als er fouten in de inhoud optreden, worden native PDF&#39;s en AEM-sites in de wachtrij geplaatst. (HIDEN-26516)
- Wanneer u AEM-sitepagina&#39;s genereert met titels die meerdere woorden bevatten die door spaties worden gescheiden, worden afbreekstreepjes weergegeven in plaats van spaties. (HIDEN-27903)
- Voor Inheemse PDF, wordt een ongeldige naam van het meta-gegevensbezit niet opgelost en als `unresolved property name` getoond in **documenteigenschappen**. (HULPLIJNEN-25680)
- Tekst met meerdere regels in `codeblock` veroorzaakt problemen met tekstoverloop tijdens het genereren van PDF. (HIDEN-15541)
- Wanneer het toevoegen van kaarten aan de kaartinzameling, worden de activa buiten kaarten (zoals onderwerpen etc.) getoond, en de vertaalde kaarttalen worden ook niet behoorlijk gesorteerd.(HIDEN-25085)
- In de oudere AEM Sites-uitvoer worden sectiekoppelingen in geneste onderwerpen van een kaart niet correct omgezet wanneer deze handmatig worden ingesteld in de Source-modus of wanneer de inhoud wordt geïmporteerd uit een externe bron. In plaats van naar de bedoelde sectie te navigeren, leiden zij naar het belangrijkste onderwerp dat het genestelde onderwerp bevat. (HIDEN-26103)
- Als het kenmerk `scope=external` ontbreekt in externe koppelingen in een DITA-onderwerp, mislukt het publiceren in HTML5 zonder de bestanden aan te geven waar dit kenmerk ontbreekt in de foutlogboeken. (GUIDEN-25969)
- Onbekwaam om videoverbindingen in Inheemse PDF in te bedden zelfs wanneer **Multimedia Dossiers** optie wordt toegelaten in vooraf ingesteld PDF. (GUIDEN-9989)
- Kan de eigenschappen van metagegevens niet doorgeven om bestemmingspagina&#39;s die zijn gegenereerd met nieuwe AEM Sites-publicatie, toe te wijzen. (GUIDEN-27288)

## Basislijn

- Het kopiëren van een kaart DITA van Assets UI kopieert ook zijn in bijlage Basislijn aan de nieuwe kaart. (GUIDEN-11227)
- Wanneer u een nieuwe basislijn met een groot aantal labels maakt, worden niet alle labels opgehaald. (GUIDEN-16232)

## Homepage

- De homepage gaat leeg wanneer één van de dossiers die in **worden vermeld Recente dossiers** widget gebaseerd is op een malplaatje de waarvan bronmalplaatje geen duimnagel omvat. (GIDS-31506)

## Platform

- Prestatieproblemen zoals langere laadtijden en intermitterende onderbrekingen worden waargenomen wanneer u werkt met grote verzamelingen. (HIDEN-29065, HULPLIJNEN-28793)
- De kwetsbaarheden die samenhangen met het gebruik van de vervangen Guava-bibliotheek in de AEM Guides-componenten die zijn geüpload op Experience Manager Guides.(HIDEN-27402)

## Bekende problemen

Adobe heeft de volgende bekende problemen voor 5.1.0-release geïdentificeerd:


- De meest recente opmerking op taakniveau wordt weergegeven in het e-mailbericht aan de taakaanvrager als de controleur de taak voltooit zonder een opmerking toe te voegen. (HIDEN-33590)
- In het dialoogvenster Samenvoegen wordt in de vervolgkeuzelijst de hoofdinhoud onjuist weergegeven in plaats van de beschikbare versies van het geselecteerde onderwerp weer te geven. (GUIDEN-30820)
- Als u schakelt tussen voorinstellingen die dezelfde basislijn gebruiken, wordt de knop Opslaan voor de huidige voorinstelling gedeactiveerd. (HIDEN-28025)
- Er wordt automatisch een lege regel ingevoegd bij het plakken van nieuwe inhoud in een nieuwe regel in een codeblokkenelement.(GUIDEN-27842)
- Een onderwerp binnen een kaart DITA ontbreekt om in de output van AEM Sites te publiceren wanneer het als zowel keydef als topicref binnen zijn submaps wordt gebruikt. (HULPLIJNEN-2269)
- In het deelvenster Eigenschappen voor inhoud wordt het veld Kenmerken automatisch gesloten wanneer u een verwijzing probeert bij te werken vanuit het dialoogvenster Koppeling bijwerken, zodat de koppeling niet kan worden bijgewerkt. (GUIDEN-17767)