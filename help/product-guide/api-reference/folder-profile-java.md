---
title: Java-API om te werken met mapprofielen
description: Meer informatie over de op Java gebaseerde API om met mapprofielen te werken
exl-id: 388ae654-c4f9-4bb7-ba98-370b8919e3a6
feature: Java-Based API Folder Profiles
role: Developer
level: Experienced
source-git-commit: 8c80a4da8e61909aab0f2db81ef97149774b36c4
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---

# Java-API om te werken met mapprofielen {#id175UB30E05Z}

>[!NOTE]
>
> U kunt op Java gebaseerde API&#39;s die beschikbaar zijn in Experience Manager Guides gebruiken om aangepaste plug-ins te maken en workflows uit te breiden. Dit artikel wordt in november 2024 gearchiveerd.
> De mening [![ javadoc ](https://javadoc.io/badge2/com.adobe.aem/aem-guides-sdk-api/javadoc.svg) ](https://javadoc.io/doc/com.adobe.aem/aem-guides-sdk-api) voor de recentste en gedetailleerde documentatie bij het gebruiken van op Java-Gebaseerde API.




Met de volgende op Java gebaseerde API kunt u voorwaardelijke kenmerken toevoegen aan een profiel op mapniveau. Deze API is beschikbaar in de vorm van een bundel. U moet deze bundel in uw code omvatten om deze APIs te gebruiken.

Details bundel:

- Identiteitskaart van de groep: **com.adobe.fmdita**

- Artefactidentiteitskaart: **api**

- Versie: **3.2**

- Pakket: **com.adobe.fmdita.api.profiles**

- Klassegegevens:

  ```JAVA
  public class FolderProfileUtils extends Object
  ```

  De klasse **`FolderProfileUtils`** bevat een methode voor het toevoegen van voorwaardelijke kenmerken in een mapprofiel.


## Voorwaardelijke kenmerken toevoegen aan een mapprofiel

De methode ``addAttributeProfiles`` voegt voorwaardelijke kenmerken toe aan een profiel op mapniveau.

**Syntaxis**:

```JAVA
public static boolean addAttributeProfiles
(List
<String> attributeNames, 
List
    <String> values, 
List
        <String> labels,
String profileName, 
Session session) throws GuidesApiException
```

**Parameters**:

| Naam | Type | Beschrijving |
|----|----|-----------|
| ``attributeNames`` | String | Een lijst met kenmerknamen. |
| ``values`` | String | Een lijst met waarden voor de opgegeven kenmerken. |
| `labels` | String | Een lijst met labels voor de `attribute` - `value` -paren. [ 1 ](#fntarg_1) |
| `profileName` | String | De naam van het profiel op mapniveau waarop deze kenmerken, waarden en labels moeten worden toegepast. **Belangrijk:** Alle bestaande attributen-waarden-etiketten die in het profiel worden bepaald worden beschreven. |
| `session` | javax.jcr.Session | Een geldige JCR-sessie. |

**Keert** terug:
`true` voor succes. In het geval van een mislukking, veroorzaakt het een uitzondering.

**Uitzondering**:
Genereert ``java.lang.Exception`` in de volgende scenario&#39;s:

- Als de API geen `resourceResolverFactory` -object kan ophalen. In dat geval moet u de bundel opnieuw starten.
- Als parameters die aan de API worden doorgegeven ongeldig zijn.
- Als de API wordt aangeroepen via een niet-geautoriseerde gebruikerssessie, bijvoorbeeld de gebruiker die geen beheerder is voor het opgegeven mapprofiel.

[&#128279;](#fnsrc_1) `attributeNames` `values`, en `labels` bij de zelfde index in een serielijst moet aan de zelfde ingang beantwoorden.
