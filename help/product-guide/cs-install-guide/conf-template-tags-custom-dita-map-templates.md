---
title: Aangepaste DITA-toewijzingssjabloon configureren
description: Leer hoe te om het malplaatje van de kaart van douaneDITA te vormen
exl-id: a0eeb43c-06e4-4922-a005-704e8929063f
feature: Template Configuration
role: Admin
level: Experienced
source-git-commit: 83971ee35a19cf0146ddd034b1ae7a345f587663
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---

# Aangepaste DITA-toewijzingssjabloon configureren {#id1774F04F05Z}

AEM Guides wordt geleverd met twee out-of-the-box kaartsjablonen — DITA-kaart en Bookmap. U kunt kaarten tot stand brengen die op deze malplaatjes worden gebaseerd; of, kunt u uw eigen kaartmalplaatjes bepalen die dan kunnen worden gebruikt om nieuwe kaarten tot stand te brengen.

Voer de volgende stappen uit om uw malplaatjes van de douanekaart toe te voegen:

1. Meld u als beheerder aan bij Adobe Experience Manager.

1. In Assets UI, navigeer aan de omslag die wordt gevormd om de dossiers van het kaartmalplaatje op te slaan. Door gebrek, worden alle kaartmalplaatjes opgeslagen in /content/dam/dita-templates/maps omslag.

   >[!NOTE]
   >
   > Om een douaneplaats te vormen om onderwerp op te slaan of malplaatjes in kaart te brengen, zie [ de weg van de malplaatjeomslag van douane DITA ](conf-template-tags-custom-dita-topic-template.md#id191LCF0095Z) vormen

1. Klik **creëren** \> **Sjabloon DITA**.

1. Selecteer op de pagina Vervagen het type kaartsjabloon dat u wilt maken.

   >[!NOTE]
   >
   > U kunt de sjabloon Kaart of Bladwijzer gebruiken als basis voor uw nieuwe sjabloon.

1. Klik op **Next**.

1. Voor de nieuwe pagina van de Eigenschappen van het malplaatje, ga a **Titel** en **Naam** voor het malplaatje in.

   >[!NOTE]
   >
   > De naam wordt automatisch voorgesteld gebaseerd op de Titel van uw malplaatje. Als u de naam handmatig wilt opgeven, moet u ervoor zorgen dat de naam geen spaties, apostrof of accolades en einden met .ditamap bevat.

1. Klik **creëren**.

   Het bericht Kaart gemaakt wordt weergegeven.

   U kunt de sjabloon openen om te bewerken in de Kaarteditor of het sjabloonbestand opslaan op de opslaglocatie van de sjabloon. Zodra het malplaatje wordt gecreeerd, kunt u de Redacteur van de Kaart gebruiken om het malplaatje aan uw auteursbehoeften aan te passen. Als een sjabloon eenmaal is ingesteld, moet u deze koppelen aan een algemeen profiel of aan een mapprofiel.


De volgende keer dat u een nieuwe kaart maakt, wordt de sjabloon weergegeven op de pagina Vervagen. Zie de handleiding Adobe Experience Manager Guides gebruiken voor meer informatie over het maken van een DITA-kaart.

>[!TIP]
>
> Zie *de de malplaatjes van de Douane* sectie in de Beste praktijken gids voor beste praktijken rond het gebruiken van de malplaatjes van de douanekaart.


## Het aantal verwijzingen in een DITA-kaart aanpassen

U kunt de drempel voor asynchrone verwerking vormen die op het aantal verwijzingen in de kaart DITA wordt gebaseerd. Standaard worden kaarten met meer dan 5 verwijzingen gemaakt via asynchrone bewerkingen, terwijl kaarten met minder verwijzingen synchrone bewerkingen blijven gebruiken.


Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](download-install-additional-config-override.md#) om het configuratiedossier tot stand te brengen. In het configuratiedossier, verstrek de volgende (bezit) details om aantal verwijzingen in het DITA kaartmalplaatje te specificeren om het proces synchroon te houden:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| com.adobe.fmdita.xmleditor.config.XmlEditorConfig | xmleditor.asyncmapcreation | > 0 <br> **Standaardwaarde**: 5 |

Wanneer het creëren van een kaart DITA met grote onderwerpverwijzingen gebruikend een douanemalplaatje, zou de kaartverwezenlijking op de wolkenserver ontbreken als de totale verwerkingstijd 60 seconden overschrijdt.

Om dit te verhinderen, vorm **asynchrone dita kaartverwezenlijking** in XmlEditorConfig die taken om parallel toestaat te lopen en verwerkingstijden voor grotere kaarten te verminderen DITA.

**Bovenliggend onderwerp:** [ vorm onderwerp en kaartmalplaatjes ](conf-template-tags.md)
