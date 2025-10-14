---
title: Opmerkingen bij de release | Nieuwe functies in de Adobe Experience Manager Guides, release 2024.4.0
description: Leer de nieuwe en verbeterde functies in de 2024.4.0 release van Adobe Experience Manager Guides as a Cloud Service.
exl-id: e9db535a-5ad5-4ff0-94af-b4425594316a
source-git-commit: 5d99274da8fdacbd255d426fa4913b5773ca45f8
workflow-type: tm+mt
source-wordcount: '1806'
ht-degree: 0%

---

# Nieuwe functies in de release 2024.4.0

Dit artikel behandelt de nieuwe en verbeterde functies van de release 2024.4.0 van Adobe Experience Manager Guides.

Voor de lijst van kwesties die in deze versie worden bevestigd, mening [&#x200B; Vaste kwesties in de versie 2024.4.0 &#x200B;](fixed-issues-2024-04-0.md).

Leer over [&#x200B; verbeteringsinstructies voor de versie 2024.4.0 &#x200B;](upgrade-instructions-2024-04-0.md).

## Mogelijkheid om inhoud in meerdere talen te vertalen met behulp van vooraf geconfigureerde taalgroepen

Met Experience Manager Guides kunt u nu taalgroepen maken en uw inhoud eenvoudig in meerdere talen vertalen. Met deze functie kunt u vertalingen volgens de behoeften van uw organisatie ordenen en beheren.

Als u bijvoorbeeld uw inhoud voor bepaalde landen in Europa wilt vertalen, kunt u een taalgroep voor Europese talen maken, zoals Engels (EN), Frans (FR), Duits (DE), Spaans (ES) en Italiaans (IT).



![&#x200B; vertaalpaneel &#x200B;](assets/translation-languages-2404.png){width="300" align="left"}

*selecteer de taalgroepen of de talen u uw documenten wilt vertalen.*

>[!NOTE]
>
>Als de doelmap van een taal ontbreekt of als de doeltaal gelijk is aan de bron, wordt deze grijs weergegeven en wordt een waarschuwingsteken weergegeven.

Als beheerder kunt u taalgroepen maken en deze configureren naar meerdere mapprofielen. Als auteur kunt u de taalgroepen weergeven die zijn geconfigureerd in uw mapprofiel.


Het maken van taalgroepen verbetert over het algemeen de efficiëntie en productiviteit van vertaalprojecten en verbetert uiteindelijk het lokalisatieproces in meerdere talen.


Leer hoe te [&#x200B; documenten van de Redacteur van het Web &#x200B;](../user-guide/translate-documents-web-editor.md) vertalen.



## Het vertaalproject na de vertaling automatisch verwijderen of uitschakelen

Nu, als beheerder, kunt u de vertaalprojecten vormen om na de voltooiing van de vertaling worden onbruikbaar gemaakt of automatisch worden geschrapt. Met deze functie kunt u efficiënt bronnen gebruiken en bestanden beheren nadat de vertaling is voltooid.

Als u een project verwijdert, worden alle bestanden en mappen in het project permanent verwijderd. Het schrappen van de vertaalprojecten laat u ook toe om de bezette schijfruimte vrij te maken.

U kunt de vertaalprojecten onbruikbaar maken als u hen later wilt gebruiken.

![](assets/editor-setting-translation.png){width="550" align="left"}


*vormt taalgroepen en de schoonmaakmontages voor vertaalprojecten.*


Leer meer over hoe te [&#x200B; automatisch schrappen of het vertaalproject &#x200B;](../user-guide/translate-documents-web-editor.md#automatically-delete-or-disable-a-completed-translation-project) onbruikbaar maken.


## De uitvoer voor uw kaarten in bulkactiveringsverzameling activeren op Voorvertoning-instantie

Nu, naast het activeren van de output voor uw bulkactiveringsinzameling op publiceer instantie, verstrekt de Gidsen van de Experience Manager als Cloud Servicen de eigenschap om het op de **1&rbrace; instantie van de Voorproef te activeren.**


Deze eigenschap helpt u uw inhoud aan een voorproefinstantie activeren, toestaand u om te controleren hoe het kijkt en werkt alvorens het aan de **Publish** instantie te activeren.


![&#x200B; gecreeerde bulkactivering inzamelingsgeschiedenis tabel &#x200B;](assets/bulk-collection-audit-history.png){width="800" align="left"}

*Mening de informatie over de geactiveerde kaartoutput in de **Geschiedenis van de Controle**&#x200B;tabel.*


Leer meer over [&#x200B; bulkactivering &#x200B;](../user-guide/conf-bulk-activation-publish-map-collection.md).

## Verbeteringen in de gegevensbronconnectors

De volgende verbeteringen zijn aangebracht in de gegevensbronconnectors voor de release 2024.4.0:

### Verbind met Salsify, Akeneo, en Microsoft Azure DevOps Boards (ADO) gegevensbronnen

Naast de bestaande out-of-the-box connectors biedt Experience Manager Guides ook connectors voor Salsify-, Akeneo- en Microsoft Azure DevOps Boards (ADO)-gegevensbronnen. Als beheerder kunt u deze connectors downloaden en installeren. Dan, vorm de geïnstalleerde schakelaars.

### Kopieer en plak de voorbeeldquery om een inhoudsfragment of onderwerp te maken

U kunt een vraag van steekproefgegevens in de generator gemakkelijk kopiëren en kleven om een inhoudsfragment of een onderwerp tot stand te brengen. Met deze eigenschap, moet u niet de syntaxis herinneren of een vraag manueel creëren. In plaats van de vraag manueel te typen, kunt u een steekproefvraag kopiëren en kleven, het uitgeven, en het gebruiken om de gegevens volgens uw vereisten te halen.

![&#x200B; neem de dialoogdoos van het inhoudsfragment op &#x200B;](assets/insert-content-snippet.png){width="800" align="left"}

*Exemplaar en geef een steekproefvraag uit om het inhoudsfragment tot stand te brengen.*

### Verbinding maken met JSON-gegevensbestanden via een bestandsconnector


Nu, als beheerder, kunt u een JSON dossierschakelaar vormen om JSON- gegevensdossiers als gegevensbron te gebruiken. Gebruik de connector om de JSON-bestanden van uw computer of de Adobe Experience Manager Assets te importeren. Vervolgens kunt u als auteur met behulp van de generatoren inhoudsfragmenten of onderwerpen maken.

Met deze functie kunt u de gegevens die in uw JSON-bestanden zijn opgeslagen, gebruiken en opnieuw gebruiken in verschillende fragmenten. De inhoud wordt ook dynamisch bijgewerkt wanneer u de JSON-bestanden bijwerkt.

### Vorm veelvoudige middel URLs voor een schakelaar om inhoudsfragmenten of onderwerpen te creëren

Als beheerder, kunt u veelvoudige middel URLs voor sommige schakelaars zoals de Generische Cliënt van de REST, Salsify, Akeneo, en Microsoft Azure DevOps Boards (ADO) vormen.

Dan, als auteur, verbind met de gegevensbronnen om inhoudsfragmenten of onderwerpen tot stand te brengen gebruikend de generators. Deze functie is handig omdat u geen gegevensbron hoeft te maken voor elke URL. Het helpt u om gegevens van om het even welke middelen voor een bepaalde gegevensbron in één enkel inhoudsfragment of onderwerp snel te halen.

Bekijk meer details over de gegevensbronschakelaars en hoe te [&#x200B; een gegevensbronschakelaar van het gebruikersinterface &#x200B;](../cs-install-guide/conf-data-source-connector-tools.md) vormen.

Leer hoe te [&#x200B; gegevens van uw gegevensbron &#x200B;](../user-guide/web-editor-content-snippet.md) gebruiken.

## Pas uw ervaring van de Redacteur van het Web met nieuwe UI van gebruikersvoorkeur aan

Het **de dialoogvakje van de Voorkeur van de Gebruiker** in de Redacteur van het Web omvat nu een nieuwe **Verschijning** tabel. Dit nieuwe lusje staat u toe om de gemeenschappelijkste blik-en-voelen voorkeur in de interface van de Redacteur van het Web gemakkelijk te vormen.

U kunt configureren om de bestanden op titel of bestandsnaam weer te geven en het thema van de toepassing en de bronweergave te wijzigen. Het helpt u ook de montages vormen om van een open dossier in de bewaarplaatmening de plaats te bepalen en de vaste ruimten te behandelen.

![&#x200B; vormgevingslusje van gebruikersvoorkeur &#x200B;](assets/user_preference_editor_appearance.png){width="550" align="left"}

*pas de verschijning volgens uw voorkeur aan.*

Leer meer over de **eigenschapbeschrijving van de voorkeur van de Gebruiker** &lbrace;in de [&#x200B; Linkerpaneel &#x200B;](../user-guide/web-editor-features.md#id2051EA0M0HS) sectie.

## Een geopend bestand zoeken in de dataweergave van de webeditor

Selecteer **altijd van dossiers in de bewaarplaats** optie in de **Voorkeur van de Gebruiker** de plaats bepalen om van uw dossier in de bewaarplaats snel te navigeren en de plaats te bepalen. Je hoeft er niet handmatig naar te zoeken.

Met deze functie kunt u tijdens het bewerken de locatie van het bestand gemakkelijk weergeven in de hiërarchie van opslagruimten.

Voor meer details, bepaal de plaats van mening [&#x200B; van een open dossier in de bewaarnemermening &#x200B;](../user-guide/web-editor-edit-topics.md#locate-an-open-file-in-the-repository-view).


## Verbeterde verwerking van vaste spaties in de webeditor

Met Experience Manager Guides kunt u een vaste-spatie-indicator weergeven tijdens het bewerken van documenten in de webeditor. Het verbetert ook de behandeling van vaste ruimten.
Het zet veelvoudige opeenvolgende witte ruimten in één enkele ruimte om om de mening WYSIWYG van het document in de Redacteur van het Web te bewaren. Deze functie draagt ook bij tot een betere algemene vormgeving en professionaliteit van het document.


Voor meer details, bekijk de [&#x200B; andere eigenschappen van de Redacteur van het Web &#x200B;](../user-guide/web-editor-other-features.md).




## Nabewerking voor selectieve mappen op Adobe Experience Manager Assets uitschakelen


Als beheerder kunt u de nabewerking en het genereren van UUID&#39;s voor selectieve mappen op Experience Manager Assets nu uitschakelen. Deze configuratie kan handig zijn, vooral wanneer u werkt met veel elementen of complexe mapstructuren. Bovendien kunnen meerdere gebruikers de elementen snel tegelijk uploaden zonder elkaar te storen.  

Als naverwerking voor een map wordt uitgeschakeld, heeft dit ook invloed op alle onderliggende mappen. Experience Manager Guides biedt nu echter de mogelijkheid om nabewerking selectief in te schakelen voor afzonderlijke onderliggende mappen in de genegeerde map.

Leer hoe te [&#x200B; postprocessing voor een omslag &#x200B;](../cs-install-guide/conf-folder-post-processing.md) onbruikbaar maken.

## Nieuwe ervaring voor het zoeken en filteren van bestanden in de dataweergave

Nu hebt u een verbeterde ervaring bij het filteren van bestanden. De vernieuwde functionaliteit voor het filteren van bestanden biedt een verbeterde manier om bestanden moeiteloos te doorzoeken en door te bladeren.


![&#x200B; onderzoeksdossiers in bewaarplaatmening &#x200B;](assets/repository-filter-search-2404.png){width="300" align="left"}

*Onderzoek naar de dossiers die de tekst bevatten`general purpose.`*

Geniet van voordelen zoals snellere toegang tot relevante bestanden en een intuïtievere gebruikersinterface, waardoor uw zoekervaring vloeiender en efficiënter wordt.

![&#x200B; snel zoekfilter &#x200B;](assets/repository-filter-search-quick.png) {width="300" align="left"}

*gebruik de snelle filters om naar DITA en niet-DITA dossiers te zoeken.*

Leer meer over de **eigenschap van het Onderzoek van de Filter** in de [&#x200B; Linkerpaneel &#x200B;](../user-guide/web-editor-features.md#id2051EA0M0HS) sectie.

## Gesegregeerde lijst om geldige elementen weer te geven en in te voegen volgens hun positie

Terwijl het uitgeven van een document in de Redacteur van het Web, kunt u een gescheiden lijst van elementen nu bekijken die bij de huidige plaats en buiten de huidige plaats geldig zijn. Op basis van uw vereisten kiest u een element uit de volgende opties:

* **Geldige elementen bij de huidige plaats** die u bij de huidige cursorplaats zelf kunt opnemen.
* **Geldige elementen buiten de huidige plaats** die u na om het even welke ouders voor het huidige element binnen de elementenhiërarchie kunt opnemen.

![&#x200B; het elementendialoog van het Tussenvoegsel &#x200B;](assets/insert-element-dialog.png){width="300" align="left"}

*Mening de gescheiden lijsten van geldige elementen om een element bij de huidige plaats op te nemen.*


Deze gesplitste lijst met geldige elementen helpt u de inhoudsstructuur te behouden en de DITA-standaarden te volgen.

Leer meer over de **eigenschap van het Element van het Tussenvoegsel** in de [&#x200B; Secundaire toolbar &#x200B;](../user-guide/web-editor-features.md#2051ea0j0y4) sectie.


## Inhoudseigenschappen Type wordt weergegeven als een vervolgkeuzemenu

Nu, verschijnt het Type van Eigenschappen van de Inhoud **&#x200B;**&#x200B;als dropdown menu. In het vervolgkeuzemenu kunt u de tags van de volledige hiërarchie voor de huidige tag weergeven en selecteren.

Met dit vervolgkeuzemenu hebt u snel toegang tot de relevante tags binnen de hiërarchische structuur.


![&#x200B; type dropdown menu in inhoudseigenschappen &#x200B;](assets/content-properties-type.png){width="300" align="left"}

*selecteer een markering van de hiërarchie voor de huidige markering.*

Leer meer over de **eigenschap van de Eigenschappen van de Inhoud** in de [&#x200B; Juiste 3&rbrace; sectie van het Comité.](../user-guide/web-editor-features.md#id2051eb003yk)



## Verbeterde prestaties tijdens het bulksgewijs controleren van bestanden in de Kaarteditor

Experience Manager Guides verbetert de prestaties en ervaring van de functie Inchecken van grote bestanden in de Kaarteditor. Deze verbetering helpt u de dossiers in bulk sneller controleren.
U kunt de vooruitgang van de controle-binnen verrichting voor de dossiers van **ook bekijken sparen als Nieuwe Versie en ontgrendelen** dialoogdoos. Tot slot verschijnt het succesbericht nadat de bewerking is voltooid en zijn alle geselecteerde uitgecheckte bestanden ingecheckt.

![&#x200B; sparen als nieuwe versie en open dialoogdoos &#x200B;](./assets/save-version-lock.png){width="300" align="left"}

*Mening de lijst en de status van de dossiers die in bulk van de Redacteur van de Kaart worden gecontroleerd.*

Leer hoe te [&#x200B; werken met de Geavanceerde Redacteur van de Kaart &#x200B;](../user-guide/map-editor-advanced-map-editor.md)

## Download het tijdelijke bestand terwijl u de uitvoer genereert via DITA-OT

U kunt de tijdelijke bestanden ook downloaden die zijn gegenereerd wanneer u de uitvoer van de AEM Site, HTML, Aangepast, JSON of PDF publiceert via DITA-OT. Met deze functie kunt u eventuele problemen analyseren die zich tijdens het genereren van de uitvoer kunnen voordoen en effectief problemen oplossen.  
U kunt het bestand metadata.xml ook downloaden als u eigenschappen van metagegevens hebt geselecteerd die zijn doorgegeven aan de uitvoer die is gegenereerd met DITA-OT. 

Voor meer details over vooraf instelt, mening [&#x200B; Begrijpend de output stelt &#x200B;](../user-guide/generate-output-understand-presets.md) vooraf in.


## IMS JWT-referenties vervangen door IMS OAuth-referenties voor op microservice gebaseerde publicaties


De geloofsbrieven van de Rekening van de Dienst (JWT) zijn afgekeurd ten gunste van de **Server-aan-Server** geloofsbrieven. Uw toepassingen die gebruikmaken van de JWT-referenties (Service Account) werken niet meer na 1 januari 2025. U moet vóór 1 januari 2025 naar de nieuwe referentie migreren om ervoor te zorgen dat uw toepassing blijft werken.


De service voor publicatie in de cloud voor Experience Manager Guides wordt nu beveiligd door verificatie op basis van Adobe IMS OAuth. Leer hoe te [&#x200B; op microservice-gebaseerde het publiceren met authentificatie OAuth &#x200B;](../knowledge-base/publishing/configure-microservices-imt-config.md) vormen.
