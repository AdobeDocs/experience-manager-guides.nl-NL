---
title: Opmerkingen bij de release | Nieuwe functies in de Adobe Experience Manager-hulplijnen, release van december 2023
description: Leer de nieuwe en verbeterde functies in de release van Adobe Experience Manager Guides van december 2023 as a Cloud Service.
feature: What's New
role: Leader
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '1017'
ht-degree: 0%

---

# Nieuwe functies in de release van Adobe Experience Manager Guides van december 2023 as a Cloud Service

Dit artikel behandelt de nieuwe en verbeterde functies in versie december 2023 van Adobe Experience Manager-hulplijnen (later aangeduid als *Experience Manager-hulplijnen as a Cloud Service*).

Voor meer informatie over de upgrade-instructies, compatibiliteitsmatrix en de problemen die in deze release zijn opgelost, raadpleegt u [Opmerkingen bij de release](release-notes-2023.12.0.md).


## Variabelen gebruiken in de PDF-uitvoer

U kunt variabelen gebruiken om herbruikbare informatie dynamisch in te voegen en te beheren. Met de Experience Manager-hulplijnen kunt u tijdens het genereren van de PDF-uitvoer variabelen maken, bewerken en voorvertonen. U kunt snel de waarden van variabelen wijzigen en uw documenten overdraagbaar en gemakkelijk bijwerken.

![native pdf-variabelen](assets/add-variable-default.png){width="800" align="left"}

*Maak en beheer variabelen in de webeditor.*

U kunt ook variabelesets maken die de standaardwaarden overschrijven en alternatieve waarden aan uw variabelen toewijzen. Voeg deze variabelen in de pagina-indeling in en gebruik dezelfde PDF-indeling. U hoeft niet voor elke set waarden een aparte indeling te maken. U kunt bijvoorbeeld een variabele maken voor elke productrelease. Deze variabele kan bestaan uit variabelen voor verschillende productdetails zoals productnaam, versienummer en releasedatum. Vervolgens kunt u verschillende waarden toevoegen voor deze variabelen.

**Variabele set 1: Adobe-set1**

* ProductName: Experience Manager Guides
* Versienummer: 2311
* Releasedatum: 02-11-2023

**Variabele set 2: Adobe-set2**

* ProductName: Experience Manager Guides
* Versienummer: 2310
* Releasedatum: 27-09-2023



<img src="./assets/native-pdf-variable-output.png" alt="Voettekst in PDF-uitvoer" width="500" border="2px">

*Genereer de PDF-uitvoer met behulp van variabelen in de PDF-indeling.*

U kunt stijlen toepassen en markeringen van de HTML gebruiken om de variabelen te formatteren.  U kunt de waarden voor alle variabelen ook snel bijwerken wanneer dat nodig is en de uitvoer opnieuw genereren. Als u bijvoorbeeld de details voor een versie moet bijwerken, kunt u de waarde van de versie in de variabele VersionNumber bewerken en de uitvoer opnieuw genereren.


Meer informatie over het gebruik van [variabelen in de PDF-uitvoer](../native-pdf/native-pdf-variables.md).





## Nieuwe ervaring om de kenmerken te bewerken

U krijgt nu een vernieuwde ervaring om de kenmerken voor een element toe te voegen of te bewerken vanuit het menu **Eigenschappen van inhoud** in de webeditor.

![Deelvenster Kenmerken](assets/attributes-multiple-properties.png){width="300" align="left"}

*Voeg kenmerken toe vanuit het deelvenster Eigenschappen van inhoud.*

U kunt de kenmerken ook gemakkelijk bewerken en verwijderen.

Raadpleeg voor meer informatie de **Eigenschappen van inhoud** functiebeschrijving in het gedeelte [Rechterdeelvenster](../user-guide/web-editor-features.md#id2051EB003YK) sectie.


## Metagegevens bewerken tijdens het ontwerpen

Tijdens het ontwerpen kunt u nu de metagegevenstags voor het bestand bijwerken met behulp van de vervolgkeuzelijst in het dialoogvenster **Bestandseigenschappen** in het rechterdeelvenster. U kunt ook **Meer eigenschappen bewerken** om meer metagegevens bij te werken.

![bestandseigenschappen](assets/file-properties-general.png){width="300" align="left"}

*Werk metagegevens bij en bewerk de bestandseigenschappen vanuit het rechterdeelvenster.*

Raadpleeg voor meer informatie de **Bestandseigenschappen** functiebeschrijving in het gedeelte [Rechterdeelvenster](../user-guide/web-editor-features.md#id2051EB003YK) sectie.

## Capaciteit om inhoud aan de ServiceNow kennisbasis te publiceren

U kunt uw inhoud nu ook publiceren aan het ServiceNow kennisbasisplatform.

Met de versie van December 2023, als beheerder, kunt u een publicatieprofiel voor de ServiceNow kennisbasisserver creëren. Vervolgens kunt u als auteur of uitgever ervoor kiezen dat ServiceNow-publicatieprofiel in de uitvoervoorinstelling bevat om de uitvoer naar de opgegeven kennisbasis te publiceren.

Met deze functie kunt u inhoud, zoals tekst, video&#39;s en afbeeldingen, publiceren naar het ServiceNow-kennisbasisplatform en een uitgebreide opslagplaats onderhouden.


![service nu, voorinstelling kennisbasis](assets/knowledgebase--output-preset.png){width="300" align="left"}

*Creeer een output vooraf ingesteld voor de de kennisbasis ServiceNow.*

Meer informatie over de [Kennisbank](../user-guide/generate-output-knowledge-base.md) uitvoervoorinstellingen.

## Verbeterd dashboard voor kaartverzameling

De Gidsen van de Experience Manager verstrekt een verbeterd dashboard van de inzameling van de Kaart. In een kaartinzameling, kunt u de meta-gegevenseigenschappen voor de kaarten snel vormen DITA. Deze functie is handig omdat u de eigenschappen van metagegevens voor elke DITA-kaart niet afzonderlijk hoeft bij te werken.

U kunt nu de bestandsnaam van de DITA-kaart bekijken. U kunt ook de basislijnen weergeven. Zo kunt u snel de basislijn vinden die voor een voorinstelling wordt gebruikt.

![Kaartverzamelingsdashboard](assets/map-collection-dashboard.png){width="800" align="left"}

*De mening, geeft, en produceert output van het dashboard van de kaartinzameling uit.*

Leer hoe u [gebruik de Inzameling van de Kaart voor outputgeneratie](../user-guide/generate-output-use-map-collection-output-generation.md).

## De belangrijkste attributen van de mening in de Mening van de Kaart

Wanneer u zeer belangrijke attributen voor het onderwerp of kaartverwijzingen bepaalt, kunt u de titel, het overeenkomstige pictogram, en de sleutel in het linkerpaneel ook bekijken. De toets wordt weergegeven als `key=<key-name>`.

Raadpleeg voor meer informatie de **Kaartweergave** functiebeschrijving in het dialoogvenster [Linkerdeelvenster](../user-guide/web-editor-features.md#id2051EA0M0HS) sectie.

![toetsen in de kaartweergave](assets/view-key-title-map-view.png) {width="300" align="left"}

*Bekijk het belangrijkste attribuut in de Mening van de Kaart.*

## De mogelijkheid om een basislijn te dupliceren op basis van een label

De Gidsen van de Experience Manager verstrekt nu een verbeterde gebruikerservaring voor het creëren van de basislijnen van de Redacteur van het Web.\
![nieuwe basislijn maken](assets/create-new-baseline.png) {width="300" align="left"}
*Maak een basislijn van de webeditor.*

Hiermee kunt u ook een basislijn dupliceren op basis van het label. De verwijzingsversie wordt gekozen gebaseerd op het bepaalde etiket (als het bestaat) terwijl het dupliceren, of anders kiest de versie van de gedupliceerde basislijn.


![een basislijn dupliceren ](assets/duplicate-baseline.png) {width="300" align="left"}

*Dupliceer een basislijn op basis van een label of maak een exacte kopie.*

Meer informatie over hoe [basislijnen maken en beheren vanuit de webeditor](../user-guide/web-editor-baseline.md).

## Verbeterd proces voor het maken van bulkactivering van kaartcollectie

Het proces om een inzameling van de bulkactiveringskaart te creëren is nu harmonieer. Wanneer nu de pagina Resultaten van activering wordt weergegeven, kunt u de resultaten van activering en logboekbestanden bekijken.
Raadpleeg voor meer informatie [Een verzameling bulkactiveringskaarten maken](../user-guide/conf-bulk-activation-create-map-collection.md).



## Cross-map koppelingen in de Site-uitvoer oplossen

Gekoppelde koppelingen (XREF met peer bereik) die worden gerenderd in de AEM Site-uitvoer, worden nu omgezet volgens de bestandstitel van de publicatiecontext die is ingesteld voor de gegenereerde kaart.


## De URL van de AEM Site-uitvoer configureren om de documenttitel te gebruiken

Met de hulplijnen voor Experience Managers kunt u als beheerder de URL van de uitvoer van de AEM site configureren. Als de bestandsnaam niet bestaat of niet alle speciale tekens bevat, kunt u deze vervangen door een scheidingsteken in de URL van de AEM Site-uitvoer. U kunt hen met de naam van het eerste kindonderwerp ook vervangen. Leer hoe u [vorm URL van de AEM output van de Plaats om de documenttitel te gebruiken](../cs-install-guide/conf-output-generation.md#configure-the-url-of-the-aem-site-output-to-use-the-document-title).

