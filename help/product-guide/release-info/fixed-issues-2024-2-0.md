---
title: Opmerkingen bij de release | Opgeloste problemen in Adobe Experience Manager Guides, release 2024.2.0
description: Meer informatie over de opgeloste problemen vindt u in de release 2024.2.0 van Adobe Experience Manager Guides as a Cloud Service.
exl-id: fae1ff07-6232-4e9a-a89e-5e760e807b9d
source-git-commit: e40ebf4122decc431d0abb2cdf1794ea704e5496
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# Opgeloste problemen in de release 2024.2.0

Dit artikel heeft betrekking op de fouten die zijn opgelost in verschillende gebieden van de release van Adobe Experience Manager Guides as a Cloud Service in 2024.2.0.

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, mening [&#x200B; wat in de versie 2024.2.0 &#x200B;](whats-new-2024-2-0.md) nieuw is.

Leer over [&#x200B; verbeteringsinstructies voor de versie 2024.2.0 &#x200B;](upgrade-instructions-2024-2-0.md).



## Authoring

- Spellingcontrole in de Editor staat niet toe dat suggesties worden geselecteerd. 15045
- De algemene navigatieknop werkt niet en het dashboard kan niet worden geladen. 14968
- In de Redacteur van het Web, ontbreekt de eigenschap van de downloadkaart om een pop-up bericht teweeg te brengen wanneer het klaar is om te downloaden. 14626
- In de Redacteur van het Web, ontbreekt de eigenschap van de downloadkaart om een kaart met basislijn te downloaden. (14622)
- Ongeldige DTD-fout in de release van oktober 2023 van Experience Manager Guides as a Cloud Service. (14482)
- Door een woordenlijstonderwerp van de repository naar een glossary map te slepen, maakt u `topicref` . 10767
- Het voorvertoningsscherm voor fragmenten is bevroren. 14840
- De etiketten van het `labels.json` dossier verschijnen in willekeurige orde in de Redacteur van het Web. 10508

## Publiceren

- In publicaties met native PDF werken aangepaste kenmerken binnen voorinstellingen voor voorwaarden niet voor publiceren via native PDF. 14943
- In Native PDF-publicaties worden belangrijke verwijzingen niet opgelost voor de release van Adobe Experience Manager Guides in december 2023. 15085
- Publiceren in AEM Sites mislukt en veroorzaakt bereikfouten voor bestanden die `xref` naar het DITA-bestand hebben dat begint met &quot;HTTP&quot;. 15154
- Onbekwaam om een douanemalplaatje van het **lusje van Output** in de Redacteur toe te voegen. 14846
- **AEM de vooraf ingestelde Plaats** werkt niet toe te schrijven aan een leeg malplaatjeweg. 14804
- AEM de regeneratie van de Plaats ontbreekt voor kaarten DITA met onderwerpen die vergelijkingen MathML bevatten. 14790
- Bij publicatie van Native PDF genereren PDF fouten bij het ophalen van afhankelijkheden voor publicatie van `Node.js` . (1445)
- AEM vooraf ingesteld staat niet de selectie van een malplaatje buiten de `/content` hiërarchie in de Redacteur van het Web toe. (14260)
- In de AEM Sites-uitvoer zijn de stijl of regeleinden verloren gegaan voor het `<lines>` -element met subelementen. 12542
- Aangepaste metagegevens zijn niet beschikbaar in de uiteindelijke uitvoer. (1216)
- In de publicatie Native PDF kunnen de metagegevenseigenschappen van de DITA-kaart niet worden gebruikt om de metagegevens voor uitvoer van PDF-bestanden te vullen. 15159



## Beheer

- **dossiers van de Filter van de Basislijn 0&rbrace; &lbrace;werken niet met de Naam van het Dossier in de Redacteur van het Web.** 13486
- Het onbruikbaar maken van het indexeren van de ouderkaart DITA om betere prestaties te krijgen kan de functionaliteit van bepaalde eigenschappen beïnvloeden.12213


## Controleren

- Klik contextmenu met de rechtermuisknop aan werkt niet voor **Accepteer** of **verwerp** spoorveranderingen. 14607
- De knevel om onderwerpen te sluiten DITA in het Scherm van het Overzicht werkt niet in de versie van december 2023 van Adobe Experience Manager Guides. 14537
- Het aanpassen van e-mailsjablonen voor de revisiewerkstroom werkt niet met overlay. 13954

## Bekend probleem

Adobe heeft het volgende bekende probleem voor de release 2024.2.0 geïdentificeerd:

- Versie 1.0 wordt niet getoond op UI voor het gedupliceerde DITA- dossier.
- De doorgave van metagegevens van elementen werkt niet voor de release 2024.2.0 waarvoor microservice is ingeschakeld voor een voorinstelling.
