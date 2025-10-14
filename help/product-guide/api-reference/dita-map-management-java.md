---
title: API's die zijn gebaseerd op Java om te werken met DITA-kaarten
description: Meer informatie over de op Java gebaseerde API's voor werken met DITA-kaarten
exl-id: bd91fc90-75f8-487c-99d1-2637e9cf9924
feature: Java-Based API Dita Map
role: Developer
level: Experienced
source-git-commit: 8c80a4da8e61909aab0f2db81ef97149774b36c4
workflow-type: tm+mt
source-wordcount: '1068'
ht-degree: 0%

---

# API&#39;s die zijn gebaseerd op Java om te werken met DITA-kaarten {#id175UB30E05Z}

>[!NOTE]
>
> U kunt op Java gebaseerde API&#39;s die beschikbaar zijn in Experience Manager Guides gebruiken om aangepaste plug-ins te maken en workflows uit te breiden. Dit artikel wordt in november 2024 gearchiveerd.
> De mening [![&#x200B; javadoc &#x200B;](https://javadoc.io/badge2/com.adobe.aem/aem-guides-sdk-api/javadoc.svg) &#x200B;](https://javadoc.io/doc/com.adobe.aem/aem-guides-sdk-api) voor de recentste en gedetailleerde documentatie bij het gebruiken van op Java-Gebaseerde API.



Met de volgende op Java gebaseerde API&#39;s kunt u werken met DITA-kaarten in AEM Guides. Deze API&#39;s zijn beschikbaar in de vorm van een bundel. U moet deze bundel in uw code omvatten om deze APIs te gebruiken.

Details bundel:

- Identiteitskaart van de groep: **com.adobe.fmdita**

- Artefactidentiteitskaart: **api**

- Versie: **3.2**

- Pakket: **com.adobe.fmdita.api.maps**

- Klassegegevens:

  ```JAVA
  public class MapUtilities extends Object
  ```

  De klasse MapUtilities bevat methoden voor het ophalen van metagegevens uit een DITA-kaartbestand.


## DITA-kaart met afhankelijke personen downloaden

De methode `zipMapWithDependents` maakt een ZIP-bestand dat een DITA-kaart bevat, samen met alle afhankelijke elementen, zoals onderwerpen waarnaar wordt verwezen, submappen, afbeeldingen en DTD&#39;s. Het .zip dossier voor de kaart DITA wordt gecreeerd gebaseerd op een bepaalde basislijn.

U kunt hiermee ook dezelfde structuur \(bovenliggende en onderliggende mappen\) behouden of een vlakke bestandsstructuur maken in één map voor alle afhankelijke bestanden.

>[!IMPORTANT]
>
> De API genereert een uitzondering en kan geen ZIP-bestand maken als een van de afhankelijke bestanden ontbreekt.

**Syntaxis**:

```JAVA
public static void zipMapWithDependents(Session session, 
                     String sourcePath, 
                     String baseline, 
                     OutputStream outputStream,
                     boolean flatFS) 
                     throws RepositoryException, IOException
```

**Parameters**:

| Naam | Type | Beschrijving |
|----|----|-----------|
| `session` | javax.jcr.Session | Een geldige JCR-sessie. |
| `sourcePath` | String | Pad \(in de AEM opslagplaats\) van het DITA-kaartbestand dat moet worden gedownload. |
| `outputStream` | java.io.OutputStream | De stream waarnaar de ZIP moet worden geschreven. |
| `baseline` | String | De titel van de basislijn die wordt gebruikt om de versie van de inhoud op te halen. <br> **Nota:** de waarde is case-sensitive. |
| flatFS | Boolean | \(Optioneel\) Indien ingesteld op true, wordt een platte structuur van bestanden geretourneerd in het ZIP-bestand. Als uw DITA-kaart bijvoorbeeld verwijst naar inhoud in meerdere mappen, worden alle bestanden waarnaar wordt verwezen, in één map geplaatst. Als er bestanden met dezelfde naam zijn, wordt de naam van deze bestanden gewijzigd door een numeriek achtervoegsel toe te voegen. Alle verwijzingen \(in kaart DITA en onderwerpen \) worden automatisch behandeld, aangezien zij gebaseerd op de nieuwe plaats van dossiers in de vlakke omslagstructuur worden bijgewerkt. Als de waarde false is, blijft de mapstructuur ongewijzigd in het ZIP-bestand. Als de DITA-kaart verwijst naar bestanden van meerdere locaties, worden al deze locaties ook gemaakt in het ZIP-bestand. Wanneer u het ZIP-bestand herstelt, wordt de exacte mapstructuur gemaakt op de doellocatie. <br> De standaardwaarde voor deze parameter is false. |

**Keert** terug:
De inhoud van het ZIP-bestand wordt geschreven naar de `outputStream` .

**Uitzondering**:
Throws ``javax.jcr.RepositoryException`` , `java.io.IOException` .

## DITA-kaart downloaden met afhankelijke personen \(Asynchroon\)

U kunt ook een DITA-kaart met afhankelijkheden downloaden in een asynchrone modus. Deze benadering is nuttiger voor grotere kaarten DITA.

De methode `zipMapWithDependents` maakt een ZIP-bestand dat een DITA-kaart bevat, samen met alle afhankelijke elementen, zoals onderwerpen waarnaar wordt verwezen, submappen, afbeeldingen en DTD&#39;s. Het .zip dossier voor de kaart DITA wordt gecreeerd gebaseerd op een bepaalde basislijn.

U kunt hiermee ook dezelfde structuur \(bovenliggende en onderliggende mappen\) behouden of een vlakke bestandsstructuur maken in één map voor alle afhankelijke bestanden.

>[!NOTE]
>
> Dit knooppunt wordt na enige tijd automatisch verwijderd op basis van de configuratie output.history.purgetime, indien gedefinieerd, of 5 dagen als standaard.

**Syntaxis**:

```JAVA
public static CompletableFuture<Node> zipMapWithDependencies(Session session,
                     String sourcePath, 
                     String baseline, 
                     boolean flatFS) 
```

**Parameters**:

| Naam | Type | Beschrijving |
|----|----|-----------|
| `session` | javax.jcr.Session | Een geldige JCR-sessie. |
| `sourcePath` | String | Pad \(in de AEM opslagplaats\) van het DITA-kaartbestand dat moet worden gedownload. |
| `baseline` | String | De titel van de basislijn die wordt gebruikt om de versie van de inhoud op te halen. <br> **Nota:** de waarde is case-sensitive. |
| flatFS | Boolean | \(Optioneel\) Indien ingesteld op true, wordt een platte structuur van bestanden geretourneerd in het ZIP-bestand. Als uw DITA-kaart bijvoorbeeld verwijst naar inhoud in meerdere mappen, worden alle bestanden waarnaar wordt verwezen, in één map geplaatst. Als er bestanden met dezelfde naam zijn, wordt de naam van deze bestanden gewijzigd door een numeriek achtervoegsel toe te voegen. Alle verwijzingen \(in kaart DITA en onderwerpen \) worden automatisch behandeld, aangezien zij gebaseerd op de nieuwe plaats van dossiers in de vlakke omslagstructuur worden bijgewerkt. Als de waarde false is, blijft de mapstructuur ongewijzigd in het ZIP-bestand. Als de DITA-kaart verwijst naar bestanden van meerdere locaties, worden al deze locaties ook gemaakt in het ZIP-bestand. Wanneer u het ZIP-bestand herstelt, wordt de exacte mapstructuur gemaakt op de doellocatie.<br> De standaardwaarde voor deze parameter is false. |

**Keert** terug:
Het knooppunt van het ZIP-bestand wordt opgenomen in de `CompletableFuture` -klasse. De gebruiker kan het asynchroon blijven behandelen, en kan `.get()` methode van de toekomst gebruiken om de draad te blokkeren wanneer de knoop nodig is. De geretourneerde waarde kan ook eindigen met een fout die kan worden afgehandeld met de methode `.exceptionally()` .

## Een lijst met basislijnen ophalen

De ``getBaselineList`` methode wint een lijst van alle basislijnen terug die voor een bepaalde kaart DITA bestaan.

**Syntaxis**:

```JAVA
public static List<HashMap<String,String>> getBaselineList( 
                  javax.jcr.Session session, 
                  String sourcePath)
                  throws javax.jcr.RepositoryException
```

**Parameters**:

| Naam | Type | Beschrijving |
|----|----|-----------|
| `session` | javax.jcr.Session | Een geldige JCR-sessie. |
| `sourcePath` | String | Pad \(in de AEM opslagplaats\) van het DITA-kaartbestand waarvoor de basislijninformatie moet worden opgehaald. |

**Keert** terug:
Een lijst met `HashMap` -objecten. Elk `HashMap` -object vertegenwoordigt een basislijn en bevat de naam en titel van de basislijn.

**Uitzondering**:
Throws ``javax.jcr.RepositoryException`` .

## Een lijst met voorwaardelijke voorinstellingen ophalen

De methode ``getConditionalPresetList`` haalt een lijst op van alle voorwaardelijke voorinstellingen die voor een bepaalde DITA-kaart bestaan.

**Syntaxis**:

```JAVA
public static List<HashMap<String,String>> getConditionalPresetList (
                  javax.jcr.Session session,
                  String sourcePath)
                  throws javax.jcr.RepositoryException
```

**Parameters**:

| Naam | Type | Beschrijving |
|----|----|-----------|
| `session` | javax.jcr.Session | Een geldige JCR-sessie. |
| `sourcePath` | String | Pad \(in de AEM opslagplaats\) van het DITA-kaartbestand waarvoor de voorwaardelijke voorinstellingsgegevens moeten worden opgehaald. |

**Keert** terug:
Een lijst met `HashMap` -objecten. Elk `HashMap` -object vertegenwoordigt een voorwaardelijke voorinstelling en bevat de naam en titel van de voorwaardelijke voorinstelling.

**Uitzondering**:
Throws ``javax.jcr.RepositoryException`` .

## De gegevens van het DITAVAL-bestand ophalen voor een voorwaardelijke voorinstelling

De methode ``getDitavalFromConditionalPreset`` haalt het pad op van het DITAVAL-bestand dat overeenkomt met een voorwaardelijke voorinstelling voor een bepaalde DITA-kaart.

**Syntaxis**:

```JAVA
public static String getDitavalFromConditionalPreset
    (Session session,
    String sourcePath, 
    String cpName) throws RepositoryException
```

**Parameters**:

| Naam | Type | Beschrijving |
|----|----|-----------|
| `session` | javax.jcr.Session | Een geldige JCR-sessie. |
| `sourcePath` | String | Pad \(in de AEM opslagplaats\) van het DITA-kaartbestand waarvoor het DITAVAL-bestand moet worden opgehaald. |
| `cpName` | String | Naam van de voorwaardelijke voorinstelling in de DITA-kaart waarvoor het DITAVAL-bestand moet worden opgehaald. |

**Keert** terug:
Het pad van het DITAVAL-bestand dat overeenkomt met de voorwaardelijke voorinstelling die is gedefinieerd in het DITA-kaartbestand.

## Hiermee worden alle afhankelijkheden voor een knooppunt opgehaald

De methode ``getAllDependencies`` retourneert alle afhankelijkheden van een opgegeven knooppunt.

**Syntaxis**:

```JAVA
public static List
<Node> getAllDependencies 
(Node rootNode) throws GuidesApiException
```

**Parameters**:

| Naam | Type | Beschrijving |
|----|----|-----------|
| `rootNode` | javax.jcr.Node | De wortelknoop waarvoor alle gebiedsdelen moeten worden teruggewonnen. |

**Keert** terug:
Een knooppuntenlijst die alle gebiedsdelen van de wortelknoop bevat.
