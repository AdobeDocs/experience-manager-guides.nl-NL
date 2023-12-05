---
title: Opmerkingen bij de release | Nieuwe functies in Adobe Experience Manager-hulplijnen, release van juni 2023
description: Leer de nieuwe en verbeterde functies van de as a Cloud Service Adobe Experience Manager-hulplijnen in juni 2023
exl-id: 625f9702-2b91-4622-9fec-282f47f1d7a6
source-git-commit: 5e0584f1bf0216b8b00f00b9fe46fa682c244e08
workflow-type: tm+mt
source-wordcount: '1212'
ht-degree: 0%

---

# Nieuwe functies in juni 2023 as a Cloud Service Adobe Experience Manager-hulplijnen

Dit artikel heeft betrekking op de nieuwe en verbeterde functies in versie juni 2023 van Adobe Experience Manager-hulplijnen (later aangeduid als *Hulplijnen AEM as a Cloud Service*).

Voor meer informatie over de upgrade-instructies, compatibiliteitsmatrix en de problemen die in deze release zijn opgelost, raadpleegt u [Opmerkingen bij de release](release-notes-2023.6.0.md).

## Verbroken rapport van Verbindingen in de Redacteur van het Web

AEM Gidsen staat u toe om de algemene volledigheid van uw technische documenten te controleren en rapporten van de Redacteur van het Web te produceren. In juni 2023 biedt de release AEM hulplijnen u nu de functie om verbroken koppelingen weer te geven en te herstellen. Dit is een handig rapport waarmee u verbroken koppelingen kunt beheren. U kunt de verbroken verbindingen gemakkelijk bekijken aanwezig in uw kaart DITA en hen ook bevestigen.
![](assets/broken-link-report.png){width="800" align="left"}

Als u een koppeling hebt hersteld, wordt deze niet weergegeven onder de lijst met verbroken koppelingen.

Zie voor meer informatie [verbroken koppelingen weergeven en corrigeren](../user-guide/reports-web-editor.md#report-broken-links).

## Bestanden hernoemen en verplaatsen in de weergave Opslagplaats

U kunt nu ook de naam van een bestand wijzigen of een bestand uit het deelvenster Opslagruimte verplaatsen. Deze functie is handig en helpt uw bestanden eenvoudig te beheren vanuit het deelvenster Opslag. U kunt een bestand selecteren en de naam ervan wijzigen of de naam ervan wijzigen met de **Opties** voor het geselecteerde bestand. AEM hulplijnen geven een bericht van slagen weer wanneer u een bestand verplaatst of de naam ervan wijzigt.

![](assets/rename-move-assets.png){width="650" align="left"}

Zie voor meer informatie over het menu Opties van een bestand de knop **Weergave opslagplaats** functiebeschrijving in het dialoogvenster [Linkerdeelvenster](../user-guide/web-editor-features.md#id2051EA0M0HS) sectie.

## Native PDF-verbeteringen

### Een watermerk toevoegen aan de PDF-uitvoer voor conceptdocumenten

Nu kunt u een watermerk toevoegen aan de PDF-uitvoer van het document dat nog niet is goedgekeurd. Dit watermerk wordt niet weergegeven als u de PDF voor het document genereert in de documentstatus &quot;Goedgekeurd&quot;. U kunt bijvoorbeeld een watermerk Concept toevoegen voor uw PDF-uitvoer.

Zie voor meer informatie [Een watermerk toevoegen aan de PDF-uitvoer voor conceptdocumenten](../native-pdf/use-javascript-content-style.md#watermark-draft-document).

### Ondersteuning voor taalvariabelen

AEM hulplijnen bieden ondersteuning voor taalvariabelen. U kunt taalvariabelen gebruiken om een gelokaliseerde versie van de uit-van-de-doos etiketten zoals Nota, Voorzichtigheid, en Waarschuwing of statische tekst in de output van PDF te bepalen.
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

Voor meer informatie, bekijkt u [Ondersteuning voor taalvariabelen](../native-pdf/native-pdf-language-variables.md).

### Mogelijkheid om AEM metagegevens te gebruiken in PDF-lay-outs

Metagegevens zijn de beschrijving of definitie van de inhoud. Deze metagegevens worden opgeslagen in de DITA-bronkaartinhoud.

In AEM hulplijnen kunt u ook de eigenschappen van de metagegevens van uw elementen selecteren en deze aan de pagina-indeling toevoegen. Vervolgens worden deze metagegevenseigenschappen van uw elementen door AEM hulplijnen geselecteerd en in de PDF-uitvoer gepubliceerd.


![](assets/native-pdf-metadata-asset.png){width="550" align="left"}

>[!NOTE]
>
> AEM de Gidsen steunen ook de meta-gegevenseigenschappen voor uw kaarten DITA.

Zie voor meer informatie [Velden en metagegevens toevoegen](../native-pdf/design-page-layout.md#add-fields-metadata).


## Verbeteringen aan schema

### Gebruik rapportinstructies om te controleren op regels in Schematron

AEM Guides steunt nu ook de verklaringen in het verslag met de Schematron. Een rapportverklaring produceert een bericht wanneer een testverklaring aan waar evalueert. Als u bijvoorbeeld wilt dat de korte beschrijving uit maximaal 150 tekens bestaat, kunt u een rapportinstructie definiëren om de onderwerpen te controleren waarvoor de korte beschrijving uit meer dan 150 tekens bestaat.

Zie voor meer informatie [Instructies voor bevestigen en rapporteren gebruiken om op regels te controleren](../user-guide/support-schematron-file.md#schematron-assert-report).

### Regex-expressies gebruiken

U kunt Regex-expressies ook gebruiken om een regel met de functie match() te definiëren en vervolgens validatie uit te voeren met het Schematron-bestand.

Zie voor meer informatie [Regex-expressies gebruiken](../user-guide/support-schematron-file.md#schematron-assert-report).


### abstracte patronen definiëren

AEM Hulplijnen ondersteunen ook abstracte patronen in Schematron. U kunt generische abstracte patronen definiëren en deze abstracte patronen opnieuw gebruiken. Abstracte patronen kunnen uw Schematron-schema vereenvoudigen en u helpen uw validatielogica te beheren en bij te werken.


Zie voor meer informatie [abstracte patronen definiëren](../user-guide/support-schematron-file.md#schematron-abstract-patterns).

## Navigeer van de Redacteur van het Web aan de AEM homepage

Nu kunt u gemakkelijk van de Redacteur van het Web aan de AEM Homepage navigeren.

![](assets/web-editor-launch-page.png){width="800" align="left"}

* Klik op de knop **Hulplijnen** icon (![](assets/aem-guides-icon.png) ), om terug te gaan naar de AEM navigatiepagina.


Zie voor meer informatie [Navigatiepagina AEM](../user-guide/web-editor-launch-editor.md#id2056BG00RZJ).

## De hiërarchische definities van onderwerpdefinities en opsommingen verwerken

AEM Hulplijnen beschikken over de krachtige functie om onderwerpschemakaarten te maken. Dit zijn gespecialiseerde DITA-kaarten die worden gebruikt om taxonomische onderwerpen en gecontroleerde waarden te definiëren. AEM Hulplijnen kunt u nu ook de onderwerpdefinitie definiëren in een kaart en de opsommingsdefinities in een andere kaart. Vervolgens kunt u de kaartverwijzing toevoegen en het onderwerpschema gebruiken.
De verwijzingen naar onderwerpopsommingen worden opgelost in dezelfde kaart of in de kaart waarnaar wordt verwezen.

Zie voor meer informatie over de verwerking van hiërarchische definities van onderwerpdefinities en opsommingen de **Onderwerpregeling** functiebeschrijving in het dialoogvenster [Linkerdeelvenster](../user-guide/web-editor-features.md#id2051EA0M0HS) sectie.

## Ondersteuning voor XLIFF-indeling in vertaling

AEM Hulplijnen bieden ook ondersteuning voor de XLIFF-indeling (XML Localization Interchange File Format) bij het vertalen. U kunt nu ook kiezen voor **Nieuw XLIFF-vertaalproject maken** om de XML-inhoud om te zetten in de XLIFF-indeling.
Met deze indeling kunt u de inhoud exporteren naar de industriestandaard XLIFF-indeling en deze indeling vervolgens aan de vertaalbureaus aanbieden. Zie voor meer informatie [Een vertaalproject maken](../user-guide/translate-documents-web-editor.md#create-translation-project).

![](assets/translation-project-types.png){width="350" align="left"}



## Verbeterd deelvenster Favorieten

Met AEM hulplijnen kunt u een verzameling of favoriete lijst met bestanden en mappen maken en deze gemakkelijk gebruiken. Nu **Opties** is ook beschikbaar in het dialoogvenster **Favorieten** deelvenster. U kunt de naam van de geselecteerde verzameling wijzigen of deze verwijderen uit het dialoogvenster **Opties** -menu. U kunt de **Vernieuwen** om een nieuwe lijst met bestanden of mappen op te halen uit de opslagplaats. U kunt de inhoud van de map ook weergeven in de interface Middelen.

![](assets/favorites-options.png){width="650" align="left"}

>[!NOTE]
>
> U kunt de lijst ook vernieuwen met de opdracht **Vernieuwen** bovenaan.

Voor meer informatie over de **Opties** menu van een inzameling van Favorieten, zie **Favorieten** functiebeschrijving in het dialoogvenster [Linkerdeelvenster](../user-guide/web-editor-features.md#id2051EA0M0HS) sectie.

## Overschakelen naar het systeemthema

U kunt nu ook het apparaatthema gebruiken. Met de **Gebruikersvoorkeuren** kunt u AEM hulplijnen configureren om automatisch te schakelen tussen lichte en donkere thema&#39;s op basis van het thema van uw apparaat.

![](assets/device-theme-user-preferences.png){width="550" align="left"}

Zie voor meer informatie de **Gebruikersvoorkeuren** functiebeschrijving in het dialoogvenster [Hoofdwerkbalk](../user-guide/web-editor-features.md#id2051EA0G05Z) sectie.
