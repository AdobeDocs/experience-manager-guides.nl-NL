---
title: Opmerkingen bij de release | Opgeloste problemen in Adobe Experience Manager Guides 4.6.0-release
description: Meer informatie over de opgeloste problemen in de 4.6.0-release van Adobe Experience Manager Guides
role: Leader
source-git-commit: 5a30d427fa579e37a18b0fca65dea96dc486c594
workflow-type: tm+mt
source-wordcount: '1946'
ht-degree: 0%

---


# Opgeloste problemen in de 4.6.0-release (september 2024)


In dit artikel worden de bugs beschreven die zijn gecorrigeerd in verschillende gebieden met de release van 4.6.0 Adobe Experience Manager Guides.


Voor meer informatie over de nieuwe eigenschappen en de verhogingen, mening [ wat in de 4.6.0 versie ](whats-new-4-6.md) nieuw is.

Leer over [ verbeteringsinstructies voor de versie 4.6.0 ](../release-info/upgrade-instructions-4-6-0.md).

## Authoring

- De **Vondst** optie werkt niet in de **Source** mening. 18610
- **Controle uit** en **Controle binnen** pictogrammen verschijnen samen wanneer `autocheckout` in xmleditor wordt gevormd. (18088)
- De grote kaarten DITA laden langzaam en nemen tijd in omschakeling aan de **mening van de Lay-out**.  17590
- De fouten voor dubbele beeld IDs in de onderwerpen beperken de gebruiker om een onderwerp op te slaan of te ontwerpen. (17528)
- De kopiëren en deegverrichting van onderwerpen groter dan 15KB ontbreekt met een onverwachte fout. 17171
- De functionaliteit om de documentstaat van het **paneel van de Eigenschappen van het Dossier te veranderen** werkt niet correct en verandert in de *3} staat van het Ontwerp {.* (17088)
- Wanneer u de instellingen van de XML-editor wijzigt met behulp van een aangepast mapprofiel, wordt de `ui_config.json` bijgewerkt met een onjuist bestand. (17011)
- De herbruikbare inhoudspanelen maken geen lijst van elementen wanneer de **voorkeur van de Gebruiker** aan meningsdossiers door **Filename** wordt geplaatst. 16896
- De subelementen binnen het element van de lijsttitel kunnen niet op de **1} wijze van de Voorproef {van Experience Manager Guides teruggeven.** (16691)
- **Speciale karakters** die met vluchtkarakters worden geschreven worden verwijderd uit het onderwerp na het worden geupload aan Experience Manager Guides. 16495
- Vimeo-video&#39;s bieden geen ondersteuning voor schermvullende functies in Experience Manager Guides. (15996)
- Als u lange vooraf opgemaakte tekstreeksen in `<pre>` - of `<codeblock>` -elementen plakt, wordt de tekst afgebroken. 15859
- De schrapping van de inhoud komt toe te schrijven aan dubbele GUIDs wanneer de malplaatjes via code worden geïnstalleerd maar onverwerkt blijven. 15858
- Experience Manager Guides slaagt er niet in om aan het **attribuut van de Rol van de 0} Verwerking {in** 3} wijze van de Voorproef te houden. **** 15787
- De Editor verwijdert periodiek extra tekst buiten het geselecteerde gebied. 15708
- Kan grote tabellen niet kopiëren en plakken vanuit Word-documenten of HTML naar de webeditor. (15369)
- Geen API&#39;s of gebeurtenissen om kenmerktoevoeging aan een element of invoeging van een nieuw element vast te leggen. 15351
- Kan tag `<data>` niet toevoegen binnen tag `<ol>` in de webeditor. 15161
- De **placeholder van het Element** component veroorzaakt UI om te bevriezen. 14957
- De webeditor kan geen .pptx-bestanden uploaden. 14837
- Terwijl het vinden van een tekst in de Redacteur van het Web, keert de curseur aan het eerste voorkomen van de gezochte tekst terug, bij het drukken van de Enter sleutel. 14820
- AutoSave veroorzaakt veelvoudige kwesties, het verplaatst de curseur, en vereist handkliks in het document. 14253
- Het drukken van **gaat** sleutel in een lijstcel binnen de tekst binnen niet de paragraaf in zoals verwacht. 14251
- De grote dossiers laden niet in de Redacteur van het Web en veroorzaken browser om te bevriezen. (1327)
- De onderzoeksresultaten worden onbruikbaar gemaakt na het openen van een dossier dat door globale **wordt gevonden vindt en vervangt**. 12142
- In de bronweergave wordt `</conbody>` soms op onjuiste locaties ingevoegd. 11305
- Het pad van de component `/libs/fmdita/components/versions` is gecodeerd en de gebruikers kunnen het niet bedekken. 8779
- `<conref>` voor een onderwerp dat binnen een kaart van DITA van verwijzingen wordt voorzien wordt niet weerspiegeld in de voorproef binnen de redacteur. 17794
- De Experience Manager DITA Guide activeert de functie Opslaan niet nadat de functie voor automatisch inspringen is gebruikt. 16482
- De knopinfo-functie kan het Source-veld niet bijwerken in de XML-editor. 15847
- De **eigenschap van de Verbinding van UUID van het Aandeel** werkt niet voor de beelden in Adobe Experience Manager. (15598)
- In de **mening van de Auteur**, komt een exemplaar-en-deegkwestie voor wanneer het gebruiken van vaste ruimten en resulteert in het overstromen van tekst. 15541
- Overlappende tekstproblemen doen zich voor in `<reltable>` - en `<fig>` -tags. 15238
- De het flikkeren kwesties komen in het **paneel van Attributen** voor. 15237
- Als u in `<othermeta>` -element binnen `<topicmeta>` een `<conref>` aan een andere DITA-kaart toevoegt, wordt de kaart-id ook toegevoegd samen met de id van het element. (15226)
- De cursor springt tussen de blokelementen wanneer een teken of woord in de inhoud wordt verwijderd. (15224)
- Het foutbericht voor een bestand dat is uitgecheckt door &#39;&#39; wordt onjuist weergegeven wanneer bestanden worden bewerkt vanaf een ander tabblad, wanneer tokens zijn verlopen of wanneer de gebruiker is afgemeld. (1523)
- `<conref>` kan niet van het **paneel van Attributen** worden bijgewerkt wanneer het aanbrengen van veranderingen. (15209)
- De volledige cel wordt geselecteerd wanneer het selecteren van een beeld binnen een lijstcel. (15188)
- Het **paneel van Attributen** wordt niet getoond in de mening van Source van de Redacteur van het Web. 14387
- `<Topicref>` die is toegevoegd met `<keyref>` , wordt niet weergegeven in eigen PDF. (1974)
- Ongewenste, vaste spaties worden toegevoegd tijdens het bewerken aan het einde van een tag in de webeditor. (11786)
- Inhoud wordt verwijderd tijdens het corrigeren van spelfouten in DITA-bestanden. (11610)
- Als u een DITA-onderwerp of -kaart op een nieuw tabblad opent voor bewerken, wordt de selectienavigatie in de gebruikersinterface van Assets bevroren. 4992
- Als revisieknooppunten worden verwijderd, kan het bestand niet meer worden geopend en kunnen opmerkingen niet meer worden weergegeven in Adobe Experience Manager Guides. (15366)
- In de DITA-versie wordt de gebruikersnaam onjuist weergegeven in de gebruikersinterface van Assets. 17580
- Het element `<title>` wordt automatisch toegevoegd wanneer het element `<fig>` wordt ingevoegd als een fragment. 18562
- Problemen treden op wanneer een groot aantal bestanden met dichte gegevenssets naar Experience Manager Guides worden geüpload.17008
- De Redacteur van het Web geeft niet het correcte sleutelwoord door gebrek, vooral als het sleutelwoord verschillend in kindkaarten wordt bepaald. (14748)
- De **Staat van het Document** wordt niet getoond wanneer het uitgeven van de eigenschappen van meer dan 50 dossiers in bulk van de mening van de Kaart van de Redacteur van het Web. 14574
- Het gedrag van de knop Sluiten is inconsistent wanneer u de functie Automatisch opslaan gebruikt. (10996)
- Validatieproblemen treden op in MathML-elementen wanneer een nieuw element wordt ingevoegd of vergelijkingen worden gewijzigd. 10624
- De functie Wijzigingen bijhouden werkt niet met tekst die begint met Koreaanse tekens. 14538



## Publiceren

- Kruisverwijzing naar de sleutel wordt niet opgelost in de uitvoer van de Native PDF. 18087
- De {**fout 0} duplicate_value komt periodiek voor wanneer het opnieuw publiceren van een bestaand artikel in Salesforce.** 17932
- Validatie van Salesforce-verbinding mislukt met de bliksemschicht-URL. 17797
- Wanneer het selecteren van de **meta-gegevens van het Gebruik die in de topicmeta** optie worden toegevoegd, worden de meta-gegevenseigenschappen niet verspreid in de documenteigenschappen van de inheemse output van PDF.17283
- Het filtreren van de voorwaarde in de inheemse output van PDF werkt niet zoals verwacht in vergelijking met DITA-OT. (17095)
- Inhoudsopgave houdt geen rekening met de tags `<sub>` of `<sup>` in de uitvoer van de native PDF. 17028)
- Gekruist koppelen mislukt om alle bovenliggende maps weer te geven in de context-instellingen voor publicatie voor een koppeling met de `scope="peer"` . (16700)
- AEM genereren van sites en incrementele publicatie-API werkt niet zoals verwacht. (16666)
- AEM de productie van de output van de Plaats ontbreekt wanneer de **Schrapping Orphan optie van de Plaats** wordt toegelaten. 15896
- De oude attributen worden behouden in de **Vooraf ingestelde Voorwaarde** wanneer het toevoegen van of het verwijderen van om het even welke nieuwe of bestaande attributen. 15890
- In de JSON-uitvoer worden metagegevens van de DITA-kaart of -onderwerpen niet doorgegeven aan de JSON-uitvoerbestanden. 15713
- De RTL-taalinhoud wordt niet correct verwerkt in de publicatie-uitvoer van Native PDF. 15709
- Publiceren van eigen PDF mislukt wanneer de naam van de voorinstelling wordt gewijzigd. (15662)
- Het **sourcePath** bezit is onjuist op de gepubliceerde AEM plaatsuitvoer. 15502
- De selectie en aanpassing van taalvariabelen werkt niet goed in de voorinstelling Eigen PDF-uitvoer. (15399)
- Native PDF genereren mislukt bij gebruik van een grote stijlpagina of lay-outsjabloon. (15344)
- Inhoud wordt niet correct weergegeven in de gepubliceerde uitvoer als `<conref>` wordt gebruikt met een absoluut pad. (15222)
- Een verkorting van de URL van AEM Sites werkt niet vanwege conflicten tussen `fmdita rewriter` en `ResourceResolver` . 14793
- De inheemse generatie van PDF ontbreekt met een fout met betrekking tot het krijgen van gebiedsdelen voor Node.js. (1445)
- De **verwerking-rol=&quot;middel-slechts&quot;**, **search= &quot;geen&quot;**, en **chunk= &quot;aan-inhoud&quot;** attributen verschijnen ongelijk in de output van AEM Sites. (1442)
- `<Conref>` wordt niet opgelost in de `Preview` -modus van de webeditor en de uitvoer van de native PDF. 17827
- In Eigen PDF, worden de genestelde onderwerpen DITA verkeerd getoond in de Inhoudslijst (TOC). 16742
- De duimnagels die van **Dynamic Media** voor videodossiers worden geproduceerd blijven niet in de gepubliceerde output bestaan. 15656
- De referenced PDF wordt niet geactiveerd van het **BulkPublish Dashboard** tijdens de Bulk Activering van gepubliceerde inhoud. 17793
- Als een map met 2k-maps wordt ingesteld in het mappad binnen een mapprofiel, mislukken de wijzigingen die op de uitvoervoorinstelling zijn toegepast. 14852
- De regeneratie van onderwerpen mislukt als gevolg van de fout in de OOTB-API voor regenereren van onderwerp of incrementele publicatie. 18452
- Met de voorinstelling voor voorwaarden worden bijgewerkte kenmerken niet opgehaald nadat u de upgrade voor Experience Manager Guides hebt uitgevoerd. 18174
- Inhoudsverwijzingen worden niet correct omgezet voor uitvoer van native PDF als het bestand met sleuteldefinities zich niet in dezelfde map bevindt als de DITA-kaart. 15062


## Beheer


- Het InDesign aan omzetting DITA heeft een hard-gecodeerd configuratiepad zodat worden de douane config dossiers niet plukt. 16891
- De niet gesloten **Resolvers van het Middel** veroorzaken stijgende zittingstelling en `PathNotFoundException` fouten post de 4.3.1 versie van Experience Manager Guides. 15604
- Fout bij het installeren van hulplijnpakketten in grote opslagruimten. 15160
- Het maken van een basislijn met de Java API werkt niet met Experience Manager Guides. 14787
- De API van `/bin/fmdita/import` blijft permanent vastzitten in een aanvraag die in behandeling is wanneer de uploadmiddelen meer dan 500 MB bedragen. 14743
- Als u een bestaande basislijn bewerkt en een specifieke versie selecteert, treden toepassingsfouten op. (14451)
- De uitvoering van postprocess manuscript ontbreekt toe te schrijven aan **FileNotFoundException** uitzondering. 16517
- Dynamische titels met `<conkeyref>` worden niet weergegeven in de onderwerpenlijst van het Rapport. (16967)
- De onnauwkeurige **tellingen van de Lijst van het Onderwerp** {komen in de Rapporten UI van Experience Manager Guides toe te schrijven aan de niet gestaafde eigenschappen wanneer het kopiëren van activa DITA. (15529)
- Onderwerpen met externe verwijzingen met %20 in de URL geven verbroken bestandsverwijzingen weer. 15347
- De eigenschappen fmditaMaprefs en fmditakeydefrefs tonen relatieve wegen, ondanks het plaatsen van absolute wegen voor de kaart DITA en onderwerpen. 18353
- Het pad voor de overlay-functionaliteit is hard-gecodeerd voor het Koreaanse taalbestand en is niet correct geselecteerd. (17089)
- De standaardtijd in de verwezenlijking van de Basislijn in de Redacteur van het Web wordt getoond als 00:00 in plaats van de huidige tijd. 15215

## Controleren

- Het ophalen van de gebruikerslijst tijdens het maken van een revisietaak mislukt als het aantal gebruikers groter is dan 25. 17329
- Revisieonderwerpen worden niet in de juiste volgorde weergegeven. (16319)
- In de webeditor wordt het deelvenster Revisie langzaam geladen. 14680
- Revisoren kunnen geen spaties toevoegen, markeren of doorhalen wanneer ze een documentrevisie uitvoeren in Experience Manager Guides. 14752
- Wanneer een gebruiker een revisietaak bijwerkt, ontvangen niet alle toegewezen revisoren een melding over de update. 9496

## Vertaling

- De verwijzingen naar vertaalde elementen worden niet bijgewerkt. 18086
- Kan geen XLIFF-projecten maken met menselijke vertaling. (16964)
- De titel met `<conref>` of `<conkeyref>` wordt niet omgezet in de dashboards Basislijn en Vertaling van de Web Editor. (16961, 16879)
- Met de 4.3.1-release van Experience Manager Guides kunnen vertaalprojecten geen nieuwe taaltaken toevoegen aan Adobe Experience Manager 6.5 SP18. 15398
- **keur Vertaling** niet goed om de vertaling van tijdelijke dossiers te voltooien. (14665)
- Het toevoegen van een bijgewerkt onderwerp in een actief vertaalproject resulteert in een dubbel onderwerp en het proces ontbreekt. (7688)
- Referenties worden niet correct gefilterd als Direct of Indirect wanneer ze in meerdere talen worden vertaald. 17891
- Op XLIFF gebaseerde omzetting mislukt vanwege een fout voor gebruikers die geen beheerder zijn.(17296)
- De titel van vertaalde bestanden wordt na de tweede vertaling teruggezet naar het Engels, ook al is de inhoud vertaald. (15200)
- Wanneer het selecteren van een vertaalproject met de **Status van de Vertaling** zoals **lopend**, opent een onjuiste pagina. (13248)
- De vertaalprojecten die door **worden gecreeerd te selecteren creëren structuur slechts** optie hebben geen toegewezen UUIDs. 18980


## Bekende problemen

Adobe heeft de volgende bekende problemen voor de release van 4.6.0 vastgesteld:
- Het openen van **AEM Sites** (niet erfenis) vooraf ingesteld merkt het onderwerp als vuil.
- Het geselecteerde paneel wordt niet behouden op browser verfrist zich van de **Output** tabel.
- Onbekwaam om onderwerpen tussen twee `topicrefs` in de **Auteur** mening te slepen en te laten vallen.
- Het filtreren van de voorwaarde die in vooraf ingesteld wordt toegepast wordt niet toegepast via **Download als PDF**.
- Enige onderwerpgeneratie van het kaartpaneel produceert alle onderwerpen die in **worden geselecteerd AEM Sites** (niet erfenis) vooraf ingesteld.
- De verwijzing van het onderwerp lijkt gebroken in het gebruikersinterface wanneer opgenomen van de hoogste toolbar van de kaart DITA.
- Native PDF genereren mislukt voor een DITA-kaart als er ontbrekende verwijzingen zijn.
- Zodra de het documentstaat van een onderwerp wordt bijgewerkt aan **Gedaan**, het **Begin een Nieuw pictogram van de Versie** is slechts beschikbaar op de **Voorproef** wijze van het onderwerp.



