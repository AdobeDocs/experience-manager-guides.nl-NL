---
title: REST API voor het maken en activeren van pakketten
description: Meer informatie over de REST API voor het maken en activeren van pakketten
exl-id: 90686f77-a769-44bc-90eb-116cf9d0341e
feature: Rest API Packages
role: Developer
level: Experienced
source-git-commit: 6e23f52fc9124d0f07f8108da1b5fe574f553469
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 0%

---

# REST API voor het maken en activeren van pakketten {#id198CF0260Y4}

Met de volgende REST API kunt u CRX-pakketten maken en activeren.

## Pakket maken en activeren

A POST method that creating and activate CRX package.

**Verzoek URL**:
http://*&lt;aem-guides-server\>*: *&lt;port-number\>*/bin/fmdita/activate

**Parameters**:
De aanvraagquery bestaat uit de tekenreeks JSON-regels. Het inhoudstype van de POST-aanvraag moet worden ingesteld op `application/json; charset=UTF-8` .

**Voorbeeld**:
In het volgende voorbeeld wordt de API-aanroep met de opdracht curl getoond:

```XML
curl -u <*username*>:<*password*> -H "Content-Type: application/json; charset=UTF-8"  -k -X POST -d "{[JSON rules string](create-activate-package-java.md#example-create-activate-package-id198JH0B905Z)}" http://<*aem-guides-server*>:<*port-number*>/bin/fmdita/activate
```


**Facultatieve parameter**

`activationTarget`

**Geldige waarden**

`preview` of `publish` voor Cloud Service en `publish` voor on-premise software

- Als de parameter voor Cloud Service een ongeldige waarde bevat, mislukt de activering van het pakket.

- Als voor On-premise Software de parameter een ongeldige waarde bevat, wordt de fout geregistreerd en wordt het publiceren uitgevoerd met de standaardwaarde `publish` .

Als u de optionele parameter `activationTarget` niet definieert, wordt de standaard publicatieagent gebruikt voor zowel Cloud Service- als On-premise software.



In het volgende voorbeeld wordt de API-aanroep getoond met de opdracht curl met optionele parameter:


```XML
curl -u <*username*>:<*password*> -H "Content-Type: application/json; charset=UTF-8"  -k -X POST -d "{[JSON rules string](create-activate-package-java.md#example-create-activate-package-id198JH0B905Z)}" http://<*aem-guides-server*>:<*port-number*>/bin/fmdita/activate?activationTarget=`<validActivationTargetValue>`
```
