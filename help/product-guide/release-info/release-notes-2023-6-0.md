---
title: Opmerkingen bij de release | Upgradeinstructies en opgeloste problemen in Adobe Experience Manager Guides, release van juni 2023
description: Meer informatie over de opgeloste problemen en hoe u een upgrade kunt uitvoeren naar de release van Adobe Experience Manager Guides as a Cloud Service in juni 2023
exl-id: df17ee33-9f50-4223-ab9f-a57a31097d22
feature: Release Notes
role: Leader
source-git-commit: 6d8c01f20f7b59fed92c404561b647d9ebecb050
workflow-type: tm+mt
source-wordcount: '1170'
ht-degree: 0%

---

# Release van Adobe Experience Manager Guides as a Cloud Service in juni 2023

Deze versienota behandelt de verbeteringsinstructies, verenigbaarheidsmatrijs, en kwesties die in versie Juni 2023 van Adobe Experience Manager Guides (later die als *worden bedoeld AEM Guides as a Cloud Service*) worden bevestigd.

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, zie [ wat in Juni 2023 versie van AEM Guides as a Cloud Service ](whats-new-2023-6-0.md) nieuw is.

## Upgrade naar juni 2023

Voer de volgende stappen uit om uw huidige AEM Guides as a Cloud Service-installatie bij te werken:

1. Controle uit de code van Git van Cloud Servicen en schakelaar aan de tak die in de pijpleiding van Cloud Servicen wordt gevormd die aan het milieu beantwoordt dat u wilt bevorderen.
2. Werk de eigenschap `<dox.version>` in het `/dox/dox.installer/pom.xml` -bestand van de Git-code van de Cloud Service bij naar 2023.6.297.
3. Leg de wijzigingen vast en voer de pijplijn met Cloud Servicen uit om de release van AEM Guides as a Cloud Service in juni 2023 te voltooien.

## Stappen om de trigger van een script via een servlet in te schakelen

Nadat u de installatie hebt voltooid, kunt u ervoor kiezen om de trigger te HIT om de vertaaltaak te starten:

POST:

```
http://localhost:4503/bin/guides/script/start?jobType=translation-map-upgrade
```

Reactie:

```
{
"msg": "Job is successfully submitted and lock node is created for future reference",
"lockNodePath": "/var/dxml/executor-locks/translation-map-upgrade/1683190032886",
"status": "SCHEDULED"
}
```

In de vorige reactie JSON bevat de sleutel `lockNodePath` het pad naar het knooppunt dat in de opslagplaats is gemaakt en dat naar de verzonden taak wijst. Het wordt automatisch verwijderd als de taak is voltooid. Tot dan kunt u naar dit knooppunt verwijzen voor de huidige status van de taak.

Wacht tot deze taak is voltooid voordat u verdergaat met de volgende stappen.

>[!NOTE]
>
> Controleer of het knooppunt nog aanwezig is en wat de status van de taak is.

```
GET
http://<aem_domain>/var/dxml/executor-locks/translation-map-upgrade/1683190032886.json
```

## Stappen om de bestaande inhoud te posten om het verbroken koppelingsrapport te gebruiken

(Alleen als u een versie hebt die ouder is dan juni 2023, release van AEM Guides as a Cloud Service)

Voer de volgende stappen uit voor de naverwerking van de bestaande inhoud en het gebruik van het nieuwe verbroken koppelingsrapport:

1. (Optioneel) Als het systeem meer dan 100.000 dita-bestanden bevat, werkt u `queryLimitReads` under `org.apache.jackrabbit.oak.query.QueryEngineSettingsService` bij tot een hogere waarde (een waarde die groter is dan het aantal aanwezige elementen, bijvoorbeeld 200.000) en herstelt u deze vervolgens.

   - Gebruik de instructies die in *worden gegeven de met voeten treedt van de Configuratie* sectie in installeer en vorm Adobe Experience Manager Guides
as a Cloud Service om het configuratiebestand te maken.
   - In het configuratiedossier, verstrek de volgende (bezit) details om de queryLimitReads optie te vormen:

     | PID | Eigenschappensleutel | Waarde van eigenschap |
     |---|---|---|
     | org.apache.jackrabbit.oak.query.QueryEngineSettingsService | queryLimitReads | Waarde: 200000 Standaardwaarde: 100000 |

1. Voer een verzoek van de POST op de server uit (met correcte authentificatie) - `http://<server:port>//bin/guides/reports/upgrade`.

1. De API retourneert een jobId. Als u de status van de taak wilt controleren, kunt u een aanvraag voor een GET met taak-id naar hetzelfde eindpunt verzenden - `http://<server:port>/bin/guides/reports/upgrade?jobId= {jobId}`
(Bijvoorbeeld: `http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678`)

1. Wanneer de taak is voltooid, reageert de vorige GET-aanvraag met succes. Als de taak om een of andere reden mislukt, kan de fout worden gezien in de serverlogboeken.

1. Terugkeren naar de standaardwaarde of vorige bestaande waarde van `queryLimitReads` als u deze hebt gewijzigd in stap 1.

## Stappen om de bestaande inhoud te indexeren om de nieuwe zoek- en vervangings- en onderwerpenlijst onder het tabblad Rapporten te gebruiken:

(Alleen als u een versie gebruikt die ouder is dan de release van AEM Guides as a Cloud Service van september 2022)

Voer de volgende stappen uit om de bestaande inhoud te indexeren en de nieuwe vondst en vervangt tekst op kaartniveau en onderwerpenlijst onder het rapportlusje te gebruiken:

1. Voer een POST-aanvraag uit op de server \(met correcte verificatie\) - `http://<server:port\>/bin/guides/map-find/indexing` . (Optioneel: u kunt specifieke paden van de kaarten doorgeven om deze te indexeren. Standaard worden alle kaarten geïndexeerd \|\| Bijvoorbeeld : `https://<Server:port\>/bin/guides/map-find/indexing?paths=<map\_path\_in\_repository\>`)

1. U kunt ook een hoofdmap doorgeven om de DITA-kaarten van een specifieke map (en de bijbehorende submappen) te indexeren. Bijvoorbeeld `http://<server:port\>/bin/guides/map-find/indexing?root=/content/dam/test` . Wanneer zowel de parameter paths als de hoofdparameter worden doorgegeven, wordt alleen de parameter paths gebruikt.

1. De API retourneert een jobId. Als u de status van de taak wilt controleren, kunt u een aanvraag van een GET met taak-id naar hetzelfde eindpunt verzenden - `http://<server:port\>/bin/guides/map-find/indexing?jobId=\{jobId\}`\(bijvoorbeeld: `http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42`\)


1. Wanneer de taak is voltooid, reageert het vorige verzoek van de GET met succes en wordt vermeld of kaarten zijn mislukt. De met succes geïndexeerde kaarten kunnen van de serverlogboeken worden bevestigd.

## Compatibiliteitsmatrix

Deze sectie bevat een overzicht van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door de AEM Guides as a Cloud Service juni 2023-release.

### FrameMaker en FrameMaker Publishing Server

| AEM Guides als Cloud Release | FMPS | FrameMaker |
| --- | --- | --- |
| 2023,06,0 | Niet compatibel | 2022 of hoger |
| | | |


### Zuurstofaansluiting

| AEM Guides als Cloud Release | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2023,06,0 | 2.9-uuid-2 | 2.9-uuid-2 | 2,3 | 2,3 |
|  |  |  |  |


## Opgeloste problemen

De fouten die in verschillende gebieden zijn gecorrigeerd, worden hieronder weergegeven:

### Authoring

- Navtitle wordt verwijderd uit content33 bij het schakelen van de layoutweergave naar de auteur- of bronweergave. 12174
- Soms treedt een toepassingsfout op bij het klikken op een DITA-kaart. (11842)
- Webeditor | De vaste ruimte wordt toegevoegd in de Redacteur van XML terwijl het uitgeven van een onderwerp. (11786)
- Elementinterface | In de lijstweergave kunnen de overschreven beschikbare kolommen niet worden samengevoegd. 11528
- Keyref wordt niet opgelost in de kaartweergave. (11490)
- Het bovenste menu wordt niet weergegeven wanneer u door de XML-editor navigeert. 10868
- `conref` in tag ph | Het weergegeven dialoogvenster Bladeren is onjuist. 9481
- Lokale koppelingen naar andere elementen worden niet opgelost in de webeditor. 8790
- De functie Matches() werkt niet in de functie schema. (11224)


### Beheer

- Het lusje van rapporten in de Redacteur UI van het Web toont niet de onderwerpenlijst van oude kaarten DITA die vóór 4.2 verbetering worden gecreeerd. (11708)

- De functionaliteit van de knop Bestanden uploaden in het gebruikersinterface-einde van Assets in versie 4.2. (11633)

### Publiceren

- Publiceren naar AEM site mislukt bij het lezen van tijdelijke bestanden uit pod die mogelijk zijn vernieuwd of opnieuw zijn gestart. (1213)
- Native PDF | Het publiceren van inhoud die een outputklasse met steunen () heeft leidt tot een het publiceren bevriezing. (1936)
- JSON-uitvoer | Metagegevens met een eigenschap toewijzen die de waarde `"value in spaces and double quotes"` heeft, leiden tot een publicatiefout. (1933)
- Webeditor | Uitvoerpad en sjabloon kunnen niet worden geselecteerd in de AEM Voorinstelling. (11530)
- Native PDF | Aangepaste kenmerken worden niet doorgegeven aan de HTML- of PDF-engine. (DXML-12005)
- Native PDF |  Java OutOfMemoryError treedt op bij het publiceren van grote inhoud. (11789)
- JSON-uitvoer | De eigenschap `fmUuid` op het knooppunt jcr:content van JSON verschilt van de eigenschap &quot;id&quot; in de JSON. 11564
- JSON-uitvoer | Als de kaart en het onderwerp met zelfde filename aanwezig zijn, wordt JSON voor de kaart verwijderd. 11524
- Native PDF | Xref drukt de inhoud van href onderwerptitel in plaats van het etiket Xref. (11322)
- Native PDF | Kan de sjablooninstellingen voor PDF niet opslaan. 10751
- Native PDF | De tekst breidt zich voorbij de kolombreedte uit bij het opnemen van meerdere Xrefs. 10876
- Native PDF | `<note>` `</note>` -element genereert geen extra bereiktitel van het type. 10549
- Native PDF | De taalmeta-gegevens kunnen niet in geproduceerde PDF worden geplaatst om aan WCAG 2.0 te voldoen. (12296)



### Vertaling

- Post-cloudrelease van februari (2302). Alle vertaalinhoud wordt weergegeven als Niet-gesynchroniseerd of Ontbrekend exemplaar. (11834)

### Controleren

- Nieuwe revisie-interface | De voorwaarden benadrukken, en tonen verberg werk anders dan hoe zij in de Redacteur van het Web werken. (11628)
