---
title: Opmerkingen bij de release | Nieuwe functies in Adobe Experience Manager Guides, release juni 2023
description: Leer de nieuwe en verbeterde functies in de release van Adobe Experience Manager Guides as a Cloud Service van juni 2023
exl-id: 625f9702-2b91-4622-9fec-282f47f1d7a6
feature: What's New
role: Leader
source-git-commit: 6d8c01f20f7b59fed92c404561b647d9ebecb050
workflow-type: tm+mt
source-wordcount: '1212'
ht-degree: 0%

---

# Nieuwe functies in juni 2023 in Adobe Experience Manager Guides as a Cloud Service

Dit artikel behandelt de nieuwe en verbeterde eigenschappen in versie Juni 2023 van Adobe Experience Manager Guides (later genoemd als *as a Cloud Service van AEM Guides*).

Voor meer details op de verbeteringsinstructies, verenigbaarheidsmatrijs, en de kwesties die in deze versie worden bevestigd, zie [ de nota&#39;s van de Versie ](release-notes-2023-6-0.md).

## Verbroken rapport van Verbindingen in de Redacteur van het Web

AEM Guides staat u toe om de algemene volledigheid van uw technische documenten te controleren en rapporten van de Redacteur van het Web te produceren. Nu biedt AEM Guides in juni 2023 de functie om verbroken koppelingen weer te geven en te herstellen. Dit is een handig rapport waarmee u verbroken koppelingen kunt beheren. U kunt de verbroken verbindingen gemakkelijk bekijken aanwezig in uw kaart DITA en hen ook bevestigen.
![](assets/broken-link-report.png){width="800" align="left"}

Als u een koppeling hebt hersteld, wordt deze niet weergegeven onder de lijst met verbroken koppelingen.

Voor meer details, zie [ Mening en moeilijke situatie gebroken verbindingen ](../user-guide/reports-web-editor.md#report-broken-links).

## Bestanden hernoemen en verplaatsen in de weergave Opslagplaats

U kunt nu ook de naam van een bestand wijzigen of een bestand uit het deelvenster Opslagruimte verplaatsen. Deze functie is handig en helpt uw bestanden eenvoudig te beheren vanuit het deelvenster Opslag. U kunt een dossier selecteren en het anders noemen of bewegen gebruikend het **menu van Opties** voor het geselecteerde dossier. AEM Guides geeft een succesbericht weer wanneer u een bestand verplaatst of hernoemt.

![](assets/rename-move-assets.png){width="650" align="left"}

Voor meer details op het menu van Opties van een dossier, zie de **eigenschapbeschrijving van de mening van de Bewaarplaats** in de [ Linkerpaneel ](../user-guide/web-editor-features.md#id2051EA0M0HS) sectie.

## Native PDF-verbeteringen

### Een watermerk toevoegen aan de PDF-uitvoer voor conceptdocumenten

Nu kunt u een watermerk toevoegen aan de PDF-uitvoer van het document dat nog niet is goedgekeurd. Dit watermerk wordt niet weergegeven als u de PDF voor het document genereert in de documentstatus &#39;Goedgekeurd&#39;. U kunt bijvoorbeeld een watermerk Concept toevoegen voor uw PDF-uitvoer.

Voor meer details, zie [ een watermerk aan de output van de PDF voor ontwerpdocumenten ](../native-pdf/use-javascript-content-style.md#watermark-draft-document) toevoegen.

### Ondersteuning voor taalvariabelen

AEM Guides ondersteunt taalvariabelen. U kunt taalvariabelen gebruiken om een gelokaliseerde versie van de uit-van-de-doos etiketten zoals Nota, Voorzichtigheid, en Waarschuwing of statische tekst in de output van PDF te bepalen.
U kunt de taalvariabelen of de gelokaliseerde versie van de etiketten aan de aangewezen secties in uw output van PDF en in de outputmalplaatjes toevoegen.

#### Taalvariabelen in de PDF-uitvoer

U kunt de taalvariabelen gebruiken om gelokaliseerde etiketten voor elementen zoals Nota, Voorzichtigheid, en Waarschuwing te bepalen. U kunt de waarde voor deze variabelen bijwerken in een of meer talen en vervolgens wordt de gelokaliseerde waarde automatisch gekozen in de uitvoer van PDF.
U kunt bijvoorbeeld het label Notitie op de volgende manieren in uw PDF-uitvoer presenteren:

* Engels: Opmerking
* Frans: Opmerking
* Duits: Hinweis

#### Taalvariabelen in de uitvoersjablonen

Als u de PDF-uitvoer in verschillende talen wilt maken, moet u verschillende PDF-sjablonen maken die gelokaliseerde tekst voor elke taal bevatten. Nu met de eigenschap van taalvariabelen, moet u het malplaatje slechts eenmaal tot stand brengen. Vervolgens kunt u voor elke statische tekst die u wilt lokaliseren, overeenkomstige taalvariabelen maken en deze gebruiken in uw sjabloon.
U kunt taalvariabelen maken voor langere tekst, zoals een hele zin of zelfs een alinea. U kunt ook stijlen toepassen en markeringen voor HTML gebruiken om deze taalvariabelen op te maken.

Voor meer details, mening [ Steun voor taalvariabelen ](../native-pdf/native-pdf-language-variables.md).

### Mogelijkheid om AEM metagegevens te gebruiken in PDF-lay-outs

Metagegevens zijn de beschrijving of definitie van de inhoud. Deze metagegevens worden opgeslagen in de DITA-bronkaartinhoud.

Nu kunt u in AEM Guides ook de eigenschappen van metagegevens van uw elementen selecteren en deze toevoegen aan de pagina-indeling. Vervolgens kiest AEM Guides deze metagegevenseigenschappen van uw elementen en publiceert het deze in uw PDF-uitvoer.


![](assets/native-pdf-metadata-asset.png){width="550" align="left"}

>[!NOTE]
>
> AEM Guides ondersteunt ook de eigenschappen van metagegevens voor uw DITA-kaarten.

Voor meer details, zie [ gebieden en meta-gegevens ](../native-pdf/design-page-layout.md#add-fields-metadata) toevoegen.


## Verbeteringen aan schema

### Gebruik rapportinstructies om te controleren op regels in Schematron

AEM Guides steunt nu ook de verklaringen in het verslag met de Schematron. Een rapportverklaring produceert een bericht wanneer een testverklaring aan waar evalueert. Als u bijvoorbeeld wilt dat de korte beschrijving uit maximaal 150 tekens bestaat, kunt u een rapportinstructie definiëren om de onderwerpen te controleren waarvoor de korte beschrijving uit meer dan 150 tekens bestaat.

Voor meer details, zie [ Gebruik bevestiging en rapportverklaringen om regels ](../user-guide/support-schematron-file.md#schematron-assert-report) te controleren.

### Regex-expressies gebruiken

U kunt Regex-expressies ook gebruiken om een regel met de functie match() te definiëren en vervolgens validatie uit te voeren met het Schematron-bestand.

Voor meer details, zie [ uitdrukkingen Regex van het Gebruik ](../user-guide/support-schematron-file.md#schematron-assert-report).


### abstracte patronen definiëren

AEM Guides ondersteunt ook abstracte patronen in Schematron. U kunt generische abstracte patronen definiëren en deze abstracte patronen opnieuw gebruiken. Abstracte patronen kunnen uw Schematron-schema vereenvoudigen en u helpen uw validatielogica te beheren en bij te werken.


Voor meer details, zie [ abstracte patronen ](../user-guide/support-schematron-file.md#schematron-abstract-patterns) bepalen.

## Navigeer van de Redacteur van het Web aan de AEM homepage

Nu kunt u gemakkelijk van de Redacteur van het Web aan de AEM Homepage navigeren.

![](assets/web-editor-launch-page.png){width="800" align="left"}

* Klik het **pictogram van Gidsen** (![](assets/aem-guides-icon.png)), om terug naar de pagina van de Navigatie van de AEM te gaan.


Voor meer details, zie [ AEM de pagina van de Navigatie ](../user-guide/web-editor-launch-editor.md#id2056BG00RZJ).

## De hiërarchische definities van onderwerpdefinities en opsommingen verwerken

AEM Guides beschikt over de krachtige functie om onderwerpschemakaarten te maken die een gespecialiseerde vorm van DITA-kaarten zijn die worden gebruikt om taxonomische onderwerpen en gecontroleerde waarden te definiëren. Nu kunt u met AEM Guides ook de onderwerpdefinitie definiëren in een kaart en de opsommingsdefinities in een andere kaart. Vervolgens kunt u de kaartverwijzing toevoegen en het onderwerpschema gebruiken.
De verwijzingen naar onderwerpopsommingen worden opgelost in dezelfde kaart of in de kaart waarnaar wordt verwezen.

Voor meer details over de behandeling van hiërarchische definities van onderwerpdefinities en opsommingen, zie de **beschrijving van de onderwerpregeling** eigenschapbeschrijving in de [ Linkerpaneel ](../user-guide/web-editor-features.md#id2051EA0M0HS) sectie.

## Ondersteuning voor XLIFF-indeling in vertaling

AEM Guides biedt ook ondersteuning voor de XLIFF-indeling (XML Localization Interchange File Format) bij het vertalen. Nu kunt u ook verkiezen om **een nieuw XLIFF vertaalproject** tot stand te brengen om de inhoud van XML in het formaat om te zetten XLIFF.
Met deze indeling kunt u de inhoud exporteren naar de industriestandaard XLIFF-indeling en deze indeling vervolgens aan de vertaalbureaus aanbieden. Voor meer details, zie [ een vertaalproject ](../user-guide/translate-documents-web-editor.md#create-translation-project) creëren.

![](assets/translation-project-types.png){width="350" align="left"}



## Verbeterd deelvenster Favorieten

Met AEM Guides kunt u een verzameling of favoriete lijst met bestanden en mappen maken en deze gemakkelijk gebruiken. Nu **het menu van Opties** is ook beschikbaar in het **Favorieten** paneel. U kunt de geselecteerde inzameling anders noemen of het van het **menu van Opties** schrappen. U kunt **selecteren verfrist** optie om een nieuwe lijst van dossiers of omslagen van de bewaarplaats te krijgen. U kunt de inhoud van de map ook weergeven in de gebruikersinterface van Assets.

![](assets/favorites-options.png){width="650" align="left"}

>[!NOTE]
>
> U kunt de lijst ook verfrissen gebruikend **verfrissen** pictogram op de bovenkant.

Voor meer details op het **menu van Opties** van een inzameling van Favorieten, zie de **Favorieten** eigenschapbeschrijving in de [ Linkerpaneel ](../user-guide/web-editor-features.md#id2051EA0M0HS) sectie.

## Overschakelen naar het systeemthema

U kunt nu ook het apparaatthema gebruiken. Gebruikend de **Voorkeur van de Gebruiker**, kunt u AEM Guides vormen om tussen lichte en donkere thema&#39;s automatisch te schakelen die op het thema van uw apparaat worden gebaseerd.

![](assets/device-theme-user-preferences.png){width="550" align="left"}

Voor meer details, zie de **eigenschapbeschrijving van de Voorkeur van de Gebruiker 1} in de [ Belangrijkste toolbar ](../user-guide/web-editor-features.md#id2051EA0G05Z) sectie.**
