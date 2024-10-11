---
title: Opmerkingen bij de release | Nieuwe functies in de release van Adobe Experience Manager Guides 2024.10.0
description: Meer informatie over de nieuwe en verbeterde functies in de 2024.10.0-release van Adobe Experience Manager Guides
role: Leader
source-git-commit: 545e51cbd970aa3df01a0fe2461a2e730c0db66a
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 0%

---

# Nieuwe functies in de release van 2024.10.0 (oktober 2024)

Dit artikel behandelt de nieuwe en verbeterde functies die zijn geïntroduceerd met de release 2024.10.0 van Adobe Experience Manager Guides as a Cloud Service.

Voor de lijst van kwesties die in deze versie worden bevestigd, mening [ Vaste kwesties in de versie 2024.10.0 ](fixed-issues-2024-10-0.md).

Leer over [ verbeteringsinstructies voor de versie 2024.10.0 ](../release-info/upgrade-instructions-2024-10-0.md).


## Verbeteringen voor publiceren

De volgende verbeteringen in het publiceren van inhoud zijn aangebracht in de release 2024.10.0:




### Verbeteringen in het publiceren van inhoudsfragmenten

Experience Manager Guides biedt ook enkele nuttige verbeteringen in Content Fragments:

- Met Experience Manager Guides kunt u een onderwerp of de elementen ervan publiceren naar een inhoudsfragment.

- U kunt de Fragmenten van de Inhoud van een onderwerp van de **sectie van Output** in de **Eigenschappen van het Dossier** publiceren en bekijken.


- U kunt eenvoudig variaties in inhoudsfragmenten maken door inhoud met voorwaarden te filteren terwijl u publiceert naar een inhoudsfragment.

- Gebruik de nieuwe toewijzingsinterface om de elementen gemakkelijk te selecteren en te publiceren naar een inhoudsfragment.

Bij het publiceren van inhoudsfragmenten wordt alleen de toegewezen inhoud vervangen in plaats van het volledige inhoudsfragment te overschrijven. Met deze functie kan een inhoudsfragment gegevens uit meerdere bronnen bevatten, zoals meerdere onderwerpen of de editor voor inhoudsfragmenten.

![ voeg het fragmentmodel en toewijzingsdetails in Publish toe als de dialoog van het Fragment van de Inhoud ](assets/content-fragment-mapping.png)

Voor meer details, mening [ de Fragmenten van de Inhoud van Publish ](../user-guide/publish-content-fragment.md).


### Publish Experience Fragment varianten based on condition filters

Met Experience Manager Guides kunt u een onderwerp of de elementen ervan publiceren naar een ervaringsfragment. U kunt nu ook variabelen voor ervaringsfragmenten maken met behulp van de voorwaarde- of DITAVAL-filters en deze filters opnieuw gebruiken op verschillende kanalen of voor verschillende doelgroepen.

Leer meer over hoe te [ de Fragmenten van de Ervaring van Publish ](../user-guide/publish-experience-fragment.md).


### AEM Sites-voorinstelling opnieuw ingedeeld voor gebruiksgemak

De instellingen zijn opnieuw ingedeeld om u te helpen de uitvoervoorinstelling snel te configureren en de AEM Sites-uitvoer te genereren.
U kunt bestaande AEM Sites tot stand brengen stelt vooraf in door de **optie van de de erfeniscomponentenafbeelding van het Gebruik** in de **Nieuwe output vooraf ingestelde** dialoogdoos te selecteren.

Bekijk de **Algemene**, **Inhoud**, en **de verwijzings** lusjes van de Kaart van de kaart in AEM Sites vooraf instelt:
- **Algemeen**: Bevat de algemene configuraties om de output te produceren. U kunt het site- en uitvoerpad opgeven, bestaande uitvoerpagina&#39;s verwijderen of overschrijven, de eerder gegenereerde pagina&#39;s voor verwijderde onderwerpen verwijderen, de ontwerpsjabloon selecteren, de tijdelijke bestanden behouden en de workflow voor na de generatie opgeven.
- **Inhoud**: Bevat de montages toepasselijk op de inhoud voor outputgeneratie. U kunt de filters, de basislijn van de kaart DITA, en de meta-gegevenseigenschappen voor het publiceren selecteren.
- **verwijzingen van de Steekkaart**: Deze lijst bevat onderwerpen die verwijzingen van de dwars-kaart met werkingsgebied = &quot;peer&quot; bevatten. U kunt de het publiceren context voor een lijst van dwars-kaartverwijzingen met scope= &quot;peer&quot;aan onderwerpen specificeren beschikbaar in andere kaarten DITA. Dit tabblad wordt weergegeven als u de Experience Manager Guides-versie (UUID) gebruikt.



### Kruismapverwijzingen uit AEM Sites-voorinstellingen in de webeditor

De meest recente uitbreiding van Experience Manager Guides introduceert verwijzingen naar kruismappen in de AEM Sites-voorinstellingen van de webeditor.
Kruisverwijzingen in Experience Manager Guides helpen de navigatie van inhoud te verbeteren, het hergebruik van inhoud te vergroten en de gebruikerservaring te verbeteren.


U kunt de het publiceren context voor een lijst van dwars-kaartverwijzingen naar onderwerpen specificeren beschikbaar in andere kaarten DITA met scope= &quot;peer&quot;. Bijvoorbeeld, bevat Onderwerp 1 in Kaart A een verwijzing naar Onderwerp 2. Onderwerp 2 kan aanwezig zijn in enige of veelvoudige kaarten.  U kunt de bovenliggende kaart en een specifieke voorinstelling selecteren of de meest recente gepubliceerde uitvoer voor elke koppeling.

Als het zelfde onderwerp naar meer dan eens in een dossier wordt verwezen, dan kunt u een verschillende het publiceren context voor elke instantie toevoegen. Dit biedt meer flexibiliteit en controle over de inhoud ervan. Bijvoorbeeld, is Onderwerp 3 aanwezig in zowel Kaart B als Kaart C. Onderwerp 1 bevat twee verwijzingen naar Onderwerp 3. U kunt Kaart B als ouderkaart voor de eerste verbinding en Kaart C als ouder voor de tweede verbinding kiezen.

![ Verouderde vooraf ingestelde AEM Sites ](assets/aem-sites-legacy.png)

*specificeer de het publiceren context voor de verbonden onderwerpen van de **Verwijzingen van de kaart**lusje van **AEM Sites**vooraf ingesteld.*

Leer meer over [ AEM Sites vooraf instelt ](../user-guide/generate-output-aem-site.md).

### Optie voor het kiezen van een platte of geneste bestandshiërarchie voor HTML5-uitvoer

Nu, staat Experience Manager Guides u toe om de vlakke omslaghiërarchie voor de tijdelijke dossiers te behouden waar de volledige inhoud in HTML5 uitvoerformaat wordt gepubliceerd en in één enkele omslag wordt bewaard.
Als u er niet voor kiest om de bestandshiërarchie af te vlakken, wordt de HTML5-uitvoer gegenereerd in een geneste mappenhiërarchie. Dit houdt in dat de oorspronkelijke mapstructuur van de inhoud, met bestanden die in submappen zijn ingedeeld, in de uitvoer wordt gerepliceerd. Deze geneste maphiërarchie maakt een complexere organisatie en categorisering van bestanden mogelijk, waardoor het eenvoudiger wordt om grote gegevensvolumes te beheren en te navigeren.


Leer meer over hoe te [ HTML5 output ](../user-guide/generate-output-html5.md) produceren.


## Verbeteringen in de Editor

De volgende redacteursverhogingen zijn toegevoegd in versie 2024.10.0:

### Alleen-lezen toegang tot de modus Auteur en Source voor vergrendelde bestanden

Als een DITA- of markeringsbestand is vergrendeld of uitgecheckt door een andere gebruiker, kunt u de inhoud niet bewerken of wijzigen. Naast Voorvertoning kunt u het bestand ook als alleen-lezen bestand weergeven in de modus Auteur of Source.
Op read-only wijze, kunt u de inhoud samen met de markeringen en de attributen binnen de **Auteur** of **Source** wijze bekijken en de dossiereigenschappen uitgeven.

U kunt tot de **mening van de Lay-out** voor read-only kaarten ook toegang hebben DITA.
>[!NOTE]
>
> Uw beheerders van het omslagprofiel moeten *ui_config.json* bijwerken zodat u tot de read-only dossiers in de Auteur, Source, en wijzen van de Lay-out kunt harmonieus toegang hebben.

![ gesloten dossierredacteur ](./assets/locked-file-editor.png)
*Mening de gesloten dossiers op Auteur en de wijze van Source.*


Leer hoe te [ open gesloten dossiers in de wijzen van de Auteur en van Source ](../user-guide/web-editor-edit-topics.md#open-locked-files-in-author-and-source-modes).


### Gegroepeerde voorwaarden voor verbeterde inhoudsorganisatie

Met Experience Manager Guides kunt u nu voorwaarden groeperen en presenteren in een geneste hiërarchie, zodat u meerdere voorwaarden aan één groep kunt toevoegen. Door de voorwaarden te groeperen, kunt u hen beter organiseren en toepassen over uw inhoud.

![ voorwaarden die in een genestelde hiërarchie ](assets/conditions-nested-hierarchy.png){width="300" align="left"} worden georganiseerd

Leer meer over de **de eigenschapbeschrijving van de Voorwaarden** in de [ Linkerpaneel ](../user-guide/web-editor-features.md#id2051EA0M0HS) sectie.




