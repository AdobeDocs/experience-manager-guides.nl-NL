---
title: Systeemeigen PDF | Variabelen gebruiken in de PDF-uitvoer
description: Variabelen gebruiken in de uitvoer- en uitvoersjablonen van PDF
feature: Output Generation
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '1446'
ht-degree: 0%

---

# Variabelen in de PDF-uitvoer

Een variabele is een naam-waardepaar met gegevens dat dient als herbruikbare informatie. Hierdoor is je inhoud draagbaar en gemakkelijk bij te werken. Wanneer u een variabele of de waarde ervan wijzigt, wordt elke instantie van die variabele of waarde bijgewerkt.



## Een nieuwe variabele maken

Voer de volgende stappen uit om een variabele te maken:

![Een nieuwe variabele maken](assets/add-variable-default.png){width="800" align="left"}

*Maak variabelen en definieer waarden voor deze variabelen.*


1. Ga in de webeditor naar de **Uitvoer** tab.
1. Selecteren **Variabelen** <img alt= "variabele, pictogram" src="./assets/variables-icon.svg" width="25"> in het linkerdeelvenster.
1. Selecteren **Bewerken** <img alt= "Pictogram Potlood bewerken" src="./assets/edit_pencil_icon.svg" width="25"> om de **Variabelen** editor.
De variabelen worden in alfabetische volgorde vermeld.
1. Voer de naam van de variabele in het dialoogvenster **Naam** en de waarde ervan in het dialoogvenster **Waarde** kolom.
   >[!TIP]
   >
   >U kunt elke HTML-inhoud als een variabelewaarde gebruiken om de variabelewaarde in specifieke opmaak weer te geven. U kunt bijvoorbeeld een `<b>` -tag naar de variabelewaarde om de waarde weer te geven **Hulplijnen Experience Manager** vetgedrukt. U kunt ook afbeeldingen uit de gegevensopslagruimte als waarden toevoegen.

1. Selecteren **Variabele toevoegen** <img alt= "Pictogram toevoegen" src="./assets/add-icon.svg" width="25"> een nieuwe variabele toevoegen. U kunt geen variabele maken met dezelfde naam als een bestaande variabele. Er wordt een fout weergegeven.

   >[!NOTE]
   >
   >Als u **Variabele toevoegen** <img alt= "Pictogram toevoegen" src="./assets/add-icon.svg" width="25">, wordt de variabele niet gemaakt en toegevoegd aan de lijst.

Op deze manier kunt u variabelen met standaardwaarden maken. Bijvoorbeeld:
* ProductName: Experience Manager Guides
* VersionNumber: 2300
* Releasedatum: 01-01-2023


### Een variabele bewerken

U kunt een variabele op twee manieren bewerken:

**Vanuit het deelvenster Variabelen aan de linkerkant**

1. Selecteer een variabele in het dialoogvenster **Variabelen** deelvenster.
1. Houd de muisaanwijzer boven de variabele om de **Opties** en selecteert u vervolgens de **Bewerken** -optie.
1. In de **Variabele bewerken** kunt u de standaardwaarde van de geselecteerde variabele bewerken.
1. Klikken **Gereed**.

**Vanuit de editor Variabelen**

1. Selecteren **Variabelen** <img alt= "variabele, pictogram" src="./assets/variables-icon.svg" width="25"> in het linkerdeelvenster.
1. Bewerken **selecteren** <img alt= "Pictogram Potlood bewerken" src="./assets/edit_pencil_icon.svg" width="25"> om de **Variabelen-editor** te openen.

1. In de **variabeleneditor** kunt u de waarde van de geselecteerde variabele bewerken.

U moet alle wijzigingen die u via de **Variabelen-editor** aanbrengt, opslaan om deze weer te geven in het **deelvenster Variabelen** aan de linkerkant.

>[!NOTE]
>
> Als u de waarde van een variabele bewerkt, worden alle verwijzingen in de Adobe Experience Manager-handleidingen bijgewerkt wanneer dat van toepassing is.

### Een variabele zoeken en voorvertonen

U kunt de waarde van een variabele zoeken en voorvertonen. Geef een tekenreeks op in het zoekvak van het dialoogvenster **Variabelen** deelvenster. Zowel op basis van de naam van de variabele als op basis van de waarde wordt gezocht.
U kunt een variabele op twee manieren voorvertonen:

In de voorvertoning van de variabele wordt de standaardwaarde weergegeven. Als u bijvoorbeeld de standaardwaarde van de variabele ProductName hebt gedefinieerd als &quot;Adobe Experience Manager Guides&quot;, wordt deze waarde in de voorvertoning weergegeven.

**Vanuit het deelvenster Variabelen aan de linkerkant**


1. Selecteer een variabele in het dialoogvenster **Variabelen** deelvenster.
1. Houd de muisaanwijzer boven de variabele om de **Opties** en selecteert u vervolgens de **Voorvertoning** -optie.

![variabele voorvertoning vanuit het deelvenster Variabelen](assets/variables-panel-preview-default.png){width="550" align="left"}

*Geef een voorvertoning van de standaardwaarde voor een variabele weer.*

**Vanuit de editor Variabelen**

1. Houd de muisaanwijzer boven de variabele in de lijst om de **Opties** -menu.
1. Selecteren **Voorvertoning**.




### Een variabele dupliceren

U kunt een variabele dupliceren en de waarde aan uw wensen aanpassen.


1. Plaats de muisaanwijzer op de variabele in de lijst om het **menu Opties weer te geven** .
1. Selecteer **Dupliceren**.

De standaardnaam van de variabele is `<selected variable name>` (zoals &quot;monster&quot;). U kunt de naam naar wens wijzigen.

### Een variabele verwijderen

U kunt een variabele op twee manieren verwijderen:

**Vanuit het deelvenster Variabelen aan de linkerkant**

1. Selecteer een variabele in het dialoogvenster **Variabelen** deelvenster.
1. Houd de muisaanwijzer boven de variabele om de **Opties** en selecteert u vervolgens de **Verwijderen** -optie.

**Vanuit de editor Variabelen**

1. Houd de muisaanwijzer boven de variabele in de lijst om de **Opties** -menu.
1. Selecteren **Verwijderen** -optie.

De variabele wordt verwijderd uit alle sets met variabelen.

## Variabelesets voor uitvoervoorinstellingen

Adobe Experience Manager-handleidingen biedt ook ondersteuning voor variabelensets, waarmee u alternatieve waarden kunt toewijzen aan uw variabelen. Een onderneming kan bijvoorbeeld twee producten, A en B, verkopen. Het heeft verschillende specificaties voor elk van hen. Hieronder vallen onder andere de productnaam, het versienummer en de releasedatum. Er kunnen andere verschillen in branding zijn. Met behulp van variabele sets definieert u een andere set waarden voor de variabelen. Wanneer u de uitvoer genereert, kiest u de juiste variabele en produceert u de vereiste uitvoer.

### Variabele-sets configureren

U moet veranderlijke reeksen vormen alvorens om het even welke variabelen aan hen toe te voegen.



1. Selecteren **Instellingen** <img alt= "Instellingenpictogram" src="./assets/settings-icon.svg" width="25"> om de **Variabele-sets configureren** in.
   ![variabele set configureren](assets/configure-variable-set.png){width="550" align="left"}
1. Voer de naam van de variabeleset in het dialoogvenster **Naam** kolom.
1. Selecteren **Variabele toevoegen** <img alt= "Pictogram toevoegen" src="./assets/add-icon.svg" width="25"> om een nieuwe set variabelen toe te voegen. De variabelesets worden in alfabetische volgorde weergegeven.
1. U kunt **Verwijderen** om een variabele te verwijderen.

### Variabele-setbewerkingen

Alle variabelesets hebben dezelfde variabelen maar kunnen verschillende waarden hebben.

U kunt de waarden voor een specifieke set variabelen weergeven, bewerken en voorvertonen. Selecteer een variabeleset in het menu **Variabele-sets** vervolgkeuzelijst. De waarden worden weergegeven volgens de gekozen set variabelen.
Wanneer u de waarden voor de variabelen in specifieke variabelesets bewerkt, worden de standaardwaarden genegeerd en worden de waarden van de geselecteerde variabeleset gewijzigd.
U kunt bijvoorbeeld de volgende waarden instellen voor de sets met variabelen: *Adobe-set1* en *Adobe-set2* .


**Variabele set 1**: *Adobe-set1*

* ProductName: ProductA
* Versienummer: 2311
* Releasedatum: 02-11-2023


**Variabele set 2**: *Adobe-set2*

* ProductName: ProductB
* Versienummer: 2310
* Releasedatum: 09-07-2023

Elke nieuwe variabele wordt toegevoegd aan alle veranderlijke reeksen. Wanneer u een variabele verwijdert of dupliceert, wordt deze bijgewerkt voor alle variabelesets.

U kunt ook een voorvertoning van de waarden voor een variabeleset weergeven.
Bijvoorbeeld voor de set met variabelen *Adobe-Set1*, hebt u de waarde van de variabele ProductName als &quot;ProductA&quot;bepaald, dan toont het deze waarde in de voorproef in de redacteur van Variabelen.

![variabele voorvertoning in de Variables-editor](assets/variables-editor-preview.png){width="550" align="left"}

*Geef een voorvertoning weer van de waarde die u in de geselecteerde set variabelen hebt gedefinieerd.*

### De waarde van een variabele opnieuw instellen

Als u de waarde hebt bewerkt, kunt u ook de standaardwaarde van een variabele herstellen.
Herstellen <img alt= "herstelpictogram" src="./assets/application-variable-revert.svg" width="25"> wordt weergegeven voor een variabele met een gewijzigde waarde.
U kunt bijvoorbeeld de waarde voor de variabele ProductName terugzetten op de standaardwaarde in de Hulplijnen van de Professionele Manager.

## Variabelen gebruiken in de sjablonen Native PDF

U kunt variabelen toevoegen terwijl u de uitvoer van uw productdocumenten genereert, zodat deze gemakkelijk kunnen worden bijgewerkt en overdraagbaar zijn. U kunt deze variabelen invoegen in de pagina-indeling die op de verschillende pagina&#39;s in uw documenten wordt weergegeven. U kunt bijvoorbeeld de variabele ProductName toevoegen die wordt weergegeven in het koptekstgebied van de paginalay-out (of een ander deel zoals de voettekst of de tekst).



Voer de volgende stappen uit om een variabele zoals uw ProductName in het koptekstgebied in te voegen:
1. Open de vereiste pagina-indeling voor bewerking.

   >[!NOTE]
   >
   > Weergave [Een pagina-indeling aanpassen](../native-pdf/components-pdf-template.md#customize-a-page-layout-customize-page-layout) voor het openen van een pagina-indeling voor aanpassen of bewerken.

1. Selecteer de koptekst om deze actief te maken en een variabele in te voegen.

1. U kunt de variabele op twee manieren invoegen:

   **In het deelvenster Variabelen aan de linkerkant**

   * Sleep een variabele vanuit het **deelvenster Variabelen** naar het kopgebied.

   **Vanaf de werkbalk**

   1. Selecteren **Variabele/velden invoegen** <img alt= "variabele, pictogram" src="./assets/variables-icon.svg" width="25">.
   1. In de **Variabele** selecteert u de naam van de variabele die u in het koptekstgebied wilt invoegen.
   1. U kunt ook de zoektekenreeks in het tekstvak invoeren. De namen van variabelen die de opgegeven tekenreeks bevatten, worden gefilterd en in de lijst weergegeven. De geselecteerde variabele wordt ingevoegd in het koptekstgebied. U kunt de standaardwaarde van de variabele weergeven.
   1. Als u een variabele wilt vervangen, dubbelklikt u op de waarde van de variabele en selecteert u een andere variabele in het menu **Variabele** in. De variabele wordt vervangen.


## PDF-uitvoer genereren met variabelen

U kunt de uitvoer van de PDF genereren met de waarden van verschillende variabelen. Voordat u de layout genereert, kiest u een variabele uit een uitvoervoorinstelling **Set variabelen** vervolgkeuzelijst om de waarden ervan te kiezen.

![dropdown voor variabele set](assets/output-preset-variable-dropdown.png){width="550" align="left"}

*Selecteer een variabelenset in het vervolgkeuzemenu van de uitvoervoorinstelling die u wilt gebruiken om de PDF-uitvoer te genereren.*

>[!NOTE]
>
> U kunt ook (Standaard) in het vervolgkeuzemenu selecteren om de standaardwaarden voor alle variabelen te publiceren.

Afhankelijk van de gekozen set met variabelen, krijgt u een uitvoer die overeenkomt met de waarden van variabelen die in de set met variabelen zijn gedefinieerd. Als u bijvoorbeeld de set met variabelen selecteert *Adobe-set1* In de uitvoer worden de waarden van de variabelen weergegeven zoals die in deze set zijn gedefinieerd.


<img src="assets/variable-pdf-output.png" alt="PDF uitvoer met variabelen" width="500" border="2px">

*Genereer de PDF-uitvoer met behulp van variabelen in de paginalay-out.*

U kunt de waarden voor elke variabele die u hebt ingesteld, ook snel bijwerken wanneer dat nodig is en de uitvoer opnieuw genereren. Als u bijvoorbeeld de details voor een versie moet bijwerken, kunt u de waarde van de versie bijwerken in de variabele VersionNumber en de uitvoer opnieuw genereren.


