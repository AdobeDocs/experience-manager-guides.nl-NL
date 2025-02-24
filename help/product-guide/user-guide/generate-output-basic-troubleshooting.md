---
title: Basisprobleemoplossing
description: Los problemen op met basisoplossingen in AEM Guides. Leer om, het logboekdossier in een tekstredacteur te bekijken te kopiëren en te controleren en JSP compilatiefouten op te lossen.
exl-id: 57b88291-b5a3-4931-b3ed-f2b2ce7a463c
feature: Publishing, Troubleshooting
role: User
source-git-commit: ff75aca9ddd7b405501a62e055fb99bd5ea2291c
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 0%

---

# Basisprobleemoplossing {#id1821I0Y0G0A}

Wanneer u met Adobe Experience Manager Guides werkt, kunnen er fouten optreden tijdens het publiceren of openen van uw document. Dergelijke fouten zouden in de kaart DITA, onderwerp, of in het proces van Experience Manager Guides zelf kunnen zijn. Deze sectie verstrekt informatie over hoe te om tot informatie in het dossier van het het logboekdossier van de outputgeneratie toegang te hebben en te ontleden. Ook, als uw onderwerp DITA te groot is, dan zou u de JSP compilatiefout kunnen bekijken. Deze sectie verstrekt ook informatie over hoe te om de JSP compilatiefout op te lossen.

## Logbestand weergeven en controleren {#id1822G0P0CHS}

Voer de volgende stappen uit om het logboekbestand van de outputgeneratie te bekijken en te controleren:

1. Zodra u het proces van de outputgeneratie hebt in werking gesteld, uitgezochte **Output** in de DITA kaartconsole.

   De **Algemene** kolom van de **Gegenereerde Output** toont de pictogrammen om een visuele richtsnoer over het succes of de mislukking van de outputgeneratie te geven.

   ![](images/output-general-settings.png){width="300" align="left"}

   In de bovenstaande schermafbeelding geven het eerste en derde pictogram een mislukte uitvoergeneratie aan. Het tweede pictogram toont een succesvolle outputgeneratie maar met berichten. De laatste is een geslaagde outputgeneratie zonder enig bericht.

1. Selecteer de verbinding in **Gegenereerd bij** kolom nadat de baan volledig is.

   Het logbestand wordt op een nieuw tabblad geopend.

   ![](images/log-file.png){width="800" align="left"}

1. Pas de volgende filters toe om de tekst in het logbestand te markeren:
   - Onherstelbaar: hiermee worden de fatale fouten in het logbestand met roze kleur gemarkeerd.
   - Fout: markeert de fouten in het logbestand met oranje kleur.
   - Waarschuwing: hiermee worden de waarschuwingen in het logbestand gemarkeerd met paarse kleur.
   - Info: hiermee worden de informatieberichten in het logbestand gemarkeerd met een blauwe kleur.
   - Uitzondering: markeert de uitzonderingen in het logbestand met een gele kleur.
1. Met de navigatieknoppen Omhoog en Omlaag kunt u naar de gemarkeerde tekst in het logbestand gaan.

   U kunt ook door het logbestand bladeren en de berichten controleren.


## Het logbestand kopiëren en controleren in een teksteditor

Voer de volgende stappen uit om het logboekdossier van de outputgeneratie in een tekstredacteur te kopiëren en te controleren:

1. Zodra u het proces van de outputgeneratie hebt in werking gesteld, uitgezochte **Output** in de DITA kaartconsole.

1. Selecteer de verbinding in **Gegenereerd bij** kolom nadat de baan volledig is.

   Het logbestand wordt op een nieuw tabblad geopend.

1. Selecteer **knoop van het Logboek van het Exemplaar**. Het logbestand wordt naar het klembord gekopieerd.
1. Open een teksteditor en plak het logbestand in de editor.

1. Blader door het logbestand en controleer op berichten.

   Aan de hand van de volgende informatie kunt u bepalen of het DITA-bestand of het Experience Manager Guides-proces een fout bevat:

   - *DITA kaartdossier verwante fout*: Voor het geval dat er een fout in het DITA kaartdossier of een ander dossier in de kaart DITA wordt gevonden, zal het logboekdossier een koord, &quot;BUILD FAILED&quot;bevatten. U kunt de informatie in het logbestand controleren om het onjuiste bestand te zoeken en het probleem op te lossen.

   In het volgende voorbeeldfragment van het logboekdossier, kunt u het `BUILD FAILED` bericht samen met de reden voor de fout bekijken.

   ![](images/dita-error-in-log-file.png){width="650" align="left"}

   - *op Experience Manager Guides betrekking hebbende fout*: Het andere type van fout dat u in het logboekdossier kunt identificeren is verwant met het proces van Experience Manager Guides zelf. In dit geval wordt het DITA-toewijzingsbestand geparseerd, maar mislukt het genereren van de uitvoer door een interne fout in Experience Manager Guides. Voor dergelijke fouten moet u hulp vragen bij het team voor technische ondersteuning.

   In het volgende voorbeeldfragment van het logboekbestand kunt u het `BUILD SUCCESSFUL` -bericht weergeven, gevolgd door een andere technische fout.

   ![](images/process-error-in-log-file.png){width="650" align="left"}


## JSP-compilatiefout oplossen

Als uw onderwerp DITA te groot is, dan zou u de JSP compilatiefout \ (`org.apache.sling.api.request.TooManyCallsException` \) in uw browser kunnen bekijken. Deze fout kan optreden wanneer u een onderwerp opent voor bewerken, reviseren of publiceren.

Voer de volgende stappen uit om dit probleem op te lossen:

1. Selecteer in de globale navigatie Gereedschappen en kies Bewerkingen \> Webconsole.

   De Adobe Experience Manager Web Console Configuration-pagina wordt weergegeven.

1. Onderzoek naar en selecteer de *Apache Sling HoofdServlet* component.

   De configureerbare opties voor de Apache Sling Main Servlet worden weergegeven.

1. Verhoog de waarde voor het *Aantal Vraag per de parameter van het Verzoek* zoals per uw vereisten.


**Bovenliggend onderwerp:**[ Productie van de Output ](generate-output.md)
