---
title: Vorm een gegevensbronschakelaar gebruikend hulpmiddelen
description: Leer hoe te om een gegevensbronschakelaar te vormen gebruikend de hulpmiddelen.
exl-id: d7cd412b-89ea-43a5-97b3-09944863bbee
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: c790d5edd1ab799564aebfa96f4a41288c977a6c
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 0%

---

# Vorm een gegevensbronschakelaar van het gebruikersinterface

Experience Manager Guides komt met het **hulpmiddel van Gegevensbronnen** dat u helpt uit-van-de-doosschakelaars voor gegevensbronnen vormen. U kunt de verbindingen JIRA, SQL (MySQL, PostgreSQL, Microsoft SQL Server, SQLite, MariaDB, H2DB), AdobeCommerce, Elasticsearch en Generic REST Client instellen.


Naast deze kant-en-klare connectors biedt Experience Manager Guides de connectors voor Salsify-, Akeneo- en Microsoft Azure DevOps Boards (ADO)-gegevensbronnen. U kunt deze open-bronschakelaars van de [&#x200B; Gemaakt Centrale bewaarplaats downloaden en installeren &#x200B;](https://central.sonatype.com/search?q=com.adobe.aem.addon.guides). De gebruikers kunnen deze schakelaars dan vormen.
Leer hoe te [&#x200B; een open-bronschakelaar &#x200B;](#install-open-source-connector) installeren.



U kunt ook verbinding maken met JSON-gegevensbestanden via een bestandsconnector. Upload het JSON-bestand van uw computer of blader erdoor vanaf de Adobe Experience Manager-elementen. Creëer vervolgens inhoudsfragmenten of -onderwerpen met behulp van de generatoren.

Voer de volgende stappen uit om een connector te configureren:

1. Selecteer de **verbinding van Adobe Experience Manager** bij de bovenkant en kies Hulpmiddelen.
1. Selecteer **Gidsen** van de lijst van hulpmiddelen.
1. Selecteer de **Bronnen van Gegevens** tegel. De **pagina van Gegevensbronnen** wordt getoond. U kunt de verbonden gegevensbronnen weergeven.

   U kunt tussen de **Mening van de Lijst van een knevel voorzien** of **Blokmening** om de diverse verbonden gegevensbronnen als lijst of als tegels te bekijken.

   <img src="./assets/data-sources-create-window.png" alt= "gegevensbronnen vermeld op de pagina met gegevensbronnen" width="800">

   *Mening of creeer een gegevensbronschakelaar.*

1. Klik **creëren**.
1. Selecteer het gegevensbestand waarvoor u de schakelaar wilt tot stand brengen. Bijvoorbeeld de Elasticsearch-aansluiting.

   >[!NOTE]
   >
   >Alle beschikbare out-of-the-box gegevensbestanden zijn vermeld.

1. Klik op **Next**.
1. Voer de configuratie- en verbindingsgegevens in volgens de database.

   >[!TIP]
   >
   >* Overslaan <img src="./assets/info-details.svg" alt= "info icon" width="25"> in de buurt van het veld voor meer informatie.
   >* Velden met * zijn verplicht. U kunt bijvoorbeeld de volgende gegevens invoeren voor de Elasticsearch-aansluiting.

   * **Naam**: Ga de naam van de gegevensbron in.
   * **Type van Authentificatie**: Selecteer het type van authentificatie van drop-down. Voorbeeld: Basic username-password authentication
   * **Gebruikersnaam**: Ga uw gebruikersbenaming in.
   * **Wachtwoord**: Ga uw gebruikersbenaming en wachtwoord in.
   * **URL**: Voeg API URL toe.


1. Selecteer de **Uitgesloten fabrieksmalplaatjes** optie om de fabrieksmalplaatjes van voor onderwerp en fragmentgeneratie uit te sluiten worden gebruikt. Zij zullen niet onder het **de kaartmalplaatje van Gegevens** dropdown in **verschijnen toevoegen inhoudsfragmentgenerator** of **toevoegen onderwerpgenerator** dialoogdoos.
1. Selecteer **verbinding van de Test**. U kunt de **toegelaten knoop van de Verbinding van de Test** bekijken slechts nadat u de vereiste details toevoegt. Een succesbericht weergeven als de verbindingsgegevens juist zijn. Anders wordt mogelijk een foutbericht weergegeven.
1. Selecteer **sparen** op de bovenkant om de schakelaar te bewaren.     Bekijk **sparen** toegelaten knoop nadat u alle details vult en de verbinding succesvol is.


   Als de connector is opgeslagen, kunt u de verbonden gegevensbron op de pagina weergeven.

**verbind met veelvoudige middelen**

U kunt veelvoudige middelen toevoegen of gebruiken die op verschillende URLs voor sommige schakelaars zoals Generische Cliënt van de REST, Salsify, Akeneo, en Microsoft Azure DevOps Boards (ADO) worden gebaseerd. Dan, verbind met hen om inhoudsfragmenten of onderwerpen tot stand te brengen gebruikend de generators voor hen.

Voer de volgende stappen uit om een bron te maken:

1. Selecteer ![&#x200B; pictogram &#x200B;](assets/Add_icon.svg) in de **het middelsectie van URL** toevoegen om een middel voor elke URL toe te voegen.
1. Vorm alle details in **voeg middel** dialoogdoos toe.
1. Klik **toevoegen**.
1. U kunt ![&#x200B; uitgeven pictogram &#x200B;](assets/edit_pencil_icon.svg) of schrapt ![&#x200B; &#x200B;](assets/Delete_icon.svg) het middel van de URL middellijst.
1. U kunt ook de standaardbronnen gebruiken die beschikbaar zijn voor gegevensbronnen zoals Salsify, Akeneo en Microsoft ADO. Schakel de opties UIT voor de bron die u niet wilt configureren voor een gegevensbron.

Dit helpt u om gegevens van om het even welke middelen voor een bepaalde gegevensbron in één enkel inhoudsfragment of onderwerp snel te halen.



## Een opensource-connector installeren{#install-open-source-connector}

Om een gebiedsdeel te publiceren dat op de [&#x200B; Gemaakt Centrale bewaarplaats &#x200B;](https://central.sonatype.com/search?q=com.adobe.aem.addon.guides) aan de Diensten van de Wolk aanwezig is, moet u het gebiedsdeel voor een open-bronschakelaar omvatten en inbedden.

1. Voeg de afhankelijkheid in `all/pom.xml` toe in de projectcode van Git voor cloudbeheer. U kunt bijvoorbeeld de volgende afhankelijkheid toevoegen voor de gegevensbronaansluiting van Microsoft Azure DevOps Boards.


   ```
   <dependency>
       <groupId>com.adobe.aem.addon.guides</groupId>
       <artifactId>konnect-azure-devops</artifactId>
       <version>1.0.0</version>
       <type>jar</type>
   </dependency> 
   ```

1. Sluit de toegevoegde afhankelijkheid in.

   ```
   <embedded>
       <groupId>com.adobe.aem.addon.guides</groupId>
       <artifactId>konnect-azure-devops</artifactId>
       <type>jar</type>
       <target>/apps/aemdoxonaemcsstageprogram-vendor-packages/content/install</target>
   </embedded> 
   ```

1. Voer de pijplijn uit om de wijzigingen in de Cloud Services toe te passen.
De connector wordt in uw omgeving geïnstalleerd.


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


Zodra u de gegevensbron hebt gevormd, is de schakelaar vermeld onder het **paneel van Gegevensbronnen** in de Redacteur van het Web. U kunt dan met de gegevensbron verbinden en een inhoudsfragment opnemen in uw onderwerpen. Voor meer details, neemt de mening [&#x200B; een inhoudsfragment van uw gegevensbron &#x200B;](../user-guide/web-editor-content-snippet.md) op.

