---
title: Een DITA-project maken
description: Maak een DITA-project met een sjabloon in AEM Guides. Leer hoe u een DITA-project kunt gebruiken om de revisies te starten.
exl-id: 0cd83fe3-1764-4f04-ae11-0b71b6ac576c
feature: Reviewing
role: User
source-git-commit: ae36a7fdff6ae147619340aa3a3d2bb6c7774fe0
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# Een DITA-project maken {#id1645HA00NM6}

Adobe Experience Manager Guides biedt een DITA-projectsjabloon waarmee u revisietaken kunt maken en beheren.

U kunt een DITA-project maken en het vervolgens gebruiken om uw revisies te starten. Met een project kunt u een deadline definiëren en de taken en tijd bepalen die nodig zijn om de overzichtstaak te voltooien waarvoor u het project hebt gemaakt.

U kunt teamleden aan een project toevoegen die dan diverse rollen - Auteurs, Recensenten, en Uitgevers zouden kunnen worden toegewezen.

Nadat u een DITA-project hebt gemaakt, kunt u de revisie starten vanuit de Editor of de gebruikersinterface van Assets. Voor meer details, verzendt de mening [ onderwerpen voor overzicht ](review-send-topics-for-review.md#).

En als een auteur een revisiewerkstroom start, krijgen de geselecteerde leden van het project een e-mailmelding. Om e-mailberichten te vormen, de mening *past e-mailmalplaatjes* aan in installeer en vorm Adobe Experience Manager Guides as a Cloud Service.

Voer de volgende stappen uit om een DITA-project tot stand te brengen:

1. Open Projectconsole.

   U kunt tot de console van Projecten ook toegang hebben gebruikend volgende URL:

   ```http
   http://<server name>:<port>/projects.html
   ```

1. Selecteer **creeer** \> **Project** om de Create tovenaar van het Project te lanceren.

   ![](images/project-console-63.png){width="650" align="left"}

1. Voor de Create pagina van het Project, selecteer het **malplaatje van het Project DITA** en selecteer **daarna**.

1. Voer op de pagina Projecteigenschappen de volgende gegevens in:

   Informatie in het **Basis** lusje:

   ![](images/create-project.png){width="650" align="left"}

   - Ga de Titel van uw project **in**, **Beschrijving**, en **Verschuldigde Datum**.

   - U kunt desgewenst een miniatuur kiezen voor het project.

   - Door gebrek, wordt u gemaakt de eigenaar van het project. Meer gebruikers toevoegen aan dit project:

   1. Ga of kies een gebruiker van de **drop-down lijst van de Gebruiker** in.

   1. Kies een gebruikerstype - Auteurs, Revisoren of Uitgevers.

      >[!NOTE]
      >
      >U zult andere gebruikerstypes in deze drop-down lijst bekijken, maar voor een DITA- project zou u slechts van Auteurs, Recensenten, of de gebruikerstype van Uitgevers moeten kiezen. Zelfs als u een gebruiker van een ander type toevoegt, heeft die gebruiker geen toegang tot DITA-specifieke functies die beschikbaar zijn in Experience Manager Guides.

   1. Selecteer **toevoegen**.

      >[!NOTE]
      >
      >Als u Experience Manager Guides versie 3.5 of eerder gebruikt, wordt u een optie getoond om een DITA kaartdossier te selecteren om zeer belangrijke verwijzingen voor onderwerphet uitgeven, voorproef en overzichtswerkschema&#39;s op te lossen. In 3.6 en latere versies kunt u de hoofdmap instellen via de Editor. Voor meer informatie, bekijk de [ Voorkeur van de Gebruiker ](web-editor-features.md#id2087G0P40SB) in de Redacteur. Een andere manier om de wortelkaart te plaatsen is door het bij de globale of omslag-vlakke profielen te vormen. Voor meer details, vorm de mening *globale of omslag-vlakke profielen* in de Gids van de Installatie en van de Configuratie.

   Informatie in het **Geavanceerde** lusje:

   - Voer een naam in voor het project. Deze naam wordt gebruikt om URL voor dit project tot stand te brengen.

1. Selecteer **creeer**.

   Het dialoogvenster Project gemaakt wordt weergegeven.

1. Selecteer **Open** om uw projectpagina te openen.


**Bovenliggend onderwerp:**[ Inleiding aan overzicht ](review.md)
