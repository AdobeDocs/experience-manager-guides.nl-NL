---
title: Vorm de medewerker van Gidsen om inhoud te zoeken
description: Leer hoe u de assistent voor hulplijnen configureert om inhoud te zoeken
source-git-commit: 8ac0ed6b867a3efdef750cb19ed4955a67def9ee
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 0%

---


# De assistent voor AI-hulplijnen configureren om inhoud te zoeken

Als beheerder, kunt u de Hulpeigenschap van Gidsen voor de auteurs vormen. De Guides Assistant-service wordt beveiligd door verificatie op basis van auteigenschappen van Adobe IMS. Integreer uw omgeving met beveiligde tokengebaseerde verificatieworkflows van de Adobe en gebruik de nieuwe functie voor hulplijnen-assistent. Met de volgende configuraties kunt u de **AI-configuratie** naar een mapprofiel. Zodra toegevoegd, kunt u de Hulpeigenschap van Gidsen in de Redacteur van het Web gebruiken.

## IMS-configuraties maken in Adobe Developer Console

Voer de volgende stappen uit om IMS-configuraties te maken in Adobe Developer Console:

>[!NOTE]
>
>Als u reeds een project OAuth hebt gecreeerd om de Slimme eigenschap van Suggesties of op microservice-gebaseerde het publiceren te vormen, kunt u de volgende stappen overslaan om het project tot stand te brengen.

1. Starten [Adobe Developer Console](https://developer.adobe.com/console).
1. Nadat u zich met succes hebt aangemeld bij de Developer Console, kunt u de **Home** scherm. De **Home** het scherm is waar u informatie en snelle verbindingen, met inbegrip van top-navigatiekoppelingen aan Projecten en Downloads gemakkelijk kunt vinden.
1. Als u een nieuw, leeg project wilt maken, selecteert u **Nieuw project maken** van de **Snel starten** koppelingen.
   ![Koppelingen snel starten](assets/conf-ss-quick-start.png) {width="550" align="left"}
   *Maak een nieuw project.*

1. Selecteren **API toevoegen** van de **Projecten** scherm.  De **Een API toevoegen** wordt weergegeven. Dit scherm toont alle beschikbare APIs, Gebeurtenissen, en de diensten voor de producten en de technologieën van de Adobe waarmee u toepassingen kunt ontwikkelen.

1. Selecteer de **API voor I/O-beheer** om het aan uw project toe te voegen.
   ![IO Management API](assets/confi-ss-io-management.png)
   *Voeg API voor I/O-beheer toe aan uw project.*

1. Een nieuwe **OAuth-referentie** en sla deze op.
   ![OAuth-referentietegel in configuratie-API](assets/conf-ss-OAuth-credential.png) {width="3000" align="left"}
   *Configureer de OAuth-referentie voor uw API.*

1. In de  **Projecten** kiest u de **OAuth Server naar Server** en selecteert u vervolgens de nieuwe referenties.

1. Selecteer de **OAuth Server-to-Server** koppeling om de referentie-details van uw project weer te geven.

   ![verbonden referenties](assets/conf-ss-connected-credentials.png) {width="800" align="left"}

   *Maak verbinding met het project om de referentie-details weer te geven.*

1. Terugkeren naar de **Projecten** en selecteert u **Overzicht van project** links.

   <img src="assets/project-overview.png" alt="projectoverzicht" width="500">

   *Ga aan de slag met het nieuwe project.*

1. Klik op de knop **Downloaden** bovenaan om de service JSON te downloaden.

   <img src="assets/download-json.png" alt="download json" width="500">

   *Download de JSON-servicegegevens.*

U hebt de OAuth-verificatiedetails geconfigureerd en de JSON-servicedetails gedownload. Houd dit bestand bij de hand zoals in de volgende sectie wordt vereist.

### IMS-configuratie toevoegen aan de omgeving

Voer de volgende stappen uit om configuratie IMS aan het milieu toe te voegen:

1. Open Experience Manager en selecteer dan uw programma, dat het milieu bevat u wilt vormen.
1. Schakel over naar de **Omgevingen** tab.
1. Selecteer de omgevingsnaam die u wilt configureren. Ga dan naar de **Omgevingsinformatie** pagina.
1. Schakel over naar de **Configuratie** tab.
1. Werk het JSON-veld SERVICE_ACCOUNT_DETAILS bij. Zorg ervoor dat u dezelfde naam en configuratie gebruikt als in de volgende schermafbeelding.

![ims-serviceconfiguratie](assets/ims-service-account-config.png){width="800" align="left"}


*Voeg de details van de omgevingsconfiguratie toe.*




Zodra u de configuratie IMS aan het milieu hebt toegevoegd, voer de volgende stappen uit om deze eigenschappen met AEM Gidsen te verbinden gebruikend OSGi:

1. Voeg in de projectcode voor Git voor cloudbeheer de onderstaande twee bestanden toe (voor bestandsinhoud, weergave [Bijlage](#appendix)).

   * `com.adobe.aem.guides.eventing.ImsConfiguratorService.cfg.json`

1. Zorg ervoor dat de toegevoegde bestanden worden gedekt door uw `filter.xml`.
1. Leg de Git-wijzigingen vast en duw erop.
1. Voer de pijpleiding in werking om de veranderingen op het milieu toe te passen.

Als dit is gebeurd, kunt u de knop **Hulplijnen, assistent** gebruiken.



## Bijlage {#appendix}

**Bestand**:
`com.adobe.aem.guides.eventing.ImsConfiguratorService.cfg.json`

**Inhoud**:

```
{
 "service.account.details": "$[secret:SERVICE_ACCOUNT_DETAILS]",
}
```


Zodra u hebt gevormd, **Hulplijnen, assistent** ![Hulplijnen, assistent](assets/guides-assistant-icon.svg) wordt weergegeven in het rechterdeelvenster van de webeditor. Selecteer het pictogram om het **Hulplijnen, assistent** deelvenster.
Voor meer informatie bekijkt u de [AI-assistent voor hulplijnen om inhoud te zoeken](../user-guide/ai-based-guides-assistant.md) in de gebruikershandleiding van de Experience Manager.
