---
title: Opmerkingen bij de release | Upgradeinstructies en opgeloste problemen in Adobe Experience Manager Guides, release van juli 2023
description: Meer informatie over de opgeloste problemen en hoe u een upgrade kunt uitvoeren naar de release van Adobe Experience Manager Guides as a Cloud Service van juli 2023
exl-id: f1765c6a-cb8e-4a06-a6f4-f5c225b6bc88
feature: Release Notes
role: Leader
source-git-commit: 6e23f52fc9124d0f07f8108da1b5fe574f553469
workflow-type: tm+mt
source-wordcount: '926'
ht-degree: 0%

---

# Release van Adobe Experience Manager Guides as a Cloud Service in juli 2023

Deze versienota behandelt de verbeteringsinstructies, verenigbaarheidsmatrijs, en kwesties die in versie worden bevestigd juli 2023 van Adobe Experience Manager Guides (later die als *wordt bedoeld as a Cloud Service van AEM Guides*).

Voor meer informatie over de nieuwe eigenschappen en de verhogingen, zie [&#x200B; wat in de versie van juli 2023 van AEM Guides as a Cloud Service &#x200B;](whats-new-2023-7-0.md) nieuw is.

## Upgrade naar release juli 2023

Voer de volgende stappen uit om uw huidige AEM Guides as a Cloud Service-installatie bij te werken:

1. Bekijk de Git-code van Cloud Services en schakel over naar de vertakking die is geconfigureerd in de Cloud Services-pijplijn die overeenkomt met de omgeving die u wilt upgraden.
2. Werk de eigenschap `<dox.version>` in het `/dox/dox.installer/pom.xml` -bestand van de Git-code voor Cloud Services bij naar 2023.7.0.314.
3. Leg de wijzigingen vast en voer de Cloud Services-pijplijn uit om naar de release van juli 2023 van AEM Guides as a Cloud Service te upgraden.

## Stappen om de trigger van een script via een servlet in te schakelen

(Alleen als u een versie hebt die ouder is dan juni 2023, release van AEM Guides as a Cloud Service)

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
as a Cloud Service, om het configuratiebestand te maken.
   - In het configuratiedossier, verstrek de volgende (bezit) details om de queryLimitReads optie te vormen:

     | PID | Eigenschappensleutel | Waarde van eigenschap |
     |---|---|---|
     | org.apache.jackrabbit.oak.query.QueryEngineSettingsService | queryLimitReads | Waarde: 200000 Standaardwaarde: 100000 |

1. Voer een POST-aanvraag uit op de server (met correcte verificatie) - `http://<server:port>//bin/guides/reports/upgrade` .

1. De API retourneert een jobId. Als u de status van de taak wilt controleren, kunt u een GET-aanvraag met taak-id naar hetzelfde eindpunt verzenden - `http://<server:port>/bin/guides/reports/upgrade?jobId= {jobId}`
(Bijvoorbeeld: `http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678`)

1. Zodra de taak is voltooid, reageert het vorige GET-verzoek met succes. Als de taak om een of andere reden mislukt, kan de fout worden gezien in de serverlogboeken.

1. Terugkeren naar de standaardwaarde of vorige bestaande waarde van `queryLimitReads` als u deze hebt gewijzigd in stap 1.

## Stappen om de bestaande inhoud te indexeren om de nieuwe zoek- en vervangings- en onderwerpenlijst onder het tabblad Rapporten te gebruiken:

(Alleen als u een versie hebt die ouder is dan juni 2023, release van AEM Guides as a Cloud Service)

Voer de volgende stappen uit om de bestaande inhoud te indexeren en de nieuwe vondst en vervangt tekst op kaartniveau en onderwerpenlijst onder het rapportlusje te gebruiken:

1. Voer een POST-aanvraag uit op de server \(met correcte verificatie\) - `http://<server:port\>/bin/guides/map-find/indexing` . (Optioneel: u kunt specifieke paden van de kaarten doorgeven om deze te indexeren. Standaard worden alle kaarten geïndexeerd \|\| Bijvoorbeeld : `https://<Server:port\>/bin/guides/map-find/indexing?paths=<map\_path\_in\_repository\>`)

1. U kunt ook een hoofdmap doorgeven om de DITA-kaarten van een specifieke map (en de bijbehorende submappen) te indexeren. Bijvoorbeeld `http://<server:port\>/bin/guides/map-find/indexing?root=/content/dam/test` . Wanneer zowel de parameter paths als de hoofdparameter worden doorgegeven, wordt alleen de parameter paths gebruikt.

1. De API retourneert een jobId. Als u de status van de taak wilt controleren, kunt u een GET-aanvraag met taak-id naar hetzelfde eindpunt verzenden - `http://<server:port\>/bin/guides/map-find/indexing?jobId=\{jobId\}`\(bijvoorbeeld: `http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42`\)


1. Als de taak is voltooid, reageert het vorige GET-verzoek met succes en vermeldt u of kaarten zijn mislukt. De met succes geïndexeerde kaarten kunnen van de serverlogboeken worden bevestigd.

## Compatibiliteitsmatrix

In deze sectie wordt een overzicht gegeven van de compatibiliteitsmatrix voor de softwaretoepassingen die worden ondersteund door de AEM Guides as a Cloud Service-release van juli 2023.

### FrameMaker en FrameMaker Publishing Server

| AEM Guides als Cloud Release | FMPS | FrameMaker |
| --- | --- | --- |
| 2023,07,0 | Niet compatibel | 2022 of hoger |
| | | |


### Zuurstofaansluiting

| AEM Guides als Cloud Release | Oxygeenaansluiting, Windows | Oxygeenconnector Mac | Bewerken in Oxygen Windows | Bewerken in Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2023,07,0 | 2.9-uuid-2 | 2.9-uuid-2 | 2,3 | 2,3 |
|  |  |  |  |  |


## Opgeloste problemen

De fouten die in verschillende gebieden zijn gecorrigeerd, worden hieronder weergegeven:

### Authoring

- De inline-/weergavekenmerken worden niet weergegeven in de layoutweergave van de webeditor. 12498
- Bestanden uploaden in de insteekmodule Oxygen voor AEM Guides werkt niet in cloudservices als u dat hebt! in de bestandsnaam. (1207)
- Het publiceren van DITA-kaarten gaat erg langzaam met bewerkbare sjablonen. 12075
- De configuratie van de globale profiel-UI komt niet overeen met het mapprofiel. (1970)
- Inhoudsverwijzingen worden verbroken wanneer DITA-bestanden worden gekopieerd en geplakt. (1959)
- Kan inhoudsfragment niet bewerken in de kolomweergave als AEM Guides is geïnstalleerd. 7342
- Inhoud gaat verloren wanneer een onverpakt xref zich onder subelementtags bevindt. 12532

### Publiceren

- De goedkeuringswerkstroom werkt niet wanneer de documentstatus wordt gewijzigd in &quot;eindstatus&quot; in de bestandseigenschappen van het rechterdeelvenster. (1026)
