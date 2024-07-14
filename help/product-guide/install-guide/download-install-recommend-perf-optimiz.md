---
title: Recommendations for performance optimization
description: Meer informatie over de Recommendations voor het optimaliseren van prestaties
exl-id: b2a836a0-de82-4d89-aae3-43276997da74
feature: Performance Optimization
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '967'
ht-degree: 0%

---

# Recommendations for performance optimization {#id213BD0JG0XA}

## Gegevensopslag \(verplicht\) configureren

**wat is de verandering?**
Plaats het `minRecordLength` bezit aan een waarde van `100` onder de configuratie `org.apache.jackrabbit.oak.plugins.blob.datastore.FileDataStore.` voor meer informatie over de opslag van de dossierdatum en S3 gegevensopslag, zie [ het Vormen knoopopslag en gegevensopslag in AEM 6 ](https://helpx.adobe.com/experience-manager/6-5/sites/deploying/using/data-store-config.html) artikel.

>[!NOTE]
>
> Voor S3 gegevensopslag, hangt de kosten voor het handhaven van inhoud in gegevensopslag ook van het aantal verzoeken af. Daarom wanneer het doen van dit het plaatsen met S3-opstellingskosten per verzoek en geheim voorgeheugengrootte ook zou moeten worden overwogen.

**Wanneer te vormen?**
Na de eerste installatie, maar voordat inhoud wordt gemigreerd. U moet deze verandering zelfs op een bestaand systeem uitvoeren, dat ervoor zorgt dat al nieuwe inhoud in gegevensopslag in plaats van segmentopslag wordt opgeslagen.

**Resultaat van deze verandering**
De DITA-bestanden worden opgeslagen in de gegevensopslag in plaats van in de segmentopslag. Hierdoor blijft de grootte van de segmentwinkel binnen de aanbevolen limieten, waardoor de reactiesnelheid van het systeem wordt verbeterd.

## Lucene-index bijwerken \(verplicht\)

**wat is de verandering?**
Sluit /var/dxml uit van eiken:index/lucene.

>[!NOTE]
>
> AEM Guides gebruikt nooit Lucene-indexen om te zoeken naar inhoud in het knooppunt /var/dxml.

**Wanneer te vormen?**
Als u deze wijziging aanbrengt op een nieuw systeem voordat u inhoud migreert, is alleen het bijwerken van de eik:index/glucose vereist. Anders, op een bestaand systeem waar de inhoud reeds gemigreerd is, dan na het aanbrengen van de verandering in eiken:index/lucene, herbouwt indexen voor Luzern \ (*die enkele uren zou kunnen vergen om* \) te voltooien.

**Resultaat van deze verandering**
Deze verandering verhindert /var/dxml knoop in de segmentopslag wordt geïndexeerd en wordt opgeslagen.

## Java-geheugenoptimalisatie \(verplicht\)

**wat is de verandering?**
De JVM-beginparameters moeten zorgvuldig worden ingesteld op basis van de infrastructuur en de schijfgrootte. U wordt aangeraden Adobe Support te raadplegen om hulp te krijgen bij het openen van de ideale configuratie. U kunt echter zelf de volgende configuraties uitproberen:

- Stel de JVM-heapgrootte in op minimaal 1/4e van het totale beschikbare geheugen. Gebruik de parameter `-Xmx<size>` om de grootte van het heapgeheugen in te stellen. Stel de waarde in voor -`Xms` gelijk aan `-Xmx` .

- Inschakelen `-XX:+HeapDumpOnOutOfMemoryError` en het pad instellen voor `-XX:HeapDumpPath=</path/to/folder``>` .

- Java GC-logbestand inschakelen als:

`* -XX:+PrintGCDateStamps`

`* -verbose:gc`

`* -XX:+PrintGCDetails`

`* -XX:+PrintTenuringDistribution`

`* -Xloggc:</path/to/gc.log>`

- In het algemeen gebruikt u voor Java 11 G1GC \(`-XX:+UseG1GC`\) en voor Java 8 CMS \(-`XX:+UseConcMarkSweepGC`\).

- Gebruik `-XX:NewRatio` om de grootte van het geheugen van de jonge generatie te bepalen. De standaardwaarde is 2, wat betekent dat 1/3 van het geheugen wordt gebruikt voor jonge generaties. Omdat er veel objecten zijn die snel worden gemaakt en vernietigd, wijst u met een waarde van 1/2 van het geheugen toe aan de jonge generatie.

- Bepaal het aantal objecten dat tot de oude generatie wordt bevorderd met `-XX:MaxTenuringThreshold` . Gebruik de waarde 15 \(standaardwaarde\) om te vertragen wanneer objecten worden geconverteerd naar de oude generatie.

**Wanneer te vormen?**
Als u deze wijziging aanbrengt op een bestaand systeem, moet u het systeem opnieuw opstarten. In het geval van een nieuwe installatie moet deze wijziging worden aangebracht in het beginscriptbestand \(.bat of .sh\) voordat het systeem wordt gestart.

**Resultaat van deze verandering**
Dit resulteert in optimale heapgrootte en gereguleerde uitvoering van GC.

## Clientbibliotheekminiatuur op Author-instantie \(optioneel\)

**wat is de verandering?**
De clientbibliotheken moeten zo worden ingesteld dat ze in de ontwerpinstanties miniaturen. Zo zorgt u ervoor dat er minder bytes worden gedownload wanneer een gebruiker op verschillende locaties naar het systeem bladert. Om deze verandering aan te brengen, plaats de configuratie in **de Manager van de Bibliotheek van de HTML** van de console van Felix.

**Wanneer te vormen?**
Dit kan in runtime door de console van Felix of via codeplaatsing worden gedaan.

**Resultaat van deze verandering**
Deze wijziging verbetert de laadtijd van pagina&#39;s op de instantie Auteur, aangezien er minder bytes worden overgedragen om de clientbibliotheken te laden.

## Configureer gelijktijdige publicatiethreads \(verplicht, afhankelijk van het gebruiksgeval\)

**wat is de verandering?**
Deze wijziging is vereist als u DITA-OT gebruikt om uitvoer te publiceren en er ook een aantal gelijktijdige publicatiethreads is gedefinieerd.

Standaard stelt AEM Guides de publicatiethreads in op het aantal CPU&#39;s+1. Het wordt echter aanbevolen deze waarde in te stellen op de helft \(1/2\) of een derde \(1/3\) van het totale aantal CPU&#39;s. Om dit te doen, plaats het **bezit van de Grootte van de Pool van de 1} Generatie onder de configuratie `com.adobe.fmdita.publish.manager.PublishThreadManagerImpl` zoals volgens de aanbevelingen.**

**Wanneer te vormen?**
Dit kan in runtime door de console van Felix of via codeplaatsing worden gedaan.

**Resultaat van deze verandering**
Deze verandering zorgt ervoor dat op een lopende instantie van de Auteur alle middelen niet voor de het publiceren verrichtingen worden toegewezen. Hierdoor blijven de systeembronnen ook beschikbaar voor auteurs, wat resulteert in een betere gebruikerservaring.

## Batchgrootte van knooppunten configureren voor het genereren van AEM Site-uitvoer \(verplicht, afhankelijk van het gebruiksgeval\)

**wat is de verandering?**
Deze wijziging is vereist als u AEM Sites-uitvoer genereert.

Plaats de **Beperking AEM de Pagina&#39;s van de Plaats in het bezit van de Zeep** onder `com.adobe.fmdita.config.ConfigManager` aan een aantal dat op de configuratie van uw systeem wordt gebaseerd. Deze eigenschap definieert de batchgrootte van knooppunten die moeten worden vastgelegd wanneer de sitepagina&#39;s worden gegenereerd. Op een systeem met bijvoorbeeld een groter aantal CPU&#39;s en heapgrootten kunt u de standaardwaarde van `500` naar een groter aantal verhogen. U moet de uitvoering met de gewijzigde waarde testen om tot een optimale waarde voor deze eigenschap te komen.

**Wanneer te vormen?**
Dit kan in runtime door de console van Felix of via codeplaatsing worden gedaan.

**Resultaat van deze verandering**
Een verhoogd aantal van de **Grens AEM de Pagina&#39;s van de Plaats in het bezit van de Samenvatting** optimaliseert het proces van de AEM de outputproductie van de Plaats.

## Het aantal naverwerkingsthreads \(verplicht, afhankelijk van het gebruiksgeval\) optimaliseren

**wat is de verandering?**
Deze wijziging is vereist als u DITA-inhoud bulksgewijs uploadt.

Plaats het **bezit van Threads van het Proces van 0} Post onder `com.adobe.fmdita.config.ConfigManager` aan `1`.**

**Wanneer te vormen?**
Dit kan tijdens runtime worden gedaan.

**Resultaat van deze verandering**
Deze wijziging verkort de naverwerkingstijd bij bulkupload van DITA-bestanden.

**Bovenliggend onderwerp:**[ Download en installeer ](download-install.md)
