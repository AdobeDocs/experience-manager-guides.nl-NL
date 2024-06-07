---
title: Onderwerpen bewerken in de webeditor
description: Leer onderwerpen te bewerken in de webeditor. U kent verschillende bewerkingsfuncties om uw onderwerpbestanden in AEM hulplijnen te wijzigen.
exl-id: 8da37a81-e8c3-434f-b3f4-4723d87c2ade
feature: Authoring, Web Editor
role: User
source-git-commit: d30f05ff614693beca5d9cf7f206a36f3dadfc8b
workflow-type: tm+mt
source-wordcount: '889'
ht-degree: 0%

---

# Onderwerpen bewerken in de webeditor {#id2056B040VUI}

De Redacteur van het Web komt met een waaier van het uitgeven eigenschappen die u gemakkelijk toestaan om uw onderwerpdossiers tot stand te brengen of te wijzigen. In het algemeen, zou u de volgende stappen uitvoeren om een onderwerp in de Redacteur van het Web uit te geven.

>[!IMPORTANT]
>
> Als u een toepassingsfout terwijl het werken aan de Redacteur van het Web tegenkomt, vernieuw de pagina om verder te werken.

1. Om veranderingen in uw onderwerp aan te brengen, klik binnen de tekstgrens van het vereiste element en begin het aanbrengen uitgeeft.

1. Als u een specifiek element wilt invoegen, klikt u aan het einde van het element waarna u het nieuwe element wilt invoegen en klikt u op het pictogram van het vereiste element op de werkbalk. U kunt ook de sneltoets gebruiken `Alt+Enter` om de **Element invoegen** popup.

   Er wordt een lijst met elementen weergegeven die in het onderwerp kan worden gebruikt. AEM Gidsen doet een intelligente plaatsing van elementen volgens hun geldige plaats in het onderwerp.

   >[!NOTE]
   >
   > U kunt ook kiezen welk pictogram in de werkbalk moet worden weergegeven door het dialoogvenster `ui_config.json` bestand bevindt zich op - `/etc/designs/fmdita/clientlibs/xmleditor/`. Neem voor meer informatie over het aanpassen van functies contact op met de systeembeheerder.

1. Nadat u het document hebt bewerkt, klikt u op **Opslaan**.

   >[!NOTE]
   >
   > Als u geen wijzigingen wilt doorvoeren in AEM opslagplaats, klikt u op **Sluiten** en klik vervolgens op **Sluiten zonder opslaan** in het dialoogvenster Niet-opgeslagen wijzigingen.


## Gedeeltelijke selectie van inhoud tussen elementen

Met de hulplijnen voor Experience Managers kunt u ook inhoud selecteren over verschillende elementen. Nadat u de inhoud hebt geselecteerd, kunt u de volgende bewerkingen uitvoeren:
- Opmaak en verwijderen: de geselecteerde inhoud vet maken, cursief maken, onderstrepen of zelfs verwijderen. De inhoud van de geldige open labels wordt vervolgens samengevoegd en weergegeven onder één element. U kunt bijvoorbeeld de inhoud in een alinea selecteren en de selectie uitbreiden naar een andere alinea. Als u de geselecteerde inhoud vervolgens vet maakt, wordt alle vette inhoud van de geopende labels samengevoegd en weergegeven onder één alinea-element.

Als u de geselecteerde inhoud verwijdert, wordt de resterende inhoud na het verwijderen in de geopende tags samengevoegd.

- Omring de inhoud met een geldig element: voer de volgende stappen uit om de inhoud te laten omlopen met een geldig element:
   - Selecteer de inhoud in een element.
   - Selecteer de ![toevoegen](images/Add_icon.svg) pictogram van de secundaire werkbalk bovenaan om de **Omcirkelen met element** in. In het dialoogvenster worden de geldige elementen voor de geselecteerde inhoud weergegeven.
     >[!NOTE]
     >
     > U kunt het dialoogvenster Surround met element ook weergeven door het contextmenu van de geselecteerde inhoud te selecteren.

   - Selecteer een element in het dialoogvenster. De geselecteerde inhoud wordt ondergebracht in dat element. Als u bijvoorbeeld de inhoud in een alinea selecteert en vervolgens de optie `<note>` element uit de **Omcirkelen met element** wordt de geselecteerde inhoud onder een notitie weergegeven.\
     ![dialoogvenster element surround](./images/surround-element.png) {width="300" align="left"}

## Browser vernieuwen tijdens bewerken van bestanden

De Gidsen van de Experience Manager verleent de steun om browser te verfrissen terwijl u uw inhoud in de Redacteur van het Web uitgeeft. Met deze functie kunt u doorgaan met het bewerken van inhoud voor het geval u tijdens het werken een toepassingsfout tegenkomt. Als u de browser vernieuwt terwijl een of meer bestanden met niet-opgeslagen wijzigingen worden geopend voor bewerking, wordt u gewaarschuwd dat de niet-opgeslagen wijzigingen verloren kunnen gaan. U kunt de vernieuwingsbewerking annuleren en uw bestanden opslaan om de wijzigingen te behouden.

Zelfs bij het verfrissen van browser, worden de meningen van de linkerzijde en het juiste paneel behouden in de Redacteur van het Web. Met de hulplijnen Experience Manager wordt de laatst opgeslagen status van de bestanden hersteld die in de webeditor zijn geopend wanneer u de browser vernieuwt. De bestanden die bijvoorbeeld in het deelvenster Opslagplaats worden geopend, worden opnieuw geopend. Het kaartvenster blijft samen met de eerder geopende kaart behouden.

Het actieve onderwerp of de kaart DITA wordt opnieuw geopend in het inhoudsuitgevende gebied.

Het rechterdeelvenster wordt ook opnieuw geopend en geeft dezelfde weergave weer als vóór het vernieuwen.

## Werkkopie-indicator

AEM Hulplijnen biedt de werkkopie-indicator die aangeeft of de huidige \(werkkopie\) van het bestand al dan niet synchroon is met de opgeslagen versie. Als u wijzigingen hebt aangebracht in uw huidige kopie en uw bestand niet hebt opgeslagen, wordt een \*-markering weergegeven samen met de titel op het tabblad Bestand van het onderwerp. Deze indicator dient als herinnering om uw wijzigingen op te slaan en verdwijnt wanneer u het bestand opslaat.

![werkkopie-indicator](images/working-copy-text-update-indicator.png){width="550" align="left"}

AEM Hulplijnen geven ook aan of de laatste opgeslagen \(werkende\) kopie van het bestand al dan niet synchroon is met de opgeslagen versie. Als u enkele niet-opgeslagen wijzigingen hebt aangebracht tussen de werkkopie en de laatst opgeslagen versie, wordt een \*-markering weergegeven samen met de versiegegevens die worden weergegeven in de rechterbovenhoek van het tabblad Bestandsbeheer van het onderwerp. Deze indicator dient als herinnering voor het opslaan en maken van een versie van de huidige \(werkende\) versie van het bestand.

![Version update-indicator](images/version-update-indicator.png){width="550" align="left"}




## Een geopend bestand zoeken in de Weergave opslagplaats

Terwijl u een dossier in de Redacteur van het Web opent, verstrekt de Gidsen van de Experience Manager de eigenschap om van het dossier in de Mening van de Bewaarplaats de plaats te bepalen. Het huidige onderwerp wordt bijvoorbeeld gezocht terwijl u het bewerkt.

U kunt de functie uitschakelen om het bestand te zoeken in het dialoogvenster **Bestanden altijd zoeken in opslagplaats** van de **Weergave** tabblad van het **Gebruikersvoorkeuren**.


**Bovenliggend onderwerp:**[ Werken met de webeditor](web-editor.md)
