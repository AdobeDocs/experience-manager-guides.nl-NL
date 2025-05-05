---
title: Op microservice gebaseerde publicaties configureren met OAuth-verificatie voor AEM Guides as a Cloud Service
description: Leer hoe u op microservices gebaseerde publicaties kunt configureren met OAuth-verificatie voor AEM Guides.
feature: Microservice in AEM Guides
role: Admin
exl-id: db0c83c7-1ece-4010-b214-f8d806d26bc9
source-git-commit: c51a372dc44921a489219f5ac99e3ad180ccc91d
workflow-type: tm+mt
source-wordcount: '827'
ht-degree: 0%

---

# Op microservice gebaseerde publicaties configureren met OAuth-verificatie

Met de publicatiemicroservice kunt u grote publicatiewerklasten tegelijkertijd uitvoeren op Experience Manager Guides as a Cloud Service en profiteren van het toonaangevende Adobe I/O Runtime-serverloze platform.

Voor elke publicatieaanvraag voert Experience Manager Guides as a Cloud Service een aparte container uit die horizontaal wordt geschaald op basis van de gebruikersaanvragen. Dit biedt de mogelijkheid om meerdere publicatieverzoeken uit te voeren en betere prestaties te krijgen dan hun grote On-premise Adobe Experience Manager-servers.

>[!NOTE]
>
> Op microservices gebaseerde publicaties in Experience Manager Guides ondersteunen de typen uitvoervoorinstellingen PDF (zowel op basis van Native als DITA-OT), HTML5, JSON en CUSTOM.

Aangezien de service voor publicatie in de cloud wordt beveiligd door verificatie op basis van OAuth van Adobe IMS, voert u de volgende stappen uit om hun omgevingen te integreren met beveiligde tokengebaseerde verificatieworkflows van de Adobe en de op de cloud gebaseerde schaalbare publicatieoplossing te gaan gebruiken.


## IMS-configuraties maken in Adobe Developer Console

**Rol die wordt vereist om de configuraties** te creëren: De Beheerder van het systeem

Voer de volgende stappen uit om configuraties IMS in **Adobe Developer Console** tot stand te brengen:

>[!NOTE]
>
>Als u reeds een project OAuth hebt gecreeerd om de op AI-Gebaseerde slimme suggesties voor creatie te vormen, kunt u de volgende stappen overslaan om het project tot stand te brengen.

1. Open **Developer Console**: `https://developer.adobe.com/console`.

1. Schakelaar aan het **lusje van Projecten** van de bovenkant.

   <img src="assets/projects-tab.png" alt="tabblad Projecten" width="500">

   *selecteer het **Projecten**&#x200B;lusje op **Adobe Developer Console***

1. Om een nieuw leeg project tot stand te brengen, selecteer **Leeg project** van **creeer nieuwe project** dropdown.

   <img src="assets/create-new-project.png" alt="nieuw project maken" width="500">

   *creeer een nieuw leeg project.*

1. Selecteer **API** van **toevoegen aan project** dropdown om IO Beheer API aan uw project toe te voegen.

   <img src="assets/add-project.png" alt="project toevoegen" width="300">

   *selecteer een API project van dropdown.*

   <img src="assets/io-management-api.png" alt="io-beheer" width="500">

   *voeg I/O Beheer API aan uw project toe.*

1. Maak een nieuwe OAuth-referentie en sla deze op.

   <img src="assets/microservice-api-oauth.png" alt="sleutelpaar genereren" width="500">

   *vorm OAuth credential aan uw API.*


1. Terugkeer aan het **lusje van Projecten** en selecteer **Overzicht van het Project** op de linkerzijde.

   <img src="assets/project-overview.png" alt="projectoverzicht" width="500">

   *krijgen begonnen op het nieuwe project.*

1. Klik de **knoop van de Download** op de bovenkant om de dienst JSON te downloaden.

   <img src="assets/download-json.png" alt="download json" width="500">

   *Download de dienstdetails JSON.*

U hebt de OAuth-verificatiedetails geconfigureerd en de JSON-servicedetails gedownload. Houd dit bestand bij de hand zoals in de volgende sectie wordt vereist.


## IMS-configuratie toevoegen aan de omgeving

>[!NOTE]
>
>Als u reeds een project OAuth voor slimme suggesties hebt gecreeerd, dan kunt u het zelfde project voor microservices opnieuw gebruiken en de volgende stappen overslaan om configuratie IMS aan het milieu toe te voegen.

### Bestaande configuratie bijwerken (JWT   naar OAuth shift )

Als u al een microservice gebruikt voor publicatie met behulp van JWT (afgekeurd), voert u de volgende stappen uit om de configuraties bij te werken:



1. Open **Experience Manager** en selecteer het programma dat het milieu bevat dat u wilt vormen.
1. Schakelaar aan de **Milieu&#39;s** tabel.
1. Selecteer de naam van het milieu dat u wilt vormen. Dit zou u aan de **pagina van de Informatie van het Milieu** moeten navigeren.
1. Schakelaar aan de **Configuratie** tabel.

1. Werk het JSON-veld SERVICE_ACCOUNT_DETAILS bij met het nieuwe OAuth JSON-bestand dat u hebt gedownload.
1. Verwijder het veld PRIVATE_KEY.



   <img src="assets/ims-service-account-config.png" alt="ims-serviceconfiguratie" width="500">

   *werk de bestaande JWT omgevingsconfiguraties bij.*

### Eerste configuratie

Als u een publicatiemicroservice voor het eerst wilt gebruiken, werkt u de configuraties bij volgens de volgende stappen:
1. Open **Experience Manager** en selecteer het programma dat het milieu bevat u wilt vormen.
1. Schakelaar aan de **Milieu&#39;s** tabel.
1. Selecteer de naam van het milieu dat u wilt vormen. Dit zou u aan de **pagina van de Informatie van het Milieu** moeten navigeren.
1. Schakelaar aan de **Configuratie** tabel.

1. Creeer een nieuwe configuratie genoemd als SERVICE_ACCOUNT_DETAILS. Voeg als waarde de inhoud van het OAuth JSON-bestand toe die u hebt gedownload van de ontwikkelaarsconsole.


<img src="assets/jws-service-account-config.png" alt="ims-serviceconfiguratie" width="500">

*vorm het milieu voor het eerst.*


### De eerste keer codeveranderingen voor op microservice-gebaseerde het publiceren enablement

>[!NOTE]
>
> Sla de volgende stappen over als u al op microservice gebaseerde publicaties gebruikt:

Zodra u de configuratie IMS aan het milieu hebt toegevoegd, voer de volgende stappen uit om deze eigenschappen met Experience Manager Guides te verbinden gebruikend OSGi:

1. In uw het projectcode van de Git van de wolkenmanager, voeg de volgende twee dossiers in `/apps/fmditaCustom/config` toe (voor dossierinhoud, mening [ Bijlage ](#appendix)).

   * `com.adobe.aem.guides.eventing.ImsConfiguratorService.cfg.json`
   * `com.adobe.fmdita.publishworkflow.PublishWorkflowConfigurationService.xml`
1. Controleer of de toegevoegde bestanden worden gedekt door de `filter.xml` .
1. Leg de Git-wijzigingen vast en duw erop.
1. Voer de pijpleiding in werking om de veranderingen op het milieu toe te passen.

Zodra dit wordt gedaan, kunt u de op microservice-gebaseerde wolkenpublicatie gebruiken.

## Veelgestelde vragen


1. Als de configuraties OSGi om microservice te gebruiken worden toegelaten, zal het het publiceren proces op de lokale server van de Experience Manager met de zelfde codebase werken?
   * Nee, als de markering `dxml.use.publish.microservice` is ingesteld op `true` , zoekt deze altijd naar microserviceconfiguraties. Stel `dxml.use.publish.microservice` in op `false` zodat het publiceren werkt op uw lokale server.
1. Hoeveel geheugen wordt toegewezen aan het proces DITA wanneer het gebruiken van op microservice-gebaseerde het publiceren? Wordt dit aangestuurd via het DITA-profiel en de parameters?
   * Bij publicatie op basis van microservices wordt geheugentoewijzing niet door het DITA-profiel en de DITA-parameters gestuurd. Het totale beschikbare geheugen op de de dienstcontainer is 8 GB, waarvan 6 GB aan het DITA-OT proces wordt toegewezen.


## Bijlage {#appendix}

**Dossier**:
`com.adobe.aem.guides.eventing.ImsConfiguratorService.cfg.json`

**Inhoud**:

```
{
"service.account.details": "$[secret:SERVICE_ACCOUNT_DETAILS]",
}
```

**Dossier**: `com.adobe.fmdita.publishworkflow.PublishWorkflowConfigurationService.xml`

**Inhoud**:
* `dxml.use.publish.microservice`: schakel over naar het inschakelen van op microservice gebaseerde publicaties met DITA-OT
* `dxml.use.publish.microservice.native.pdf`: schakel over naar het inschakelen van op microservice gebaseerde Native PDF-publicaties

```
<?xml version="1.0" encoding="UTF-8"?>
<jcr:root xmlns:jcr="http://www.jcp.org/jcr/1.0" xmlns:sling="http://sling.apache.org/jcr/sling/1.0"
          jcr:primaryType="sling:OsgiConfig"
          dxml.publish.microservice.url="https://adobeioruntime.net/api/v1/web/543112-guidespublisher/default/publishercaller.json"
          dxml.use.publish.microservice="{Boolean}true"
          dxml.use.publish.microservice.native.pdf="{Boolean}true"
/>
```
