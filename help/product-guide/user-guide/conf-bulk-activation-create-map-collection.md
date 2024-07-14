---
title: Een verzameling bulkactiveringskaarten maken
description: Leer hoe u een bulkactiveringskaartverzameling maakt in AEM hulplijnen.
exl-id: ea0bd465-a2d9-488f-83e9-62b336233eb1
feature: Publishing, Bulk Activation
role: User
source-git-commit: 1be8cddcbf58696a53bfccf887a04e5807f2198e
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# Een verzameling bulkactiveringskaarten maken {#id214GG0E90EV}

Voer de volgende stappen uit om een bulkactiveringskaartverzameling te maken:

1. Selecteer **Gidsen** van de lijst van hulpmiddelen.

1. Selecteer de verbinding van Adobe Experience Manager bij de bovenkant en kies **Hulpmiddelen**.

1. Selecteer het **BulkPublish Dashboard** tegel.

   Voor het eerst wordt een lege verzamelingspagina weergegeven. Als u eerder bulkactiveringsverzamelingen hebt gemaakt, worden deze op deze pagina weergegeven.

1. Klik **creëren**.

1. Ga een titel voor uw bulkactiveringskaartinzameling in en klik **creeer**.

   Een succesbericht wordt getoond bij de verwezenlijking van de bulkactivering kaartinzameling.

1. Klik **Open** op het succesbericht.

1. Selecteer **uitgeven** en selecteer dan **Kaarten** toevoegen.

1. Zoek en voeg de DITA-kaarten toe die u aan de bulkactiveringskaartverzameling wilt toevoegen.

   Standaard worden alle voorinstellingen en landinstellingen die aan de kaart zijn gekoppeld, automatisch toegevoegd.

1. Selecteer de gewenste uitvoer door de schuifknop in of uit te schakelen.

   U kunt meerdere uitvoervoorinstellingen kiezen voor alle beschikbare landinstellingen.

1. Klik **Gedaan**.

De DITA kaartdossiers worden toegevoegd aan uw bulkactiveringskaartinzameling.

![ Gemaakte bulkactivering inzameling ](images/bulk-activation-collection-created.png){width="800" align="left"}

## Tabblad Kaarten en voorinstellingen

Het **Kaarten en stelt** lusje vooraf in stelt informatie in de volgende kolommen voor:

- **Kaart**: Toont de titel van het DITA kaartdossier.
- **Weg van de Kaart**: Toont de volledige weg van het DITA kaartdossier.

- **UUID**: Toont het unieke herkenningsteken verbonden aan het dossier.

- **Taal**: Toont de taalcode van de kaart DITA.
- **Vooraf ingesteld**: Toont de titel van de output die op het kaartdossier wordt gevormd. Het pictogram wordt ook weergegeven op basis van het type uitvoervoorinstelling.

  >[!NOTE]
  >
  > Het kleine pictogram ![](images/global-preset-icon.svg) geeft een voorinstelling voor het mapprofielniveau aan.

- **Gewijzigd**: Wijst op als de kaart DITA na laatste publicatie wordt bijgewerkt. Op basis van deze informatie kunt u beslissen of u de uitvoer voor deze DITA-kaart wilt activeren.
- **Gegenereerde**: Toont de datum en de tijd van de laatste geproduceerde output.
- **Gepubliceerd**: Toont de datum en de tijd van de laatste gepubliceerde (of geactiveerde) output. Als u de verbinding selecteert, wordt de **pagina van de Resultaten van de Activering** getoond, die de logboeken met informatie over de wortelweg bevat waar de inhoud wordt geactiveerd.

## Tabblad Controlegeschiedenis

Het **lusje van de Geschiedenis van de Controle** stelt informatie over de geactiveerde kaartoutput in de volgende kolommen voor:
- **Kaart**: Toont de titel van het DITA kaartdossier.
- **Weg van de Kaart**: Toont de volledige weg van het DITA kaartdossier.
- **UUID** : Toont het unieke herkenningsteken verbonden aan het dossier.
- **Taal**: Toont de taalcode van de kaart DITA.
- **Vooraf ingesteld**: Toont de titel van de output die op het kaartdossier wordt gevormd. Het pictogram wordt ook weergegeven op basis van het type uitvoervoorinstelling.
- **Status**: Toont het statuut van activering als succesvol of niet succesvol.
- **Doel**: Als u de output op as a Cloud Service Experience Manager Guides produceert, kunt u de bestemming van de output als Publish of Voorproef bekijken.

  >[!NOTE]
  >
  > Het kleine pictogram ![](images/global-preset-icon.svg) geeft een voorinstelling voor het mapprofielniveau aan.

- **Gewijzigd**: Wijst op als de kaart DITA na de laatste publicatie werd bijgewerkt. Op basis van deze informatie kunt u beslissen of u de uitvoer voor deze DITA-kaart wilt activeren.
- **Gepubliceerd**: Toont de datum en de tijd van de laatste gepubliceerde (of geactiveerde) output. Als u de koppeling selecteert, wordt de pagina Activeringsresultaten weergegeven. Deze pagina bevat de logbestanden met informatie over het hoofdpad waar de inhoud is geactiveerd.
  ![ gecreeerde bulkactivering inzamelingsgeschiedenis tabel ](images/bulk-collection-audit-history.png){width="800" align="left"}

  *Mening de informatie over de geactiveerde kaartoutput in de **Geschiedenis van de Controle**tabel.*


  >[!NOTE]
  >
  > De output in het **lusje van de Geschiedenis van de Controle** wordt gesorteerd gebaseerd op de **Gepubliceerde** kolom.



## Deelvenster Links

De volgende filteropties zijn beschikbaar in het linkerdeelvenster:

- **Gewijzigd**: U kunt ja of Nr selecteren. Als u ja selecteert, slechts worden de gewijzigde kaarten DITA getoond. Een gewijzigde kaart is een kaart die is gegenereerd sinds deze voor het laatst is gepubliceerd.
- **vooraf ingesteld**: Selecteer vooraf ingesteld waarvoor u de kaartdossiers wilt uit filtreren. In deze kolom wordt de titel weergegeven van de uitvoervoorinstelling die in het kaartbestand is geconfigureerd. Bijvoorbeeld, als u *AEM* vooraf ingestelde Plaats kiest, dan slechts worden die kaarten getoond die de *AEM* output hebben die op hen wordt gevormd.
- **Taal**: U kunt om het even welke beschikbare taalcodes selecteren en slechts de geselecteerde taal tonen in de Kaarten en stelt tabel vooraf in.

De filters worden bijgewerkt wanneer u van de **Kaarten en vooraf instelt** lusje aan het **lusje van de Geschiedenis van de Controle** schakelt en vice versa.

**Bovenliggend onderwerp: **[ Bulk Activering van gepubliceerde inhoud ](conf-bulk-activation.md)
