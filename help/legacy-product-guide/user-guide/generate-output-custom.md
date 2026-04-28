---
title: Aangepast
description: Learn how to create custom preset from the web editor and map dashboard. Configure a custom output preset in AEM Guides.
feature: Publishing
role: User
hide: true
exl-id: b96e6599-f8f3-491a-8b8f-fcb1e0f58aae
source-git-commit: a70b3ce942b3e69445ad1d7ba6c8f7542e0ff176
workflow-type: tm+mt
source-wordcount: '995'
ht-degree: 0%

---

# Aangepast {#id205BEF00PX0}

The Custom output presets are available for custom DITA-OT plug-ins. You can create a custom DITA-OT output preset to publish output using your custom DITA-OT plug-in.

You can create the Custom preset in two ways:

**From the Web Editor:** In the Repository panel, open the DITA map file in Map View, then in the Output tab, select the + icon to create an output preset, and then select Custom from the type drop-down in the Add preset dialog.

In de redacteur van het Web zijn de configuraties georganiseerd onder Algemene en Geavanceerde lusjes:

**Algemeen**

Het **Algemene** lusje bevat de volgende configuraties:

- Argumenten DITA-OT-opdrachtregel
- Transformatienaam
- Bestandsnaam
- Uitvoerpad
- Voorwaarden toepassen met \(als de voorwaarden voor een kaart zijn gedefinieerd\)
- Basislijn gebruiken \(als een basislijn is gemaakt voor een kaart\)
- Workflow na generatie

**Geavanceerd**

Het tabblad Geavanceerd bevat de volgende configuraties:

- Tijdelijke bestanden behouden
- Bestandseigenschappen

For details, refer to [Custom configuration](#id231KJA00REJ).

**van het kaartdashboard**

To open output presets for PDF, click on a DITA map file from the Assets UI, then click on Output Presets, and then click on the HTML5 option. In het dashboard van de Kaart, geeft de klik **** op de bovenkant uit om de diverse configuraties bij te werken, en klikt dan **sparen**.

**de configuratie van de Douane**

De volgende opties zijn beschikbaar voor de voorinstelling Aangepaste uitvoer:

| Aangepaste uitvoeropties | Beschrijving |
| --- | --- |
| Uitvoertype | Het type uitvoer dat u wilt genereren. Als u uitvoer wilt genereren met een aangepaste DITA-OT-plug-in, kiest u de optie Aangepast. |
| Naam instellen | Geef een beschrijvende naam voor de uitvoerinstellingen die u maakt. Bijvoorbeeld, kunt u _Interne klantenoutput_ of _eind-gebruikers output_ specificeren. |
| Argumenten DITA-OT-opdrachtregel | Geef de aanvullende argumenten op die u tijdens het genereren van uitvoer wilt laten verwerken door DITA-OT. Voor details over de bevel-lijn argumenten die in DITA-OT worden gesteund, zie [ documentatie DITA-OT ](https://www.dita-ot.org/). |
| Transformatienaam | Geef het type uitvoer op dat u wilt genereren. Dit is vereist als u uitvoer wilt genereren met uw eigen aangepaste plug-in, die is geïntegreerd in de DITA-OT-plug-in. Als u bijvoorbeeld XHTML-uitvoer wilt genereren, geeft u `xhtml` op. Voor een lijst van transformaties beschikbaar in DITA-OT, zie [ transformaties DITA-OT (outputformaten) ](http://www.dita-ot.org/2.3/user-guide/AvailableTransforms.html) in de Gids van de Gebruiker van OASIS DITA-OT. |
| Bestandsnaam | Specificeer het dossier - noem waarmee u de output wilt bewaren.<br><br>**Nota**: Als u geen dossier verstrekt - noem, dan wordt de titel van de kaart DITA gebruikt om de definitieve naam van het outputdossier te produceren. Als de kaart geen titel heeft, dan wordt de het dossiernaam van de kaart DITA gebruikt om de definitieve output te noemen. De bestandsnaam wordt ontsmet volgens de regels die in het systeem zijn geconfigureerd voor het verwerken van elk ongeldig teken. |
| Voorwaarden toepassen met | Selecteer één van de volgende opties:<br><br>* **toegepaste niets**: Selecteer deze optie als u geen voorwaarde op de gepubliceerde output wilt toepassen.<br>* **DITAVal dossier**: Selecteer DITAVal dossier(s) om gepersonaliseerde inhoud te produceren. U kunt meerdere DITAVal-bestanden selecteren via het dialoogvenster Bladeren of door een bestandspad te typen. Gebruik het kruispictogram bij de bestandsnaam om het te verwijderen. DITAVal-bestanden worden in de opgegeven volgorde geëvalueerd, zodat de voorwaarden die in het eerste bestand zijn opgegeven voorrang hebben op de voorwaarden die in latere bestanden worden vermeld. U kunt de bestandsvolgorde behouden door bestanden toe te voegen of te verwijderen. Als het DITAVal-bestand naar een andere locatie wordt verplaatst of wordt verwijderd, wordt het niet automatisch verwijderd van het kaartdashboard. U moet de locatie bijwerken als bestanden worden verplaatst of verwijderd. U kunt de muisaanwijzer boven de bestandsnaam plaatsen om het pad te zien in de AEM-opslagplaats waar het bestand is opgeslagen. U kunt slechts DITAVal dossiers selecteren en een fout wordt getoond als u een ander dossiertype hebt geselecteerd.<br>* **Vooraf ingestelde Voorwaarde**: Selecteer een voorwaarde vooraf ingesteld van drop-down om een voorwaarde toe te passen terwijl het publiceren van de output. De optie is zichtbaar als u een voorwaarde hebt toegevoegd op het tabblad Voorinstellingen voorwaarde van de DITA-kaartconsole. Om meer over vooraf ingestelde voorwaarde te weten, zie [ Voorinstellingen van het Gebruik ](generate-output-use-condition-presets.md#id1825FL004PN). |
| Doelpad | Het pad in uw AEM-opslagplaats waar de EPUB-uitvoer wordt opgeslagen. |
| Tijdelijke bestanden behouden | Selecteer deze optie om de tijdelijke bestanden te behouden die door DITA-OT worden gegenereerd. Als er fouten optreden bij het genereren van uitvoer via DITA-OT, selecteert u deze optie om de tijdelijke bestanden te behouden. U kunt die dossiers dan gebruiken om de fouten van de outputgeneratie problemen op te lossen.<br> <br> Na het produceren van de output, selecteer het **tijdelijke dossiers van de Download** ![ pictogram van de download tijdelijke dossiers ](images/download-temp-files-icon.png) om de omslag te downloaden van het PIT die de tijdelijke dossiers bevat. <br><br> **Nota**: Als de dossiereigenschappen tijdens generatie worden toegevoegd, omvatten de output tijdelijke dossiers ook a *metadata.xml* dossier die die eigenschappen bevatten. |
| Workflow na generatie uitvoeren | Als u deze optie kiest, wordt een nieuwe vervolgkeuzelijst Werkstroom na generatie weergegeven met alle werkstromen die in AEM zijn geconfigureerd. U moet een werkschema selecteren dat u na voltooiing van het werkschema van de outputgeneratie wilt uitvoeren.<br><br>**Nota**: Voor meer informatie over het creëren van een werkschema van de douanepost-outputgeneratie, zie _werkschema van de post-outputgeneratie aanpassen_ in installeer en vorm Adobe Experience Manager Guides as a Cloud Service. |
| Basislijn gebruiken | Als u een basislijn voor de geselecteerde kaart hebt gecreeerd DITA, selecteer deze optie om de versie te specificeren die u wilt publiceren.<br><br> zie [ Werk met Basislijn ](generate-output-use-baseline-for-publishing.md#id1825FI0J0PF) voor meer detail. |
| Bestandseigenschappen | Selecteer de eigenschappen die u als metagegevens wilt verwerken. Deze eigenschappen worden ingesteld op de pagina Eigenschappen van de DITA-kaart of het bladwijzerbestand. De eigenschappen u van de dropdown lijst selecteert verschijnen onder het **gebied van de Eigenschappen van het Dossier 0} {.** Selecteer het kruispictogram naast de eigenschap om deze te verwijderen. <br><br>**Nota**: U kunt de meta-gegevens tot de output ook overgaan gebruikend DITA-OT het publiceren. Voor meer details zie, [ pas op de meta-gegevens aan de output over gebruikend DITA-OT ](pass-metadata-dita-ot.md#id21BJ00QD0XA). |

**Bovenliggend onderwerp:**[ Begrijpend de output stelt ](generate-output-understand-presets.md) vooraf in
