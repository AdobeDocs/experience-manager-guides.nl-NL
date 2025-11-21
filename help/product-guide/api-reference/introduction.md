---
title: Inleiding
description: Inleiding tot de API Reference Guide voor AEM Guides
exl-id: d8ee9cf7-1d67-4b4a-aa80-64e893a99463
feature: API Introduction
role: Developer
level: Experienced
source-git-commit: 6e23f52fc9124d0f07f8108da1b5fe574f553469
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 0%

---

# Inleiding {#id1761C0007W7}

Adobe Experience Manager Guides \ (later die als *AEM Guides* wordt bedoeld \) is een oplossing van begin tot eind, ondernemingsoplossing die Adobe Experience Manager \ (AEM \) toelaat om componenteninhoudbeheeroplossing \ (CCMS \) mogelijkheden voor op DITA-Gebaseerde inhoudsverwezenlijking en levering te hebben. Klanten hebben via programmacode toegang tot AEM Guides-workflows om deze te integreren met andere bedrijfstoepassingen. Deze API&#39;s kunnen ook door Adobe-partners worden gebruikt om de waardepropositie van AEM Guides te verbeteren door de functionaliteit ervan uit te breiden of door deze te integreren met andere toepassingen of services.

## AEM Guides API&#39;s

De AEM Guides API&#39;s zijn beschikbaar in twee indelingen:

- [Java-API&#39;s](#java-based-apis)
- [REST-API&#39;s](#rest-based-apis)

Deze API&#39;s maken belangrijke functies van AEM Guides toegankelijk voor toepassingsontwikkelaars. Met deze functies kunnen ontwikkelaars hun eigen plug-ins maken om de workflows uit de doos uit te breiden. De API&#39;s zijn beschikbaar voor het beheren van uitvoer voor DITA-inhoud, het werken met DITA-kaarten, het toevoegen van voorwaardelijke kenmerken aan profielen op mapniveau en het converteren van HTML- en Word-documenten naar DITA-indeling.


### Java-API&#39;s

U kunt op Java gebaseerde API&#39;s die beschikbaar zijn in Experience Manager Guides gebruiken om aangepaste plug-ins te maken en workflows uit te breiden.

**vorm SDK van Gemaakt centrale bewaarplaats voor AEM Guides as a Cloud Service**

>[!INFO]
>
>De mening [![&#x200B; javadoc &#x200B;](./images/javadoc-cs-icon.svg) &#x200B;](https://javadoc.io/doc/com.adobe.aem/aem-dox-sdk-api/latest/index.html) voor de recentste en gedetailleerde documentatie bij het gebruiken van op Java-Gebaseerde API voor Experience Manager Guides as a Cloud Service.

Om de dienst API JARs van Maven bewaarplaats in uw projecten te vormen en te gebruiken, voeg API SDK als projectgebiedsdeel in het `pom.xml` dossier van uw project toe zoals hieronder getoond.

```XML
<dependency>
<groupId>com.adobe.aem</groupId>
<artifactId>aem-dox-sdk-api</artifactId>
<version>${RELEASE}</version>
</dependency>
```

>[!NOTE]
>
> Zorg ervoor dat u dezelfde versie van de API JAR gebruikt als het AEM Guides-pakket dat op uw server is geïnstalleerd.

**vorm en gebruik API JAR van Gemaakt centrale bewaarplaats (On-premise)**

>[!INFO]
>
>De mening [![&#x200B; javadoc &#x200B;](https://javadoc.io/badge2/com.adobe.aem/aem-guides-sdk-api/javadoc.svg) &#x200B;](https://javadoc.io/doc/com.adobe.aem/aem-guides-sdk-api/latest/index.html) voor de recentste en gedetailleerde documentatie bij het gebruiken van op Java-Gebaseerde API voor de opstelling van Experience Manager Guides op-gebouw.

Om de dienst API JARs voor plaatsingen op-gebouw te vormen en te gebruiken, voeg de dienst API JAR als projectgebiedsdeel in het `pom.xml` dossier van uw project toe &lbrace;zoals hieronder getoond:

```XML
<dependency>
<groupId>com.adobe.aem</groupId>
<artifactId>aem-guides-sdk-api</artifactId>
<version>${RELEASE}</version>
</dependency>
```

>[!NOTE]
>
> Zorg ervoor dat u dezelfde versie van de API JAR gebruikt als het AEM Guides-pakket dat op uw server is geïnstalleerd.


**vorm en gebruik API JAR van de openbare Maven bewaarplaats van AEM Guides (On-premise)**

>[!NOTE]
>
> De openbare AEM Guides Maven-opslagplaats wordt vervangen na de 5.3.0-release van Experience Manager Guides. De API JAR is daarna alleen beschikbaar in de Maven Central-dataopslag.

Voer de volgende stappen uit om de dienst API JARs van de openbare GeMaven bewaarplaats te gebruiken:

1. Configureer de openbare Maven-opslagplaats van AEM Guides in uw `pom.xml` - of `settings.xml` -bestand, zoals hieronder wordt weergegeven:

   ```XML
   <repository>
       <id>fmdita-public</id>
       <name>fmdita-public</name>
       <url>https://repo.aem-guides.com/repository/fmdita-public</url>
    </repository>
   ```

1. Als de opslagplaats is ingesteld, voegt u de service-API JAR toe als een projectafhankelijk in het `pom.xml` -bestand van het project.

   ```XML
   <dependency>
       <groupId>com.adobe.fmdita</groupId>
       <artifactId>api</artifactId>
       <version>${RELEASE}</version>
   </dependency>
   ```

   >[!NOTE]
   >
   > Gebruik dezelfde versie van de API JAR als het AEM Guides-pakket dat u op de server hebt geïnstalleerd.

Zodra de dienst API JAR als projectgebiedsdeel in het `pom.xml` dossier van het project wordt toegevoegd, kunt u AEM Guides Java APIs in uw project bouwen en gebruiken.


### REST-API&#39;s

Experience Manager Guides biedt een uitgebreide set REST-API&#39;s waarmee ontwikkelaars via HTTP toegang hebben tot kernfuncties en deze kunnen gebruiken.

Deze API&#39;s zijn ideaal voor:

- Experience Manager Guides integreren met andere bedrijfssystemen
- Workflows voor publiceren en revisie automatiseren
- Aangepaste toepassingen en extensies maken

Voor gedetailleerde informatie over gebruik API, parameters, en voorbeeldverzoeken, bekijk de relevante onderwerpen in de **API sectie van de Verwijzing** van de documentatie van Experience Manager Guides.

## Aanvullende bronnen

Na is een lijst van andere nuttige middelen van AEM Guides, die op [&#x200B; &#x200B;](https://helpx.adobe.com/nl/support/xml-documentation-for-experience-manager.html) pagina Leren &amp; van de Steun beschikbaar zijn:

- Handboek
- Installatie- en configuratiehandleiding
- Handleiding voor snel starten
- [&#x200B; de Archiefpagina van het Archief van de Hulp &#x200B;](https://helpx.adobe.com/nl/xml-documentation-for-experience-manager/archive.html) \ (de documentatie van de toegangsoudere versie \)
