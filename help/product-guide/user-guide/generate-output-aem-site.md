---
title: Incrementele productie van uitvoer
description: Leer hoe incrementele uitvoergeneratie voor AEM Sites werkt in AEM Guides.
exl-id: 019d9fbf-2f23-4669-8022-d693be75c1c3
feature: Publishing
role: User
source-git-commit: ac83f613d87547fc7f6a18070545e40ad4963616
workflow-type: tm+mt
source-wordcount: '579'
ht-degree: 0%

---


# Incrementele productie van uitvoer

>[!NOTE]
>
> Incrementele productie van uitvoer is alleen van toepassing op AEM Sites-uitvoer. U kunt ook alleen DITA \(.dita/.xml\)-onderwerpen opnieuw genereren op basis van een DITA-kaart of submappen. Als u een kaart DITA, sub-kaart, onderwerpgroep, of een onderwerp met `@processing-role="resource-only"` selecteert, dan is de regenerate optie niet beschikbaar.

Er zou een aantal instanties kunnen zijn waar u slechts een paar onderwerpen in uw kaart zou bijwerken DITA en duw slechts die bijgewerkte onderwerpen levend. Om dergelijke scenario&#39;s te behandelen, staat Experience Manager Guides u toe om stijgende output tot stand te brengen. Als u een paar onderwerpen hebt bijgewerkt, te hoeven u niet om de volledige kaart opnieuw te produceren DITA. U kunt alleen de bijgewerkte onderwerpen selecteren en opnieuw genereren.

Als uw kaart wordt bebroed en u één enkel onderwerp in die kaart hebt bijgewerkt, dan moet u de volledige kaart voor het bijgewerkte onderwerp of de inhoud regenereren om in de output te weerspiegelen. U zult niet de optie van de outputregeneratie op een onderwerpniveau krijgen, is het slechts beschikbaar op het \(gescheurde \) kaartniveau. Dit is van toepassing op de bovenliggende kaart en alle submaps.

Voer de volgende stappen uit om output voor een specifiek onderwerp of een groep onderwerpen opnieuw te produceren:

>[!IMPORTANT]
>
> Wanneer u de AEM Sites-uitvoer opnieuw genereert, wordt de uitvoer gemaakt met de huidige versie van de bestanden en niet met de gekoppelde basislijn.

## Incrementele uitvoer genereren vanuit de kaartconsole

Voer de volgende stappen uit om incrementele uitvoer voor AEM Sites te genereren met behulp van Kaartconsole:

1. [ open het DITA kaartdossier in de console van de Kaart ](./open-files-map-console.md).
1. Selecteer de AEM Sites-voorinstelling waarvoor u incrementele uitvoer wilt genereren.
1. In het **lusje van Onderwerpen**, selecteer de onderwerpen die u wilt publiceren.

   ![ het onderwerpenlijst van plaatsen ](images/aem-presets-topic-list.png) {align="left"}

   >[!NOTE]
   >
   > Wanneer een Basislijn in het **Inhoud** lusje wordt geselecteerd, toont de lijst van het Onderwerp onderwerpen en hun versies van de Basislijn in bijlage.<br><br>
   > De incrementele publicatie uit de lijst met onderwerpen moet alleen worden gebruikt als de structuur van de kaart niet is gewijzigd. Als er een verandering in de kaartstructuur/TOC is, dan zou de volledige kaart eens moeten worden gepubliceerd om TOC bij te werken.
1. Selecteer **sparen** om de veranderingen te bewaren.
1. Selecteer **produceren output** om de output te produceren.


## Incrementele uitvoer van het dashboard Kaart genereren

Voer de volgende stappen uit om incrementele uitvoer voor AEM Sites te genereren met behulp van het kaartdashboard:

1. Navigeer in de gebruikersinterface van Assets naar het DITA-kaartbestand en selecteer dit.

   De DITA kaartconsole verschijnt met de lijst van de Voorinstellingen van de Output beschikbaar om output te produceren.

1. Selecteer de **Onderwerpen** tabel.

   Een lijst van onderwerpen beschikbaar in de kaart DITA wordt getoond.

1. Selecteer de onderwerpen die u opnieuw wilt genereren.

   >[!NOTE]
   >
   > Als u nieuwe onderwerpen aan de kaart DITA hebt toegevoegd, zult u niet die nieuwe onderwerpen van hier kunnen produceren. U moet de onlangs toegevoegde onderwerpen eerst publiceren door de DITA kaart te gebruiken publiceert functie.

   ![](images/regenerate-topics.png){align="left"}

1. Selecteer **Regenerate**.

   De **Regenereer Geselecteerde pagina van Onderwerpen** verschijnt.

1. Selecteer de uitvoervoorinstelling die u wilt gebruiken om de geselecteerde onderwerpen opnieuw te genereren.

1. Selecteer **Regenereren** om het proces van de outputgeneratie te beginnen.


>[!IMPORTANT]
>
> Als u een onderwerptitel anders noemt en het onderwerp regenereert, reflecteert de bijgewerkte onderwerptitel niet in de DITA kaartlijst van inhoud. Om de onderwerptitel in TOC bij te werken, moet u de volledige kaart DITA produceren.

U kunt het huidige statuut van het verzoek van de outputgeneratie in de **Uitvoer** tabel bekijken. Voor meer informatie, mening [ bekijk het statuut van de taak van de outputgeneratie ](#view-the-status-of-the-output-generation-task).



**Bovenliggend onderwerp:** [ Begrijpend de output stelt ](generate-output-understand-presets.md) vooraf in
