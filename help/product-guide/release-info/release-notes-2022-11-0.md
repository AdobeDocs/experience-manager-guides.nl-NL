---
title: Opmerkingen bij de release | Adobe Experience Manager Guides as a Cloud Service, release november 2022
description: Release van Adobe Experience Manager Guides as a Cloud Service
exl-id: 9f329ec1-dd74-47cc-8567-3fadd962584a
feature: Release Notes
role: Leader
source-git-commit: 6d8c01f20f7b59fed92c404561b647d9ebecb050
workflow-type: tm+mt
source-wordcount: '1384'
ht-degree: 0%

---

# Release van Adobe Experience Manager Guides as a Cloud Service

## Upgrade naar de release van november

Bevorder uw huidige as a Cloud Service Adobe Experience Manager Guides (later als *wordt bedoeld AEM Guides as a Cloud Service*) opstelling door de volgende stappen uit te voeren:
1. Controle uit de code van Git van Cloud Servicen en schakelaar aan de tak die in de pijpleiding van Cloud Servicen wordt gevormd die aan het milieu beantwoordt dat u wilt bevorderen.
1. Werk de eigenschap `<dox.version>` in het `/dox/dox.installer/pom.xml` -bestand van de Git-code van de Cloud Service bij tot 2022.11.198.
1. Leg de veranderingen vast en stel de pijpleiding van Cloud Servicen in werking om aan de versie van November van as a Cloud Service AEM Guides te bevorderen.

## Stappen om de bestaande inhoud te indexeren (Alleen als u een versie hebt die ouder is dan de release van AEM Guides as a Cloud Service in september)

Voer de volgende stappen uit om de bestaande inhoud te indexeren en de nieuwe tekst zoeken en vervangen op kaartniveau te gebruiken:

* Voer een verzoek van de POST op de server uit (met correcte authentificatie) - `http://<server:port>/bin/guides/map-find/indexing`.
(Optioneel) U kunt specifieke paden van de kaarten doorgeven om deze te indexeren. Standaard worden alle kaarten geïndexeerd || Voorbeeld: `https://<Server:port>/bin/guides/map-find/indexing?paths=<map_path_in_repository>`)

* De API retourneert een jobId. Als u de status van de taak wilt controleren, kunt u een aanvraag voor een GET met taak-id naar hetzelfde eindpunt verzenden - `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}`
(Bijvoorbeeld: http://&lt;_localhost:8080_>/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c183 79f11c42_678)

* Als de taak is voltooid, reageert het bovenstaande verzoek van de GET met succes en vermeldt u of kaarten zijn mislukt. De met succes geïndexeerde kaarten kunnen van de serverlogboeken worden bevestigd.

## Compatibiliteitsmatrix

Deze sectie maakt een lijst van de verenigbaarheidsmatrijs voor de softwaretoepassingen die door de versie van AEM Guides as a Cloud Service November 2022 worden gesteund.

### FrameMaker en FrameMaker Publishing Server

| FMPS | FrameMaker |
| --- | --- |
| Niet compatibel | 2020-update 4 en hoger |
| | |

*Basislijn en voorwaarden die in AEM zijn gemaakt, worden vanaf 2020.2 ondersteund in FMPS-releases.

### Zuurstofaansluiting

| AEM Guides als Cloud Release | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2022 11,0 | 2.7.13. | 2.7.13. | 2,3 | 2,3 |
|  |  |  |  |


## Nieuwe en verbeterde functies

AEM Guides as a Cloud Service verstrekt verhogingen en nieuwe eigenschappen in de versie van november:


### Bestanden verwijderen uit het deelvenster Opslagplaats

Nu kunt u dossiers (enig dossier tegelijkertijd) van het **menu van Opties** van het geselecteerde dossier van het bewaarplaatspaneel gemakkelijk schrappen.
<img src="assets/repository-delete-file.png" alt="Verwijderen uit opslagplaats" width="500">

Er wordt een bevestigingsbericht weergegeven voordat u het bestand verwijdert. Als er vanuit een ander bestand niet naar het bestand wordt verwezen, wordt het bestand verwijderd en wordt een succesbericht weergegeven.

Als het geselecteerde bestand is uitgecheckt, kunt u het niet verwijderen en wordt een foutbericht weergegeven. Als het geselecteerde bestand wordt toegevoegd aan een favoriete verzameling of vanuit een ander bestand wordt verwezen, controleert AEM hulplijnen of het bestand is bevestigd en kunt u het bestand met kracht verwijderen. Als u een onderwerp waarnaar wordt verwezen verwijdert en u het bestand met verwijzingen hebt geopend voor bewerken, wordt de verbroken koppeling voor het bestand waarnaar wordt verwezen, weergegeven.

**Nota**: U kunt het geselecteerde dossier ook schrappen gebruikend de sleutel van de Schrapping van het toetsenbord.


### Geselecteerde versies van bestanden wissen

Terwijl u inhoud maakt en onderhoudt, worden mogelijk veel versies gemaakt voor uw DITA-bestanden in uw opslagplaats. Met AEM Guides kunt u oudere versies van uw DITA-bestanden uit de opslagplaats verwijderen en schijfruimte vrijmaken.

<img src="assets/preview-purge-report.png" alt="Voorvertoning rapport leegmaken" width="500">


AEM Guides verwijdert niet de eerste versie van het bestand of een versie die in een basislijn is opgenomen, of heeft er een label op toegepast. Met Leegmaken worden zelfs geen bestanden verwijderd die deel uitmaken van een vertaling- of revisiewerkstroom. U kunt het aantal versies kiezen dat u wilt behouden en u kunt ook besluiten om de bestanden te verwijderen die ouder zijn dan het gedefinieerde aantal dagen.

Voordat u de purgeerbewerking start, kunt u een voorvertoning van het rapport bekijken van de versies die worden gewist. Vervolgens kunt u besluiten de leegmaakbewerking te starten of te annuleren.

<img src="assets/download-purge-report.png" alt="PDownload-rapport" width="500">

Zodra de leegmaakbewerking is voltooid, kunt u het rapport leegmaken controleren om de gezuiverde bestanden te zien.

### Uitvoervoorinstellingen voor Algemeen en Mapprofiel beheren

AEM Guides biedt u de functie om uitvoervoorinstellingen voor de algemene profielen en mapprofielen te maken en te beheren. Vervolgens kunt u deze uitvoervoorinstellingen eenvoudig gebruiken om uitvoer te genereren voor alle mappen die betrekking hebben op dat algemene profiel of mapprofiel.

<img src="assets/add-global-output-preset.png" alt="Globaal profiel toevoegen" width="400">

**Nota** slechts kunnen de beheergebruikers van het omslagniveau Globale en Voorinstellingen van het Profiel van de Omslag tot stand brengen.

Deze globale voorinstellingen verschijnen onder het **lusje van de Output** van alle verwante kaarten. U kunt ze gebruiken om de uitvoer voor alle verwante kaarten te genereren. U kunt de voorinstelling selecteren als standaard PDF-voorinstelling om de PDF-uitvoer te genereren. U kunt ook **uitgeven**, **anders noemen**, **Dupliceren**, of **schrapt** een bestaande output vooraf ingesteld van het **menu van Opties**.

### De kolom Versielabel die aan het vertaaldashboard wordt toegevoegd

In het vertaaldashboard, kunt u de kolom van het Etiket van de Versie ook zien. Hierdoor wordt het label voor de geselecteerde versie van het bronbestand weergegeven. Hiermee kunt u alle bestanden met een specifiek label selecteren en in één keer vertalen.

<img src="assets/send-translation.png" alt="verzenden voor vertaling" width="600">


### Native PDF | PDF met wijzigingsbalk die het verschil tussen documentversies aangeeft

Nu kunt u een PDF maken die de verschillen in inhoud tussen twee versies weergeeft met de wijzigingsbalk. U kunt de huidige versie vergelijken met een basislijn van de vorige versie of de twee geselecteerde basislijnversies vergelijken.

<img src="assets/pdf-change-version.png" alt="spdf-change-version" width="600">

Er wordt een wijzigingsbalk weergegeven in de PDF om de gewijzigde, ingevoegde of verwijderde inhoud aan te geven. U kunt ook het volgende doen:
* Ingevoegde inhoud in groene kleur en onderstreept weergeven
* De verwijderde inhoud rood weergeven en doorhalen

### Native PDF | Ondersteuning voor variabelen voor Uitvoerpad en bestandsnaam PDF

U kunt nu ook de volgende variabelen gebruiken om het uitvoerpad en het PDF-bestand te definiëren. U kunt een enkele of een combinatie van variabelen gebruiken om de volgende opties te definiëren:
* `${map_filename}`
* `${map_title}`
* `${preset_name}`
* `${language_code}`
* `${map_parentpath}` (Alleen voor uitvoerpad)
* `${path_after_langfolder}` (Alleen voor uitvoerpad)


### Native PDF | Inhoudsopgave genereren voor DITA-kaarten en de paginalay-outs opnieuw ordenen

Nu kunt u TOC in kaarten ook produceren DITA gebruikend een geavanceerde PDF het plaatsen van het malplaatje. U kunt de weergave van de verschillende paginalay-outs in- of uitschakelen en ook de positie ervan wijzigen.

## Opgeloste problemen

De fouten die in verschillende gebieden zijn gecorrigeerd, worden hieronder weergegeven:

* Native PDF | `conkeyref` wordt niet omgezet in de gegenereerde PDF-uitvoer. 10564
* Native PDF | Er doen zich problemen voor bij de toegang tot metagegevens van een kaart in de uitvoer van PDF. (10556)
* Native PDF | Inline stijl wordt gebruikt voor het genereren van tags in plaats van klassenaam.  10498
* De webeditor laadt regelmatig een lege pagina. 10678
* Publiceren via PDF mislukt als we een voorinstelling maken door een bestaande voorinstelling te dupliceren. 10584
* **de knoop van het Logboek van de Mening** werkt niet wanneer de generatie van de PDF voor vooraf ingesteld ontbreekt. 10576
* Notitie in een paratag die een conref is, wordt niet weergegeven in de voorvertoning. (10559)
* Als u de backspace aan het einde van een lijstitem aanpast, wordt de hele lijst verwijderd. 10540
* Wanneer u een native PDF-export gebruikt, worden de geneste `<indexterm>` niet in de index genest. 10521
* **auto-Inspringing** knoop in de toolbar ontbreekt in de Mening van Source. (10448)
* Het eerste teken van een lijstitem gaat verloren terwijl de lijst wordt geschreven in de editor. 10447
* Er worden meerdere pop-ups weergegeven als een DITA-elementversie wordt gewijzigd en opgeslagen in het basislijnbewerkingsvenster. 10399
* De fout van de toepassing komt bij het klikken **uit** knoop na het selecteren van al Output vooraf instelt van Snel uit produceert paneel. (10388)
* De meta-gegevens van de douane voor DITA onderwerp wordt niet behouden wanneer een actie van de exemplaardeeg van Assets UI wordt uitgevoerd. 10367
* Post-verwerking wordt geblokkeerd voor de volledige taalmap waarvan de middelen aanwezig zijn in een actief vertaalproject. (1032)
* Het tabblad Sjabloon in de XML-editor is niet zichtbaar voor beheerders van mapprofielen. (10266)
* De kwesties van de navigatie komen in de Redacteur van het Web na 4.0 verbetering voor. 10159
* SVG-bestanden worden niet weergegeven in de modus Voorbeeld. 10010
* Als het tabblad Uitvoer van de Editor meer voorinstellingen bevat, kan de sectie Voorinstellingen niet worden geschoven en worden niet alle voorinstellingen weergegeven. 9787
* **geeft** uit en **annoteert** opties voor een beeld niet correct in de kolommening. 8758
* Peer-koppeling wordt niet omgezet en wordt weergegeven als normale tekst in de gegenereerde uitvoer. (774)
