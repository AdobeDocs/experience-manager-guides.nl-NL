---
title: Java-API's voor conversieworkflow
description: Meer informatie over de op Java gebaseerde API's voor de conversieworkflow
exl-id: 807d9ffa-23e3-476c-992d-c1f495233892
feature: Java-Based API Conversion Workflow
role: Developer
level: Experienced
source-git-commit: be06612d832785a91a3b2a89b84e0c2438ba30f2
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# Java-API&#39;s voor conversieworkflow {#id175UB30E05Z}

Met de volgende op Java gebaseerde API&#39;s kunt u HTML- en Word-documenten converteren naar DITA-indeling. Deze API&#39;s zijn beschikbaar in de vorm van een bundel. U moet deze bundel in uw code omvatten om deze APIs te gebruiken.

**de details van de Bundel**:

- Identiteitskaart van de groep: **com.adobe.fmdita**

- Artefactidentiteitskaart: **api**

- Versie: **3.2**

- Pakket: **com.adobe.fmdita.api.conversion**

- Klassegegevens:

  ```JAVA
  public class ConversionUtils extends Object
  ```

  De **klasse ConversionUtils** bevat methodes om HTML en documenten van Word in formaat om te zetten DITA.


## HTML-documenten converteren

Met de methode `convertHtmlToDita` worden HTML-documenten omgezet in DITA-indeling.

**Syntaxis**:

```JAVA
public static void convertHtmlToDita(Session session, 
                  String inputFile, 
                  String destPath, 
                  boolean createRev) 
                  throws RepositoryException, WorkflowException
```

**Parameters**:
|Naam|Type|Omschrijving|
|—|—|—|
|`session`|javax.jcr.Session|Een geldige JCR-sessie.|
|`inputFile`|String|Absoluut pad van de bronbestanden van de HTML in AEM opslagplaats.|
|`destPath`|String|Absoluut pad van de doellocatie waar de geconverteerde DITA-bestanden worden opgeslagen.|
|`createRev`|Boolean|Opgeven of een revisie van de bestanden \( `true`\) wordt gemaakt op het opgegeven doel of niet \( `false`\). Dit wordt alleen overwogen wanneer de doellocatie een bestaande versie van de omgezette bestanden bevat.|

**Uitzondering**:
Throws `RepositoryException` .

## Word-documenten converteren

De methode ``convertWordToDita`` zet Word-documenten om in DITA-indeling.

**Syntaxis**:

```JAVA
public static void convertWordToDita(Session session, 
                  String inputFile,
                  String destPath, 
                  String style2tagMap, 
                  boolean createRev) 
                  throws RepositoryException, WorkflowException
```

**Parameters**:
|Naam|Type|Omschrijving|
|—|—|—|
|`session`|javax.jcr.Session|Een geldige JCR-sessie.|
|`inputFile`|String|Absoluut pad van de Word-bronbestanden in AEM opslagplaats.|
|`destPath`|String|Absoluut pad van de doellocatie waar de geconverteerde DITA-bestanden worden opgeslagen.|
|`style2tagMap`|String|Absoluut pad van het stijltoewijzingsbestand dat wordt gebruikt voor conversie.|
|`createRev`|Boolean|Opgeven of een revisie van de bestanden \( `true`\) wordt gemaakt op het opgegeven doel of niet \( `false`\). Dit wordt alleen overwogen wanneer de doellocatie een bestaande versie van de omgezette bestanden bevat.|

**Uitzondering**:
Throws `RepositoryException` .
