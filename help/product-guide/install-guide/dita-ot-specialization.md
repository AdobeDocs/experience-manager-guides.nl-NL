---
title: Aangepaste DITA-OT en DITA-specialisatie gebruiken
description: Leer hoe u aangepaste DITA-OT- en DITA-specialisatie gebruikt
exl-id: ddc1393b-b269-40e5-9627-96dad82b42e9
feature: DITA-OT Configuration
role: Admin
level: Experienced
source-git-commit: b04f20af6e1f85746e13dad464513bf60b039378
workflow-type: tm+mt
source-wordcount: '2122'
ht-degree: 0%

---

# Aangepaste DITA-OT en DITA-specialisatie gebruiken {#id181GAJ0005Z}

De Open Toolkit DITA \(DITA-OT \) is een reeks op Java-Gebaseerde, open-bronhulpmiddelen die verwerking voor kaarten DITA en onderwerpinhoud verstrekken. Met AEM Guides kunt u eenvoudig aangepaste DITA-OT-plug-ins importeren en gebruiken. Als AEM Guides eenmaal is geïmporteerd, kan het zo worden geconfigureerd dat de aangepaste DITA-OT-insteekmodule wordt gebruikt om uitvoer in elke gewenste indeling te genereren. Als de uitvoer wordt gegenereerd, selecteert u gewoon de DITA-OT-optie en gebruikt AEM Guides de aangepaste DITA-OT-plug-in om de vereiste uitvoer te genereren.

Als u Ant-parameters wilt verwerken terwijl u uitvoer publiceert, biedt AEM Guides u een eenvoudige manier om dit te doen. U kunt opgeven welke Ant-parameters u wilt gebruiken en dezelfde parameters vervolgens door het publicatieproces worden verwerkt.

>[!NOTE]
>
> AEM Guides wordt geleverd met DITA-OT versie 3.3.2. AEM Guides biedt echter wel ondersteuning voor DITA-OT versie 1.7 en hoger. Voor de volledige lijst van versies DITA-OT, zie [&#x200B; versies DITA-OT &#x200B;](http://www.dita-ot.org/download).

>[!TIP]
>
> Zie de *configuratie van Profielen DITA-OT* en *Gebruikend douaneDITA-OT* secties in de Beste praktijken gids voor beste praktijken rond het gebruiken van douaneDITA-OT stop-ins.

## Aangepaste DITA-OT-plug-ins gebruiken {#id181NH1020L7}

Er zijn twee manieren om aangepaste insteekmodule DITA-OT te gebruiken voor publicatie. De eerste methode is het uploaden van de aangepaste DITA-OT plug-in naar de AEM opslagplaats. De andere methode is om de aangepaste DITA-OT-plug-in op uw server op te slaan, een profiel te maken en de locatie van de aangepaste DITA-OT-plug-in in uw profiel op te geven.

AEM Guides wordt standaard geleverd met een vooraf geconfigureerd profiel dat de configuraties bevat voor de standaardsjablonen die moeten worden gebruikt voor het bewerken en publiceren van inhoud. U kunt aangepaste profielen maken met aangepaste sjablonen die u kunt gebruiken tijdens het bewerken van documenten en aangepaste DITA-OT-plug-ins voor het publiceren van inhoud.

Het standaard DITA-OT-pakket dat beschikbaar is bij AEM Guides wordt geleverd met Apache FOP XSL-FO-processor, die geen ondersteuning biedt voor rendering van MathML-vergelijkingen. Als u MathML-vergelijkingen in uw inhoud gebruikt, moet u ervoor zorgen dat u een insteekmodule voor Apache FOP voor MathML-rendering-engine hebt geïntegreerd of een andere XSL-FO-processor hebt gebruikt.

>[!IMPORTANT]
>
> Als u AEM Guides van versie 2.2 tot 2.5.1 of 2.6 hebt bevorderd, dan worden alle veranderingen die door configuratiemanager worden aangebracht automatisch gekozen en in het Standaardprofiel opgeslagen.

Voer de volgende stappen uit om aangepaste DITA-OT-plug-in te uploaden naar de AEM opslagplaats:

1. Meld u aan bij AEM en open de modus CRXDE Lite.

1. Download het `DITA-OT.ZIP` -bestand.

   De locatie van het `DITA-OT.ZIP` -bestand is `/libs/fmdita/dita_resources/DITA-OT.zip` .

   ![](assets/dita-ot-zip-in-crx.png)

1. Extraheer de inhoud van het ZIP-bestand op de server.

1. Gebruik een integratormechanisme voor DITA-OT-plug-ins om de nieuwe versie van DITA-OT te integreren met uw aangepaste DITA-OT-plug-in.

   >[!NOTE]
   >
   > Het klassepadscheidingsteken in het ZIP-bestand van de plug-in is afhankelijk van het besturingssysteem. Dit betekent dat als de server wordt gehost op Windows, het klassepadscheidingsteken anders is dan het scheidingsteken voor Linux. Voor meer informatie over manueel het integreren stop-ins, zie *manueel het installeren van stop-ins* onderwerp in documentatie DITA-OT.

1. Maak het ZIP-bestand opnieuw met dezelfde naam \(`DITA-OT.ZIP`\) en mapstructuur.

1. Upload het bijgewerkte ZIP-bestand weer naar de AEM-opslagplaats.

   Controleer het volgende voordat u het ZIP-bestand uploadt:

   - Voer de integrator \(om de aangepaste insteekmodule te installeren\) uit op een Mac/Linux-besturingssysteem om problemen met bestandsscheidingstekens te voorkomen - aangezien Windows en Linux-besturingssystemen verschillende bestandscheiders hebben, is de insteekmodule die is geïntegreerd in Mac/Linux OS compatibel met zowel Windows- als Linux-instellingen.
   - Zorg ervoor dat het `DITA-OT.ZIP` -bestand een map met de naam &quot;DITA-OT&quot; bevat die alle relevante plug-ins en bestanden bevat.
   - Controleer of het `DITA-OT.ZIP` -bestand dat u maakt van het mimeType is: &quot;nt:file&quot; \(dit komt overeen met het primaire type ZIP-bestand wanneer het wordt geüpload naar AEM\). Gebruik een WebDAV-tool of code-implementatie om dit ZIP-bestand te uploaden naar het gewenste pad in AEM. \(Gebruik AEM pakketbeheer niet om dit ZIP-bestand te implementeren, omdat dit ZIP-bestand geen pakket met AEM inhoud is, maar slechts een archiefbestand.\)

   >[!NOTE]
   >
   > Het wordt aanbevolen het standaard DITA-OT-pakket niet te overschrijven. U moet uw aangepaste DITA-OT-pakket met uw plug-in uploaden naar een andere locatie in de map `apps` .

1. Open het standaard DITA-profiel voor bewerken en sla dit op \(zonder updates uit te voeren\) zodat de wijzigingen van kracht worden.


Voer de volgende stappen uit om een nieuw profiel te maken en dit te configureren voor het gebruik van een aangepaste DITA-OT-plug-in die op uw server is opgeslagen:

1. Sla de aangepaste DITA-OT-insteekmodule op uw server op.

   >[!NOTE]
   >
   > De mapstructuur voor het opslaan van de aangepaste DITA-OT-plug-in moet als volgt zijn: `\*<parent-folder\>*\DITA-OT`.

1. Klik op de verbinding van Adobe Experience Manager bij de bovenkant en kies **Hulpmiddelen**.

1. Selecteer **Gidsen** van de lijst van hulpmiddelen.

1. Klik op de **1&rbrace; tegel van Profielen DITA &lbrace;.**

   >[!NOTE]
   >
   > De standaardprofielgegevens worden weergegeven op de pagina Profielen. Als u AEM Guides van versie 2.2 tot 2.5.1 of 2.6 hebt bevorderd, dan worden alle veranderingen die door configuratiemanager worden aangebracht automatisch gekozen en in het Standaardprofiel opgeslagen.

1. U kunt het standaardprofiel bewerken, een nieuw profiel maken of instellingen in het standaardprofiel dupliceren om een nieuw profiel te maken.

   >[!NOTE]
   >
   > U kunt het standaardprofiel bijwerken, maar u kunt het niet verwijderen. Alle nieuwe profielen die u maakt, kunnen echter worden bewerkt en verwijderd.

1. Configureer de volgende eigenschappen voor het gebruik van de aangepaste DITA-OT-plug-in:

   | Eigenschapnaam | Beschrijving |
   |-------------|-----------|
   | **Eigenschappen van het Profiel** |
   | Profielnaam | Geef dit profiel een unieke naam. |
   | Uitvoer opnieuw gebruiken | *\(Optioneel\)* Als uw profiel op een bestaand profiel gebaseerd is, dan selecteer deze optie. Als u deze optie selecteert, zorgt AEM Guides ervoor dat de inhoud van het DITA-OT-pakket niet opnieuw wordt geëxtraheerd en wordt het bestaande DITA-OT-pakket opnieuw gebruikt. |
   | Pad voor exporteren van profiel | *\ (Facultatief \)* specificeer de weg waar DITA-OT op schijf wordt gehouden. Standaard bundelt AEM Guides een DITA-OT-pakket in de opslagplaats en wordt het op de schijf opgehaald bij dit pad.<br>**Nota** U kunt deze weg bepalen gebruikend om het even welk bestaand systeemvariabele of bezit. Zie beschrijving het [&#x200B; DITA-OT bezit van de Variabelen van het Milieu &#x200B;](#id181NH0YN0AX) voor meer informatie. |
   | Toegewezen pad | \ (*Facultatief* \) specificeer de weg in uw inhoudsbewaarplaats waarvoor dit profiel van toepassing is. U kunt meerdere locaties opgeven. |
   | **DITA-OT Eigenschappen** |
   | Tijdslimiet DITA-OT | \ (*Facultatief* \) specificeer de tijd \ (in seconden \) waarvoor AEM Guides op een reactie van de stop DITA-OT wacht. Als er geen reactie is ontvangen binnen de opgegeven tijd, wordt de publicatietaak beëindigd en wordt de taak gemarkeerd als mislukt. Ook, worden de mislukkingslogboeken ter beschikking gesteld in het dossier van het outputgeneratie. <br> Standaardwaarde: 300 seconden \(5 minuten\) |
   | DITA-OT PDF-argumenten | Geef de opdrachtregelargumenten op die door de aangepaste DITA-OT-plug-in worden verwerkt voor het genereren van de PDF-uitvoer. Voor alle douaneDITA-OT profielen, specificeer het volgende bevel-lijn argument:`-lib plugins/org.dita.pdf2.fop/lib/` |
   | DITA-OT AEM Argumenten | \ (*Facultatief* \) specificeer de douane bevel-lijn argumenten die door de douaneDITA-OT stop-binnen voor het produceren van de output van de Plaats worden verwerkt AEM. |
   | DITA-OT bibliotheekpaden | \ (*Facultatief* \) specificeer de extra bibliotheekwegen van stop - van DITA-OT. |
   | DITA-OT XML samenstellen | \ (*Facultatieve* \) specificeer de weg van het douaneAnt bouwt manuscript dat met de aangepaste stop DITA-OT wordt gebundeld. Dit pad is relatief ten opzichte van de map DITA-OT op uw bestandssysteem. |
   | DITA-OT map Ant Script | \(Optioneel\) Geef het pad op van de map DITA-OT Ant-script. Dit pad is relatief ten opzichte van de map DITA-OT op uw bestandssysteem. |
   | DITA-OT-omgevingsvariabelen | *\ (Facultatief \)* specificeer omgevingsvariabelen om tot het DITA-OT proces over te gaan. Standaard voegt AEM Guides vier variabelen toe: `ANT_OPTS`, `ANT_HOME`, `PATH` en `CLASSPATH` . <br> U kunt alle bestaande systeemomgevingsvariabelen of -eigenschappen opnieuw gebruiken om nieuwe omgevingsvariabelen samen te stellen. Als u bijvoorbeeld `JAVA_HOME` systeemvariabele in uw systeem hebt gedefinieerd en u een nieuwe omgevingsvariabele wilt definiëren met de naam `JAVA_BIN` die is gemaakt met `JAVA_HOME` . Vervolgens kunt u de definitie van `JAVA_BIN` toevoegen als:<br> `JAVA_BIN= ${JAVA_HOME}/bin` <br> **Nota** U kunt het systeemeigenschappen van Java ook gebruiken om omgevingsvariabelen te bouwen. Als AEM beginscript bijvoorbeeld een Java-systeemeigenschap `java.io.tmpdir` in een tijdelijke map definieert, kunt u deze eigenschap gebruiken om de nieuwe variabele als: `${java.io.tmpdir}/fmdita/dita_ot` <br> te definiëren. **Belangrijk** om het even welk bestaand systeemvariabele of bezit opnieuw te gebruiken, moet het binnen `${}` worden ingesloten. |
   | DITA-OT-uitvoer overschrijven | *\(Facultatief \)* als deze optie wordt geselecteerd, dan kunt u het pakket specificeren DITA-OT beschikbaar op uw lokale systeem om output te produceren gebruikend DITA-OT. Deze configuratie wordt geplaatst bij activering van ConfigManager. <br> Als u het pad wilt opgeven van een DITA-OT-pakket dat is opgeslagen op AEM server, schakelt u deze optie uit. |
   | AEM DITA-OT ZIP-pad/lokaal DITA-OT-mappad | Afhankelijk van uw selectie in Overschrijven DITA-OT Output, specificeer de volledige weg waar het douane DITA-OT.zip- dossier wordt opgeslagen. Dit zou het pad in uw AEM opslagplaats of lokaal systeem kunnen zijn. |
   | DITA-OT plug-inpad | Pad van de aangepaste plug-in. Deze plug-in wordt automatisch geïntegreerd met het hoofdpakket DITA-OT. |
   | Catalogi integreren | \ (*Facultatieve* \) Weg van de dossiers van aangepaste DTD en XSD catalog.xml in de AEM bewaarplaats. Dit moet alleen worden opgegeven wanneer de catalogi ontbreken in het DITA-OT-pakket. Deze catalogi worden automatisch als een plug-in geïntegreerd met de hoofdmap DITA-OT. |
   | Catalogus systeem-id toevoegen | \ (*Facultatieve* \) selecteer deze optie slechts als er ontbrekende Publieke ingangen van identiteitskaart in de catalogus zijn of als de DITA- dossiers slechts systeem IDs gebruiken die met betrekking tot de serverweg van waar zij worden geupload zijn. |
   | DITA-OT tijdelijk pad | *\(Optioneel\)* Geef een tijdelijke locatie op waar DITA-bestanden worden gekopieerd voor verwerking. Voordat DITA-OT bestanden verwerkt, worden ze naar deze tijdelijke locatie gekopieerd. De tijdelijke opslaglocatie is standaard: <br> **Nota** U kunt deze weg bepalen gebruikend om het even welk bestaand systeemvariabele of bezit. Zie beschrijving het [&#x200B; DITA-OT bezit van de Variabelen van het Milieu &#x200B;](#id181NH0YN0AX) voor meer informatie. |

   >[!NOTE]
   >
   >  Het AEM Guides-installatieprogramma maakt twee omgevingsvariabelen waarmee u het pad van de aangepaste DITA-OT-plug-inbestanden kunt opgeven. Deze omgevingsvariabelen zijn: DITAOT\_DIR, die het pad van de map DITA-OT op het bestandssysteem bevat, en DITAMAP\_DIR, die het pad bevat waar de DITA-kaartinhoud wordt geëxtraheerd op het bestandssysteem.

1. Klik **Gedaan** om het profiel te bewaren.


>[!NOTE]
>
> U kunt het aangepaste DITA-profiel exporteren als een pakket en uploaden naar de andere AEM Guides-instanties om tijd te besparen. Voor meer informatie, zie [&#x200B; Bijlage &#x200B;](appendix.md).

## DITA-specialisatie integreren {#id211MB0E00XA}

De specialisatie DITA is het proces om nieuwe structuren te creëren DITA door nieuwe elementen toe te voegen of bestaande elementen te verwijderen. Om een nieuw element te creëren DITA, kunt u een bestaand element DITA als basis nemen en het wijzigen volgens uw auteursvereisten. In wezen, staat de specialisatie DITA u toe om aangepaste informatiemodellen tot stand te brengen die aan uw bedrijfsvereisten voldoen terwijl het behouden van de voordelen van de bestaande architectuur DITA.

Met de functie Profiel kunt u aangepaste DITA-specialisatie-instellingen opslaan. Deze instellingen kunnen vervolgens worden gebruikt bij het ontwerpen en publiceren van aangepaste DITA-inhoud. AEM Guides staat u toe om Openbare identiteitskaart en identiteitskaart van het Systeem in uw douane DTDs/XSDs te gebruiken.

>[!NOTE]
>
> AEM Guides Web Editor biedt geen ondersteuning voor XSD&#39;s.

Voer de volgende stappen uit om een nieuw profiel te creëren en het te vormen om gespecialiseerde DTDs en XSDs AEM Guides te gebruiken:

1. Maak op uw lokale computer een specialisatiemap met de gespecialiseerde DTD&#39;s en XSD&#39;s.

1. Geef de DTD-gegevens op in het `catalog.xml` -bestand dat ook in de specialisatiemap moet worden opgenomen.

   >[!NOTE]
   >
   > In het geval van DITA 1.3 is de standaardlocatie voor het DTD `catalog.xml` -bestand in de AEM-opslagplaats: `/libs/fmdita/dita_resources/DITA-1.3/dtd/catalog.xml` .

1. Geef de XSD-gegevens in het `catalog.xml` -bestand op die ook in de specialisatiemap moeten worden opgenomen.

   >[!NOTE]
   >
   > In het geval van DITA 1.3 is de standaardlocatie voor het bestand XSD catalog.xml in de AEM opslagplaats: `/libs/fmdita/dita_resources/DITA-1.3/xsd/catalog.xml`.

1. Upload de map naar de volgende locatie:

   `/apps/fmdita/dita_resources`

1. Klik op de verbinding van Adobe Experience Manager bij de bovenkant en kies **Hulpmiddelen**.

1. Selecteer **Gidsen** van de lijst van hulpmiddelen.

1. Klik op de **1&rbrace; tegel van Profielen DITA &lbrace;.**

   >[!NOTE]
   >
   > De standaardprofielgegevens worden weergegeven op de pagina Profielen. Als u AEM Guides van versie 2.2 tot 2.5.1 of 2.6 hebt bevorderd, dan worden alle veranderingen die door configuratiemanager worden aangebracht automatisch gekozen en in het Standaardprofiel opgeslagen.



1. U kunt het standaardprofiel bewerken, een nieuw profiel maken of instellingen in het standaardprofiel dupliceren om een nieuw profiel te maken.

   >[!NOTE]
   >
   > U kunt het standaardprofiel niet verwijderen. Alle nieuwe profielen die u maakt, kunnen echter worden bewerkt en verwijderd.

1. In het **Schema** \> **Catalogus** montages, specificeer de weg van de douaneDTD en XSD `catalog.xml` dossiers in uw AEM bewaarplaats.

   >[!NOTE]
   >
   > Als u het douaneschema gebruikt, moet u de weg van de dossiers van douane DTD en XSD catalog.xml in de AEM bewaarplaats in **bepalen integreer Catalogi** optie.



1. Selecteer **toevoegen de Catalogus van identiteitskaart van het Systeem** optie.

   >[!NOTE]
   >
   > Selecteer deze optie alleen als er items voor openbare id&#39;s ontbreken in de catalogus of als de DITA-bestanden alleen de systeem-id&#39;s gebruiken die relatief zijn ten opzichte van het lokale bestandspad van waaruit ze worden geüpload.

   Voor meer informatie over andere eigenschappen op de pagina van Profielen, zie de eigenschappen lijst in [&#x200B; Stap 6 &#x200B;](#id17A9F0D075Z) van de [&#x200B; douane DITA-OT stop-ins van het Gebruik &lbrace;](#id181NH1020L7) sectie.

1. Klik **Gedaan** om het profiel te bewaren.


>[!NOTE]
>
> U kunt het aangepaste DITA-profiel exporteren als een pakket en uploaden naar de andere AEM Guides-instanties om tijd te besparen. Voor meer informatie, zie [&#x200B; Appendix.md &#x200B;](appendix.md).
