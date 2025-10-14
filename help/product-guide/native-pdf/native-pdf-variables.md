---
title: Oorspronkelijke PDF | Variabelen gebruiken in de PDF-uitvoer
description: Variabelen gebruiken in de PDF-uitvoer en -uitvoersjablonen
feature: Output Generation
role: Admin
level: Experienced
exl-id: 96e54aee-52df-4af1-97fd-34986f553be4
source-git-commit: 594248c42b14c960d858a2e0e6994aa9bb4acd4e
workflow-type: tm+mt
source-wordcount: '1450'
ht-degree: 0%

---

# Variabelen in de PDF-uitvoer

Een variabele is een naam-waardepaar van gegevens die als herbruikbare informatie dienen. Hierdoor kunt u uw inhoud draagbaar maken en eenvoudig bijwerken. Wanneer u een variabele of de bijbehorende waarde wijzigt, wordt elke instantie van die variabele of waarde bijgewerkt.

## Een nieuwe variabele maken

Voer de volgende stappen uit om een variabele te maken:

![&#x200B; creeer een nieuwe variabele &#x200B;](assets/add-variable-default.png){width="800" align="left"}

*creeer variabelen en bepaal waarden voor hen.*


1. Navigeer in de editor naar het linkerdeelvenster en selecteer **Variabelen** <img alt= "variabele, pictogram" src="./assets/variables-icon.svg" width="25">. Deze optie is beschikbaar onder de sectie Meer.
1. Selecteer **uitgeven** <img alt= "Het pictogram van het potlood bewerken" src="./assets/edit_pencil_icon.svg" width="25"> om de **Variabelen** redacteur te openen.
De variabelen worden in alfabetische volgorde weergegeven.
1. Ga de veranderlijke naam in de **kolom van de Naam** en zijn waarde in de **kolom van de Waarde** in.
   >[!TIP]
   >
   >U kunt alle HTML-inhoud gebruiken als variabele om de variabelewaarde in een specifieke opmaak weer te geven. U kunt bijvoorbeeld een `<b>` tag toevoegen aan de variabele waarde om de waarde **Experience Manager Guides** vetgedrukt weer te geven. U kunt ook afbeeldingen uit de opslagplaats als waarden toevoegen.

1. Selecteer **Variabele toevoegen** <img alt= "Pictogram toevoegen" src="./assets/add-icon.svg" width="25"> om een nieuwe variabele toe te voegen. U kunt geen variabele maken met dezelfde naam als een bestaande variabele. Er wordt een fout weergegeven.

   >[!NOTE]
   >
   >Als u niet **selecteert voeg veranderlijke** toe <img alt= "Pictogram toevoegen" src="./assets/add-icon.svg" width="25"> wordt de variabele niet gemaakt en toegevoegd aan de lijst.

Op deze manier kunt u variabelen met standaardwaarden maken. Bijvoorbeeld:
* Productnaam: Experience Manager Guides
* VersionNumber: 2300
* Releasedatum: 01-01-2023


### Een variabele bewerken

U kunt een variabele op twee manieren bewerken:

**van het paneel van Variabelen op de linkerkant**

1. Selecteer een variabele in het **paneel van Variabelen**.
1. Beweeg over de variabele om het **menu van Opties** te bekijken en dan **uitgezocht geef** optie uit.
1. In **geef Variabele** dialoogdoos uit, kunt u de standaardwaarde van de geselecteerde variabele uitgeven.
1. Selecteer **Gereed**.

**van de redacteur van Variabelen**

1. Selecteer **Variabelen** <img alt= "variabele, pictogram" src="./assets/variables-icon.svg" width="25"> in het linkerdeelvenster.
1. Selecteer **uitgeven** <img alt= "Pictogram Potlood bewerken" src="./assets/edit_pencil_icon.svg" width="25"> om de **Variabelen** redacteur te openen.

1. In de **redacteur van Variabelen**, kunt u de waarde van de geselecteerde variabele uitgeven.

U moet om het even welke veranderingen bewaren u van de **redacteur van Variabelen** aanbrengt om hen in het **deelvenster van Variabelen** op de linkerkant te bekijken.

>[!NOTE]
>
> Als u een waarde van een variabele bewerkt, werkt Adobe Experience Manager Guides tegelijkertijd alle referenties bij, waar van toepassing.

### Een variabele zoeken en voorvertonen

U kunt de waarde van een variabele zoeken en voorvertonen. Ga een koord in de onderzoeksdoos van het **paneel van Variabelen** in. Zowel op basis van de naam van de variabele als op basis van de waarde wordt gezocht.
U kunt een variabele op twee manieren voorvertonen:

In de voorvertoning van de variabele wordt de standaardwaarde weergegeven. Als u bijvoorbeeld de standaardwaarde van de variabele ProductName hebt gedefinieerd als &quot;Adobe Experience Manager Guides&quot;, wordt deze waarde in de voorvertoning weergegeven.

**van het paneel van Variabelen op de linkerkant**


1. Selecteer een variabele in het **paneel van Variabelen**.
1. Beweeg over de variabele om het **menu van Opties** te bekijken en dan de **optie van de Voorproef** te selecteren.

   ![&#x200B; veranderlijke voorproef van het veranderlijke paneel &#x200B;](assets/variables-panel-preview-default.png){width="550" align="left"}

*Voorproef de standaardwaarde voor een variabele.*

**van de redacteur van Variabelen**

1. Beweeg over de variabele in de lijst om het **menu van Opties** te bekijken.
1. Selecteer **Voorproef**.

### Een variabele dupliceren

U kunt een variabele dupliceren en de waarde naar wens wijzigen.


1. Beweeg over de variabele in de lijst om het **menu van Opties** te bekijken.
1. Selecteer **Dupliceren**.

De standaardnaam van de variabele is `<selected variable name>` (zoals &quot;sample&quot;). U kunt de naam naar wens wijzigen.

### Een variabele verwijderen

U kunt een variabele op twee manieren verwijderen:

**van het paneel van Variabelen op de linkerkant**

1. Selecteer een variabele in het **paneel van Variabelen**.
1. Beweeg over de variabele om het **menu van Opties** te bekijken en dan de **schrapping** optie te selecteren.

**Vanuit de editor Variabelen**

1. Plaats de muisaanwijzer op de variabele in de lijst om het **menu Opties** weer te geven.
1. Selecteer **Schrapping** optie.

De variabele wordt verwijderd uit alle sets met variabelen.

## Variabelesets voor uitvoervoorinstellingen

Adobe Experience Manager Guides ondersteunt ook variabelesets, waarmee u de variabelen alternatieve waarden kunt toewijzen. Een onderneming kan bijvoorbeeld twee producten, A en B, verkopen. Het heeft verschillende specificaties voor elk van hen. Deze specificaties kunnen bestaan uit de productnaam, het versienummer en de releasedatum. Er kunnen andere verschillen zijn in branding. Met behulp van variabelensets definieert u een andere set waarden voor uw variabelen. Wanneer u de uitvoer genereert, kiest u de juiste variabelenset en produceert u de vereiste uitvoer.

### Variabelensets configureren

U moet variabelensets configureren voordat u er variabelen aan toevoegt.

1. Selecteer **Montages** <img alt= "Instellingenpictogram" src="./assets/settings-icon.svg" width="25"> om **te openen vormt veranderlijke reeksen** dialoogdoos.
   ![&#x200B; vorm veranderlijke reeks &#x200B;](assets/configure-variable-set.png){width="550" align="left"}
1. Ga de veranderlijke vastgestelde naam in de **Naam** kolom in.
1. Selecteer **veranderlijk toevoegen** <img alt= "Pictogram toevoegen" src="./assets/add-icon.svg" width="25"> om een nieuwe set variabelen toe te voegen. De variabelesets worden in alfabetische volgorde weergegeven.
1. U kunt **Schrapping** selecteren om een veranderlijke reeks te verwijderen.

### Variabele-setbewerkingen

Alle variabelesets hebben dezelfde variabelen maar kunnen verschillende waarden hebben.

U kunt de waarden voor een specifieke set variabelen weergeven, bewerken en voorvertonen. Selecteer een veranderlijke reeks van de **Veranderlijke reeksen** dropdown. De waarden worden weergegeven volgens de gekozen set variabelen.
Wanneer u de waarden voor de variabelen in specifieke variabelesets bewerkt, worden de standaardwaarden genegeerd en worden de waarden van de geselecteerde variabeleset gewijzigd.
Bijvoorbeeld, kunt u de volgende waarden voor de veranderlijke reeksen plaatsen, *Adobe-set1* en *Adobe-set2*.


**Veranderlijke reeks 1**: *Adobe-set1*

* ProductName: ProductA
* Versienummer: 2311
* Releasedatum: 02-11-2023


**Veranderlijke reeks 2**: *Adobe-set2*

* ProductName: ProductB
* Versienummer: 2310
* Releasedatum: 09-07-2023

Elke nieuwe variabele wordt toegevoegd aan alle veranderlijke reeksen. Wanneer u een variabele verwijdert of dupliceert, wordt deze bijgewerkt voor alle variabelesets.

U kunt ook een voorvertoning van de waarden voor een variabeleset weergeven.
Bijvoorbeeld, voor veranderlijke reeks *Adobe-Set1*, hebt u de waarde van de variabele ProductName als &quot;ProductA&quot;bepaald, dan toont het deze waarde in de voorproef in de redacteur van Variabelen.

![&#x200B; veranderlijke voorproef van de variabelenredacteur &#x200B;](assets/variables-editor-preview.png){width="550" align="left"}

*Voorproef de waarde die u in de geselecteerde veranderlijke reeks hebt bepaald.*

### De waarde van een variabele opnieuw instellen

Als u de waarde hebt bewerkt, kunt u ook de standaardwaarde van een variabele herstellen.
Herstellen <img alt= "herstelpictogram" src="./assets/application-variable-revert.svg" width="25"> wordt weergegeven voor een variabele met een gewijzigde waarde.
U kunt bijvoorbeeld de waarde voor de variabele ProductName terugzetten op de standaardwaarde in de Hulplijnen van de Professionele Manager.

## Variabelen gebruiken in de native PDF-sjablonen

U kunt variabelen toevoegen terwijl u de uitvoer van uw productdocumenten genereert, zodat deze gemakkelijk kunnen worden bijgewerkt en overdraagbaar zijn. U kunt deze variabelen invoegen in de pagina-indeling die op de verschillende pagina&#39;s in uw documenten wordt weergegeven. U kunt bijvoorbeeld de variabele ProductName toevoegen die wordt weergegeven in het koptekstgebied van de paginalay-out (of een ander deel zoals de voettekst of de tekst).



Voer de volgende stappen uit om een variabele zoals uw ProductName in het koptekstgebied in te voegen:
1. Open de vereiste pagina-indeling voor bewerking.

   >[!NOTE]
   >
   > De mening [&#x200B; past een sectie van de paginalay-out &#x200B;](../native-pdf/components-pdf-template.md#customize-a-page-layout-customize-page-layout) voor het openen van een paginalay-out voor aanpassing of het uitgeven aan.

1. Selecteer de koptekst om deze actief te maken en een variabele in te voegen.

1. U kunt de variabele op twee manieren invoegen:

   **van het paneel van Variabelen op de linkerkant**

   * Sleep een variabele van het **paneel van Variabelen** en laat vallen het op het kopbalgebied.

   **van de toolbar**

   1. Selecteer **Variabele/Gebieden van het Tussenvoegsel** <img alt= "variabele, pictogram" src="./assets/variables-icon.svg" width="25">.
   1. In het **Veranderlijke** dialoogvakje, selecteer de naam van de variabele om het in het kopbalgebied op te nemen.
   1. U kunt ook de zoektekenreeks in het tekstvak invoeren. De namen van variabelen die de opgegeven tekenreeks bevatten, worden gefilterd en in de lijst weergegeven. De geselecteerde variabele wordt ingevoegd in het koptekstgebied. U kunt de standaardwaarde van de variabele weergeven.
   1. Als u een variabele wilt vervangen, dubbelklikt u op de variabelewaarde en selecteert u een andere variabele in het **dialoogvenster Variabele** . De variabele wordt vervangen.


## PDF-uitvoer genereren met variabelen

U kunt de PDF-uitvoer genereren met de waarden van verschillende variabelen. Alvorens de lay-out te produceren, verkies een veranderlijke reeks van een output vooraf ingesteld **Veranderlijke reeks** drop-down lijst om zijn waarden te kiezen.

![&#x200B; veranderlijke vastgestelde dropdown &#x200B;](assets/output-preset-variable-dropdown.png){width="550" align="left"}

*Selecteer een variabelenset in de vervolgkeuzelijst in de uitvoervoorinstelling die u wilt gebruiken om de PDF-uitvoer te genereren.*

>[!NOTE]
>
> U kunt ook (Standaard) selecteren in de vervolgkeuzelijst om de standaardwaarden voor alle variabelen te publiceren.

Afhankelijk van de door u gekozen variabelenset, krijgt u een uitvoer die overeenkomt met de variabelewaarden die in de variabelenset zijn gedefinieerd. Als u bijvoorbeeld de variabelenset *Adobe-set1* selecteert, worden de waarden van de variabelen in uw uitvoer weergegeven zoals gedefinieerd in deze set.


<img src="assets/variable-pdf-output.png" alt="PDF-uitvoer met variabelen" width="500" border="2px">

*Genereer de PDF-uitvoer met behulp van variabelen in de paginalay-out.*

U kunt de waarden voor elke variabele die u hebt ingesteld, ook snel bijwerken wanneer dat nodig is en de uitvoer opnieuw genereren. Als u bijvoorbeeld de details voor een versie moet bijwerken, kunt u de waarde van de versie bijwerken in de variabele VersionNumber en de uitvoer opnieuw genereren.
