---
title: Nieuwe basislijn (Beta) maken en beheren vanaf de kaartconsole
description: Maak en beheer nieuwe basislijn (Beta) vanaf de kaartconsole in Adobe Experience Manager Guides.
feature: Authoring, Features of Web Editor, Publishing
role: User
exl-id: 574806bb-21c5-41fe-b8be-4c6506ce8cce
source-git-commit: d7e5af83e88de18cd8ac2e849c9d6e1807988099
workflow-type: tm+mt
source-wordcount: '1294'
ht-degree: 0%

---

# Nieuwe basislijn (Beta) in Experience Manager Guides

>[!NOTE]
>
> Dit artikel is op nieuwe basislijn van toepassing, momenteel beschikbaar als a *Beta* eigenschap, die betere prestaties en stabiliteit beschikbaar met Experience Manager Guides 2026.03.0 versie aanbiedt. Om de nieuwe basislijneigenschap in uw opstelling toe te laten, contacteer het Team van het Succes van de Klant.

De nieuwe basislijneigenschap richt kritieke betrouwbaarheid en prestatieskwesties verbonden aan grote, complexe kaarten. Het wordt geleverd met een herontworpen basislijnarchitectuur die een snellere, stabielere en consistentere basislijnervaring biedt. Alvorens wij in de details duiken, is hier een korte doorlichtingsvideo die de mogelijkheden van de nieuwe basislijneigenschap benadrukt.

>[!VIDEO](https://video.tv.adobe.com/v/3483154/aem-guides)

Het nieuwe basislijnmodel versterkt basislijnbehandeling door de gemeenschappelijke pijnpunten aan te pakken:

- Langzaam laden en slechte reactiesnelheid bij het werken met grote basislijnen
- Inconsistente basislijnstaten veroorzaakt door gedeeltelijke updates of mislukte validaties
- Beperkte zichtbaarheid en controle bij het beheren van uitgebreide basislijninhoud
- De knelpunten van prestaties tijdens basislijnverwezenlijking, updates, of herbouwt

De volgende secties beschrijven het nieuwe basislijnmodel, met inbegrip van de verbeteringen het introduceert, belangrijkste gedragsveranderingen om vóór migratie te overwegen, en instructies voor migratie aan en het gebruiken van de nieuwe basislijn:

- [Belangrijke verbeteringen in de nieuwe basislijn](#key-enhancements-introduced-in-the-new-baseline)
- [Gedrag verandert voordat naar de nieuwe basislijn wordt gemigreerd](#behavior-changes-to-know-before-migrating-to-the-new-baseline)
- [Migreren naar nieuwe basislijn](#migrate-to-new-baseline)
- [De nieuwe basislijn gebruiken](#use-the-new-baseline)

## Belangrijke verbeteringen in de nieuwe basislijn

De nieuwe basislijn introduceert significante verbeteringen die basislijnbeheer sneller en gemakkelijker maken om te schrapen zonder te veranderen hoe u werkt. Overweeg naar de nieuwe basislijn voor:

- **Verbeterde prestaties en scalability:** het model en het teruggeven van basislijngegevens gedrag zijn geoptimaliseerd om efficiënt met grote basislijnen te schrapen, gebruikend stijgende lading en een gestroomlijnde gegevensstructuur om ontvankelijkheid te verbeteren.
- **sterkere UI en backendconsistentie:** Om het even welke veranderingen die aan een basislijn (zoals versie of gebiedsupdates) worden aangebracht worden nu weerspiegeld in UI slechts na succesvolle backendbevestiging, die de verwezenlijking van ongeldige basislijnen verhinderen.
- **het Filtreren, het sorteren, en de navigatie:** Baselines steunen het uitvoerige filtreren over veelvoudige attributen, met inbegrip van documentstaat, etiketten, dossiertype, verwijzingstype, en op GUID-Gebaseerd onderzoek over de volledige basislijn. Paginering wordt ondersteund voor grote basislijnen, met een optie voor het opnemen van bestanden zonder labels.
- **Duidelijke zichtbaarheid in gebiedsdeelinvloed:** het effect van de Afhankelijkheid (voor toegevoegde of verwijderde gebiedsdelen) wordt getoond als voorproef alvorens de versieveranderingen worden toegepast, toelatend u om de veranderingen te herzien alvorens hen toe te passen.
- **flexibeler etiketbeheer:** de Etiketten kunnen tussen versies binnen een basislijn worden bewogen, die grotere flexibiliteit verstrekken wanneer het beheren van etiketten over verschillende onderwerpversies.
- **deterministisch het uitgeven en sparen gedrag:** basislijn geeft rij-vlakke updates uit, laadt middel-intensieve gegevens (zoals versiebomen en gebiedsdeelverschillen) slechts tijdens versieupdates, en voltooit sparen verrichtingen deterministisch in één enkele stap - verminderend onverwachte sparen mislukkingen en gedeeltelijke updates.
- **betrouwbaardere basislijnverwezenlijking:** basislijnen worden gecreeerd gebruikend opgeslagen verwijzingsgegevens eerder dan runtime het ontleden, met vereiste versieinformatie die vooraf wordt bevestigd om onvolledige of ongeldige basislijnen te verhinderen.
- **API en automatiseringssteun:** het nieuwe basislijnmodel wordt volledig gesteund door REST APIs en Java SDK, toelatend automatisering en integratie met externe werkschema&#39;s.


## Gedrag verandert voordat naar de nieuwe basislijn wordt gemigreerd

Voordat u naar het nieuwe basislijnmodel gaat, controleert u de volgende gedragswijzigingen. Deze wijzigingen zijn van invloed op de manier waarop basislijnen worden gemaakt, bijgewerkt en beheerd en kunnen van invloed zijn op bestaande workflows.

| Gebied | Wijzigen (beschrijving) |
|------|-------------|
| **resolutie van de Verwijzing** | De directe kaartverwijzingen worden geclassificeerd als **DIRECT**. Ongeldige verwijzingen worden overgeslagen, en verwijzingen van `reltable` blijven worden uitgesloten. |
| **kiezen automatisch** | Versieselectie wordt meteen geëvalueerd voordat directe verwijzingen worden opgelost, zodat een nauwkeurige versiesolutie wordt verkregen. |
| **de aanmaakregels van de Basislijn** | Versie **1.0** is verplicht. Basislijnen met ontbrekende of dubbelzinnige versies kunnen na de migratie anders worden opgelost. |
| **Migratie behandeling** | Ongeldige verwijzingen worden overgeslagen. **DIRECT** de verwijzingen nemen belangrijkheid, unpinned verwijzingen bewegen zich naar de recentste versie, en de extra meta-gegevens worden toegevoegd van versie **5.0** verder. |
| **het gegevensmodel van de Basislijn** | Het nieuwe op grafiek-gebaseerde basislijnmodel verwijdert veranderbare gebieden en is achterwaarts compatibel met het vorige basislijnmodel. |
| **API gebruik** | Basislijnbewerkingen worden ondersteund via REST API&#39;s en de Java SDK. Onbewerkte basislijnobjecten worden niet meer weergegeven. |
| **het zuiveren van de Versie** | Na migratie wordt bij het opschonen van versies alleen rekening gehouden met basislijnen die zijn opgeslagen in de nieuwe basislijnopslagruimte. |

## Migreren naar nieuwe basislijn

Zodra u de eigenschap hebt die van het Team van het Succes van de Klant wordt toegelaten, moet u de bestaande basislijnen aan de nieuwe basislijn migreren.

Voer de volgende stappen uit om de bestaande basislijn naar de nieuwe basislijn te migreren.

1. Selecteer het embleem van Adobe Experience Manager bij de bovenkant en kies **Hulpmiddelen**.
1. In het **paneel van Hulpmiddelen** uitgezocht **Gidsen**.
1. Selecteer de **tegel van de Bewerker van 0&rbrace; Bulk &lbrace;.**

   ![&#x200B; stroom-activa-bewerker &#x200B;](images/flow-asset-processor.png){align="left"}

   De **pagina van de Bewerker van het Bulk van Gidsen** wordt getoond.

1. Selecteer **Nieuw Proces** van de hoogste juiste hoek van de pagina om een nieuwe verwerkingstaak te beginnen.

   Het **Nieuwe proces** dialoog wordt getoond.

1. Geef de volgende gegevens op in het dialoogvenster:

   1. **type van Eigenschap**: Selecteer **Basislijn** van de daling neer.
   1. **Uitgezochte omslag(en) en dossier(s)**: Navigeer en kies één of veelvoudige omslagen en dossiers om te verwerken.
   1. **Uitgezochte omslag(en) om** te negeren: Naar keuze, selecteer subfolders binnen de gekozen ouderomslag om van de migratie uit te sluiten.

   ![&#x200B; nieuw-proces-basislijn &#x200B;](images/new-process-baseline.png){align="left"}

1. Selecteer **creeer**.

Een pop-up die **activa tonen met succes teweeggebrachte verwerking van Activa** wordt getoond. U kunt de status van de verwerkingstaak op de pagina weergeven.

U kunt **Logboeken van de Mening** ook selecteren om de logboeken voor de migratietaak te controleren en te downloaden.

![&#x200B; mening-logboeken-basislijn &#x200B;](images/view-logs-baseline.png){align="left"}

Het lograpport bevat details over de migratie, zoals het aantal kaarten dat is gemigreerd, de basislijnen die met succes zijn gemigreerd en de bijbehorende details.

![&#x200B; logboeken-detail-basislijn &#x200B;](images/logs-detail-baseline.png){align="left"}

>[!NOTE]
>
> Tijdens de migratie mogen geen basisbewerkingen worden uitgevoerd, met name in werkkopieën, om storingen te voorkomen. Na de migratie moeten bepaalde basislijnen mogelijk opnieuw worden opgebouwd als versies ontbreken.

## De nieuwe basislijn gebruiken

Het nieuwe basislijnmodel gebruikt dezelfde workflows en gebruikersinterface als de bestaande basislijnfunctie in Experience Manager Guides. U kunt [&#x200B; blijven creëren en basislijn van de console van de Kaart beheren &#x200B;](./web-editor-baseline.md) gebruikend de beschikbare opties.

>[!NOTE]
>
> Het nieuwe basislijnmodel ondersteunt het maken en beheren van basislijnen van het dashboard Kaart niet.

In deze sectie worden alleen de wijzigingen en verbeteringen beschreven die zijn geïntroduceerd met het nieuwe basislijnmodel. Algemene basislijnworkflows blijven ongewijzigd, tenzij dit expliciet wordt vermeld.

**Nieuwe/verbeterde opties beschikbaar in de nieuwe basislijn UI**

De volgende updates zijn van toepassing wanneer het werken met gecreeerde basislijnen gebruikend het **nieuwe basislijnmodel**:

- De **basislijnoptie van de Uitvoer** in het menu van Opties wordt anders genoemd **Download** voor basislijnen die zowel Handmatig als Automatische updates worden gecreeerd.

  ![](images/baseline-v2-options-menu.png)

- De dynamische basislijnen kunnen direct van het **paneel van de Basislijn** worden geopend en worden geleid gebruikend de beschikbare acties in het menu van Opties.

  ![](images/baseline-v2-dynamic-baseline-new.png)

  U kunt ook de nieuwe opties gebruiken die zijn geïntroduceerd voor dynamische basislijnen die zijn gemaakt met het nieuwe basislijnmodel:
   - **geeft eigenschappen** uit: Staat u toe om de eigenschappen van een bestaande basislijn uit te geven.
   - **herbouwt**: Staat u toe om een dynamische basislijn opnieuw te bouwen wanneer de veranderingen voorkomen.

     ![&#x200B; rebuild-baseline &#x200B;](images/rebuild-baseline.png){align="left"}

- De **Download** actie steunt gepagineerde downloads. Alle basislijninhoud die overeenkomt met de toegepaste filters, wordt opgenomen in de download en niet alleen de inhoud die zichtbaar is op de huidige pagina.
- Filter bestanden op GUID, naast bestandsnamen of bestandslocatie. Een extra optie aan **dossiers van de Filter zonder etiketten** is ook beschikbaar.

  ![](images/baseline-v2-filters.png)
- Het nieuwe basislijnmodel ondersteunt deterministische bewerkingen, zodat u één referentie tegelijk kunt bijwerken met gevalideerde afhankelijkheidsresolutie.

  +++Stappen voor het bewerken van de referenties van een nieuwe basislijn

  Voer de volgende stappen uit om bewerkingen op een basislijn uit te voeren:

   - Open de basislijn van het **paneel van de Basislijn**.

     De tabelweergave van de referenties van de basislijnen wordt weergegeven.

   - Navigeer naar en houd de muisaanwijzer boven het bestand dat u wilt bewerken.
   - Selecteer **uitgeven** pictogram.

     ![&#x200B; geef-basislijn-pictogram uit &#x200B;](images/edit-baseline-icon.png){align="left"}

     Het **geeft versie** dialoog uit wordt getoond.
   - Selecteer de vereiste versie van **drop-down van de Versie** (bijvoorbeeld, verandering van versie 1.0 in 1.1).


     ![&#x200B; uitgeven-versie-basislijn &#x200B;](images/edit-version-baseline.png){align="left"}

     Toegevoegde en verwijderde afhankelijkheden worden geëvalueerd en als voorvertoning weergegeven. Controleer de wijzigingen voordat u ze toepast.

     ![](images/baseline-v2-version-added.png)

     Als geen gebiedsdeelveranderingen worden ontdekt, wordt een leeg-staat bericht getoond.

   - Selecteer **Update** om de veranderingen toe te passen.

  De basislijn wordt bijgewerkt met de geselecteerde versie.
  +++
