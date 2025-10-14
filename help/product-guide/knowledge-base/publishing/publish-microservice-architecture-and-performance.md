---
title: Cloud Publishing Microservice-architectuur en -prestaties
description: Begrijp hoe de nieuwe microservice schaalbare publicatie op AEMaaCS mogelijk maakt.
exl-id: 948fce3f-b989-48f0-9a85-e921717e2986
feature: Microservice in AEM Guides
role: User, Admin
source-git-commit: 462647f953895f1976af5383124129c3ee869fe9
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 0%

---

# Cloud Publishing Microservice-architectuur en prestatieanalyse

In dit artikel wordt uitgelegd wat de architectuur en prestatienummers zijn van de nieuwe cloudpublicatiesmicroservice.

>[!NOTE]
>
> Op microservices gebaseerde publicaties in AEM Guides ondersteunen de typen uitvoervoorinstellingen PDF (zowel op basis van Native als DITA-OT), HTML5, JSON en CUSTOM.

## Problemen met bestaande publicatieworkflows in de cloud

DITA Publishing is een hulpbronnenintensief proces dat voornamelijk afhankelijk is van het beschikbare systeemgeheugen en de CPU. De behoefte aan deze middelen neemt verder toe als de uitgevers grote kaarten met vele onderwerpen publiceren of als veelvoudige parallelle het publiceren verzoeken teweeggebracht worden.

Als u de nieuwe service niet gebruikt, gebeurt alle publicaties op dezelfde pod Kubernetes (k8) die ook de AEM cloudserver uitvoert. Een standaard k8-pod heeft een limiet voor de hoeveelheid geheugen en CPU die deze kan gebruiken. Als AEM Guides-gebruikers grote of parallelle werklasten publiceren, kan deze limiet snel worden overschreden. K8 start pods opnieuw die meer bronnen proberen te gebruiken dan de geconfigureerde limiet en die ernstige gevolgen kunnen hebben voor de AEM cloudinstantie zelf.

Deze beperking van bronnen was de belangrijkste motivatie om een speciale service te ontwikkelen waarmee we meerdere gelijktijdige en grote publicatiewerklasten in de cloud kunnen uitvoeren.

## Inleiding tot de nieuwe architectuur

De service maakt gebruik van de meest geavanceerde cloudoplossingen van de Adobe, zoals App Builder, IO Event en IMS. Deze diensten zijn zelf gebaseerd op de algemeen aanvaarde industriestandaarden zoals Kubernetes en docker.

Elk verzoek aan de nieuwe het publiceren microservice wordt uitgevoerd in een geïsoleerde docker container die slechts één het publiceren verzoek tegelijkertijd in werking stelt. Er worden automatisch meerdere nieuwe containers gemaakt voor het geval nieuwe publicatieverzoeken worden ontvangen. Deze enige container per verzoekconfiguratie staat microservice toe om de beste prestaties aan de klanten te leveren zonder enige veiligheidsrisico&#39;s te introduceren. Deze containers worden verwijderd zodra de publicatie is voltooid, waardoor ongebruikte bronnen vrijkomen.

Al deze communicatie wordt beveiligd door Adobe IMS met behulp van JWT-verificatie en -autorisatie en wordt uitgevoerd via HTTPS.

<img src="assets/architecture.png" alt="tabblad Projecten" width="600">

>[!NOTE]
>
> Het publiceren proces voert sommige inhoud afhankelijke delen van het verzoek op de AEM server zelf uit, zoals de productie van de gebiedslijst. De meest uitgebreide onderdelen van het publicatieproces, zoals het uitvoeren van DITA-OT- of native engine, zijn echter naar de nieuwe service verschoven.


## Prestatieanalyse

In deze sectie worden de prestatienummers van de microservice weergegeven. De prestaties van de microservice worden vergeleken met die van de AEM Guides on-prem-service, aangezien de oude cloudarchitectuur problemen had bij het gelijktijdig publiceren of het publiceren van zeer grote kaarten.

Als u een grote kaart op prem publiceert, dan zou u de heap parameters van Java kunnen moeten aanpassen of anders kunt u uit-van-geheugenfouten ontmoeten. In de cloud wordt de microservice al geprofileerd en zijn de Java-heap en andere configuraties optimaal.

### Eén publicatie uitvoeren op cloud versus on-prem

* Wolk

  Als u één publicatie uitvoert op de cloud met de nieuwe service, kan het enige publiceren op de voorgrond wat meer tijd in beslag nemen. Deze lichte verhoogde tijd is toe te schrijven aan de gedistribueerde aard van de nieuwe wolkenarchitectuur.

  <img src="assets/cloud_single_publish.png" alt="tabblad Projecten" width="600">

* On-prem

  De resultaten van één publicatie zijn beter op de oude cloudarchitectuur of op de voorgrond, omdat de volledige publicatie plaatsvindt op dezelfde pod/computer waarop AEM wordt uitgevoerd.

  <img src="assets/onprem_single_publish.png" alt="tabblad Projecten" width="600">

### Meerdere publicaties uitvoeren op cloud versus on-prem

* Wolk

  De nieuwe het publiceren microdienst schijnt in dit scenario. Zoals u kunt zien in de onderstaande afbeelding, kan de cloud deze publiceren zonder dat de publicatietijd aanzienlijk toeneemt, gezien de toename van het aantal gelijktijdige publicatietaken.

  <img src="assets/cloud_bulk_publish.png" alt="tabblad Projecten" width="600">

* On-prem

  Als u tegelijkertijd publiceert op een on-prem-server, neemt de prestaties sterk af. Deze prestatievermindering is ernstiger als uitgevers nog meer kaarten tegelijk publiceren.

  <img src="assets/onprem_bulk_publish.png" alt="tabblad Projecten" width="600">

## Aanvullende voordelen

Een deel van elke publicatieaanvraag moet op de AEM worden uitgevoerd om de juiste publicatie-inhoud op te halen die naar de microservice moet worden verzonden. De nieuwe cloudarchitectuur gebruikt AEM taken in plaats van AEM workflows, zoals in de oude architectuur het geval was. Met deze wijziging kunnen AEM Guides-beheerders de instellingen voor de wachtrij voor publicatie van wolken afzonderlijk configureren zonder dat dit gevolgen heeft voor andere AEM taken of workflowconfiguraties.

De details op hoe te om nieuwe te vormen publiceren microservice kunnen hier worden gevonden: [&#x200B; vormen Microservice &#x200B;](configure-microservices.md)
