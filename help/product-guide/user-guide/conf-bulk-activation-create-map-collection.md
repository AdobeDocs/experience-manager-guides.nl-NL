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

1. Selecteren **Hulplijnen** in de lijst met gereedschappen.

1. Selecteer de Adobe Experience Manager-koppeling bovenaan en kies **Gereedschappen**.

1. Selecteer de **Bulk publicatiedashboard** tegel.

   Voor het eerst wordt een lege verzamelingspagina weergegeven. Als u eerder bulkactiveringsverzamelingen hebt gemaakt, worden deze op deze pagina weergegeven.

1. Klikken **Maken**.

1. Voer een titel in voor uw bulkactiveringskaartverzameling en klik op **Maken**.

   Een succesbericht wordt getoond bij de verwezenlijking van de bulkactivering kaartinzameling.

1. Klikken **Openen** over de succesboodschap.

1. Selecteren **Bewerken** en selecteer vervolgens **Kaarten toevoegen**.

1. Zoek en voeg de DITA-kaarten toe die u aan de bulkactiveringskaartverzameling wilt toevoegen.

   Standaard worden alle voorinstellingen en landinstellingen die aan de kaart zijn gekoppeld, automatisch toegevoegd.

1. Selecteer de gewenste uitvoer door de schuifknop in of uit te schakelen.

   U kunt meerdere uitvoervoorinstellingen kiezen voor alle beschikbare landinstellingen.

1. Klikken **Gereed**.

De DITA kaartdossiers worden toegevoegd aan uw bulkactiveringskaartinzameling.

![ gemaakte bulkactivering](images/bulk-activation-collection-created.png){width="800" align="left"}

## Tabblad Kaarten en voorinstellingen

De **Kaarten en voorinstellingen** tabblad bevat informatie in de volgende kolommen:

- **Kaart**: geeft de titel van het DITA-kaartbestand weer.
- **Pad toewijzen**: geeft het volledige pad van het DITA-kaartbestand weer.

- **UUID**: Hiermee wordt de unieke id weergegeven die aan het bestand is gekoppeld.

- **Taal**: Geeft de taalcode van de DITA-kaart weer.
- **Voorinstelling**: Hiermee geeft u de titel weer van de uitvoervoorinstelling die in het kaartbestand is geconfigureerd. Het pictogram wordt ook weergegeven op basis van het type uitvoervoorinstelling.

  >[!NOTE]
  >
  > De kleine ![](images/global-preset-icon.svg) geeft een voorinstelling voor het mapprofielniveau aan.

- **gewijzigd**: Geeft aan of de DITA-kaart wordt bijgewerkt na de laatste publicatie. Op basis van deze informatie kunt u beslissen of u de uitvoer voor deze DITA-kaart wilt activeren.
- **Gegenereerd**: Geeft de datum en tijd weer van de laatst gegenereerde uitvoer.
- **Gepubliceerd**: Geeft de datum en tijd weer van de laatst gepubliceerde (of geactiveerde) uitvoer. Als u de koppeling selecteert, wordt **Activeringsresultaten** wordt weergegeven, die de logboekbestanden bevat met informatie over het hoofdpad waar de inhoud is geactiveerd.

## Tabblad Controlegeschiedenis

De **Controlegeschiedenis** tab bevat informatie over de geactiveerde kaartuitvoer in de volgende kolommen:
- **Kaart**: geeft de titel van het DITA-kaartbestand weer.
- **Pad toewijzen**: geeft het volledige pad van het DITA-kaartbestand weer.
- **UUID** : Hiermee wordt de unieke id weergegeven die aan het bestand is gekoppeld.
- **Taal**: Geeft de taalcode van de DITA-kaart weer.
- **Voorinstelling**: Hiermee geeft u de titel weer van de uitvoervoorinstelling die in het kaartbestand is geconfigureerd. Het pictogram wordt ook weergegeven op basis van het type uitvoervoorinstelling.
- **Status**: Geeft aan dat de activeringsstatus is gelukt of niet.
- **Doel**: Als u de uitvoer genereert op as a Cloud Service hulplijnen voor Experience Managers, kunt u de bestemming van de uitvoer weergeven als Publiceren of Voorvertoning.

  >[!NOTE]
  >
  > De kleine ![](images/global-preset-icon.svg) geeft een voorinstelling voor het mapprofielniveau aan.

- **gewijzigd**: Geeft aan of de DITA-kaart is bijgewerkt na de laatste publicatie. Op basis van deze informatie kunt u beslissen of u de uitvoer voor deze DITA-kaart wilt activeren.
- **Gepubliceerd**: Geeft de datum en tijd weer van de laatst gepubliceerde (of geactiveerde) uitvoer. Als u de koppeling selecteert, wordt de pagina Activeringsresultaten weergegeven. Deze pagina bevat de logbestanden met informatie over het hoofdpad waar de inhoud is geactiveerd.
  ![ gemaakt tabblad Geschiedenis van collectie voor bulkactivering](images/bulk-collection-audit-history.png){width="800" align="left"}

  *Bekijk de informatie over de geactiveerde kaartuitvoer in het dialoogvenster **Controlegeschiedenis**tab.*


  >[!NOTE]
  >
  > De uitvoer in de **Controlegeschiedenis** worden gesorteerd op basis van de **Gepubliceerd** kolom.



## Deelvenster Links

De volgende filteropties zijn beschikbaar in het linkerdeelvenster:

- **gewijzigd**: U kunt Ja of Nee selecteren. Als u ja selecteert, slechts worden de gewijzigde kaarten DITA getoond. Een gewijzigde kaart is een kaart die is gegenereerd sinds deze voor het laatst is gepubliceerd.
- **Voorinstelling**: Selecteer een voorinstelling waarvoor u de kaartbestanden wilt uitfilteren. In deze kolom wordt de titel weergegeven van de uitvoervoorinstelling die in het kaartbestand is geconfigureerd. Als u bijvoorbeeld *Site AEM* voorinstelling, worden alleen de kaarten weergegeven die de *Site AEM* uitvoervoorinstelling geconfigureerd op deze apparaten.
- **Taal**: U kunt alle beschikbare taalcodes selecteren en alleen de geselecteerde taal weergeven op het tabblad Kaarten en Voorinstellingen.

De filters worden bijgewerkt wanneer u van **Kaarten en voorinstellingen** aan de **Controlegeschiedenis** en omgekeerd.

**Bovenliggend onderwerp: **[Bulkactivering van gepubliceerde inhoud](conf-bulk-activation.md)
