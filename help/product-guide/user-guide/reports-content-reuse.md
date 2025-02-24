---
title: Rapport voor hergebruik van inhoud
description: Leer hoe u het rapport voor hergebruik van inhoud kunt weergeven in AEM Guides. Genereer het rapport om het percentage voor hergebruik van de inhoud te zoeken.
exl-id: ccae4303-75b1-4077-829a-7ef6a14fd8ad
feature: Report Generation
role: User
source-git-commit: ae36a7fdff6ae147619340aa3a3d2bb6c7774fe0
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# Rapport voor hergebruik van inhoud {#id205BB900OQD}

Een ander nuttig rapport dat u kunt produceren is het Rapport van de Hergebruik van de Inhoud. Dit rapport berekent het gemiddelde percentage van het inhoudsgebruik, dat zeer nuttig voor projectmanagers en bedrijfseigenaars is om de hoeveelheid inhoud te bekijken die wordt opnieuw gebruikt.

>[!TIP]
>
> Voor een goede werking van het Rapport voor hergebruik van inhoud moet u de nabewerkingsworkflow inschakelen. Neem contact op met de systeembeheerder voor het inschakelen van workflows na verwerking.

Voer de volgende stappen uit om het Rapport voor hergebruik van inhoud weer te geven:

1. Selecteer het embleem van Adobe Experience Manager bij de bovenkant en kies **Hulpmiddelen**.

1. Selecteer **Gidsen** van de lijst van hulpmiddelen.

1. Selecteer de **tegel van het Rapport van het Hergebruik van de Inhoud 0}**.

1. Selecteer **doorbladeren** om een weg te kiezen waar uw onderwerpen verblijven of manueel de weg ingaan.

   Het rapport wordt gegenereerd door de inhoud in de bovenliggende en alle onderliggende mappen te scannen.

1. Selecteer **produceren Rapport** om het Rapport van de Hergebruik van de Inhoud te krijgen.

   ![](images/content-reuse-uuid.png){width="800" align="left"}

   De rapportpagina bestaat uit twee delen:

   - **Overzicht van het Rapport:**

     Hiermee geeft u het gemiddelde hergebruik van inhoud weer, dat wordt berekend als Instanties voor hergebruik van inhoud/Totaal aantal onderwerpen. Dit rapport houdt rekening met alle verwijzingen naar directe inhoud op het eerste niveau en onderwerpverwijzingen voor berekening. De Instanties voor hergebruik van inhoud wordt berekend als de som van waarden in het veld Aantal keren opnieuw gebruikt. Het onderwerp dat het meest wordt hergebruikt is ook vermeld in de Samenvatting van het Rapport. Het selecteren van de verbinding van het onderwerp in het Meest gebruikte Onderwerp opent de voorproef van het onderwerp.

   - **Details:**

     De sectie Details bevat de volgende kolommen:

      - **Titel**: De titel van het onderwerp. Het selecteren van de de titelverbinding van het onderwerp opent de onderwerpvoorproef.

      - **UUID**: Het universeel unieke herkenningsteken \ (UUID \) van het dossier.

      - **Grootte**: De grootte van dossiers in bytes.

      - **Status**: De huidige staat van het document - Ontwerp, In-Overzicht of herzien.

      - **Aantal Hergebruikte Tijden**: Aantal tijden het overeenkomstige onderwerp is opnieuw gebruikt. Dit is berekend als de som van de vermeldingen in de kolommen waarnaar wordt verwezen min 1.

      - **die door** wordt verwezen: De onderwerpen waarin het overeenkomstige onderwerp is van verwijzingen voorzien. Hier worden alleen de directe verwijzingen \(first level\) in overweging genomen. Meerdere onderwerpen worden gescheiden door komma&#39;s. UUID van het referenced dossier wordt ook vermeld tussen haakjes.Selecterend op de de titelverbinding van het onderwerp opent de onderwerpvoorproef.


>[!NOTE]
>
> U kunt het Rapport voor hergebruik van inhoud ook exporteren in CSV-indeling. Selecteer hiertoe Exporteren naar CSV-koppeling in de linkerbovenhoek van het scherm en kies een locatie waar u het CSV-bestand wilt opslaan. U kunt dit CSV-bestand vervolgens openen in elke CSV-editor.

**Bovenliggend onderwerp:**[ Inleiding aan rapporten ](reports-intro.md)
