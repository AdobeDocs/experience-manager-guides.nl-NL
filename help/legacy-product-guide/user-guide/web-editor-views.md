---
title: Weergaven van de webeditor
description: Documenten weergeven in auteur-, bron- en voorvertoningsmodus. Leer hoe u inhoud weergeeft op basis van voorwaardelijke filters, de markeringen voor wijzigingen in de track weergeeft en een onderwerp exporteert als PDF in AEM Guides.
feature: Authoring, Features of Web Editor
role: User
hide: true
exl-id: dbc27856-6903-4694-9875-77dc778c80bd
source-git-commit: ea597cd14469f21e197c700542b9be7c373aef14
workflow-type: tm+mt
source-wordcount: '1449'
ht-degree: 0%

---

# Weergaven van de webeditor {#id204GK0D0V5Z}

De Web Editor van AEM Guides ondersteunt het weergeven van documenten in drie verschillende modi of weergaven:

## Auteur

Dit is een typisch wat u ziet is wat u \ (WYSISYG \) mening van de Redacteur van het Web krijgt. U kunt onderwerp uitgeven zoals u in om het even welke regelmatige rijke redacteur zou doen. In de weergave Auteur kunt u een revisie van het document opslaan, inhoud zoeken en vervangen, element invoegen, hyperlink invoegen, inhoudsverwijzing invoegen en meer.

>[!NOTE]
>
> Wanneer u de inhoudsverwijzing gebruikt, wordt de bedoelde inhoud ook in blauwe kleur weergegeven in de weergave Auteur. De betreffende inhoud kan niet worden bewerkt.

## Source

De mening van Source toont onderliggende XML die omhoog het onderwerp maakt. Als u het prettig bent om rechtstreeks met XML te werken, moet u de Source-weergave gebruiken. U kunt in deze weergave niet alleen gewone tekstbewerkingen uitvoeren, maar u kunt ook elementen en kenmerken toevoegen met de slimme catalogus, of tekst, elementen of kenmerken zoeken en vervangen.

- Als u de slimme catalogus wilt aanroepen, plaatst u de cursor aan het einde van een elementtag op de plaats waar u het nieuwe element wilt invoegen en typt u &quot;&lt;&quot;. De redacteur toont een lijst van alle geldige elementen van XML die u bij die plaats kunt opnemen. Gebruik de pijltoetsen om het element te selecteren dat u wilt invoegen en druk op Enter. Wanneer u het afsluitende haakje &quot;\> invoert, wordt de afsluitende tag voor het element automatisch toegevoegd.

  ![](images/smart-catalog-elements.png){width="400" align="left"}

- U kunt een element ook gemakkelijk wijzigen vanuit de Source-weergave. Als u bijvoorbeeld de openingstag van een `p` -element wijzigt in `note` , wordt de afsluitende `p` -tag automatisch gewijzigd in `/note` . Als u een element vervangt door een onjuist element, wordt onmiddellijk de validatiefout weergegeven.

- Als u een kenmerk aan een element wilt toevoegen, plaatst u de cursor in de elementtag en drukt u op de spatiebalk. In de slimme catalogus wordt een lijst met geldige kenmerken voor dat element weergegeven. Selecteer het gewenste element met de pijltoetsen en druk op Enter om het element in te voegen. Als u een waarde voor het kenmerk wilt opgeven, voert u het gelijkteken \(=\) in en voert de editor automatisch de aanhalingstekens openen en sluiten &quot;&quot; in, waarin u de waarde van het kenmerk kunt opgeven.

  ![](images/smart-catalog-attribute.png){width="350" align="left"}

- In de Source-weergave is er een optie voor automatisch inspringen waarmee de XML-code opnieuw wordt gerangschikt in een indeling die presenteerbaar en gemakkelijk leesbaar is. Als u tekst selecteert en van Auteur naar Source of van Source naar Auteur overschakelt, wordt de geselecteerde tekst ook gemarkeerd in de andere weergave.
- Een andere krachtige functie in de weergave Source is de XML-validatie in uw document. Als u een document opent dat ongeldige XML bevat, wordt het geopend in de mening van Source met de informatie over ongeldige XML. In de volgende schermafbeelding wordt bijvoorbeeld de exacte informatie over de onjuiste XML gegeven in het pop-upvenster Parseerfout.

  ![](images/invalid-topic-xml.png){width="650" align="left"}

  In de bovenstaande schermafbeelding wordt een kruismarkering gebruikt om de regel met onjuiste XML te laten aanwijzen.

- Met de functie Zoeken en vervangen kunt u zoeken naar tekst, elementen of kenmerken in de weergave Source.
Voor meer details, zie **Vondst en vervang** eigenschapbeschrijving in de [ Belangrijkste toolbar ](web-editor-features.md#id#id2051EA0G05Z) sectie.

- De Source-weergave bevat veel sneltoetsen waarmee u snel door een document kunt navigeren en aan een document kunt werken. In de volgende tabel worden de ondersteunde acties en de bijbehorende sneltoetsen weergegeven:

  | Dit doen | Deze sneltoets gebruiken |
  |----------|-----------------|
  | Meerdere cursors toevoegen | **CTRL**+Linkerklik |
  | Meerdere niet-opeenvolgende tekstselecties | **CTRL** + linkerklik om tekst te slepen en te selecteren |
  | Tekst tussen regels selecteren | **Alt** + linkerklik om tekst te slepen en te selecteren |
  | Meerdere selecties ongedaan maken of de modus Volledig scherm afsluiten | **Esc** |
  | Automatisch aanvullen tonen | **CTRL** + **Ruimte** |
  | Naar de openings- of afsluitende tag van de huidige tag gaan | **CTRL** + **J** |
  | De huidige tag en de inhoud ervan uitvouwen of samenvouwen | **CTRL** + **Q** |
  | Selecteer het huidige element en de inhoud ervan | **CTRL** + **L** |
  | Het huidige element uitspringen | **Verschuiving** + **Lusje** |
  | Huidig element en inhoud verwijderen | **Verschuiving** + **CTRL** + **K** |
  | Cursor één woord naar links verplaatsen | **Alt** + **Linkerpijl** |
  | Cursor één woord naar rechts verplaatsen | **Alt** + **Juiste Pijl** |
  | Eén regel omhoog schuiven zonder de cursorlocatie te wijzigen | **CTRL** + **Omhoog Pijl** |
  | Eén regel omlaag schuiven zonder de cursorlocatie te wijzigen | **CTRL** + **Omlaag Pijl** |
  | Volledig scherm in-/uitschakelen | **F11** |
  | Nieuwe regel invoegen na het huidige element | **CTRL** + **gaat** binnen |
  | Nieuwe regel invoegen voor het huidige element | **Verschuiving** + **CTRL** + **gaat** binnen |
  | De volgende instantie van het huidige woord zoeken en selecteren | **CTRL** + **D** |
  | Het huidige element en de inhoud ervan één element omhoog verplaatsen | **Verschuiving** + **CTRL** + **omhoog Pijl** |
  | Het huidige element en de inhoud ervan één element omlaag verplaatsen | **Verschuiving** + **CTRL** + **onderaan Pijl** |
  | Het huidige element laten teruglopen in de commentaartag | **CTRL** + **/** |
  | Huidig element en inhoud dupliceren | **Verschuiving** + **CTRL** + **D** |
  | Tekst na de cursor verwijderen. Als de cursor zich vóór een openingselement bevindt, wordt het gehele element verwijderd. | **CTRL** + **K** + **K** |
  | Tekst links van de cursor op de huidige regel verwijderen. Als de cursor zich na de afsluitende tag van een element bevindt, wordt het hele element verwijderd. | **CTRL** + **K** + **Backspace** |
  | Huidige tekst omzetten in hoofdletters | **CTRL** + **K** + **U** |
  | Zet de huidige tekst om in kleine letters | **CTRL** + **K** + **L** |
  | Het huidige element naar het midden van de editor schuiven | **CTRL** + **K** + **C** |
  | Een cursor boven de huidige positie toevoegen | **CTRL** + **Alt** + **omhoog Pijl** |
  | Een cursor onder de huidige positie toevoegen | **CTRL** + **Alt** + **onderaan Pijl** |
  | Het huidige woord \(in voorwaartse richting\) recursief zoeken | **CTRL** + **F3** |
  | Het huidige woord \(in achterwaartse richting\) recursief zoeken | **Verschuiving** + **CTRL** + **F3** |


## Voorvertoning

Het openen van een onderwerp op de wijze van de Voorproef toont hoe een onderwerp zal worden getoond wanneer het door een gebruiker in hun browser wordt bekeken. In het geval van een kaart DITA, wordt een voorproef van de kaart getoond waar één enkel samengesteld document van alle onderwerpen binnen de kaart wordt getoond.

In de modus Voorbeeld hebt u de volgende functies:

- [Inhoud weergeven op basis van voorwaardelijke filters](#id2114BI00VXA)
- [Markeringen voor wijzigingen in tracks weergeven](#id2114BJ00CE8)
- [Een onderwerp exporteren als PDF](#id2114BL00B5U)

### Inhoud weergeven op basis van voorwaardelijke filters {#id2114BI00VXA}

Als u voorwaarden in uw onderwerp of kaart hebt gebruikt, worden die voorwaarden getoond in het paneel van Filters. Standaard zijn alle voorwaarden geselecteerd en wordt de volledige inhoud weergegeven. Als u een voorwaarde deselecteert, wordt de inhoud met die voorwaarde verwijderd uit de weergave. U kunt ook geconditionaliseerde inhoud markeren.

In de volgende afbeelding ziet u een onderwerp dat gebruikmaakt van twee voorwaarden: `Audience` en `Product` . De geconditionaliseerde inhoud wordt gemarkeerd met een gele achtergrond.

![](images/preview-filters.png){width="800" align="left"}

### Markeringen voor wijzigingen in tracks weergeven {#id2114BJ00CE8}

Als een document markeringen \(of visuele aanwijzingen\) voor wijzigingen in de track bevat, kunt u ook een voorvertoning van het document weergeven met of zonder deze markeringen. Tijdens het voorvertonen van een document bevat het rechterdeelvenster de opties Filters en Tekstspatiëring.

![](images/preview-tracking_cs.png){width="400" align="left"}

Er zijn drie **het Volgen** opties die u van kunt kiezen:

- **Geen Prijsverhoging**: In deze mening, worden alle toevoegingen en schrappingen goedgekeurd, en een eenvoudige mening van het document wordt voorgesteld. In deze weergave ziet u geen markeringen voor wijzigingen in de track.
- **Origineel**: In deze mening, worden alle tussenvoegsels verworpen en alle schrappingen worden hersteld terug, en dan wordt een voorproef getoond. Eenvoudig, krijgt u de originele vorm van het document alvorens u de wijze van spoorveranderingen toeliet.
- **toon Markup**: In deze mening, krijgt u alle markeringen voor opgenomen en geschrapte inhoud.

  In de volgende afbeelding ziet u een voorvertoning van een kaartbestand met markeringen:

  ![](images/preview-map-with-track-changes.PNG){width="800" align="left"}


### Een onderwerp exporteren als PDF {#id2114BL00B5U}

PDF is een van de meest gebruikte uitvoerindelingen die in elke mogelijke fase van de ontwikkelingscyclus van het document wordt gebruikt. AEM Guides biedt u de flexibiliteit om de PDF van een individueel onderwerp of een volledig kaartdossier te produceren. Met de functie Exporteren als PDF kunnen auteur, uitgever of beheerder de PDF-uitvoer voor een afzonderlijk onderwerp gemakkelijk genereren. De DITA-OT-configuraties die zijn opgeslagen in het profiel op mapniveau worden gebruikt om de PDF te genereren.

Deze functie ondersteunt de volgende functies:

- Genereer de PDF van de momenteel actieve werkkopie van een onderwerp.
- Accepteer de transformatienaam en opdrachtregelargumenten voor de DITA-OT om de PDF te genereren.
- Sla de gegenereerde uitvoer op het lokale systeem op.
- Los sleutel en inhoudsverwijzingen op die in het onderwerp worden gebruikt alvorens de output te produceren.

Voer de volgende stappen uit om een onderwerp als PDF te exporteren:

1. Open het onderwerp in de modus Voorbeeld.

1. Klik de **Uitvoer als PDF** \ (![](images/export-as-pdf-icon.svg) \) pictogram.

   Het dialoogvenster Exporteren als PDF wordt weergegeven.

   ![](images/export-as-pdf-dialog.png){width="350" align="left"}

1. *\ (Facultatief \)* specificeer de transformatienaam DITA-OT en om het even welke bevel-lijn argumenten die u wilt gebruiken.

1. Klik **Download**.

   >[!NOTE]
   >
   > Zorg ervoor dat u het pop-upvenster hebt ingeschakeld in de browserconfiguratie, anders wordt de PDF niet gedownload.

   De PDF wordt gegenereerd en geopend op een nieuw tabblad of er wordt een dialoogvenster weergegeven waarin u de PDF op uw lokale systeem kunt opslaan.


**Bovenliggend onderwerp:**[ Werk met de Redacteur van het Web ](web-editor.md)
