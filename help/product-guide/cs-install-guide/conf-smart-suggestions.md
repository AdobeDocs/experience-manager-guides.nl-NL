---
title: De slimme suggesties voor het ontwerpen configureren
description: Leer hoe u de slimme suggesties voor het ontwerpen configureert
exl-id: a595ca1f-0123-40d3-a79c-a066bc6517b4
source-git-commit: d3e0c475ebd50a2664ea45c293d34b3a10772633
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 0%

---

# De door AI aangedreven slimme suggesties voor het ontwerpen configureren

Als beheerder, kunt u de Slimme eigenschap van Suggesties voor de auteurs vormen. De service voor slimme suggesties wordt beveiligd door verificatie op basis van auteigenschappen van Adobe IMS. Integreer uw omgeving met beveiligde tokengebaseerde verificatieworkflows van de Adobe en gebruik de nieuwe functie voor slimme suggesties. De volgende configuratiehulp u om het **AI configuratie** lusje aan omslagprofiel toe te voegen. Zodra toegevoegd, kunt u de slimme suggesties eigenschap in de Redacteur van het Web gebruiken.

## IMS-configuraties maken in Adobe Developer Console

Voer de volgende stappen uit om IMS-configuraties te maken in Adobe Developer Console:

>[!NOTE]
>
>Als u reeds een project OAuth hebt gecreeerd om op microservice-gebaseerde het publiceren te vormen, kunt u de volgende stappen overslaan om het project tot stand te brengen.

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

   ![ OAuth geloofstegel in vorm API ](assets/conf-ss-OAuth-credential.png)

   *vorm OAuth credential aan uw API.*

1. In het **lusje van Projecten**, kies **OAuth Server aan de optie van de Server** en selecteer dan de pas gecreëerde geloofsbrieven.

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

1. Open Experience Manager en selecteer dan uw programma dat het milieu bevat u wilt vormen.
1. Schakelaar aan de **Milieu&#39;s** tabel.
1. Selecteer de omgevingsnaam die u wilt configureren. Dit zou u aan de **pagina van de Informatie van het Milieu** moeten navigeren.
1. Schakelaar aan de **Configuratie** tabel.
1. Werk het JSON-veld SERVICE_ACCOUNT_DETAILS bij. Zorg ervoor dat u dezelfde naam en configuratie gebruikt als in de volgende schermafbeelding.

![ de configuratie van de de dienstrekening van ims ](assets/ims-service-account-config.png){width="800" align="left"}


*voeg de details van de omgevingsconfiguratie toe.*




Zodra u de configuratie IMS aan het milieu hebt toegevoegd, voer de volgende stappen uit om deze eigenschappen met AEM Guides te verbinden gebruikend OSGi:

1. In u het projectcode van de Git van de wolkenmanager, voeg hieronder twee dossiers (voor dossierinhoud, mening [ Bijlage ](#appendix) toe).

   * `com.adobe.aem.guides.eventing.ImsConfiguratorService.cfg.json`
   * `com.adobe.fmdita.smartsuggest.service.SmartSuggestConfigurationConsumer.cfg.json`
1. Controleer of de toegevoegde bestanden worden gedekt door de `filter.xml` .
1. Leg de Git-wijzigingen vast en duw erop.
1. Voer de pijpleiding in om de veranderingen op het milieu toe te passen.

Zodra dit wordt gedaan, zou u de slimme eigenschap van suggesties moeten kunnen gebruiken.



## Bijlage {#appendix}

**Dossier**:
`com.adobe.aem.guides.eventing.ImsConfiguratorService.cfg.json`

**Inhoud**:

```
{
 "service.account.details": "$[secret:SERVICE_ACCOUNT_DETAILS]",
}
```

**Dossier**: `com.adobe.fmdita.smartsuggest.service.SmartSuggestConfigurationConsumer.cfg.json`

**Inhoud**:

```
{
  "smart.suggestion.flag":true,
  "conref.inline.threshold":0.6,
  "conref.block.threshold":0.7,
  "emerald.url":"https://adobeioruntime.net/apis/543112-smartsuggest/emerald/v1",
  "instance.type":"prod"
}
```

## Configuratiegegevens van slimme suggesties

| Sleutel | Beschrijving | Toegestane waarden | Standaardwaarde |
|---|---|---|---|
| smart.suggestion.flag | Bepaalt of slimme suggesties zijn ingeschakeld | true/false | false |
| conref.inline.threshold | Drempel die de precisie/het terugroepen controleert van suggesties die voor de markering worden gehaald die de gebruiker momenteel typt. | Een waarde tussen -1,0 en 1,0. | 0,6 |
| conref.block.threshold | Drempel die de precisie/terugroeping van suggesties controleert die voor markeringen over het volledige dossier worden gehaald. | Een waarde tussen -1,0 en 1,0. | 0,7 |
| emerald.url | Eindpunt voor de Emerald-vectordatabase | [ https://adobeioruntime.net/apis/543112-smartsuggest/emerald/v1](https://adobeioruntime.net/apis/543112-smartsuggest/emerald/v1) | [ https://adobeioruntime.net/apis/543112-smartsuggest/emerald/v1](https://adobeioruntime.net/apis/543112-smartsuggest/emerald/v1) |
| instance.type | Type AEM instantie. Zorg ervoor dit voor elke AEM instantie uniek is dat de slimme suggesties worden gevormd. Een gebruiksgeval zou zijn om de eigenschap op het milieu van het stadium met &quot;instance.type&quot; = &quot;stadium&quot;te testen terwijl tezelfdertijd de eigenschap ook op &quot;prod&quot;wordt gevormd. | Elke unieke sleutel die de omgeving identificeert. Slechts *alpha numerieke* waarden worden toegestaan. &quot;dev&quot;/&quot;stage&quot;/&quot;prod&quot;/&quot;test1&quot;/&quot;stage2&quot; | &quot;prod&quot; |

Zodra u hebt gevormd, wordt het slimme suggesties pictogram getoond in het juiste paneel van de Redacteur van het Web. U kunt de lijst met slimme suggesties weergeven wanneer u uw onderwerpen bewerkt. Voor meer details, mening [ op AI gebaseerde slimme suggesties voor authoring ](../user-guide/authoring-ai-based-smart-suggestions.md) sectie in de Gids van de Gebruiker van de Experience Manager.
