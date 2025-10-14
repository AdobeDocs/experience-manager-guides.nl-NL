---
title: Release-aantekeningen voor  [!DNL AEM Guides], release januari 2022
description: De versie van januari van  [!DNL Adobe Experience Manager Guides]  as a Cloud Service
exl-id: b2da77fa-f17c-440b-be59-acaafcd9a57c
feature: Release Notes
role: Leader
source-git-commit: 6d8c01f20f7b59fed92c404561b647d9ebecb050
workflow-type: tm+mt
source-wordcount: '2441'
ht-degree: 0%

---

# Release van januari [!DNL Adobe Experience Manager Guides] as a Cloud Service

## Upgrade naar de release van januari

Voer de volgende stappen uit om de huidige [!DNL Adobe Experience Manager Guides] as a Cloud Service instelling (later [!DNL AEM Guides] as a Cloud Service genoemd) bij te werken:
1. Controle uit de code van Git van Cloud Servicen en schakelaar aan de tak die in de pijpleiding van Cloud Servicen wordt gevormd die aan het milieu beantwoordt u wilt bevorderen.
1. Werk de eigenschap `<dox.version>` in het `/dox/dox.installer/pom.xml` -bestand van de Git-code van de Cloud Service bij naar 202.1.78.
1. Leg de wijzigingen vast en voer de pijplijn met Cloud Servicen uit om naar de release van januari van [!DNL AEM Guides] as a Cloud Service te upgraden.

## Compatibiliteitsmatrix

Deze sectie bevat een overzicht van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door de release van [!DNL AEM Guides] as a Cloud Service januari 2022.

### FrameMaker en FrameMaker Publishing Server

| FMPS | FrameMaker |
| --- | --- |
| Niet compatibel | 2020-update 4 en hoger |
| | |


### Zuurstofaansluiting

| [!DNL AEM Guides] Cloud Release | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2022,1,0 | 2.4.0. | 2.4.0. | 2,2 | 2,2 |
|  |  |  |  |  |


## Nieuwe en verbeterde functies

### Publicaties op basis van artikelen

Met de versie van Januari, hebben wij een op artikel-gebaseerde het publiceren eigenschap geïntroduceerd die binnen de Redacteur van het Web wordt geïntegreerd. U kunt de op artikel-gebaseerde het publiceren eigenschap gebruiken om output van één of meerdere onderwerpen stapsgewijs te produceren of uw inhoud aan een platform van de kennisbank te publiceren.

Deze eigenschap staat de gebruikers toe om de kaart DITA op een additieve manier te bouwen en onderwerpen te publiceren aangezien en wanneer zij klaar zijn. Zodra u uw kaart hebt gepubliceerd, gebruikt u de op artikel gebaseerde publicatiefunctie om alleen voor de bijgewerkte artikelen incrementele publicaties te maken.

![&#x200B; Op artikel-gebaseerde het publiceren &#x200B;](assets/article-based-publishing.png)

Naast AEM kunt u deze unieke functie gebruiken om uw artikelen te publiceren naar alle bekende portalen zoals Salesforce. Deze functie wordt ook geleverd met een sjabloon voor OOTB-inhoud, die is gebaseerd op AEM kerncomponenten, waarmee u een op kennis gebaseerde opslagplaats voor de technische inhoud kunt maken. Wat geweldig is aan deze sjabloon, is dat deze volledig aanpasbaar is aan uw organisatorische vereisten en ook ondersteuning biedt voor gebruiksgevallen zoals intranetportalen van bedrijven.
U kunt de artikelen ook filteren op basis van de documentstatus en de gewijzigde tijd.

Dit op behoefte-gebaseerde op artikel het publiceren van onderweg geeft u niet alleen volledige controle over uw inhoud het publiceren, maar vermindert ook de algemene tijd om uw bijgewerkte inhoud te publiceren.
Wanneer u artikelen publiceert met deze sjabloon, kunnen de metagegevens ook worden doorgegeven aan gepubliceerde pagina&#39;s.
Voor meer details, zie *Op artikel-gebaseerde het publiceren van de Redacteur van het Web* in de Gids van de Gebruiker.

### Verbeterde webeditor

Er zijn veel verhogingen en nieuwe eigenschappen die in de Redacteur van het Web worden geïntroduceerd:

* De steun voor onderwerpregeling is ook toegevoegd in de Redacteur van het Web. U kunt nu een onderwerpschema maken en gebruiken via het venster Onderwerpschema. Met de toevoeging van onderwerpschema, kunt u eigen collectieve meta-gegevens en taxonomie nu gebruiken.

![&#x200B; Onderwerpregeling &#x200B;](assets/subject-scheme-panel.png)

* Deze versie bevat een nieuw hulpprogramma voor woordenlijsten en hotspots voor het beheer van woordenlijsten. Met dit gereedschap kunt u snel tekst omzetten in een verklarende woordenlijst en een verklarende woordenlijst in termen die bulksgewijs worden gebruikt voor een geselecteerde kaart of open onderwerpen.

![&#x200B; Verklarende woordenlijst hotspot &#x200B;](assets/glossary-hotspot-tool.png)

* Functionaliteit voor vernieuwen is toegevoegd in het deelvenster Herbruikbare inhoud, waarmee u de herbruikbare inhoud in referentiebestanden snel kunt vernieuwen.
* De nieuwe het werk exemplaarindicator toont u of uw huidig (werkende exemplaar) van dossier met de bewaarde versie of niet synchroon is.

![&#x200B; de indicator van de Versie &#x200B;](assets/version-update-indicator.png)

* Het zoekfilter in het deelvenster Opslag en het dialoogvenster Bladeren van bestanden is verbeterd en biedt nu meer filteropties die u verder kunt aanpassen.

![&#x200B; filters van het Onderzoek in bewaarplaats &#x200B;](assets/repository-filter-search.png)

* U kunt .docx dossiers van de Redacteur van het Web nu uploaden.

### Auteur met FrameMaker

Nu kunt u documenten ontwerpen en publiceren in FrameMaker. FrameMaker wordt geleverd met een out-of-the-box aansluiting op Adobe Experience Manager. In de FrameMaker krijgt u een gebruiksvriendelijke interface waarmee u versies van uw documenten kunt onderhouden in een gedistribueerde omgeving met samenwerking.

Nadat u de inhoud hebt gemaakt, kunt u met FrameMaker uw documenten in verschillende indelingen publiceren: PDF, HTML,5, EPUB en DITA. U kunt ook de verschillende bestandsbeheerbewerkingen uitvoeren, zoals uitchecken, uitchecken met afhankelijke personen, inchecken, vernieuwen enzovoort.
Naar auteur met FrameMaker in [!DNL AEM Guides] as a Cloud Service versie van de FrameMaker 2020.4 en hoger.

### Nieuw vertaaldashboard

Een nieuw vertaaldashboard is geïntroduceerd in de Redacteur van het Web met de volgende eigenschappen:

* Het sorteren, het zoeken, en het filtreren van onderwerpenlijst.
* Inhoud filteren op referentietype - directe of indirecte referenties.
* Eenvoudige navigatie om een bestaand project te vinden terwijl het in werking stellen van een vertaalverzoek.
* Er is een meertalig vertaalmechanisme geïntroduceerd om te voorkomen dat er meerdere projecten voor elke taal worden gemaakt wanneer een vertaalaanvraag voor meer dan één taal wordt ingediend.
* Introduceerde een configuratie om het vertaallusje in kaartdashboard te verbergen. Standaard is deze zichtbaar. U kunt ervoor kiezen om inhoud te vertalen met behulp van het kaartdashboard of de webeditor.

![&#x200B; Vertaal dashboard &#x200B;](assets/translation-from-web-editor.png)

### Verbeterde publicatie

* Auteurs kunnen nu metagegevens op kaart- en onderwerpniveau doorgeven aan DITA-OT-publicaties. Dit is handig wanneer aangepaste PDF-sjablonen zijn ontworpen voor het gebruik van eigenschappen van bestandsmetagegevens, zoals tags, auteur, documentstatus en meer.

![&#x200B; meta-gegevens DITA-OT &#x200B;](assets/custom-meta-data-output-preset.png)

* Een nieuwe configuratie is toegevoegd om gebruikers toe te staan om de versies van de onderwerpen te behouden of te schrappen die worden geschrapt wanneer **schrapping en creeer** optie wordt gebruikt in de de outputgeneratie van de AEM.

### Verbeterde bestandsafhandeling

De volgende verbeteringen zijn nu zichtbaar tijdens het werken met bestanden in AEM Assets:
* Er is een nieuwe ervaring met het uploaden van bestanden en een nieuwe dialoog geïntroduceerd om een strategie voor het oplossen van conflicten te kiezen.

![&#x200B; het uploadconflict van het Dossier &#x200B;](assets/file-upload-name-conflict.png)

* Mogelijkheid om een nieuwe versie van het geüploade bestand te maken met de mogelijkheid te voorkomen dat een uitgecheckt bestand wordt overschreven.
* Nu kunt u een voorvertoning van afbeeldingen direct bekijken in de weergave Versiehistorie. Ook, voor DITA en niet-DITA- dossiers, toont de Geschiedenis van de Versie de huidige versieinformatie afzonderlijk.

![&#x200B; de geschiedenisduimnagel van de Versie &#x200B;](assets/version-history-preview-image.png)

* Telkens wanneer de gebruiker een DITA-bestand maakt, wordt de standaardbestandsnaam in kleine letters weergegeven om inline te zijn met het scenario dat de map Native AEM maakt.

### Nieuwe functie voor exporteren van rapport

Rapporten zijn zeer nuttig om de gezondheid van uw inhoud te identificeren. [!DNL AEM Guides] as a Cloud Service biedt verschillende rapporten die controle kunnen verkrijgen over uw inhoud. Nu, kunt u niet alleen de rapporten bekijken, maar ook de rapportgegevens in een Csv- dossier naar mening en met uw groter team delen. Rapportgegevens kunnen u een kort overzicht geven van verbroken koppelingen of ontbrekende afbeeldingen.

![&#x200B; de uitvoer van het Rapport &#x200B;](assets/export-report.png)

### Verbeterde Oxygen DAM-vernieuwingservaring

Wanneer u bestanden vernieuwt van AEM Server in Oxygen, wordt een waarschuwingsbericht weergegeven als u niet-opgeslagen bestanden in uw huidige Zuurstofsessie hebt. U kunt desgewenst de vernieuwingsbewerking annuleren om niet-opgeslagen bestanden op te slaan. Zonder deze functie verloren gebruikers niet-opgeslagen gegevens in hun documenten.


### Overige functieverbeteringen

* U kunt een nieuw **malplaatje van het Project van Dita** onder **/apps/projects/templates** nu creëren weg.
* Download nu het standaard {**dossier 0} ui_config.json van uw omslagprofielen.** Dit kan worden gebruikt om douaneveranderingen van het bestaande **ui_config.json** dossier samen te voegen terwijl het bevorderen.
* U hoeft de browsercache niet te wissen, zelfs niet wanneer er nieuwe versies van JS-bestanden aanwezig zijn.

## Opgeloste problemen

De fouten die in verschillende gebieden zijn gecorrigeerd, worden hieronder weergegeven:

### Webeditor

* Conrefs worden in rode kleur weergegeven, zelfs als ze niet worden gebroken. 8239
* Waarde voor voorwaardelijk kenmerk wordt niet automatisch ingevuld wanneer Alle eigenschappen toevoegen is geselecteerd in de DITAVAL-editor. 8234
* Auteurs kunnen geen afbeelding in een onderwerp invoegen met een relatief pad. 8112
* Controleer de taakpagina die de multimediabestanden niet weergeeft als er spaties voorkomen in de bestandsnaam. (8111)
* Ph-conref die in een tabelcel wordt toegevoegd, wordt in rode kleur weergegeven. 8083
* Koppelingen in de controletaak worden niet bijgewerkt wanneer de te controleren bestanden worden verplaatst. 8080
* De Redacteur van het Web geeft correct geen beelden terug die het schrapen bezit geplaatst aan 75% of hoger hebben. 8073
* Afbeeldingen van GIFFEN worden als statische afbeeldingen gerenderd in de webeditor. 8024
* Een conkeyref in een nota-element wordt niet getoond in de voorproef van de Redacteur van het Web of in de output. 8006
* xref naar een element dat zelf een conref is wordt niet opgelost in de redacteur. (7933)
* Titel met sleutel wordt niet correct weergegeven in de voorvertoning van de editor en in het deelvenster Opslagplaats. 7909
* Fragmenten met speciale tekens worden niet correct opgeslagen. 7908
* Het opslaan van een onderwerp na het formatteren van vergelijkingen MathML resulteert in een fout. 7954
* keydef (tm) wordt niet correct teruggegeven in de redacteur en de AEM plaatsuitvoer bevatte dubbele symbolen TM. 7859
* Het slepen en neerzetten van een fragment werkt niet volgens de DTD&#39;s. 7758
* HTML negeert aangepaste, gedefinieerde afmetingen voor afbeeldingen. 7718
* conrefend-kenmerk wordt niet bijgewerkt wanneer het bronbestand wordt verplaatst. 7698
* Het werken met het onderwerptypedocumenten van de Verwijzing leidt tot verscheidene kwesties UI. 7656
* DITAVAL-bestanden worden niet weergegeven wanneer de auteur ditavalref toevoegt aan een kaart. 7594
* Onverwachte ruimte wordt gevonden in elk leeg `<entry>` -element wanneer het attribuut outputclass wordt toegevoegd aan het `<tgroup>` -element. 7532
* De knop Source werkt niet voor onderwerpen die worden geopend via het dashboard voor kaarten. 7465
* Bij de mooie afdruk worden lege regels en spaties ingevoegd die zichtbaar zijn wanneer het bestand wordt geopend in FrameMaker of Zuurstof. 7408
* Kaarten met href=&quot;/&quot; in een van de onderwerpen publiceren niet op AEM sites. 7405
* De kwesties van prestaties die in de redacteur worden gevonden wanneer de wortelkaart groot aantal keydefs heeft. 7400
* De documentstatus voor een kaart met een aangepaste sjabloon wordt niet overgenomen van het corresponderende statusprofiel. 7359
* `<tm>` -element onjuist weergegeven als een blokelement. 7286
* Dubbele sjablonen worden weergegeven in het deelvenster met editorsjablonen wanneer een nieuwe sjabloon wordt gemaakt. 5814
* Sjablonen die zijn gedefinieerd in ui_config voor afbeeldingen voor het instellen van extra kenmerken, zijn niet van toepassing voor gevallen van slepen en neerzetten. 5713
* Onjuiste standaardweergave van uicontrol in menucascade. 5483
* De malplaatjes van de douane voor Onderwerp/Kaart tonen geen nieuwe naam in UI. Het toont de naam als &quot;Onderwerp&quot;/&quot;Kaart&quot;eerder dan het tonen van de gevormde naam. 4958
* Mogelijkheid om een routekaart te wissen uit de instellingen voor gebruikersvoorkeuren. 8534
* Een nieuw gemaakte kaartverzameling wordt niet weergegeven, zelfs niet nadat de pagina is vernieuwd.8603
* Het ontgrendelde onderwerp kan niet worden gesloten. 8545
* Het schakelen tussen bron en auteurswijze merkt het onderwerp als vuil en vereist dat de inhoud opnieuw wordt bewaard.8524
* Het deelvenster Inhoud opnieuw gebruiken crasht bij het zoeken naar speciale tekens `[` of `*` .8279
* De cursor wordt niet weergegeven in de zoekbalk wanneer het dialoogvenster Element invoegen wordt geopend met de sneltoets Alt+Enter.7912
* Met de optie Zoeken kunt u alleen zoeken in bestandsnamen en niet in inhoud. 7784


### Zuurstofaansluiting

* Bestanden waarvan de bovenliggende map speciale tekens bevat, geven een fout weer bij het laden in oxygen. 8054
* Wanneer een nieuw gecreeerd document in Zuurstof wordt geopend, het &quot;kan GUID&quot;fout vinden. 7856
* De optie Inchecken is uitgeschakeld nadat het bestand is uitgecheckt uit AEM met Bewerken in zuurstof. (7471)


### Controleren

* Synchronisatie in realtime werkt niet voor opmerkingen. 7661

### Kaartdashboard

* Kan conref-inhoud niet zien in de titel van een onderwerp in de onderwerpen of rapporten van het kaartdashboard. 8263
* AEM Sites-uitvoer | jcr:titel van de gegenereerde sitepagina wordt niet bijgewerkt wanneer de titel van het DITA-onderwerp wordt bijgewerkt. 8131
* Met MAP downloaden worden de videobestanden die in de onderwerpen worden gebruikt, niet gedownload. 8070
* Mediabestanden worden niet gedownload wanneer de objecttag wordt gebruikt via de API voor het downloaden van bladwijzers. 8057
* Het onjuiste rapport wordt getoond in het lusje van Rapporten als om het even welk onderwerp conref aan dossier heeft waarvan titel met conref begint. 4698
* Het dialoogvenster Labels toepassen op het tabblad Basislijn geeft geen labels weer in de vervolgkeuzelijst. 8455

### Publiceren

* Het maken van PDF mislukt voor de eerste keer wanneer Versioning inschakelen is geselecteerd. (8053, 8294)
* Witruimte wordt automatisch toegevoegd na een &#39;tm; -tag in AEM Site-uitvoer. 7964
* Kan YouTube-video&#39;s niet weergeven in AEM Site-uitvoer. 7401
* Filteren op label mislukt voor inhoud waarnaar wordt verwezen nadat de gebruiker op alle onderwerpen in het basislijntabblad van het kaartdashboard heeft geklikt. 7388
* Het publiceren van een onderwerp met element `<tm>` dat bezitswaarde SM of reg heeft wordt verkeerd getoond in geproduceerde output. 7239
* Bij publicatie in de basislijn met afbeelding wordt de meest recente versie van de afbeelding niet overgenomen in gepubliceerde uitvoer. 7231
* Relatable referenced onderwerpen wordt getoond in basislijnlusje. 5424
* De incrementele publicatie voor een onderwerp met conkeyref in de titel werkt niet zoals verwacht. 4474
* Paginatitel wordt niet gebruikt voor het genereren van URL-uitvoerbestanden, ook al is die instelling ingeschakeld. 8257
* Basislijnpublicatie kiest de huidige versie van de afbeeldingen in plaats van het bevroren knooppunt. Dit wordt ook weergegeven als een afbeelding spatie of speciale tekens in de bestandsnaam bevat. (8274, 832)
* Incrementeel publiceren mislukt voor DITA-kaart met hoofdletteronderwerpregeling. 8218)
* Null wordt toegevoegd wanneer een kaart wordt toegevoegd aan het Bulk Publish-dashboard. 8695
* Bij het gebruiken van basislijnpubliceren met beeld als conref in het onderwerp, wordt het beeld niet gepubliceerd in de output. 8564
* Publiceren mislukt, met een uitzondering als de basislijn die wordt gebruikt in AEM publicatie van de site wordt verwijderd. 8572
* De regeneratie van onderwerpen werkt niet. 8091
* Er zijn problemen met het publiceren van voetnoten in tabellen. 4709

### AEM Assets

* Er zijn prestatieproblemen aangetroffen tijdens het selecteren/verwijderen van enorme inhoud die is ingesteld in de gebruikersinterface van Assets. 8238
* Opgeslagen zoekfunctie (slimme verzameling) wordt afgebroken als DITA Predicate wordt toegevoegd aan zoekfilters. 8048
* Het terugzetten van de afbeelding naar een oudere versie werkt niet. (DXML-7903)
* De optie Verwijderen is ook zichtbaar voor auteurs die geen machtigingen hebben om te verwijderen. 7322
* CCMS-bedekking voor Assets Editor verbreekt rendering van de optie Verwijderen. 8093
* Documentprofiel wordt niet verwijderd. 8604
* Verwijzingen zijn verbroken wanneer u &quot;Alles selecteren&quot; uitvoert en de multimedia/Dita_Content naar een andere map verplaatst. 8621
* Er treden onjuiste verwijzingen op in de bron bij het verplaatsen van de elementen. (8627)
* De weergave met vaste lijsten wordt niet geladen. 8542

### Inhoud importeren

* HTML naar DITA-conversie | Tabel met &#39;tr&#39; met lege &#39;td&#39;-items veroorzaakt extra rijen in de uitvoer. 8132
* HTML naar DITA-conversie | HTML met een tabel met meerdere hoofdletters mislukt, met uitzondering van de tabel. 7940
* HTML naar DITA-conversie | fouten uit als bron HTML opmerkingen heeft. 7937
* Het importeren van DITA 1.3 DITA-bestanden zorgt ervoor dat sommige href wordt getransformeerd naar onjuist gevormde koppelingen. 8019

## Bekende problemen

Adobe heeft de volgende bekende problemen vastgesteld voor de release van [!DNL AEM Guides] as a Cloud Service januari 2022.


### Bekende problemen met tijdelijke oplossing

Gebruik de opgegeven tijdelijke oplossing voor de volgende bekende problemen:

* De webverificatie werkt niet voor de Zuurstofconnector op Mac.
  **Oplossing**: Gebruik de schakelaar van de Zuurstof op Vensters voor nu.

* In de Firefox-browser kunnen revisieopmerkingen alleen worden geïmporteerd als de weergave Naast elkaar wordt geopend.
  **Oplossing**: Gebruik browser van Chrome voor nu.

* Verwijzingen komen te vervallen bij het verplaatsen van afbeeldingen of multimediabestanden die ruimte(n) bevatten in de bestandsnamen.
  **Oplossing**: noem het dossier anders en verwijder de ruimten uit het dossier - naam alvorens hen te bewegen.

* Het kaartdashboard wordt niet periodiek geladen in de nieuwste versie van de Chrome-browser.
  **Oplossing**: vernieuw de pagina van het kaartdashboard.

### Andere bekende problemen

* Als Oxygen is aangesloten op de [!DNL AEM Guides] -oplossing via webverificatie, mislukt het afmelden.
* Revisietaken kunnen niet opnieuw aan de gebruikers worden toegewezen.
* De kwesties zijn aanwezig in de inzameling UI van de Kaart aangezien de tekst vervormd is en **Uitgezochte Al** functionaliteit niet correct werkt.
