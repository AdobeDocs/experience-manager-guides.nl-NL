---
title: Vorm de medewerker van Gidsen om inhoud te zoeken
description: Leer hoe u de assistent voor hulplijnen configureert om inhoud te zoeken
source-git-commit: 8ac0ed6b867a3efdef750cb19ed4955a67def9ee
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 0%

---


# De assistent voor AI-hulplijnen configureren om inhoud te zoeken

Als beheerder, kunt u de Hulpeigenschap van Gidsen voor de auteurs vormen. De Guides Assistant-service wordt beveiligd door verificatie op basis van auteigenschappen van Adobe IMS. Integreer uw omgeving met beveiligde tokengebaseerde verificatieworkflows van de Adobe en gebruik de nieuwe functie voor hulplijnen-assistent. De volgende configuraties helpen u om het **AI configuratie** lusje aan een omslagprofiel toe te voegen. Zodra toegevoegd, kunt u de Hulpeigenschap van Gidsen in de Redacteur van het Web gebruiken.

## IMS-configuraties maken in Adobe Developer Console

Voer de volgende stappen uit om IMS-configuraties te maken in Adobe Developer Console:

>[!NOTE]
>
>Als u reeds een project OAuth hebt gecreeerd om de Slimme eigenschap van Suggesties of op microservice-gebaseerde het publiceren te vormen, kunt u de volgende stappen overslaan om het project tot stand te brengen.

1. Start [ Adobe Developer Console ](https://developer.adobe.com/console).
1. Na met succes het programma openen aan Developer Console, zult u het **1} scherm van het Huis {bekijken.** Het **1} scherm van het Huis {is waar u informatie en snelle verbindingen, met inbegrip van top-navigatiekoppelingen aan Projecten en Downloads gemakkelijk kunt vinden.**
1. Om een nieuw leeg project tot stand te brengen, creeer **nieuw project** van de **Snelle begin** verbindingen.
   ![ Snelle beginverbindingen ](assets/conf-ss-quick-start.png) {width="550" align="left"}
   *creeer een nieuw project.*

1. Selecteer **API** van het **scherm van Projecten** toevoegen.  **voeg API** scherm toe verschijnt. Dit scherm toont alle beschikbare APIs, Gebeurtenissen, en de diensten voor de producten en de technologieën van de Adobe waarmee u toepassingen kunt ontwikkelen.

1. Selecteer **I/O Beheer API** om het aan uw project toe te voegen.
   ![ IO Beheer API ](assets/confi-ss-io-management.png)
   *voeg I/O Beheer API aan uw project toe.*

1. Creeer een nieuwe **referentie OAuth** en bewaar het.
   ![ OAuth credential tegel in vorm API ](assets/conf-ss-OAuth-credential.png) {width="3000" align="left"}
   *vorm OAuth credential aan uw API.*

1. In het **lusje van Projecten**, kies de **OAuth Server aan de optie van de Server** en selecteer dan de pas gecreëerde geloofsbrieven.

1. Selecteer de **Server-aan-Server** verbinding OAuth om de referentie details van uw project te bekijken.

   ![ verbonden geloofsbrieven ](assets/conf-ss-connected-credentials.png) {width="800" align="left"}

   *verbind met het project om de referentie details te bekijken.*

1. Terugkeer aan het **lusje van Projecten** en selecteer **Overzicht van het Project** op de linkerzijde.

   <img src="assets/project-overview.png" alt="projectoverzicht" width="500">

   *krijgen begonnen op het nieuwe project.*

1. Klik de **knoop van de Download** op de bovenkant om de dienst JSON te downloaden.

   <img src="assets/download-json.png" alt="download json" width="500">

   *Download de dienstdetails JSON.*

U hebt de OAuth-verificatiedetails geconfigureerd en de JSON-servicedetails gedownload. Houd dit bestand bij de hand zoals in de volgende sectie wordt vereist.

### IMS-configuratie toevoegen aan de omgeving

Voer de volgende stappen uit om configuratie IMS aan het milieu toe te voegen:

1. Open Experience Manager en selecteer dan uw programma, dat het milieu bevat u wilt vormen.
1. Schakelaar aan de **Milieu&#39;s** tabel.
1. Selecteer de omgevingsnaam die u wilt configureren. Dit zou u aan de **pagina van de Informatie van het Milieu** moeten navigeren.
1. Schakelaar aan de **Configuratie** tabel.
1. Werk het JSON-veld SERVICE_ACCOUNT_DETAILS bij. Zorg ervoor dat u dezelfde naam en configuratie gebruikt als in de volgende schermafbeelding.

![ de configuratie van de de dienstrekening van ims ](assets/ims-service-account-config.png){width="800" align="left"}


*voeg de details van de omgevingsconfiguratie toe.*




Zodra u de configuratie IMS aan het milieu hebt toegevoegd, voer de volgende stappen uit om deze eigenschappen met AEM Guides te verbinden gebruikend OSGi:

1. In uw het projectcode van de Git van de wolkenmanager, voeg hieronder twee dossiers (voor dossierinhoud, mening [ Bijlage ](#appendix) toe).

   * `com.adobe.aem.guides.eventing.ImsConfiguratorService.cfg.json`

1. Controleer of de toegevoegde bestanden worden gedekt door de `filter.xml` .
1. Leg de Git-wijzigingen vast en duw erop.
1. Voer de pijpleiding in werking om de veranderingen op het milieu toe te passen.

Zodra dit wordt gedaan, zou u de **eigenschap van de Medewerker van Gidsen moeten kunnen gebruiken 0}.**



## Bijlage {#appendix}

**Dossier**:
`com.adobe.aem.guides.eventing.ImsConfiguratorService.cfg.json`

**Inhoud**:

```
{
 "service.account.details": "$[secret:SERVICE_ACCOUNT_DETAILS]",
}
```


Zodra u hebt gevormd, wordt het **Medewerker van Gidsen** ![ Medewerker van Gidsen ](assets/guides-assistant-icon.svg) pictogram getoond in het juiste paneel van de Redacteur van het Web. Selecteer het pictogram om het **Medewerker van Gidsen** paneel te bekijken.
Voor meer details, bekijk de [ AI-Aangedreven Medewerker van Gidsen om inhoud ](../user-guide/ai-based-guides-assistant.md) sectie in de Gids van de Gebruiker van de Experience Manager te zoeken.
