---
title: Java-API voor het maken en activeren van pakketten
description: Meer informatie over de Java-API voor het maken en activeren van pakketten
exl-id: b801c2b3-445f-4aa7-a4f2-029563d7cb3a
feature: Java-Based API Packages
role: Developer
level: Experienced
source-git-commit: ed0b0e6124a8656e711a8e64b290b805569fbd48
workflow-type: tm+mt
source-wordcount: '591'
ht-degree: 0%

---

# Java-API voor het maken en activeren van pakketten {#id175UB30E05Z}

>[!NOTE]
>
> U kunt op Java gebaseerde API&#39;s die beschikbaar zijn in Experience Manager Guides gebruiken om aangepaste plug-ins te maken en workflows uit te breiden. Dit artikel wordt in november 2024 gearchiveerd.
> De mening [![ javadoc ](https://javadoc.io/badge2/com.adobe.aem/aem-guides-sdk-api/javadoc.svg) ](https://javadoc.io/doc/com.adobe.aem/aem-guides-sdk-api) voor de recentste en gedetailleerde documentatie bij het gebruiken van op Java-Gebaseerde API.


Met de volgende Java-API kunt u CRX-pakketten maken en activeren. Deze API is beschikbaar in de vorm van een bundel. U moet deze bundel in uw code omvatten om deze APIs te gebruiken.

Details bundel:

- Identiteitskaart van de groep: **com.adobe.fmdita**

- Artefactidentiteitskaart: **api**

- Versie: **3.3**

- Pakket: **com.adobe.fmdita.api.crxactivate**

- Klassegegevens:

  ```JAVA
  public class CRXActivator
  ```

  De **`CRXActivator`** -klasse bevat een methode voor het maken van CRX-pakketten en het repliceren ervan op de publicatie-instantie.


## Pakketten maken en activeren

De methode `activate` maakt een CRX-pakket op de instantie van de auteur en repliceert dit, indien nodig, op de instantie publish. Men veronderstelt dat de AEM replicatieparameters reeds opstelling op de auteursinstantie zijn geweest. Met deze methode wordt het CRX-pakket gemaakt op basis van een lijst met regels die als invoerparameters in een JSON-tekenreeks worden opgegeven.
>[!NOTE]
>
> Fouten tijdens het maken of activeren worden naar de `outputstream` geschreven.

### Voorbeeld met twee parameters

**Syntaxis**:


```JAVA
public static void activate
(
  String json, 
  OutputStream outputstream, 
  Session session
) 
throws GuidesApiException
```

### Voorbeeld met derde optionele parameter

```JAVA
public static void activate
(
  String json, 
  OutputStream outputstream,
  String activationTarget, 
  Session session
) 
throws GuidesApiException
```

**Parameters**:

| Naam | Type | Beschrijving |
|----|----|-----------|
| `json` | String | JSON-tekenreeks die het CRX-pakket bepaalt dat moet worden gemaakt. Gebruik de volgende indeling om de JSON-tekenreeks te maken: <br> - `activate` : is van het type Boolean \(`true`/`false`\). Hiermee wordt bepaald of het CRX-pakket dat in de auteurinstantie is gemaakt, wordt gerepliceerd naar de publicatie-instantie. <br> - `rules`: is van het type JSON Array. Een array met JSON-regels, die opeenvolgend worden verwerkt om het CRX-pakket samen te stellen. <br> - `rootPath`: is van het type String. Het basispad waarop de query&#39;s voor het knooppunt/de eigenschap worden uitgevoerd. Als er geen knooppunten/eigenschapquery&#39;s aanwezig zijn, worden het hoofdpad en alle knooppunten die zich onder het hoofdpad bevinden opgenomen in het CRX-pakket. <br> - `nodeQueries` : is van het type Regex Array. Een array van reguliere expressies die wordt gebruikt om specifieke bestanden op te nemen onder het hoofdpad. <br> - `propertyQueries`: is van het type JSON Array. Een array van JSON-objecten met elk JSON-object dat bestaat uit een XPath-query die moet worden uitgevoerd op het hoofdpad en de naam van een eigenschap die aanwezig is in elk JCR-knooppunt nadat de query is uitgevoerd. De waarde van de eigenschap in elk JCR-knooppunt moet een pad of een array van paden zijn. De paden in deze eigenschap worden toegevoegd aan het CRX-pakket. |
| `outputstream` | java.io.OutputStream | Dit wordt gebruikt om het resultaat van diverse stadia te schrijven, zoals vraaguitvoering, dossieropneming, het pakketverwezenlijking van CRX, of activering. Eventuele fouten die tijdens het maken of activeren worden aangetroffen, worden naar de `outputstream` geschreven. Dit is handig voor foutopsporing. |
| `session` | String | Een geldige JCR-sessie met activeringsmachtigingen. |
| `activationTarget` | String | (*Facultatief*) `preview` of `publish` voor Cloud Service en `publish` voor Software Op-premise <br> - voor Cloud Service, als de parameter een ongeldige waarde bevat, dan ontbreekt de pakketactivering. <br> - Voor software op locatie geldt dat als de parameter een ongeldige waarde bevat, de fout wordt geregistreerd en het publiceren wordt uitgevoerd met de standaardwaarde `publish` . |

**Uitzondering**:

Throws `java.io.IOException` en `java.io.IllegalArgumentException`


Als u de optionele parameter `activationTarget` niet definieert, wordt de standaard publicatieagent gebruikt voor zowel Cloud Service- als On-premise software.


**Voorbeeld**:
In het volgende voorbeeld ziet u hoe u een JSON-query bouwt:

```JSON
{
  "activate": true,
  "rules": [
    {
      "rootPath": "/content/dam/nested",
      "nodeQueries": [
        ".*\\.jpg",
        ".*\\.png",
        ".*\\.gif"        
      ]
    },
    {
      "rootPath": "/content/output/sites/hierarchy_ditamap"
    },
    {
      "rootPath": "/content/output/sites/hierarchy_ditamap",
      "propertyQueries": [
        {
          "query": "//*[@fileReference]",
          "property": "fileReference"
        }
      ]
    }
  ]
}
```

De voorbeeld-JSON-query bestaat uit de volgende regels:

- Alleen de .png-, .jpg- en .gif-afbeeldingen onder /content/dam/nested pad worden in het pakket opgenomen.
- Alle knooppunten onder /content/output/sites/shiërarchie\_ditamap worden opgenomen in het pakket.
- De paden in de eigenschap `fileReference` van knooppunten onder /content/output/sites/shiërarchie\_ditamap worden opgenomen in het pakket.
