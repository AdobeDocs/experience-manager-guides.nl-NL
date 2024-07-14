---
title: REST API voor het maken en activeren van pakketten
description: Meer informatie over de REST API voor het maken en activeren van pakketten
exl-id: 90686f77-a769-44bc-90eb-116cf9d0341e
feature: Rest API Packages
role: Developer
level: Experienced
source-git-commit: b95a64ca2e8ebffebec3d8ff8704f76f7faceca2
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---

# REST API voor het maken en activeren van pakketten {#id198CF0260Y4}

Met de volgende REST API kunt u CRX-pakketten maken en activeren.

## Pakket maken en activeren

Een methode van de POST die tot een pakket van CRX leidt en activeert.

**Verzoek URL**:
http://*&lt;aem-guides-server\>*: *&lt;port-number\>*/bin/fmdita/activate

**Parameters**:
De aanvraagquery bestaat uit de tekenreeks JSON-regels. Het inhoudstype van de POST request must be set to `application/json; charset=UTF-8`.

**Voorbeeld**:
In het volgende voorbeeld wordt de API-aanroep met de opdracht curl getoond:

```XML
curl -u <*username*>:<*password*> -H "Content-Type: application/json; charset=UTF-8"  -k -X POST -d "{[JSON rules string](create-activate-package-java.md#example-create-activate-package-id198JH0B905Z)}" http://<*aem-guides-server*>:<*port-number*>/bin/fmdita/activate
```


**Facultatieve parameter**

`activationTarget`

**Geldige waarden**

`preview` of `publish` for Cloud Service and `publish` for On-premise Software

- Als de Cloud Service een ongeldige waarde bevat, mislukt de pakketactivering.

- Als voor On-premise Software de parameter een ongeldige waarde bevat, wordt de fout geregistreerd en wordt het publiceren uitgevoerd met de standaardwaarde `publish` .

Als u de optionele parameter `activationTarget` niet definieert, wordt de standaard publicatieagent gebruikt voor zowel Cloud Service- als On-premise software.



In het volgende voorbeeld wordt de API-aanroep getoond met de opdracht curl met optionele parameter:


     &quot;XML 
    
     krullen -u &lt;*username*>:&lt;*password*> - H &quot;Content-Type: application/json; charset=UTF-8&quot; -k -X POST -d &quot;{[JSON-rules string](create-activate-package-java.md#example-create-activate-package-id198JH0B905Java Z)}&quot; http://&lt;*aem-guides-server*>:&lt;*port-number*>/bin/fmdita/activate?activationTarget=`&lt;validActivationTargetValue>`
    &quot;
