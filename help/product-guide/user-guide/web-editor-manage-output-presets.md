---
title: Uitvoervoorinstellingen voor Algemeen en Mapprofiel beheren
description: Leer hoe u voorinstellingen voor algemene profielen en mapprofielen als gebruikers met beheerdersrechten in AEM Guides maakt, bewerkt, hernoemt, dupliceert en verwijdert.
exl-id: 549c9fe2-77f8-423c-8b3e-b43e56055732
feature: Authoring, Features of Web Editor, Publishing
role: User
source-git-commit: f6ff978305d9a1587366acbe96d274408bf457f4
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---

# Uitvoervoorinstellingen voor Algemeen en Mapprofiel beheren {#id22BLJ0D0V1U}

De voorinstellingen voor Algemeen en Mapprofiel zijn alleen beschikbaar voor gebruikers met beheerdersrechten op mapniveau.

Als beheerder kunt u met Adobe Experience Manager Guides uitvoervoorinstellingen voor de algemene profielen en de mapprofielen maken en beheren. Vervolgens kunt u deze uitvoervoorinstellingen eenvoudig gebruiken om uitvoer te genereren voor alle mappen die betrekking hebben op dat algemene profiel of mapprofiel.

Voer de volgende stappen uit om een uitvoervoorinstelling voor de algemene profielen en mapprofielen te maken:

1. Selecteer de DITA-kaart waarvoor u een uitvoervoorinstelling wilt maken.
1. Selecteer **uitgeven Onderwerpen** optie van **Opties** menu van het kaartdossier. Het kaartbestand wordt geopend voor bewerking in de Editor.
1. Selecteer **Open in kaartconsole** pictogram om het kaartdossier in de console van de Kaart te openen.
1. In de console van de Kaart, navigeer aan **vooraf instelt van de Output** tabel, en selecteer dan + pictogram om een output tot stand te brengen die voor uw kaart DITA vooraf wordt ingesteld.

   ![](images/add-global-output-preset.png){width="350" align="left"}

1. Ga de volgende details in **in vooraf ingestelde** dialoog toevoegen:
   - Type
   - Naam
   - Doel \(voor voorinstelling voor kennisdatabase\)
1. Selecteer **toevoegen aan omslagprofiel** controledoos om een output tot stand te brengen vooraf ingesteld voor het verwante omslagprofiel en dan **selecteren** toevoegt. Vooraf ingesteld wordt gecreeerd, en het verschijnt onder **vooraf instelt van de Output** lusje van alle verwante kaarten. \( ![](images/global-preset-icon.svg)\)-pictogram geeft een voorinstelling voor het mapprofielniveau aan.
1. Voer de configuratiedetails in. Voor meer details op output stelt vooraf in, mening [ Begrijpend de output vooraf in ](./generate-output-understand-presets.md).

   >[!NOTE]
   >
   > Deze voorinstellingen die aan het mappenprofiel worden toegevoegd, zijn onafhankelijk van de kaarten. De mapspecifieke configuraties zijn dus niet aanwezig voor deze voorinstellingen.

1. U kunt selecteren **output** pictogram bij de hoogste juiste hoek produceren om de output voor de kaarten met betrekking tot de gecreeerde vooraf ingestelde output te produceren. U kunt de status van het productieproces van de uitvoer weergeven. Om de output te bekijken, uitgezochte **Output van de Mening** in het **de dialoogvakje van het Succes**.

>[!NOTE]
>
> Experience Manager Guides beschikt ook over een PDF-uitvoervoorinstelling buiten de doos om de uitvoer voor uw DITA-kaarten te genereren.

**Andere verrichtingen van het menu van Opties**

U kunt ook de volgende bewerkingen uitvoeren op de voorinstelling via het menu Opties:

- **produceer output**: Staat u toe om een output voor bestaande vooraf ingesteld te produceren.
- **output van de Mening** en **Logboek van de Mening**: Snelle verbindingen om de geproduceerde output en logboeken te bekijken.
- **noem** anders, **Dupliceer**, of **schrap** een bestaande output vooraf ingesteld van het **menu van Opties**.
- **StandaardPDF**: Staat u toe om bestaande vooraf ingesteld PDF als gebrek te selecteren pdf vooraf ingesteld. Geselecteerde vooraf ingesteld zou, dan gebruikt als gebrek worden vooraf ingesteld om de output van PDF te produceren gebruikend de **Download als optie van PDF** voor een kaart.

>[!NOTE]
>
> Wanneer een output vooraf ingesteld in Globale en Profielen van de Omslag wordt geschrapt, zal het in alle verwante kaarten weerspiegelen en zal niet onder **vooraf instelt van de Output** tabel verschijnen.

**Bovenliggend onderwerp:**[ Werk met de Redacteur van het Web ](web-editor.md)
