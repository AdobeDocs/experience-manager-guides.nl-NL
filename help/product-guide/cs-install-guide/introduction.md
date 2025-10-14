---
title: Over deze handleiding
description: Meer informatie over deze handleiding
exl-id: cdd40267-3f0c-40d2-acbc-2ebe43633c2f
feature: Introduction
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '663'
ht-degree: 2%

---

# Over deze handleiding {#id175MC0P0S5Z}

Adobe Experience Manager Guides \ (later die als *wordt bedoeld AEM Guides* \) is een krachtige, op wolk-gebaseerde oplossing van het de componentenbeheer van ondernemingsniveau \ (CCMS \). Het maakt native DITA-ondersteuning in Adobe Experience Manager mogelijk en biedt AEM de mogelijkheid om op DITA gebaseerde inhoud te maken en te leveren. Het machtigt auteurs om inhoud tot stand te brengen gebruikend makkelijk te gebruiken ingebouwde Redacteur van het Web en het te publiceren in diverse outputformaten.

Deze handleiding bevat de instructies voor het downloaden, installeren en configureren van AEM Guides. In deze handleiding vindt u gedetailleerde instructies voor het instellen van AEM Guides op basis van uw behoeften op het gebied van ontwerpen en publiceren voor organisaties.

Deze handleiding is bedoeld voor het volgende type publiek:

- Beheerders, die AEM Guides zouden installeren en beheren.

- Uitgevers, die de publicatietaak zouden uitvoeren om uitvoer in verschillende indelingen te genereren.


## Inhoudstructuur

De informatie in deze handleiding is als volgt geordend:

- [&#x200B; Ongeveer deze gids &#x200B;](#id175MC0P0S5Z): Dit onderwerp verstrekt een inleiding aan deze gids, voorgenomen publiek, en hoe de informatie in deze gids wordt georganiseerd.

- [&#x200B; Download en installeer &#x200B;](download-install.md#): Dit onderwerp beschrijft om, AEM Guides te downloaden te installeren of te bevorderen.

- [&#x200B; beleid van de Gebruiker en veiligheid &#x200B;](user-admin-sec.md#): Dit onderwerp beschrijft het kernconcept gebruikers en authentificatie in AEM en de standaardgebruikersgroepen die door AEM Guides worden gecreeerd.

- [&#x200B; specialisatie DITA-OT van het Gebruik en DITA &#x200B;](dita-ot-specialization.md#): Dit onderwerp verklaart hoe te om douaneDITA-OT stop-ins te vormen en specialisatie te gebruiken DITA.

- [&#x200B; vorm documentstaten &#x200B;](customize-doc-state.md#): Dit onderwerp verklaart hoe te om douanestatus voor uw documenten te vormen DITA.

- [&#x200B; migreer bestaande inhoud &#x200B;](migrate-content.md#): Dit onderwerp beschrijft hoe te aan boord uw bestaande inhoud op AEM bewaarplaats.

- [&#x200B; vorm filenames &#x200B;](conf-file-names.md#): Dit onderwerp verklaart hoe te om het plaatsen te vormen om dossiernamen automatisch toe te wijzen en een regex voor geldige dossier te bepalen - noem karakters.

- [&#x200B; vorm onderwerp en kaartmalplaatjes &#x200B;](conf-template-tags.md#): Dit onderwerp beschrijft hoe te om onderwerp en kaartmalplaatjes te vormen om aan uw auteursbehoeften te voldoen. Leer hoe u het systeem in AEM kunt labelen en hoe u tags kunt configureren voor gebruik met AEM Guides.

- [&#x200B; pas de Redacteur van het Web &#x200B;](conf-web-editor.md#) aan: Dit onderwerp verklaart de diverse aanpassingen die u in de Redacteur van het Web kunt maken om zijn functionaliteit te verbeteren.

- [&#x200B; omvat @navtitle attributen door gebrek &#x200B;](auto-add-navtitle.md#): Dit onderwerp verklaart hoe te om het `@navtitle` attribuut aan een verwijzingsdossier in een kaart toe te voegen door gebrek.

- [&#x200B; vorm globale of omslag-vlakke profielen &#x200B;](conf-folder-level.md#): Dit onderwerp verklaart het proces om omslagprofielen tot stand te brengen en toestemmingen te geven aan specifieke gebruikers.

- [&#x200B; het beheer van de Versie &#x200B;](version-management.md#): Dit onderwerp beschrijft hoe te om automatische dossiercontrole voor dossiers te vormen die voor het uitgeven in de Redacteur van het Web worden geopend.

- [&#x200B; vormt de montages van de outputgeneratie &#x200B;](conf-output-generation.md#): Dit onderwerp beschrijft de diverse configuraties die u kunt maken om het proces van de standaardoutputgeneratie aan te passen.

- [&#x200B; vorm en pas werkschema&#39;s &#x200B;](customize-workflows.md#) aan: Dit onderwerp beschrijft diverse configuraties om de standaardwerkschema&#39;s aan te passen die in AEM Guides worden verscheept.

- [&#x200B; vertaal inhoud &#x200B;](translation.md#): Dit onderwerp verstrekt verbindingen aan de relevante artikelen van de Hulp in AEM documentatie om u te helpen het vertaalkader begrijpen en vormen. Leer ook hoe u op componenten gebaseerde vertaalworkflows kunt inschakelen.

- [&#x200B; vorm onderzoek naar AEM Assets UI &#x200B;](conf-dita-search.md#): Dit onderwerp beschrijft hoe te om DITA inhoudsonderzoek in Assets UI te vormen en uw douanekenmerken in onderzoek toe te voegen.


## Overzicht van Adobe Experience Manager \(AEM\)

[&#x200B; Adobe Experience Manager \ (AEM \) &#x200B;](https://business.adobe.com/products/experience-manager/adobe-experience-manager.html) is een uitvoerige oplossing van het inhoudsbeheer voor de bouw van websites, mobiele apps, en vormen. AEM helpt u uw marketinginhoud en -middelen te beheren. AEM is as a Cloud Service beschikbaar. Met AEM as a Cloud Service kunt u uw klanten voorzien van persoonlijke, contentgestuurde ervaringen door de kracht van het AEM Content Management System te combineren met AEM Digital Asset Management. Enkele belangrijke bronnen die u kunnen helpen om op AEM as a Cloud Service te starten en te implementeren zijn:

- [&#x200B; as a Cloud Service Overzicht van de Experience Manager &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/home.html?lang=nl-NL)
- [&#x200B; Begonnen het worden met de Weg van de Migratie aan AEM as a Cloud Service &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/migration-journey/getting-started.html?lang=nl-NL)
- [&#x200B; Begin op instapniveau aan Experience Manager as a Cloud Service &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/onboarding/home.html?lang=nl-NLhttps://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/home.html?lang=en)
- [Applicaties voor AEM as a Cloud Service implementeren](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/home.html?lang=nl-NL)
- [Implementeren naar AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/deploying/overview.html?lang=nl-NL)
- [&#x200B; as a Cloud Service Gids van Assets &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/home.html?lang=nl-NL)

## Aanvullende bronnen

Na is een lijst van andere nuttige middelen van AEM Guides, die op [&#128279;](https://helpx.adobe.com/nl/support/xml-documentation-for-experience-manager.html) pagina Leren &amp; van de Steun beschikbaar zijn:

- Handboek
- API-naslaggids
