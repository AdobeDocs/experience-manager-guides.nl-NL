---
title: Een DITA-project maken
description: Maak een DITA-project met een sjabloon in AEM Guides. Leer hoe u een DITA-project kunt gebruiken om de revisies te starten.
feature: Reviewing
role: User
source-git-commit: 76c731c6a0e496b5b1237b9b9fb84adda8fa8a92
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# Een DITA-project maken {#id1645HA00NM6}

AEM Guides biedt een DITA-projectsjabloon waarmee u revisietaken kunt maken en beheren.

U kunt een DITA-project maken en het vervolgens gebruiken om uw revisies te starten. Met een project kunt u een deadline definiëren en de taken en tijd bepalen die nodig zijn om de overzichtstaak te voltooien waarvoor u het project hebt gemaakt.

U kunt teamleden aan een project toevoegen die dan diverse rollen - Auteurs, Recensenten, en Uitgevers zouden kunnen worden toegewezen.

Zodra u uw project DITA hebt gecreeerd, kunt u uw overzicht van de Redacteur van het Web of de UI van Assets in werking stellen. Voor meer details, zie [ onderwerpen voor overzicht ](review-send-topics-for-review.md#) verzenden.

En als een auteur een revisiewerkstroom start, krijgen de geselecteerde leden van het project een e-mailmelding. Om e-mailberichten te vormen, zie *e-mailmalplaatjes* aanpassen in installeer en vorm as a Cloud Service Adobe Experience Manager Guides.

Voer de volgende stappen uit om een DITA-project tot stand te brengen:

1. Open Projectconsole.

   U kunt tot de console van Projecten ook toegang hebben gebruikend volgende URL:

   ```http
   http://<server name>:<port>/projects.html
   ```

1. Klik **creëren** \> **Project** om de Create tovenaar van het Project te lanceren.

   ![](images/project-console-63.png){width="650" align="left"}

1. Voor de Create pagina van het Project, selecteer het **malplaatje van het Project DITA** en klik **daarna**.

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
      >U zult andere gebruikerstypes in deze drop-down lijst zien, maar voor een DITA- project zou u slechts van Auteurs, Recensenten, of het gebruikerstype van Uitgevers moeten kiezen. Zelfs als u een gebruiker van een ander type toevoegt, heeft die gebruiker geen toegang tot DITA-specifieke functies die beschikbaar zijn in AEM Guides.

   1. Klik **toevoegen**.

      >[!NOTE]
      >
      >Als u AEM Guides versie 3.5 of eerder gebruikt, wordt u een optie getoond om een DITA kaartdossier te selecteren om zeer belangrijke verwijzingen voor onderwerphet uitgeven, voorproef en overzichtswerkschema&#39;s op te lossen. In 3.6 en recentere versies, kunt u de wortelkaart door de Redacteur van het Web plaatsen. Voor meer informatie, zie de [ Voorkeur van de Gebruiker ](web-editor-features.md#id2087G0P40SB) in de Redacteur van het Web. Een andere manier om de wortelkaart te plaatsen is door het bij de globale of omslag-vlakke profielen te vormen. Voor meer details, zie *globale of omslag-vlakke profielen* in de Gids van de Installatie en van de Configuratie vormen.

   Informatie in het **Geavanceerde** lusje:

   - Voer een naam in voor het project. Deze naam wordt gebruikt om URL voor dit project tot stand te brengen.

1. Klik **creëren**.

   Het dialoogvenster Project gemaakt wordt weergegeven.

1. Klik **Open** om uw projectpagina te openen.


**Bovenliggend onderwerp:**[ onderwerpen of kaarten van het Overzicht ](review.md)
