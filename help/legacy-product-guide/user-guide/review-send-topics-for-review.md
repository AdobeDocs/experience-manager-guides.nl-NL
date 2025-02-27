---
title: Onderwerpen ter controle verzenden
description: Leer hoe u een overzichtstaak maakt en onderwerpen ter controle verzendt in AEM Guides. Verzend één of meerdere onderwerpen in een kaart DITA voor overzicht.
feature: Reviewing
role: User
hide: true
exl-id: 4e47536a-ad78-4c97-9cea-a6af854f6e2f
source-git-commit: ea597cd14469f21e197c700542b9be7c373aef14
workflow-type: tm+mt
source-wordcount: '2752'
ht-degree: 0%

---

# Onderwerpen ter controle verzenden {#id199RD0S035Z}

De revisiewerkstroom maakt een omgeving met meerdere revisoren waarin de aanvrager een lijst met onderwerpen opgeeft voor revisie, meerdere revisoren toevoegt en een tijdlijn toewijst aan de revisietaak. Met AEM Guides kunnen gebruikers die tot de groepen Auteurs en Publishers behoren, een revisie starten.

Aangezien het revisiewerkschema project-specifiek is, moet de initiatiefnemer van overzicht een deel van het projectteam zijn of rechten hebben om een project tot stand te brengen. Op het tijdstip van het creëren van een project, bepaalt u de teamleden voor het project en wijst hen diverse rollen of groepen toe. Voor meer informatie over projecten, zie [ tot een project DITA ](authoring-create-dita-project.md#) leiden.

U kunt een revisietaak maken op basis van:

- **Redacteur van het Web**: Staat u toe om een individueel onderwerp of kaart DITA voor overzicht te verzenden. Merk op dat het werkschema voor het creëren van een overzichtstaak over de Redacteur van het Web en UI van Assets gemeenschappelijk is. Alleen de methode voor het starten van de revisiewerkstroom verschilt. Voor informatie over het lanceren van het overzichtswerkschema van de Redacteur van het Web, zie [ de Taak van het Overzicht ](web-editor-features.md#id215OCJ00JXA) eigenschap in de Redacteur van het Web creëren.

- **Assets UI**: Staat u toe om één of veelvoudige onderwerpen en kaart DITA voor overzicht te verzenden. Het delen van documenten voor overzicht van de gebruikersinterface van Assets wordt behandeld onder dit onderwerp.


In de gebruikersinterface van Assets kunt u op twee manieren een revisietaak maken:

- Een of meer onderwerpen ter controle verzenden
- Meerdere onderwerpen vanuit een DITA-kaart verzenden voor revisie

## Een of meer onderwerpen ter controle verzenden {#id1721E600FY4}

>[!IMPORTANT]
>
> Voordat u een revisietaak maakt, moet u controleren of u een project hebt gemaakt en revisoren aan dat project hebt toegevoegd.

Voer de volgende stappen uit om een overzichtstaak te maken en onderwerpen ter controle te verzenden:

>[!NOTE]
>
> U kunt een overzichtstaak slechts tot stand brengen als u een auteur of uitgever in een DITA- project bent.

1. Navigeer naar de vereiste map in de gebruikersinterface van Assets.

1. Klik op het pictogram Selecteren in de snelle actie en selecteer de onderwerpen die u wilt verzenden voor revisie.

   ![](images/select-asset-62.png){width="300" align="left"}

1. In de toolbar, klik **creëren de Taak van het Overzicht**. De pagina voor het maken van revisietaken wordt weergegeven.

   >[!NOTE]
   >
   > U kunt een overzichtstaak voor slechts die onderwerpen tot stand brengen die een revisie hebben. Als het geselecteerde onderwerp geen revisie heeft, zult u een herinnering worden getoond.

   ![](images/create-review-task-023.png){width="650" align="left"}

1. Ga a **Titel** voor de taak in en selecteer een DITA **Project** van de drop-down lijst.

1. Op **wijs** drop-down gebied toe, selecteer de recensenten aan wie u de onderwerpen voor overzicht wilt verzenden.

   U kunt een overzichtstaak aan individuele gebruikers van het project of aan gebruikersgroepen toewijzen. Merk op dat u een overzichtstaak aan individuele gebruikers kunt toewijzen slechts wanneer u een deel van de de beheerdergroep van het project bent, anders zult u slechts de gebruikersgroepen in Toewijzen aan gebied zien.

   >[!NOTE]
   >
   > De revisiewerkstroom is projectspecifiek. Wanneer u projecten creeert, voegt u de teamleden aan het project toe en wijst hen aan groepen toe. Dus als je het project hier selecteert, kies je de leden die deel uitmaken van dat project. Voor meer informatie over projecten, zie [ tot een project DITA ](authoring-create-dita-project.md#) leiden.

1. Ga a **Beschrijving** voor de taak in.

   Deze beschrijving wordt gebruikt als de hoofdtekst van de e-mailmelding die aan de controleurs wordt verzonden.

1. Selecteer de **Verschuldigde Datum** en de tijd om de deadline voor de overzicht te merken.

   >[!NOTE]
   >
   > Na het bereiken van de deadline wordt een e-mail verzonden naar de aanvrager met de kennisgeving dat de revisietaak is voltooid. De initiatiefnemer kan de deadline van de overzichtstaak van het [ Dashboard van het Overzicht ](review-manage-tasks-review-dashboard.md#) uitbreiden.

1. Selecteer de wortelkaart van de **weg Rootmap**. Deze routekaart wordt gebruikt om alle belangrijkste verwijzingen en verklarende woordenlijsttermijnen op te lossen die in de overzichtsinhoud worden gebruikt. Als u niet rootmap selecteert dan worden de belangrijkste verwijzingen of verklarende woordenlijsttermijnen verbonden aan het onderwerp DITA, niet opgelost alvorens het onderwerp voor overzicht te verzenden.

   Als u de overzicht voor een kaart DITA creeert, dan door gebrek **weg Rootmap** wordt geplaatst aan de weg van die kaart. Als u de overzicht voor één of veelvoudige onderwerpen creeert, dan door gebrek wordt de **weg Rootmap** geplaatst aan de kaart die in de Voorkeur van de Gebruiker wordt bepaald.

   >[!NOTE]
   >
   > De geselecteerde hoofdmap heeft de hoogste prioriteit om toetsverwijzingen op te lossen. Voor meer details, zie [ zeer belangrijke verwijzingen ](map-editor-other-features.md#id176GD01H05Z) oplossen.

1. Aangezien u verschillende recensenten aan verschillende onderwerpen kunt toewijzen, **Toestaan Assignees om het even welk Onderwerp** optiecontroles te herzien of de recensenten alle onderwerpen in een overzichtstaak of slechts die onderwerpen kunnen herzien die zij aan overzicht worden toegewezen.

   Als u alle recensenten wilt toestaan om het even welk onderwerp in de overzichtstaak te herzien, selecteer **Toestaan Toewijzingen om het even welk Onderwerp** te herzien.

   Als u deze optie niet selecteert dan zullen de recensenten die op **worden toegevoegd toewijzen aan** gebied toegang hebben om slechts die onderwerpen te herzien die aan hen worden toegewezen.

1. Klik op **Next**.

   De pagina Inhoud wordt weergegeven.

   ![](images/content_page_review.png){width="800" align="left"}

1. Selecteer op de pagina Inhoud een versie van het onderwerp dat u wilt delen voor revisie.

   U kunt een van de volgende methoden gebruiken om een versie te selecteren:

   - *\ (Gebrek \)* verkies de optie **Hun Laatste Versie** om de laatste bewaarde revisie van de onderwerpen te selecteren.
   - Kies de **Versie op** optie en specificeer de datum en de tijd om een versie zoals op de gespecificeerde datum en de tijd te selecteren. Als er geen versie van onderwerp beschikbaar op de gespecificeerde datum is, dan een versie beschikbaar onmiddellijk na de gespecificeerde datum en de tijd wordt geselecteerd.
   - Kies **Uitgezocht een optie van het Etiket** en selecteer een etiket van de drop-down lijst.
1. Na het maken van uw selectie voor het kiezen van een versie, klik **toepassen**.

   De versie die op de geselecteerde optie wordt gebaseerd wordt gekozen voor de onderwerpen.

   >[!NOTE]
   >
   > U kunt de gewenste versie van de **drop-down lijst van de Versie** van elk onderwerp ook manueel selecteren.

1. Klik op **Next**.

   De pagina Revisors wordt weergegeven op de plaatsen waar u revisoren kunt toevoegen of verwijderen. Standaard worden de controleurs die in het veld Toewijzen aan zijn toegevoegd, automatisch toegevoegd aan elk onderwerp dat voor de revisie is geselecteerd.

   ![](images/add-reviewers-topics.png){width="650" align="left"}

1. Op de pagina Revisors kunt u revisoren toevoegen of verwijderen. De volgende bewerkingen zijn beschikbaar op de pagina Revisors:

   - **Uitgezocht allen**: Selecteert alle onderwerpen in de onderwerpenlijst. U kunt een partijverrichting gemakkelijk uitvoeren na het selecteren van alle onderwerpen.
   - **Duidelijke Selectie**: Deselecteert de onderwerpen die in de onderwerpenlijst worden geselecteerd.

     >[!NOTE]
     >
     > U kunt een onderwerp ook individueel selecteren of schrappen door op checkbox naast het onderwerp te klikken.

   - **voeg toe**: Toont de Add dialoog van Recensenten. U kunt de naam typen van een revisor of gebruikersrol \(of groep\) die u als controleur wilt toevoegen aan de geselecteerde onderwerpen.
   - **verwijder**: Toont de Remove dialoog van Recensenten. U kunt de naam typen van een revisor of gebruikersrol \(of groep\) die u als controleur wilt verwijderen uit de geselecteerde onderwerpen.

     >[!NOTE]
     >
     > U kunt een revisie ook verwijderen uit een onderwerp door op het kruisje te klikken in het vak van de revisor.

   - **opnieuw toewijzen**: Toont het Opnieuw toewijzen van de dialoog van Revisoren. U kunt de naam typen van een revisor of gebruikersrol \(of groep\) waaraan u de revisietaak wilt toewijzen. Hiermee verwijdert u alle bestaande revisoren uit de geselecteerde onderwerpen en wijst u de nieuw geselecteerde revisoren toe aan deze onderwerpen.
   - **Uitvoer**: Staat u toe om de details van de overzichtstaak in een Csv- dossier uit te voeren. Het bestand bevat details zoals het pad en de titel van het onderwerp, de naam van de controleur en de versie van de onderwerpen die ter controle zijn verzonden.
   - **geeft Recensenten** uit: Het klikken van het ![](images/edit_pencil_icon.svg) pictogram in de onderwerpenlijst toont de Edit dialoog van Reviewers. U kunt revisoren voor het geselecteerde onderwerp toevoegen aan of verwijderen uit dit dialoogvenster.
1. Klik **creëren** om de overzichtstaak tot stand te brengen.

   Er wordt een bevestigingsbericht weergegeven wanneer de revisietaak met succes is gemaakt. De [ staat van het Document ](web-editor-document-states.md#) voor de onderwerpen die voor overzicht worden verzonden wordt geplaatst aan In-Overzicht.

   >[!NOTE]
   >
   > U kunt ook op Meldingen beluisteren rechtsboven in het scherm klikken en bevestigen dat de revisietaak is voltooid. In het deelvenster Meldingen vindt u elk één melding voor de revisoren die deel uitmaakten van de revisietaak en één melding voor de aanvrager van de revisie.


Een e-mail wordt verzonden naar alle revisoren, op de hoogte gesteld van het feit dat aan hen een of meerdere onderwerpen ter controle zijn toegewezen. Het e-mailbericht bevat een directe koppeling waarop de gebruikers kunnen klikken en het onderwerp kunnen openen in een browservenster.

Als er meerdere onderwerpen zijn toegewezen, kunnen de revisoren deze weergeven en selecteren in een vervolgkeuzelijst met onderwerpen in de webbrowser.

## Meerdere onderwerpen ter controle verzenden vanuit een DITA-kaart

Een kaart DITA is een logische organisatie van onderwerpen binnen een boek. Wanneer u een individueel onderwerp voor overzicht verzendt, krijgt de recensent geen informatie over de plaats van dat onderwerp in het boek. Als een controleur informatie over de nauwkeurige plaats van het onderwerp heeft dat wordt herzien, krijgt de recensent een betere context van het onderwerp dat wordt herzien.

AEM Guides staat u toe om één of meerdere onderwerpen in een kaart DITA voor overzicht tezelfdertijd te verzenden. De controleur krijgt om het volledige kaartdossier samen met onderwerpen te zien die voor overzicht zijn gedeeld. Dit maakt het voor de recensent gemakkelijker om een context van het onderwerp in het kaart of boekdossier te krijgen.

U kunt dezelfde DITA-kaart delen voor revisie in meerdere revisietaken. Bijvoorbeeld, als in een kaart DITA onderwerp A, B, C, D en E zijn. In één overzichtstaak kunt u A, B, en C voor overzicht en in een andere overzichtstaak delen u onderwerpen C, D en E voor overzicht verzenden. Het revisieproces staat voor het delen van het zelfde onderwerp en kaartdossier in veelvoudige overzichtstaken toe. Voor het gemeenschappelijke onderwerp in veelvoudige overzichtstaken, beschrijven de commentaren die in één overzichtstaak worden gegeven of voegen met de commentaren in de andere overzichtstaken niet samen.

>[!IMPORTANT]
>
> Als een onderwerp van een kaartdossier in veelvoudige overzichtstaken is gedeeld, zou hun status in-Overzicht tonen tot alle overzichtstaken zijn voltooid.

Als u een of meerdere onderwerpen samen met het kaartbestand ter controle wilt verzenden, voert u de volgende stappen uit:

>[!IMPORTANT]
>
> Zodra u een overzicht door een kaartdossier in werking stelt, moet u niet de structuur van het kaartdossier veranderen door nieuwe onderwerpen toe te voegen of bestaande onderwerpen te verwijderen.

1. Navigeer naar de vereiste map in de gebruikersinterface van Assets.

   >[!NOTE]
   >
   > Zorg ervoor dat de weergave van de console is ingesteld op de kaartweergave of lijstweergave.

1. Selecteer de kaart van waar u de onderwerpen voor overzicht wilt verzenden.

1. In de toolbar, klik **creëren de Taak van het Overzicht**. De pagina voor het maken van revisietaken wordt weergegeven.

1. Ga a **Titel** voor de taak in en selecteer een DITA **Project** van de drop-down lijst.

   >[!NOTE]
   >
   > U kunt een overzichtstaak voor slechts die onderwerpen tot stand brengen die een revisie hebben. Als uw kaart onderwerpen bevat die geen revisie hebben, dan wordt u getoond een herinnering met een lijst van dergelijke dossiers. Bestanden zonder revisie worden uitgesloten van de revisietaak.

1. Op **wijs** drop-down gebied toe, selecteer de recensenten aan wie u de onderwerpen voor overzicht wilt verzenden.

   U kunt een overzichtstaak aan individuele gebruikers van het project of aan gebruikersgroepen toewijzen. Merk op dat u een overzichtstaak aan individuele gebruikers kunt toewijzen slechts wanneer u een deel van de de beheerdergroep van het project bent, anders zult u slechts de gebruikersgroepen in Toewijzen aan gebied zien.

   >[!NOTE]
   >
   > De revisiewerkstroom is projectspecifiek. Wanneer u projecten creeert, voegt u de teamleden aan het project toe en wijst hen aan groepen toe. Dus als je het project hier selecteert, kies je de leden die deel uitmaken van dat project. Voor meer informatie over projecten, zie [ tot een project DITA ](authoring-create-dita-project.md#) leiden.

1. Ga a **Beschrijving** voor de taak in.

   Deze beschrijving wordt gebruikt als de hoofdtekst van de e-mailmelding die aan de controleurs wordt verzonden.

1. Selecteer de **Verschuldigde Datum** en de tijd om de deadline voor de overzicht te merken.

   >[!NOTE]
   >
   > Na het bereiken van de deadline wordt een e-mail verzonden naar de aanvrager met de kennisgeving dat de revisietaak is voltooid. De initiatiefnemer kan de deadline van de overzichtstaak van het [ Dashboard van het Overzicht ](review-manage-tasks-review-dashboard.md#) uitbreiden.

1. Aangezien u verschillende recensenten aan verschillende onderwerpen kunt toewijzen, **Toestaan Assignees om het even welk Onderwerp** optiecontroles te herzien of de recensenten alle onderwerpen in een overzichtstaak of slechts die onderwerpen kunnen herzien die zij aan overzicht worden toegewezen.

   Als u alle recensenten wilt toestaan om het even welk onderwerp in de overzichtstaak te herzien, selecteer **Toestaan Toewijzingen om het even welk Onderwerp** te herzien.

   Als u deze optie niet selecteert dan zullen de recensenten die op **worden toegevoegd toewijzen aan** gebied toegang hebben om slechts die onderwerpen te herzien die aan hen worden toegewezen.

1. Klik op **Next**.

   De pagina Inhoud wordt weergegeven met alle onderwerpen waarnaar in het kaartbestand wordt verwezen. Als uw kaart DITA genestelde kaarten bevat, dan zijn de onderwerpen van de genestelde kaarten ook hier vermeld.

   ![](images/content-page-map-review.png){width="800" align="left"}

1. Selecteer op de pagina Inhoud een versie van het onderwerp dat u wilt delen voor revisie.

   U kunt een van de volgende methoden gebruiken om een versie te selecteren:

   - *\ (Gebrek \)* verkies de optie **Hun Laatste Versie** om de laatste bewaarde revisie van de onderwerpen te selecteren.
   - Kies de **Versie op** optie en specificeer de datum en de tijd om een versie zoals per de datum en de tijd te selecteren. Als er geen versie van onderwerp beschikbaar op de gespecificeerde datum is, dan een versie beschikbaar onmiddellijk na de gespecificeerde datum en de tijd wordt geselecteerd.
   - Kies **Uitgezocht een optie van het Etiket** en selecteer een etiket van de drop-down lijst. Alle onderwerpen die het geselecteerde etiket bevatten worden geselecteerd in de **drop-down lijst van de Versie**.
   - Kies **Uitgezocht een optie van de Basislijn** en selecteer een basislijn van de drop-down lijst. Alle onderwerpversies die een deel van de geselecteerde basislijn zijn worden geselecteerd in de **drop-down lijst van de Versie**.
1. Na het maken van uw selectie voor het kiezen van een versie, klik **toepassen**.

   De versie die op de geselecteerde optie wordt gebaseerd wordt gekozen voor de onderwerpen.

   >[!NOTE]
   >
   > U kunt de gewenste versie van de **drop-down lijst van de Versie** van elk onderwerp ook manueel selecteren.

1. Klik op **Next**.

   De pagina Revisors wordt weergegeven op de plaatsen waar u revisoren kunt toevoegen of verwijderen. Standaard worden de controleurs die in het veld Toewijzen aan zijn toegevoegd, automatisch toegevoegd aan elk onderwerp dat voor de revisie is geselecteerd.

1. Op de pagina Revisors kunt u revisoren toevoegen of verwijderen. De volgende bewerkingen zijn beschikbaar op de pagina Revisors:

   - **Uitgezocht allen**: Selecteert alle onderwerpen in de onderwerpenlijst. U kunt een partijverrichting gemakkelijk uitvoeren na het selecteren van alle onderwerpen.
   - **Duidelijke Selectie**: Deselecteert de onderwerpen die in de onderwerpenlijst worden geselecteerd.

     >[!NOTE]
     >
     > U kunt een onderwerp ook individueel selecteren of schrappen door op checkbox naast het onderwerp te klikken.

   - **voeg toe**: Toont de Add dialoog van Recensenten. U kunt de naam typen van een revisor of gebruikersrol \(of groep\) die u als controleur wilt toevoegen aan de geselecteerde onderwerpen.
   - **verwijder**: Toont de Remove dialoog van Recensenten. U kunt de naam typen van een revisor of gebruikersrol \(of groep\) die u als controleur wilt verwijderen uit de geselecteerde onderwerpen.
   - **opnieuw toewijzen**: Toont het Opnieuw toewijzen van de dialoog van Revisoren. U kunt de naam typen van een revisor of gebruikersrol \(of groep\) waaraan u de revisietaak wilt toewijzen. Hiermee verwijdert u alle bestaande revisoren uit de geselecteerde onderwerpen en wijst u de nieuw geselecteerde revisoren toe aan deze onderwerpen.
   - **Uitvoer**: Staat u toe om de details van de overzichtstaak in een Csv- dossier uit te voeren. Het bestand bevat details zoals het pad en de titel van het onderwerp, de naam van de controleur en de versie van de onderwerpen die ter controle zijn verzonden.
   - **geeft Recensenten** uit: Het klikken van het ![](images/edit_pencil_icon.svg) pictogram in de onderwerpenlijst toont de Edit dialoog van Reviewers. U kunt revisoren voor het geselecteerde onderwerp toevoegen aan of verwijderen uit dit dialoogvenster.
   >[!IMPORTANT]
   >
   > U moet ten minste één controleur toewijzen om de revisietaak te maken.

1. Klik **creëren** om de overzichtstaak tot stand te brengen.

   Er wordt een bevestigingsbericht weergegeven wanneer de revisietaak met succes is gemaakt. De [ staat van het Document ](web-editor-document-states.md#) voor de onderwerpen die voor overzicht worden verzonden wordt geplaatst aan In-Overzicht.

   >[!NOTE]
   >
   > U kunt ook op het deelvenster Meldingen rechtsboven in de interface klikken en bevestigen dat de taak is gemaakt. In het deelvenster Meldingen vindt u elk één melding voor de revisies die deel uitmaakten van de revisietaak en één melding voor de aanvrager van de revisie.

   >[!IMPORTANT]
   >
   > Zodra u een overzicht in werking hebt gesteld, moet u niet de kaart of de onderwerpen DITA aan een verschillende plaats bewegen of schrappen. Dit leidt tot een onderbreking van het beoordelingsproces.


Er wordt een e-mail verzonden naar alle revisoren, met de kennisgeving dat aan hen onderwerpen zijn toegewezen voor revisie. Het e-mailbericht bevat een directe koppeling waarop de gebruikers kunnen klikken en het onderwerp kunnen openen in een browservenster. De onderwerpen samen met de kaart DITA worden geopend op de overzichtswijze.

**Bovenliggend onderwerp:**[ onderwerpen of kaarten van het Overzicht ](review.md)
