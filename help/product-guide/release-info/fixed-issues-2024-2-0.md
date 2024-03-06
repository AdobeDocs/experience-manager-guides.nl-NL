---
title: Opmerkingen bij de release | Opgeloste problemen in Adobe Experience Manager Guides, release 2024.2.0
description: Meer informatie over de opgeloste problemen vindt u in de 2024.2.0-release van Adobe Experience Manager Guides as a Cloud Service.
source-git-commit: 3da78dd90bd219809d0a47bcdc2775b2c5ba29e1
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# Opgeloste problemen in de release 2024.2.0

In dit artikel worden de bugs beschreven die zijn gecorrigeerd in verschillende gebieden van de release 2024.2.0 van Adobe Experience Manager Guides as a Cloud Service.

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, mening [Nieuwe functies in de release 2024.2.0](whats-new-2024-2-0.md).

Meer informatie over [upgradeinstructies voor de release van 2024.2.0](upgrade-instructions-2024-2-0.md).



## Authoring

- Spellingcontrole in de Editor staat niet toe dat suggesties worden geselecteerd. 15045
- De algemene navigatieknop werkt niet en het dashboard kan niet worden geladen. 14968
- In de Redacteur van het Web, ontbreekt de eigenschap van de downloadkaart om een pop-up bericht teweeg te brengen wanneer het klaar is om te downloaden. 14626
- In de Redacteur van het Web, ontbreekt de eigenschap van de downloadkaart om een kaart met basislijn te downloaden. (14622)
- Ongeldige DTD-fout in de release van oktober 2023 van Experience Manager Guides as a Cloud Service. (14482)
- Het slepen van een verklarend woordenlijstonderwerp van de bewaarplaats in een verklarende woordenlijstkaart leidt tot `topicref`. 10767
- Het voorvertoningsscherm voor fragmenten is bevroren. 14840
- Labels uit de `labels.json` bestand wordt in willekeurige volgorde weergegeven in de webeditor. 10508

## Publiceren

- In publicaties met native PDF werken aangepaste kenmerken binnen voorinstellingen voor voorwaarden niet voor publiceren via native PDF. 14943
- In de publicatie Native PDF worden belangrijke verwijzingen niet opgelost voor de release van Adobe Experience Manager Guides in december 2023. 15085
- Publiceren in AEM Sites mislukt en veroorzaakt bereikfouten voor bestanden met `xref` naar het DITA-bestand dat begint met &quot;HTTP&quot;. 15154
- Kan geen aangepaste sjabloon toevoegen vanuit het dialoogvenster **Uitvoer** in de Editor. 14846
- **Site AEM** De voorinstelling werkt niet vanwege een leeg sjabloonpad. 14804
- AEM de regeneratie van de Plaats ontbreekt voor kaarten DITA met onderwerpen die vergelijkingen MathML bevatten. 14790
- In het Publiceren van Native PDF, genereren van PDF fouten in het krijgen van afhankelijkheden voor `Node.js` publiceren. (1445)
- Met AEM voorinstelling kunt u geen sjabloon buiten de `/content` in de webeditor. (14260)
- In de AEM Sites-uitvoer gingen de stijl of regeleinden verloren voor de `<lines>` element met subelementen. 12542
- Aangepaste metagegevens zijn niet beschikbaar in de uiteindelijke uitvoer. (1216)
- In de publicatie Native PDF kunnen de metagegevenseigenschappen van de DITA-kaart niet worden gebruikt om de metagegevens voor uitvoer van PDF-bestanden te vullen. 15159



## Beheer

- **Basislijnfilter** de dossiers werken niet met de Naam van het Dossier in de Redacteur van het Web. 13486
- Het onbruikbaar maken van het indexeren van de ouderkaart DITA om betere prestaties te krijgen kan de functionaliteit van bepaalde eigenschappen beïnvloeden.12213


## Controleren

- Klikken met rechtermuisknop in contextmenu werkt niet voor **Accepteren** of **Afwijzen** wijzigingen bijhouden. 14607
- De knevel om onderwerpen te sluiten DITA in het Scherm van het Overzicht werkt niet in de versie van december 2023 van de Gidsen van Adobe Experience Manager. 14537
- Het aanpassen van e-mailsjablonen voor de revisiewerkstroom werkt niet met overlay. 13954

## Bekend probleem

Adobe heeft het volgende bekende probleem voor de release 2024.2.0 geïdentificeerd:

- Versie 1.0 wordt niet getoond op UI voor het gedupliceerde DITA- dossier.
- De doorgave van metagegevens van elementen werkt niet voor de release 2024.2.0 waarvoor microservice is ingeschakeld voor een voorinstelling.

