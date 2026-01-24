---
title: Opmerkingen bij de release | Opgeloste problemen in de release 2024.12.0 van Adobe Experience Manager Guides
description: Meer informatie over de opgeloste problemen vindt u in de release 2024.12.0 van Adobe Experience Manager Guides as a Cloud Service.
exl-id: 04a57e1a-6e74-46f6-acde-5045d3dcacdc
source-git-commit: dd404c42863f0b4a5f31b54f770c0bf296d68ab9
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---

# Opgeloste problemen in de release 2024.12.0

Dit artikel heeft betrekking op de fouten die zijn opgelost in verschillende gebieden van de release 2024.12.0 van Adobe Experience Manager Guides as a Cloud Service.

Leer over [&#x200B; verbeteringsinstructies voor de versie 2024.12.0 &#x200B;](./upgrade-instructions-2024-12-0.md).

## Authoring

- Het maken van een DITA-kaart op een UUID-instantie mislukt wanneer `xmleditor.uniquefilenames` is ingeschakeld in `XMLEditorConfig` . (21201)
- Wanneer het sluiten van een dossier, worden de commentaren en de etiketten die in **worden toegevoegd sparen Veranderingen en ontgrendelen van het Dossier** dialoogdoos niet bewaard in de Geschiedenis van de Versie met de nieuwe versie. Dit is specifiek voor een gebruiksgeval waar **om Controle-binnen op Sluiten** vraagt of **vraagt om Nieuwe Versie op Sluiten** binnen `XMLEditorConfig` wordt toegelaten. (2006)
- De staat van het document duidelijk zoals **Gedaan** keert terug naar **Ontwerp** alvorens een nieuwe versie op te slaan, resulterend in de **Gedaan** staat die niet in om het even welke documentversies voortduurt. (2006)
- Unable to add a PDF file as an image reference in a topic in the Web Editor. (21206)
- Het selecteren van een DITA- dossier in Assets UI toont **Open in FrameMaker** optie, zelfs wanneer onbruikbaar gemaakt in de configuratie. (2008)

## Publiceren

- In de uitvoer Native PDF ontbreken hoofdstuktitels in de inhoudsopgave. Dit leidt tot een onjuiste hiërarchie. 21840


## Beheer

- De lekken van het middel komen toe te schrijven aan **Unclosed ResourceResolver** fouten in logboeken. (18488)
- Wanneer u een nieuwe of gedupliceerde basislijn maakt, worden labels in willekeurige volgorde weergegeven. (19307)


## Basislijn

- Het uitgeven en dan het opslaan van een basislijn op een chronologie van de wolkenopstelling na 1 minuut als de basislijn groot aantal onderwerpen of kaarten heeft. (1958)

## Vertaling

- De vertaling van de kaart gebruikend basislijn wordt langzaam en uiteindelijk ontbreekt om de lijst van alle bijbehorende onderwerpen en kaartdossiers te laden. (1973)

## Bekende problemen met tijdelijke oplossing

Adobe heeft de volgende bekende problemen vastgesteld in de release 2024.12.0 van Adobe Experience Manager Guides as a Cloud Service.

**de verwezenlijking van het Project ontbreekt terwijl het verwerken van inhoud vertaling**

Tijdens het verzenden van inhoud voor vertaling, mislukt het maken van het project met de volgende logfouten:

`com.adobe.cq.wcm.translation.impl.TranslationPrepareResource` Fout tijdens het verwerken van het vertaalproject

`com.adobe.cq.projects.api.ProjectException`: kan het project niet maken

Veroorzaakt door: `org.apache.jackrabbit.oak.api.CommitFailedException`: `OakAccess0000`: toegang geweigerd


**Oplossing**: Om deze kwestie op te lossen, voer de volgende tijdelijke stappen uit:

1. Voeg een repointbestand toe. In het geval, bestaat het dossier niet, creeer het dossier door de [&#x200B; steekproef uit te voeren opnieuw richt config aanmaakstappen &#x200B;](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-cloud-questions/repoinit-configuration-for-property-set-on-aem-as-cloud-service/m-p/438854?profile.language=nl).
2. Voeg de volgende regel in het bestand toe en implementeer de code:

   ```
   { "scripts": [ "set principal ACL for translation-job-service\n allow jcr:all on /home/users/system/cq:services/internal/translation\nend" ] }
   ```

3. Test de vertaling na implementatie.

