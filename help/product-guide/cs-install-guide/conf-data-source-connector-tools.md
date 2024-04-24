---
title: Vorm een gegevensbronschakelaar gebruikend hulpmiddelen
description: Leer hoe te om een gegevensbronschakelaar te vormen gebruikend de hulpmiddelen.
exl-id: d7cd412b-89ea-43a5-97b3-09944863bbee
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: acd16f23a7b3023a62b3c15007b03d4f3b2cfb4f
workflow-type: tm+mt
source-wordcount: '788'
ht-degree: 0%

---

# Vorm een gegevensbronschakelaar van het gebruikersinterface

De Gidsen van de Experience Manager komt met **Gegevensbronnen** hulpmiddel dat u helpt uit-van-de-doosschakelaars voor gegevensbronnen vormen. U kunt opstelling JIRA, SQL (MySQL, PostgreSQL, de Server van Microsoft SQL, SQLite, MariaDB, H2DB), de schakelaars van de Cliënt van de Handel van Adobe, Elasticsearch, en Algemene REST.

Naast deze out-of-the-box schakelaars, verstrekt de Gidsen van de Experience Manager de schakelaars voor Salsify, Akeneo, en Microsoft Azure DevOps Boards (ADO) gegevensbronnen. U kunt ze downloaden en installeren. De gebruikers kunnen deze schakelaars dan vormen.

U kunt ook verbinding maken met JSON-gegevensbestanden via een bestandsconnector. Upload het JSON-bestand van uw computer of blader erdoor vanaf de Adobe Experience Manager-elementen. Creëer vervolgens inhoudsfragmenten of -onderwerpen met behulp van de generatoren.

Voer de volgende stappen uit om een connector te configureren:

1. Selecteer de **Adobe Experience Manager** en kies Gereedschappen.
1. Selecteren **Hulplijnen** in de lijst met gereedschappen.
1. Selecteer de **Gegevensbronnen** tegel. De **Gegevensbronnen** wordt weergegeven. U kunt de verbonden gegevensbronnen weergeven.

   U kunt schakelen tussen de **Lijstweergave** of **Tegelweergave** om de verschillende verbonden gegevensbronnen als een lijst of als tegels te bekijken.

   <img src="./assets/data-sources-create-window.png" alt= "gegevensbronnen vermeld op de pagina met gegevensbronnen" width="800">

   *Een gegevensbronaansluiting weergeven of maken.*
1. Klikken **Maken**.
1. Selecteer het gegevensbestand waarvoor u de schakelaar wilt tot stand brengen. Bijvoorbeeld, de schakelaar van de Elasticsearch.
   >[!NOTE]
   >
   >Alle beschikbare out-of-the-box gegevensbestanden zijn vermeld.

1. Klik op **Next**.
1. Voer de configuratie- en verbindingsgegevens in volgens de database.

   >[!TIP]
   >
   >* Overslaan <img src="./assets/info-details.svg" alt= "info icon" width="25"> in de buurt van het veld voor meer informatie.
   > * Velden met * zijn verplicht. U kunt bijvoorbeeld de volgende gegevens invoeren voor de aansluiting van de Elasticsearch.

   * **Naam**: Voer de naam van de gegevensbron in.
   * **Type verificatie**: Selecteer het type verificatie in de keuzelijst. Voorbeeld: Basic username-password authentication
   * **Gebruikersnaam**: Voer uw gebruikersnaam in.
   * **Wachtwoord**: Voer uw gebruikersnaam en wachtwoord in.
   * **URL**: Voeg de API-URL toe.


1. Selecteer de **Fabriekssjablonen uitsluiten** optie om de fabrieksmalplaatjes van voor onderwerp en fragmentgeneratie uit te sluiten worden gebruikt. Zij worden niet onder de **Gegevenstoewijzingssjabloon** vervolgkeuzelijst  **Generator voor inhoudsfragmenten toevoegen** of de **Onderwerpgenerator toevoegen** in.


1. Selecteren **Verbinding testen**. U kunt de **Verbinding testen** Deze knop is alleen ingeschakeld nadat u de vereiste details hebt toegevoegd. Een succesbericht weergeven als de verbindingsgegevens juist zijn. Anders wordt mogelijk een foutbericht weergegeven.



1. Selecteren **Opslaan** op de bovenkant om de schakelaar te bewaren.     De weergave **Opslaan** ingeschakeld nadat u alle details hebt ingevuld en de verbinding tot stand is gebracht.


   Als de connector is opgeslagen, kunt u de verbonden gegevensbron op de pagina weergeven.

**Verbinding maken met meerdere bronnen**

U kunt veelvoudige middelen toevoegen of gebruiken die op verschillende URLs voor sommige schakelaars zoals Generische Cliënt van de REST, Salsify, Akeneo, en Microsoft Azure DevOps Boards (ADO) worden gebaseerd. Dan, verbind met hen om inhoudsfragmenten of onderwerpen tot stand te brengen gebruikend de generators voor hen.

Voer de volgende stappen uit om een bron te maken:

1. Selecteren ![pictogram toevoegen](assets/Add_icon.svg) in de **Sectie URL-bron** om een bron voor elke URL toe te voegen.
1. Configureer alle details in het dialoogvenster **Bron toevoegen** in.
1. Klikken **Toevoegen**.
1. U kunt ![bewerkingspictogram](assets/edit_pencil_icon.svg) of verwijderen ![delete](assets/Delete_icon.svg) de bron in de URL-bronlijst.

1. U kunt ook de standaardbronnen gebruiken die beschikbaar zijn voor gegevensbronnen zoals Salsify, Akeneo en Microsoft ADO. Schakel de opties UIT voor de bron die u niet wilt configureren voor een gegevensbron.

Dit helpt u om gegevens van om het even welke middelen voor een bepaalde gegevensbron in één enkel inhoudsfragment of onderwerp snel te halen.

## Beschikbare functies voor een aansluiting

* Schakelen tussen de **Lijstweergave** of **Tegelweergave**  om de verschillende verbonden gegevensbronnen als een lijst of als tegels te bekijken.
* Schakel het selectievakje voor één aansluiting in. Klikken **Alles selecteren** om alle schakelaars te selecteren. U kunt op **Alle selecties opheffen** wanneer alle schakelaars worden geselecteerd.

<img src="./assets/data-sources-features.png" alt= "kenmerken van de gegevensbronnen op de pagina met gegevensbronnen" width="800">

*Een gegevensbronaansluiting bewerken, opnieuw verbinden, dupliceren of verwijderen.*

U kunt de volgende functies gebruiken voor de aansluiting op de **Gegevensbronnen** pagina:

* **Bewerken**: Bewerk de configuratiedetails voor de geselecteerde connector.

* **Opnieuw verbinden**: Opnieuw verbinden met een losgekoppelde connector.

* **Dupliceren**: Maak een nieuwe dubbele connector met de huidige connector als basis. De dubbele schakelaar wordt gecreeerd met een achtervoegsel (als connectorname_1) door gebrek. Bijvoorbeeld: sample-elastic-search_1.
U bekijkt een fout als de schakelaar met de zelfde naam bestaat.

* **Verwijderen**: Verwijder de geselecteerde connector.


Zodra u de gegevensbron hebt gevormd, is de schakelaar vermeld onder **Deelvenster Gegevensbronnen** in de webeditor. U kunt dan met de gegevensbron verbinden en een inhoudsfragment opnemen in uw onderwerpen. Voor meer informatie, bekijkt u [Een inhoudsfragment uit uw gegevensbron invoegen](../user-guide/web-editor-content-snippet.md).
