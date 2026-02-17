---
title: Bedek de HTML-tags in niet-verouderde AEM Sites-uitvoer
description: De video- en afbeeldingsinstellingen configureren voor de uitvoer van bepaalde sites op basis van de toewijzing van kerncomponenten
feature: Installation
role: Admin
level: Experienced
exl-id: 726420e0-fe52-4334-b72a-8eb8bcae4d6c
source-git-commit: e0b0df19b7ec691a894130eb42df827921b4890c
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 0%

---

# HTML-tags bedekken in AEM Sites-uitvoer

U kunt HTML-tags toevoegen en aanpassen in AEM Sites-uitvoer die wordt gegenereerd met de AEM Sites-voorinstelling op basis van de toewijzing van kerncomponenten in de webeditor. Als u de HTML-tags wilt aanpassen, kunt u het `config.xml` -bestand bedekken. U kunt bijvoorbeeld de video- en afbeeldingstoewijzingen configureren in AEM Sites-uitvoer.

Voer de volgende stappen uit om het `config.xml` -bestand te bedekken en bij te werken:

1. Meld u aan bij AEM en open de CRXDE Lite-modus.

1. Navigeer naar het configuratiebestand dat beschikbaar is op de volgende locatie:

   `/libs/cq/xssprotection/config.xml`

1. Maak een overlayknooppunt van de map `xssprotection` in het knooppunt apps.

1. Navigeer naar het configuratiebestand dat beschikbaar is in het knooppunt `apps` :

   `/apps/fmdita/config/config.xml`

1. Werk de volgende tags bij voor de video&#39;s en afbeeldingen. Sla het bestand vervolgens op.

Video&#39;s:

```XML
    <tag name="video" action="validate">
    <attribute name="src">
      <regexp-list>
        <regexp name="anything"/>
      </regexp-list>
    </attribute>
    <attribute name="width">
       <regexp-list>
           <regexp name="anything"/>
       </regexp-list>
    </attribute>
    <attribute name="height">
       <regexp-list>
          <regexp name="anything"/>
       </regexp-list>
     </attribute>
     <attribute name="data">
       <regexp-list>
         <regexp name="anything"/>
       </regexp-list>
    </attribute>
    <attribute name="class">
       <regexp-list>
           <regexp name="anything"/>
       </regexp-list>
    </attribute>
    <attribute name="poster">
      <regexp-list>
        <regexp name="anything"/>
        </regexp-list>
    </attribute>
    <attribute name="controls">
        <regexp-list>
            <regexp name="anything"/>
        </regexp-list>
    </attribute>
    </tag>
    <tag name="source" action="validate">
      <attribute name="src">
        <regexp-list>
           <regexp name="anything"/>
        </regexp-list>
      </attribute>
    </tag>
```

Afbeeldingskaarten:

```XML
        <tag name="map" action="validate">
    <attribute    name="name">
        <regexp-list>
            <regexp name="anything"/>
        </regexp-list>
    </attribute>
    </tag>
    <!-- Image & image related tags -->
    <tag name="img" action="validate">
    <attribute name="src" onInvalid="removeTag">
        <regexp-list>
            <regexp name="onsiteURL"/>
            <regexp name="offsiteURL"/>
        </regexp-list>
    </attribute>
    <attribute name="name"/>
    <attribute name="alt"/>
    <attribute name="height"/>
    <attribute name="width"/>
    <attribute name="border"/>
    <attribute name="align"/>
    <attribute name="usemap">
        <regexp-list>
            <regexp name="anything"/>
        </regexp-list>
    </attribute>
    <attribute name="hspace">
        <regexp-list>
            <regexp name="number"/>
        </regexp-list>
    </attribute>
    <attribute name="vspace">
        <regexp-list>
            <regexp name="number"/>
        </regexp-list>
    </attribute>
    </tag>
    <tag name="area" action="validate">
    <attribute name="shape">
        <regexp-list>
            <regexp name="anything"/>
        </regexp-list>
    </attribute>
    <attribute name="coords">
        <regexp-list>
            <regexp name="anything"/>
        </regexp-list>
    </attribute>
    <attribute name="href">
        <regexp-list>
            <regexp name="anything"/>
        </regexp-list>
    </attribute>
   </tag>
```




Leer meer over de beste praktijken van [&#x200B; Veiligheid &#x200B;](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/introduction/security).
