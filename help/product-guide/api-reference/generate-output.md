---
title: Op Java gebaseerde API om met uitvoergeneratie te werken
description: Meer informatie over de op Java gebaseerde API om met uitvoergeneratie te werken
exl-id: e19439df-39ec-47fd-9da5-24f51750a7e5
feature: Java-Based API Publishing
role: Developer
level: Experienced
source-git-commit: a255007fc9fe169f926e356ec9d2a8f5a2fdbe29
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# Op Java gebaseerde API om met uitvoergeneratie te werken {#id175UB30E05Z}

Met de volgende op Java gebaseerde API kunt u uitvoer genereren voor een DITA-kaart. Deze API is beschikbaar in de vorm van een bundel. U moet deze bundel in uw code omvatten om deze APIs te gebruiken.

Details bundel:

- Identiteitskaart van de groep: **com.adobe.fmdita**

- Artefactidentiteitskaart: **api**

- Versie: **3.4**

- Pakket: ****com.adobe.fmdita.api.maps****

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
