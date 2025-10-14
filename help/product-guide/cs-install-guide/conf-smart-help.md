---
title: De slimme Help configureren om inhoud te zoeken
description: Leer hoe u de slimme Help configureert om inhoud te zoeken
source-git-commit: 48f7b38448e821a7ad5931a685dedc95303aea95
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 0%

---


# De door AI aangedreven Smart Help configureren om inhoud te zoeken

Als beheerder, kunt u de Slimme eigenschap van de Hulp voor de auteurs vormen. De Smart Help-service wordt beveiligd door verificatie op basis van auteigenschappen van Adobe IMS. Integreer uw omgeving met beveiligde tokengebaseerde verificatieworkflows van de Adobe en gebruik de nieuwe functie Slimme Help. De volgende configuraties helpen u om het **AI configuratie** lusje aan een omslagprofiel toe te voegen. Zodra toegevoegd, kunt u de Slimme eigenschap van de Hulp in de Redacteur van het Web gebruiken.

## IMS-configuraties maken in Adobe Developer Console

Voer de volgende stappen uit om IMS-configuraties te maken in Adobe Developer Console:

>[!NOTE]
>
>Als u reeds een project OAuth hebt gecreeerd om de Slimme eigenschap van Suggesties of op microservice-gebaseerde het publiceren te vormen, kunt u de volgende stappen overslaan om het project tot stand te brengen. U kunt met Stap 8 beginnen.

1. Start [&#x200B; Adobe Developer Console &#x200B;](https://developer.adobe.com/console).
1. Na met succes het programma openen aan Developer Console, zult u het **1&rbrace; scherm van het Huis {bekijken.** Het **1} scherm van het Huis &lbrace;is waar u informatie en snelle verbindingen, met inbegrip van top-navigatiekoppelingen aan Projecten en Downloads gemakkelijk kunt vinden.**
1. Om een nieuw leeg project tot stand te brengen, creeer **nieuw project** van de **Snelle begin** verbindingen.
   ![&#x200B; Snelle beginverbindingen &#x200B;](assets/conf-ss-quick-start.png) {width="550" align="left"}
   *creeer een nieuw project.*

1. Selecteer **API** van het **scherm van Projecten** toevoegen.  **voeg API** scherm toe verschijnt. Dit scherm toont alle beschikbare APIs, Gebeurtenissen, en de diensten voor de producten en de technologieën van de Adobe waarmee u toepassingen kunt ontwikkelen.

1. Selecteer **I/O Beheer API** om het aan uw project toe te voegen.
   ![&#x200B; IO Beheer API &#x200B;](assets/confi-ss-io-management.png)
   *voeg I/O Beheer API aan uw project toe.*

1. Creeer een nieuwe **referentie OAuth** en bewaar het.
   ![&#x200B; OAuth credential tegel in vorm API &#x200B;](assets/conf-ss-OAuth-credential.png) {width="3000" align="left"}
   *vorm OAuth credential aan uw API.*

1. In het **lusje van Projecten**, kies de **OAuth Server aan de optie van de Server** en selecteer dan de pas gecreëerde geloofsbrieven.

1. Selecteer de **Server-aan-Server** verbinding OAuth om de referentie details van uw project te bekijken.

   ![&#x200B; verbonden geloofsbrieven &#x200B;](assets/conf-ss-connected-credentials.png) {width="800" align="left"}

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

![&#x200B; de configuratie van de de dienstrekening van ims &#x200B;](assets/ims-service-account-config.png){width="800" align="left"}


*voeg de details van de omgevingsconfiguratie toe.*




Zodra u de configuratie IMS aan het milieu hebt toegevoegd, voer de volgende stappen uit om deze eigenschappen met AEM Guides te verbinden gebruikend OSGi:

1. In uw het projectcode van de Git van de wolkenmanager, voeg hieronder twee dossiers (voor dossierinhoud, mening [&#x200B; Bijlage &#x200B;](#appendix) toe).

   * `com.adobe.aem.guides.eventing.ImsConfiguratorService.cfg.json`

1. Controleer of de toegevoegde bestanden worden gedekt door de `filter.xml` .
1. Leg de Git-wijzigingen vast en duw erop.
1. Voer de pijpleiding in werking om de veranderingen op het milieu toe te passen.

Zodra dit wordt gedaan, zou u de **Slimme eigenschap van de Hulp** moeten kunnen gebruiken.



## Bijlage {#appendix}

**Dossier**:
`com.adobe.aem.guides.eventing.ImsConfiguratorService.cfg.json`

**Inhoud**:

```
{
 "service.account.details": "$[secret:SERVICE_ACCOUNT_DETAILS]",
}
```


Zodra u hebt gevormd, wordt het **Slimme pictogram van de Hulp** ![&#x200B; Slimme Hulp &#x200B;](assets/smart-help-icon.svg) getoond in het juiste paneel van de Redacteur van het Web. Selecteer het pictogram om het **Slimme paneel van de Hulp** te bekijken.
Voor meer details, bekijk de [&#x200B; AI-Aangedreven Slimme Hulp om inhoud &#x200B;](../user-guide/ai-based-smart-help.md) sectie in de Gids van de Gebruiker van de Experience Manager te zoeken.
