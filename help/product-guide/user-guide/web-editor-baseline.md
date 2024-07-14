---
title: Basislijnen maken en beheren vanuit de webeditor
description: Basislijnen maken en beheren vanuit de webeditor in AEM Guides. Leer hoe u basislijnen maakt op basis van labels en filters toepast op de basislijnen.
exl-id: 14f87bdd-3042-46f9-853e-e9ded81b10ed
feature: Authoring, Features of Web Editor, Publishing
role: User
source-git-commit: c4c5fa16daf3f713f85783152094c8af59eb4f8c
workflow-type: tm+mt
source-wordcount: '1699'
ht-degree: 0%

---

# Basislijnen maken en beheren vanuit de webeditor {#id223MB0ZF043}

>[!TIP]
>
> Het wordt geadviseerd om deze eigenschap van de Basislijn van de Redacteur van het Web te gebruiken als u aan de versie van AEM Guides as a Cloud Service Maart of later hebt bevorderd.

AEM Guides verstrekt de eigenschap van de Basislijn die binnen de Redacteur van het Web wordt geïntegreerd die de gebruikers toestaat om basislijnen tot stand te brengen en hen te gebruiken om onderwerpen van verschillende versies te publiceren of te vertalen. Ze kunnen ook meerdere uitvoervoorinstellingen van dezelfde DITA-kaart tegelijk publiceren.

## Een basislijn maken

U kunt een basislijn van de Redacteur van het Web tot stand brengen door de volgende stappen uit te voeren:

1. Open het DITA-kaartbestand in de Kaartweergave in het deelvenster Opslagplaats.
1. Klik **leiden** tabel. Het **paneel van de Basislijn** toont de basislijnen van de kaart DITA.

   ![ het paneel van de Basleine ](images/baseline-manage.png){width="800" align="left"}

1. Voor het **paneel van de Basislijn**, selecteer + pictogram bij top-right beginnen een basislijn te creëren.
1. Ga een naam voor de basislijn in **Naam** in.
1. In **Configuratie**, kunt u of **Handmatige update** optie of **Automatische update** optie kiezen:

   **Hand update**: U kunt een statische basislijn met een specifieke versie van de onderwerpen en van verwijzingen voorzien inhoud manueel tot stand brengen beschikbaar op een specifieke datum en een tijd, of met een etiket dat voor een versie van onderwerpen wordt bepaald:

   - In **selecteer de versie die op wordt gebaseerd,** selecteer één van de volgende opties:


      1. **Datum** &lt;tijdstempel\>: Kies de versie van de onderwerpen zoals op de gespecificeerde datum en de tijd.
      1. **Etiket**: Selecteer deze optie om de onderwerpen volgens het etiket te kiezen dat op hen wordt toegepast. Als voor de onderwerpen labels zijn opgegeven, worden de labels vermeld in de vervolgkeuzelijst. U kunt een label in de lijst kiezen. U kunt ook een label toevoegen in het tekstvak.

         Voor de directe verwijzingen in statische basislijnen, worden de etiketten getrokken van de recentste bewaarde versie van de kaart. Bijvoorbeeld, als u etiketten `Label Release 1.0` en `Label Release 1.1` voor versies 1.0 en 1.1 van Onderwerp A hebt gecreeerd, en dan Onderwerp A aan de kaart toevoegt die als versie 1.0 wordt bewaard. In dit geval kunt u de labels `Label Release 1.0` en `Label Release 1.1` in het vervolgkeuzemenu weergeven voor statische basislijnlabels.


         Wanneer u **Etiket selecteert,** kunt u de directe en indirecte verwijzingen kiezen.
         - Voor directe verwijzingen binnen de kaart DITA, krijgt u een optie om de recentste versie van onderwerpen te gebruiken die niet het gespecificeerde etiket hebben op hen wordt toegepast.

           >[!NOTE]
           >
           > Als u een etiket ingaat dat niet bestaat en de optie **selecteert creeer geen basislijn** dan ontbreekt de basislijnverwezenlijking en geeft een foutenmelding dichtbij de basislijnnaam in het paneel van de Basislijn.

         - Voor indirecte verwijzingen binnen de kaart DITA, krijgt u een extra optie om de recentste versie van onderwerpen te gebruiken die niet het gespecificeerde etiket hebben op hen wordt toegepast. U kunt ook aan **kiezen automatisch** voor de referenced inhoud kiezen, en het systeem plukt automatisch de versie van de referenced inhoud die aan de versie van de inhoud beantwoordt waarin het van verwijzingen wordt voorzien.

         Nadat u een label of versie hebt geselecteerd als op datum, worden alle onderwerpen waarnaar wordt verwezen en mediabestanden in de kaart dienovereenkomstig geselecteerd. Deze selectie van onderwerpen wordt niet getoond op het gebruikersinterface, maar het wordt bewaard in het achterste eind.

   **Automatische update**: Selecteer deze optie voor basislijnverwezenlijking om de onderwerpen volgens het etiket automatisch te kiezen dat op hen wordt toegepast.

   Basislijnen die zijn gemaakt met de automatische updateconfiguratie worden dynamisch bijgewerkt. Als u een basislijn genereert, een basislijn downloadt of een vertaalproject maakt met een basislijn, worden de bestanden dynamisch gekozen op basis van de bijgewerkte labels. Bijvoorbeeld, als u versie 1.2 van een onderwerp met Versie 1.0 van het Etiket voor de basislijn en recentere bijgewerkte versie 1.5 met Versie 1.0 van het Etiket hebt gebruikt, zal de basislijn dynamisch worden bijgewerkt, en versie 1.5 zal worden gebruikt.

   ![ creeer een basislijn ](images/dynamic-baseline.png){width="300" align="left"}

   - **Etiketten**: Als de onderwerpen labels hebben voor hen worden gespecificeerd, dan gebruik **Etiketten** dropdown om van de [ vermelde etiketten ](#labels-list) te kiezen.
De eerst geselecteerde labels krijgen een hogere prioriteit dan de latere labels.

     >[!NOTE]
     >
     >Terwijl de labels worden gesleept, wordt een lader weergegeven en wordt het vervolgkeuzemenu uitgeschakeld.

     Voor dynamische basislijnen worden de labels opgehaald uit de laatst opgeslagen versie en de huidige werkkopie van de kaart. Als u bijvoorbeeld labels hebt gemaakt   `Label Release A.1.0 ` en `Label Release A.1.1` voor versies 1.0 en 1.1 van Onderwerp A en labels `Label Release B.1.0` en `Label Release B.1.1` voor versies 1.0 en 1.1 van Onderwerp B. Dan kunt u Onderwerp A aan Kaart A in versie 1.0 en Onderwerp B aan Kaart A in 1.0* (het werk exemplaar) toevoegen. In dit geval kunt u `Label Release A.1.0 ` , `Label Release A.1.1` , `Label Release B.1.0` en `Label Release B.1.1` weergeven in het vervolgkeuzemenu met dynamische basislijnlabels.

1. **Indirecte Verwijzingen**: Voor indirecte verwijzingen binnen de kaart DITA, wordt u gegeven de volgende opties:

   - **Keuze automatisch**: U kunt kiezen **kiezen automatisch** voor de referenced inhoud, en het systeem plukt automatisch de versie van de referenced inhoud die aan de versie van de inhoud beantwoordt waarin het van verwijzingen wordt voorzien.

   - **Uitgezochte etiket van het Gebruik**: U kunt een basislijn met het geselecteerde die etiket tot stand brengen voor een versie van onderwerpen wordt bepaald.
   - **Gebruik de recentste versie of het het werk exemplaar**: Gebruik de recentste versie van onderwerpen die niet het gespecificeerde etiket hebben dat op hen wordt toegepast, of als geen versie is gecreeerd, dan gebruik het werkende exemplaar van de onderwerpen om de basislijn tot stand te brengen.
1. Klik **toepassen**.

De basislijn wordt gemaakt. De basislijnverwezenlijking gebeurt asynchroon, zodat kunt u aan andere dossiers in de Redacteur van het Web blijven werken. Zodra de basislijn wordt gecreeerd, wordt een pop-up bericht getoond bevestigend dat de basislijn is gecreeerd, en u ontvangt ook een Inbox- bericht voor het zelfde.

## Basislijnen beheren

U kunt uw bestaande basislijnen beheren met de verschillende functies op het basislijndashboard.

- U kunt zoeken naar een bestaande basislijn met het tekstvak in het deelvenster Basislijn. Gebruik **pas het pictogram van de Filter** toe om alle basislijnen te tonen of van de basislijnen met de schepingsstatus als Succes, in uitvoering, of Ontbroken een lijst te maken.
- Gebruik **verfrissen zich** pictogram in het paneel van de Basislijn om voor alle basislijnen opnieuw te controleren en een nieuwe lijst van basislijnen voor de kaart te tonen DITA die in de Mening van de Kaart wordt geopend.
- U kunt de inhoud van een bestaande statische basislijn bekijken of uitgeven door de basislijn van de lijst in het **paneel van de Basislijn** tweemaal te klikken. In het basislijnbewerkingsvenster in het midden worden het DITA-kaartbestand, de inhoud of onderwerpen van de kaart en de inhoud waarnaar wordt verwezen, weergegeven.

  >[!NOTE]
  >
  >Bewerking voor statische basislijnen wordt alleen aanbevolen voor een klein aantal wijzigingen in de verwijzing. Bewerkingen bewerken wordt niet aangeraden om de versie van de hoofd-DITA-kaart te wijzigen, omdat alle referenties opnieuw moeten worden berekend. Dit kan een fout van de basislijnupdate voor grote kaarten DITA veroorzaken. Voor de grotere DITA kaarten, kunt u een nieuwe basislijn tot stand brengen of de eigenschappen van de basislijn uitgeven.
  >
  >Met de bewerking Bewerken in het geval van een dynamische basislijn kunt u de eigenschappen van de basislijn bewerken terwijl de referenties voor dynamische basislijnen bij uitvoering worden gegenereerd met de labels.

  ![ opties van een basislijn ](images/baseline-options.png){width="800" align="left"}



  U kunt ook de volgende bewerkingen op de basislijn uitvoeren vanuit het menu Opties:

### Een basislijn dupliceren

U kunt een basislijn dupliceren en deze aanpassen aan uw vereisten.
![ dupliceer een basislijn ](images/baseline-duplicate.png){width="300" align="left"}
*Dupliceer een basislijn die op een etiket wordt gebaseerd of creeer een nauwkeurige kopie.*

1. Selecteer **Dupliceer** van het menu van Opties van een basislijn. Het **Duplicate basislijn** dialoogvakje opent.
>[!NOTE]
>
>De standaardnaam van de basislijn is `<selected baseline name>` _suffix (zoals sample-baseline_1). U kunt de naam naar wens wijzigen.

   In **selecteer de versie die op** wordt gebaseerd, kunt u of de **Exacte exemplaar** optie of de **optie van het Etiket** kiezen:

   - **Exact exemplaar**: Experience Manager Guides plukt de zelfde versie van alle onderwerpen en leidt tot een nauwkeurige kopie van de gedupliceerde basislijn.
   - **Etiket**: Gebruikend dropdown, kunt u één van de [ vermelde etiketten ](#labels-list) kiezen. Experience Manager Guides kiest die versies van de onderwerpen met het geselecteerde die etiket voor hen wordt bepaald, terwijl voor de resterende onderwerpen, het de versie van de gedupliceerde basislijn kiest. U selecteert bijvoorbeeld het label `Release 1.0` in het vervolgkeuzemenu en kiest vervolgens de versies van de onderwerpen waarvoor u dit label hebt gedefinieerd. Voor alle andere onderwerpen, kiest het de versie van de gedupliceerde basislijn.
1. Klik **Dupliceren**.

- **noem** anders, of **schrap** een bestaande basislijn.
- Voeg, verwijder, of breng veranderingen in bestaande etiketten van **toe leidt de optie van Etiketten** voor statische basislijnen. Als uw beheerder vooraf gedefinieerde labels heeft geconfigureerd, worden deze labels weergegeven in de vervolgkeuzelijst Label toevoegen. Voor meer informatie over het toevoegen van etiketten, zie {de etiketten van het 0} Gebruik ](web-editor-use-label.md#).[

  >[!NOTE]
  >
  > Het proces om etiketten toe te voegen of te verwijderen gebeurt asynchroon, zodat kunt u aan andere dossiers in de Redacteur van het Web blijven werken. Nadat het label is toegevoegd of verwijderd, wordt een pop-upbericht weergegeven met de bevestiging dat het label is toegevoegd of verwijderd. U ontvangt ook een melding in het Postvak IN.

- **geeft eigenschappen** van een bestaande statische basislijn uit die u terwijl het creëren van de basislijn hebt geplaatst.
- Exporteer de momentopname van een basislijn in een dossier van Microsoft Excel met de **optie van de Basislijn van de Uitvoer**.


### Lijst met labels {#labels-list}

De labels in de vervolgkeuzelijst zijn gebaseerd op de volgende criteria:
- De etiketten zouden aan één van de versies van de onderwerpen in de kaart moeten worden toegevoegd DITA (waarop de basislijn wordt gecreeerd).
- En alleen de verwijzingen op het eerste niveau (onderwerpen of submaps) van de DITA-kaart worden in overweging genomen bij het kiezen van de labels.



## Basislijnfilters

Gebruikend het pictogram van Filters in het **paneel van de Filters van de Basislijn** kunt u filters op de basislijn toepassen die in het basislijn het uitgeven venster wordt geopend:

![ basislijnfilters ](images/baseline-filter.png){width="300" align="left"}

- De bestanden filteren op bestandsnamen of bestandslocatie.
- Filter de bestanden op basis van de waarden voor verschillende kolommen, zoals Bestandstype, Referentietype, enzovoort.
- Kies de kolommen die u wilt weergeven in het basislijnbewerkingsvenster.

>[!NOTE]
>
> U kunt op een kolomkop klikken en de bestanden sorteren op basis van de kolommen in het basislijnbewerkingsvenster.

**sparen of het Terugstellen een Basislijn**

Zodra u de basislijn hebt uitgegeven, kunt u **klikken sparen** knoop op de bovenkant om de veranderingen in de basislijn te bewaren. U kunt de **knoop van het Terugstellen** klikken als u niet de verandering wilt bewaren en de basislijn terugstellen. Wanneer u de **knoop van het Terugstellen** klikt wordt een waarschuwing getoond dat uw niet bewaarde veranderingen zouden worden verloren.

**Bovenliggend onderwerp:**[ Werk met de Redacteur van het Web ](web-editor.md)

