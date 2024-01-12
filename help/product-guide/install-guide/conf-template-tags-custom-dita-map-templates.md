---
title: Aangepaste DITA-toewijzingssjabloon configureren
description: Leer hoe te om het malplaatje van de kaart van douaneDITA te vormen
exl-id: ea8a6687-1a7b-45c7-8cbc-161f9e88a8be
feature: Template Configuration
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# Aangepaste DITA-toewijzingssjabloon configureren {#id1774F04F05Z}

AEM hulplijnen worden geleverd met twee &#39;out-of-the-box&#39;-kaartsjablonen: DITA-kaart en -bladmap. U kunt kaarten tot stand brengen die op deze malplaatjes worden gebaseerd; of, kunt u uw eigen kaartmalplaatjes bepalen die dan kunnen worden gebruikt om nieuwe kaarten tot stand te brengen.

Voer de volgende stappen uit om uw malplaatjes van de douanekaart toe te voegen:

1. Meld u als beheerder aan bij Adobe Experience Manager.

1. Navigeer in de interface Middelen naar de map die is geconfigureerd voor het opslaan van de sjabloonbestanden voor de kaart. Door gebrek, worden alle kaartmalplaatjes opgeslagen in /content/dam/dita-templates/maps omslag.

   >[!NOTE]
   >
   > Om een douaneplaats te vormen om onderwerp of kaartmalplaatjes op te slaan, zie [Aangepast pad voor DITA-sjabloonmap configureren](conf-template-tags-custom-dita-topic-template.md#id191LCF0095Z)

1. Klikken **Maken** \> **DITA-sjabloon**.

1. Selecteer op de pagina Vervagen het type kaartsjabloon dat u wilt maken.

   >[!NOTE]
   >
   > U kunt de sjabloon Kaart of Bladwijzer gebruiken als basis voor uw nieuwe sjabloon.

1. Klik op **Next**.

1. Voer op de nieuwe pagina Sjablooneigenschappen een **Titel** en **Naam** voor de sjabloon.

   >[!NOTE]
   >
   > De naam wordt automatisch voorgesteld gebaseerd op de Titel van uw malplaatje. Als u de naam handmatig wilt opgeven, moet u ervoor zorgen dat de naam geen spaties, apostrof of accolades en einden met .ditamap bevat.

1. Klikken **Maken**.

   Het bericht Kaart gemaakt wordt weergegeven.

   U kunt de sjabloon openen om te bewerken in de Kaarteditor of het sjabloonbestand opslaan op de opslaglocatie van de sjabloon. Zodra het malplaatje wordt gecreeerd, kunt u de Redacteur van de Kaart gebruiken om het malplaatje aan uw auteursbehoeften aan te passen. Als een sjabloon eenmaal is ingesteld, moet u deze koppelen aan een algemeen profiel of aan een mapprofiel.


De volgende keer dat u een nieuwe kaart maakt, wordt de sjabloon weergegeven op de pagina Vervagen. Voor meer informatie over het creëren van een kaart DITA, zie *Adobe Experience Manager-hulplijnen gebruiken*.

>[!TIP]
>
> Zie de *Aangepaste sjablonen* in de gids met aanbevolen werkwijzen voor tips en trucs voor het gebruik van aangepaste kaartsjablonen.

**Bovenliggend onderwerp:** [Onderwerp- en kaartsjablonen configureren](conf-template-tags.md)
