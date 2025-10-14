---
title: Opmerkingen bij de release | Opgeloste problemen in Adobe Experience Manager Guides, release 2024.10.0
description: Meer informatie over de opgeloste problemen vindt u in de release 2024.10.0 van Adobe Experience Manager Guides as a Cloud Service.
source-git-commit: 64c5318a064d28a42f3f11d2fe5b7d8548e341d8
workflow-type: tm+mt
source-wordcount: '1166'
ht-degree: 0%

---

# Opgeloste problemen in de release 2024.10.0

Dit artikel heeft betrekking op de fouten die zijn opgelost in verschillende gebieden van de release 2024.10.0 van Adobe Experience Manager Guides as a Cloud Service.

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, mening [&#x200B; wat in de versie 2024.10.0 &#x200B;](whats-new-2024-10-0.md) nieuw is.

Leer over [&#x200B; verbeteringsinstructies voor de versie 2024.10.0 &#x200B;](upgrade-instructions-2024-10-0.md).


## Authoring

- De **Vondst** optie werkt niet in de **Source** mening. 18610
- Het element `<title>` wordt automatisch toegevoegd wanneer het element `<fig>` wordt ingevoegd als een fragment. 18562
- De regeneratie van onderwerpen mislukt als gevolg van de fout in de OOTB-API voor regenereren van onderwerp of incrementele publicatie. 18452
- De Experience Manager Guides-instantie wordt instabiel en het logbestand met fouten wordt groter tot 30-40 GB nadat de interface van Assets is geopend. 18414
- **Controle uit** en **Controle binnen** pictogrammen verschijnen samen wanneer `autocheckout` in xmleditor wordt gevormd. (18088)
- Kopiëren en plakken van afbeeldingen uit de weergave Auteur werkt niet in versie 2024.06.0 van Adobe Experience Manager Guides as a Cloud Service.(18062)
- `<conref>` voor een onderwerp dat binnen een kaart van DITA van verwijzingen wordt voorzien wordt niet weerspiegeld in de voorproef binnen de redacteur. 17794
- De grote kaarten DITA laden langzaam en nemen tijd in omschakeling aan de **mening van de Lay-out**. 17590
- In de DITA-versie wordt de gebruikersnaam onjuist weergegeven in de gebruikersinterface van Assets. 17580
- De fouten voor dubbele beeld IDs in de onderwerpen beperken de gebruiker om een onderwerp op te slaan of te ontwerpen. (17528)
- Problemen treden op wanneer een groot aantal bestanden met dichte gegevenssets naar Experience Manager Guides worden geüpload.17008
- Er treden af en toe fouten op bij de renderfunctie PDF in Experience Manager Guides as a Cloud Service. (16966)
- Tijdens het maken van een DITA-kaart op basis van een sjabloon veroorzaakt de DXML-workflow van OTB procesonderbrekingen en leidt deze tot 503 onbruikbare fouten. 16529
- **Speciale karakters** die met vluchtkarakters worden geschreven worden verwijderd uit het onderwerp na het worden geupload aan Experience Manager Guides. 16495
- Het foutbericht voor een bestand dat is uitgecheckt door &#39;&#39; wordt onjuist weergegeven wanneer bestanden worden bewerkt vanaf een ander tabblad, wanneer tokens zijn verlopen of wanneer de gebruiker is afgemeld. (1523)
- De grote dossiers laden niet in de Redacteur van het Web en veroorzaken browser om te bevriezen. (1327)
- `<Topicref>` die is toegevoegd met `<keyref>` , wordt niet weergegeven in eigen PDF. (1974)
- Het pad van de component `/libs/fmdita/components/versions` is gecodeerd en de gebruikers kunnen het niet bedekken. 8779
- Als u een DITA-onderwerp of -kaart op een nieuw tabblad opent voor bewerken, wordt de selectienavigatie in de gebruikersinterface van Assets bevroren. 4992
- Wanneer een DITA-kaart met grote videobestanden wordt gedownload, treedt een fout als gevolg van onvoldoende geheugen op in de logboeken en wordt de interface niet geactiveerd. (1884)
- Wanneer het opnemen van een vergelijking van MathML die &quot;&lt;&quot;symbool bevat, wordt een **Ongeldige karakter** fout geproduceerd. 18742
- Onjuiste UUID-generatie tijdens het insluiten van de inhoud leidt tot verbroken submapverwijzingen in de ingesloten kaart. 18308
- In sommige gevallen, worden vertragingen in het verwerken van een nieuw onderwerp DITA waargenomen wanneer gecreeerd van de Webredacteur. 16836
- Het zoeken van dossiers in de **Bewaarplaats** binnen de Redacteur van het Web duurt te lang en soms ontbreekt om de resultaten te laden. 16837

## Publiceren

- Kruisverwijzing naar de sleutel wordt niet opgelost in de uitvoer van de Native PDF. 18087
- De {**fout 0} duplicate_value komt periodiek voor wanneer het opnieuw publiceren van een bestaand artikel in Salesforce.** 17932
- De opmaak van stijlen en inhoud in klantsjablonen wordt automatisch gewijzigd wanneer de layout metagegevensvelden bevat, waardoor de opmaak in gepubliceerde PDF onjuist wordt. (17900)
- Validatie van Salesforce-verbinding mislukt met de bliksemschicht-URL. 17797
- De referenced PDF wordt niet geactiveerd van het **BulkPublish Dashboard** tijdens de Bulk Activering van gepubliceerde inhoud. 17793
- Bulk-activering van gepubliceerde inhoud werkt niet voor gelokaliseerde kaarten. 17638
- Wanneer het selecteren van de **meta-gegevens van het Gebruik die in de topicmeta** optie worden toegevoegd, worden de meta-gegevenseigenschappen niet verspreid in de documenteigenschappen van de inheemse output van PDF. 17283
- Het filtreren van de voorwaarde in de inheemse output van PDF werkt niet zoals verwacht in vergelijking met DITA-OT. (17095)
- Inhoudsopgave houdt geen rekening met de tags `<sub>` of `<sup>` in de uitvoer van de native PDF. 17028)
- AEM genereren van sites en incrementele publicatie-API werkt niet zoals verwacht. (16666)
- De inheemse generatie van PDF ontbreekt met een fout met betrekking tot het krijgen van gebiedsdelen voor Node.js. (1445)
- `<Conref>` wordt niet opgelost in de `Preview` -modus van de webeditor en de uitvoer van de native PDF. 17827
- Inhoudsverwijzingen worden niet correct omgezet voor uitvoer van native PDF als het bestand met sleuteldefinities zich niet in dezelfde map bevindt als de DITA-kaart. 15062
- Wanneer een DITA-kaart kopniveaus tot 7 of hoger bevat, wordt de kop van niveau 7 onjuist behandeld als een kop van niveau 1 in de uitvoer van de oorspronkelijke PDF. (19698)
- Wanneer een inhoudsstuk (tekst) binnen een element is verpakt, worden de spaties voor en na de tekst niet weergegeven in de opmaak Voorbeeld of Uitvoer. (19308)
- Workflows na het genereren die handmatig worden geactiveerd, mislukken als gevolg van een NULL-AANWIJZER-UITZONDERING in de workflow, waardoor de inhoud elf keer wordt geüpload. (1880)
- **Bulk Publish Dashboard** toont leeg voor kaarten die nog in het vertaalproces zijn. (19352)


## Beheer

- Het pad voor de overlay-functionaliteit is hard-gecodeerd voor het Koreaanse taalbestand en is niet correct geselecteerd. (17089)
- De veranderingen/de aanpassing die aan **worden aangebracht sparen de dialoog van de Versie** weerspiegelen niet wanneer het gebruiken van het Kader van de Uitbreiding van Hulplijnen. 17828
- Het InDesign aan omzetting DITA heeft een hard-gecodeerd configuratiepad zodat worden de douane config dossiers niet plukt. 16891
- Volledige referenties/middelen worden niet gedownload wanneer een DITA-kaart met grote afhankelijkheden/verwijzingen wordt gedownload met behulp van de basislijn. (19099)


### Controleren

- Het ophalen van de gebruikerslijst tijdens het maken van een revisietaak mislukt als het aantal gebruikers groter is dan 25. 17329
- Als een taak-onderwerp `<cmd>` markering in één of meerdere stappen bevat, toont het overzichtspaneel het attribuut `importance` als prefix in alle stappen die de markering bevatten. (1969)

## Vertaling

- De verwijzingen naar vertaalde elementen worden niet bijgewerkt. 18086
- Referenties worden niet correct gefilterd als Direct of Indirect wanneer ze in meerdere talen worden vertaald. 17891
- Kan geen XLIFF-projecten maken met menselijke vertaling. (16964)
- Het toevoegen van een bijgewerkt onderwerp in een actief vertaalproject resulteert in een dubbel onderwerp en het proces ontbreekt. (7688)
- De vertaalprojecten die door **worden gecreeerd te selecteren creëren structuur slechts** optie hebben geen toegewezen UUIDs. 18980
- Wanneer het selecteren van een vertaalproject met de **Status van de Vertaling** zoals **lopend**, opent een onjuiste pagina. (13248)
- De titel met `<conref>` wordt niet omgezet in de dashboards Basislijn en Vertaling van de Web Editor. (16961)

## Bekende problemen

- Als u een AEM Sites-voorinstelling (niet verouderd) opent, wordt het onderwerp als vies gemarkeerd.
- Het geselecteerde deelvenster blijft niet behouden wanneer de browser wordt vernieuwd vanaf het tabblad Uitvoer.
- Onbekwaam om onderwerp tussen twee onderwerpen in de **Auteur** mening te slepen en te laten vallen.
- Het filtreren van de voorwaarde die in vooraf ingesteld wordt toegepast wordt niet toegepast via **Download als PDF**.
- Eén onderwerp genereren in het kaartvenster genereert alle onderwerpen die zijn geselecteerd in de AEM Sites-voorinstelling (niet verouderd).
- De verwijzing van het onderwerp lijkt gebroken in het gebruikersinterface wanneer opgenomen van de hoogste toolbar van de kaart DITA.
- Native PDF genereren mislukt voor een DITA-kaart als er ontbrekende verwijzingen zijn.
- Eén onderwerp publiceren van AEM Site met voorwaarden mislukt in een omgeving met microservices.
- Zodra de het documentstaat van een onderwerp wordt bijgewerkt aan **Gedaan**, het **Begin een Nieuw pictogram van de Versie** is slechts beschikbaar op de **Voorproef** wijze van het onderwerp.
