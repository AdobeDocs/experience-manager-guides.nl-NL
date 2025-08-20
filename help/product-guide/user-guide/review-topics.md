---
title: Onderwerpen bekijken
description: Leer hoe u onderwerpen kunt beoordelen en de functies kunt gebruiken als revisor, documentweergave, onderwerpweergave, contextafhankelijke werkbalk, voorvertoningsmodus, bijlagen toevoegen aan opmerkingen en deelvenster Voorwaarden in AEM Guides.
exl-id: fc87fc37-f1cd-4a19-96c2-3a08a8222002
feature: Reviewing
role: User
source-git-commit: b7648fe1d36de3c243ca5a55f42a41f7523056ce
workflow-type: tm+mt
source-wordcount: '2655'
ht-degree: 0%

---

# Onderwerpen bekijken {#id2056B0W0FBI}

Als u een revisor bent, ontvangt u een e-mail met een revisieverzoek met de koppeling naar de revisieonderwerpen. Met deze koppeling hebt u toegang tot de overzichtspagina waarop u uw feedback over de gedeelde onderwerpen kunt toevoegen.

>[!NOTE]
>
> Terwijl u het revisieverzoek opent vanuit het bericht, kunt u het opnieuw toewijzen aan een andere gebruiker die deel uitmaakt van hetzelfde revisieproject. Voor details, wijst de mening [ opnieuw revisietaak toe gebruikend bericht ](./reassign-review-using-notification.md).

Voer de volgende stappen uit om een onderwerp te herzien:

1. Selecteer de directe koppeling in het e-mailverzoek voor revisie.

   De onderwerp of kaartverbinding wordt geopend in browser.

   >[!NOTE]
   >
   > U kunt tot de verbinding van de onderwerprevisie van uw Inbox berichtengebied in de Gebruikersinterface van Adobe Experience Manager ook toegang hebben.

1. Afhankelijk van de manier waarop de onderwerprevisie in werking wordt gesteld, kon u om het even welke volgende twee schermen bekijken:

   >[!NOTE]
   >
   > De interface kan anders zijn als u de revisie hebt gemaakt in:
   >
   > - Adobe Experience Manager Guides as a Cloud Service Release 2022 of eerder
   > - Adobe Experience Manager Guides versie 4.1 of lager

   Het volgende scherm verschijnt wanneer een kaart DITA wordt gebruikt om het overzichtswerkschema in werking te stellen:

   ![](images/multiple-topics-review.png){align="left"}

   De volgende opties zijn beschikbaar op dit scherm:

   - **A**: De naam van de overzichtstaak.
   - **B**: Selecteer het pictogram van de Mening van Onderwerpen om het onderwerppaneel te tonen of te verbergen.

   - **C**: U kunt naar het vereiste onderwerp zoeken door één of ander deel van de tekst van de titel of dossierweg in de onderzoeksbar in te gaan.

     Selecteer ![](images/view-options.svg) bij de zoekbalk om alle onderwerpen of onderwerpen met opmerkingen weer te geven. Standaard kunt u alle onderwerpen in de overzichtstaak weergeven.


   - **D**: De aantallen die door ***worden benadrukt F*** kunnen worden gefiltreerd door de gewenste filteroptie van hier te kiezen. U kunt opmerkingen filteren op type, status, revisor of versie. Bijvoorbeeld, als u wilt bekijken hoeveel Strikethrough commentaren in elk van onder overzichtsonderwerp zijn gemaakt, selecteer het filterpictogram en kies dan **\>** Schrapping **van het Type van Overzicht**.

     >[!NOTE]
     >
     > Bij het toepassen van de filters worden alleen de opmerkingen die overeenkomen met de geselecteerde filters weergegeven in het venster Opmerkingen. Het aantal gefilterde opmerkingen wordt links in het deelvenster Onderwerpen weergegeven.

   - **E**: Een onderwerp dat voor overzicht aan de huidige recensent wordt toegewezen wordt getoond in zwart en kan worden geselecteerd. Wanneer de controleur een onderwerpverbinding selecteert die onderwerp aan de bovenkant van het scherm wordt gebracht.
   - **F**: Een onderwerp dat niet voor overzicht beschikbaar is wordt grijs weergegeven. Het onderwerp wordt getoond op read-only wijze en u wordt niet toegestaan om het even welke overzichtscommentaren over dergelijke onderwerpen toe te voegen.

   - **G**: Aantal commentaren die op een onderwerp worden ontvangen. Dit getal verandert op basis van het filter dat u toepast.


   Alle onderwerpen in de kaart worden getoond als één enkel samengesteld document. De onderwerpen die de controleur mag beoordelen, worden normaal weergegeven. De onderwerpen die de revisie niet mag reviseren, worden niet weergegeven.

   ![](images/review-read-only.png){align="left"}

   In het bovenstaande schermafbeelding wordt het algemene beschrijvingsonderwerp gedeeld voor revisie met de huidige revisor, die normaal wordt weergegeven. Nochtans, wordt het volgende onderwerp, Geschiedenis van vlieginhoud niet gedeeld voor overzicht en het wordt getoond op read-only wijze. Het onderwerp dat momenteel in focus is, wordt ook benadrukt in de inhoudsopgave.

   Het volgende scherm verschijnt wanneer een onderwerp of veelvoudige onderwerpen voor overzicht worden geselecteerd en worden gedeeld:

   ![](images/review-composite-view.png){align="left"}

   >[!NOTE]
   >
   > Bij meerdere onderwerpen worden deze als één samengesteld document weergegeven in de documentweergave. De bovenstaande schermafbeelding markeert twee verschillende onderwerpen die elkaar in één weergave worden gepresenteerd.

1. Open het paneel van Commentaren door het **pictogram van Commentaren** bij de hoogste juiste hoek van de toolbar te selecteren.

   Geef revisieopmerkingen door een geschikt type opmerking op de werkbalk te selecteren en druk op Enter om uw opmerking te verzenden.
Het commentaarvakje steunt multi-line ingangen en staat gebruikers toe om het uit te breiden zoals nodig voor het verstrekken van gedetailleerde terugkoppelen. U kunt **Verschuiving** gebruiken + **gaat** binnen om naar de volgende lijn te gaan terwijl het schrijven van de commentaar.

   >[!NOTE]
   >
   > In het venster Opmerkingen worden alleen de opmerkingen over de huidige onderwerpen weergegeven. Wanneer u nadruk naar ander onderwerp beweegt, worden de commentaren die op het andere onderwerp worden gegeven getoond.

1. Selecteer **dicht** knoop zodra u het herzien van het onderwerp voltooit. Bij het selecteren van de **Dichte** knoop, zult u aan de pagina worden opnieuw gericht van waar u het overzichtsonderwerp betreedde.

## Extra functies beschikbaar op het revisiescherm

**de mening van het Document en onderwerpmening** - door gebrek, als de veelvoudige onderwerpen voor overzicht worden gedeeld, dan wordt een samengestelde documentmening van onderwerpen getoond aan de recensenten. In het geval van een DITA kaartoverzicht, worden alle onderwerpen in de kaart voorgesteld in de vorm van één enkel document, gelijkend op een boekmening. Als u wilt, kunt u een bepaald onderwerp ook selecteren en slechts wordt dat onderwerp dan getoond op het overzichtsscherm.

Wanneer u één onderwerp bekijkt, krijgt u een extra optie om terug naar de documentmening te schakelen. In het volgende schermafbeelding wordt een bepaald onderwerp van een kaartbestand geopend voor revisie. De benadrukte optie — **toont de Mening van het Document** staat gebruiker toe terug naar de documentmening van het kaartdossier te schakelen.

>[!NOTE]
>
> Een schermresolutie met een breedte van meer dan 1600 px is compatibel met de standaardbreedte van het deelvenster (links en rechts). Hierdoor wordt geen horizontale schuifbalk weergegeven en blijft de inhoud op de juiste wijze uitgelijnd in de documentweergave. U kunt ook het scherm altijd vergroten of verkleinen om de juiste documentweergave te behouden in de revisieinterface.



![](images/switch-document-view.png){align="left"}

**Werkend met verschillende types van het becommentariëren hulpmiddelen** - u kunt gealigneerde commentaren toevoegen door tekst te benadrukken, door tekst te schrappen, tekst op te nemen, of een commentaarnota toe te voegen. De verschillende typen gereedschappen voor opmerkingen op de werkbalk Opmerkingen worden hieronder beschreven:

![](images/comments-toolbar.png){width="350" align="left"}

- **Hoogtepunt** \ (![](images/review-highlight-icon.svg) \): Om een hoogtepuntcommentaar toe te voegen, selecteer de tekst en kies het pictogram van het Hoogtepunt. U kunt ook eerst het pictogram Hooglicht kiezen en vervolgens de gewenste tekst selecteren.

  ![](images/highlight-comment.png){width="650" align="left"}

  Er verschijnt een pop-up in het venster Opmerkingen waarin u uw opmerking voor de gemarkeerde inhoud kunt toevoegen.

- **Doorhaling** \ (![](images/review-text-strike-through-icon.svg) \): Als u inhoudsafzetting wilt voorstellen, kunt u dit doen door de inhoud te selecteren en dan het Strikethrough pictogram te kiezen. U kunt ook eerst de gewenste tekst selecteren en vervolgens de toets Delete kiezen.

  Er verschijnt een pop-up in het venster Opmerkingen waarin u uw opmerking voor de verwijderde inhoud kunt toevoegen.

- **Tekst van het Tussenvoegsel** \ (![](images/review-insert-text-icon.svg) \): Als u tekst wilt opnemen, selecteer het pictogram van de Tekst van het Tussenvoegsel en plaats de curseur waar u de tekst en type in de informatie wilt opnemen. Of plaats de cursor op de plaats waar u tekst wilt invoegen en begin te typen. De toegevoegde informatie wordt weergegeven in een groen gekleurd lettertype.

- **voeg Commentaar** \ (![](images/review-comment-icon.svg) \) toe: Als u een kleverig notitietype van commentaar wilt toevoegen, selecteer het Add pictogram van de Commentaar en ga de commentaar in pop - op in.


**Contextafhankelijke toolbar**

U kunt tekst ook snel markeren of doorhalen met de contextuele werkbalk. Voer de volgende stappen uit om opmerkingen toe te voegen met de contextafhankelijke werkbalk:

1. Selecteer de tekst die u wilt markeren of doorhalen. De contextafhankelijke werkbalk wordt weergegeven.

   ![](images/review-quick-launch-toolbar.png){width="550" align="left"}

1. Selecteer het **Hoogtepunt** of **Strikethrough** pictogram.
1. U kunt opmerkingen toevoegen in het venster Opmerking voor de markeringsactie of doorhalingsactie.

**Overzicht gebruikend het paneel van Commentaren** - het paneel van Commentaren toont een lijst van commentaren die op het huidige onderwerp worden gegeven. Dit deelvenster bevat ook opmerkingen van andere revisoren als het onderwerp naar meerdere revisoren is verzonden. Elke opmerking in het opmerkingenvenster is gekoppeld aan de corresponderende tekst in het huidige onderwerp. Hiermee kunt u de tekst met opmerkingen herkennen. Elke opmerking bevat de naam van de controleur die de opmerking samen met de tijdstempel heeft toegevoegd.

De opmerkingen worden weergegeven in de volgorde van de tekst met opmerkingen in het document. Er is bijvoorbeeld een gemarkeerde opmerking bij de eerste zin en een invoegtekstcommentaar bij de tweede zin in de eerste alinea en de gemarkeerde tekstopmerking wordt vóór de ingevoegde tekstopmerking weergegeven.

De taken die u kunt uitvoeren via het venster Opmerkingen worden hieronder beschreven:

- Als u een opmerking selecteert, wordt de desbetreffende opmerking gemarkeerd en wordt de locatie van de opmerking in het document weergegeven.
- U kunt reacties toevoegen aan opmerkingen.
- U kunt uw eigen commentaar uitgeven door uw gecommentarieerde tekst in het paneel van Commentaren te selecteren en dan **te kiezen geeft** van het menu van Opties uit.
- U kunt uw eigen commentaren schrappen door de commentaar in het paneel van Commentaren te selecteren en dan de **schrapping** optie van het menu van Opties te kiezen.

  ![](images/review-comment-options-menu.png){width="300" align="left"}

  >[!NOTE]
  >
  > Het menu Opties wordt alleen weergegeven wanneer u de muisaanwijzer op uw eigen opmerkingen plaatst. Deze wordt niet weergegeven voor de opmerkingen van andere revisoren.

- Alle deelnemende gebruikers kunnen reageren op opmerkingen die door andere gebruikers zijn ingediend. Voor een commentaar, uitgezochte **Antwoord** en druk binnengaan om een reactie voor te leggen. Het antwoordvak is meerdere regels en kan worden uitgebreid, zodat gebruikers gedetailleerde antwoorden op opmerkingen kunnen geven. U kunt **Verschuiving** gebruiken + **gaat** binnen om naar de volgende lijn te gaan terwijl het schrijven van het antwoord.

**wijze van de Voorproef**

- Als u een onderwerp opent in de modus Voorvertoning, ziet u hoe een onderwerp wordt weergegeven wanneer een onderwerp wordt bekeken door een auteur nadat alle wijzigingen zijn toegepast. Alle ingevoegde tekst wordt bijvoorbeeld als normale tekst weergegeven en alle verwijderde \(verwijderde\) tekst wordt uit de inhoud verwijderd.

- De volgende het schermschot toont de inhoud op *1} wijze van het Overzicht {:*

![](images/review-author-mode.png){width="550" align="left"}

De volgende het schermschot toont de inhoud op *1} wijze van de Voorproef {:*

![](images/review-preview-mode.png){width="550" align="left"}


**de taakgebruikers van de Markering in een commentaar**

Wanneer u met meerdere revisoren samenwerkt aan een revisietaak, kunt u de communicatie verbeteren door specifieke gebruikers in zowel nieuwe opmerkingen als antwoorden te coderen. Als controleur kunt u een opmerking initiëren of reageren op een bestaande opmerking terwijl u andere gebruikers die bij dezelfde revisietaak zijn betrokken, van tags voorziet om hun aandacht te vestigen of follow-ups toe te wijzen. Deze functionaliteit is alleen beschikbaar voor actieve revisietaken.

>[!NOTE]
>
> Om de lijst van gebruikers te bekijken die aan een overzichtstaak worden toegewezen en hen in een commentaar etiketteren, moet u *Gelezen toegang* op `/home/users and /home/groups` knopen hebben. Voor details, mening [ gebruikersbeleid en veiligheid ](../cs-install-guide/user-admin-sec.md#additional-notes-on-user-groups). <br> Als er na het bevestigen van de toegang nog steeds geen codes beschikbaar zijn, moet uw beheerder mogelijk een `user-admin` -licentie toewijzen om deze functionaliteit in te schakelen.

![](images/tag-users-review-ui.png){width="350" align="left"}

Gecodeerde gebruikers ontvangen zowel een e-mail als een AEM-melding, zodat ze deze snel kunnen informeren. Voor meer details op hoe de heroverwegingsberichten teweegbrengen, mening [ het Begrip van heroverwegingsberichten ](./review-understanding-review-notifications.md).

![](images/mentioned-in-tags-author.png){width="350" align="left"}

**voegt gehechtheid aan commentaren** toe -   Als u uw opmerking wilt aanvullen met aanvullende informatie die beschikbaar is in een ander bestand, kunt u dit doen door de opmerking bij de opmerking te voegen. Als revisor kunt u eenvoudig een of meerdere bestanden van uw lokale systeem aan uw opmerking toevoegen. U kunt een bestand toevoegen aan alle ondersteunde formulieren met opmerkingen: Markeren, Doorhalen, Tekst invoegen of Opmerking.

Als u een van de opmerkingen invoegt, wordt het pop-upvenster met opmerkingen weergegeven. Nadat u in het pop-upvenster aanvullende opmerkingen of informatie hebt opgegeven, kunt u deze verzenden door op Enter te drukken. Nadat de opmerking is toegevoegd, kunt u een bijlage aan die opmerking toevoegen.

![](images/comment-pop-up-panel.png){align="left"}

In de bovenstaande schermafbeelding bevat het document de pop-up van de gemarkeerde opmerking en wordt de opmerking ook toegevoegd in het venster Opmerkingen. Het pictogram van de dossiergehechtheid ![](images/file-attach-review.svg) is beschikbaar samen met de commentaar bij beide plaatsen.

Voer de volgende stappen uit om bijlage aan uw commentaar toe te voegen:

1. Selecteer *toevoegen Bijlage* pictogram ![](images/file-attach-review.svg) op de commentaar waarmee u een gehechtheid wilt toevoegen.

   Het dialoogvenster Bestand openen wordt geopend.

1. Selecteer een of meerdere bestanden die u wilt bijvoegen.

   De geselecteerde bestanden worden samen met de opmerking weergegeven in het venster Opmerkingen.

   In het venster Opmerkingen kunt u de bestandsnaam en de grootte bekijken. U kunt een bestand ook verwijderen door het verwijderpictogram ![](images/Delete_icon.svg) te selecteren dat aan de bestandsnaam is gekoppeld.

1. Selecteer **voorleggen**.

   De bijlagen worden geüpload en aan de opmerking toegevoegd.


**Extra nota&#39;s bij het werken met gehechtheid:**

- Standaard worden slechts twee bestanden weergegeven die zijn gekoppeld aan een opmerking. Als er meer dossiers zijn, dan **toont de knoop van de Bijlage van de Mening** op het recht het aantal alle gehechtheid \ (die meer dan twee zijn \) verbonden aan de commentaar. U kunt het nummer selecteren om alle bijlagen weer te geven. Als u bijvoorbeeld vier bijlagen met een opmerking hebt, ziet u +2 op de knop.

![](images/review-view-attachment.png){width="550" align="left"}

- Als u de muisaanwijzer op een bijlage plaatst, kunt u de bijlage downloaden of verwijderen. Het verwijderen van de bijlage is alleen beschikbaar als de huidige revisor die opmerking heeft toegevoegd, zoals in de volgende schermafbeelding wordt getoond:

![](images/current-user-comment-options.png){width="550" align="left"}

De andere revisoren of auteurs krijgen alleen de optie voor downloadbijlagen.

![](images/other-reviewer-download.png){width="550" align="left"}

- U kunt alle gehechtheid downloaden verbonden aan een commentaar van de **dialoog van de Gehechtheid van de Mening**. Selecteer de gehechtheid en selecteer het **pictogram van de Download** op het commentaarniveau.

- U kunt de gehechtheid ook schrappen verbonden aan een commentaar van de **dialoog van de Gehechtheid van de Mening**. Selecteer de gehechtheid en selecteer het **pictogram van de Schrapping**.

![](images/attach-files-comments-panel.png){width="550" align="left"}


**Voorwaarden paneel** -   Als uw onderwerp voorwaardelijke inhoud heeft, dan zult u de **Voorwaarden** \ (![](images/conditions-icon.svg) \) pictogram op het recht bekijken. Het selecteren van **Voorwaarden** pictogram opent het paneel van Voorwaarden dat u toestaat om de inhoud volgens de beschikbare voorwaarden in het onderwerp te benadrukken.

:   Door gebrek **wordt het Hoogtepunt Alle Voorwaarden** optie toegelaten, worden alle voorwaarden geselecteerd, wordt de volledige inhoud getoond, en de geconditionaliseerde inhoud wordt getoond zoals benadrukt zowel op overzicht als voorproefwijze.

:   U kunt **Markeren Alle Voorwaarden** optie onbruikbaar maken en alle inhoud bekijken huidig in het onderwerp als normale tekst zonder enige hoogtepunten.

![](images/review-conditions-panel.png){width="350" align="left"}

U kunt een bepaalde voorwaarde verbergen of weergeven.

- Als u een voorwaarde verbergt, wordt de inhoud met die voorwaarde niet gemarkeerd in de revisiemodus.
- Als u een voorwaardelijk geconditioneerde inhoud weergeeft, wordt deze gemarkeerd in de revisiemodus. In de volgende schermafbeelding gebruikt bijvoorbeeld alleen de inhoud twee voorwaarden: `win` en `mac` wordt gemarkeerd.


![](images/review-condition-normal-mode.png){width="650" align="left"}

In de voorvertoningsmodus worden de niet-geconditioneerde inhoud en de geconditioneerde inhoud weergegeven die de twee weergegeven voorwaarden `win` en `mac` gebruikt. De resterende geconditioneerde inhoud waarvoor de voorwaarden verborgen zijn, wordt niet weergegeven.

**overzicht in real time** -   Het venster Opmerkingen wordt in real-time bijgewerkt met opmerkingen en de feedback of actie die de auteur op de opmerkingen heeft uitgevoerd.

- Meerdere revisoren kunnen opmerkingen op hetzelfde document achterlaten of op opmerkingen tegelijk reageren. U kunt erachter komen wie momenteel het document controleert door de muis boven het gebruikerspictogram in de rechterbovenhoek van het scherm te plaatsen.

- Als een onderwerp een deel van veelvoudige overzichtstaken is, dan worden de commentaren die in één taak worden gemaakt niet getoond in de andere taak.

- Als u het pictogram Verouderde opmerking selecteert \(![](images/outdated-comment-icon.svg)\), worden de verschillen weergegeven tussen de meest recente en de versie met opmerkingen van het document. De versienummers \(van de versies die worden vergeleken\) worden boven aan de documenten weergegeven.

  ![](images/comments-page-review-mode.png){align="left"}

  >[!NOTE]
  >
  > Wanneer u de muisaanwijzer op het pictogram Verouderde opmerking plaatst, wordt het versienummer weergegeven van het onderwerp waarop de opmerking is toegevoegd. Als bijvoorbeeld een opmerking is gegeven op versie 1.0, wordt hetzelfde weergegeven.

- Als u een verouderde opmerking selecteert, wordt de versie van die opmerking in het linkervenster geopend. De vorige versie wordt weergegeven in het linkerdeelvenster en de huidige versie wordt weergegeven in het rechterdeelvenster. Alle opmerkingen over de verouderde versie worden links geïmporteerd. U kunt de vorige versie vergelijken met de huidige versie.

**commentaren van de Filter** -   U kunt opmerkingen in een document filteren om de gewenste specifieke opmerkingen weer te geven. Om commentaren te filtreren, selecteer het **pictogram van de Filter** \ (![](images/filter-search-icon.svg) \) dat in het menu op het recht van het de tekstvakje van Commentaren van het Onderzoek in het paneel van Commentaren verschijnt.

Selecteer één of meerdere van de volgende het filtreren opties van het **Type van Filter** dialoog en selecteer **van toepassing zijn**.

- **Type van Overzicht** - filter op basis van het commentaartype - Hoogtepunt, Schrapping, Invoeging, of Commentaar.
- **Status van het Overzicht** - filter op de basis van de status van de commentaar zoals Toegelaten, Afgewezen, of niets.
- **Recensenten** - filter op basis van de naam van de recensent.

- **Versies** - filter op basis van de commentaren die op een bepaalde versie van het onderwerp worden ontvangen.

  Als u de filters gebruikt, worden de opmerkingen in het rechtervenster gefilterd op basis van de selectie en wordt het aantal opmerkingen in het linkervenster dienovereenkomstig bijgewerkt.


Om de filter te verwijderen en alle commentaren te bekijken, schrap alle filters van het **Type van Filter** dialoog en selecteer **toepassen**.

**Bovenliggend onderwerp:**[ Inleiding aan overzicht ](review.md)
