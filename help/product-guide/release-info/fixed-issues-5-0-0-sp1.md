---
title: Opmerkingen bij de release | Problemen met Adobe Experience Manager Guides 5.0.0 Service Pack 1-release opgelost.
description: Meer informatie over de opgeloste problemen vindt u in de 5.0.0 Service Pack 1-release van Adobe Experience Manager Guides
role: Leader
source-git-commit: 083a8e16b9d3cd6c3894d7eaa2fee489b1dc0bb8
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---


# Oplossingen voor problemen in de 5.0.0 Service Pack 1-release (juni 2025)


Dit artikel behandelt de fouten die in diverse gebieden van 5.0.0 Service Pack 1 versie van Adobe Experience Manager Guides worden opgelost.

Leer over [&#x200B; verbeteringsinstructies voor 5.0.0 Service Pack 1 versie &#x200B;](upgrade-instructions-5-0-0-sp1.md).

## Authoring

- Wanneer inhoud in een `codeblock` wordt geplakt of wanneer ruimten in `codeblock` worden toegevoegd en de weergave wordt geschakeld, gaat de afstand verloren. (HULPLIJNEN-29347)
- Wanneer een commentaar van XML binnen een element in de **&#x200B;**&#x200B;mening van Source wordt toegevoegd, worden de belangrijke en het slepen ruimten rond de commentaar verloren op omschakelingsmeningen. (HULPLIJNEN- 28188)

## Beheer van bedrijfsmiddelen

- Wanneer het openen van een onderwerp in **Auteur** mening na browser verfrist zich, worden eerder toegepaste markeringen in het **paneel van de Eigenschappen van het Dossier** niet behouden, en het toevoegen van nieuwe markeringen beschrijft de bestaande degenen, vooral wanneer een groot aantal markeringen voor selectie beschikbaar zijn. (HIDEN-29078)
- Wanneer het produceren van een rapport van Meta-gegevens voor een kaart DITA die een groot aantal activa bevat, leidt **&#x200B;**&#x200B;knoop wordt unresponsief of toont vertraagde reactie. (HULPLIJNEN-2978)

## Vertaling

- Wanneer het verzenden van activa voor vertaling van Experience Manager Guides, worden de activa niet toegevoegd in de Vertaalbaan, die het **Begin** knoop verhindert te verschijnen en u verhindert om de vertaalbaan in werking te stellen. (HIDEN-28237)

## Publiceren

- Wanneer het wijzigen van de montages van een output vooraf ingesteld binnen het omslagprofiel en het selecteren van **vooraf ingestelde Veranderingen** toepassen, worden de veranderingen niet verspreid aan de output vooraf instelt huidig in de kaart DITA. (GUIDEN-26694)

## Controleren

- Pogingen om overzichtstaken tot stand te brengen door het werkschema van AEM ontbreken constant omdat de overzichtsknoop niet wordt gecreeerd. (HIDEN-28214)
