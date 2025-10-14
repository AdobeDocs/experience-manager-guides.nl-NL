---
title: Opmerkingen bij de release | Nieuwe functies in de Adobe Experience Manager Guides, release december 2023
description: Leer de nieuwe en verbeterde functies in de release van Adobe Experience Manager Guides as a Cloud Service van december 2023.
feature: What's New
role: Leader
exl-id: bf8d98e9-97fe-4195-9286-60d8517ab19c
source-git-commit: e40ebf4122decc431d0abb2cdf1794ea704e5496
workflow-type: tm+mt
source-wordcount: '966'
ht-degree: 0%

---

# Nieuwe functies in de release van Adobe Experience Manager Guides as a Cloud Service van december 2023

Dit artikel behandelt de nieuwe en verbeterde eigenschappen in versie December 2023 van Adobe Experience Manager Guides (later die als *wordt bedoeld Experience Manager Guides as a Cloud Service*).

Voor meer details op de verbeteringsinstructies, verenigbaarheidsmatrijs, en de kwesties die in deze versie worden bevestigd, mening [&#x200B; de Nota&#39;s van de Versie &#x200B;](release-notes-2023-12-0.md).


## Variabelen gebruiken in de PDF-uitvoer

U kunt variabelen gebruiken om herbruikbare informatie dynamisch in te voegen en te beheren. Met Experience Manager Guides kunt u tijdens het genereren van de PDF-uitvoer variabelen maken, bewerken en voorvertonen. U kunt snel de waarden van variabelen wijzigen en uw documenten overdraagbaar en gemakkelijk bijwerken.

![&#x200B; inheemse pdf variabelen &#x200B;](assets/add-variable-default.png){width="800" align="left"}

*creeer en beheer variabelen in de Redacteur van het Web.*

U kunt ook variabelesets maken die de standaardwaarden overschrijven en alternatieve waarden aan uw variabelen toewijzen. Voeg deze variabelen in de pagina-indeling in en gebruik dezelfde PDF-indeling. U hoeft niet voor elke set waarden een aparte indeling te maken. U kunt bijvoorbeeld een variabele maken voor elke productrelease. Deze variabele kan bestaan uit variabelen voor verschillende productdetails zoals productnaam, versienummer en releasedatum. Vervolgens kunt u verschillende waarden toevoegen voor deze variabelen.

**Veranderlijke reeks 1: Adobe-set1**

* Productnaam: Experience Manager Guides
* Versienummer: 2311
* Releasedatum: 02-11-2023

**Veranderlijke reeks 2: Adobe-set2**

* Productnaam: Experience Manager Guides
* Versienummer: 2310
* Releasedatum: 27-09-2023



<img src="./assets/native-pdf-variable-output.png" alt="Voettekst in PDF-uitvoer" width="500" border="2px">

*produceer de output van de PDF gebruikend variabelen in de lay-out van de PDF.*

U kunt stijlen toepassen en markeringen van de HTML gebruiken om de variabelen te formatteren.  U kunt de waarden voor alle variabelen ook snel bijwerken wanneer dat nodig is en de uitvoer opnieuw genereren. Als u bijvoorbeeld de details voor een versie moet bijwerken, kunt u de waarde van de versie in de variabele VersionNumber bewerken en de uitvoer opnieuw genereren.


Leer meer over hoe te om [&#x200B; variabelen in de output van PDF &#x200B;](../native-pdf/native-pdf-variables.md) te gebruiken.





## Nieuwe ervaring om de kenmerken te bewerken

Nu, krijgt u een vernieuwde ervaring om de attributen voor een element van het **paneel van de Eigenschappen van de Inhoud** in de Redacteur van het Web toe te voegen of uit te geven.

![&#x200B; het paneel van Attributen &#x200B;](assets/attributes-multiple-properties.png){width="300" align="left"}

*voegt attributen van het paneel van Eigenschappen van de Inhoud toe.*

U kunt de kenmerken ook gemakkelijk bewerken en verwijderen.

Voor meer details, verwijs naar de **eigenschapbeschrijving van de Eigenschappen van de Inhoud** {binnen de [&#x200B; Juiste 3} sectie van het Comité.](../user-guide/web-editor-features.md#id2051EB003YK)


## Metagegevens bewerken tijdens het ontwerpen

Nu, terwijl het ontwerpen, kunt u de markeringen van dossiermeta-gegevens bijwerken gebruikend dropdown van de **Eigenschappen van het Dossier** in het juiste paneel. U kunt **ook selecteren uitgeeft meer eigenschappen** om meer meta-gegevens bij te werken.

![&#x200B; dossier-eigenschappen &#x200B;](assets/file-properties-general.png){width="300" align="left"}

*de meta-gegevens van de Update en geeft dossiereigenschappen van het juiste paneel uit.*

Voor meer details, verwijs naar de **eigenschapbeschrijving van de Eigenschappen van het 0&rbrace; Dossier {binnen de [&#x200B; Juiste 3} sectie van het Comité.**](../user-guide/web-editor-features.md#id2051EB003YK)

## Capaciteit om inhoud aan de ServiceNow kennisbasis te publiceren

U kunt uw inhoud nu ook publiceren aan het ServiceNow kennisbasisplatform.

Met de versie van December 2023, als beheerder, kunt u een publicatieprofiel voor de ServiceNow kennisbasisserver creëren. Vervolgens kunt u als auteur of uitgever ervoor kiezen dat ServiceNow-publicatieprofiel in de uitvoervoorinstelling bevat om de uitvoer naar de opgegeven kennisbasis te publiceren.

Met deze functie kunt u inhoud, zoals tekst, video&#39;s en afbeeldingen, publiceren naar het ServiceNow-kennisbasisplatform en een uitgebreide opslagplaats onderhouden.


![&#x200B; de dienst nu vooraf ingestelde kennisbasis &#x200B;](assets/knowledgebase--output-preset.png){width="300" align="left"}

*creeer een output vooraf ingesteld voor de de kennisbasis ServiceNow.*

Leer meer over [&#x200B; de outputpresets van de Kennisbank &#x200B;](../user-guide/generate-output-knowledge-base.md).

## Verbeterd dashboard voor kaartverzameling

Experience Manager Guides biedt een uitgebreid dashboard voor kaartverzamelingen. In een kaartinzameling, kunt u de meta-gegevenseigenschappen voor de kaarten snel vormen DITA. Deze functie is handig omdat u de eigenschappen van metagegevens voor elke DITA-kaart niet afzonderlijk hoeft bij te werken.

U kunt nu de bestandsnaam van de DITA-kaart bekijken. U kunt ook de basislijnen weergeven. Zo kunt u snel de basislijn vinden die voor een voorinstelling wordt gebruikt.

![&#x200B; de inzamelingsdashboard van de Kaart &#x200B;](assets/map-collection-dashboard.png){width="800" align="left"}

*Mening, geef, en produceer output van het dashboard van de kaartinzameling uit.*

Leer hoe te [&#x200B; de Inzameling van de gebruiksKaart voor outputgeneratie &#x200B;](../user-guide/generate-output-use-map-collection-output-generation.md).

## De belangrijkste attributen van de mening in de Mening van de Kaart

Wanneer u zeer belangrijke attributen voor het onderwerp of kaartverwijzingen bepaalt, kunt u de titel, het overeenkomstige pictogram, en de sleutel in het linkerpaneel ook bekijken. De toets wordt weergegeven als `key=<key-name>` .

Voor meer details, verwijs naar de **eigenschapbeschrijving van de Mening van de Kaart** &lbrace;in de [&#x200B; Linkerpaneel &#x200B;](../user-guide/web-editor-features.md#id2051EA0M0HS) sectie.

![&#x200B; sleutels in kaartmening &#x200B;](assets/view-key-title-map-view.png) {width="300" align="left"}

*Mening de belangrijkste attributen in de Mening van de Kaart.*

## De mogelijkheid om een basislijn te dupliceren op basis van een label

Experience Manager Guides biedt nu een verbeterde gebruikerservaring voor het maken van de basislijnen in de webeditor.\
![&#x200B; creeer nieuwe basislijn &#x200B;](assets/create-new-baseline.png) {width="300" align="left"}
*creeer basislijn van de Redacteur van het Web.*

Hiermee kunt u ook een basislijn dupliceren op basis van het label. De verwijzingsversie wordt gekozen gebaseerd op het bepaalde etiket (als het bestaat) terwijl het dupliceren, of anders kiest de versie van de gedupliceerde basislijn.


![&#x200B; Een basislijn dupliceren &#x200B;](assets/duplicate-baseline.png) {width="300" align="left"}

*dupliceer een basislijn die op een etiket wordt gebaseerd of creeer een nauwkeurige kopie.*

Leer meer over hoe te om [&#x200B; basislijnen van de Redacteur van het Web &#x200B;](../user-guide/web-editor-baseline.md) tot stand te brengen en te beheren.

## Cross-map koppelingen in de Site-uitvoer oplossen

Gekoppelde koppelingen (XREF met peer bereik) die worden gerenderd in de AEM Site-uitvoer, worden nu omgezet volgens de bestandstitel van de publicatiecontext die is ingesteld voor de gegenereerde kaart.


## De URL van de AEM Site-uitvoer configureren om de documenttitel te gebruiken

Met Experience Manager Guides kunt u als beheerder de URL van de AEM Site-uitvoer configureren. Als de bestandsnaam niet bestaat of niet alle speciale tekens bevat, kunt u deze vervangen door een scheidingsteken in de URL van de AEM Site-uitvoer. U kunt hen met de naam van het eerste kindonderwerp ook vervangen. Leer hoe te [&#x200B; vorm URL van de output van de Plaats van de AEM om de documenttitel &#x200B;](../cs-install-guide/conf-output-generation.md#configure-the-url-of-the-aem-site-output-to-use-the-document-title) te gebruiken.
