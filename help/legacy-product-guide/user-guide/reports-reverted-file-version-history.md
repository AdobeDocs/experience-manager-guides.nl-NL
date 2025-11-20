---
title: Rapport voor versiehistorie van teruggedraaide bestanden
description: Rapporten over versiehistorie van omgekeerde bestanden weergeven in AEM Guides. Leer hoe u versielogboeken kunt terugkeren vanuit de gebruikersinterface van Assets, de voorvertoning van onderwerpen en de gereedschapsselectie van AEM's.
feature: Report Generation
role: User
hide: true
exl-id: c787947a-b235-4c12-a9cc-eac5136d31db
source-git-commit: 5081aa032c13ca684c6882149448b05c77028a90
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 0%

---

# Rapport voor versiehistorie van teruggedraaide bestanden {#id205BBC00PRK}

Wanneer u aan veelvoudige gelijktijdige versies samen met veelvoudige auteurs werkt, is uw inhoud verbindend om veelvoudige versies te hebben. Er zou wat gemeenschappelijke informatie over veelvoudige versies kunnen zijn, die verschillende auteurs in hun project konden gebruiken. Om dergelijke werktoewijzingen af te handelen, kunnen auteurs meerdere versies van bestanden gebruiken. Dergelijke versies kunnen gewoon een nieuwere versie van een bestand zijn of een eerdere versie. Het is een complexe taak om vast te stellen wanneer een bestand is teruggezet en waarom.

Met AEM Guides kunt u een versiehistorierapport genereren voor een afzonderlijk bestand of voor alle bestanden in een map. Deze versiegeschiedenis geeft u een geconsolideerde mening van alle versies van een dossier dat werd teruggedraaid en wie die versies en de reden creeerde om die versies tot stand te brengen.

{{$include /help/_includes/overview.md}}

U kunt dit rapport openen op de volgende plaatsen:

- **Assets UI**: door een dossier te selecteren en de **Geschiedenis van de Versie** van linkerspoor te openen. De **mening van de Geschiedenis van de Versie** bevat de **Revert Logs van de Versie** verbinding bij de bodem van het paneel. Wanneer u op deze koppeling klikt, wordt de geschiedenis van de omgezette versies van het geselecteerde bestand weergegeven.

  ![](images/revert-log-from-assets-ui.png){width="300" align="left"}

- **voorproef van het Onderwerp**: wanneer u een onderwerp previewing, kunt u ook het **paneel van de Geschiedenis van de Versie** van het linkerspoor omhoog brengen. U zult een paneel gelijkend op Assets UI van waar krijgen u de **Revert Logboeken van de Versie** verbinding kunt klikken om tot de teruggekeerde versiegeschiedenis van het actieve document toegang te hebben.

- **AEM sectie van Hulpmiddelen**: u kunt tot dit rapport van de sectie van Hulpmiddelen van AEM ook toegang hebben. In de volgende procedure wordt uitgelegd hoe u de versiegeschiedenis kunt herstellen vanuit de sectie AEM Tools.


Voer de volgende stappen uit om tot het Terugkeren rapport van de Geschiedenis toegang te hebben:

1. Klik op de verbinding van Adobe Experience Manager bij de bovenkant en kies **Hulpmiddelen**.

1. Selecteer **Gidsen** van de lijst van hulpmiddelen.

1. Klik op de **Versie terugkeert de tegel van de Geschiedenis** terug.

   Er wordt een lege pagina Versiehistorie herstellen weergegeven waar u naar een bestand of map moet bladeren en deze moet selecteren om het rapport te genereren.

1. Klik **tonen Logboeken** om het rapport voor het geselecteerde dossier of de omslag te produceren.

   ![](images/revert-version-history-report.png){width="800" align="left"}

   Het verslag bevat de volgende gegevens:

   - **Naam van het Dossier**: De titel van het onderwerp. Als u op de titelkoppeling van het onderwerp klikt, wordt de voorvertoning van het onderwerp geopend.

   - **Stempel van de Tijd**: De datum en de tijd toen het onderwerp aan een vroegere versie werd teruggedraaid.

   - **Gebruiker**: Naam van de gebruiker die aan een vroegere versie terugkwam.

   - **keert van** terug: Het originele versieaantal van het dossier van waar het werd teruggedraaid.

   - **terugkeren aan**: De versie waaraan het dossier werd teruggedraaid aan.

   - **Commentaar**: Om het even welke die commentaar door de gebruiker wordt gegeven die het dossier terugkeerde.



**Bovenliggend onderwerp:**&#x200B;[&#x200B; Rapporten &#x200B;](reports-intro.md)
