---
title: HTML5 gebruiken
description: Leer hoe u een HTML5-voorinstelling maakt via het dashboard voor de webeditor en de kaart. HTML5-uitvoervoorinstelling configureren in AEM Guides.
exl-id: b54bf3a0-7a13-41a0-ae72-cdf2caf8d974
feature: Publishing
role: User
source-git-commit: c2a97a134b9e7367689778a2a1e1f4bbead9860b
workflow-type: tm+mt
source-wordcount: '1226'
ht-degree: 0%

---

# HTML 5 {#id205BE700XO1}

De HTML5-uitvoer wordt gegenereerd in een platte maphiërarchie. Dit houdt in dat de mapstructuur die door de inhoud in de opslagplaats wordt gebruikt, niet wordt gerepliceerd in de HTML5-uitvoer. De volledige inhoud wordt gepubliceerd in de uitvoerindeling HTML5 en opgeslagen in één map. De bestandsnamen worden ook vervangen door de UUID&#39;s van de bestanden in de gegenereerde uitvoer. Het enige bestand dat geen op UUID gebaseerde bestandsnaam heeft, is het bestand index.html.

U kunt de voorinstelling HTML op twee manieren maken:

**van de Redacteur van het Web:** in het paneel van de Bewaarplaats, open het DITA kaartdossier in de Mening van de Kaart, dan in het lusje van de Output, selecteer + pictogram om tot een output vooraf ingesteld te leiden, en selecteer dan HTML5 van het type drop-down in Add vooraf ingestelde dialoog.

>[!NOTE]
>
> U kunt de methode kiezen om HTML5 te produceren gebruikend DITA-OT of FMPS \(als uw systeembeheerder het \) heeft gevormd.

In de redacteur van het Web zijn de configuraties georganiseerd onder Algemene en Geavanceerde lusjes:

**Algemeen**

Het **Algemene** lusje bevat de volgende configuraties:

- Uitvoerpad
- Argumenten DITA-OT-opdrachtregel
- Bestandsnaam
- Voorwaarden toepassen met \(als de voorwaarden voor een kaart zijn gedefinieerd\)
- Basislijn gebruiken \(als een basislijn is gemaakt voor een kaart\)
- Workflow na generatie

**Geavanceerd**

Het tabblad Geavanceerd bevat de volgende configuraties:

- Transformatienaam
- Tijdelijke bestanden behouden
- Bestandseigenschappen

Voor details, verwijs naar [ HTML5 configuratie ](#id231KJA00REJ).

**van het kaartdashboard**

Als u uitvoervoorinstellingen voor PDF wilt openen, klikt u op een DITA-toewijzingsbestand in de Assets-interface en klikt u op Voorinstellingen uitvoer. Klik vervolgens op de optie HTML5. In het dashboard van de Kaart, geeft de klik **** op de bovenkant uit om de diverse configuraties bij te werken, en klikt dan **sparen**.

**HTML5 configuratie**

De volgende opties zijn beschikbaar voor de uitvoer van HTML5:

| HTML5-opties | Beschrijving |
| --- | --- |
| Uitvoertype | Het type uitvoer dat u wilt genereren. Kies de optie HTML HTML5 om5-uitvoer te genereren. |
| Naam instellen | Geef een beschrijvende naam voor de HTML5-uitvoerinstellingen die u maakt. Bijvoorbeeld, kunt u _Interne klantenoutput_ of _eind-gebruikers output_ specificeren. |
| Argumenten DITA-OT-opdrachtregel | Geef de aanvullende argumenten op die u tijdens het genereren van uitvoer wilt laten verwerken door DITA-OT. Voor details over de bevel-lijn argumenten die in DITA-OT worden gesteund, zie [ documentatie DITA-OT ](https://www.dita-ot.org/). |
| Responsief maken met | Selecteer DITA-OT om de HTML5-uitvoer te genereren. |
| Voorwaarden toepassen met | Selecteer één van de volgende opties:<br><br>* **toegepaste niets**: Selecteer deze optie als u geen voorwaarde op de gepubliceerde output wilt toepassen.<br>* **DITAVal dossier**: Selecteer DITAVal dossier(s) om gepersonaliseerde inhoud te produceren. U kunt meerdere DITAVal-bestanden selecteren via het dialoogvenster Bladeren of door een bestandspad te typen. Gebruik het kruispictogram bij de bestandsnaam om het te verwijderen. DITAVal-bestanden worden in de opgegeven volgorde geëvalueerd, zodat de voorwaarden die in het eerste bestand zijn opgegeven voorrang hebben op de voorwaarden die in latere bestanden worden vermeld. U kunt de bestandsvolgorde behouden door bestanden toe te voegen of te verwijderen. Als het DITAVal-bestand naar een andere locatie wordt verplaatst of wordt verwijderd, wordt het niet automatisch verwijderd van het kaartdashboard. U moet de locatie bijwerken als bestanden worden verplaatst of verwijderd. U kunt de muisaanwijzer boven de bestandsnaam plaatsen om het pad te zien in de AEM opslagplaats waar het bestand is opgeslagen. U kunt alleen DITAVal-bestanden selecteren en er wordt een fout weergegeven als u een ander bestandstype hebt geselecteerd. FrameMaker Publishing Server ondersteunt geen meerdere DITAVAL-bestanden.<br>* **Vooraf ingestelde Voorwaarde**: Selecteer een voorwaarde vooraf ingesteld van drop-down om een voorwaarde toe te passen terwijl het publiceren van de output. De optie is zichtbaar als u een voorwaarde hebt toegevoegd op het tabblad Voorinstellingen voorwaarde van de DITA-kaartconsole. Om meer over vooraf ingestelde voorwaarde te weten, zie [ Voorinstellingen van het Gebruik ](generate-output-use-condition-presets.md#id1825FL004PN).<br><br> u kunt veelvoudige DITAVAL dossiers selecteren gebruikend doorbladerdialoog of door dossierweg te typen. Gebruik het kruispictogram bij de bestandsnaam om het te verwijderen. DITAVAL-bestanden worden in de opgegeven volgorde geëvalueerd, zodat de voorwaarden die in het eerste bestand zijn opgegeven voorrang hebben op de voorwaarden die in latere bestanden worden vermeld. U kunt de bestandsvolgorde behouden door bestanden toe te voegen of te verwijderen. U moet de locatie bijwerken als bestanden worden verplaatst of verwijderd. U kunt de muisaanwijzer boven de bestandsnaam plaatsen om het pad te zien in de AEM opslagplaats waar het bestand is opgeslagen. U kunt alleen DITAVAL-bestanden opslaan. Er wordt een fout weergegeven als u een ander bestand hebt geselecteerd.<br><br>**Nota**: de FrameMaker Publishing Server steunt geen veelvoudige DITAVAL dossiers. |
| Transformatienaam | Geef het type uitvoer op dat u wilt genereren. Dit is vereist als u uitvoer wilt genereren met uw eigen aangepaste plug-in, die is geïntegreerd in de DITA-OT-plug-in. Als u bijvoorbeeld XHTML-uitvoer wilt genereren, geeft u `xhtml` op. Voor een lijst van transformaties beschikbaar in DITA-OT, zie [ transformaties DITA-OT (outputformaten) ](http://www.dita-ot.org/2.3/user-guide/AvailableTransforms.html) in de Gids van de Gebruiker van OASIS DITA-OT. |
| Bestandsnaam | Geef de bestandsnaam op waarmee u de HTML5-uitvoer wilt opslaan.<br><br>**Nota**:Als u geen dossier verstrekt - noem, dan wordt de titel van de kaart DITA gebruikt om de definitieve naam van het HTML5 outputdossier te produceren. Als de kaart geen titel heeft, dan wordt de het dossiernaam van de kaart DITA gebruikt aan naam de definitieve HTML5 output. De bestandsnaam wordt ontsmet volgens de regels die in het systeem zijn geconfigureerd voor het verwerken van elk ongeldig teken. |
| Workflow na generatie uitvoeren | Wanneer u deze optie kiest, wordt een nieuwe vervolgkeuzelijst Werkstroom na generatie weergegeven met alle werkstromen die in AEM zijn geconfigureerd. U moet een werkstroom selecteren die u wilt uitvoeren nadat de werkstroom van de outputgeneratie is voltooid.<br><br>**Nota**:Voor meer informatie over het creëren van een werkschema van de douanepost-output generatie, zie _werkschema van de post-outputgeneratie aanpassen_ in installeer en vorm Adobe Experience Manager Guides as a Cloud Service. |
| Doelpad | Het pad in uw AEM opslagplaats waar de HTML5-uitvoer wordt opgeslagen. |
| Tijdelijke bestanden behouden | Selecteer deze optie om de tijdelijke bestanden te behouden die door DITA-OT worden gegenereerd. Als er fouten optreden bij het genereren van uitvoer via DITA-OT, selecteert u deze optie om de tijdelijke bestanden te behouden. U kunt die dossiers dan gebruiken om de fouten van de outputgeneratie problemen op te lossen.<br> <br> Na het produceren van de output, selecteer het **tijdelijke dossiers van de Download** ![ pictogram van de download tijdelijke dossiers ](images/download-temp-files-icon.png) om de omslag te downloaden van het PIT die de tijdelijke dossiers bevat. <br><br> **Nota**: Als de dossiereigenschappen tijdens generatie worden toegevoegd, omvatten de output tijdelijke dossiers ook a *metadata.xml* dossier die die eigenschappen bevatten. |
| Bestandshiërarchie afvlakken | Selecteer de optie om de HTML5-uitvoer te genereren in een platte maphiërarchie. De volledige inhoud wordt gepubliceerd in de indeling HTML5-uitvoer in een platte bestandshiërarchie en wordt in één map opgeslagen. <br> Als u deze optie uitschakelt, wordt de uitvoer gegenereerd in een geneste maphiërarchie en wordt de volledige mapstructuur gerepliceerd. |
| Basislijn gebruiken | Als u een basislijn voor de geselecteerde kaart hebt gecreeerd DITA, selecteer deze optie om de versie te specificeren die u wilt publiceren.<br><br> zie [ Werk met Basislijn ](generate-output-use-baseline-for-publishing.md#id1825FI0J0PF) voor meer detail. |
| Bestandseigenschappen | Selecteer de eigenschappen die u als metagegevens wilt verwerken. Deze eigenschappen worden ingesteld op de pagina Eigenschappen van de DITA-kaart of het bladwijzerbestand. De eigenschappen u van de dropdown lijst selecteert verschijnen onder het **gebied van de Eigenschappen van het Dossier 0} {.** Selecteer het kruispictogram naast de eigenschap om deze te verwijderen. <br><br>**Nota**: U kunt de meta-gegevens tot de output ook overgaan gebruikend DITA-OT het publiceren. Voor meer details zie, [ pas op de meta-gegevens aan de output over gebruikend DITA-OT ](pass-metadata-dita-ot.md#id21BJ00QD0XA). |

**Bovenliggend onderwerp:**[ Begrijpend de output stelt ](generate-output-understand-presets.md) vooraf in
