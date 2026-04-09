---
title: Opmerkingen bij de release | Opgeloste problemen in Adobe Experience Manager Guides, release 2026.04.0
description: Meer informatie over de opgeloste problemen vindt u in de release 2026.04.0 van Adobe Experience Manager Guides as a Cloud Service.
source-git-commit: ce2c9da0d9beb05a15f7cefcf9483e0c93abbf37
workflow-type: tm+mt
source-wordcount: '816'
ht-degree: 0%

---

# Opgeloste problemen in de release 2026.04.0

Dit artikel heeft betrekking op de fouten die zijn verholpen in verschillende gebieden van de release 2026.04.0 van Adobe Experience Manager Guides as a Cloud Service.

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, mening [&#x200B; wat in de versie 2026.04.0 &#x200B;](whats-new-2026-04-0.md) nieuw is.

Leer over [&#x200B; verbeteringsinstructies voor de versie 2026.04.0 &#x200B;](upgrade-instructions-2026-04-0.md).

## Authoring

- Als u een Schematron-bestand (`*.sch` ) bewerkt en de functie Zoeken en vervangen gebruikt, wordt het deelvenster Zoeken en vervangen gedeeltelijk buiten het scherm onderaan weergegeven, waardoor toegang tot de invoervelden en -besturingselementen wordt voorkomen. (GUIDEN-38412)

## Publiceren

- Wanneer hetzelfde onderwerp opnieuw wordt gebruikt op meerdere kaarten met verschillende voorwaardelijke voorinstellingen, overschrijft het publiceren van de nieuwste kaart naar Salesforce de inhoud van het onderwerp, waardoor onjuiste gegevens worden weergegeven aan gebruikers van eerder gepubliceerde kaarten. (GUIDEN-37806)
- Wanneer u een native PDF publiceert voor een kaart die voorwaardelijke verwerking of bepaalde geneste kaarten bevat, wordt de `dc:title` die is gedefinieerd in de kaart niet weergegeven op de PDF-omslag, waardoor een titel van de omslag ontbreekt. (GUIDEN-37733)
- Het genereren van de uitvoer van de AEM-site (met samengestelde componenttoewijzing) voor een toewijzing mislukt en resulteert in een fout wanneer de variabele `map_title` aanwezig is in het uitvoerpad. (GUIDEN-36968)
- Wanneer een uitvoerpad met een schuine streep wordt opgegeven in de voorinstelling voor eigen PDF-uitvoer, voegt de gebruikersinterface automatisch een extra schuine streep aan het einde toe. Dit resulteert in een pad met een dubbele schuine streep die ervoor zorgt dat de PDF-upload in bepaalde scenario&#39;s mislukt. (GUIDEN-34932)
- Als u AEM Sites-pagina&#39;s publiceert die zijn gegenereerd vanuit DITA-inhoud via Snel publiceren of Publicatie beheren, worden de bijbehorende DITA-elementen onbedoeld gepubliceerd. (GUIDEN-27967)
- Wanneer het publiceren van een kaart aan AEM Sites (gebruikend erfeniscomponentenafbeelding), de verwijzingen (`xrefs`) met `scope = peer` die subelementen van een onderwerp (zoals paragrafen) in een verschillende kaart richten oplossen niet aan specifiek element identiteitskaart en in plaats daarvan oplossen slechts aan het ouderonderwerp, die de pagina veroorzaken om bij het begin van het onderwerp te laden eerder dan het scrollen aan de voorgenomen sectie. (HIDEN-21802)


## Vertaling

- Wanneer een afbeelding die oorspronkelijk werd beheerd als taalspecifiek middel met een specifieke versie (bijvoorbeeld onder `/en/`), wordt verplaatst naar een algemene map met een bijgewerkte versie en er wordt een basislijnexport uitgevoerd, blijft de nieuwe basislijn verwijzen naar verouderde taalspecifieke versies van die afbeelding, wat leidt tot een mislukte basislijnexport. (GUIDEN-39394)
- Wanneer het verwerken van vertaalprojecten die buiten Experience Manager Guides worden gecreeerd, worden de veelvoudige berichten van het foutenlogboek geproduceerd verklarend dat *`fmTarget`geen bezit* wordt gevonden. (GUIDEN-37804)

## Basislijn

- Wanneer u een dynamische basislijn maakt, reageert de Editor soms niet meer omdat meerdere gelijktijdige API-aanvragen worden uitgevoerd, waardoor alle andere bewerkingen worden gestopt. (GUIDEN-39054)

## Controleren

- Wanneer u een gebruiker toewijst aan een revisietaak, worden in het vervolgkeuzemenu alle gebruikers weergegeven in plaats van alleen de gebruikers die zijn gekoppeld aan de geselecteerde projecten. Dit leidt tot ongeldige gebruikersopties. (GUIDEN-37781)

## Rapporten

- Bij het openen van een rapport voor een kaart is er een vertraging in het laden van het deelvenster Filters (GUIDES-39385)

## Bekende problemen

Adobe heeft de volgende bekende problemen vastgesteld voor de release 2026.04.0:

- Er wordt een leeg scherm geladen wanneer u een dubbele voorinstelling voor de ServiceNow Knowledge Base maakt. (HIDEN-42732)
- De API voor het ophalen van de documentstatus retourneert een null-reactie voor sommige bestanden, waardoor onjuiste documentstatussen worden weergegeven in de gebruikersinterface. (HIDEN-42561)
- UI-aanpassingen op basis van tabnamen in het kaartdashboard worden niet toegepast. (HULPLIJNEN-42285)
- Wanneer een bestand in zowel de Editor als het deelvenster Zoeken is geopend en u het verwijdert uit het deelvenster Verkenner, wordt het bestand verwijderd en wordt de lijst Verkenner vernieuwd. Als u de pagina vernieuwt, wordt het bestand wel weergegeven in het deelvenster Zoeken. (HIDEN-41935)
- Terwijl het bijwerken van een actieve overzichtstaak, als een onderwerp dat reeds deel van het overzicht uitmaakt wordt verwijderd en dan opnieuw toegevoegd zonder **Update** te klikken, wordt de recensent(s) informatie in het lusje van Revisoren verloren.   (GUIDEN-38774)
- Als u een onderwerp in de modus Voorvertoning selecteert, wordt dit niet gemarkeerd in de weergave Kaart als het onderwerp zich in de bladwijzers (voorgrond, hoofdstuk, onderdeel of achtergrond) of een deel van de cyclische inhoud bevindt. (HIDEN-42416)
- In Assets UI, wordt de **Beweging** knoop niet toegelaten op de eerste poging wanneer meer dan 2 dossiers of omslagen worden geselecteerd. (HULPLIJNEN-42721) <br> **Oplossing**: Na het selecteren van meer dan twee dossiers of omslagen, wacht op een paar seconden alvorens de bestemmingsomslag te selecteren.
- Wanneer u aan **voorkeur van de Gebruiker** van de Redacteur navigeert en de wortelkaart bijwerkt terwijl de wijze van de Voorproef in de Redacteur open is, laadt de kaartvoorproef als leeg scherm wanneer u aan de Redacteur terugkeert. (HULPLIJNEN-42412) <br> **Oplossing**: Het verfrissen van de voorproef gebruikend **verfrist** pictogram beschikbaar op de wijze van de Voorproef lost de kwestie.
- Het anders noemen van een bestaand malplaatje werkt niet de naam in het **malplaatjes van de Output** paneel bij tot de pagina manueel wordt verfrist. (HULPLIJNEN-42528) <br> **Oplossing**: Vernieuw browser om de bijgewerkte malplaatjenaam in het paneel van de malplaatjes van de Output te bekijken.
