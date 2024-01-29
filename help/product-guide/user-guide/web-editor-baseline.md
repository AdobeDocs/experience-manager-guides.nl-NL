---
title: Basislijnen maken en beheren vanuit de webeditor
description: Maak en beheer basislijnen in de webeditor in AEM hulplijnen. Leer hoe u basislijnen maakt op basis van labels en filters toepast op de basislijnen.
exl-id: 14f87bdd-3042-46f9-853e-e9ded81b10ed
feature: Authoring, Features of Web Editor, Publishing
role: User
source-git-commit: 6006cabdc11b80179833a21b4d99d2f6c3f968ee
workflow-type: tm+mt
source-wordcount: '1687'
ht-degree: 0%

---

# Basislijnen maken en beheren vanuit de webeditor {#id223MB0ZF043}

>[!TIP]
>
> Het wordt geadviseerd om deze eigenschap van de Basislijn van de Redacteur van het Web te gebruiken als u aan AEM Gidsen as a Cloud Service versie van Maart of later hebt bevorderd.

AEM Gidsen verstrekt de eigenschap van de Basislijn die binnen de Redacteur van het Web wordt geïntegreerd die de gebruikers toestaat om basislijnen tot stand te brengen en hen te gebruiken om onderwerpen van verschillende versies te publiceren of te vertalen. Ze kunnen ook meerdere uitvoervoorinstellingen van dezelfde DITA-kaart tegelijk publiceren.

## Een basislijn maken

U kunt een basislijn van de Redacteur van het Web tot stand brengen door de volgende stappen uit te voeren:

1. Open het DITA-kaartbestand in de Kaartweergave in het deelvenster Opslagplaats.
1. Klik op de knop **Beheren** tab. De **Basislijn** geeft de basislijnen van de DITA-kaart weer.

   ![Deelvenster Basleine](images/baseline-manage.png){width="800" align="left"}

1. Op de **Basislijn** selecteert u het plus-pictogram (+) rechtsboven om een basislijn te maken.
1. Voer een naam in voor de basislijn in **Naam**.
1. In **Configuratie** U kunt kiezen **Handmatige update** of **Automatische update** optie:

   **Handmatige update**: U kunt handmatig een statische basislijn maken met een specifieke versie van de onderwerpen en inhoud waarnaar wordt verwezen, beschikbaar op een specifieke datum en tijd, of met een label dat is gedefinieerd voor een versie van de onderwerpen:

   - In **Selecteer de versie op basis van** Selecteer een van de volgende opties:


      1. **Datum** &lt;time stamp=&quot;&quot;>: Kies de versie van de onderwerpen op de opgegeven datum en tijd.
      1. **Label**: Selecteer deze optie als u de onderwerpen wilt selecteren op basis van het label dat op de onderwerpen is toegepast. Als voor de onderwerpen labels zijn opgegeven, worden de labels vermeld in de vervolgkeuzelijst. U kunt een label in de lijst kiezen. U kunt ook een label toevoegen in het tekstvak.

         Voor de directe verwijzingen in statische basislijnen, worden de etiketten getrokken van de recentste bewaarde versie van de kaart. Als u bijvoorbeeld labels hebt gemaakt `Label Release 1.0` en `Label Release 1.1` voor versies 1.0 en 1.1 van Onderwerp A, en voeg dan Onderwerp A aan de kaart toe die als versie 1.0 wordt bewaard. In dit geval kunt u de labels weergeven `Label Release 1.0` en `Label Release 1.1` in de vervolgkeuzelijst voor statische basislijnlabels.


         Wanneer u **Label,** u kunt de directe en indirecte referenties kiezen.
         - Voor directe verwijzingen binnen de kaart DITA, krijgt u een optie om de recentste versie van onderwerpen te gebruiken die niet het gespecificeerde etiket hebben op hen wordt toegepast.

           >[!NOTE]
           >
           > Als u een label invoert dat niet bestaat, selecteert u de optie **Geen basislijn maken** Dan ontbreekt de basislijnverwezenlijking en geeft een foutenmelding dichtbij de basislijnnaam in het paneel van de Basislijn.

         - Voor indirecte verwijzingen binnen de kaart DITA, krijgt u een extra optie om de recentste versie van onderwerpen te gebruiken die niet het gespecificeerde etiket hebben op hen wordt toegepast. U kunt ook **Automatisch kiezen** voor de inhoud waarnaar wordt verwezen, en het systeem kiest automatisch de versie van de inhoud waarnaar wordt verwezen die overeenkomt met de versie van de inhoud waarnaar wordt verwezen.

         Nadat u een label of versie hebt geselecteerd als op datum, worden alle onderwerpen waarnaar wordt verwezen en mediabestanden in de kaart dienovereenkomstig geselecteerd. Deze selectie van onderwerpen wordt niet getoond op het gebruikersinterface, maar het wordt bewaard in het achterste eind.

   **Automatische update**: Selecteer deze optie voor het maken van de basislijn om de onderwerpen automatisch te selecteren op basis van het label dat op de onderwerpen is toegepast.

   Basislijnen die zijn gemaakt met de automatische updateconfiguratie worden dynamisch bijgewerkt. Als u een basislijn genereert, een basislijn downloadt of een vertaalproject maakt met een basislijn, worden de bestanden dynamisch gekozen op basis van de bijgewerkte labels. Bijvoorbeeld, als u versie 1.2 van een onderwerp met Versie 1.0 van het Etiket voor de basislijn en recentere bijgewerkte versie 1.5 met Versie 1.0 van het Etiket hebt gebruikt, zal de basislijn dynamisch worden bijgewerkt, en versie 1.5 zal worden gebruikt.

   ![Een basislijn maken](images/dynamic-baseline.png){width="300" align="left"}

   - **Labels selecteren**: Als voor de onderwerpen labels zijn opgegeven, gebruikt u de opdracht **Labels selecteren** keuzelijst die u in het dialoogvenster [vermelde labels](#labels-list).
De eerst geselecteerde labels krijgen een hogere prioriteit dan de latere labels.

     Voor dynamische basislijnen worden de labels opgehaald uit de laatst opgeslagen versie en de huidige werkkopie van de kaart. Als u bijvoorbeeld labels hebt gemaakt   `Label Release A.1.0 ` en `Label Release A.1.1` voor versies 1.0 en 1.1 van Onderwerp A en etiketten `Label Release B.1.0` en `Label Release B.1.1` voor versies 1.0 en 1.1 van Onderwerp B. Dan kunt u Onderwerp A aan Kaart A in versie 1.0 en Onderwerp B aan Kaart A in 1.0* (het werk exemplaar) toevoegen. In dit geval kunt u  `Label Release A.1.0 `, `Label Release A.1.1`, `Label Release B.1.0`, en `Label Release B.1.1` in de vervolgkeuzelijst met dynamische basislijnlabels.

1. **Indirecte verwijzingen**: Voor indirecte verwijzingen binnen de kaart DITA, krijgt u de volgende opties:

   - **Automatisch selecteren**: U kunt ervoor kiezen **Automatisch kiezen** voor de inhoud waarnaar wordt verwezen, en het systeem kiest automatisch de versie van de inhoud waarnaar wordt verwezen die overeenkomt met de versie van de inhoud waarnaar wordt verwezen.

   - **Geselecteerd label gebruiken**: U kunt een basislijn maken met het geselecteerde label dat is gedefinieerd voor een versie van onderwerpen.
   - **De nieuwste versie of de werkkopie gebruiken**: Gebruik de nieuwste versie van onderwerpen waarop het opgegeven label niet is toegepast of als er geen versie is gemaakt, gebruikt u de werkkopie van de onderwerpen om de basislijn te maken.
1. Klikken **Toepassen**.

De basislijn wordt gemaakt. De basislijnverwezenlijking gebeurt asynchroon, zodat kunt u aan andere dossiers in de Redacteur van het Web blijven werken. Zodra de basislijn wordt gecreeerd, wordt een pop-up bericht getoond bevestigend dat de basislijn is gecreeerd, en u ontvangt ook een Inbox- bericht voor het zelfde.

## Basislijnen beheren

U kunt uw bestaande basislijnen beheren met de verschillende functies op het basislijndashboard.

- U kunt zoeken naar een bestaande basislijn met het tekstvak in het deelvenster Basislijn. Gebruik de **Filter toepassen** om alle basislijnen weer te geven of de basislijnen weer te geven met de aanmaakstatus Voltooid, Bezig of Mislukt.
- Gebruik de **Vernieuwen** in het deelvenster Basislijn om opnieuw te controleren op alle basislijnen en een nieuwe lijst met basislijnen weer te geven voor de DITA-kaart die wordt geopend in de Kaartweergave.
- U kunt de inhoud van een bestaande statische basislijn weergeven of bewerken door te dubbelklikken op de basislijn in de lijst in het dialoogvenster **Basislijn** deelvenster. In het basislijnbewerkingsvenster in het midden worden het DITA-kaartbestand, de inhoud of onderwerpen van de kaart en de inhoud waarnaar wordt verwezen, weergegeven.

  >[!NOTE]
  >
  >Bewerking voor statische basislijnen wordt alleen aanbevolen voor een klein aantal wijzigingen in de verwijzing. Bewerkingen bewerken wordt niet aangeraden om de versie van de hoofd-DITA-kaart te wijzigen, omdat alle referenties opnieuw moeten worden berekend. Dit kan een fout van de basislijnupdate voor grote kaarten DITA veroorzaken. Voor de grotere DITA kaarten, kunt u een nieuwe basislijn tot stand brengen of de eigenschappen van de basislijn uitgeven.
  >
  >Met de bewerking Bewerken in het geval van een dynamische basislijn kunt u de eigenschappen van de basislijn bewerken terwijl de referenties voor dynamische basislijnen bij uitvoering worden gegenereerd met de labels.

  ![opties van een basislijn](images/baseline-options.png){width="800" align="left"}



  U kunt ook de volgende bewerkingen op de basislijn uitvoeren vanuit het menu Opties:

### Een basislijn dupliceren

U kunt een basislijn dupliceren en deze aanpassen aan uw vereisten.
![een basislijn dupliceren](images/baseline-duplicate.png){width="300" align="left"}
*Dupliceer een basislijn op basis van een label of maak een exacte kopie.*

1. Selecteren **Dupliceren** in het menu Opties van een basislijn. De **Basislijn dupliceren** wordt geopend.
>[!NOTE]
> >De standaardnaam van de basislijn is `<selected baseline name>`_suffix (zoals sample-baseline_1). U kunt de naam naar wens wijzigen.

   In **Selecteer de versie op basis van** kunt u kiezen voor **Exacte kopie** of de **Label** optie:

   - **Exacte kopie**: Met Hulplijnen voor Experience Manager wordt dezelfde versie van alle onderwerpen gekozen en wordt een exacte kopie van de gedupliceerde basislijn gemaakt.
   - **Label**: Met het vervolgkeuzemenu kunt u een van de opties [vermelde labels](#labels-list). De Gidsen van de Experience Manager selecteert die versies van de onderwerpen met het geselecteerde die etiket voor hen wordt bepaald, terwijl voor de resterende onderwerpen, het de versie van de gedupliceerde basislijn kiest. U selecteert bijvoorbeeld het label `Release 1.0` in het vervolgkeuzemenu selecteert u de versies van de onderwerpen waarvoor u dit label hebt gedefinieerd. Voor alle andere onderwerpen, kiest het de versie van de gedupliceerde basislijn.
1. Klikken **Dupliceren**.

- **Naam wijzigen**, of **Verwijderen** een bestaande basislijn.
- Bestaande labels toevoegen, verwijderen of wijzigen in het menu **Labels beheren** optie voor statische basislijnen. Als uw beheerder vooraf gedefinieerde labels heeft geconfigureerd, worden deze labels weergegeven in de vervolgkeuzelijst Label toevoegen. Zie voor meer informatie over het toevoegen van labels [Labels gebruiken](web-editor-use-label.md#).

  >[!NOTE]
  >
  > Het proces om etiketten toe te voegen of te verwijderen gebeurt asynchroon, zodat kunt u aan andere dossiers in de Redacteur van het Web blijven werken. Nadat het label is toegevoegd of verwijderd, wordt een pop-upbericht weergegeven met de bevestiging dat het label is toegevoegd of verwijderd. U ontvangt ook een melding in het Postvak IN.

- **Eigenschappen bewerken** van een bestaande statische basislijn die u hebt ingesteld tijdens het maken van de basislijn.
- De opname van een basislijn exporteren in een Microsoft Excel-bestand met de opdracht **Basislijn exporteren** -optie.


### Lijst met labels {#labels-list}

De labels in de vervolgkeuzelijst zijn gebaseerd op de volgende criteria:
- De etiketten zouden aan één van de versies van de onderwerpen in de kaart moeten worden toegevoegd DITA (waarop de basislijn wordt gecreeerd).
- En alleen de verwijzingen op het eerste niveau (onderwerpen of submaps) van de DITA-kaart worden in overweging genomen bij het kiezen van de labels.



## Basislijnfilters

Het pictogram Filters in het dialoogvenster **Basislijnfilters** kunt u filters toepassen op de basislijn die is geopend in het basislijnbewerkingsvenster:

![basislijnfilters](images/baseline-filter.png){width="300" align="left"}

- De bestanden filteren op bestandsnamen of bestandslocatie.
- Filter de bestanden op basis van de waarden voor verschillende kolommen, zoals Bestandstype, Referentietype, enzovoort.
- Kies de kolommen die u wilt weergeven in het basislijnbewerkingsvenster.

>[!NOTE]
>
> U kunt op een kolomkop klikken en de bestanden sorteren op basis van de kolommen in het basislijnbewerkingsvenster.

**Een basislijn opslaan of opnieuw instellen**

Nadat u de basislijn hebt bewerkt, kunt u op de knop **Opslaan** aan de bovenkant om de wijzigingen in de basislijn op te slaan. U kunt op de knop **Herstellen** als u de wijziging niet wilt opslaan en de basislijn opnieuw wilt instellen. Wanneer u op de knop **Herstellen** er verschijnt een waarschuwing dat de niet-opgeslagen wijzigingen verloren gaan.

**Bovenliggend onderwerp:**[ Werken met de webeditor](web-editor.md)

