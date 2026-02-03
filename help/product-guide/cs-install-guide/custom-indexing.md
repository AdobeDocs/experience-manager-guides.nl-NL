---
title: Aangepaste implementatie voor indexering
description: Leer hoe u indexinhoud kunt aanpassen
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 7d2d0c21001cd53244588f6b700db184a73ffa77
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%

---

# Aangepaste index gebruiken voor de functie Zoeken en vervangen (Source-weergave)

## Overzicht

Deze handleiding bevat stapsgewijze instructies voor het implementeren van de aangepaste index `guidesAssetLucene‑1‑custom‑1` op Adobe Experience Manager (AEM) as a Cloud Service. Hoewel de standaardfunctie Zoeken en vervangen in de weergave Auteur zonder deze index werkt, is de aangepaste index specifiek vereist om Zoeken en vervangen in de weergave Source in te schakelen. Met de weergave Zoeken en vervangen (Source) kunt u niet alleen zoeken in de zichtbare geschreven inhoud, maar ook in de onderliggende XML-structuur, inclusief elementen, tags en kenmerkwaarden.

## Vereisten

Voordat u verdergaat met de indeximplementatie, moet u controleren of u beschikt over:

- **milieu van AEM as a Cloud Service** met geïnstalleerde AEM Guides
- **Toegang tot codebase van uw project** (de bewaarplaats van de it)
- **de toegang van Cloud Manager** met plaatsingstoestemmingen

## Indexdefinitie

Als u de functie Zoeken en vervangen (Source-weergave) wilt inschakelen, moet u een aangepaste index met de naam **`guidesAssetLucene-1-custom-1`** in uw AEM Cloud Service-omgeving implementeren.

### Indexnaam

```
guidesAssetLucene-1-custom-1
```

### Indexdefinitie (.content.xml)

Maak de volgende indexdefinitie in uw project op:

`ui.apps/src/main/content/jcr_root/_oak_index/guidesAssetLucene-1-custom-1/.content.xml`

```xml
<?xml version="1.0" encoding="UTF-8"?>
<jcr:root xmlns:jcr="http://www.jcp.org/jcr/1.0" xmlns:dam="http://www.day.com/dam/1.0"
          xmlns:nt="http://www.jcp.org/jcr/nt/1.0" xmlns:oak="http://jackrabbit.apache.org/oak/ns/1.0"
          xmlns:rep="internal"
          jcr:mixinTypes="[rep:AccessControllable]"
          jcr:primaryType="oak:QueryIndexDefinition"
          async="[async,nrt]"
          compatVersion="{Long}2"
          evaluatePathRestrictions="{Boolean}true"
          includedPaths="[/content/dam]"
          reindex="{Boolean}false"
          reindexCount="{Long}1"
          seed="{Long}958982603885135223"
          selectionPolicy="tag"
          tags="[ditaSearch]"
          type="lucene">

    <aggregates jcr:primaryType="nt:unstructured">
        <dam:Asset jcr:primaryType="nt:unstructured">
            <include0
                    jcr:primaryType="nt:unstructured"
                    path="jcr:content/renditions/original/jcr:content"
                    relativeNode="{Boolean}true"/>
        </dam:Asset>
    </aggregates>

    <analyzers jcr:primaryType="nt:unstructured">
        <default jcr:primaryType="nt:unstructured">
            <tokenizer
                    jcr:primaryType="nt:unstructured"
                    name="Whitespace"/>
        </default>
    </analyzers>

    <indexRules jcr:primaryType="nt:unstructured">
        <dam:Asset
                jcr:primaryType="nt:unstructured"
                indexNodeName="{Boolean}true">
            <properties jcr:primaryType="nt:unstructured">
                <cqTags
                        jcr:primaryType="nt:unstructured"
                        name="jcr:content/metadata/cq:tags"
                        nodeScopeIndex="{Boolean}true"
                        propertyIndex="{Boolean}true"
                        useInSpellcheck="{Boolean}true"
                        useInSuggest="{Boolean}true"/>
                <jcrLastModified
                        jcr:primaryType="nt:unstructured"
                        name="jcr:content/jcr:lastModified"
                        ordered="{Boolean}true"
                        propertyIndex="{Boolean}true"
                        type="Date"/>
                <jcrCreated
                        jcr:primaryType="nt:unstructured"
                        name="jcr:created"
                        ordered="{Boolean}true"
                        propertyIndex="{Boolean}true"
                        type="Date"/>
                <guidesParentMaps
                        jcr:primaryType="nt:unstructured"
                        name="jcr:content/guidesParentMaps"
                        propertyIndex="{Boolean}true"/>
                <guidesDirectParentMaps
                        jcr:primaryType="nt:unstructured"
                        name="jcr:content/guidesDirectParentMaps"
                        propertyIndex="{Boolean}true"/>
                <ditaClass
                        jcr:primaryType="nt:unstructured"
                        name="jcr:content/metadata/dita_class"
                        propertyIndex="{Boolean}true"/>
                <nodeNameLowerCase
                        jcr:primaryType="nt:unstructured"
                        function="fn:lower-case(fn:name())"
                        ordered="{Boolean}true"
                        propertyIndex="{Boolean}true"/>
                <cqDriveLock
                        jcr:primaryType="nt:unstructured"
                        name="jcr:content/cq:driveLock"
                        propertyIndex="{Boolean}true"
                        ordered="{Boolean}true"/>
                <docState
                        jcr:primaryType="nt:unstructured"
                        name="jcr:content/metadata/docstate"
                        propertyIndex="{Boolean}true"
                        ordered="{Boolean}true"/>
                <jcrPath
                        jcr:primaryType="nt:unstructured"
                        function="fn:path()"
                        ordered="{Boolean}true"/>
                <dcTitleLowerCase
                        jcr:primaryType="nt:unstructured"
                        function="fn:lower-case(jcr:first(jcr:content/metadata/@dc:title))"
                        propertyIndex="{Boolean}true"
                        ordered="{Boolean}true"/>
                <dcTitle
                        jcr:primaryType="nt:unstructured"
                        name="jcr:content/metadata/dc:title"
                        propertyIndex="{Boolean}true"/>
            </properties>
        </dam:Asset>
    </indexRules>

    <tika jcr:primaryType="nt:unstructured">
        <mimeTypes jcr:primaryType="nt:unstructured">
            <application jcr:primaryType="nt:unstructured">
                <xml
                        jcr:primaryType="nt:unstructured"
                        mappedType="application/dita+xml"/>
            </application>
            <text jcr:primaryType="nt:unstructured">
                <markdown
                        jcr:primaryType="nt:unstructured"
                        mappedType="text/markdown+source"/>
            </text>
        </mimeTypes>
    </tika>
</jcr:root>
```

## Implementatiestappen

Voor gedetailleerde instructies bij het opstellen van douaneindexen aan AEM as a Cloud Service, bekijk [&#x200B; Inhoud Onderzoek en het Indexeren - AEM as a Cloud Service &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/operations/indexing).

### Belangrijke punten voor deze index

Wanneer het volgen van de plaatsingsgids, gebruik de volgende specificaties voor de Vondst en vervang index:

- **Naam van de Index**: `guidesAssetLucene-1-custom-1`
- **Type van Index**: Volledige douaneindex (niet een aanpassing van index OTB)
- **Plaats**: `ui.apps/src/main/content/jcr_root/_oak_index/guidesAssetLucene-1-custom-1/.content.xml`
- **Vereiste de Eigenschappen van het Pakket**:
   - `noIntermediateSaves=true`
   - `allowIndexDefinitions=true`

## Opnieuw indexeren

Het opnieuw indexeren wordt behandeld **&#x200B;**&#x200B;automatisch door AEM as a Cloud Service wanneer u de index door de pijpleiding van Cloud Manager CI/CD opstelt.

Indexering wordt meestal automatisch afgehandeld. Als de oude gegevens echter ondoorzoekbaar blijven, zelfs na de correcte implementatie en de voltooiing van het indexeringsproces, moet de index eenmaal handmatig opnieuw worden geïndexeerd.

### Wat te verwachten

- De indexeertaak wordt automatisch gestart na de implementatie.
- U kunt de voortgang volgen op de Cloud Manager-bouwstijlpagina.
- Het milieu blijft volledig operationeel tijdens het indexeren.

## Verificatie

Na plaatsing en het indexeren voltooiing, verifieer dat de index correct werkt.

### Indeximplementatie verifiëren

In uw ontwikkelomgeving (als CRXDE Lite beschikbaar is):

1. Navigeer naar `/oak:index/guidesAssetLucene-1-custom-1` .
2. Verifieer de knoop met de verwachte configuratie bestaat.

### De functie Zoeken en vervangen testen

De belangrijkste verificatie is het testen van de functie:

1. Open AEM Guides.
2. Navigeer aan **Hulpmiddelen** > **Gidsen** > **Vondst en vervangt in Bewaarplaats**.
3. Configureer een zoekopdracht naar tekst in uw DITA- of Markdown-bestanden.
4. Controleer of de zoekresultaten correct zijn geretourneerd.
5. Test de vervangingsfunctionaliteit op een testdossier.

## Aanvullende bronnen

- [&#x200B; AEM as a Cloud Service Indexing Documentation &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/operations/indexing)
- [&#x200B; Apache Jackrabbit Oak Indexing Guide &#x200B;](https://jackrabbit.apache.org/oak/docs/query/indexing.html)
- [&#x200B; Documentatie van AEM Guides &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-manager-guides)
- [Documentatie voor Cloud Manager](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-manager)
