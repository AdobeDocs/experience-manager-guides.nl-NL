---
title: Rapport voor hergebruik van inhoud
description: Leer hoe u het rapport voor hergebruik van inhoud kunt weergeven in AEM Guides. Genereer het rapport om het percentage voor hergebruik van de inhoud te zoeken.
exl-id: ccae4303-75b1-4077-829a-7ef6a14fd8ad
feature: Report Generation
role: User
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%

---

# Rapport voor hergebruik van inhoud {#id205BB900OQD}

Een ander nuttig rapport dat u kunt produceren is het Rapport van de Hergebruik van de Inhoud. Dit rapport berekent het gemiddelde percentage van het inhoudsgebruik, dat zeer nuttig voor projectmanagers en bedrijfseigenaars is om de hoeveelheid inhoud te zien die wordt opnieuw gebruikt.

>[!TIP]
>
> Voor een goede werking van het Rapport voor hergebruik van inhoud moet u de nabewerkingsworkflow inschakelen. Neem contact op met de systeembeheerder voor het inschakelen van workflows na verwerking.

Voer de volgende stappen uit om het Rapport voor hergebruik van inhoud weer te geven:

1. Klik op de verbinding van Adobe Experience Manager bij de bovenkant en kies **Hulpmiddelen**.

1. Selecteer **Gidsen** van de lijst van hulpmiddelen.

1. Klik op de **tegel van het Rapport van de Hergebruik van de Inhoud 0}**.

1. Klik **doorbladeren** om een weg te kiezen waar uw onderwerpen verblijven of manueel de weg ingaan.

   Het rapport wordt gegenereerd door de inhoud in de bovenliggende en alle onderliggende mappen te scannen.

1. Klik **produceren Rapport** om het Rapport van de Hergebruik van de Inhoud te krijgen.

   ![](images/content-reuse-uuid.png){width="800" align="left"}

   De rapportpagina bestaat uit twee delen:

   - **Overzicht van het Rapport:**

     Hiermee geeft u het gemiddelde hergebruik van inhoud weer, dat wordt berekend als Instanties voor hergebruik van inhoud/Totaal aantal onderwerpen. Dit rapport houdt rekening met alle verwijzingen naar directe inhoud op het eerste niveau en onderwerpverwijzingen voor berekening. De Instanties voor hergebruik van inhoud wordt berekend als de som van waarden in het veld Aantal keren opnieuw gebruikt. Het onderwerp dat het meest wordt hergebruikt is ook vermeld in de Samenvatting van het Rapport. Het klikken op de verbinding van het onderwerp in het Meest gebruikte Onderwerp opent de voorproef van het onderwerp.

   - **Details:**

     De sectie Details bevat de volgende kolommen:

      - **Titel**: De titel van het onderwerp. Als u op de titelkoppeling van het onderwerp klikt, wordt de voorvertoning van het onderwerp geopend.

      - **UUID**: Het universeel unieke herkenningsteken \ (UUID \) van het dossier.

      - **Grootte**: De grootte van dossiers in bytes.

      - **Status**: De huidige staat van het document - Ontwerp, In-Overzicht of herzien.

      - **Aantal Hergebruikte Tijden**: Aantal tijden het overeenkomstige onderwerp is opnieuw gebruikt. Dit is berekend als de som van de vermeldingen in de kolommen waarnaar wordt verwezen min 1.

      - **die door** wordt verwezen: De onderwerpen waarin het overeenkomstige onderwerp is van verwijzingen voorzien. Hier worden alleen de directe verwijzingen \(first level\) in overweging genomen. Meerdere onderwerpen worden gescheiden door komma&#39;s. UUID van het referenced dossier wordt ook vermeld tussen haakjes.Het klikken op de de titelverbinding van het onderwerp opent de onderwerpvoorproef.


>[!NOTE]
>
> U kunt het Rapport voor hergebruik van inhoud ook exporteren in CSV-indeling. Klik hiertoe op de koppeling Exporteren naar CSV in de linkerbovenhoek van het scherm en kies een locatie waar u het CSV-bestand wilt opslaan. U kunt dit CSV-bestand vervolgens openen in elke CSV-editor.

**Bovenliggend onderwerp:**[ Rapporten ](reports-intro.md)
