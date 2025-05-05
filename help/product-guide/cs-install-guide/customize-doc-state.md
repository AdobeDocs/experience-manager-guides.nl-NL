---
title: Documentstatussen configureren
description: Leer hoe u documentstatussen kunt configureren
exl-id: ab155879-4472-464d-ab25-6075088d718b
feature: Document State
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '1212'
ht-degree: 0%

---

# Documentstatussen configureren {#id181GB0400UI}

Met AEM Guides kunt u de documentstatussen voor uw DITA-onderwerpen definiëren volgens de vereisten van uw organisatie. U kunt verschillende statussen van het document definiëren, van het begin tot het einde. De eerste status kan bijvoorbeeld Concept zijn en naar Revisie, Goedgekeurd, Vertaald en tot slot naar Gepubliceerd worden verplaatst.

Er zijn twee manieren waarop een onderwerp van één staat aan een andere kan overgaan - handboek en automatisch. De documentstatussen die in een profiel zijn gedefinieerd, kunnen worden gebruikt voor het handmatig wijzigen van de documentstatus. Dit kan van de pagina van Eigenschappen van een onderwerpdossier worden gedaan. U kunt ook bepalen wie het document van het ene naar het andere frame kan verplaatsen. Een auteur kan bijvoorbeeld een document maken en de standaardstatus van het document kan Concept zijn. Wanneer de auteur het document ter controle verzendt, kan hij de documentstatus wijzigen in In-Review. De controleur kan de documentstatus wijzigen in Goedgekeurd of in Concept op basis van het revisieproces. Als het document is goedgekeurd, kan de uitgever de documentstatus wijzigen in Vertaald of Gepubliceerd, afhankelijk van de workflow.

>[!NOTE]
>
> Als een gebruiker tot de *beheerders* groep behoort, kan de gebruiker de staat van een document van om het even welke staat veranderen ongeacht de overgangen van de documentstaat die in het systeem worden bepaald.

## Een documentstatus maken

AEM Guides wordt geleverd met een set standaardstatussen van documenten. Deze staten zijn:

- Concept
- Bewerken
- Evaluatieversie
- Goedgekeurd
- Bekeken
- Gereed

Deze standaardstaten zijn beschikbaar aan alle onderwerpen DITA die onder DAM worden gecreeerd. U kunt uw eigen documentstaten maken en deze toewijzen aan een specifieke map. Alle DITA-bestanden die in die map worden gemaakt, hebben vervolgens toegang tot de nieuwe documentstatussen.

Voer de volgende stappen uit om documentstatussen te maken met behulp van het mapprofiel:

1. Klik op de verbinding van Adobe Experience Manager bij de bovenkant en kies **Hulpmiddelen**.
1. Selecteer **Gidsen** van de lijst van hulpmiddelen.
1. Klik op de tegel Documentstatussen.

   De pagina Assets States wordt weergegeven. Standaard wordt op de pagina een standaardprofiel weergegeven.

1. Klik **creëren Profiel** en ga de volgende details in:
   - Voer in het veld Profiel de naam voor het profiel in.
   - Geef het pad op waarop u het nieuwe profiel wilt toepassen.
   - Specificeer de staten van het document in de **Toegestane Staten** onder **Staten**. De standaarddocumentstatussen zijn Concept, Bewerken, In-Review, Goedgekeurd en Gereed.-

     Klik **toevoegen** knoop om een documentstaat toe te voegen.

      - Klik op het pictogram Verwijderen om een documentstatus te verwijderen.

     >[!NOTE]
     >
     > Verwijder geen documentstatus als de documenten zich nog in die status bevinden. Als u een documentstaat schrapt, zult u niet de documentstaat van dergelijke documenten kunnen veranderen tenzij u tot de *beheerder* gebruikersgroep behoort.

   - Specificeer de beginstaat van het document in de **Staat van het Begin**.
   - Specificeer de eindstaat van het document in de **Staat van het Eind**.
   - Specificeer de staatsovergang van het document in **van** en **aan** onder **Overgang van de Staat**.

      - Specificeer de gebruikers en gebruikersgroepen die de documentstaat in **Groepen** kunnen veranderen.

      - Klik **toevoegen** knoop om een staatsovergang toe te voegen.

      - Klik op het pictogram Verwijderen om een frameovergang te verwijderen.

     >[!NOTE]
     >
     > Verwijder een statusovergang niet als de documenten nog steeds de status `From` hebben. Als u een staatsovergang schrapt, zult u niet de documentstaat van dergelijke documenten kunnen veranderen tenzij u tot de *beheerder* gebruikersgroep behoort.

1. Klik **Gedaan**.

## Een kopie van een documentstatusprofiel maken

Afhankelijk van uw vereiste kunt u een kopie van een bestaand documentstatusprofiel maken. U kunt de kopie gebruiken als basis voor het maken van een ander documentprofiel.

Voer de volgende stappen uit om een kopie van een documentstatusprofiel te maken:

1. Klik op de verbinding van Adobe Experience Manager bij de bovenkant en kies **Hulpmiddelen**.
1. Selecteer **Gidsen** van de lijst van hulpmiddelen.
1. Klik op de tegel Documentstatussen.

   De pagina Assets States wordt weergegeven.

1. Selecteer het profiel van de documentstaat dat u wilt dupliceren en **klikken dupliceert Profiel**.
1. Breng vereiste veranderingen aan en klik **Gedaan**.

## Een documentstatus of statusovergang verwijderen

>[!NOTE]
>
> Verwijder een documentstatus of statusovergang niet als de documenten zich nog in de status of in een statusovergang bevinden. Als u een staat of staatsovergang schrapt, zult u niet de documentstaat van dergelijke documenten kunnen veranderen tenzij u tot de *beheerder* gebruikersgroep behoort.

Voer de volgende stappen uit om een documentstatus of statusovergang te verwijderen uit een documentstatusprofiel:

1. Klik op de verbinding van Adobe Experience Manager bij de bovenkant en kies **Hulpmiddelen**.
1. Selecteer **Gidsen** van de lijst van hulpmiddelen.
1. Klik op de tegel Documentstatussen.

   De pagina Assets States wordt weergegeven.

1. Selecteer het profiel van de documentstaat van waar u de documentstaat wilt schrappen en **klikken geeft Profiel** uit.
1. Schrap de documentstaat of staatsovergang en klik **Gedaan**.

## Een documentstatusprofiel verwijderen

Voer de volgende stappen uit om een documentstatusprofiel te verwijderen:

1. Klik op de verbinding van Adobe Experience Manager bij de bovenkant en kies **Hulpmiddelen**.
1. Selecteer **Gidsen** van de lijst van hulpmiddelen.
1. Klik op de **tegel van de Staten van het 0&rbrace; Document &lbrace;.**

   De pagina Assets States wordt weergegeven.

1. Selecteer het profiel van de documentstaat dat u wilt schrappen en **Profiel van de Schrapping** klikken.

## De documentstatuswijziging automatiseren

Als u de documentstatus niet handmatig wilt wijzigen, kunt u een workflow maken en de wijziging van de documentstatus automatiseren.

>[!NOTE]
>
> Geautomatiseerde workflows moeten in overeenstemming zijn met de documentstatussen en overgangen die in de configuratie zijn gedefinieerd. Het systeem voert geen controles uit op statuswijzigingen die via geautomatiseerde workflows zijn uitgevoerd.

1. Klik op de verbinding van Adobe Experience Manager bij de bovenkant en kies **Hulpmiddelen**.
1. Selecteer **Werkschema** van de lijst van hulpmiddelen.

1. Klik op de **tegel van 0&rbrace; Modellen &lbrace;.**

1. Selecteer de relevante workflow, Lees de onderwerpen van de revisie.

1. Klik **uitgeven**.

   De workflow wordt geopend op een nieuw tabblad.

1. Klik **uitgeven** \ (top-right \).

1. Open **Stappen** browser; het gebruiken **Knevel Zijpaneel**, bij de verre linkerzijde van de hoogste toolbar

1. Sleep de gewenste stap naar de gewenste locatie in het model.

1. Klik de nieuwe stap u in het werkschemamodel toevoegde en **selecteert vormt** van de componententoolbar

1. Open het **Proces** lusje.

1. In de **drop-down lijst van het Proces**, uitgezochte **plaats de Staat van het Document voor Om het even welk element DAM**.

1. Selecteer de **optie van de vooruitgang van de 0&rbrace; Handler &lbrace;.**

   ![](assets/update-workflow-doc-state_cs.png)

1. In het **de tekstvakje van Argumenten**, ga een documentstaat in waarnaar u van het geselecteerde werkschema wilt overgaan.

   >[!NOTE]
   >
   > Zorg ervoor dat u de juiste documentstatus invoert in het tekstvak Argumenten. Als u een onjuiste waarde opgeeft, wordt de status van het document onjuist.

1. Bevestig de verandering met **sparen &amp; sluit**.


## Goedkeuringswerkstroom inschakelen

AEM Guides biedt een workflow voor documentgoedkeuring waarmee u de levenscyclus van het ontwikkelingsproces van uw document kunt bepalen. Voer de volgende stappen uit om de goedkeuringswerkstroom in te schakelen:

1. U kunt als beheerder het configuratiebestand van de gebruikersinterface downloaden door u aan te melden bij Adobe Experience Manager.

1. Klik op de verbinding van Adobe Experience Manager bij de bovenkant en kies **Hulpmiddelen**.
1. Selecteer **Gidsen** van de lijst van hulpmiddelen en klik de **Profielen van de Omslag**.
1. Klik op de **Globale tegel van het Profiel**.
1. Selecteer het **lusje van de Configuratie van de Redacteur van XML** en klik **uitgeven** pictogram op de bovenkant
1. Klik het **pictogram van de Download** om het ui \_config.json- dossier op uw lokaal systeem te downloaden. Vervolgens kunt u wijzigingen in het bestand aanbrengen en het bestand vervolgens uploaden.
1. In het `ui_config.json` dossier, laat de eigenschap van het goedkeuringswerkschema door de *eigenschappen* sectie te veranderen zoals hieronder getoond:

   ```
   "features":  
   { 
      "approvalWorkflow":  true 
   }
   ```

1. Sla het bestand op en upload het.
