---
title: '@navtitle-kenmerk standaard opnemen'
description: Leer hoe u standaard @navtitle-kenmerk kunt opnemen
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 6f3f05419f4f5cdd45ab580cdee6fa869f20f01d
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# @navtitle-kenmerk standaard opnemen {#id2115BC0J0XA}

U kunt verschillende soorten verwijzingsdossiers in een kaart toevoegen, bijvoorbeeld onderwerp, verwijzing, taak, \(sub\) kaarten, etc. De meeste van deze bestanden ondersteunen het kenmerk `@navtitle` . Niet veel auteurs gebruiken het echter consistent. Als u het gebruik van het kenmerk `@navtitle` wilt afdwingen in alle bestanden waarnaar wordt verwezen in een kaart, kunt u dit doen met een eenvoudige configuratie.

Als deze optie is ingeschakeld, wordt het kenmerk `@navtitle` automatisch toegevoegd aan de eigenschappen van elk referentiebestand dat u in een kaart toevoegt. De `@navtitle` krijgt ook de waarde van het `title` -element van de inhoud waarnaar wordt verwezen.

Op de volgende tabbladen vindt u instructies voor het standaard opnemen van het kenmerk `@navtitle` in de eigenschappen van referentiebestanden op basis van de Experience Manager Guides-instelling: Cloud Service of On-Premise.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

1. U kunt als beheerder het configuratiebestand van de gebruikersinterface downloaden door u aan te melden bij Adobe Experience Manager.
1. Klik op de verbinding van Adobe Experience Manager bij de bovenkant en kies **Hulpmiddelen**.
1. Selecteer **Gidsen** van de lijst van hulpmiddelen en klik de **Profielen van de Omslag**.
1. Klik op de **Globale tegel van het Profiel**.
1. Selecteer het **lusje van de Configuratie van de Redacteur van XML** en klik **uitgeven** pictogram op de bovenkant
1. Klik het **pictogram van de Download** om het ui \_config.json- dossier op uw lokaal systeem te downloaden.
1. U kunt deze wijziging doorvoeren op algemeen niveau of op een mapniveau. Afhankelijk van waar u deze wijziging wilt aanbrengen, moet u het respectievelijke bestand ui\_config.json downloaden. Voor meer informatie over het downloaden ui\_config.json- dossier, zie [&#x200B; vormen en de Redacteur van het Web van XML aanpassen &#x200B;](conf-profiles.md#id2065G300O5Z).

1. Zoek naar de `ditaAttributes` definitie.

   De standaarddefinitie van `ditaAttributes` is:

   ```
   "ditaAttributes": {
                           "attributes": [],
                           "constraint": false,
                           "required": {}
                           },
   ```

1. Verander de parameter `required` zoals hieronder getoond:

   ```
   "required": {"navtitle": true}
   ```

   Wanneer de reeks aan `true`, **verfrist het attribuut van de navigatitel** knoop wordt toegelaten om omhoog in de toolbar van de Redacteur te tonen. Wanneer ingesteld op `false` of leeg gelaten, blijft de knop verborgen in de Editor.
1. Sla het bestand op.

1. Upload het bestand in het bijbehorende profiel \(Algemeen of Map\).


Met deze configuratie bevat elk referentiebestand dat u toevoegt aan een kaart standaard het kenmerk `@navtitle` .

>[!TAB  Op locatie ]

1. Download het bestand ui\_config.json.

   U kunt deze wijziging doorvoeren op algemeen niveau of op een mapniveau. Afhankelijk van waar u deze wijziging wilt aanbrengen, moet u het respectievelijke bestand ui\_config.json downloaden. Voor meer informatie over het downloaden ui\_config.json- dossier, zie [&#x200B; vormen en de Redacteur van het Web van XML aanpassen &#x200B;](conf-profiles.md#id2065G300O5Z).

1. Zoek naar de `ditaAttributes` definitie.

   De standaarddefinitie van `ditaAttributes` is:

   ```json
   "ditaAttributes": {
   "attributes": [],
   "constraint": false,
   "required": {}
   },
   ```

1. Wijzig de parameter `required` als:

   ```json
   "required": {"navtitle": true}
   ```

1. Sla het bestand op.

1. Upload het bestand in het bijbehorende profiel \(Algemeen of Map\).


Met deze configuratie bevat elk referentiebestand dat u toevoegt aan een kaart standaard het kenmerk `@navtitle` .

>[!ENDTABS]

**Bovenliggend onderwerp:**&#x200B;[&#x200B; pas de Redacteur van het Web &#x200B;](customize-overview.md) aan
