---
title: REST-API voor het maken en activeren van pakketten
description: Meer informatie over de REST-API voor het maken en activeren van pakketten
exl-id: 90686f77-a769-44bc-90eb-116cf9d0341e
feature: Rest API Packages
role: Developer
level: Experienced
source-git-commit: b95a64ca2e8ebffebec3d8ff8704f76f7faceca2
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---

# REST-API voor het maken en activeren van pakketten {#id198CF0260Y4}

Met de volgende REST-API kunt u CRX-pakketten maken en activeren.

## Pakket maken en activeren

Een methode POST waarmee een CRX-pakket wordt gemaakt en geactiveerd.

**Aanvraag-URL**:
*&lt;aem-guides-server\>* http://: *&lt;port-number\>*/bin/fmdita/activate&lt;/port-number\>&lt;/aem-guides-server\>

**Parameters**:
De aanvraagquery bestaat uit de JSON-regelsreeks. Het inhoudstype van de POST-aanvraag moet zijn ingesteld op `application/json; charset=UTF-8`.

**Voorbeeld**:
In het volgende voorbeeld wordt de API-aanroep getoond met de opdracht Krullen:

```XML
curl -u <*username*>:<*password*> -H "Content-Type: application/json; charset=UTF-8"  -k -X POST -d "{[JSON rules string](create-activate-package-java.md#example-create-activate-package-id198JH0B905Z)}" http://<*aem-guides-server*>:<*port-number*>/bin/fmdita/activate
```


**Optionele parameter**

`activationTarget`

**Geldige waarden**

`preview` of `publish` voor cloudservice en `publish` voor on-premises software

- Als de parameter voor Cloud Service een ongeldige waarde bevat, mislukt de activering van het pakket.

- Als bij on-premises software de parameter een ongeldige waarde bevat, wordt de fout geregistreerd en wordt de publicatie uitgevoerd met de standaardwaarde, `publish`.

Als u de optionele parameter toch wilt definiëren, `activationTarget`wordt deze geactiveerd met de standaard publicatie-agent voor zowel cloudservice als software op locatie.



In het volgende voorbeeld wordt de API-aanroep getoond met de opdracht Krullen en een optionele parameter:


    &#39;&#39;&#39;XML curl
    
    -u &lt;*username*>:&lt;*password*> -H &quot;Content-Type: application/json; charset=UTF-8&quot; -k -X POST -d &quot;{[JSON rules string](create-activate-package-java.md#example-create-activate-package-id198JH0B905Z)}&quot; http://&lt;*aem-guides-server*>:&lt;*port-number*>/bin/fmdita/activate?activationTarget=&lt;validActivationTargetValue>&#39;&#39;
    &#39;&#39;
&lt;/validActivationTargetValue>&lt;/*port-number*>&lt;/*aem-guides-server*>&lt;/*password*>&lt;/*username*>