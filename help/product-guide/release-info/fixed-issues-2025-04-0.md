---
title: Opmerkingen bij de release | Opgeloste problemen in Adobe Experience Manager Guides, release 2025.04.0
description: Meer informatie over de opgeloste problemen vindt u in de release 2025.04.0 van Adobe Experience Manager Guides as a Cloud Service.
source-git-commit: 9a943a26a22b64035b61c72c47268a0de2c23b7f
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 0%

---

# Opgeloste problemen in de release 2025.04.0

Dit artikel heeft betrekking op de fouten die zijn opgelost in verschillende gebieden van de release 2025.04.0 van Adobe Experience Manager Guides as a Cloud Service.

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, mening [ wat in de versie 2025.04.0 ](whats-new-2025-04-0.md) nieuw is.

Leer over [ verbeteringsinstructies voor de versie 2025.04.0 ](upgrade-instructions-2025-04-0.md).

## Authoring

- Het vak voor speciale tekeninvoeging in de Editor kan niet worden geladen voor de landinstelling Duits. 24537
- Opmerkingen en labels die zijn toegevoegd tijdens het opslaan van een nieuwe versie van een DITAVAL-bestand, worden niet in de versiegeschiedenis opgeslagen met de nieuwe versie. (24076)
- De uitgaande en inkomende verwijzingen onder **eigenschappen van het Dossier** in het juiste paneel verfrissen zich niet behoorlijk wanneer het schakelen tussen kaartdossiers. Dit probleem treedt specifiek op wanneer de kaartbestanden een groot aantal verwijzingen bevatten. (23344)
- Het filter Bewaarplaats behoudt niet de volgorde van aangepaste filters die zijn gedefinieerd in de `ui_config.json` . (2193)
- Als u meerdere tekstregels in een `codeblock` -element verwijdert, wordt een lege ruimte gemaakt die niet uit de weergave Auteur kan worden verwijderd. (20672)
- Nieuwe ids ontbreekt om voor elementen te produceren wanneer dergelijke elementen via fragmenten worden toegevoegd of via malplaatjes worden gecreeerd, zelfs wanneer **auto produceert identiteitskaart** optie binnen `XMLEditorConfig` wordt toegelaten. 21734
- Het creëren van een nieuw element DITA van malplaatjes DITA kopieert de replicatie eigenschappen van overeenkomstige malplaatjes DITA. (25145)
- Kan geen toegang krijgen tot bestandseigenschappen vanuit het paneel van de repository als de naam van de bovenliggende map het teken &#39;&amp;&#39; bevat. (25762)
- Als u een onderwerpbestand sluit, kan dit als een nieuwe versie worden opgeslagen, zelfs als het onderwerp is vergrendeld. Deze kwestie komt specifiek voor wanneer **vraagt om nieuwe versie op dichte** optie binnen `XMLEditorConfig` wordt toegelaten. 23875
- De huidige maximumbreedte van het paneel van de bewaarplaats verbergt onderwerp en kaarttitels wanneer de inhoudshiërarchie diep wordt genesteld. (27751)

## Publiceren

- In de oudere AEM Sites-uitvoer worden sectiekoppelingen in geneste onderwerpen van een kaart niet correct omgezet wanneer deze handmatig worden ingesteld in de Source-modus of wanneer de inhoud wordt geïmporteerd uit een externe bron. In plaats van naar de bedoelde sectie te navigeren, leiden zij naar het belangrijkste onderwerp dat het genestelde onderwerp bevat. (26103)
- Als het kenmerk `scope=external` ontbreekt in externe koppelingen in een DITA-onderwerp, mislukt het publiceren in HTML5 zonder de bestanden aan te geven waar dit kenmerk ontbreekt in de foutlogboeken, met name wanneer de microservice is ingeschakeld. (25969)
- Onbekwaam om videoverbindingen in Inheemse PDF in te bedden zelfs wanneer **Multimedia Dossiers** optie wordt toegelaten in vooraf ingesteld PDF. (9989)
- Kan de eigenschappen van metagegevens niet doorgeven om bestemmingspagina&#39;s die zijn gegenereerd met nieuwe AEM Sites-publicatie, toe te wijzen. (27288)

## Beheer

- De staat van het document van het werkende exemplaar van een onderwerp wordt getoond tegen alle versies van dat onderwerp in de Vertaling en Basislijn UI. (20674)


## Controleren

- Als u de details van een revisietaak bijwerkt op het dashboard Revisie, wordt niet bevestigd of de update is gelukt of niet. 8051

## Vertaling

- De vertalingen die door Experience Manager Guides worden voorgelegd omvatten niet de activa in bijlage, veroorzakend de **knoop van het Begin** voor vertaalbaan om niet aan gebruikers onbeschikbaar te worden.

## Bekende problemen

Adobe heeft de volgende bekende problemen vastgesteld voor de release 2025.04.0:

- De referentietelling in de interface van de basislijn wordt niet bijgewerkt bij het bewerken van de basislijn. Deze wordt alleen bijgewerkt wanneer de wijzigingen worden opgeslagen. (28015)
- Wanneer de veelvoudige lusjes in de Redacteur open zijn, ongedaan makend **&#x200B;**&#x200B;verrichting in de **Source** mening van een dossier terugkeert laatste uitgeeft maar ook schakelaars aan het eerder geopende lusje. 27891
- De **optie van de Controle van de Spelling van 0&rbrace; AEM {verschijnt in de** 3} dropdown lijst van het Menu &lbrace;, zelfs wanneer de **Browser spellingcontrole** optie in de montages van de Redacteur wordt toegelaten. **&#x200B;**&#x200B;(27993)
- Een extra versie wordt gecreeerd en getoond in het **paneel van de Geschiedenis van de Versie** wanneer u een beeld in Assets UI uitgeeft en het bewaart. (28001)
- Er wordt automatisch een lege regel ingevoegd bij het plakken van nieuwe inhoud in een nieuwe regel binnen een `codeblock` -element.27842
- Het schakelen tussen vooraf instelt die de zelfde Basislijn gebruiken deactiveert **&#x200B;**&#x200B;knoop voor huidige vooraf ingesteld. (28025)
- Een onderwerp in een DITA-kaart kan niet worden gepubliceerd in de AEM Sites-uitvoer wanneer het wordt gebruikt als zowel `keydef` als `topicref` in de submaps. (2269)
- In AEM Sites-uitvoer worden afbeeldingen afgebroken wanneer Basislijn niet wordt toegepast tijdens het publiceren. (28043)
- Een toepassingsfout komt voor wanneer de veelvoudige onderwerpen van een kaart worden uitgegeven en dan gesloten gebruikend **sluit alle** optie, met **Vraag op sparen versie op dicht** toegelaten plaatsen.27931







