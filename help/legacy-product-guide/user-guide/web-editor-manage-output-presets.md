---
title: Uitvoervoorinstellingen voor Algemeen en Mapprofiel beheren
description: Leer hoe u voorinstellingen voor algemene profielen en mapprofielen als gebruikers met beheerdersrechten in AEM Guides maakt, bewerkt, hernoemt, dupliceert en verwijdert.
feature: Authoring, Features of Web Editor, Publishing
role: User
hide: true
exl-id: 4e9cd1d5-1c28-4363-917d-f58511c4f809
source-git-commit: ea597cd14469f21e197c700542b9be7c373aef14
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# Uitvoervoorinstellingen voor Algemeen en Mapprofiel beheren {#id22BLJ0D0V1U}

De voorinstellingen voor Algemeen en Mapprofiel zijn alleen beschikbaar voor gebruikers met beheerdersrechten op mapniveau.

Als beheerder kunt u met AEM Guides uitvoervoorinstellingen voor de algemene profielen en de mapprofielen maken en beheren. Vervolgens kunt u deze uitvoervoorinstellingen eenvoudig gebruiken om uitvoer te genereren voor alle mappen die betrekking hebben op dat algemene profiel of mapprofiel.

Voer de volgende stappen uit om een uitvoervoorinstelling voor de algemene profielen en mapprofielen te maken:

1. Selecteer de DITA-kaart waarvoor u een uitvoervoorinstelling wilt maken.
1. Selecteer **uitgeven Onderwerpen** optie van **Opties** menu van het kaartdossier. Het kaartdossier wordt geopend voor het uitgeven in de Redacteur van het Web.
1. In het **lusje van de Output**, selecteer + pictogram om tot een output vooraf ingesteld voor uw kaart te leiden DITA.

   ![](images/add-global-output-preset.png){width="350" align="left"}

1. Ga de volgende details in **in vooraf ingestelde** dialoog toevoegen:
   - Type
   - Naam
   - Doel \(voor voorinstelling voor kennisdatabase\)
1. Selecteer **toevoegen aan omslagprofiel** controledoos om een output tot stand te brengen die voor het verwante omslagprofiel vooraf wordt ingesteld en dan **klikken voegt** toe. Vooraf ingesteld wordt gecreeerd, en het verschijnt onder het **lusje van de Output** van alle verwante kaarten. \( ![](images/global-preset-icon.svg)\)-pictogram geeft een voorinstelling voor het mapprofielniveau aan.
1. Voer de configuratiedetails in. Voor meer details op output stelt vooraf in, mening [ Begrijpend de output vooraf in ](./generate-output-understand-presets.md).

   >[!NOTE]
   >
   > Deze voorinstellingen die aan het mappenprofiel worden toegevoegd, zijn onafhankelijk van de kaarten. De mapspecifieke configuraties zijn dus niet aanwezig voor deze voorinstellingen.

1. U kunt **selecteren produceert vooraf ingesteld** pictogram bij de bovenkant om de output voor de kaarten met betrekking tot de gecreeerde vooraf ingestelde output te produceren. De status van het productieproces van de uitvoer wordt weergegeven. Om de output te bekijken, houd de muiswijzer over het onderwerp en klik **Uitvoer van de Mening**.

>[!NOTE]
>
> AEM Guides beschikt ook over een PDF-uitvoervoorinstelling buiten de doos om de uitvoer voor uw DITA-kaarten te genereren.

**Andere verrichtingen van het menu van Opties**

U kunt ook de volgende bewerkingen uitvoeren op de voorinstelling via het menu Opties:

- Selecteer de voorinstelling als standaard-PDF-voorinstelling. Dan zou geselecteerde vooraf ingesteld als gebrek worden gebruikt vooraf ingesteld om de output van PDF te produceren gebruikend de **Download als optie van PDF** voor een kaart.
- **geeft** uit, **anders noemt**, **dupliceert**, of **schrapt** een bestaande output vooraf ingesteld van het **menu van Opties**.

>[!NOTE]
>
> Wanneer een output vooraf ingesteld in Globale en Profielen van de Omslag wordt geschrapt, zal het in alle verwante kaarten weerspiegelen en zal niet onder de **Output** tabel verschijnen.

**Bovenliggend onderwerp:**[ Werk met de Redacteur van het Web ](web-editor.md)
