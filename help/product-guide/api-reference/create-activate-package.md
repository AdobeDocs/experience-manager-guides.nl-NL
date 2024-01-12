---
title: REST API voor het maken en activeren van pakketten
description: Meer informatie over de REST API voor het maken en activeren van pakketten
exl-id: 90686f77-a769-44bc-90eb-116cf9d0341e
feature: Rest API Packages
role: Developer
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---

# REST API voor het maken en activeren van pakketten {#id198CF0260Y4}

Met de volgende REST API kunt u CRX-pakketten maken en activeren.

## Pakket maken en activeren

Een methode van de POST die tot CRX pakket leidt en activeert.

**Aanvraag-URL**: http://*&lt;aem-guides-server>*: *&lt;port-number>*/bin/fmdita/activate

**Parameters**: De aanvraagquery bestaat uit de tekenreeks JSON-regels. Het inhoudstype van het verzoek van de POST moet worden geplaatst aan `application/json; charset=UTF-8`.

**Voorbeeld**: In het volgende voorbeeld wordt de API-aanroep met de opdracht curl getoond:

    &quot;
    curl -u &lt;*username*>:&lt;*password*> -H &quot;Content-Type: application/json; charset=UTF-8&quot; -k -X POST -d &quot;{[JSON rules string](create-activate-package-java.md#example-create-activate-package-id198JH0B905Z)&quot; http://&lt;*ave em-guides-server*>:&lt;*poort-nummer*>/bin/fmdita/activate
    &quot;
