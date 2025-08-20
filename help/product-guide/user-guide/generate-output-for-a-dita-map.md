---
title: Uitvoer genereren
description: Produceer output voor een kaart DITA van de kaartconsole en het dashboard van de Kaart in AEM Guides.
exl-id: d6cbd44c-e74c-4192-bcc4-fb7752c59508
feature: Publishing
role: User
source-git-commit: 358d38ca761661eaee7aeac2cc7d46c53105c543
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# Uitvoer genereren

Er zijn twee manieren om output voor een kaart te produceren DITA:

- [ produceer output voor een kaart DITA van de console van de Kaart ](#generate-output-for-a-dita-map-from-the-map-console)
- [Output voor een DITA-kaart genereren via het kaartdashboard](#generate-output-for-a-dita-map-from-the-map-dashboard)

## Produceer output voor een kaart DITA van de console van de Kaart

Voer de volgende stappen uit om output voor een kaart te produceren DITA gebruikend de console van de Kaart:

1. [ open een kaartdossier in de console van de Kaart ](./open-files-map-console.md).
2. De DITA kaartconsole wordt getoond met de lijst van **Voorinstellingen van de Output** beschikbaar om output te produceren.

3. Open vooraf ingesteld die u voor het produceren van de output wilt gebruiken, en **selecteren produceert output** om het generatieproces te beginnen.

   <img src="images/generate-output-pdf.png" alt="tabblad Metagegevens" width="600">

   Of, beweeg over vooraf ingesteld en selecteer **** van het vooraf ingestelde contextmenu produceren.


   <img src="images/generate-preset-map-console.png" alt="tabblad Metagegevens" width="600">

Zodra de outputgeneratie volledig is, uitgezochte **output van de Mening** om de output te bekijken.

A **de dialoogdoos van het Succes** is zichtbaar bij de laag-juiste hoek van het scherm.

Als de uitvoer niet is gelukt, wordt het onderstaande foutbericht weergegeven.

<img src="images/error-log.png" alt="foutenlogboek" width="250">

Om het foutenlogboek te bekijken, selecteer **Ontwerpen**, over het geselecteerde vooraf ingestelde lusje, en selecteer **Logboek van de Mening** van het vooraf ingestelde contextmenu.

## Output voor een DITA-kaart genereren via het kaartdashboard

Voer de volgende stappen uit om output voor een kaart te produceren DITA gebruikend het dashboard van de Kaart:

1. Navigeer in de gebruikersinterface van Assets naar het DITA-toewijzingsbestand dat u wilt publiceren en selecteer dit.

   De DITA kaartconsole verschijnt met de lijst van de Voorinstellingen van de Output beschikbaar om output te produceren.

1. Selecteer een of meerdere uitvoervoorinstellingen die u wilt gebruiken voor het genereren van de uitvoer.

   ![](images/generate-multiple-outputs-uuid.png){align="left"}

1. Selecteer **produceer** pictogram om het proces van de outputgeneratie te beginnen.


U kunt het huidige statuut van het verzoek van de outputgeneratie in de **Uitvoer** tabel bekijken. Voor meer informatie, mening [ bekijk het statuut van de taak van de outputgeneratie ](./generate-output-manage-process.md#view-the-status-of-the-output-generation-task).

>[!IMPORTANT]
>
> Als een uitvoergeneratieproces voor een voorinstelling zich in de wachtrij of in uitvoering bevindt, kunt u geen andere uitvoergeneratietaak voor dezelfde voorinstelling starten.

U kunt de output van AEM Sites voor één of meerdere onderwerpen, of de volledige kaart DITA van de console van de Kaart ook produceren. Voor meer details, produceert de mening [ output van de Kennisbank ](web-editor-article-publishing.md#id218CK0U019I).

## Verschillende onderwerpen in een DITA-kaart samenvoegen met het kenmerk `chunk`

Een kaart DITA kan verschillende onderwerptypes zoals verwijzing, concept, en taak omvatten. Met het kenmerk `chunk=to-content` kunt u deze onderwerpen samenvoegen om één pagina-uitvoer op AEM Sites te genereren. Nochtans, om het samengevoegde onderwerp behoorlijk te publiceren, zorg ervoor dat uw Beheerder de correcte catalogus van XML in de Profielen DITA heeft gevormd.

Het systeem vereist een Openbare identiteitskaart met het `composite` sleutelwoord in de catalogus van XML om de aangewezen regel correct te identificeren en toe te passen DTD.
Deze configuratie is standaard opgenomen in de standaard XML-catalogus. Nochtans, als u een catalogus van douaneXML gebruikt, zorg ervoor uw Beheerder deze openbare identiteitskaart aan de configuratie heeft toegevoegd. Zonder het, kan het samengevoegde onderwerp niet behoorlijk publiceren.

Voor details op hoe te om Openbare identiteitskaart en identiteitskaart van het Systeem in uw douaneDTDs/XSDs te gebruiken, mening [ integreer specialisatie DITA ](../cs-install-guide/dita-ot-specialization.md#integrate-dita-specialization-id211mb0e00xa).



**Bovenliggend onderwerp:**[ Productie van de Output ](generate-output.md)
