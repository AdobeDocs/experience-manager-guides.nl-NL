---
title: DITA kaartrapport van de Redacteur van het Web
description: Genereer DITA-kaartrapporten vanuit de webeditor in AEM hulplijnen. Leer hoe te om CSV voor een onderwerpenlijst, multimedia, meta-gegevens, en gebroken verbindingsrapporten te produceren.
exl-id: 2f202b41-85d9-4a5a-aa28-e25715ce5e2e
feature: Report Generation
role: User
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '2366'
ht-degree: 0%

---

# DITA kaartrapport van de Redacteur van het Web {#id231HF0Z0NXA}

AEM de Gidsen komen met een eigenschap in de Redacteur van het Web die u toelaat om de algemene integriteit van uw verwijzingen te controleren en rapporten voor hen te produceren.

U kunt de onderwerpenlijst bekijken, de meta-gegevens van alle verwijzingen beheren, en de lijst van verschillende media voor de huidige kaart van **Rapporten** in de webeditor.

## Een CSV genereren vanuit de onderwerpenlijstweergave

De **Lijst met onderwerpen** de mening verstrekt gedetailleerde informatie over uw onderwerpen, zoals het verwijzingstype, documentstaat, en auteur.

U kunt een rapport van de onderwerpen tot stand brengen door de volgende stappen uit te voeren:

1. In de **Bewaarplaats** opent u het DITA-kaartbestand in de Kaartweergave.
1. Klik op de knop **Beheren** tab.
1. Dubbelklikken **Lijst met onderwerpen** links. De lijst van onderwerpen aanwezig in de kaart DITA wordt getoond.

   ![](images/web-editor-topiclist-panel.png){width="800" align="left"}

1. Van de **Filters** Het paneel u kunt uw onderwerpen filtreren die op **Referentietype** \(direct of indirect\), **Documentstatus** \(de huidige status van uw onderwerpen. Als uw onderwerpen bijvoorbeeld de status Bewerken, In revisie of Reviewed hebben, worden deze weergegeven\) of de status **Auteur** van het onderwerp.

1. U kunt ook de volgende opties voor het filteren van onderwerpen gebruiken om de volgende kolommen in de lijst weer te geven:

   - **Onderwerp** De titel van het onderwerp wordt gespecificeerd in de kaart DITA. U kunt op het onderwerp klikken om het te bewerken.
   - **Bestandsnaam** Naam van het bestand.
   - **UUID** De universeel unieke id \(UUID\) van het bestand.
   - **Bestandslocatie** De volledige weg van het onderwerp.
   - **Referentietype** Het type verwijzing - direct of indirect.
   - **Documentstatus** De huidige status van het onderwerp.
   - **Auteur** De gebruiker die het laatst aan het onderwerp werkte.
   - **Bovenliggende kaart** De lijst van alle kaarten waar het onderwerp direct van verwijzingen wordt voorzien.
   >[!NOTE]
   >
   > Klikken **Vernieuwen** om een nieuwe lijst van onderwerpen te krijgen en om het even welke verandering in uw kaartdossier te bekijken of als om het even welke verwijzing binnen uw onderwerpdossier wordt bijgewerkt.

1. Klikken **CSV downloaden** om de huidige momentopname van de onderwerpen in de kaart te downloaden DITA. CSV bevat de geselecteerde kolommen en de onderwerpen gefilterd in **Lijst met onderwerpen** weergeven. U kunt dit dossier van onderwerpenlijst CSV in om het even welke redacteur dan openen CSV.

**Metagegevens bulksgewijs beheren vanuit het metagegevensrapport**

AEM de Gidsen staat u toe om inhoud DITA van de redacteur van het Web te etiketteren. U kunt markeringen op een individueel onderwerp toepassen of de bulketiketterende eigenschap gebruiken om veelvoudige markeringen op veelvoudige onderwerpen, een kaart DITA, of op een sub-kaart toe te passen. U kunt de documentstatus van alle geselecteerde onderwerpen ook wijzigen in de volgende mogelijke algemene documentstatus.

## Metagegevens weergeven

Voer de volgende stappen uit om de metagegevens van uw verwijzingen in de huidige DITA-kaart weer te geven:

1. Open het DITA-kaartbestand in de Kaartweergave in het deelvenster Opslagplaats.
1. Klik op de knop **Beheren** tab.
1. Dubbelklikken **Metagegevens** links. De lijst met metagegevens van alle referenties in de DITA-kaart wordt weergegeven. Dit geldt ook voor de mediaverwijzingen.

   ![](images/web-editor-metadata-panel.png){width="800" align="left"}

1. Van de **Filters** kunt u uw onderwerpen filteren op basis van de **Documentstatus** \(de huidige status van uw onderwerpen. Als uw onderwerpen bijvoorbeeld de status Bewerken, In revisie of Reviewed hebben, worden deze weergegeven\). **Verwijzingen** \(direct of indirect\), **Bestandstype** \(Kaart, Onderwerp, en Beeld \) van de verwijzing.
1. U kunt er ook voor kiezen alleen de **Bestanden zonder tags** of kies ook specifieke tags in het menu **Tags** om de bijbehorende bestanden weer te geven.
   1. U kunt ook de volgende opties voor het filteren van onderwerpen gebruiken om de volgende kolommen in de lijst met metagegevens weer te geven:
      - **Titel** \(standaard geselecteerd\) De titel van het bestand waarnaar wordt verwezen, wordt opgegeven in de DITA-kaart. U kunt op het bestand klikken om het te bewerken. U kunt ook op een audio- of videobestand klikken en dit afspelen in de webeditor. U kunt het volume of de weergave van de video wijzigen. In het snelmenu hebt u ook de mogelijkheid om de afspeelsnelheid te downloaden, te wijzigen of de afbeelding in beeld te bekijken.

        >[!NOTE]
        >
        > Er verschijnt ook een uitcheckpictogram naast de titel van een uitgecheckt bestand. U kunt de muisaanwijzer boven het pictogram plaatsen om de naam van de gebruiker weer te geven.

      - **Bestandsnaam** De naam van het bestand.
      - **Bestandslocatie** Het volledige pad van het bestand.
      - **Tags** \(standaard ingeschakeld\) Labels die op het bestand zijn toegepast.

        >[!NOTE]
        >
        > Standaard kunt u twee tags voor een bestand weergeven. Als u meer tags wilt weergeven, klikt u op **Meer weergeven**. Klikken **Minder tonen** om de lijst opnieuw in te schakelen.

      - **Referentietype** Het soort referentie - direct of indirect
      - **Documentstatus** \(standaard geselecteerd\) De huidige status van het referentiebestand.
      - **Bestandstype** \(standaard geselecteerd\) Type van het bronbestand. De beschikbare opties zijn Kaart, Onderwerp, en Beeld.
      - **Uitgecheckt door** De gebruiker die het bestand heeft uitgecheckt.
1. Klikken **CSV downloaden** om de huidige momentopname van de verwijzingen in de kaart te downloaden DITA. CSV bevat de geselecteerde kolommen en de verwijzingen die in de mening van de Lijst van het Onderwerp worden gefilterd. U kunt dit CSV-bestand met metagegevens vervolgens openen in elke CSV-editor.

**Metagegevens bijwerken**

1. Als u metagegevens wilt bijwerken, selecteert u de bestanden waarvan u de metagegevens wilt bijwerken.

   >[!NOTE]
   >
   > U kunt geen uitgecheckte bestanden selecteren. Er verschijnt ook een uitcheckpictogram naast de titel van een uitgecheckt bestand. U kunt de muisaanwijzer boven het pictogram plaatsen om de naam van de gebruiker weer te geven.

1. Selecteren **Beheren** vanaf de bovenkant.

   ![](images/web-editor-manage-metadata.png){width="350" align="left"}

1. Als u nieuwe tags wilt toevoegen, selecteert u nieuwe tags in de vervolgkeuzelijst om deze toe te passen op alle geselecteerde onderwerpen. U kunt elke tag ook verwijderen door op het kruispictogram bij de tag te klikken.

   >[!NOTE]
   >
   > De gemeenschappelijke markeringen die op alle geselecteerde onderwerpen worden toegepast worden vermeld.

1. Selecteer een nieuwe documentstatus als u de documentstatus van alle geselecteerde verwijzingen wilt wijzigen. Het dopdown toont de gemeenschappelijke mogelijke staat voor alle geselecteerde onderwerpen. Als de huidige status van uw onderwerpen bijvoorbeeld In-Review is, kunt u de status Concept, Goedgekeurd of Herzien weergeven.
1. Klikken **Bijwerken** de metagegevens bijwerken. Er wordt een bevestigingsbericht weergegeven voor de metagegevens, ongeacht of deze zijn bijgewerkt of dat de updates zijn mislukt. U klikt ook op **Rapport downloaden** om de CSV-metagegevens te downloaden vanuit het bevestigingsvenster. Dit CSV bevat de details van de updatestatus voor de geselecteerde verwijzingen.

## Een multimediapport genereren

De **Multimedia** biedt gedetailleerde informatie over de multimedia die in uw kaart wordt gebruikt, zoals de titel, het type \(audio, video en afbeeldingen\), bestanden waarin multimedia wordt gebruikt en het referentietype van de bestanden waarin deze zijn gebruikt. U kunt ook de UUID en de locatie van de multimedia in de opslagplaats bekijken. U kunt een multimediapport maken door de volgende stappen uit te voeren:

1. In de **Bewaarplaats** opent u het DITA-kaartbestand in de Kaartweergave.
1. Klik op de knop **Beheren** tab.
1. Dubbelklikken **Multimedia** links. De lijst met multimedia in de DITA-kaart wordt weergegeven.
1. Van de **Filters** kunt u de lijst ordenen op basis van multimedia of op basis van de namen die worden gebruikt in verwijzingen.

   - Wanneer u bestelt op **Multimedia** De naam****van de multimedia wordt weergegeven in de eerste kolom en de namen van alle verwijzingen waarin ze zijn gebruikt, worden weergegeven in een andere kolom op dezelfde rij. De volgende schermafbeelding toont bijvoorbeeld de multimedia WarmCoolForC.gif in de eerste kolom en drie verwijzingen waarin deze wordt gebruikt, worden weergegeven in de derde kolom op dezelfde rij.

     ![](images/multimedia-report-file-order.png){width="650" align="left"}

   - Als u bestelt op **Gebruikt in** in de kolom, kunt u de omgezette weergave bekijken waarin de namen van de verwijzingen waarin multimedia is gebruikt, worden weergegeven in de eerste kolom, terwijl de multimedianamen in een andere kolom op afzonderlijke rijen worden weergegeven. In de volgende screenshot ziet u bijvoorbeeld de namen van drie verwijzingen \(De temperatuur van de licentie aanpassen, het display van de temperatuur van de licentie wijzigen en het gebied van de bemanning wijzigen\) in de eerste kolom en de multimedia WarmCoolForC.gif wordt weergegeven in de derde kolom op drie aparte rijen.

     ![](images/multimedia-report-used-in-order.png){width="650" align="left"}

1. U kunt uw multimedia filteren op basis van de **Multimediatype**, en **Referentietype**. De lijst met multimediabestanden wordt weergegeven op basis van uw selectie in de vervolgkeuzelijst. U kunt er bijvoorbeeld voor kiezen om alleen de audioreferenties in uw DITA-kaart weer te geven en een bestand toont alleen de audioreferenties die in de kaart worden gebruikt.

   >[!NOTE]
   >
   > Afhankelijk van het type multimedia dat wordt gebruikt in de kaart, worden de afbeelding, video en audio weergegeven in het dialoogvenster **Multimediatype** en Direct of indirect worden vermeld in het dialoogvenster **Referentietype** vervolgkeuzelijst.

1. U kunt ook de volgende filteropties gebruiken om de volgende kolommen in de lijst weer te geven:

   - **Multimedia** \(standaard geselecteerd\) De titel van de multimedia wordt gespecificeerd in de kaart DITA. U kunt op de multimedia klikken om deze te bewerken.
   - **Multimedialocatie** Het volledige pad van de multimedia.
   - **UUID multimedia** De universeel unieke id \(UUID\) van het bestand.
   - **Multimediatype** \(standaard geselecteerd\) Type multimedia. De beschikbare opties zijn Audio, Video of Afbeelding.
   - **Gebruikt in** \(standaard geselecteerd\) De referenties waarin de multimedia is gebruikt. U kunt op de verwijzing klikken om deze te bewerken.
   - **Referentietype** \(standaard geselecteerd\) Het type verwijzing - direct of indirect.
   >[!NOTE]
   >
   > Klikken **Vernieuwen** om een nieuwe lijst met multimedia te verkrijgen en elke wijziging in het kaartbestand weer te geven of als er multimedia in de DITA-kaart is bijgewerkt.

1. U kunt ook op een audio- of videobestand in de webeditor klikken en dit afspelen. U kunt het volume of de weergave van de video wijzigen. In het snelmenu hebt u ook de mogelijkheid om de afspeelsnelheid te downloaden, te wijzigen of de afbeelding in beeld te bekijken.

   ![](images/video-web-editor.png){width="800" align="left"}

1. Klikken **CSV downloaden** om de huidige momentopname van de multimedia in de kaart te downloaden DITA. CSV bevat de geselecteerde kolommen en de multimedia die in **Multimedia** weergeven. U kunt dit CSV-bestand van multimedia vervolgens openen in elke CSV-editor.


## De verbroken koppelingen weergeven en herstellen{#report-broken-links}

De **Verbroken koppelingen** is een nuttig rapport dat u de details van de gebroken verbindingen in uw huidige kaart verstrekt. U kunt de verbroken koppelingen weergeven, bijvoorbeeld voor DITA-onderwerpen, verwijzingen naar multimediabestanden, verwijzingen naar inhoudssleutels enzovoort. Je hebt ook de mogelijkheid om ze hier zelf op te lossen.
Het rapport bevat gedetailleerde informatie, zoals de verbroken koppeling, het type koppeling, de bestanden waarin de verwijzing wordt gebruikt en het type bestanden waarin deze is gebruikt.
U kunt het rapport voor verbroken koppelingen weergeven door de volgende stappen uit te voeren:
1. In de **Bewaarplaats** opent u het DITA-kaartbestand in de Kaartweergave.
1. Klik op de knop **Beheren** tab.
1. Dubbelklikken **Verbroken koppelingen** links. De lijst met verbroken koppelingen of verwijzingen in de DITA-kaart wordt weergegeven.
1. Van de **Filters** kunt u de lijst ordenen aan de hand van koppelingen of aan de hand van de namen die worden gebruikt in verwijzingen.

   - Wanneer u bestelt met **Verbroken koppeling**, worden de paden van de verbroken koppelingen weergegeven in de eerste kolom en worden de namen van alle verwijzingen waarin ze zijn gebruikt, weergegeven in een andere kolom op aparte rijen. Als dezelfde verbroken koppeling in meerdere bestanden wordt gebruikt, worden deze op één rij weergegeven en worden ze als gegroepeerde of subrijen weergegeven. In de volgende screenshot ziet u bijvoorbeeld drie verbroken koppelingen in de eerste kolom en de referentie waarin deze worden gebruikt. `TestMap.ditamap` wordt weergegeven in de derde kolom op drie aparte rijen.
   ![](images/broken-link-report.png){width="800" align="left"}

   - Als u bestelt met **Gebruikt in** in de kolom, kunt u de omgezette weergave bekijken waarin de namen van de verwijzingen waarin de verbroken koppelingen zijn gebruikt, in de eerste kolom worden weergegeven, terwijl de verbroken koppelingen in een andere kolom op dezelfde rij staan. De volgende schermafbeelding toont bijvoorbeeld de verwijzing (waarin de verbroken koppeling wordt gebruikt) `TestMap.ditamap` in de eerste kolom en de verbroken koppelingen worden weergegeven in de derde kolom op dezelfde rij.
   ![](images/broken-link-filter-usedin.png){width="800" align="left"}
1. U kunt verbroken koppelingen filteren op basis van de **Bestandstype** en **Koppelingstype**. De lijst met verbroken koppelingen wordt weergegeven op basis van uw selectie in de vervolgkeuzelijst. U kunt er bijvoorbeeld voor kiezen alleen de inhoudsverwijzingen in uw DITA-kaart weer te geven en een bestand toont alleen de inhoudsverwijzingen die erin worden gebruikt.

   Afhankelijk van het type verwijzingen dat in uw kaart wordt gebruikt, worden de bestandsverwijzing, de belangrijkste verwijzing, de Content Reference, de Content Key Reference, de Afbeeldingsreferentie en de Multimedia File Reference weergegeven in het dialoogvenster **Koppelingstype** vervolgkeuzelijst en **DITA-onderwerp** of **DITA-kaart** worden vermeld in **Bestandstype** vervolgkeuzelijst.
1. U kunt ook de volgende filteropties gebruiken om de volgende kolommen in de lijst weer te geven:

   - **Verbroken koppeling** (standaard geselecteerd) Het pad van de verbroken koppeling wordt opgegeven in de DITA-kaart.

   - **Koppelingstype** (standaard geselecteerd) Het type koppelingen. De beschikbare opties zijn Content Key Reference, Content Reference, DITA Topic, File Reference, Image Reference, Key reference en Multimedia File Reference.

   - **Gebruikt in** (standaard geselecteerd) De verwijzingen waarin de verbroken koppeling is gebruikt. U kunt op de verwijzing klikken om deze weer te geven in de modus Schrijver.

   - **Bestandstype** (standaard geselecteerd) Het type verwijzing - DITA Map of DITA Topic.
Klikken **Vernieuwen** om een nieuwe lijst met verbroken koppelingen op te halen en wijzigingen in het kaartbestand weer te geven of als een verbroken koppeling in de DITA-kaart is bijgewerkt.
1. U kunt op de knop **Koppeling herstellen** icon (![](images/fix-broken-link.svg)) om de verbroken koppeling te herstellen.

   >[!NOTE]
   >
   > Houd de muisaanwijzer boven het verbroken koppelingspad onder de kolom Verbroken koppeling om de koppeling Repareren weer te geven (![](images/fix-broken-link.svg)).

   U kunt een koppeling in beide weergaven corrigeren - wanneer u hebt besteld door **Verbroken koppelingen** of door **Gebruikt in**.

   >[!NOTE]
   >
   > Wanneer u een verbroken koppeling corrigeert terwijl u de opdracht Verbroken koppelingen hebt gekregen, wordt de koppeling hersteld in alle bestanden waar deze wordt gebruikt (die in één rij zijn gegroepeerd).

1. U moet de vereiste referentiedetails in bijwerken **Koppeling bijwerken** in. De in **Koppeling bijwerken** is afhankelijk van het type verwijzing.\
   Als u een koppeling hebt hersteld, wordt deze niet weergegeven onder de lijst met verbroken koppelingen. In plaats daarvan kunt u deze weergeven onder Onderwerplijst of Metagegevens.

1. Klikken **CSV downloaden** om de huidige momentopname van de gebroken verbindingen in de kaart te downloaden DITA. CSV bevat de geselecteerde kolommen en de verbroken verbindingen die in de Gebroken mening van Verbindingen worden gefiltreerd. U kunt dit CSV-bestand vervolgens openen en weergeven in elke CSV-editor.


**Bovenliggend onderwerp:**[ Rapporten](reports-intro.md)
