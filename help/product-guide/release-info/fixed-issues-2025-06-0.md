---
title: Opmerkingen bij de release | Opgeloste problemen in Adobe Experience Manager Guides, release 2025.06.0
description: Meer informatie over de opgeloste problemen vindt u in de release 2025.06.0 van Adobe Experience Manager Guides as a Cloud Service.
source-git-commit: 78d8896982ff73e954de6d6daa9832faf30ed3b3
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---

# Opgeloste problemen in de release 2025.06.0

Dit artikel heeft betrekking op de fouten die zijn opgelost in verschillende gebieden van de release 2025.06.0 van Adobe Experience Manager Guides as a Cloud Service.

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, mening [ wat in de versie 2025.06.0 ](whats-new-2025-06-0.md) nieuw is.

Leer over [ verbeteringsinstructies voor de versie 2025.06.0 ](upgrade-instructions-2025-06-0.md).

## Authoring

- Wanneer het openen van een kaart DITA met verenigde toegelaten shell, verandert de redacteur af en toe. (GUIDEN-26919)
- Als u geen JCR-sessieverbindingen sluit tijdens het bijwerken of maken van onderwerpen, resulteert dit in geheugenlekken en downtime van de service. (GUIDEN-26282)
- Als u de kolommen sleept, verandert de breedte van een percentage in pixelwaarden. Dit leidt tot vervormde of onjuist uitgelijnde tabellen.(HIDEN-23128)
- Wanneer inhoud in een `code block` wordt geplakt of wanneer ruimten in `code block` worden toegevoegd en de weergave wordt geschakeld, gaat de afstand verloren. (GUIDEN-27478)
- Wanneer u een kaart toevoegt aan de `bookmap` , wordt deze opgeslagen in `fmditatopicrefs` in plaats van `fmditamaprefs` . (HIDEN-25480)
- Het **beeld van het Tussenvoegsel** dialoog ontbreekt om correct op een hoog-resolutie of gezoomde schermen terug te geven die de beeldtitel en afwisselende tekstgebieden veroorzaken om te verdwijnen. (GUIDEN-26459)


## Publiceren

- Native PDF-publicatie gaat eindeloos door als de DITA-inhoud een webkoppeling heeft zonder bereik als `external` . (HIDEN-26434)
- Als er fouten in de inhoud optreden, worden native PDF&#39;s en AEM-sites in de wachtrij geplaatst. (HIDEN-26516)
- Wanneer u een nieuwe basislijn met een groot aantal labels maakt, worden niet alle labels opgehaald. (GUIDEN-16232)
- Wanneer u AEM-sitepagina&#39;s genereert met titels die meerdere woorden bevatten die door spaties worden gescheiden, worden afbreekstreepjes weergegeven in plaats van spaties. (HIDEN-27903)
- Voor Inheemse PDF, wordt een ongeldige naam van het meta-gegevensbezit niet opgelost en als `unresolved property name` getoond in **documenteigenschappen**. (HULPLIJNEN-25680)
- Tekst met meerdere regels in `codeblock` veroorzaakt problemen met tekstoverloop tijdens het genereren van PDF. (HIDEN-15541)
- Wanneer het toevoegen van kaarten aan de kaartinzameling, worden de activa buiten kaarten (zoals onderwerpen etc.) getoond, en de vertaalde kaarttalen worden ook niet behoorlijk gesorteerd.(HIDEN-25085)


## Controleren

- In de documentweergave in de revisie-interface wordt de inhoud voor bepaalde schermgrootten niet verpakt. Gebruikers moeten dan horizontaal schuiven om de volledige inhoud weer te geven. (GUIDEN-25292)


## Bekende problemen

Adobe heeft het volgende bekende probleem voor de release 2025.06.0 geïdentificeerd:

- Als u de optie Zoeken en vervangen gebruikt en de bewerking Eén exemplaar vervangen hebt toegepast op een bestand, kunnen geen verdere acties meer worden uitgevoerd in het deelvenster Zoeken en vervangen. (HIDEN-28930)

- Wanneer in een mappenprofiel een al geïndexeerd element uit de gebruikersinterface wordt verwijderd, wordt het bijbehorende geïndexeerde pad niet verwijderd en mislukt een poging om het element opnieuw te indexeren met een foutbericht. (HULPLIJNEN-29147) <br>**Oplossing:** u moet de verouderde weg verwijderen die niet meer bestaat alvorens het re-indexeren in werking te stellen.

- Als een kaart cyclische afhankelijkheden bevat en u de Kaartweergave opent, zijn de weergaven Source, Auteur en Layout niet toegankelijk totdat de pagina is vernieuwd. (HULPLIJNEN-28334) <br>**Oplossing:** u moet de pagina verfrissen om toegang tot deze meningen te herstellen.
