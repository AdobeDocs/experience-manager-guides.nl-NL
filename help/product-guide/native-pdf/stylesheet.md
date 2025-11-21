---
title: Systeemeigen PDF-publicatiefunctie | Werken met algemene inhoudsstijlen
description: Leer hoe u gebruiksstijlen maakt en stijlen voor uw inhoud maakt.
exl-id: 42ba7347-d81d-45d9-9627-8d164e4f9539
feature: Output Generation
role: Admin
level: Experienced
source-git-commit: 6e23f52fc9124d0f07f8108da1b5fe574f553469
workflow-type: tm+mt
source-wordcount: '3778'
ht-degree: 0%

---

# Werken met algemene inhoudsstijlen {#work-with-common-styles}

Een stijlpagina bevat de definities van stijlen voor de elementen die in uw PDF-uitvoer worden gebruikt. U kunt ervoor kiezen om met de voorbeeldopmaakmodellen te werken of nieuwe opmaakmodellen te maken. In de meeste gevallen kunt u snel aan de slag door een kopie van de OOTB-voorbeeldstijlpagina te maken.

De stijleneditor is een WYSIWYG-editor die alle complexe onderdelen van een CSS-code achter de gebruikersinterface verbergt. Met de stijleditor kunt u de stijlen voor de elementen van uw keuze gemakkelijk en zeer snel aanpassen. De stijlen worden onder de volgende koppen gecategoriseerd:

* Stijlen kop
* Alineastijlen
* Tekenstijlen
* Hyperlinkstijlen
* Afbeeldingsstijlen
* Lijststijlen
* Tabelstijlen
* Div-stijlen
* Paginastijlen
* Overige stijlen

Wanneer het werken met gestructureerde inhoud DITA, is de stijlafbeelding voor de meeste elementen DITA op zijn plaats in het standaardstijlblad. Als u met standaard-DITA-elementen werkt, kunt u hun uiterlijk wijzigen door de stijldefinitie rechtstreeks te wijzigen. Deze stijldefinities zijn beschikbaar onder de categorie Andere stijl. Voor meer details, zie [&#x200B; Werk met andere stijlen &#x200B;](#other-styles) later in dit onderwerp.

In de volgende secties worden de meest gebruikte stijlinstellingen in de vorm van voorbeelden besproken.

>[!NOTE]
>
>In de volgende voorbeelden wordt aangenomen dat u werkt met het voorbeeldstijlblad dat bij het product wordt geleverd.

## Werken met kopstijlen {#heading-styles}

Met de kopstijlen worden alle basisstijlen ingekapseld voor de koppen die in de inhoud worden gebruikt. OOTB u zult 6 stijlen van de basisrubriek en een kopstijl voor het onderwerp/het hoofdstuk en de titelrubriek van het bijlage krijgen. In een gestructureerd document, vertegenwoordigt H1 de titel van het onderwerp of van het hoofdstuk en H2 door H6 worden gebruikt voor subonderwerpen of secties binnen een onderwerp/hoofdstuk. Deze hiërarchie van koppen wordt automatisch toegepast op uw inhoud wanneer de overeenkomstige rubriek wordt gevonden.

>[!NOTE]
>
>U kunt uw eigen stijlen van de douanekop tot stand brengen en die kunnen in uw inhoud worden gebruikt gebruikend de outputklasse. Voor meer details, zie Stap 4 in [&#x200B; de paginarichting van het Gebruik en meningsomwenteling &#x200B;](design-page-layout.md#page-orientation-rotation) voorbeeld.

### Aangepaste koppen op hoofdstukniveau maken {#create-chapter-level-heading}

In een boek (of een boekenkaart), werkt u met Hoofdstuk. De stijlen van de basiskop zijn zodanig ontworpen dat ze zonder aanpassingen op hoofdstukniveau worden toegepast. Als u echter speciale koppen voor uw inhoud wilt maken, moet u die koppen maken. De standaardkop `h1.chapter` wordt bijvoorbeeld toegepast op de titel van het hoofdstuk. Als u de hoofdstuktitel in een andere stijl wilt weergeven, moet u de stijl `h1.chapter` aanpassen. Op dezelfde manier kunt u aangepaste stijlen voor subkoppen in uw hoofdstuk maken. Bijvoorbeeld, als u een douanestijl voor alle 2 <sup> en </sup> en 3 <sup> de 3 </sup> niveaurubrieken in uw hoofdstuk wilt tot stand brengen, dan moet u een nieuwe stijl als `h2.chatper` en `h3.chatper` tot stand brengen.

Aangezien de functie Native PDF Publishing de basisstijldefinities bevat voor de meest gebruikte stijlen, wordt de standaardstijl toegepast op de inhoud, zelfs als u per ongeluk een stijl verwijdert. Als er bijvoorbeeld geen stijldefinitie voor h2-stijl voorkomt in uw stijlpagina, wordt met de functie Native PDF Publishing een basisstijl toegepast op h2-inhoud.

In dit voorbeeld maken we een hoofdstukstijl op het tweede niveau:

1. Open de vereiste stijlpagina voor bewerking.
   >[!NOTE]
   >
   >Zie [&#x200B; een vooraf bepaalde of nieuwe stijl &#x200B;](components-pdf-template.md#customize-style) sectie aanpassen voor het openen van een stylesheet voor aanpassing of het uitgeven.

1. In de **lijst van Stijlen**, breid de **Stijlen van de Kop** uit.
1. Klik op **Stijlen van de Kop** met de rechtermuisknop aan en kies **Nieuwe Stijl**.
1. In *voeg de dialoog van de Stijl* toe, houd de **naam van de Markering** als `h2` en ga `chapter` in het **de naamgebied van de Klasse** in.
1. Klik **Gedaan**.

Er wordt een nieuwe kopstijl met de naam `h2.chapter` gemaakt en toegevoegd onder de lijst Kopstijlen.

Nadat u een stijl hebt gemaakt, kunt u de vereiste eigenschappen van de stijl aanpassen met de stijleditor.

### Koppen met automatische nummering maken {#auto-number-heading}

Één van de het meest algemeen gebruikte outputstijlen is autonumbered rubrieken. Deze rubrieken vertegenwoordigen het hoofdstukaantal, onderwerp en subonderwerpaantallen. De auto-aantalrubrieken zijn verschillend van de lijststijlen waar een lijst van punten binnen een onderwerp auto-aantallen wordt toegewezen.

In dit voorbeeld zullen we de koppen van niveau 1 tot niveau 3 aanpassen om automatische getallen in verschillende indelingen te gebruiken.

1. Open de vereiste stijlpagina voor bewerking.

   >[!NOTE]
   >
   >Zie [&#x200B; een vooraf bepaalde of nieuwe stijl &#x200B;](components-pdf-template.md#customize-style) sectie aanpassen voor het openen van een stylesheet voor aanpassing of het uitgeven.

1. In de **lijst van Stijlen**, breid de **Stijlen van de Kop** uit.

1. Selecteer de **h1** stijl van de lijst.
De eigenschappen voor de h1-stijl worden samen met de voorvertoning weergegeven in het deelvenster Eigenschappen.

   >[!NOTE]
   >
   >In het deelvenster Voorvertoning krijgt u een real-time weergave van alle stijtupdates die u op elk element toepast.

1. Selecteer het **Autonumber** bezit.

   De stijlen die u op de auto-aantallijst kunt toepassen worden getoond onder het bezit Autonumber.

1. Stel de volgende eigenschappen in:
   * **Stijl**: Uitgezocht van een brede waaier van scènespecifieke of generische nummeringsstijlen. U kunt stijlen kiezen zoals Arabisch-Indic, Devanagari, Georgisch, Decimaal, Lower-Alpha en meer. Selecteer `upper-alpha` voor het huidige voorbeeld.

   * **Formaat**: Het standaardformaat wordt geplaatst aan `<x>`, waar de `x` waarde met de nummeringsStijl wordt vervangen die u in het bezit van de Stijl selecteerde. Als u bijvoorbeeld de stijl `decimal` (1) hebt geselecteerd, wordt de waarde van `x` auto-increment voor elke instantie van de stijl `h1` gebruikt en wordt deze waarde ingesteld op 2, 3, enzovoort. U kunt ook aangepaste tekst in het veld toevoegen om de kopstijl op te maken. Als u bijvoorbeeld wilt dat alle h1-koppen een voorvoegsel `Chapter` hebben, moet u dit veld instellen als `Chapter <x>` .

   * **Teken van het Tussenvoegsel**: Als u om het even welk speciaal karakter in het Formaat wilt toevoegen, dan klik het Teken van het Tussenvoegsel (<img src="./assets/insert-chars.png" width="25"> ). Selecteer het gewenste teken dat u in de stijlindeling wilt toevoegen en klik op Invoegen. Er zijn verschillende typen speciale tekens die u kunt kiezen in de vervolgkeuzelijst Categorie selecteren. In ons voorbeeld selecteert u het rechter aanwijsteken voor dubbele hoek in de categorie Leestekens.

     <img src="./assets/insert-special-chars.png" width="400">


   * **Nummering van het Begin van**: Als u de nummering van een specifiek aantal wilt beginnen, dan die waarde verstrekken. Voor ons voorbeeld, houd de standaardwaarde van 1.

   * **Inspringen**: Als u de rubriek wilt inspringen, dan moet u de Inspringing waarde plaatsen. Stel het bijvoorbeeld in op 0 px.

     >[!NOTE]
     >
     >U kunt de waarde invoeren in px (pixels), pt (punten), rem, em, % (percentage) of in (inches) eenheden.

   * **Breedte van de Prefix**: Dit is het gebied dat door het auto-aantalformaat bezet is. De stijl wordt automatisch ingesteld op een grootte die gemakkelijk geschikt is voor de geselecteerde stijlindeling. Als u de grootte wilt vergroten, kunt u de standaardwaarde vervangen.

     Wanneer u deze waarde handmatig instelt, wijzigt u de andere eigenschappen die van invloed zijn op de breedte. Bijvoorbeeld, verander de doopvontgrootte, het formaat met prefix (Hoofdstuk) of een achtervoegsel (:), plaats de maximumwaarde in het *Nummering van het Begin van* bezit, en de diverse doopvonteigenschappen om omhoog met de optimale grootte te komen.

     Voor ons voorbeeld, houd de standaardwaarde.

   * **het Uit elkaar plaatsen**: Specificeer het horizontale en verticale uit elkaar plaatsen. Behoud de standaardwaarden voor ons voorbeeld.

     Met de bovenstaande aanpassingen wordt de stijl aangepast zoals hieronder wordt weergegeven:

     <img src="./assets/h1-style-custmization.png" width="500">

   * **pas het Formatteren op** toe: De eigenschappen onder de Herfstnummeringscategorie zullen u helpen de nummeringsstijl bepalen. Als u de nummeringsstijl of de inhoud van de kopindeling verder wilt aanpassen, kiest u Nummering of Alinea in dit veld. Als u Nummering kiest, worden wijzigingen in lettertype, rand, layout en andere categorieën alleen toegepast op de nummeringsstijl in de kop. Als u echter Alinea kiest, worden de wijzigingen toegepast op de inhoud van de kop en niet op de nummeringsstijl.

   Gebruik de volgende instellingen om een uitvoer te genereren die in de volgende schermafbeelding wordt getoond:

   | **Stijl van de Kop** | **Bezit** | **Waarde** | **Extra Commentaren** |
   | :- | :- | :- | :- |
   | h1 | Stijl | Decimaal | Deze eigenschappen vallen onder de categorie Autonumber |
   |  | Indeling | `Capter <x>:` |  |
   |  | Voorvoegselbreedte | 160 px |  |
   |  | Font > Text Alignment | Links | Zorg ervoor dat Opmaak toepassen op is ingesteld op Nummering |
   | h2 | Stijl | Decimaal | Deze eigenschappen vallen onder de categorie Autonumber |
   |  | Indeling | `Section <x>:` |  |
   |  | Voorvoegselbreedte | 125 px |  |
   |  | Font > Text Alignment | Links | Zorg ervoor dat Opmaak toepassen op is ingesteld op Nummering |
   | h3 | Stijl | Decimaal | Deze eigenschappen vallen onder de categorie Autonumber |
   |  | Niveau invoegen | 2 |  |
   |  | Indeling | `Section <2>.<x>:` |  |
   |  | Voorvoegselbreedte | 125 px |  |
   |  | Font > Text Alignment | Links | Zorg ervoor dat Opmaak toepassen op is ingesteld op Nummering |

   <img src="./assets/auto-number-output.png" width="500">

## Werken met alineastijlen {#paragraph-style}

U kunt een alineastijl maken om speciale opmaak toe te passen op een hele alinea. Met de pseudo-klasse kunt u echter een stijl alleen op een bepaald deel van de tekst toepassen. In het volgende voorbeeld maken we een alineastijl die de initiaalstijl gebruikt.

### De stijl van de initiaal maken {#drop-cap-style}

In tijdschriften wordt een initiaal (of een vervallen hoofdletter) gebruikt en in literaire documenten waarin het eerste teken van een alinea of sectie een speciale opmaak krijgt. Met de functie Native PDF Publishing kunt u hetzelfde effect bereiken.

In het volgende voorbeeld wordt een initiaalstijl gemaakt:

1. Open de vereiste stijlpagina voor bewerking.

   >[!NOTE]
   >
   >Zie [&#x200B; een vooraf bepaalde of nieuwe stijl &#x200B;](components-pdf-template.md#customize-style) sectie aanpassen voor het openen van een stylesheet voor aanpassing of het uitgeven.

1. In de **lijst van Stijlen**, breid de **Stijlen van de Paragraaf** uit.

1. Klik op de **Stijl van de Paragraaf** met de rechtermuisknop aan en kies **Nieuwe Stijl**.

1. In *voeg de dialoog van de Stijl* toe, houd de **naam van de Markering** als p en in het **Pseudo** **gebied van de Klasse**, uitgezocht `::first-letter`.

1. Klik **Gedaan**.

   Een nieuwe genoemde paragraafstijl `::first-letter` wordt gecreeerd en onder de **2&rbrace; lijst van de Stijlen van de Paragraaf toegevoegd &lbrace;toegevoegd.**

1. Selecteer `::first-letter` onder de stijl p en stel de volgende eigenschappen in:

   * **Doopvont**: Plaats de gewenste doopvont voor de eerste brief in uw paragraaf. Stel de lettertypefamilie bijvoorbeeld in op krompen, tekendikte op 500, tekengrootte op 30 pt en kies een lettertypekleur.

   * **Lay-out**: Plaats de verticale groepering van de tekst rond de dalingsGLB stijl. In ons voorbeeld wordt de verticale uitlijning ingesteld op Onder.

Aangezien de tag `p` wordt toegewezen aan het element `<p>` in DITA, hoeft u deze stijl niet expliciet toe te voegen met het kenmerk outputclass. Overal in de inhoud wordt een `<p>` -element gebruikt, wordt de initiaalstijl er automatisch op toegepast. In de volgende schermafbeelding zijn de titel van het hoofdstuk, de korte beschrijving en de definitielijst niet opgemaakt met de initiaalstijl. Alleen de alineastijl wordt opgemaakt met de initiaalstijl:

<img src="./assets/char-style-drop-cap.png" width="500">

## Werken met tekenstijlen {#char-style}

Met behulp van de tekenstijlen kunt u stijlen maken voor het opmaken van tekens of woorden binnen de inhoud. U kunt bijvoorbeeld een tekenstijl voor inline code of bestandsnaam maken of een stijl met meerdere opmaakindelingen voor geselecteerde inhoud.

### Een inline-tekenstijl maken {#inline-char-style}

Het opmaken van inline-tekens of woorden in een alinea komt veel voor. Bij het maken van een inline stijl zijn twee taken betrokken: eerst een nieuwe stijl in het stijlblad maken en vervolgens de stijl in de inhoud toepassen met het kenmerk `outputclass` .

In het volgende voorbeeld wordt een inline tekenstijl gemaakt:

1. Open de vereiste stijlpagina voor bewerking.

   >[!NOTE]
   >
   >Zie [&#x200B; een vooraf bepaalde of nieuwe stijl &#x200B;](components-pdf-template.md#customize-style) sectie aanpassen voor het openen van een stylesheet voor aanpassing of het uitgeven.

1. In de **lijst van Stijlen**, breid de **Stijlen van het Karakter** uit.

1. Klik op de **Stijl van het Karakter** met de rechtermuisknop aan en kies **Nieuwe Stijl**.

1. In de Add dialoog van de Stijl, houd de **naam van de Markering** als spanwijdte en ga `BoldItalic` op het **de naamgebied van de Klasse** in.

   <img src="./assets/create-char-style.png" width="400">

1. Klik **Gedaan**.

   Er wordt een nieuwe tekenstijl met de naam code gemaakt en toegevoegd onder de lijst Tekenstijlen.

1. Selecteer `span.BoldItalic` van de **lijst van de Stijl van het Karakter**, en plaats de volgende eigenschappen:

   * **Doopvont**: Alle doopvont-verwante eigenschappen kunnen van deze sectie worden aangepast. Standaard zijn er enkele lettertypen die bij het product zijn gebundeld. U kunt het gewenste lettertype voor de tekenstijl kiezen. Voor ons voorbeeld, plaats de Familie van de Doopvont aan *Serif,* en selecteer *Vet* en *Cursief* in het bezit van de Stijl van de Doopvont. U kunt ook andere lettertype-eigenschappen aanpassen, zoals Dikte lettertypen (zoals vet, lichter), Tekstdecoratie (zoals onderstrepen, onderstrepen), Tekengrootte, Lettertypekleur, Tekstuitlijning, enzovoort.

     >[!NOTE]
     >
     >U kunt ook lettertypen toevoegen aan uw sjabloon. Deze lettertypen worden opgeslagen in het gedeelte Bronnen van uw sjabloon. Voor meer details over het toevoegen van doopvonten en het werken met Middelen, zie [&#x200B; Werk met middelen &#x200B;](components-pdf-template.md#work-with-resources).

   * **Lay-out**: U kunt de lay-out-related eigenschappen zoals Hoogte en Breedte, Marge, het Opvullen, Uitlijning, en meer plaatsen.

   * **Achtergrond**: De eigenschappen van de Achtergrond staan u toe om de achtergrondkleur van een bepaalde stijl te formatteren. U kunt de achtergrondkleur of afbeelding voor elke stijl definiëren.

Nadat u de inline tekenstijl hebt gemaakt, moet u deze toepassen in de inhoud. Als u de inline-codestijl wilt toepassen, gaat u naar de bronweergave en voegt u het kenmerk `outputclass` toe in de gewenste inhoud:

`outputclass="BoldItalic"`

In het volgende voorbeeld wordt de indeling Vet-cursief weergegeven die op verschillende plaatsen in de actieve tekst wordt toegepast:

<img src="./assets/char-format-applied.png" width="500">

## Lijststijl aanpassen {#custom-list-style}

De lijststijlen bevatten de standaardstijlinstellingen voor de geordende en ongeordende lijsten. U kunt deze lijststijlen gemakkelijk aanpassen om aan uw documentatievereisten te voldoen.

In het volgende voorbeeld wordt de stijl van de genummerde of geordende lijst aangepast:

1. Open de vereiste stijlpagina voor bewerking.

   >[!NOTE]
   >
   >Zie [&#x200B; een vooraf bepaalde of nieuwe stijl &#x200B;](components-pdf-template.md#customize-style) sectie aanpassen voor het openen van een stylesheet voor aanpassing of het uitgeven.

1. In de **lijst van Stijlen**, breid de **Stijlen van de Lijst** uit.

1. Selecteer de **ol** stijl van de lijst.

   De eigenschappen voor de oliestijl worden samen met de voorvertoning weergegeven in het deelvenster Eigenschappen.

   <img src="./assets/list-style-default.png" width="500">

1. Selecteer de **Geavanceerde het Formatteren** optie.

   Er wordt een bevestigingsbericht weergegeven.

1. Klik **ja** op het *Bevestigings* bericht om de **Geavanceerde het Formatteren** eigenschappen te openen.

   De volgende eigenschappen zijn standaard beschikbaar:

   * **Niveau**: Door gebrek, zijn er 6 niveaus van genummerde lijsten. Het niveau dat u in deze drop-down controles selecteert de stijlveranderingen op het geselecteerde niveau en alle verdere niveaus. Als u bijvoorbeeld niveau 4 selecteert, worden alle stijlwijzigingen die u toepast, ingesteld op niveaus 4, 5 en 6.

   * **het Type van Stijl van de Lijst**: Er zijn een aantal lijst nummeringsstijlen die u van kunt kiezen. De lijst bevat landspecifieke en generieke nummeringsstijlen die worden gebruikt om een genummerde lijst te maken. Sommige lijststijltypen zijn Arabisch, Cambodjaans, Devanagari, Ethiopic, Hangul, Hebreeuws, Japans, Koreaans, Eenvoudig Chinees, Urdu en meer.

   Verder kunt u met de volgende eigenschappen voor Geavanceerde opmaak werken:

   * **Formaat van het Aantal**: Het standaardformaat wordt geplaatst aan `<x>`, waar de `x` waarde met de nummeringsStijl wordt vervangen die u in het bezit van het Type van Stijl van de Lijst selecteerde. Als u bijvoorbeeld de stijl `decimal` (1) hebt geselecteerd, wordt de waarde van `x` automatisch verhoogd voor elke instantie van het lijstelement en de waarde 2, 3 enzovoort. U kunt ook aangepaste tekst in het veld toevoegen om de lijststijl op te maken. Bijvoorbeeld, als u alle eerste-niveaulijststijlen een achtervoegsel &quot;`)`&quot;wilt hebben, dan moet u dit gebied voor eerste-niveaulijststijl als &quot;`<x>)`&quot;plaatsen.

   * **Teken van het Tussenvoegsel**: Als u om het even welk speciaal karakter in het Formaat van het Aantal wilt toevoegen, dan klik het Teken van het Tussenvoegsel (<img src="./assets/insert-chars.png" width="25"> ). Selecteer het gewenste teken dat u in de stijlindeling wilt toevoegen en klik op Invoegen. Er zijn verschillende typen speciale tekens die u kunt kiezen in de vervolgkeuzelijst Categorie selecteren.

   * **Niveau van het Tussenvoegsel**: U kunt het aantal van om het even welke voorafgaande niveaus in uw aantalformaat omvatten. Als u bijvoorbeeld de getalnotatie van het 5e niveau wilt opnemen in de getalnotatie van het 6e niveau, kiest u 5 in de vervolgkeuzelijst Niveau invoegen. Let op: in de vervolgkeuzelijst Niveau invoegen worden alleen de nummers van de voorafgaande niveaus weergegeven en niet het volgende niveau. Als u bijvoorbeeld op niveau 3 werkt, worden in de lijst Niveau invoegen alleen niveaus 1 en 2 weergegeven.

     <img src="./assets/list-insert-level.png" width="400">

     U kunt ook de nummeropmaak wijzigen en zo nodig de lijstwaarden weergeven. Bijvoorbeeld, wanneer u een genestelde nummeringsstijl voor niveau 3 gebruikt, dan kunt u het als &quot;`<2>.<x>))`&quot;formatteren. Dit toont lijst nummer 2, gevolgd door een punt, gevolgd door lijst nummer 3 en vervolgens twee haakjes, als `2.3))` .

   * **Inspringen**: Als u de lijst wilt inspringen, dan moet u de Inspringing waarde plaatsen. Wijzigingen in de inspringing kunnen worden gecontroleerd in het deelvenster Voorvertoning en aangepast.

     >[!NOTE]
     >
     >U kunt de waarde invoeren in px (pixels), pt (punten), rem, em, % (percentage) of in (inches) eenheden.

   * **Breedte van de Prefix**: Dit is het gebied dat door het Formaat van het Aantal bezet is. Deze wordt automatisch ingesteld op een grootte die gemakkelijk geschikt is voor de geselecteerde indeling. Als u de grootte wilt vergroten, kunt u de standaardwaarde vervangen.

     Wanneer u deze waarde handmatig instelt, wijzigt u de andere eigenschappen die van invloed zijn op de breedte. Wijzig bijvoorbeeld de tekengrootte, de opmaak met voor- of achtervoegsel en de verschillende lettertype-eigenschappen om de optimale grootte te bereiken.

   * **het Tussenruimte**: Specificeer het horizontale uit elkaar plaatsen tussen het formaat van het lijstaantal en de inhoud. De verticale spatiëring bepaalt de tussenruimte tussen de twee lijstitems.

     De volgende schermafbeelding toont de aangepaste geordende lijst voor elk niveau:

     <img src="./assets/list-number-format-final.png" width="500">

## Werken met tabelstijl {#table-styles}

Gebruikend stylesheets, kunt u *n* aantal lijststijlen ontwerpen. Met behulp van de tabelstijlen kunt u ontwerpen hoe de volledige tabel, een bepaalde rij of kolom. Met controle bij cel-vlakke het stileren, kunt u zeer presenteerbare lijststijlen tot stand brengen.

In het volgende voorbeeld ziet u hoe u een tabelstijl en de verschillende opties voor tabelopmaak kunt maken die u kunt aanpassen:

1. Open de vereiste stijlpagina voor bewerking.

   >[!NOTE]
   >
   >Zie [&#x200B; een vooraf bepaalde of nieuwe stijl &#x200B;](components-pdf-template.md#customize-style) sectie aanpassen voor het openen van een stylesheet voor aanpassing of het uitgeven.

1. In de **lijst van Stijlen**, klik op de **Stijl van de Lijst** met de rechtermuisknop aan en kies **Nieuwe Stijl**.

1. In *voeg de dialoog van de Stijl* toe, houd de **naam van de Markering** als `table` en ga `double-border` in het **de naamgebied van de Klasse** in.

1. Klik **Gedaan**.

   Er wordt een nieuwe tabelstijl met de naam `table.double-border` gemaakt en toegevoegd onder de lijst Tabelstijlen.

1. Selecteer `table.double-border` van de **lijst van de Stijlen van de Lijst**, en plaats de volgende eigenschappen:

   * **pas het Formatteren op** toe: U kunt verkiezen om het stijlformatteren op de volledige lijst, oneven/even rijen of kolommen, of eerste/laatste rij of kolom toe te passen.

     >[!NOTE]
     >
     >De volgende montages zijn beschikbaar onder de **Algemene** sectie wanneer **het Formatteren op** wordt geplaatst aan **Gehele Lijst**.

   * **Wrapping van de Tekst**: Selecteer hoe te om tekst rond de lijst te verpakken. Dit is handig wanneer de tabel zich in een ander element op blokniveau bevindt en de tabel samen met andere inhoud in het blokelement moet worden gerenderd. De het verpakken opties zijn *verlaten* of *recht* gericht, of *niets*.

   * **de Samenvouwen van de Grens**: Selecteer de verschijning van de lijstgrens. Als u samenvouwen selecteert, wordt er slechts één randlijn tussen de tabelcellen getekend. Voor afzonderlijke stijlen is de rand echter zichtbaar rond elke cel met extra opvulling.

     <img src="./assets/table-style-collapse-separate.png" width="500">

   * **Grensspatiëring**: Deze instelling is alleen beschikbaar wanneer Rand samenvouwen is ingesteld op Afzonderlijk. Met deze instelling kunt u de verticale en horizontale afstand tussen de celranden opgeven.

     <img src="./assets/table-border-spacing.png" width="500">

     >[!NOTE]
     >
     >De volgende montages zijn beschikbaar onder de **1&rbrace; sectie van de Cel wanneer** Formatterend op **wordt geplaatst aan** Gehele Lijst **.**

   * **het Opvullen**: Specificeer binnen het opvullen tussen lijstcellen. U kunt verschillende opvullingswaarden opgeven voor de boven-, onder-, linker- en rechterzijde.

   * **Verticale Uitlijning**: Specificeer de verticale groepering voor celinhoud. Beschikbare opties zijn: Boven, Midden en Onder.

   * **Kant van de Grens, Stijl, Kleur, Breedte, Straal:** specificeer de op grens betrekking hebbende eigenschappen. U kunt ervoor kiezen om alleen randen te hebben aan bepaalde zijden, zoals Links of Rechts. De randstijl geeft een overzicht van de beschikbare randstijlen, zoals Effen, Onderbroken, Dubbele lijn en nog veel meer. Geef de randkleur op met het kleurenpalet. U kunt de randbreedte opgeven in px, pt, rem, em, % en in eenheden. De straal bepaalt de kromme om cirkelhoeken te maken.

   De andere eigenschappen onder Lettertype, Rand, Lay-out, Paginering, en Achtergrond worden verklaard onder andere voorbeelden in dit onderwerp. Afhankelijk van uw selectie in **pas het Formatteren op** bezit toe, kunt u deze waarden op de volledige lijst of geselecteerde rijen of kolommen toepassen.

   Hieronder ziet u een voorbeeld van een voorbeeldtabel met verschillende rijen die op een andere manier zijn opgemaakt:

   <img src="./assets/table-final-design.png" width="500">

## Werken met andere stijlen {#other-styles}

Als u met gestructureerde (DITA) inhoud werkt, dan zult u merken dat bijna alle elementen DITA een stijlafbeelding in het standaardstijlblad hebben. Bijvoorbeeld, wordt de stijl van een `<shortdesc>` element bepaald onder **Andere Stijl** > **.shortdesc** stijldefinitie. U kunt al deze stijlen eenvoudig aanpassen en ze worden automatisch toegepast in de PDF-uitvoer die wordt gegenereerd op basis van uw gestructureerde inhoud. Dit betekent dat u, in tegenstelling tot andere aangepaste stijlen, geen attribuut `outputclass` hoeft toe te voegen aan de inhoud voor deze stijlen.

Als u een stijldefinitie voor om het even welk element wilt tot stand brengen dat niet door gebrek beschikbaar is of u een douaneelement hebt, dan kunt u het gemakkelijk tot stand brengen in het stijlblad. Het enige punt dat u moet overwegen, is het maken van de stijl met dezelfde naam als de naam van het gestructureerde element.

In het volgende voorbeeld, zullen wij de titel (`wintitle`) stijl van een nieuw venster creëren:

1. Open de vereiste stijlpagina voor bewerking.

   >[!NOTE]
   >
   >Zie [&#x200B; een vooraf bepaalde of nieuwe stijl &#x200B;](components-pdf-template.md#customize-style) sectie aanpassen voor het openen van een stylesheet voor aanpassing of het uitgeven.

1. In de **lijst van Stijlen**, breid **Andere Stijlen** uit.

1. Klik op de **Andere Stijl** met de rechtermuisknop aan en kies **Nieuwe Stijl**.

1. In *voeg de dialoog van de Stijl* toe, houd de **naam van de Markering** als *leeg* en ga `wintitle` in het **de naamgebied van de Klasse** in.

   Aangezien `wintitle` een herkende DITA-elementnaam is, wordt de stijldefinitie ervan automatisch toegewezen aan het `<wintitle>` -element in de bron.

1. Klik **Gedaan**.

   Een nieuwe stijl genoemd `.wintitle` wordt gecreeerd en onder de **Andere 2&rbrace; lijst van Stijlen &lbrace;toegevoegd.**

1. Selecteer .wintitle van de **Andere lijst van Stijlen**, en plaats de eigenschappen zoals vereist.

In de volgende schermafbeelding wordt de stijl van de venstertitel weergegeven die wordt toegepast op de tekst &quot;Primair besturingselement&quot;.

<img src="./assets/other-style-wintitle.png" width="500">


## Een unieke stijl voor een lay-out van één pagina definiëren

Bij het publiceren van de eigen PDF-uitvoer worden alle stijlen samengevoegd in de uiteindelijke PDF. Het is van cruciaal belang dat u een unieke stijl toewijst aan elke sjabloon in de CSS.
Gebruik verschillende CSS-stijlnamen om specifieke lettertypen en stijlen toe te passen op verschillende secties van een PDF. U kunt bijvoorbeeld het gewenste lettertype voor de omslagpagina definiëren met behulp van de volgende CSS.

```css
...
[data-page-layout="Front"] * { 
    font-size: 18pt; 
}  
...
```


Voor de rest van het document wordt het standaardlettertype gebruikt dat u voor de body-tag in `content.css` of `layout.css` hebt opgegeven. Dit zorgt ervoor dat stijlen niet worden samengevoegd en dat elke sectie zijn voorgenomen ontwerp behoudt. Als u verschillende tekengrootten wilt gebruiken, maakt u daarvoor specifieke stijlen.

U kunt bijvoorbeeld de volgende stijlen definiëren om tekengrootte 18 te definiëren op de voorste omslagalinea&#39;s en tekengrootte 11 pt voor de achterste omslagpagina:

```css
[data-page-layout="Front"] p { //For all paragraphs inside Front page
  font-size: 18pt; 
} 
  
[data-page-layout="Back"] p { //For all paragraphs inside Back page
  font-size: 11pt; 
}
```

>[!NOTE]
>
> In het vorige voorbeeld zijn &quot;Voor&quot; en &quot;Terug&quot; de voorbeeldnamen van de lay-outbestanden die u in de sjablonen kunt gebruiken.


## Aangepaste CSS-stijl definiëren voor voor- en achtervoegselinhoud

Als u aangepaste CSS-stijlen definieert, krijgen deze de eerste prioriteit tijdens het genereren van de eigen PDF-uitvoer.
In de volgende standaard CSS-stijl worden zowel voor- als achtervoegselinhoud verborgen.

```css
...
.prefix-content, .suffix-content{
    display: none;
} 
...
```

Als u deze voorvoegsels wilt toestaan binnen het element `<note>` , neemt u de volgende CSS op in uw `content.css` :

```css
...
.prefix-content{
    display: inline !important;
}
...
```

Het element `<note>` genereert een extra `<span>` met het voorvoegsel-inhoud van de klasse die overeenkomt met het typekenmerk. Deze CSS-regel is gericht op de `.prefix-content` -klasse binnen `<note>` -elementen met een type-kenmerk, zodat u de inhoud van het voorvoegsel naar wens kunt opmaken of bewerken.

