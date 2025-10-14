---
title: Nieuwe op microservices gebaseerde publicaties voor AEM Guides as a Cloud Service configureren
description: Leer hoe u nieuwe op microservices gebaseerde publicaties voor AEM Guides kunt configureren.
exl-id: 92e3091d-6337-4dc6-9609-12b1503684cd
feature: Microservice in AEM Guides
role: User, Admin
source-git-commit: f929d4fd74e98e2025d80c14dbef6aeb464c0dd5
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 0%

---

# Op microservice gebaseerde publicaties configureren met JWT-verificatie

[!BADGE &#x200B; Cloud Service &#x200B;]{type=Informative}

>[!NOTE]
>
> De geloofsbrieven van de Rekening van de Dienst (JWT) zijn afgekeurd ten gunste van de geloofsbrieven van de Server-aan-Server OAuth. Uw toepassingen die gebruikmaken van de JWT-referenties (Service Account) werken niet meer na 1 januari 2025. U moet vóór 1 januari 2025 naar de nieuwe referentie migreren om ervoor te zorgen dat uw toepassing blijft werken. Leer meer over [&#x200B; migrerend van de Rekening van de Dienst (JWT) credential aan OAuth Server-aan-Server credential &#x200B;](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/).



Op microservice gebaseerde publicatie in voor Adobe Experience Manager Guides as a Cloud Service biedt ondersteuning voor PDF (zowel op basis van Native als DITA-OT), HTML5, JSON en CUSTOM-typen van uitvoervoorinstellingen.

Aangezien de JWT-gegevens (Service Account) zijn afgekeurd, wordt het aanbevolen om op Adobe IMS gebaseerde verificatie te gebruiken. Leer hoe te [&#x200B; op microservice-gebaseerde het publiceren met authentificatie OAuth &#x200B;](configure-microservices-imt-config.md) vormen.

Voor de service voor publicatie in de cloud die wordt beveiligd door verificatie op basis van Adobe IMS JWT, moeten klanten onderstaande stappen volgen om hun omgevingen te integreren met beveiligde tokengebaseerde verificatieworkflows van de Adobe en de nieuwe, op de cloud gebaseerde schaalbare publicatieoplossing te gaan gebruiken.


## IMS-configuraties maken in Adobe Developer Console

**Rol die wordt vereist om de configuraties** tot stand te brengen: De Beheerder van het systeem

Voer de volgende stappen uit om IMS-configuraties te maken in Adobe Developer Console:

1. Open Developer Console: `https://developer.adobe.com/console`.

1. Schakelaar aan **Projecten** tabel van bovenkant.

   <img src="assets/projects-tab.png" alt="tabblad Projecten" width="500">

1. Om een nieuw leeg project tot stand te brengen, selecteer **Leeg project** van **creeer nieuwe project** dropdown.

   <img src="assets/create-new-project.png" alt="nieuw project maken" width="500">

1. Selecteer **API** van **toevoegen aan project** dropdown om IO Beheer API aan uw project toe te voegen.

   <img src="assets/add-project.png" alt="project toevoegen" width="300">

   <img src="assets/io-management-api.png" alt="io-beheer" width="500">

1. Maak een nieuw paar met een persoonlijke of openbare sleutel terwijl u de API toevoegt. De persoonlijke sleutel wordt dan automatisch naar uw systeem gedownload.

   <img src="assets/generate-key-pair.png" alt="sleutelpaar genereren" width="500">

1. Sla de geconfigureerde API op.

   <img src="assets/save-api.png" alt="api opslaan" width="600">

1. Ga terug naar **Projecten** tabel en klik **Overzicht van het Project** op de linkerzijde.

   <img src="assets/project-overview.png" alt="projectoverzicht" width="500">

1. Klik **Download** knoop op de bovenkant om de dienst JSON te downloaden.

   <img src="assets/download-json.png" alt="download json" width="500">

U hebt nu de JWT-verificatiegegevens geconfigureerd en ook de persoonlijke sleutel en de servicedetails JSON gedownload. Houd deze twee bestanden bij de hand, aangezien deze bestanden in de volgende sectie zijn vereist.

### IMS-configuratie toevoegen aan de omgeving

Voer de volgende stappen uit om configuratie IMS aan het milieu toe te voegen:

1. Open Experience Manager en selecteer vervolgens uw programma met de omgeving die u wilt configureren.
1. Schakelaar aan **Milieu&#39;s** tabel.
1. Klik op de naam van de omgeving die u wilt configureren. Hiermee navigeert u naar de pagina Informatie over omgeving.
1. Schakelaar aan **Configuratie** tabel.
1. Upload de persoonlijke sleutel en het project JSON zoals hieronder in het schermafbeelding wordt getoond. Zorg ervoor u de zelfde namen en configuratie gebruikt zoals hieronder benadrukt.

   <img src="assets/ims-config-environment.png" alt="ims-configuraties" width="500">

>[!NOTE]
>
> U moet de inhoud van het JSON-bestand met persoonlijke sleutel en servicedetails openen, kopiëren en in de waardekolom van het deelvenster Configuratie plakken, zoals in de bovenstaande schermafbeelding wordt getoond.

Zodra u de configuratie IMS aan het milieu hebt toegevoegd, voer de volgende stappen uit om deze eigenschappen met Experience Manager Guides te verbinden gebruikend OSGi:

1. In u het projectcode van de Git van de wolkenmanager, voeg hieronder twee dossiers toe (voor dossierinhoud, zie [&#x200B; Bijlage &#x200B;](#appendix)).

   * `com.adobe.aem.guides.eventing.ImsConfiguratorService.cfg.json`
   * `com.adobe.fmdita.publishworkflow.PublishWorkflowConfigurationService.xml`
1. Controleer of de toegevoegde bestanden worden gedekt door de `filter.xml` .
1. Leg de Git-wijzigingen vast en duw erop.
1. Voer de pijpleiding in om de veranderingen op het milieu toe te passen.

Zodra dit wordt gedaan, zou u de nieuwe op microservice-gebaseerde wolkenpublicatie moeten kunnen gebruiken.

## Veelgestelde vragen

1. Kan één sleutel worden gebruikt op veelvoudige wolkenmilieu&#39;s?
   * Ja, u kunt één privé sleutel produceren en het voor alle milieu&#39;s gebruiken, maar u moet milieuvariabelen voor alle milieu&#39;s vormen en de zelfde sleutel gebruiken.
1. Als de configuraties OSGi om microservice te gebruiken worden toegelaten, zal het het publiceren proces op lokale AEM server met de zelfde codebase werken?
   * Nee, als de markering `dxml.use.publish.microservice` is ingesteld op `true` , zoekt deze altijd naar microserviceconfiguraties. Stel `dxml.use.publish.microservice` in op `false` zodat het publiceren werkt op uw lokale computer.
1. Hoeveel geheugen wordt toegewezen aan het proces DITA wanneer het gebruiken van op microservice-gebaseerde het publiceren? Wordt dit aangestuurd via parameters van het DITA-profiel?
   * Bij publicatie op basis van microservices wordt geheugentoewijzing niet aangestuurd door parameters van het type DITA-profiel. Het totale beschikbare geheugen op de de dienstcontainer is 8 GB, waarvan 6 GB aan het DITA-OT proces wordt toegewezen.


## Bijlage {#appendix}

**Dossier**:
`com.adobe.aem.guides.eventing.ImsConfiguratorService.cfg.json`

**Inhoud**:

```
{
  "service.account.details": "$[secret:SERVICE_ACCOUNT_DETAILS]",
  "private.key": "$[secret:PRIVATE_KEY]"
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
