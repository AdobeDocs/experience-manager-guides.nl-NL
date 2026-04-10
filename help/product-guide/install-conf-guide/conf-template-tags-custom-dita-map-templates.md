---
title: Aangepaste DITA-toewijzingssjabloon configureren
description: Leer hoe te om het malplaatje van de kaart van douaneDITA te vormen
feature: Template Configuration
role: Admin
level: Experienced
source-git-commit: 6f3f05419f4f5cdd45ab580cdee6fa869f20f01d
workflow-type: tm+mt
source-wordcount: '668'
ht-degree: 0%

---

# Aangepaste DITA-toewijzingssjabloon configureren {#id1774F04F05Z}

AEM Guides wordt geleverd met twee out-of-the-box kaartsjablonen — DITA-kaart en Bookmap. U kunt kaarten tot stand brengen die op deze malplaatjes worden gebaseerd; of, kunt u uw eigen kaartmalplaatjes bepalen die dan kunnen worden gebruikt om nieuwe kaarten tot stand te brengen.

Op de volgende tabbladen vindt u instructies voor het configureren van een aangepaste DITA-kaartsjabloon op basis van uw Experience Manager Guides-instellingen: Cloud Service of On-Premise.


>[!BEGINTABS]

>[!TAB  Cloud Service ]

Voer de volgende stappen uit om uw malplaatjes van de douanekaart toe te voegen:

1. Meld u als beheerder aan bij Adobe Experience Manager.

1. In Assets UI, navigeer aan de omslag die wordt gevormd om de dossiers van het kaartmalplaatje op te slaan. Door gebrek, worden alle kaartmalplaatjes opgeslagen in /content/dam/dita-templates/maps omslag.

   >[!NOTE]
   >
   > Om een douaneplaats te vormen om onderwerp op te slaan of malplaatjes in kaart te brengen, zie [&#x200B; de weg van de malplaatjeomslag van douane DITA &#x200B;](conf-template-tags-custom-dita-topic-template.md#id191LCF0095Z) vormen

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

>[!TAB  Op locatie ]

Voer de volgende stappen uit om uw malplaatjes van de douanekaart toe te voegen:

1. Meld u als beheerder aan bij Adobe Experience Manager.

1. In Assets UI, navigeer aan de omslag die wordt gevormd om de dossiers van het kaartmalplaatje op te slaan. Door gebrek, worden alle kaartmalplaatjes opgeslagen in /content/dam/dita-templates/maps omslag.

   >[!NOTE]
   >
   > Om een douaneplaats te vormen om onderwerp op te slaan of malplaatjes in kaart te brengen, zie [&#x200B; de weg van de malplaatjeomslag van douane DITA &#x200B;](conf-template-tags-custom-dita-topic-template.md#id191LCF0095Z) vormen

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

>[!ENDTABS]

Het bericht Kaart gemaakt wordt weergegeven.

     u kunt verkiezen om het malplaatje voor het uitgeven in de Redacteur van de Kaart te openen, of het malplaatjedossier in de plaats van de malplaatjeopslag op te slaan. Zodra het malplaatje wordt gecreeerd, kunt u de Redacteur van de Kaart gebruiken om het malplaatje aan uw auteursbehoeften aan te passen. Zodra een malplaatje op zijn plaats is, zorg ervoor dat u het of met een globaal of omslag-niveau profiel associeert.


De volgende keer dat u een nieuwe kaart maakt, wordt de sjabloon weergegeven op de pagina Vervagen. Voor meer informatie over het creëren van een kaart DITA, zie *Gebruikend Adobe Experience Manager Guides*.

>[!TIP]
>
> Zie de *sectie van de Malplaatjes van de Douane* in de Beste praktijken gids voor beste praktijken rond het gebruiken van de malplaatjes van de douanekaart.


## Het aantal verwijzingen in een DITA-kaart aanpassen (alleen voor Cloud Service)

U kunt de drempel voor asynchrone verwerking vormen die op het aantal verwijzingen in de kaart DITA wordt gebaseerd. Standaard worden kaarten met meer dan 5 verwijzingen gemaakt via asynchrone bewerkingen, terwijl kaarten met minder verwijzingen synchrone bewerkingen blijven gebruiken.

Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-config-override.md#) om het configuratiedossier tot stand te brengen. In het configuratiedossier, verstrek de volgende (bezit) details om aantal verwijzingen in het DITA kaartmalplaatje te specificeren om het proces synchroon te houden:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| com.adobe.fmdita.xmleditor.config.XmlEditorConfig | xmleditor.asyncmapcreation | > 0 <br> **Standaardwaarde**: 5 |

Wanneer het creëren van een kaart DITA met grote onderwerpverwijzingen gebruikend een douanemalplaatje, zou de kaartverwezenlijking op de wolkenserver ontbreken als de totale verwerkingstijd 60 seconden overschrijdt.

Om dit te verhinderen, vorm **asynchrone dita kaartverwezenlijking** in XmlEditorConfig die taken om parallel toestaat te lopen en verwerkingstijden voor grotere kaarten te verminderen DITA.


**Bovenliggend onderwerp:** [&#x200B; vorm onderwerp en kaartmalplaatjes &#x200B;](conf-template-tags.md)
