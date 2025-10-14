---
title: DITAVAL-editor gebruiken
description: Begrijp hoe u DITAVAL-bestanden maakt en bewerkt met de DIVATAL Editor in AEM Guides. Weet hoe de DITAVAL-editor DITAVAL-bestanden ondersteunt in auteur- en bronweergaven.
feature: Authoring, DITAVAL Editor
role: User
hide: true
exl-id: 8eee347d-840e-4eaf-9441-c7c53a7c3aa0
source-git-commit: 26fa1e52920c1f1abd5655b9ca7341600a9bca67
workflow-type: tm+mt
source-wordcount: '758'
ht-degree: 0%

---

# DITAVAL-editor {#ditaval-editor}

DITAVAL-bestanden worden gebruikt om voorwaardelijke uitvoer te genereren. In één onderwerp, kunt u voorwaarden toevoegen gebruikend elementenattributen om inhoud te conditionaliseren. Vervolgens maakt u een DITAVAL-bestand waarin u de voorwaarden opgeeft die moeten worden opgepakt om inhoud te genereren en welke voorwaarde niet in de uiteindelijke uitvoer moet worden opgenomen.

Met AEM Guides kunt u eenvoudig DITAVAL-bestanden maken en bewerken met de DITAVAL-editor. De DITAVAL-editor haalt de kenmerken \(of tags\) op die in uw systeem zijn gedefinieerd en u kunt deze gebruiken om DITAVAL-bestanden te maken of te bewerken. Voor meer details over het creëren van en het leiden van markeringen in AEM, zie [&#128279;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/tags.html?lang=nl-NL) sectie van de Codes van het beheer  in de documentatie van AEM.

## DITAVAL-bestand maken

Voer de volgende stappen uit om een DITAVAL-bestand te maken:

1. Navigeer in de gebruikersinterface van Assets naar de locatie waar u het DITAVAL-bestand wilt maken.

1. Klik **creëren** \> **Onderwerp DITA**.

1. Voor de pagina van de Vervaging, uitgezochte DITAVAL dossiermalplaatje en klik **daarna**.

1. Voor de pagina van Eigenschappen, specificeer de **Titel** en **Naam** voor het DITAVAL dossier.

   >[!NOTE]
   >
   > De naam wordt automatisch voorgesteld gebaseerd op de Titel van uw dossier. Als u de bestandsnaam handmatig wilt opgeven, moet u ervoor zorgen dat de naam geen spaties, apostrof of accolades bevat en eindigt met .ditaval.

1. Klik **creëren**. Het bericht Gemaakt onderwerp wordt weergegeven.

   U kunt het DITAVAL-bestand openen om te bewerken in de DITAVAL-editor of het onderwerpbestand opslaan in de AEM-opslagplaats.


## DITAVAL-bestand bewerken

Voer de volgende stappen uit om een DITAVAL-bestand te bewerken:

1. Navigeer in de gebruikersinterface van Assets naar het DITAVAL-bestand dat u wilt bewerken.

1. Om een exclusieve slot op het dossier te krijgen, selecteer het dossier en klik **Controle uit**.

1. Selecteer het dossier en klik **uitgeven** om het dossier in de redacteur van AEM Guides te openen DITAVAL.

   Met de DITAVAL-editor kunt u de volgende taken uitvoeren:

   A: Linkerdeelvenster in-/uitschakelen
De weergave van het linkerdeelvenster in-/uitschakelen. Als u het DITAVAL-bestand hebt geopend via de DITA-kaart, worden de kaart en de opslagplaats weergegeven in dit deelvenster. Voor meer informatie over het openen van een dossier door kaart DITA, zie [&#x200B; onderwerpen door kaart DITA &#x200B;](map-editor-advanced-map-editor.md#id17ACJ0F0FHS) uitgeven.

   B: Opslaan
Hiermee slaat u de wijzigingen op die u in het bestand hebt aangebracht. Alle wijzigingen worden opgeslagen in de huidige versie van het bestand.

   C: Eigenschap toevoegen
Voeg één eigenschap toe aan uw DITAVAL-bestand.

   ![](images/ditaval-editor-props.png)

   De eerste vervolgkeuzelijst bevat de toegestane DITA-kenmerken die u kunt gebruiken in het DITAVAL-bestand. Er zijn vijf kenmerken die worden ondersteund: `audience` , `platform` , `product` , `props` en `otherprops` .

   De tweede drop-down lijst toont de waarden die voor de geselecteerde attributen worden gevormd. Dan, toont de volgende drop-down lijst de acties die u op de geselecteerde attributen kunt vormen. De toegestane waarden in de vervolgkeuzelijst voor handelingen zijn - `include` , `exclude` , `passthrough` en `flag` . Voor meer informatie over deze waarden, zie de definitie van [&#x200B; prop &#x200B;](http://docs.oasis-open.org/dita/dita/v1.3/errata01/os/complete/part3-all-inclusive/langRef/ditaval/ditaval-prop.html#ditaval-prop) element in OASIS DITA- documentatie

   D: Alle eigenschappen toevoegen
Als u met één klik alle voorwaardelijke eigenschappen of kenmerken wilt toevoegen die in uw systeem zijn gedefinieerd, gebruikt u de functie Alle eigenschappen toevoegen.

   >[!NOTE]
   >
   > Als het DITAVAL-bestand al alle gedefinieerde voorwaardelijke eigenschappen bevat, kunt u geen eigenschappen meer toevoegen. Er verschijnt een foutbericht in dit scenario.

   ![](images/ditaval-all-props.png)

1. Zodra u klaar bent met het uitgeven van uw DITAVAL dossier, klik **sparen**.

   >[!NOTE]
   >
   > Als u het bestand sluit zonder op te slaan, gaan de wijzigingen verloren. Als u niet wenst om veranderingen in de bewaarplaats van AEM vast te leggen, klik **dicht**, en klik dan **Sluiten zonder** op te slaan in de **Unsaved dialoog van Veranderingen**.


## Weergaven DITAVAL-editor

De DITAVAL-editor van AEM Guides ondersteunt het weergeven van DITAVAL-bestanden in twee verschillende modi of weergaven:

**Auteur**:   Dit is een typisch wat u ziet is wat u \ (WYSISYG \) mening van de redacteur van DITAVAL krijgt. U kunt eigenschappen toevoegen of verwijderen met behulp van de eenvoudige gebruikersinterface, die de eigenschappen, waarden en handelingen in de vervolgkeuzelijst weergeeft. In de weergave Auteur kunt u een afzonderlijke eigenschap invoegen en alle eigenschappen met één klik invoegen.

U kunt ook de versie van het DITAVAL-bestand vinden waaraan u momenteel werkt door de aanwijzer op de bestandsnaam te plaatsen.

**Source**:   In de Source-weergave wordt de onderliggende XML weergegeven waaruit het DITAVAL-bestand bestaat. Naast het uitvoeren van regelmatige tekstbewerkingen in deze weergave, kan een auteur ook eigenschappen toevoegen of bewerken met de slimme catalogus.

Om de Slimme Catalogus aan te halen, plaats de curseur aan het eind van om het even welke bezitsdefinitie en ga &quot;&lt;&quot; in. De redacteur zal een lijst van alle geldige elementen van XML tonen die u bij die plaats kunt opnemen.

![](images/ditaval-source-view.png)
