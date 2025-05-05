---
title: Op Java gebaseerde API om met uitvoergeneratie te werken
description: Meer informatie over de op Java gebaseerde API om met uitvoergeneratie te werken
exl-id: e19439df-39ec-47fd-9da5-24f51750a7e5
feature: Java-Based API Publishing
role: Developer
level: Experienced
source-git-commit: ee4eb829ebe215315b05cd1f376e934c02a73b1e
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---

# Op Java gebaseerde API om met uitvoergeneratie te werken {#id175UB30E05Z}

>[!NOTE]
>
> U kunt op Java gebaseerde API&#39;s die beschikbaar zijn in Experience Manager Guides gebruiken om aangepaste plug-ins te maken en workflows uit te breiden. Dit artikel wordt in november 2024 gearchiveerd.
> De mening [![ javadoc ](https://javadoc.io/badge2/com.adobe.aem/aem-guides-sdk-api/javadoc.svg) ](https://javadoc.io/doc/com.adobe.aem/aem-guides-sdk-api) voor de recentste en gedetailleerde documentatie bij het gebruiken van op Java-Gebaseerde API.

Met de volgende op Java gebaseerde API kunt u uitvoer genereren voor een DITA-kaart. Deze API is beschikbaar in de vorm van een bundel. U moet deze bundel in uw code omvatten om deze APIs te gebruiken.

Details bundel:

- Identiteitskaart van de groep: **com.adobe.fmdita**

- Artefactidentiteitskaart: **api**

- Versie: **3.4**

- Pakket: **&#x200B;**&#x200B;com.adobe.fmdita.api.maps&#x200B;**&#x200B;**

- Klassegegevens:

  ```JAVA
  public class **PublishUtils** extends Object
  ```

  De klasse **`PublishUtils`** bevat een methode voor het genereren van uitvoer voor een of meer uitvoervoorinstellingen.


## Uitvoer genereren

De methode ``generateOutput`` genereert uitvoer voor een DITA-toewijzingsbestand met de opgegeven uitvoervoorinstellingen.

**Syntaxis**:

```JAVA
public static void generateOutput(Session session,
String sourcePath,
String outputName)
throws GuidesApiException
```

**Parameters**:

| Naam | Type | Beschrijving |
|----|----|-----------|
| `session` | javax.jcr.Session | Een geldige JCR-sessie. |
| ``sourcePath`` | String | Pad \(in de AEM opslagplaats\) van het DITA-kaartbestand waarvoor de uitvoer moet worden gegenereerd. |
| ``outputName`` | String | Naam van de uitvoervoorinstelling\(en\) die moet worden gebruikt om uitvoer te genereren. U kunt meerdere uitvoervoorinstellingen opgeven met een scheidingsteken voor de pipe \(&quot;\|&quot;\), bijvoorbeeld `aemsite\|pdfoutput` . |

**Uitzondering**:
Genereert ``javax.jcr.RepositoryException`` , `java.io.IOException` en `java.lang.Exception` .
