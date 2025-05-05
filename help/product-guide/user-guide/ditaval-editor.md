---
title: DITAVAL-editor gebruiken
description: Begrijp hoe u DITAVAL-bestanden maakt en bewerkt met de DIVATAL Editor in Adobe Experience Manager Guides. Weet hoe de DITAVAL-editor DITAVAL-bestanden ondersteunt in auteur- en bronweergaven.
exl-id: f3901a4f-1925-42aa-b773-0d6f18175ce8
feature: Authoring, DITAVAL Editor
role: User
source-git-commit: ac83f613d87547fc7f6a18070545e40ad4963616
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 0%

---

# DITAVAL-editor {#ditaval-editor}

DITAVAL-bestanden worden gebruikt om voorwaardelijke uitvoer te genereren. In één onderwerp, kunt u voorwaarden toevoegen gebruikend elementenattributen om inhoud te conditionaliseren. Vervolgens maakt u een DITAVAL-bestand waarin u de voorwaarden opgeeft die moeten worden opgepakt om inhoud te genereren en welke voorwaarde niet in de uiteindelijke uitvoer moet worden opgenomen.

Met Adobe Experience Manager Guides kunt u eenvoudig DITAVAL-bestanden maken en bewerken met de DITAVAL-editor. De DITAVAL-editor haalt de kenmerken \(of tags\) op die in uw systeem zijn gedefinieerd en u kunt deze gebruiken om DITAVAL-bestanden te maken of te bewerken. Voor meer details over het creëren van en het leiden van markeringen in Adobe Experience Manager, mening [&#128279;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/tags.html?lang=nl-NL) sectie van de Markeringen van 0&rbrace; het Beheer in de documentatie van Adobe Experience Manager.

In de volgende secties vindt u de opties die beschikbaar zijn voor een DITAVAL-bestand in Experience Manager Guides.

- [DITAVAL-bestand maken](#create-ditaval-file)
- [DITAVAL-bestand bewerken](#edit-ditaval-file)
- [Weergaven van DITAVAl-bestandseditor](#ditaval-editor-views)
- [Werken met DITAVAL-bestand in de gebruikersinterface van Assets](#working-with-ditaval-files-in-the-assets-ui)

## DITAVAL-bestand maken

Voer de volgende stappen uit om een DITAVAL-bestand te maken:

1. In het paneel van de Bewaarplaats, selecteer het **Nieuwe dossier** pictogram en selecteer dan **Onderwerp** van het dropdown menu.

   ![](images/new-file-option.png){align="left"}

   U kunt tot deze optie van de [ Homepage van Experience Manager Guides ](./intro-home-page.md) en tot het optiesmenu van een omslag in de mening van de Bewaarplaats ook toegang hebben.

2. Het **Nieuwe onderwerp** dialoogvakje wordt getoond.

3. In het **Nieuwe onderwerp** dialoogvakje, verstrek de volgende details:
   - Een titel voor het onderwerp.
   - \(Optioneel\)* De bestandsnaam voor het onderwerp. De bestandsnaam wordt automatisch voorgesteld op basis van de titel van het onderwerp. Als de beheerder automatische bestandsnamen heeft ingeschakeld op basis van de UUID-instelling, wordt het veld Naam niet weergegeven.
   - Een malplaatje waarop het onderwerp zal worden gebaseerd. Voor een DITAVAL dossier, uitgezochte **Ditaval** van de dropdown lijst.
   - Pad waar u het onderwerpbestand wilt opslaan. Standaard wordt het pad van de geselecteerde map in de opslagplaats weergegeven in het veld Pad.

   ![](images/new-topic-dialog-ditaval.png){width="300" align="left"}


4. Selecteer **creeer**.

Het onderwerp wordt gecreeerd bij de gespecificeerde weg. Het onderwerp wordt ook geopend in de Editor voor bewerking.

![](images/ditaval-file-editor.png){align="left"}

## DITAVAL-bestand bewerken

Als u een DITAVAL-onderwerp maakt, wordt dit geopend in de Editor en bewerkt. Om een bestaand DITAVAL onderwerp uit te geven, navigeer aan de omslag of de kaart waar het DITAVAL onderwerp wordt gevestigd, en selecteer dan **uitgeven** van het **&#x200B;**&#x200B;menu van Opties.

Met de DITAVAL-editor kunt u de volgende taken uitvoeren:

- Linkerdeelvenster in-/uitschakelen

  De weergave van het linkerdeelvenster in-/uitschakelen. Als u het DITAVAL-bestand hebt geopend via de DITA-kaart, worden de kaart en de opslagplaats weergegeven in dit deelvenster. Voor meer informatie over het openen van een dossier door kaart DITA, geeft de mening [ onderwerpen door kaart DITA ](map-editor-advanced-map-editor.md#id17ACJ0F0FHS) uit.

- Opslaan

  Hiermee slaat u de wijzigingen op die u in het bestand hebt aangebracht. Alle wijzigingen worden opgeslagen in de huidige versie van het bestand.

- Prop toevoegen

  Voeg één eigenschap toe aan uw DITAVAL-bestand.

  ![](images/ditaval-editor-props-new.png)

  De eerste vervolgkeuzelijst bevat de toegestane DITA-kenmerken die u kunt gebruiken in het DITAVAL-bestand. Er zijn vijf kenmerken die worden ondersteund: `audience` , `platform` , `product` , `props` en `otherprops` .

  De tweede drop-down lijst toont de waarden die voor de geselecteerde attributen worden gevormd. Dan, toont de volgende drop-down lijst de acties die u op de geselecteerde attributen kunt vormen. De toegestane waarden in de vervolgkeuzelijst voor handelingen zijn - `include` , `exclude` , `passthrough` en `flag` . Voor meer informatie over deze waarden, bekijk de definitie van [ prop ](http://docs.oasis-open.org/dita/dita/v1.3/errata01/os/complete/part3-all-inclusive/langRef/ditaval/ditaval-prop.html#ditaval-prop) element in OASIS DITA- documentatie

- Alle eigenschappen toevoegen

  Als u met één klik alle voorwaardelijke eigenschappen of kenmerken wilt toevoegen die in uw systeem zijn gedefinieerd, gebruikt u de functie Alle eigenschappen toevoegen.

  >[!NOTE]
  >
  > Als het DITAVAL-bestand al alle gedefinieerde voorwaardelijke eigenschappen bevat, kunt u geen eigenschappen meer toevoegen. Er verschijnt een foutbericht in dit scenario.

  ![](images/ditaval-all-props-new.png)

Zodra u klaar bent met het uitgeven van uw DITAVAL dossier, uitgezocht **sparen**.

>[!NOTE]
>
> Als u het bestand sluit zonder op te slaan, gaan de wijzigingen verloren. Als u niet wenst om veranderingen in de bewaarplaats van Adobe Experience Manager vast te leggen, selecteer **dicht**, en selecteer dan **Sluiten zonder** op te slaan in de **Unsaved dialoog van Veranderingen**.

## Weergaven DITAVAL-editor

De DITAVAL-editor van Adobe Experience Manager Guides ondersteunt het weergeven van DITAVAL-bestanden in twee verschillende modi of weergaven:

**Auteur**:   Dit is een typisch wat u ziet is wat u \ (WYSISYG \) mening van de redacteur van DITAVAL krijgt. U kunt eigenschappen toevoegen of verwijderen met behulp van de eenvoudige gebruikersinterface, die de eigenschappen, waarden en handelingen in de vervolgkeuzelijst weergeeft. In de weergave Auteur kunt u een afzonderlijke eigenschap invoegen en alle eigenschappen met één klik invoegen.

U kunt ook de versie van het DITAVAL-bestand vinden waaraan u momenteel werkt door de aanwijzer op de bestandsnaam te plaatsen.

**Source**:   In de Source-weergave wordt de onderliggende XML weergegeven waaruit het DITAVAL-bestand bestaat. Naast het uitvoeren van regelmatige tekstbewerkingen in deze weergave, kan een auteur ook eigenschappen toevoegen of bewerken met de slimme catalogus.

Om de Slimme Catalogus aan te halen, plaats de curseur aan het eind van om het even welke bezitsdefinitie en ga &quot;&lt;&quot; in. De redacteur zal een lijst van alle geldige elementen van XML tonen die u bij die plaats kunt opnemen.

![](images/ditaval-source-view-new.png)


## Werken met DITAVAL-bestanden in de gebruikersinterface van Assets

U kunt ook een DITAVAL-bestand maken via de gebruikersinterface van Assets. De stappen om een nieuw onderwerp te creëren DITAVAL zijn als volgt:

1. Navigeer in de gebruikersinterface van Assets naar de locatie waar u het DITAVAL-bestand wilt maken.

1. Selecteer **creeer** \> **Onderwerp DITA**.

1. Voor de pagina van de Vervaging, uitgezochte DITAVAL dossiermalplaatje en selecteer **daarna**.

1. Voor de pagina van Eigenschappen, specificeer de **Titel** en **Naam** voor het DITAVAL dossier.

   >[!NOTE]
   >
   > De naam wordt automatisch voorgesteld gebaseerd op de Titel van uw dossier. Als u de bestandsnaam handmatig wilt opgeven, moet u ervoor zorgen dat de naam geen spaties, apostrof of accolades bevat en eindigt met .ditaval.

1. Selecteer **creeer**.

   Het bericht Gemaakt onderwerp wordt weergegeven.

U kunt het DITAVAL-bestand openen om te bewerken in de DITAVAL-editor of het onderwerpbestand opslaan in de Adobe Experience Manager-opslagplaats.

Voer de volgende stappen uit om een bestaand DITAVAL-bestand te bewerken:

1. Navigeer in de gebruikersinterface van Assets naar het DITAVAL-bestand dat u wilt bewerken.

1. Om een exclusieve slot op het dossier te krijgen, selecteer het dossier en selecteer **Controle uit**.

1. Selecteer het dossier en selecteer **uitgeven** om het dossier in de redacteur van Adobe Experience Manager Guides te openen DITAVAL.



