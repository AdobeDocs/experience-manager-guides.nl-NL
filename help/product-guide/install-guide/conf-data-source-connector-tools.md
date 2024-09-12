---
title: Vorm een gegevensbronschakelaar gebruikend hulpmiddelen
description: Leer hoe te om een gegevensbronschakelaar te vormen gebruikend de hulpmiddelen.
exl-id: 2a0ac0a0-b2a9-453e-851b-fb04c8903526
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 1eb4fcb33d6f905df3f543232e7040d1da42560b
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 0%

---

# Vorm een gegevensbronschakelaar van het gebruikersinterface

Experience Manager Guides komt met het **hulpmiddel van Gegevensbronnen** dat u helpt uit-van-de-doosschakelaars voor gegevensbronnen vormen. U kunt opstellingsschakelaars voor JIRA, SQL (MySQL, PostgreSQL, de Server van Microsoft SQL, SQLite, MariaDB, H2DB), de gegevensbestanden van de Handel van Adobe, en van de Elasticsearch.

Voer de volgende stappen uit om een connector te configureren:

1. Selecteer de **verbinding van Adobe Experience Manager** bij de bovenkant en kies Hulpmiddelen.
1. Selecteer **Gidsen** van de lijst van hulpmiddelen.
1. Selecteer de **Bronnen van Gegevens** tegel. De **pagina van Gegevensbronnen** wordt getoond. U kunt de verbonden gegevensbronnen weergeven.

   U kunt tussen de **Mening van de Lijst van een knevel voorzien** of **Blokmening** om de diverse verbonden gegevensbronnen als lijst of als tegels te bekijken.

   <img src="./assets/data-sources-create-window.png" alt= "gegevensbronnen vermeld op de pagina met gegevensbronnen" width="800">

   *Mening of creeer een gegevensbronschakelaar.*
1. Klik **creëren**.
1. Selecteer het gegevensbestand waarvoor u de schakelaar wilt tot stand brengen. Bijvoorbeeld, de schakelaar van de Elasticsearch.
   >[!NOTE]
   >
   >Alle beschikbare out-of-the-box gegevensbestanden zijn vermeld.

1. Klik op **Next**.
1. Voer de configuratie- en verbindingsgegevens in volgens de database.

   >[!TIP]
   >* Overslaan <img src="./assets/info-details.svg" alt= "info icon" width="25"> in de buurt van het veld voor meer informatie.
   > * Velden met * zijn verplicht. U kunt bijvoorbeeld de volgende gegevens invoeren voor de aansluiting van de Elasticsearch.

   * **Naam**: Ga de naam van de gegevensbron in.
   * Verificatietype: selecteer het type verificatie in het keuzemenu. Voorbeeld: Basic username-password authentication
   * **Gebruikersnaam**: Ga uw gebruikersbenaming in.
   * **Wachtwoord**: Ga uw gebruikersbenaming en wachtwoord in.
   * **URL**: Voeg API URL toe.

1. Selecteer **verbinding van de Test**. U kunt de **toegelaten knoop van de Verbinding van de Test** bekijken slechts nadat u de vereiste details toevoegt. Een succesbericht weergeven als de verbindingsgegevens juist zijn. Anders wordt mogelijk een foutbericht weergegeven.



1. Selecteer **sparen** op de bovenkant om de schakelaar te bewaren.     Bekijk **sparen** toegelaten knoop nadat u alle details vult en de verbinding succesvol is.


   Als de connector is opgeslagen, kunt u de verbonden gegevensbron op de pagina weergeven.

## Beschikbare functies voor een aansluiting

* Wisselen tussen de **Mening van de Lijst** of **Blokmening** om de diverse verbonden gegevensbronnen als lijst of als tegels te bekijken.
* Schakel het selectievakje voor één aansluiting in. Klik **Uitgezocht allen** om alle schakelaars te selecteren. U kunt **klikken schrap allen** wanneer alle schakelaars worden geselecteerd.

<img src="./assets/data-sources-features.png" alt= "kenmerken van de gegevensbronnen op de pagina met gegevensbronnen" width="800">

*geef, maak opnieuw aan, dupliceerde, of schrap een gegevensbronschakelaar.*

U kunt de volgende eigenschappen voor de schakelaar op de **Bronnen van Gegevens** pagina gebruiken:

* **geeft** uit: geef de configuratiedetails voor de geselecteerde schakelaar uit.

* **opnieuw verbinden**: Verbind opnieuw met een losgemaakte schakelaar.

* **Dupliceer**: Creeer een nieuwe dubbele schakelaar gebruikend de huidige schakelaar als basis. De dubbele schakelaar wordt gecreeerd met een achtervoegsel (als connectorname_1) door gebrek. Bijvoorbeeld: sample-elastic-search_1.
U bekijkt een fout als de schakelaar met de zelfde naam bestaat.

* **Schrapping**: Schrap de geselecteerde schakelaar.


Zodra u de gegevensbron hebt gevormd, is de schakelaar vermeld onder het **paneel van Gegevensbronnen** in de Redacteur van het Web. U kunt dan met de gegevensbron verbinden en een inhoudsfragment opnemen in uw onderwerpen. Voor meer details, mening [ Gegevens van het Gebruik van uw gegevensbron ](../user-guide/web-editor-content-snippet.md).

>[!NOTE]
>
>U kunt ook aangepaste connectors maken en deze gebruiken met de verschillende gegevensbronnen. Leer hoe te om [ douaneschakelaars ](../knowledge-base/kb-articles/data-source/conf-custom-data-source-connector.md) te vormen.