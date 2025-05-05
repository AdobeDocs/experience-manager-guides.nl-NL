---
title: Opmerkingen bij de release | Opgeloste problemen in Adobe Experience Manager Guides 4.4.0-release
description: Meer informatie over de opgeloste problemen in de 4.4.0-release van Adobe Experience Manager Guides
role: Leader
exl-id: ff3083d3-062b-4a79-875f-86991978a18e
source-git-commit: e40ebf4122decc431d0abb2cdf1794ea704e5496
workflow-type: tm+mt
source-wordcount: '1434'
ht-degree: 0%

---

# Opgeloste problemen in de 4.4.0-release (januari 2024)


In dit artikel worden de bugs beschreven die zijn gecorrigeerd in verschillende gebieden van de release 4.4.0 van Adobe Experience Manager Guides.

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, mening [ wat in de 4.4.0 versie ](./whats-new-4-4.md) nieuw is.

Leer over [ verbeteringsinstructies voor de versie 4.4.0 ](../release-info/upgrade-instructions-4-4.md).


## Authoring

- Spellingcontrole in de Editor staat niet toe dat suggesties worden geselecteerd. 15045
- De algemene navigatieknop werkt niet en het dashboard kan niet worden geladen. 14968
- In de Redacteur van het Web, ontbreekt de eigenschap van de downloadkaart om een pop-up bericht teweeg te brengen wanneer het klaar is om te downloaden. 14626
- In de Redacteur van het Web, ontbreekt de eigenschap van de downloadkaart om een kaart met basislijn te downloaden. (14622)
- Ongeldige DTD-fout in de Experience Manager Guides. (14482)
- De titel op het tabblad Webeditor wordt afgekapt na een punt (.) teken. 14372
- Foutberichten voor dubbele kaartnamen in de gebruikersinterface van Assets worden niet bijgewerkt. 14320
- Er treedt een fout op in de logica voor het maken van versies tijdens het slepen en neerzetten van elementen. 14291
- Herbruikbare inhoud slaat de element-id&#39;s over. 14213
- De plaatsende controle om **paneel van de Variabelen van de Taal te verbergen** onder **lusje van de Output &lbrace;ontbreekt.** (14194)
- De Redacteur van het Web werpt toepassingsfouten wanneer het toevoegen van een nieuwe verwijzing of een onderwerp gebruikend een gespecialiseerd schema in de **mening van de Lay-out**. (14094)
- De ruimte na het conref `<ph>` -element verdwijnt bij het opslaan van het onderwerp. 13642
- Er treedt een toepassingsfout op wanneer wordt geprobeerd DITA-bestanden op te slaan voordat de naverwerking is voltooid. 13571
- Een ankerkoppeling naar `<dlentry>` of `<dt>` -element geeft de koppelingstekst niet weer. 13543
- De **inzameling van Favorieten** in de Redacteur van het Web slaagt er niet in om te laden. 13495
- Als de titel van een onderwerp een schuine streep `/` bevat, toont het lusje in de Redacteur van het Web slechts de brieven die na het komen. (13455)
- De voorvertoning van de afbeelding verdwijnt niet nadat de voorvertoning in de webeditor is weergegeven. 13454
- Bij het maken van een unieke id met spaties worden niet-klikbare koppelingen weergegeven. (13447)
- Wanneer u een onderwerp sluit nadat u het hebt bewerkt, wordt u omgeleid naar de AEM startpagina in plaats van terug te keren naar de mappenweergave. (13306)
- Het sleutelwoord van het Tussenvoegsel pop-up verschijnt niet wanneer het gebruiken van wortel kaart-bepaalde sleutels in andere onderwerpen. 12950
- De dichte pictogrammen zijn niet zichtbaar wanneer zeer hoge grafiek in het **paneel van de Geschiedenis van de Versie** wordt voorvertoond. 12867
- Onbekwaam om timezone van **Versie te wijzigen die op** wordt gecreeerd kolom voor Baselines. (1271)
- Zip-bestanden worden niet herkend in de webeditor en u kunt ze niet slepen en neerzetten. 12709
- Het **paneel van de Geschiedenis van de Versie** in Assets UI toont een onjuiste timestamp voor het **Huidige** gebied. 12624
- In de **mening van de Lay-out** voor een Bookmap, gebruikend **Beweging Juist** om een geselecteerd hoofdstuk te maken werkt een sub-element niet. 12567
- Als u een DITA-bestand maakt op basis van een sjabloon met een bestandsnaam die begint met numerieke tekens, treedt er een naamruimtefout op. (12188)
- Het rootmap plaatsen blijft in de Redacteur van het Web bestaan zelfs als de gebruiker het niet uitdrukkelijk van de **Voorkeur van de Gebruiker** heeft geplaatst. (11551)
- De inhoud met sommige toegepaste attributen wordt niet benadrukt in **Auteur** of **3&rbrace; wijze van de Voorproef &lbrace;.** (1063)
- In de Redacteur van het Web, opent het **Zeer belangrijke venster van Verwijzingen** wanneer het opnemen van de `varname` markering. 10940
- Door een woordenlijstonderwerp van de repository naar een glossary map te slepen, maakt u `topicref` . 10767
- Het voorvertoningsvenster van de XML-editor wordt afgebroken in Google Chrome- en Microsoft Edge-browsers. 10755
- In de webeditor is het niet mogelijk een element binnen de mogelijke bovenliggende elementen te plaatsen. 8791
- De webeditor wordt verwijderd nadat Adobe Experience Manager Guides versie 4.3.1 opnieuw is geïnstalleerd. 14519
- Het installatieprogramma van versie 4.3.1 vindt een filterconflict, wat resulteert in het overschrijven van `apps/cq/core/content/projects/properties`. 14517
- Een zelfverwijzingsverbinding verschijnt onder de lijst van **Gebroken Verbindingen** in Rapporten. 13539
- Het voorvertoningsscherm voor fragmenten is bevroren. 14840
- Verbroken tekens worden weergegeven tijdens het maken van de fragmenten in de Koreaanse taal. 13489

## Publiceren

- Publiceren in AEM Sites mislukt en veroorzaakt bereikfouten voor bestanden die `xref` naar het DITA-bestand hebben dat begint met &quot;HTTP&quot;. 15154
- In de publicatie Native PDF kunnen de metagegevenseigenschappen van de DITA-kaart niet worden gebruikt om de metagegevens voor uitvoer van PDF-bestanden te vullen. 15159
- In publicaties met native PDF werken aangepaste kenmerken binnen voorinstellingen voor voorwaarde niet voor publicatie met eigen PDF. 14943
- Onbekwaam om een douanemalplaatje van het **lusje van Output** in de Redacteur toe te voegen. 14846
- **AEM de vooraf ingestelde Plaats** werkt niet toe te schrijven aan een leeg malplaatjeweg. 14804
- AEM de regeneratie van de Plaats ontbreekt voor kaarten DITA met onderwerpen die vergelijkingen MathML bevatten. 14790
- Bij publicatie van Native PDF genereren PDF fouten bij het ophalen van afhankelijkheden voor publicatie van `Node.js` . (1445)
- **AEM de vooraf ingestelde Plaats** staat niet de selectie van een malplaatje buiten de `/content` hiërarchie in de Redacteur van het Web toe. (14260)
- De functionaliteit om als inhoudsfragment te publiceren werkt niet voor dossiers die in onderzoeksresultaten worden vermeld. (14090)
- Fmdita-componenten hebben een hardcoderingspad van `delegator.jsp`, waardoor de bedekking van AEM Sites-componenten wordt voorkomen. (13993)
- De getagde weergave van de PDF-reactor in Native PDF-publicatie-uitvoer werkt niet zoals u had verwacht. (13622)
- In het Inheemse publiceren van PDF, vereist de selectie van de achtergrondkleur op de **lay-out van het Malplaatje** een pagina herladen wanneer het terugkeren aan `None`. 13621
- AEM het publiceren van de Plaats ontmoet een kwestie wanneer het begaan aan aan de datastore voor grote kaarten met werkingsgebied peer verbindingen. 13531
- Probleem doet zich voor bij het doorverbinden aan datastore voor een grote DITA-kaart met bereik van peer-koppelingen in AEM publicatie van site. (13530)
- Het onjuiste pictogram en tooltip worden getoond voor **geef inhoud** optie in de **3&rbrace; toolbar van de Lay-outs van de Pagina &lbrace;van de Malplaatjes uit die in het Inheemse publiceren van PDF worden gebruikt.** 13492
- Onbekwaam om een plaats te activeren gebruikend het Dashboard van Publish van Experience Manager Guides **Bulk**. 13439
- In het publiceren van de Eigen PDF, wordt de toegankelijkheid gecompromitteerd aangezien de beelden in kopbal en footer alt geen tekst tonen. 12829
- In de AEM Sites-uitvoer zijn de stijl of regeleinden verloren gegaan voor het `<lines>` -element met subelementen.12542
- Het dupliceren van de paginalay-out in de native PDF werkt niet zonder automatische toevoeging. 12534
- De lokalisatie van de elementlabels werkt niet goed in de AEM Sites-uitvoer. (12144)
- Aangepaste metagegevens zijn niet beschikbaar in de uiteindelijke uitvoer. (1216)
- `fmdita rewriter` veroorzaakt een conflict met het opnieuw schrijven van de gebruiker config en leidt tot de vertoning van lange URLs in plaats van de verbindingen. (12076)
- Ontbrekende **ditaval** optie in het niveau van de output van het omslagprofiel vooraf instelt die via de Redacteur UI van het Web worden gecreeerd. (1903)
- In de **AEM vooraf ingestelde Plaats**, is de optie om **afzonderlijke PDF voor elk onderwerp** te produceren niet-functioneel. (11555)
- Native PDF-publicaties bieden geen ondersteuning voor het omzetten van CMYK-kleurruimten. 10754
- Bij de upgrade naar versie 4.3.1 zijn er enkele uitzonderingen in het knooppunt Native PDF. (1492)
- Wanneer u de PDF-uitvoer genereert met Native PDF-publicatie, wordt de bestandsnaam na een punt afgekapt. 13620


## Beheer

- De verwijzing van de inhoud wordt gebroken op kopiëren-kleeft de DITA- dossiers die zelfverwijzingsverbindingen zonder GUID hebben. 13540)
- **dossiers van de Filter van de Basislijn 0&rbrace; &lbrace;werken niet met de Naam van het Dossier in de Redacteur van het Web.** 13486
- In de Redacteur van het Web, toont de basislijn de titel voor de vorige versie in plaats van de geselecteerde versie van het DITA- dossier. (13444)
- Het onbruikbaar maken van het indexeren van de ouderkaart DITA om betere prestaties te krijgen kan de functionaliteit van bepaalde eigenschappen beïnvloeden.12213
- Voorinstellingen voor voorwaarden voor grote DITA-kaarten worden niet gemaakt. 10936
- Kan de voorinstellingen voor de eerste kaarten van de verzameling niet bewerken tijdens het bewerken van een kaartverzameling. 10649
- De etiketten van het `labels.json` dossier verschijnen in willekeurige orde in de Redacteur van het Web. 10508
- Dynamische basislijnaanroepen gebruiken de naam in plaats van de titel, wat resulteert in een fout van de DITA-kaart-API exporteren. 14268

## Controleren

- Klik contextmenu met de rechtermuisknop aan werkt niet voor **Accepteer** of **verwerp** spoorveranderingen. 14607
- In- en uitschakelen om DITA-onderwerpen in het revisiescherm te sluiten, werkt niet in versie 4.3.1 van Adobe Experience Manager Guides. 14537
- Symmetriekwesties doen zich voor in de deelvensters Naast elkaar van de vorige en de huidige versies in de Webeditor. 14156
- Het aanpassen van e-mailsjablonen voor de revisiewerkstroom werkt niet met overlay. 13954
- Op Koreaanse bijlagen kan niet worden geklikt in het scherm Experience Manager Guides Review. 13436
- De kaarthandleiding wordt afgesneden in het overzichts- en samenwerkingsscherm, zonder optie om de volledige titel te bekijken. 13012

## Vertaling

- De **Accepteren/verwerpen** knopen verschijnen abusievelijk voor auto-goedgekeurde menselijke vertaling. (14318)
- Problemen met internationalisatie (i18n) treden op tijdens de transformatie van DITA-bestanden die niet in het Engels staan, naar AEM pagina&#39;s. 14286
- Auto keurt niet soms goed, en de uitzonderingen komen voor als een onjuiste waarde op **de Status van de Vertaling** wordt geplaatst. 13607
- De basislijn die u exporteert vanaf het dashboard Vertalen mislukt en wordt niet geopend in de doeltaal. (12993)
- De vertaalde inhoud synchroniseert niet van tijdelijke vertaalprojecten, en de redacteurs vertaaltovenaar van DITA XML toont verkeerd **Bezig** status voor goedgekeurde banen. (9938)

## Bekend probleem

Adobe heeft het volgende bekende probleem voor de release 4.4.0 geïdentificeerd:

- Versie 1.0 wordt niet getoond op UI voor het gedupliceerde DITA- dossier.
