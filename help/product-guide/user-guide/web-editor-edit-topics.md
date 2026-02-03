---
title: Onderwerpen bewerken in de Editor
description: Leer onderwerpen te bewerken in de Editor. U kent verschillende bewerkingsfuncties om uw onderwerpbestanden in AEM Guides te wijzigen.
exl-id: 8da37a81-e8c3-434f-b3f4-4723d87c2ade
feature: Authoring, Web Editor
role: User
source-git-commit: df3da8a0b4dd50ac177c3b51f04a855e9638058e
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 0%

---

# Onderwerpen bewerken in de Editor {#id2056B040VUI}

De Redacteur komt met een waaier van het uitgeven eigenschappen die u gemakkelijk toestaan om uw onderwerpdossiers tot stand te brengen of te wijzigen. In grote lijnen voert u de volgende stappen uit om een onderwerp in de Editor te bewerken.

>[!IMPORTANT]
>
> Als er een toepassingsfout optreedt terwijl u aan de Editor werkt, vernieuwt u de pagina om verder te werken.

1. Om veranderingen in uw onderwerp aan te brengen, klik binnen de tekstgrens van het vereiste element en begin het aanbrengen uitgeeft.

1. Als u een specifiek element wilt invoegen, plaatst u de cursor aan het einde van het element waarna u het nieuwe element wilt invoegen en selecteert u het gewenste elementpictogram op de werkbalk. U kunt de toetsenbordkortere weg `Alt+1` ook gebruiken om **te roepen het Element van het Tussenvoegsel** popup.

   Er wordt een lijst met elementen weergegeven die in het onderwerp kan worden gebruikt. Experience Manager Guides voert een intelligente plaatsing van elementen volgens hun geldige plaats in het onderwerp uit.

   >[!NOTE]
   >
   > U kunt ook kiezen welk pictogram op de werkbalk moet worden weergegeven door het `ui_config.json` -bestand te configureren dat zich op - `/etc/designs/fmdita/clientlibs/xmleditor/` bevindt. Neem voor meer informatie over het aanpassen van functies contact op met de systeembeheerder.

1. Zodra u klaar bent met het uitgeven van uw document, uitgezocht **sparen allen**.

   >[!NOTE]
   >
   > Als u niet wenst om veranderingen in de bewaarplaats van Adobe Experience Manager vast te leggen, selecteer **dicht**, en selecteer dan **Sluiten zonder** in de Unsaved dialoog van Veranderingen te bewaren.


## Gedeeltelijke selectie van inhoud tussen elementen

Met Experience Manager Guides kunt u ook inhoud selecteren voor verschillende elementen. Nadat u de inhoud hebt geselecteerd, kunt u de volgende bewerkingen uitvoeren:

- Opmaak en verwijderen: de geselecteerde inhoud vet maken, cursief maken, onderstrepen of zelfs verwijderen. De inhoud van de geldige open labels wordt vervolgens samengevoegd en weergegeven onder één element. U kunt bijvoorbeeld de inhoud in een alinea selecteren en de selectie uitbreiden naar een andere alinea. Als u de geselecteerde inhoud vervolgens vet maakt, wordt alle vette inhoud van de geopende labels samengevoegd en weergegeven onder één alinea-element.

Als u de geselecteerde inhoud verwijdert, wordt de resterende inhoud na het verwijderen in de geopende tags samengevoegd.

- Omring de inhoud met een geldig element: voer de volgende stappen uit om de inhoud te laten omlopen met een geldig element:

   - Selecteer de inhoud in een element.
   - Selecteer ![ voeg ](images/Add_icon.svg) pictogram van de toolbar op de bovenkant toe om het **element van het Tussenvoegsel** dialoogvakje te bekijken. In het dialoogvenster worden de geldige elementen voor de geselecteerde inhoud weergegeven.
     >[!NOTE]
     >
     > U kunt het dialoogvenster Element invoegen ook weergeven door het contextmenu van de geselecteerde inhoud te selecteren.

   - Selecteer een element in het dialoogvenster. De geselecteerde inhoud wordt ondergebracht in dat element. Bijvoorbeeld, als u de inhoud in een paragraaf selecteert en dan het `<note>` element van het **het element van het Tussenvoegsel** dialoogvakje kiest, verschijnt de geselecteerde inhoud onder een nota.

     ![ de dialoogdoos van het element van het Tussenvoegsel ](./images/insert-element-editor.png) {width="300" align="left"}

## Browser vernieuwen tijdens bewerken van bestanden

Experience Manager Guides biedt ondersteuning voor het vernieuwen van de browser terwijl u uw inhoud bewerkt in de Editor. Met deze functie kunt u doorgaan met het bewerken van inhoud voor het geval u tijdens het werken een toepassingsfout tegenkomt. Als u de browser vernieuwt terwijl een of meer bestanden met niet-opgeslagen wijzigingen worden geopend voor bewerking, wordt u gewaarschuwd dat de niet-opgeslagen wijzigingen verloren kunnen gaan. U kunt de vernieuwingsbewerking annuleren en uw bestanden opslaan om de wijzigingen te behouden.

Zelfs bij het vernieuwen van de browser blijven de weergaven links en rechts in de Editor behouden. Experience Manager Guides herstelt de laatst opgeslagen status van de bestanden die zijn geopend in de Editor wanneer u de browser vernieuwt. De bestanden die bijvoorbeeld in het deelvenster Opslagplaats worden geopend, worden opnieuw geopend. Het kaartvenster blijft samen met de eerder geopende kaart behouden.

Het actieve onderwerp of de kaart DITA wordt opnieuw geopend in het inhoudsuitgevende gebied.

Het rechterdeelvenster wordt ook opnieuw geopend en geeft dezelfde weergave weer als vóór het vernieuwen.

## Werkkopie-indicator

Experience Manager Guides geeft de werkkopie-indicator weer, waarmee wordt aangegeven of de huidige \(werkkopie\) van het bestand al dan niet synchroon is met de opgeslagen versie. Als u wijzigingen hebt aangebracht in uw huidige kopie en uw bestand niet hebt opgeslagen, wordt een \*-markering weergegeven samen met de titel op het tabblad Bestand van het onderwerp. Deze indicator dient als herinnering om uw wijzigingen op te slaan en verdwijnt wanneer u het bestand opslaat.

![ werkende exemplaarindicator ](images/working-copy-text-update-indicator.png){width="550" align="left"}

Experience Manager Guides geeft ook aan of de laatst opgeslagen \(werkende\) kopie van het bestand al dan niet synchroon is met de opgeslagen versie. Als u enkele niet-opgeslagen wijzigingen hebt aangebracht tussen de werkkopie en de laatst opgeslagen versie, wordt een \*-markering weergegeven samen met de versiegegevens die worden weergegeven in de rechterbovenhoek van het tabblad Bestandsbeheer van het onderwerp. Deze indicator dient als herinnering voor het opslaan en maken van een versie van de huidige \(werkende\) versie van het bestand.

>[!NOTE]
>
> Om het even welke veranderingen in de meta-gegevensgebieden beschikbaar onder [ eigenschappen van het Dossier ](./web-editor-right-panel.md#file-properties) zullen ook de het werk exemplaarindicator op de documentversie teweegbrengen.

![ de updateindicator van de Versie ](images/version-update-indicator.png){width="550" align="left"}

## Vergrendelde bestanden openen in de modus Auteur en Source

Wanneer een DITA- of Markdown-bestand is vergrendeld of uitgecheckt door een andere gebruiker, is het niet mogelijk de inhoud te bewerken of te wijzigen. Nochtans, kunt u het dossier in een read-only formaat in zowel de **Auteur** als **Source** wijzen, naast de **** wijze van de Voorproef nog bekijken.

Op de read-only wijze, hebt u de capaciteit om de inhoud, de markeringen, en de attributen binnen de **Auteur** of **Source** wijzen te bekijken. U kunt ook de bestandseigenschappen wijzigen.

>[!NOTE]
>
> Als beheerder, krijgt u toegang tot **de Grijsmacht ontgrendelt** eigenschap die u toestaat om een dossier te ontgrendelen dat door iemand anders wordt gesloten.

<!-- This is no more available -->
<!--
The toolbar displays the following icons for read-only access:

- Toggle Tags view
- Version History
- Version Label

Experience Manager Guides also displays a **Read only access** indicator near the version number.
 
![view read only file in author mode](images/locked-file-editor.png)

You can access the **Layout** view for read-only DITA maps. This view lets you see the DITA map and its properties but prevents edits.

>[!NOTE]
>
> Your folder-level administrative users must update *ui_config.json* so that you can harmoniously access the read-only files in the  Author, Source, and Layout modes.

 -->

## Open bestanden zoeken in Verkenner

Terwijl u een bestand opent in de Editor, biedt Experience Manager Guides de functie om het bestand te zoeken in de Verkenner. Het huidige onderwerp wordt bijvoorbeeld gezocht terwijl u het bewerkt.

U kunt de eigenschap uitzetten om van het dossier met **de plaats te bepalen bepaalt altijd van dossiers in de Ontdekkingsreiziger** optie van het **3} lusje van de Verschijning** voorkeur van de Gebruiker **.**

>[!NOTE]
>
>Van versie 2025.11.0, het plaatsen **bepaalt altijd van dossiers in de bewaarplaats** wordt anders genoemd aan **bepaalt altijd van dossiers in de ontdekkingsreiziger**. Voor de installatie op locatie blijft deze beschikbaar als Altijd bestanden zoeken in de opslagplaats tot de release van Experience Manager Guides 5.1.

**Bovenliggend onderwerp:**[ Werk met de Redacteur ](web-editor.md)
