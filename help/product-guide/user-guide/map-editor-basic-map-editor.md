---
title: Werken met de basiskaarteditor
description: Leer hoe u met de Basic Map Editor in AEM Guides werkt. Ken de eigenschappen van de basiskaartredacteur op kaartniveau en onderwerpniveau. Creeer en geef relatietabellen in een kaart DITA uit.
exl-id: 13da729d-e8f7-46ae-873a-1bfc32da974f
feature: Authoring, Map Editor
role: User
source-git-commit: ac83f613d87547fc7f6a18070545e40ad4963616
workflow-type: tm+mt
source-wordcount: '1471'
ht-degree: 0%

---

# Werken met de basiskaarteditor {#id1942CM005Y4}

>[!NOTE]
>
> De Basic Map Editor, die voorheen beschikbaar was in Experience Manager Guides, is vanaf versie 4.3 en 2307 vervangen. U kunt tot de Basis Redacteur van de Kaart niet toegang hebben om kaarten te creëren en te beheren DITA.
>U wordt geadviseerd om de Geavanceerde Redacteur van de Kaart te gebruiken. De geavanceerde Kaarteditor biedt verbeterde functies en betere aanpassingsopties. Onderzoek meer over hoe te met de [ Geavanceerde Redacteur van de Kaart ](../user-guide/map-editor-advanced-map-editor.md) te werken.

De Basis Redacteur van de Kaart verstrekt een gemakkelijke belemmering-en-dalingseigenschap om onderwerpen van uw bewaarplaats van AEM toe te voegen om de kaart DITA of bookmap tot stand te brengen. U kunt geneste onderwerpen, relatietabellen \(reltable\), attributen en meta-gegevensinformatie toevoegen, en ook de kaart voor correctheid bevestigen.

>[!NOTE]
>
> Als uw beheerder de Geavanceerde optie van de Redacteur van de Kaart heeft toegelaten, dan zult u geen toegang tot de BasisRedacteur van de Kaart hebben. Alle kaartdossiers zullen in de Geavanceerde Redacteur van de Kaart door gebrek openen.

De volgende secties beschrijven de diverse functies beschikbaar in de Basis Redacteur van de Kaart.

## Onderwerpen toevoegen aan een kaartbestand {#id193CBL0505Z}

Zodra een kaartdossier wordt gecreeerd, moet u onderwerpen aan het kaartdossier toevoegen. Gebruikend de Basis Redacteur van de Kaart, kunt u onderwerpen, relatietabellen, of andere kaartdossiers toevoegen.

Voer de volgende stappen uit om uw kaartbestand te maken:

1. Navigeer in de gebruikersinterface van Assets naar het kaartbestand dat u wilt bewerken.

1. Om een exclusief slot op het kaartdossier te krijgen, selecteer het kaartdossier en klik **Controle uit**.

   >[!NOTE]
   >
   > Als u eenmaal een exclusief kaartbestand hebt vergrendeld, kunnen andere gebruikers de kaart niet meer bewerken. Ze kunnen echter wel aan de onderwerpen in het kaartbestand werken.

1. Met het geselecteerde kaartdossier, geeft de klik **&#x200B;**&#x200B;uit.

   Het kaartbestand wordt geopend voor bewerking in de Kaarteditor. Gebruikend de Redacteur van de Kaart, bouwt u een kaart door de momenteel beschikbare onderwerpen te gebruiken die in de spoorstaaf van Verwijzingen worden getoond.

   ![](images/dita-map-01.png){align="left"}

1. Gebruikend het **spoor van Verwijzingen**, navigeer aan de omslag die de onderwerpen of sub-maps bevat die u wilt toevoegen.

   >[!NOTE]
   >
   > U kunt onderwerpen of submaps van om het even welke omslag in de spoorstaaf van Verwijzingen toevoegen.

1. Om het eerste onderwerp aan de kaart toe te voegen, sleep-en-daling het onderwerp op de Basis Redacteur van de Kaart.

   >[!NOTE]
   >
   > Nadat u de eerste koppeling hebt toegevoegd, is de koppeling Nieuwe verwijzing toevoegen beschikbaar wanneer u de muisaanwijzer op een bestaand onderwerp in de kaart plaatst.

1. Als u volgende onderwerpen of een submap wilt toevoegen, sleept u het onderwerp of de submap naar de gewenste locatie in de kaart en zet u deze neer.

   Als u een sub-kaart aan uw kaart DITA toevoegt, wordt submap getoond als verbinding in de kaart DITA. Om alle onderwerpen van sub-kaart te bekijken, klik de sub-kaart verbinding. De inhoud van de submap wordt weergegeven op een nieuw tabblad.

   >[!NOTE]
   >
   > Als u een nieuw onderwerp op een bestaand onderwerp in de kaart laat vallen, krijgt u een bericht over het vervangen van het onderwerp. Klik ja als u het onderwerp wilt vervangen, Nr klikken als u niet het onderwerp wilt vervangen. Met CTRL+Z en CTRL+Y kunt u elke wijziging in de kaart ongedaan maken of opnieuw uitvoeren.

1. Klik **sparen**.


## Functies beschikbaar op de werkbalk van de Basic Map Editor

Met de hoofdwerkbalk in de Basic Map Editor kunt u de volgende taken uitvoeren:

![](images/ditamap-toolbar-actions.png){align="left"}

**A: Onderzoek**

U kunt naar de vereiste onderwerpen van DAM zoeken en omvatten. Wanneer u op dit pictogram klikt, wordt het dialoogvenster Zoeken weergegeven:

![](images/search-dita-map.png){align="left"}

Voer de trefwoorden in waarnaar u wilt zoeken. Deze trefwoorden komen overeen met de bestandsnaam, inhoud en zelfs kenmerkwaarden van het onderwerp. Als de zoekresultaten beschikbaar zijn, selecteert u het gewenste onderwerp en klikt u op de knop Controleren om de geselecteerde bestanden toe te voegen aan het einde van de kaartstructuur. U kunt de zoekresultaten filteren door de parameters Wijzigen van datum op te geven.

**B: Groep**

Klik checkbox links van de onderwerpen en klik Groep in de toolbar om de geselecteerde onderwerpen te groeperen. Voor meer informatie over het groeperen van onderwerpen, zie de [&#128279;](https://docs.oasis-open.org/dita/v1.0/langspec/topicgroup.html) documentatie 0&rbrace; topicgroup &lbrace;in de Specificatie van de Taal van OASIS DITA.

**C: Schrapping**

Klik checkbox links van een onderwerp en klik Schrapping in de toolbar om de geselecteerde onderwerpen van de kaart te verwijderen.

**D: Toon Aantallen/verberg Aantallen**

Nummering \(of verbergen\) weergeven voor de onderwerpen in de kaart.

**E: Valideren**

Controleer of de kaart geldig is of fouten bevat.

**F: De Wijze van Standaard/XML**

In de **StandaardWijze**, toont het klikken van een onderwerpverbinding de voorproef van het onderwerp in een nieuw lusje. Het klikken op het **Standaardpictogram van de Wijze** verandert zijn wijze in **Wijze van XML**. In **Wijze van XML**, toont het klikken overal in een onderwerpregel onderliggende XML van onderwerpverwijzingen binnen het onderwerp. In de bronmening van XML, is er een **AutoInspringing** optie die de code van XML in presenteerbare en gemakkelijk leesbare formaat reorganiseert. Als u een kaart handmatig bewerkt, voert de bronweergave ook validatiecontroles uit. In het geval dat uw XML fouten bevat, wordt het zelfde benadrukt in de **Wijze van XML** en u wordt niet toegestaan om het DITA kaartdossier te bewaren. Als u XML voor de volledige kaart wilt bekijken, klik overal buiten de onderwerpgrens.


**Nota:** op de StandaardWijze kunt u de toetsenbordkortere weg gebruiken om \ (`Ctrl+z` \) ongedaan te maken of \ (`Ctrl+y` \) opnieuw te doen de laatste actie.


![](images/dita-map-invalid-source.png){width="650" align="left"}

**G: De Eigenschappen van de kaart**

Geef het dialoogvenster Eigenschappen kaart weer waarin u de kenmerken en metagegevens voor de kaart kunt instellen. Om een attribuut toe te voegen, klik **voeg** knoop bij de bodem-linkerhoek van de dialoog toe om de **3&rbrace; drop-down lijst van Attributen &lbrace;te krijgen.** Selecteer in de lijst het kenmerk dat u wilt toevoegen. Als voor het geselecteerde kenmerk vooraf gedefinieerde waarden zijn opgegeven in het DTD-bestand, worden deze waarden weergegeven in een nieuwe vervolgkeuzelijst. U kunt de gewenste waarde selecteren in de vervolgkeuzelijst. Als er geen vooraf gedefinieerde waarde is, wordt een tekstvak weergegeven waarin u een waarde voor het geselecteerde kenmerk kunt invoeren.

![](images/map-properties.png){width="300" align="left"}

## Functies beschikbaar op onderwerpniveau in de Basic Map Editor

Wanneer u de muiswijzer over een onderwerp of een sub-kaartdossier in de Basis Redacteur van de Kaart beweegt, kunt u de volgende taken uitvoeren:

![](images/ditamap-actions.png){width="650" align="left"}

**A: Beweging Linksom of Beweging Juist**

Klik op de pictogrammen voor pijl-links of pijl-rechts om het onderwerp naar links of rechts te verplaatsen. Als u een onderwerp op een dergelijke manier verplaatst, wordt dit een onderliggend onderwerp \(nesten\) of wordt \(nesten verwijderen\) verwijderd ten opzichte van het onderwerp erboven.

**B: Eigenschappen**

Klik op het pictogram Eigenschappen om het dialoogvenster Eigenschappen van Topicref te openen. In dit dialoogvenster kunt u de onderwerpkenmerken en metagegevens instellen. Voor meer informatie over de standaardonderwerpattributen en meta-gegevens, zie de [ topicref ](https://docs.oasis-open.org/dita/v1.2/os/spec/langref/topicref.html) documentatie in de Specificatie van de Taal OASIS DITA.


![](images/map-properties-metadata.png){width="350" align="left"}

**C: Voeg Nieuwe Verwijzing** toe

Klik op het pictogram Nieuwe verwijzing toevoegen om een nieuwe verwijzing op hetzelfde niveau als het huidige onderwerp toe te voegen.

**D: Voeg Nieuwe Zeer belangrijke Definitie toe**

Klik op het pictogram Key om een nieuwe sleuteldefinitie toe te voegen. Overschreven toetsen of toetsen die al in de kaart zijn gedefinieerd, worden rood weergegeven. Als u op het pictogram Eigenschappen op een sleuteldefinitie klikt, wordt het dialoogvenster Eigenschappen van keydef weergegeven.

## Werken met relatietabellen in de Basic Map Editor {#id1944B0I0COB}

De kaartredacteurs van AEM Guides komen met een krachtige eigenschap die u toestaat om relatietabellen in uw kaart te creëren en uit te geven DITA.

Voer de volgende stappen uit om met relatietabellen in de BasisRedacteur van de Kaart te werken:

1. In Assets UI, navigeer aan de kaart DITA waarin u de relatietabel wilt tot stand brengen.

1. Klik op de kaart DITA om het in DITA kaartconsole te openen.

1. Selecteer het **lusje van Onderwerpen** om een lijst van onderwerpen beschikbaar in de kaart te zien DITA.

   >[!TIP]
   >
   > Het lusje van Onderwerpen geeft u een optie om het kaartdossier met zijn gebiedsdelen te downloaden. Voor meer details, zie [ Exporteer een DITA kaartdossier ](authoring-download-assets.md#id218UBA00IXA).

1. In de belangrijkste toolbar, geeft de klik **&#x200B;**&#x200B;uit.

   Het kaartbestand wordt geopend in de Basic Map Editor.

1. Selecteer **Reltable** van de toolbar.

   ![](images/reltable.png){width="650" align="left"}

1. De belemmering-en-dalingsonderwerpen van de onderwerpenlijst aan de Reltable redacteur.

   >[!NOTE]
   >
   > U kunt onderwerpen vanuit elke map toevoegen in de References-rail.

   ![](images/create-reltable.png){width="550" align="left"}

1. Om een kopbal aan uw relatietabel toe te voegen, klik **voeg Relheader** toe.

1. Om een kolom aan uw relatielijst toe te voegen, klik **voeg een Kolom** toe.

   ![](images/complete-reltable.png){width="550" align="left"}

1. Klik **sparen**.


U kunt de volgende acties van de redacteur van de relatietabel ook uitvoeren:

**Schrap rijen of kolommen**

Als u een kolom uit uw lijst wilt schrappen, selecteer checkbox in de kolomkopbal en klik Schrapping. Als u een rij uit lijst wilt verwijderen, checkbox in de eerste kolom van de respectieve rij en klik Schrapping.

**Schrap een onderwerp**

Als u een onderwerp van uw lijst wilt schrappen, klik het dwarspictogram naast het onderwerp.

**Schrap de relatielijst**

Als u de relatietabel wilt verwijderen, klikt u ergens buiten de relatietabel en klikt u op Verwijderen.

**Bovenliggend onderwerp:**&#x200B;[ Werk met de Redacteur van de Kaart ](map-editor.md)
