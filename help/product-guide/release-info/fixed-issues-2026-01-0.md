---
title: Opmerkingen bij de release | Opgeloste problemen in Adobe Experience Manager Guides, release 2026.01.0
description: Meer informatie over de opgeloste problemen vindt u in de release 2026.01.0 van Adobe Experience Manager Guides as a Cloud Service.
source-git-commit: 8a9a82e79c757e403141e853aafbc64e1618c30a
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---

# Opgeloste problemen in de release 2026.01.0

Dit artikel heeft betrekking op de fouten die zijn verholpen in verschillende gebieden van de release 2026.01.0 van Adobe Experience Manager Guides as a Cloud Service.

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, mening [ wat in de versie 2026.01.0 ](whats-new-2026-01-0.md) nieuw is.

Leer over [ verbeteringsinstructies voor de versie 2026.01.0 ](upgrade-instructions-2026-01-0.md).

## Authoring

- Wanneer u een inline MathML-vergelijking bijwerkt met de optie MathML bewerken in het contextmenu, wordt de bijgewerkte waarde pas weergegeven wanneer de pagina is vernieuwd. (GUIDEN-38198)
- Wanneer een onderwerp vele herbruikbare elementen (die met IDs) bevat die in het Herbruikbare paneel worden toegevoegd, kunnen sommige elementen niet wegens vaste containerhoogte toegankelijk zijn. (GUIDEN-37220)
- Wanneer u een kruisverwijzing naar een bestand invoegt, zijn de pictogrammen voor mappen en onderwerpen identiek.(GUIDEN-36662)
- Wanneer u een kaart bewerkt, worden speciale symbolen in de `navtitle` niet weergegeven voor `topichead` in de weergave Auteur. (HIDEN-35435)
- Onbekwaam om de veelvoudige etiketten van de Versie aan een onderwerp van **toe te voegen sparen als nieuwe versie** dialoog. (GUIDEN-32716)

## Beheer van bedrijfsmiddelen

- Kan versielabels niet verwijderen uit het deelvenster Versiegeschiedenis in de gebruikersinterface van Assets. (GUIDEN-38276)
- Wanneer het uploaden van activa met filename die ongeldige karakters bevatten, ontbreekt de activa om een onjuist bericht **Dossier te uploaden en te tonen wordt gesloten door andere gebruiker** ondanks de activa die worden ontgrendeld. (HULPLIJNEN-32680)
- In de zoekopdracht in Assets worden subelementen en metagegevensknooppunten (zoals afbeeldingen en PDF&#39;s) ten onrechte in de resultaten opgenomen. Bovendien retourneert de zoekopdracht voor een voorinstelling voor uitvoer wanneer DITAVAL-filters worden toegepast intern gegenereerde DITAVAL-bestanden die zijn gemaakt op basis van voorinstellingen voor voorwaarden. (HIDEN-35418)

## Publiceren

- Bij het genereren van AEM Sites-uitvoer worden de kaartitels met trefwoorden en onderwerptitels met het element `<ph>` niet opgenomen in de gepubliceerde uitvoer. (GUIDEN-36641)
- Wanneer u publiceert met een aangepaste voorinstelling met inhoud die koppelingen bevat naar PDF&#39;s zonder dat het bereik als extern is ingesteld, kan het proces niet worden voltooid. (HULPLIJNEN-21708)
- Wanneer bulkactivering wordt uitgevoerd, voegt het maken van het pakket filters toe voor alle paden die onder de eigenschap `fileReference` van een pagina worden vermeld, inclusief externe paden en peerpaden. (HULPLIJNEN-2487)
- In native PDF-uitvoer geeft het `abbreviated-form` -element de `glossterm` weer in plaats van de toegewezen `glossSurfaceForm` of `glossAcronym` . (GUIDEN-26393)
- Voor native PDF-uitvoer wordt het `<alt>` -element voor afbeeldingen genegeerd, zodat er geen alternatieve tekst kan worden toegepast voor toegankelijkheid. (GUIDES-29087)
- Wanneer u tijdelijke bestanden downloadt voor een kaart met een basislijn tijdens het publiceren voor een voorinstelling, verwijst het `metadata.xml` -bestand onjuist naar de `versionPath` in plaats van naar de `dampath` .(GUIDEN-29815)
- Wanneer u een onderwerp maakt of bewerkt dat een aanhalingsteken bevat, wordt de PDF niet gegenereerd als het veld Auteur niet wordt toegevoegd aan het dialoogvenster voor aanroepen. (GUIDEN-37934)
- Het CSS-bestand (`rhdefault.css`) wordt onjuist toegepast op de PDF-sjabloon, ondanks dat er niet naar CSS wordt verwezen, waardoor de logboekbestanden met fouten voor CSS-bestanden ontbreken.(GUIDEN-31752)

## Platform

- Wanneer het proberen om een onderwerp of een kaart te bewaren, kan de verrichting met a **met mislukte a tijdelijk ontbreken om dossier** fout, met name tijdens intensieve taken van de activaverwerking of vertaalwerkschema&#39;s op de achtergrond te bewaren die. (GUIDEN-37837)
- Als u `scope="external"` gebruikt voor een verwijzing naar DAM-inhoud binnen een onderwerp of kaart, wordt het relatieve pad van het element vervangen door een GUID. (GUIDEN-38783)

## Rapporten

- Het rapport van de verbroken lijst bevat onjuist externe koppelingen, geldige `keyrefs` en trefwoorden die correct zijn omgezet binnen het bereik van de huidige kaart. (HULPLIJNEN-2774)

## Bekende problemen

Adobe heeft de volgende bekende problemen vastgesteld voor de release 2026.01.0:

- Wanneer een onderwerp in-overzicht van een aan de gang zijnde overzichtstaak wordt verwijderd, blijft zijn documentstaat **in Overzicht** blijven, alhoewel het onderwerp geen langer deel van om het even welke overzichtstaak is. (HULPLIJNEN-38709) <br>**Oplossing**: Verander de documentstaat van het onderwerp van **in Overzicht** aan de aangewezen staat van de pagina van Eigenschappen of het paneel van de Eigenschappen van het Dossier.
- Wanneer het uitvoeren van een onderzoek dat **gebruikt vindt en vervangt**, als u een dossier van de onderzoeksresultaten opent, het sluit, en dan probeert om het opnieuw te openen door het vermelde resultaat te selecteren, ontbreekt het dossier om opnieuw te openen. (HULPLIJNEN-39050) <br>**Oplossing**: Open om het even welk ander dossier van de onderzoeksresultaten eerst, dan heropen het eerder gesloten dossier van de lijst om de kwestie op te lossen.
- Als u Hulplijnen gebruikt met een databaseserver, voor inhoud die zelfverwijzingen bevat, worden in het rapport van de onderwerpenlijst ongeldige items voor elke zelfverwijzing weergegeven, wat resulteert in een onnauwkeurig aantal bestanden. (GUIDEN-39420)












