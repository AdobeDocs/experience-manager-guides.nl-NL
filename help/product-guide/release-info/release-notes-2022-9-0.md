---
title: Opmerkingen bij de release | Adobe Experience Manager Guides as a Cloud Service, release september 2022
description: Release Adobe Experience Manager Guides as a Cloud Service september
exl-id: f6247f91-43cc-43a4-a6f8-3b1f09d0533f
feature: Release Notes
role: Leader
source-git-commit: 6d8c01f20f7b59fed92c404561b647d9ebecb050
workflow-type: tm+mt
source-wordcount: '1299'
ht-degree: 0%

---

# Release Adobe Experience Manager Guides as a Cloud Service september

## Upgrade naar de release van september

Bevorder uw huidige as a Cloud Service Adobe Experience Manager Guides (later als *wordt bedoeld AEM Guides as a Cloud Service*) opstelling door de volgende stappen uit te voeren:
1. Controle uit de code van Git van Cloud Servicen en schakelaar aan de tak die in de pijpleiding van Cloud Servicen wordt gevormd die aan het milieu beantwoordt dat u wilt bevorderen.
1. Werk de eigenschap `<dox.version>` in het `/dox/dox.installer/pom.xml` -bestand van de Git-code van de Cloud Service bij naar 2022.9.178.
1. Leg de wijzigingen vast en voer de pijplijn met Cloud Servicen uit om naar de release van AEM Guides as a Cloud Service in september te upgraden.

## Stappen om de bestaande inhoud te indexeren

Voer de volgende stappen uit om de bestaande inhoud te indexeren en de nieuwe tekst zoeken en vervangen op kaartniveau te gebruiken:
* Voer een verzoek van de POST op de server uit (met correcte authentificatie) - `http://<server:port>/bin/guides/map-find/indexin`.
(Optioneel) U kunt specifieke paden van de kaarten doorgeven om deze te indexeren. Standaard worden alle kaarten geïndexeerd ||  Voorbeeld:   `https://<Server:port>/bin/guides/map-find/indexing?paths=<map_path_in_repository>`)
* De API retourneert een jobId. Als u de status van de taak wilt controleren, kunt u een aanvraag voor een GET met taak-id naar hetzelfde eindpunt verzenden - `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}`
(Bijvoorbeeld: `http://<_localhost:8080_>/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678)`
* Als de taak is voltooid, reageert het bovenstaande verzoek van de GET met succes en vermeldt u of kaarten zijn mislukt. De met succes geïndexeerde kaarten kunnen van de serverlogboeken worden bevestigd.


## Compatibiliteitsmatrix

In deze sectie wordt een overzicht gegeven van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door de AEM Guides as a Cloud Service september 2022-release.

### FrameMaker en FrameMaker Publishing Server

| FMPS | FrameMaker |
| --- | --- |
| Niet compatibel | 2020-update 4 en hoger |
| | |

*Basislijn en voorwaarden die in AEM zijn gemaakt, worden vanaf 2020.2 ondersteund in FMPS-releases.

### Zuurstofaansluiting

| AEM Guides als Cloud Release | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2022,9,0 | 2.7.13. | 2.7.13. | 2,3 | 2,3 |
|  |  |  |  |


## Nieuwe en verbeterde functies

AEM Guides as a Cloud Service biedt veel verbeteringen en nieuwe functies in de release van september:


### Een dynamische basislijn maken op basis van labels

AEM Guides beschikt nu over de functie om dynamische basislijnen te maken op basis van labels. Als u een basislijn genereert, een basislijn downloadt of een vertaalproject maakt met een basislijn, worden de bestanden dynamisch gekozen op basis van de bijgewerkte labels. Deze functie is handig omdat u de basislijn niet hoeft te wijzigen wanneer u de labels bijwerkt.
U kunt de momentopname van de basislijn als CSV ook uitvoeren.

![&#x200B; creeer basislijnen &#x200B;](assets/dynamic-baseline.png)

### Tekst zoeken en vervangen op kaartniveau

U kunt nu zoeken naar bestanden in een kaart die specifieke tekst bevatten. De gezochte tekst wordt benadrukt in de dossiers. U kunt het gezochte woord of de gezochte uitdrukking met een ander woord of een uitdrukking binnen de dossiers ook vervangen.
Selecteer **vervangen** pictogram om het huidige voorkomen te vervangen en **vervangen allen in dossier** pictogram om alle voorkomen in het geselecteerde dossier te vervangen.

![&#x200B; vinden Vervangen in kaart &#x200B;](assets/map-find-replace.png)

Door gebrek, worden het dossier van de optiecontrole **alvorens** te vervangen en **nieuwe versie na vervangen** geselecteerd, zodat wordt een dossier gecontroleerd alvorens u de tekst vervangt, en een nieuwe versie wordt gecreeerd nadat de tekst wordt vervangen.

### Het versieverschil voor uit-synchronisatiebestanden van het vertaaldashboard weergeven

U kunt nu verkiezen om **uit de dossiers van de Synchronisatie** te vertalen die op de veranderingen worden gebaseerd die tussen de twee versies van een onderwerp worden gedaan.\
![&#x200B; Vertaal dashboard &#x200B;](assets/translation-version-diff.png)
Vanuit het vertaaldashboard kunt u eenvoudig zien wat de verschillen zijn tussen de laatste vertaalde versie en de huidige versie van het geselecteerde bestand.

![&#x200B; de dialoog van het versieverschil &#x200B;](assets/version-diff.png)

Gebaseerd op de verschillen, kunt u beslissen of u een onderwerp wilt vertalen of niet.

### Gebruikersinterface met metagegevens beschikbaar voor PDF-voorinstellingen

U kunt de metagegevens instellen vanuit de uitvoervoorinstelling van een DITA-kaart. U kunt de metagegevens Titel, Auteur, Onderwerp en Trefwoorden instellen. Deze metagegevens worden toegewezen aan de metagegevens in de bestandseigenschappen van de uitvoer PDF.
Deze metagegevens overschrijven de metagegevens die op boekniveau zijn gedefinieerd. U kunt de metagegevens specifiek definiëren in elke uitvoervoorinstelling en deze doorgeven aan de PDF van de uitvoer.

![&#x200B; Meta-gegevens in Vooraf ingesteld &#x200B;](assets/preset-metadata.png)


## Opgeloste problemen

De fouten die in verschillende gebieden zijn gecorrigeerd, worden hieronder weergegeven:

* Webeditor | Bij het bewegen van elementen binnen een onderwerp, toegewezen IDs op elementen worden beschreven door auto-toegewezen IDs. 7895
* Wijzigingen bijhouden | De inhoud gaat verloren wanneer een nieuw element wordt ingegaan gebruikend de Enter sleutel. 10246
* Submap die naar de hoofdkaart in dita-malplaatjes wordt verwezen wordt niet gecreeerd. 10231
* XML-editor | Kopiëren en plakken werkt niet in de modus Schrijver. 10309
* Meerdere versielabels die u hebt geselecteerd, worden niet uitgeschakeld. 9561
* Automatische navigatie naar het pad in het dialoogvenster Bladeren van de site werkt niet zoals bladeren door bestanden. (9920)
* Het paneel van het overzicht toont geen inhoud wanneer geschakeld van **Auteur** aan **Source** wijze. 10319
* Conref in een nieuw gecreeerd onderwerp gebruikend een inhoud in het onderwerpmalplaatje werkt niet. De gekopieerde hash-id wordt niet bijgewerkt in de inhoudskopie. 9890
* Web-editor | Er bestaat geen lader tijdens het maken van een kaart van de kaartsjabloon. 9891
* Nieuwe kaarteditor | De toegevoegde gewaagde of Cursieve tekst in de kaarttitel wordt niet behouden als wij van **Auteur** aan de **3&rbrace; mening van de Lay-out &lbrace;schakelen.** 10218
* Nieuwe kaarteditor | De voorwaarden die op een verwijzing worden toegepast, kunnen niet uit de layoutweergave worden verwijderd. 10213
* Nieuwe kaarteditor | Het toepassen van voorwaardenverwijzingen werkt niet in de mening van de Lay-out zoals de mening van de Auteur. (10198)
* Nieuwe kaarteditor | Met de optie Naar links verplaatsen in het contextmenu wordt de verwijzing verwijderd als deze niet naar links kan worden verplaatst. 10219
* Nieuwe kaarteditor |Het pictogram wordt onjuist weergegeven voor de verwijzingen in een kaart die is gemaakt met de layoutweergave. (10197)
* Deelvenster Opslagplaats | Klik met de rechtermuisknop in het deelvenster Opslagruimte geeft een toepassingsfout. 10123
* Zoeken en vervangen | De donkere modus is niet leesbaar voor zoekresultaten in de webeditor. (978)
* Vertaling | Metagegevens en tags worden niet doorgegeven aan de vertaalde kopieën. 4696
* Bij kopiëren en plakken (ctrl+c/ctrl+v) treedt een fout op in de auteurmodus. 10304
* PDF-sjabloon | Als u achtergrondafbeeldingen toevoegt aan een paginalay-out, wordt het afbeeldingspad absoluut weergegeven en worden de afbeeldingen niet weergegeven in de PDF van de uitvoer. 10297
* Native PDF | De titel van het hoofdstuk en de koptekst van het hoofdstuk werken niet in het publiceren van PDF. (9947)
* Native PDF | `xref` voor een concept wordt niet correct opgelost voor een specifiek onderwerp DITA. (1029)
* Native PDF | Kan de bijschrifttekst voor een tabel niet weergeven in de gegenereerde PDF-uitvoer. 9827
* Native PDF | Verwijzingen in bijlagen worden niet als bijlagen weergegeven in PDF-uitvoer. (10182)
* Native PDF | Het kenmerk Frame voor een tabel wordt niet doorgegeven aan de tijdelijke HTML (als klasse). 10353
* Native PDF | temp HTML-bestanden voegen de klassen colsep en rowsep toe aan td en de klassen zelfs als de waarde 0 is in de bron-DITA. 10352
* Native PDF |  Metagegevens voor criteria die in paginalay-out zijn toegevoegd, worden niet ondersteund. 10377
* Native PDF |  Genereren van PDF mislukt voor specifieke inhoud. (9927)
* Native PDF | Inhoud via conkeyref wordt niet weergegeven in de PDF-uitvoer. 9836
* Native PDF | Belangrijke referenties voor Keydefs met afbeeldingen of externe koppelingen zijn niet opgelost. 10063
* In de weergave Auteur voor een kaart wordt geen plaatsaanduidingstekst weergegeven voor tabellen en figuurlijsten. (10330)
* Wanneer we een nieuwe basislijn maken, wordt het reeds geselecteerde basislijnfilter niet toegepast. (9954)
* Videobestand ontbreekt vanaf de basislijn als de naam van de bovenliggende map een spatieteken heeft. (10031)
* Bij het maken van de basislijn wordt de laatste versie niet gekozen als de tijdzone van de gebruiker afwijkt van de tijdzone van de server. (10190)
* Met Control + F wordt de zoekmodus van de browser in de Assets-console niet geopend nadat u AEM Guides 4.1 op AEM 6.5.12 hebt geïnstalleerd. 10189


## Bekende problemen

Adobe heeft de volgende bekende problemen voor de release van AEM Guides as a Cloud Service september 2022 vastgesteld.


* Dynamische basislijn is niet geïntegreerd met publicatie op basis van kennis.

* Vertaling | Het pictogram Versieverschil wordt weergegeven voor de broninhoud vanwege wijzigingen in de doelinhoud.
