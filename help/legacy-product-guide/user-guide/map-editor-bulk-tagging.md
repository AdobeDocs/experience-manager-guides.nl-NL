---
title: Labels in bulk voor DITA-inhoud
description: Gebruik bulksgewijs labelen van inhoud in AEM Guides om de ontdekkingsmogelijkheden voor DITA-inhoud te verbeteren. Leer hoe u bulkcodes op één of meerdere onderwerpen toepast, verwijdert, weergeeft of verbergt.
feature: Metadata Management
role: User
hide: true
exl-id: b320e34f-ee0a-4cc3-b4f6-d322fbb29844
source-git-commit: ea597cd14469f21e197c700542b9be7c373aef14
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 0%

---

# Labels in bulk voor DITA-inhoud {#id179SG0TN05Z}

Met labels kunt u inhoud groeperen of classificeren in de gegevensopslagruimte en ook in de gepubliceerde uitvoer. Als u labels op uw inhoud hebt toegepast, kunt u gemakkelijk verwante onderwerpen zoeken in een DITA-kaart die u kan helpen bij het ontwerpen van inhoud. Met de gepubliceerde uitvoer kunnen eindgebruikers de juiste inhoud sneller vinden met de juiste tags.

Met AEM Guides kunt u DITA-inhoud na een paar klikken labelen. U kunt de bulketiketterende eigenschap gebruiken om veelvoudige markeringen op veelvoudige onderwerpen, een kaart DITA, of op een sub-kaart toe te passen. U kunt ook labels toepassen op een afzonderlijk onderwerp. Het etiketteren is de inheemse eigenschap in AEM, kunt u meer details over het creëren van en het leiden van markeringen in de [ Beheersende sectie van Markeringen ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/tags.html?lang=en) in de documentatie van AEM vinden.

AEM Guides geeft standaard geen leestoegang aan gebruikers in de map waarin alle tags in de AEM-opslagplaats zijn opgeslagen. Als u tags wilt gebruiken die zijn gedefinieerd in de AEM-opslagplaats, moet u de systeembeheerder vragen toegang te verlenen tot de map waarin de tags zijn opgeslagen.

## Bulktags toepassen

Gebruik de functie voor bulkcodes om meerdere tags tegelijk toe te passen. Voer de volgende stappen uit om markeringen op uw onderwerpen in een kaart toe te passen DITA:

1. Navigeer in de gebruikersinterface van Assets naar het DITA-kaartbestand en klik erop.

   De DITA kaartconsole verschijnt tonend de lijst van Output stelt beschikbaar om output te produceren.

1. Klik **Onderwerpen**.

   Een lijst van onderwerpen beschikbaar in de kaart DITA wordt getoond. De UUIDs van onderwerpen&#39; wordt getoond onder de onderwerptitel.

1. Selecteer de onderwerpen of submap waarop u tags wilt toepassen.

   ![](images/apply-tags-uuid.png){width="650" align="left"}


   >[!NOTE]
   >
   > In de bovenstaande schermafbeelding ziet u een submap die is geselecteerd en uitgevouwen. Bij het selecteren van de submap worden ook alle onderwerpen onder de submap geselecteerd.

1. Klik **toepassen Markeringen**.

   Het dialoogvenster Codes selecteren wordt geopend.

1. Selecteer een of meer tags die u wilt toepassen op de geselecteerde onderwerpen.

1. Bevestig uw selectie.

   De geselecteerde markeringen worden toegepast op de onderwerpen en naast de onderwerptitel getoond.

   >[!NOTE]
   >
   > Na het toevoegen van markeringen aan uw onderwerpen, als u een onderwerp beweegt of schrapt, dan worden de markeringen voor die onderwerpen ook verwijderd. Nochtans, blijft dat onderwerp in de kaart tot u het verwijdert.


## Tags toepassen op een afzonderlijk onderwerp

Voer de volgende stappen uit om markeringen op een individueel onderwerp toe te passen:

1. In Assets UI, navigeer aan en selecteer het onderwerpdossier waarop u markeringen wilt toepassen.

1. In de toolbar, klik **Eigenschappen**.

   De eigenschappenpagina van het onderwerp wordt weergegeven.

1. In het Basis lusje, klik het Browse pictogram naast het **gebied van Markeringen**.

1. Selecteer een of meer tags die u op het geselecteerde onderwerp wilt toepassen.

1. Bevestig uw selectie.

1. Klik **toepassen Markeringen**.

   De geselecteerde labels worden toegepast op het onderwerp en weergegeven in het veld Codes.

1. Klik **sparen &amp; Sluiten**.


## Labels verwijderen

Naar gelang uw bedrijfsbehoeften, kunt u de het etiketteren informatie voor om het even welk DITA onderwerp veranderen. U kunt gemakkelijk alle markeringen meteen verwijderen of slechts die markeringen verwijderen die op het onderwerp ongeldig zijn.

Voer de volgende stappen uit om alle markeringen uit één of meerdere onderwerpen te verwijderen:

1. Navigeer in de gebruikersinterface van Assets naar het DITA-kaartbestand en klik erop.

   De DITA kaartconsole verschijnt tonend de lijst van Output stelt beschikbaar om output te produceren.

1. Klik **Onderwerpen**.

   Een lijst van onderwerpen beschikbaar in de kaart DITA wordt getoond.

1. Selecteer de onderwerpen waarvan u tags wilt verwijderen.

1. Klik **verwijdert Markeringen**.

   >[!NOTE]
   >
   > Als het pictogram Codes verwijderen niet zichtbaar is, controleert u of u de functie Codes verbergen niet hebt ingeschakeld.

1. Voor de Bevestig dialoog van de Schrapping, klik **O.K.** om markeringen uit de geselecteerde onderwerpen te verwijderen.


## Tags tonen of verbergen

Als u een lange lijst van markeringen hebt die op uw onderwerpen worden toegepast, dan zou u het een beetje omslachtig kunnen vinden om te navigeren. U kunt eenvoudig tags verbergen in de weergave van de DITA-kaartconsole door op het pictogram Codes verbergen te klikken. Als de labels niet zichtbaar zijn, worden ook alle tags weergegeven wanneer u op Tags tonen klikt.

**Bovenliggend onderwerp:**&#x200B;[ leidt meta-gegevens ](manage-metadata.md)
