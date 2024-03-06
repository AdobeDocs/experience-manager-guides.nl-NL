---
title: Opmerkingen bij de release | Upgradeinstructies en opgeloste problemen in Adobe Experience Manager Guides 4.4.0 release
description: Meer informatie over de opgeloste problemen en over het upgraden naar versie 4.4.0 van de Adobe Experience Manager-hulplijnen
source-git-commit: 1b25f1df67fa2442ab79830dc2ac5a6eabd0394c
workflow-type: tm+mt
source-wordcount: '1820'
ht-degree: 0%

---

# 4.4.0 Release van Adobe Experience Manager Guides (februari 2024)

In deze releasenotitie worden de instructies voor de upgrade, de compatibiliteitsmatrix en de problemen behandeld die zijn opgelost in versie 4.4.0 van de Adobe Experience Manager-hulplijnen (later genoemd als *Hulplijnen Experience Manager*).

Zie voor meer informatie over de nieuwe functies en verbeteringen [Nieuwe functies in 4.4.0-release van Adobe Experience Manager-hulplijnen](./whats-new-4-4.md).

## Upgrade naar versie 4.4.0 van de hulplijnen voor Experience Managers


U kunt uw huidige versie van de Gidsen van de Experience Manager aan versie 4.4.0 gemakkelijk bevorderen. Voordat u verdergaat met de upgrade naar versie 4.4.0 van de Experience Manager-hulplijnen, moet u rekening houden met de volgende punten:


- Als u versie 4.3.1, 4.3.0 of 4.2.1 (Hotfix 4.2.1.3) gebruikt, kunt u rechtstreeks upgraden naar versie 4.4.0.
- Als u versie 4.2, 4.1 of 4.1.x gebruikt, moet u een upgrade naar versie 4.3.1, 4.3.0 of 4.2.1 (Hotfix 4.2.1.3) uitvoeren voordat u een upgrade naar versie 4.4.0 uitvoert.
- Als u versie 4.0 gebruikt, moet u een upgrade naar versie 4.2 uitvoeren voordat u een upgrade naar versie 4.3.x uitvoert.
- Als u versie 3.8.5 gebruikt, moet u een upgrade naar versie 4.0 uitvoeren voordat u een upgrade naar versie 4.2 uitvoert.
- Als u een versie gebruikt die ouder is dan 3.8.5, raadpleegt u de sectie met instructies voor upgrades van Experience Manager in de productspecifieke installatiegids die beschikbaar is op [Adobe Experience Manager-hulplijnen Help PDF archiveren](https://helpx.adobe.com/xml-documentation-for-experience-manager/archive.html).



>[!NOTE]
>
>U moet AEM de dienstpak installeren alvorens de versie van de Gidsen van de Experience Manager te bevorderen.

Zie voor meer informatie [Upgradeinstructies](../install-guide/upgrade-xml-documentation.md).

## Compatibiliteitsmatrix

In deze sectie wordt een overzicht gegeven van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door de release van Experience Manager Guides 4.4.0.

### Adobe Experience Manager

**4.4.0 Niet-UUID**
Versie 6.5 Service Pack 19, 18, 17

**4.4.0 UUID**
Versie 6.5 Service Pack 19, 18, 17

Zie voor meer informatie de *Technische voorschriften* in de handleiding Adobe Experience Manager-hulplijnen installeren en configureren.

### FrameMaker en FrameMaker Publishing Server

| Geen | FMPS 2022 | FMPS 2020 | Fm 2022 | Fm 2020 |
| --- | --- | --- | --- | --- |
| 4.4.0 (niet-UUID) | 2022 of hoger | 2020.2 of hoger* | 2022 of hoger | 2020.3 of hoger |
| 4.4.0 (UUID) | 2022 of hoger | 2020.2 of hoger* | 2022 of hoger | 2020.4 of hoger |
| | | | |

*Basislijn en voorwaarden die in AEM zijn gemaakt, worden vanaf 2020.2 ondersteund in FMPS-releases.

### Zuurstofaansluiting

| Geen | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- |--- |--- |
| 4.4.0 (niet-UUID) | 2.7-regelmatig-1 | 2.7-regelmatig-1 | 1,6 | 1,6 |
| 4.4.0 (UUID) | 3.4-uuid-1 | 3.4-uuid-1 | 2,3 | 2,3 |
|  |  |   |



### Versie van basissjabloon

| Naam van componentenpakket | Versie van componenten | Sjabloonversie |
|---|---|---|
| Experience Manager Guides Components Content Package for Cloud Service | dxml-components.all-1.2.2 | aem-site-template-dxml.all-1.0.15 |

## Opgeloste problemen

De fouten die in verschillende gebieden zijn gecorrigeerd, worden hieronder weergegeven:

### Authoring

- Spellingcontrole in de Editor staat niet toe dat suggesties worden geselecteerd. 15045
- De algemene navigatieknop werkt niet en het dashboard kan niet worden geladen. 14968
- In de Redacteur van het Web, ontbreekt de eigenschap van de downloadkaart om een pop-up bericht teweeg te brengen wanneer het klaar is om te downloaden. 14626
- In de Redacteur van het Web, ontbreekt de eigenschap van de downloadkaart om een kaart met basislijn te downloaden. (14622)
- Ongeldige DTD-fout in de hulplijnen van de Experience Manager. (14482)
- De titel op het tabblad Webeditor wordt afgekapt na een punt (.) teken. 14372
- Foutberichten voor dubbele kaartnamen in de interface Elementen worden niet bijgewerkt. 14320
- Er treedt een fout op in de logica voor het maken van versies tijdens het slepen en neerzetten van elementen. 14291
- Herbruikbare inhoud slaat de element-id&#39;s over. 14213
- Het instellingsbesturingselement voor verbergen **Taalvariabelen** paneel onder **Uitvoer** ontbreekt. (14194)
- De Redacteur van het Web werpt toepassingsfouten wanneer het toevoegen van een nieuwe verwijzing of een onderwerp gebruikend een gespecialiseerd schema in **Layout** weergeven. (14094)
- De ruimte na conref `<ph>` het element verdwijnt bij het bewaren van het onderwerp. 13642
- Er treedt een toepassingsfout op wanneer wordt geprobeerd DITA-bestanden op te slaan voordat de naverwerking is voltooid. 13571
- Een ankerkoppeling naar `<dlentry>` of `<dt>` -element kan de koppelingstekst niet weergeven. 13543
- De **Favorieten** verzameling in de webeditor kan niet worden geladen. 13495
- Als de titel van een onderwerp een slash bevat `/`Op het tabblad in de webeditor worden alleen de letters weergegeven die erna komen. (13455)
- De voorvertoning van de afbeelding verdwijnt niet nadat de voorvertoning in de webeditor is weergegeven. 13454
- Bij het maken van een unieke id met spaties worden niet-klikbare koppelingen weergegeven. (13447)
- Wanneer u een onderwerp sluit nadat u het hebt bewerkt, wordt u omgeleid naar de AEM startpagina in plaats van terug te keren naar de mappenweergave. (13306)
- Het sleutelwoord van het Tussenvoegsel pop-up verschijnt niet wanneer het gebruiken van wortel kaart-bepaalde sleutels in andere onderwerpen. 12950
- Pictogrammen sluiten zijn niet zichtbaar wanneer een voorvertoning wordt weergegeven van zeer grote afbeeldingen in het dialoogvenster **Versiehistorie** deelvenster. 12867
- Kan de tijdzone van niet wijzigen **Versie gemaakt op** kolom voor de basislijnen. (1271)
- Zip-bestanden worden niet herkend in de webeditor en u kunt ze niet slepen en neerzetten. 12709
- De **Versiehistorie** in de interface Middelen een onjuist tijdstempel voor de **Huidig** veld. 12624
- In de **Layout** weergave voor een bladmap, gebruiken **Naar rechts** om een geselecteerd hoofdstuk te maken werkt een subelement niet. 12567
- Als u een DITA-bestand maakt op basis van een sjabloon met een bestandsnaam die begint met numerieke tekens, treedt er een naamruimtefout op. (12188)
- Het plaatsen van rootmap blijft in de Redacteur van het Web bestaan zelfs als de gebruiker het niet uitdrukkelijk van plaatsen **Gebruikersvoorkeuren**. (11551)
- De inhoud waarop bepaalde kenmerken zijn toegepast, wordt niet gemarkeerd in **Auteur** of **Voorvertoning** -modus. (1063)
- In de webeditor **Belangrijke verwijzingen** wordt geopend wanneer het venster wordt ingevoegd `varname` -tag. 10940
- Het slepen van een verklarend woordenlijstonderwerp van de bewaarplaats in een verklarende woordenlijstkaart leidt tot `topicref`. 10767
- Het voorvertoningsvenster van de XML-editor wordt afgebroken in Google Chrome- en Microsoft Edge-browsers. 10755
- In de webeditor is het niet mogelijk een element binnen de mogelijke bovenliggende elementen te plaatsen. 8791
- De webeditor wordt verwijderd nadat u Adobe Experience Manager Guides versie 4.3.1 opnieuw hebt geïnstalleerd. 14519
- Het installatieprogramma van versie 4.3.1 vindt een filterconflict, wat leidt tot het overschrijven van `apps/cq/core/content/projects/properties`. 14517
- Een koppeling met zelfverwijzing wordt weergegeven onder de lijst met **Verbroken koppelingen** in Rapporten. 13539
- Het voorvertoningsscherm voor fragmenten is bevroren. 14840
- Verbroken tekens worden weergegeven tijdens het maken van de fragmenten in de Koreaanse taal. 13489

### Publiceren

- Publiceren in AEM Sites mislukt en veroorzaakt bereikfouten voor bestanden met `xref` naar het DITA-bestand dat begint met &quot;HTTP&quot;. 15154
- In de publicatie Native PDF kunnen de metagegevenseigenschappen van de DITA-kaart niet worden gebruikt om de metagegevens voor uitvoer van PDF-bestanden te vullen. 15159
- In publicaties met native PDF werken aangepaste kenmerken binnen voorinstellingen voor voorwaarde niet voor publicatie met eigen PDF. 14943
- Kan geen aangepaste sjabloon toevoegen vanuit het dialoogvenster **Uitvoer** in de Editor. 14846
- **Site AEM** De voorinstelling werkt niet vanwege een leeg sjabloonpad. 14804
- AEM de regeneratie van de Plaats ontbreekt voor kaarten DITA met onderwerpen die vergelijkingen MathML bevatten. 14790
- In het Publiceren van Native PDF, genereren van PDF fouten in het krijgen van afhankelijkheden voor `Node.js` publiceren. (1445)
- **Site AEM** Met de voorinstelling kunt u een sjabloon niet buiten de `/content` in de webeditor. (14260)
- De functionaliteit om als inhoudsfragment te publiceren werkt niet voor dossiers die in onderzoeksresultaten worden vermeld. (14090)
- Fmdita-componenten hebben een hardcoded pad van `delegator.jsp`te voorkomen, de bedekking van AEM Sites-componenten te voorkomen. (13993)
- De getagde weergave van de PDF-reactor in Native PDF-publicatie-uitvoer werkt niet zoals u had verwacht. (13622)
- Bij publicatie als native PDF selecteert u de achtergrondkleur op het tabblad **Sjabloon** layout vereist dat de pagina opnieuw wordt geladen wanneer u terugkeert naar `None`. 13621
- AEM het publiceren van de Plaats ontmoet een kwestie wanneer het begaan aan aan de datastore voor grote kaarten met werkingsgebied peer verbindingen. 13531
- Probleem doet zich voor bij het doorverbinden aan datastore voor een grote DITA-kaart met bereik van peer-koppelingen in AEM publicatie van site. (13530)
- Onjuist pictogram en knopinfo worden weergegeven voor  **Inhoud bewerken** in de **Pagina-indelingen** werkbalk van de sjablonen die worden gebruikt in publicaties met native PDF. 13492
- Kan een site niet activeren met de hulplijnen voor Experience Managers **Bulk publicatiedashboard**. 13439
- In het publiceren van de Eigen PDF, wordt de toegankelijkheid gecompromitteerd aangezien de beelden in kopbal en footer alt geen tekst tonen. 12829
- In de AEM Sites-uitvoer gingen de stijl of regeleinden verloren voor de `<lines>` element met subelementen.12542
- Het dupliceren van de paginalay-out in de native PDF werkt niet zonder automatische toevoeging. 12534
- De lokalisatie van de elementlabels werkt niet goed in de AEM Sites-uitvoer. (12144)
- Aangepaste metagegevens zijn niet beschikbaar in de uiteindelijke uitvoer. (1216)
- `fmdita rewriter` veroorzaakt een conflict met de rewriter van de gebruiker config en leidt tot de vertoning van lange URLs in plaats van de verbindingen. (12076)
- Ontbreekt **ditaval** in uitvoervoorinstellingen op het niveau van het mapprofiel die zijn gemaakt via de gebruikersinterface van de webeditor. (1903)
- In de **Site AEM**  voorinstelling, de optie **Afzonderlijke PDF genereren voor elk onderwerp** is niet functioneel. (11555)
- Native PDF-publicaties bieden geen ondersteuning voor het omzetten van CMYK-kleurruimten. 10754
- Bij de upgrade naar versie 4.3.1 zijn er enkele uitzonderingen in het knooppunt Native PDF. (1492)
- Wanneer u de PDF-uitvoer genereert met Native PDF-publicatie, wordt de bestandsnaam na een punt afgekapt. 13620


### Beheer

- De verwijzing van de inhoud wordt gebroken op kopiëren-kleeft de DITA- dossiers die zelfverwijzingsverbindingen zonder GUID hebben. 13540)
- **Basislijnfilter** de dossiers werken niet met de Naam van het Dossier in de Redacteur van het Web. 13486
- In de Redacteur van het Web, toont de basislijn de titel voor de vorige versie in plaats van de geselecteerde versie van het DITA- dossier. (13444)
- Het onbruikbaar maken van het indexeren van de ouderkaart DITA om betere prestaties te krijgen kan de functionaliteit van bepaalde eigenschappen beïnvloeden.12213
- Voorinstellingen voor voorwaarden voor grote DITA-kaarten worden niet gemaakt. 10936
- Kan de voorinstellingen voor de eerste kaarten van de verzameling niet bewerken tijdens het bewerken van een kaartverzameling. 10649
- Labels uit de `labels.json` bestand wordt in willekeurige volgorde weergegeven in de webeditor. 10508
- Dynamische basislijnaanroepen gebruiken de naam in plaats van de titel, wat resulteert in een fout van de DITA-kaart-API exporteren. 14268

### Controleren

- Klikken met rechtermuisknop in contextmenu werkt niet voor **Accepteren** of **Afwijzen** wijzigingen bijhouden. 14607
- In- en uitschakelen om DITA-onderwerpen in het revisiescherm te sluiten, werkt niet in versie 4.3.1 van Adobe Experience Manager-hulplijnen. 14537
- Symmetriekwesties doen zich voor in de deelvensters Naast elkaar van de vorige en de huidige versies in de Webeditor. 14156
- Het aanpassen van e-mailsjablonen voor de revisiewerkstroom werkt niet met overlay. 13954
- Op Koreaanse bijlagen kan niet worden geklikt in het scherm Experience Manager Guides Review. 13436
- De kaarthandleiding wordt afgesneden in het overzichts- en samenwerkingsscherm, zonder optie om de volledige titel te bekijken. 13012

### Vertaling

- De **Accepteren/afwijzen** De knoppen worden abusievelijk weergegeven voor automatisch goedgekeurde menselijke vertaling. (14318)
- Problemen met internationalisatie (i18n) treden op tijdens de transformatie van DITA-bestanden die niet in het Engels staan, naar AEM pagina&#39;s. 14286
- Automatisch goedkeuren werkt soms niet, en de uitzonderingen komen voor als een onjuiste waarde wordt geplaatst **Vertaalstatus**. 13607
- De basislijn die u exporteert vanaf het dashboard Vertalen mislukt en wordt niet geopend in de doeltaal. (12993)
- De vertaalde inhoud synchroniseert niet van tijdelijke vertaalprojecten, en de redacteurs vertaaltovenaar van DITA XML toont verkeerd **In uitvoering** status voor goedgekeurde banen. (9938)

## Bekend probleem

Adobe heeft het volgende bekende probleem voor de release 4.4.0 geïdentificeerd:

- Versie 1.0 wordt niet getoond op UI voor het gedupliceerde DITA- dossier.