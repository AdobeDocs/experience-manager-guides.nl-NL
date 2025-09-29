---
title: Aanbevolen procedures voor het instellen van een mappenstructuur
description: Leer meer over de beste werkwijzen om mapstructuur in te stellen wanneer u werkt met de inhoud voor leren en training in Experience Manager Guides.
feature: Authoring
role: Admin
level: Experienced
source-git-commit: 64adc89966e60823f6b46fb062b7659ed150cfc3
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# Aanbevolen procedures voor het instellen van de mapstructuur

Dit artikel bevat essentiële stappen en aanbevolen procedures voor beheerders om mapstructuren in Adobe Experience Manager Guides in te stellen. Een goed georganiseerde mappenhiërarchie zorgt voor vloeiende workflows voor ontwerpen, publiceren en vertalen voor leer- en trainingsinhoud.

## De mapstructuur instellen

Als u toegang wilt tot verschillende functies voor het schrijven, publiceren en vertalen van Experience Manager Guides, moet u mappen instellen in de juiste hiërarchie, zoals hieronder wordt uitgelegd.

**creeer een wortel-vlakke omslag**

Begin door een wortelomslag voor uw organisatie te creëren. Dit fungeert als basis voor alle mappen op afdelingsniveau en algemeen gedeelde elementen.

Voorbeeld: `/content/dam/ABC-Corp/`

Maak in deze hoofdmap een speciale map voor het beheer van middelen die op meerdere afdelingen worden gebruikt. Bijvoorbeeld, creeer a **Gemeenschappelijke** omslag om gedeelde middelen zoals beelden, video&#39;s, en meer te omvatten.

![](assets/root-level-folder.png)

**creeer departementaal-vlakke omslagen**

Maak aparte mappen voor elke afdeling, zoals HR, Financiën en Legal, zodat ze hun eigen inhoud kunnen beheren.

![](assets/department-level-folders.png)
*Bijschrift: Afzonderlijke die omslagstructuur voor het Afdeling van u binnen de wortelomslag wordt gecreeerd*

**Beste praktijken voor het plaatsen van de omslagen van het afdelingsniveau**

- Creeer een specifieke **Gemeenschappelijke** > **activa** omslag onder elke afdeling voor op afdelingsniveau gemeenschappelijke activa (indien nodig).
- Als u de inhoud wilt delen voor vertaling, maakt u taalspecifieke mappen (bijvoorbeeld en, de, fr). Auteurs dienen alleen inhoud in de brontaalmap (zoals en) te maken of bij te werken, omdat inhoud buiten de brontaalmap niet in de vertaalworkflow is opgenomen. De andere taalmappen kunnen leeg blijven als plaatsaanduidingen. Leer meer over [ inhoudsomzetting ](../user-guide/translation.md).
- De toestemmingen kunnen worden gebruikt om toegang van specifieke afdelingen of gebruikers tot de pas gecreëerde omslagstructuur te beperken. Wijs bijvoorbeeld machtigingen toe om ervoor te zorgen dat alleen gebruikers van de HR-afdeling inhoud binnen de toegewezen map kunnen maken of wijzigen.

Herhaal dezelfde structuur voor andere afdelingen, zoals Financiën, Juridische Zaken, enz.

## De structuur van de uitvoermap instellen

De map `fm-ditaoutputs` fungeert als de standaardopslaglocatie voor gegenereerde uitvoer van leer- en trainingsinhoud. Deze output omvat typisch pakketten SCORM (de dossiers van het PIT) in de **alm** omslag en PDFs in de **pdf** omslag.U kunt deze standaardoutputweg op vooraf ingesteld niveau van de **console van de Kaart** veranderen indien nodig.

![](assets/fmdita-output-lc.png)

Wanneer u met meerdere afdelingen werkt, kunt u afdelingsspecifieke mappen maken in de mapstructuur van `fm-ditaoutputs` om ervoor te zorgen dat gebruikers binnen een specifieke afdeling toegang hebben tot de relevante uitvoermappen.

## Gebruikers maken en toewijzen aan de juiste groepen

Zodra de mappenhiërarchie is ingesteld, kunt u beginnen met het maken van gebruikers en deze toevoegen aan groepen, zodat zij toegang hebben tot relevante functies in de Experience Manager Guides. Experience Manager Guides biedt drie out-of-the-box groepen: auteurs, revisoren en uitgevers. Afhankelijk van de groep waaraan een gebruiker is gekoppeld, mogen deze specifieke taken uitvoeren. Zo kan het publiceren alleen worden uitgevoerd door een uitgever, maar niet door een auteur.

Om nieuwe gebruikers tot stand te brengen en hen toe te voegen aan groepen, navigeer aan **Hulpmiddelen** > **Veiligheid** > **Gebruikers**.

Voor de pagina van het Beheer van de Gebruiker, creeert de uitgezochte **&#x200B;**&#x200B;om een nieuwe gebruiker tot stand te brengen. Voeg gebruikersgegevens toe en wijs deze toe aan een groep.

![](assets/create-users-page.png)

Voor meer details, mening [ gebruikersbeleid en veiligheid ](../cs-install-guide/user-admin-sec.md)


## Machtigingen toewijzen aan elke gebruikersgroep

Nadat de gebruikers aan aangewezen groepen worden toegevoegd, vorm toestemmingen op groepsniveau om ervoor te zorgen zij toegang tot de correcte auteursings en outputomslagen in de Bewaarplaats hebben.

Om toestemmingen toe te wijzen, navigeer aan **Hulpmiddelen** > **Veiligheid** > **Toestemmingen**.

Met deze machtigingen kunt u ervoor zorgen dat gebruikers alleen inhoud binnen hun toegewezen mappen kunnen maken of wijzigen.

Voor meer details, mening [ Toestemmingen in AEM ](https://experienceleague.adobe.com/nl/docs/experience-manager-65/content/security/security#permissions-in-aem).

