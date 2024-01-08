---
title: Zuurstofinsteekmodule voor Adobe Experience Manager-hulplijnen
description: Leer hoe u Oxygen-insteekmodule voor Adobe Experience Manager-hulplijnen kunt gebruiken om uw inhoud te maken en te beheren.
hide: true
hidefromtoc: true
exl-id: 9a140564-27eb-404e-93a5-f5c81364e7f7
source-git-commit: 0e19b870541e8e65dc371eb01fc3256f172c1a91
workflow-type: tm+mt
source-wordcount: '6294'
ht-degree: 0%

---

# Zuurstofinsteekmodule voor Adobe Experience Manager-hulplijnen {#id1645H6010Q5}

Met de insteekmodule Zuurstof voor Adobe Experience Manager-hulplijnen \(later Oxygen-insteekmodule voor AEM hulplijnen genoemd in de handleiding\) kunt u de Oxygen XML-auteur verbinden met de Adobe Experience Manager \(AEM\)-opslagplaats voor het ontwerpen en beheren van inhoud. U kunt de plug-in gebruiken om bestanden te zoeken, te openen, te checken en in te checken; mappen en bestanden te uploaden in AEM opslagplaats. Met het deelvenster AEM hulplijnen in de bureaubladtoepassing kunt u de gewenste mappen \(van AEM opslagplaats\) markeren naar de lijst met favoriete mappen, zodat u ze snel kunt openen. Bovendien kunt u een pakket installeren in AEM webinterface en uw DITA-bestanden rechtstreeks vanuit de AEM webinterface openen in Oxygen XML Author.

## Downloaden en installeren {#id1826M0L0PUI}

De insteekmodule Zuurstof voor AEM hulplijnen wordt beschikbaar gesteld via de portal voor softwaredistributie van Adobe. Zoek naar &quot;zuurstof&quot; op het tabblad Experience Manager en download het installatieprogramma van de insteekmodule van uw [Distributieportaal voor software voor Adobe](https://experience.adobe.com/#/downloads/content/software-distribution/en/general.html).

>[!NOTE]
>
>Controleer of de versiecompatibiliteit van de Zuurstofconnector compatibel is met de releaseopmerkingen voor de specifieke Adobe Experience Manager-hulplijnen.

Wanneer u het installatieprogramma hebt, installeert u het op de lokale computer waar de Oxygen XML Author is geïnstalleerd. Voordat u met het installatieproces begint, moet u controleren of uw systeem voldoet aan de technische vereisten voor de installatie van de insteekmodule voor AEM.

### Technische voorschriften

- Oxygen XML Author versie 25.1

- Adobe Experience Manager Guides versie 4.3 of hoger

- Adobe Experience Manager versie 6.5 met Service Pack 14, 15, 16 en 17

- Besturingssysteem ondersteund door Oxygen XML Author versie 25.1

- Java Development Kit
   - Oracle SE 8 JRE 1.8

### De insteekmodule installeren in Windows

>[!IMPORTANT]
>
>Als u een oudere versie van de plug-in op uw systeem hebt geïnstalleerd, moet u deze verwijderen voordat u het installatieproces start. Zie de **Pakketten verwijderen** in de [Werken met pakketten](https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/package-manager.html) artikel voor instructies voor het verwijderen.

Voer de volgende stappen uit op het systeem waarop Oxygen XML Author is geïnstalleerd:

1. De installatie starten `.exe` bestand.

   Het welkomstscherm van de installatiewizard wordt weergegeven.

1. Klikken **Volgende** en blader aan plaats waar het.exe dossier van de Auteur van Zuurstof XML beschikbaar is.

1. Selecteer het bestand en klik op **Openen**.

   De locatie van het geselecteerde bestand wordt toegevoegd aan de installatiewizard.

1. Klik op **Next**.

1. Klikken **Installeren**.

1. Klikken **Voltooien** om de installatiewizard te sluiten.
1. Start Oxygen XML Author.

   Het deelvenster AEM Hulplijnen wordt weergegeven in de Oxygen XML-auteur.

   ![AEM](images/oxygen-aem-connector.png){width="800" align="left"}

   >[!NOTE]
   >
   >Als u het deelvenster Hulplijnen AEM niet ziet, raadpleegt u de oplossingen in de sectie Problemen oplossen—[Ontbrekende AEM deelvenster Hulplijnen](#id192BH200ZAX).


### De insteekmodule installeren op Mac

>[!IMPORTANT]
>
>Als u een oudere versie van de plug-in op uw systeem hebt geïnstalleerd, moet u deze verwijderen voordat u het installatieproces start. Zie de **Pakketten verwijderen** in de [Werken met pakketten](https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/package-manager.html) instructies voor het verwijderen van artikelen.

Voer de volgende stappen uit op het systeem waarop Oxygen XML Author is geïnstalleerd:

1. Zoek het .dmg-bestand van de plug-in op uw systeem.

1. Dubbelklik op het .dmg-bestand om de bestandsinhoud te openen.

   Het .dmg-bestand bevat een map aem-connector-x.x en een bestand aem-connector-x.x-setup.

   >[!NOTE]
   >
   >x.x in de bestandsnamen is het versienummer van de plug-in.

1. Kopieer de map aem-connector-x.x in de map plugins van Oxygen XML Author.
1. Dubbelklik op het bestand aem-connector-x.x-setup om het installatieprogramma te starten.

1. Start Oxygen XML Author.

   Het deelvenster AEM Hulplijnen wordt weergegeven in de Oxygen XML-auteur.

   ![AEM Mac](images/oxygen-aem-connector-mac.png) {width="800" align="left"}

   >[!NOTE]
   >
   >Als u het deelvenster Hulplijnen AEM niet ziet, raadpleegt u de oplossingen in de sectie Problemen oplossen—[Ontbrekende AEM deelvenster Hulplijnen](#id192BH200ZAX).


### Het pakket installeren om de functie voor het bewerken van documenten vanuit AEM webinterface in te schakelen {#id182CE0Q0TY4}

Als auteur, kunt u uw kaarten DITA of onderwerpen in de Auteur van XML van Zuurstof direct van de AEM Webinterface openen en uitgeven. Om deze functie in AEM webinterface in te schakelen, moet uw AEM een pakket installeren in uw AEM ontwerpinstantie.

Als AEM beheerder voert u de volgende stappen uit om het pakket te installeren:

1. Haal het ZIP-bestand van het pakket op van uw IT-team.
1. Aanmelden bij uw AEM *\(als beheerder\)* en navigeer naar de CRX Package Manager. De standaard-URL voor toegang tot pakketbeheer is

   `http://<server name>:<port>/crx/packmgr/index.jsp`

   De pakketmanager beheert de pakketten op uw lokale AEM installatie. Zie voor meer informatie over het werken met de Package Manager [Werken met pakketten](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developer-tools/package-manager.html?lang=en) in AEM documentatie.

   ![Pakketbeheer](images/package-manager.png) {width="650" align="left"}

1. Als u het Zuurstofpakket wilt uploaden, klikt u op **Pakket uploaden**.
1. Navigeer in het dialoogvenster Pakket uploaden naar het Oxygen-pakketbestand dat u in Stap 1 hebt gedownload en klik op OK.

   Het pakket wordt geüpload naar uw AEM-instantie.

1. Klik op **Installeren**.

   ![Zuurstofpakket](images/oxygen-package.png){width="650" align="left"}

1. Klik in het dialoogvenster Pakket installeren op **Installeren**.
1. Nadat de installatie is voltooid, klikt u op de knop Home in de linkerbovenhoek van de CRX Package Manager.
1. Selecteer een DITA-bestand in de map met middelen.

   **Bewerken in zuurstof** is beschikbaar in de werkbalk. Zie voor meer informatie over het gebruik van deze optie [Open DITA-onderwerp in Oxygen XML Author vanuit AEM webinterface](#id182CE0I905Z).

   >[!NOTE]
   >
   >De **Bewerken in zuurstof** Deze optie is zichtbaar wanneer u een DITA-onderwerp selecteert. Als u meerdere onderwerpen selecteert, is de optie niet zichtbaar.


## De insteekmodule Zuurstof voor AEM hulplijnen configureren {#id1826KF00AHS}

Nadat u de plug-in hebt gedownload en geïnstalleerd, moet u de volgende instellingen configureren om met de plug-in te werken:

- **Instellingen voor webverificatie**: Instellingen voor SSO-verificatie in de plug-in voor AEM hulplijnen.
- **Algemene instellingen**: Verbindingsinstellingen voor de plug-in, zoals URL van AEM server, aanmeldingsgegevens enzovoort.
- **Voorkeur voor het profileren van kenmerkaanpassingen en bestandsnamen in kruisverwijzingen**: Deze configuratie is vereist voor de kenmerkenschema&#39;s voor profilering voor de documentatiesets.

### Instellingen voor webverificatie

JxBrowser wordt gebruikt voor SSO-verificatie door de Oxygen-connector plug-in. Het is een op chroom gebaseerde browser. Voor java 9+ is toegang tot niet openbare API&#39;s vereist en u moet deze toegang tot JxBrowser uitdrukkelijk verlenen. Zie voor meer informatie [Problemen met JxBrowser oplossen](https://jxbrowser-support.teamdev.com/docs/guides/troubleshooting/issues.html).

Werk de opgegeven bestanden bij om de instellingen voor webverificatie in de insteekmodule Zuurstof voor AEM hulplijnen te configureren:

>[!NOTE]
>
>Maak een back-up van het bestand voordat u het bijwerkt.

**Voor Mac en Zuurstof 25.1**

Voeg de volgende regels toe in env.sh

```java
--illegal-access=permit\
--add-opens=java.desktop/javax.swing.plaf.basic=ALL-UNNAMED\
--add-exports=javafx.controls/com.sun.javafx.scene.control=ALL-UNNAMED\
--add-exports=javafx.graphics/com.sun.javafx.stage=ALL-UNNAMED\
--add-exports=javafx.graphics/com.sun.javafx.scene=ALL-UNNAMED\
--add-exports=javafx.graphics/com.sun.javafx.scene.traversal=ALL-UNNAMED\
--add-exports=javafx.graphics/com.sun.javafx.tk=ALL-UNNAMED\
--add-exports=javafx.graphics/com.sun.glass.ui=ALL-UNNAMED\
--add-opens=javafx.graphics/com.sun.glass.ui=ALL-UNNAMED\
--add-opens=javafx.graphics/javafx.stage=ALL-UNNAMED\
--add-opens=javafx.graphics/com.sun.javafx.tk.quantum=ALL-UNNAMED\
--add-exports=java.desktop/sun.awt=ALL-UNNAMED\
--add-opens javafx.swing/javafx.embed.swing=ALL-UNNAMED
```

Voeg de volgende regels toe aan de functie oxydator.sh

```java
-Djdk.module.illegalAccess=permit\-Djava.ipc.external=true\
```

**Voor Windows en Zuurstof 25.1**

De volgende regels toevoegen in env.bat

```java
--illegal-access=permit --add-opens=java.desktop/javax.swing.plaf.basic=ALL-UNNAMED --add-exports=javafx.controls/com.sun.javafx.scene.control=ALL-UNNAMED --add-exports=javafx.graphics/com.sun.javafx.stage=ALL-UNNAMED --add-exports=javafx.graphics/com.sun.javafx.scene=ALL-UNNAMED --add-exports=javafx.graphics/com.sun.javafx.scene.traversal=ALL-UNNAMED --add-exports=javafx.graphics/com.sun.javafx.tk=ALL-UNNAMED --add-exports=javafx.graphics/com.sun.glass.ui=ALL-UNNAMED --add-opens=javafx.graphics/com.sun.glass.ui=ALL-UNNAMED --add-opens=javafx.graphics/javafx.stage=ALL-UNNAMED --add-opens=javafx.graphics/com.sun.javafx.tk.quantum=ALL-UNNAMED --add-exports=java.desktop/sun.awt=ALL-UNNAMED --add-opens javafx.swing/javafx.embed.swing=ALL-UNNAMED
```

Voeg de volgende regels toe aan de zuurstofAuthor.bat

```java
-Djdk.module.illegalAccess=permit -Djava.ipc.external=true
```

>[!NOTE]
>
>Als beheerder moet u zuurstof uitvoeren van zuurstofAuthor.sh voor Mac en zuurstofAuthor.bat voor Windows.

### Algemene instellingen

Voer de volgende stappen uit om de verbindingsinstellingen te configureren in de Oxygen-insteekmodule voor Adobe Experience Manager-hulplijnen:

1. Klik in het deelvenster Hulplijnen AEM op het pictogram Instellingen en selecteer vervolgens **Instellingen**.

   ![Verbindingsinstellingen ](images/settings.png){width="800" align="left"}

1. Geef de volgende details op:
   - **Server-URL**: URL van de AEM server, bijvoorbeeld:

     ```http
     http[s]://<host>:<port>
     ```

     Geef in de bovenstaande URL de hostnaam en poort op van de server waar AEM server wordt geïmplementeerd.

     >[!IMPORTANT]
     >
     >Als uw AEM server wordt opgesteld op haven 80 of 443, dan te hoeven u niet het in URL te specificeren.

   - **Verificatie:** Kiezen uit **Standaard \(gebruikersnaam/wachtwoord\)** of **Webverificatie**. Als u **Basis** verificatie die u moet invoeren **Gebruikersnaam** en **Wachtwoord** in het dialoogvenster Voorkeuren.

     Als u Webverificatie selecteert, wordt het aanmeldingsscherm van de AEM weergegeven. Voer uw aanmeldingsgegevens in en klik op de knop **Aanmelden** knop. Wanneer de aanmelding is voltooid, wordt het aanmeldingsscherm AEM en geeft het deelvenster AEM de bestandslijst van de AEM server weer.

   - **Time-out verbinding**: Geef in seconden tijd op waarop de client wacht op een reactie van de AEM server. Als er binnen de opgegeven tijd geen reactie van de server wordt ontvangen, wordt het verzoek beëindigd. De standaardwaarde is 20 seconden.

   - **Lokale map**: Locatie op uw lokale computer waar de bestanden van AEM opslagplaats worden opgeslagen na uitchecken. Als u een locatie opgeeft die niet op het station aanwezig is, maakt de plug-in die locatie.
   - **Bestand openen bij uitchecken**: Als deze optie is geselecteerd, worden de bestanden bij het uitchecken geopend.
   - **Bestand sluiten bij aanmelden**: Als deze optie is geselecteerd, worden de bestanden tijdens het inchecken gesloten. Voordat u het bestand sluit, wordt een pop-up weergegeven waarin u de versieopmerkingen kunt opgeven.
   - **Dialoogvenster Inchecken weergeven bij het sluiten van een bestand**: Als deze optie is geselecteerd, wordt een pop-up weergegeven bij het sluiten van een bestand. In het pop-upvenster kunt u het bestand inchecken of sluiten zonder het in te checken.
   - **Bestand automatisch uitchecken wanneer geopend**: Als deze optie is geselecteerd, wordt het bestand automatisch uitgecheckt en wordt het geopend voor bewerking. Als het bestand al is uitgecheckt, wordt het gewoon geopend voor bewerking. Als deze optie niet is geselecteerd, wordt het openen van een bestand waarvoor u geen vergrendeling hebt, geopend in de alleen-lezen modus.
1. Klikken **OK**.

### Voorkeur voor het profileren van kenmerkaanpassingen en bestandsnamen in kruisverwijzingen {#id1827K0D0OHT}

U moet de voorkeur in de Auteur van XML van Oxygen vormen om het profilerende attribuut te gebruiken verbonden aan de onderwerpen DITA in de AEM bewaarplaats. U moet ook de voorkeur aan vertoningsbestandsnamen in plaats van GUIDs in de verwijzingen vormen.

Voer de volgende stappen uit om profielkenmerken en kruisverwijzingen te configureren:

1. Klik in Oxygen XML-auteur op **Opties** \> **Voorkeuren**.
1. In de **Koppeling naar documenttype** tab, selecteert u **DITA** en klik vervolgens op **Uitbreiden**.

   ![documenttype koppelen](images/document_type_association.png){width="650" align="left"}

1. In de **Classpath** tab, selecteert u `com.adobe.o2.connector` in de **Loader van bovenliggende klasse gebruiken vanuit insteekmodule met id** vervolgkeuzelijst.

   ![Tabblad Klassepad](images/dita-extension.png){width="650" align="left"}

1. In de **Extensies** wijzigt u de volgende wijzigingen:

   - Klikken **Kies** naast de **Extensiebundel** en selecteert u   `LinkResolverExtensionBundle - com.adobe.o2.framework.extn` in de **Klasse** lijst. Klikken **OK**.
     ![Gevormde uitbreiding voor onderwerpen DITA](images/dita-map-extenstion-link-resolve.png) {width="650" align="left"}
   - Klikken **Kies** naast de **Auteur Extension State Listener** krachtens **Afzonderlijke extensies** en selecteert u `CustomAuthorExtensionStateListener - com.adobe.o2.framework.extn` in de **Klasse** lijst. Klikken **OK**.
   - Klikken **Kies** naast de **Editor aangepaste kenmerkwaarde auteur** krachtens **Afzonderlijke extensies** en selecteert u `CustomValueEditor - com.adobe.o2.framework.extn` in de **Klasse** lijst. Klikken **OK**.
   - Klikken **Kies** naast de **Invoeghandler voor externe objecten van auteur** krachtens **Afzonderlijke extensies** en selecteert u `CustomURLInsertionHandler - com.adobe.o2.ui ` in de **Klasse** lijst. Klikken **OK**.


   Het volgende schermschot toont gevormd **Extensie** tab voor DITA-onderwerpen:
   <img src="images/dita-topic-extension-tab.png" alt="Gevormde uitbreiding voor onderwerpen DITA" width="650" border="2px">
1. Klikken **OK** in alle dialoogvensters om uw wijzigingen op te slaan.

### DITA-kaartextensie configureren

De configuratie van de DITA-kaartextensie is vereist om het openen van kaartbestanden in de Oxygen XML-auteur rechtstreeks vanuit de AEM webinterface mogelijk te maken. Deze configuraties zijn gelijkaardig aan de configuraties voor het profileren van attributen die in de voorafgaande procedure worden gedaan.

Voer de volgende stappen uit om de DITA kaartuitbreiding te vormen:

1. Klik in Oxygen XML-auteur op **Opties** \> **Voorkeuren**.
1. In de **Koppeling naar documenttype** tab, selecteert u **DITA-kaart** en klik vervolgens op **Uitbreiden**.
1. In de **Classpath** selecteert u com.adobe.o2.connector in het dialoogvenster **Loader van bovenliggende klasse gebruiken vanuit insteekmodule met id** vervolgkeuzelijst.
1. In de **Extensies** wijzigt u de volgende wijzigingen:
   - Klikken **Kies** naast de **Extensiebundel** en selecteert u   `com.adobe.o2.framework.extn.LinkResolverDITAMapExtensionBundle` in de **Klasse** lijst. Klikken **OK**.

   - Klikken **Kies** naast de **Auteur Extension State Listener** krachtens **Afzonderlijke extensies** en selecteert u `CustomDITAMapAuthorExtensionStateListener - com.adobe.o2.framework.extn` in de **Klasse** lijst. Klikken **OK**.

   - Klikken **Kies** naast de **Invoeghandler voor externe objecten van auteur** krachtens **Afzonderlijke extensies** en selecteert u `CustomURLInsertionHandler - com.adobe.o2.ui ` in de **Klasse** lijst. Klikken **OK**.

   - Klikken **Kies** naast de **Editor aangepaste kenmerkwaarde auteur** krachtens **Afzonderlijke extensies** en selecteert u `CustomValueEditor - com.adobe.o2.framework.extn` in de **Klasse** lijst. Klikken **OK**.

   - Klikken **Kies** naast de **Verwijzingen oplossen** krachtens **Afzonderlijke extensies** en selecteert u `CustomDITAMapReferenceResolver - com.adobe.o2` in de **Klasse** lijst. Klikken **OK**.
   - *\(Optioneel\)* Als u verwijzingen niet wilt oplossen terwijl het openen van een kaartdossier, dan moet u de volgende extra configuratie uitvoeren:

   Het volgende schermschot toont gevormd **Extensie** tab:
   <img src="images/dita-map-extension-tab.png" alt="Gevormde uitbreiding voor kaart DITA" width="650" border="2px">

1. Klikken **OK** in alle dialoogvensters om uw wijzigingen op te slaan.

## Werken met zuurstofinsteekmodule voor AEM hulplijnen {#id1826JG00WY4}

### Deelvenster Hulplijnen AEM

In het volgende scherm ziet u het deelvenster Hulplijnen AEM.

![connectorpaneel](images/connector-panel.png){width="550" align="left"}

**A**\) Geeft de zoekbalk weer.

**B**\) Toont de map Favorieten. Standaard is deze leeg. U kunt mappen uit de AEM opslagplaats toevoegen als favoriet. De favoriete mappen worden dan hier weergegeven.

**C**\) In de map DAM wordt de AEM weergegeven. U kunt de mappenweergave uitvouwen en samenvouwen.

**D**\) Het pictogram Instellingen \(versnelling\) met de volgende opties:

- **Verbinden**: Selecteer deze optie als u verbinding wilt maken met de AEM server. De optie is uitgeschakeld wanneer de XML-auteur van Zuurstof is verbonden met de AEM.
- **Vernieuwen**: Selecteer deze optie om de meest recente status van de bestanden en map op te halen uit de AEM opslagplaats.

  >[!NOTE]
  >
  >Sla uw bestanden op voordat u ze vernieuwt. Wanneer u **Vernieuwen** krijgt u een waarschuwing om uw bestanden op te slaan voordat u ze vernieuwt. Als u uw bestanden niet hebt opgeslagen, klikt u op **Annuleren** en sla ze op.

- **Instellingen**: U kunt deze optie gebruiken om het algemene dialoogvenster Voorkeuren van de insteekmodule te openen.
- **Afmelden**: Selecteer deze optie om de AEM serververbinding te sluiten. Deze optie is beschikbaar slechts als u de wijze van de Authentificatie van het Web gebruikt.

### Functies van contextmenu

De functies van de insteekmodule Zuurstof voor AEM hulplijnen zijn beschikbaar wanneer u met de rechtermuisknop op een map of bestand in de AEM klikt. De functies die beschikbaar zijn voor de mappen verschillen van die voor de bestanden. Hier volgt een volledige lijst met functies in het contextmenu Zuurstofinsteekmodule voor AEM hulplijnen:

- **Openen**: Hiermee opent u het geselecteerde bestand of breidt u de geselecteerde map uit.
- **Openen in**: U kunt het geselecteerde bestand openen in AEM webeditor of kaartdashboard van hulplijnen of in de Kaarteditor. Zie voor meer informatie over deze opties [Bestand openen in AEM editor voor hulplijnen](#id195GH0V30KX).
- **Uitchecken**: Hiermee wordt een bestand uitgecheckt uit AEM opslagplaats. Zie voor meer informatie [Bestanden uitchecken](#id195HC020TS4).
- **Uitchecken met afhankelijke personen**: Controleert een bestand met de directe referenties. Zie voor meer informatie [Bestanden uitchecken](#id195HC020TS4).
- **Uitchecken met alleen-lezen afhankelijke personen**: Controleert het geselecteerde bestand samen met de afhankelijke componenten. U kunt de afhankelijke bestanden niet wijzigen. Zie voor meer informatie [Bestanden uitchecken](#id195HC020TS4).
- **Uitchecken annuleren**: Hiermee annuleert u het uitgecheckte bestand, sluit u het bestand uit de editor en keert u de wijzigingen terug naar de laatste versie van het bestand dat op de server is opgeslagen.
- **Vernieuwen**: In het geval van een bestand haalt u de meest recente kopie van het bestand op van de AEM opslagplaats. Voor een map worden de mapstructuur en de status van het bestand opgehaald. Dit betekent dat er een bestand is toegevoegd en dat het vervolgens wordt weergegeven in de weergave AEM. Als een bestand is uitgecheckt op AEM server, wordt het bestand ook weergegeven als uitgecheckt bij Vernieuwen in Zuurstofauteur. De bestandenlijst in de *Bestanden uitgecheckt in AEM hulplijnen* Weergeven.
- **Uitgecheckte bestanden vernieuwen**: Hiermee vernieuwt u de lijst met uitgecheckte bestanden in het dialoogvenster *Bestanden uitgecheckt in AEM hulplijnen* Weergeven. Als een bestand is uitgecheckt op AEM server, wordt bij het uitvoeren van een vernieuwen de lijst met uitgecheckte bestanden in het dialoogvenster *Bestanden uitgecheckt in AEM hulplijnen* Weergeven. Als er echter een nieuw bestand is toegevoegd of de status van een bestand is gewijzigd, wordt dit niet bijgewerkt in de boomstructuurweergave AEM hulplijnen. Als u de status van bestanden op AEM wilt bijwerken, moet u een vernieuwen uitvoeren.
- **Inchecken**: Controleert een bestand dat u hebt uitgecheckt. Zie voor meer informatie [Een bestand inchecken](#id182CF0J0FHS).
- **Inchecken met afhankelijke personen**: Als u bestanden met afhankelijke personen hebt uitgecheckt, controleert deze optie het hoofdbestand samen met de afhankelijke personen. Zie voor meer informatie [Een bestand inchecken](#id182CF0J0FHS).
- **Map maken**: Maakt een map in de AEM opslagplaats. Deze optie is alleen beschikbaar op mapniveau.
- **Bestand\(en\) uploaden**: uploadt een of meer bestanden. Zie voor meer informatie [Bestanden en mappen uploaden](#id195HC03F03J).
- **Uploaden met afhankelijke personen**: Hiermee uploadt u DITA-bestanden \(XML, DITA, Boekenkaart of DITA-kaart\) met de afhankelijke personen. Zie voor meer informatie [Bestanden en mappen uploaden](#id195HC03F03J).
- **Map uploaden**: Hiermee wordt een map geüpload naar de AEM. Zie voor meer informatie [Bestanden en mappen uploaden](#id195HC03F03J).
- **Toevoegen aan Favorieten**: Voegt een map toe aan de *Favorieten* in het deelvenster Hulplijnen AEM. U wordt aangeraden hier uw werkmap toe te voegen, zodat bestanden en de status van het bestand gemakkelijker kunnen worden gesynchroniseerd vanaf AEM.
- **Verwijderen uit Favorieten**: Hiermee wordt een map verwijderd uit *Favorieten*. Zie voor meer informatie [Favorieten toevoegen of verwijderen](#id195HC04405P).
- **Metagegevens weergeven**: Hiermee worden de metagegevens weergegeven, zoals DITA-klasse, Titel, Type, UUID en andere informatie die aan een bestand is gekoppeld. Zie voor meer informatie [De metagegevens van een bestand weergeven](#id195GHN0H05C).
- **Versies weergeven**: geeft de versiegeschiedenis van een bestand weer. Zie voor meer informatie [De versiehistorie van een bestand weergeven](#id195GI000D5Q).

### Een bestand openen in Oxygen XML Author {#id195GHJ0A0UB}

Nadat u verbinding hebt gemaakt met de AEM opslagplaats, kunt u bestanden openen voor bewerking in de Oxygen XML-auteur. Voer de volgende stappen uit om een bestand te openen voor bewerking in de XML-auteur van zuurstof:

1. Klik met de rechtermuisknop op een bestand in het deelvenster AEM hulplijnen dat u wilt openen voor bewerken.

1. Selecteren **Openen** in het contextmenu.

   Het bestand wordt geopend in de Editor van de Oxygen XML-auteur.

   ![Hulplijn op tabblad Bestand](images/guid-in-file-tab.png) {width="800" align="left"}

   Wanneer u de muisaanwijzer boven het tabblad van een bestand plaatst, wordt het serverpad en de bijbehorende UUID weergegeven. In de bovenstaande schermafbeelding wordt de UUID van het document gemarkeerd.


Als u **Bestand automatisch uitchecken wanneer geopend** optie \(in het dialoogvenster Voorkeuren\), wordt het bestand bij het openen van een bestand automatisch uitgecheckt en kan het worden bewerkt. Als u een bestand wilt openen, dubbelklikt u op een bestandsnaam of klikt u met de rechtermuisknop op de bestandsnaam en kiest u **Openen** in het contextmenu. Als deze optie niet is geselecteerd, wordt het bestand geopend in de modus Alleen-lezen.

>[!NOTE]
>
>U kunt ook dubbelklikken op een bestand om het te openen.

### Bestand openen in AEM editor voor hulplijnen {#id195GH0V30KX}

Als u de editors wilt gebruiken beschikbaar in AEM Hulplijnen, kunt u dit doen door de vereiste optie in het contextmenu te selecteren. Voer de volgende stappen uit om AEM de redacteur van Gidsen in plaats van de redacteur van de Schrijver van XML van Oxygen te gebruiken:

1. Klik met de rechtermuisknop op een bestand in het deelvenster AEM hulplijnen dat u wilt openen voor bewerken.

1. Selecteren **Openen in** in het contextmenu en kies een van de volgende opties:

   - **Web Topic Editor**: Als het bestand dat u opent, een .xml- of een .dita-bestand is, kunt u het openen voor bewerking in de webeditor. Kies de optie **Web Topic Editor** om het geselecteerde bestand te openen en te bewerken in de webeditor.

   - **Kaartdashboard**: U kunt ervoor kiezen om een .ditamap-bestand te bewerken in het kaartdashboard, waarin u verschillende bewerkingen kunt uitvoeren op het kaartbestand. Deze bewerkingen zijn afhankelijk van de rol/groep waartoe u behoort.

   - **Web DITA Map Editor**: Als u het .ditamap-bestand wilt openen voor bewerking in de Kaarteditor, kiest u deze optie. Gebruikend de optie van de Redacteur van de Kaart DITA, kunt u onderwerpen toevoegen of verwijderen, relatietabellen toevoegen, en andere verrichtingen op uw kaart uitvoeren.


### Bestanden uitchecken {#id195HC020TS4}

Wanneer u een bestand uitcheckt, wordt het lokaal op uw systeem opgeslagen en vergrendeld voor bewerking in de AEM opslagplaats. Voer de volgende stappen uit om een bestand uit te checken:

1. U kunt uw bestanden op een van de volgende manieren uitchecken:
   - Klik met de rechtermuisknop op een bestand in het deelvenster Hulplijnen AEM.
   - Klik met de rechtermuisknop op het tabblad Kaart in het deelvenster DITA Maps Manager.
   - Klik met de rechtermuisknop op een bestand in het deelvenster DITA Maps Manager.
   - Klik met de rechtermuisknop op het tabblad Bestanden wanneer u een kaart of onderwerp opent in de Editor.

1. Selecteer een van de volgende opties:
   - **Uitchecken:** Hiermee wordt een bestand uit AEM opslagplaats uitgecheckt en beschikbaar gesteld voor bewerking.
   - **Uitchecken met afhankelijke personen**: Controleert een bestand met de directe referenties. Met deze optie kunt u de bovenliggende en onderliggende pagina&#39;s wijzigen. Met de insteekmodule Zuurstof voor AEM hulplijnen kunt u één niveau afhankelijke personen uitchecken. Bijvoorbeeld, de Verwijzingen van de Kaart A Onderwerp A en Onderwerp A verwijst naar Onderwerp B. Het uitchecken van Kaart A zal Onderwerp A ongeacht zijn niveau in de hiërarchie van TOC uitchecken. Nochtans, zal het geen Onderwerp B controleren omdat het niet direct van Kaart A verbonden is.
   - **Uitchecken met alleen-lezen afhankelijke personen**: Hiermee wordt een bestand uitgecheckt en worden de afhankelijkheden van het bestand als alleen-lezen kopieën naar uw lokale computer gedownload. U kunt de afhankelijke bestanden niet wijzigen.

Als u **Bestanden openen bij uitchecken** optie \(in het dialoogvenster Voorkeuren\), wordt het bestand bij het uitchecken automatisch geopend voor bewerking.

Als u **Bestand automatisch uitchecken wanneer geopend** optie \(in het dialoogvenster Voorkeuren\), wordt het bestand bij het openen automatisch uitgecheckt en beschikbaar gesteld voor bewerken. Als u een bestand wilt openen, dubbelklikt u op een bestandsnaam of klikt u met de rechtermuisknop op de bestandsnaam en kiest u **Openen** in het contextmenu.

Wanneer een bestand is uitgecheckt, verandert het pictogram van het bestand om de vergrendelde status weer te geven.

![Een bestand uitchecken](images/check-out-file.png){width="650" align="left"}

In de bovenstaande schermafbeelding wordt een bestand dat door een andere gebruiker is uitgecheckt, weergegeven met een zwart gekleurd vergrendelingspictogram \(A\). Het bestand dat door de huidige gebruiker is uitgecheckt, wordt weergegeven met een groene kleurvergrendeling \(B\).

>[!NOTE]
>
>Als het uitgecheckte bestand wordt verwijderd of naar een andere map in AEM wordt verplaatst, wordt een foutbericht weergegeven wanneer u het bestand incheckt. Zorg ervoor dat het uitgecheckte bestand niet wordt verplaatst of verwijderd via de AEM webinterface.

### Een bestand inchecken {#id182CF0J0FHS}

Wanneer u een bestand incheckt, wordt de lokale kopie van uw systeem opgeslagen in de AEM opslagplaats en wordt de vergrendeling van het bestand verwijderd. Voer de volgende stappen uit om een bestand in te checken:

1. Sla het bestand op door op **Bestand** \> **Opslaan**.

1. Klik met de rechtermuisknop op een uitgecheckt bestand of kaart op een van de volgende locaties:
   - Deelvenster Hulplijnen AEM
   - Het deelvenster DITA Maps Manager
   - Het dossierlusje wanneer u een kaart of een onderwerp in de Redacteur opent.
   - Het tabblad Kaart in het deelvenster DITA Maps Manager.

1. Kies uit de volgende twee opties:

   - **Inchecken**: Het geselecteerde bestand wordt vanaf uw lokale systeem ingecheckt in AEM opslagplaats.
   - **Inchecken met afhankelijke personen:** Als u een bestand samen met de afhankelijke bestanden hebt uitgecheckt, kunt u met deze optie alle afhankelijke bestanden in één bewerking inchecken. Als u deze optie selecteert, wordt het dialoogvenster Inchecken weergegeven met alle afhankelijke bestanden. Klik op OK om alle bestanden tegelijk in te checken.

   Als u afhankelijke bestanden niet hebt uitgecheckt en deze optie kiest, worden alleen de afhankelijke bestanden die u \(afzonderlijk\) hebt uitgecheckt, ingecheckt. Er wordt een lijst weergegeven met bestanden die niet kunnen worden ingecheckt:

   ![fouten controleren](images/check-in-error.png){width="800" align="left"}

   Het wordt sterk aanbevolen om een uitgecheckt bestand niet te verplaatsen. Als een uitgecheckt bestand echter naar een andere locatie wordt verplaatst, moet u het uitchecken van dat bestand annuleren. Als u updates wilt uitvoeren op dat bestand, checkt u het bestand opnieuw uit, brengt u wijzigingen aan en checkt u het opnieuw in. Als u een bestand probeert in te checken dat van de oorspronkelijke locatie is verplaatst, wordt er een fout weergegeven.

   Als een afhankelijk bestand is uitgecheckt in AEM, wordt het afhankelijke bestand niet weergegeven in het dialoogvenster Inchecken met afhankelijke personen. Voor een lijst met afhankelijke bestanden die zijn uitgecheckt in AEM, moet u een map vernieuwen.

   En als u een afhankelijk bestand hebt ingecheckt via AEM, wordt de bestandslijst pas vernieuwd in de Zuurstofauteur als u een map uitvoert die is uitgecheckte bestanden vernieuwen en vernieuwen. Als u een inchecken met afhankelijke bestanden uitvoert en sommige bestanden zijn AEM ingecheckt, wordt een foutmelding weergegeven met de bestanden die niet konden worden ingecheckt.

1. \(Optioneel\) In het dialoogvenster **Inchecken** of de **Inchecken met afhankelijke personen** een opmerking toevoegen in **Opmerkingen bij versie** tekstvak.

   >[!NOTE]
   >
   >Deze opmerking wordt weergegeven in de AEM versiegeschiedenis van het bestand.

1. Label(s) toevoegen in het dialoogvenster **Label** tekstvak in het dialoogvenster **Inchecken** of de **Inchecken met afhankelijke personen** dialoog. Voer een label in en druk op Enter. Bijvoorbeeld: *2307 Release*.

   Als uw beheerder een lijst met labels vooraf heeft gedefinieerd en deze in het dialoogvenster `label.json` en worden deze labels weergegeven als een vervolgkeuzelijst. U kunt een of meer labels kiezen in de vervolgkeuzelijst.

   ![Het dialoogvenster Inchecken](images/checkin-dropdown-labels.png){width="550" align="left"}

   U kunt veelvoudige etiketten (die door komma&#39;s worden gescheiden) aan de zelfde versie van een onderwerp toevoegen.  Bijvoorbeeld: *Adobe*, *AEM*, *Hulplijnen*.
Nochtans, kunt u niet het zelfde etiket aan de verschillende versies van een onderwerp toevoegen. Als u een label toevoegt dat u al aan een eerdere versie hebt toegevoegd, wordt het toegevoegd aan de meest recente versie en verwijderd uit de vorige versie.

   >[!NOTE]
   > 
   > Deze labels worden weergegeven in de AEM versiegeschiedenis van het bestand.


1. Klikken **OK**.

>[!NOTE]
>
>Als het uitgecheckte bestand wordt verwijderd of naar een andere map in AEM wordt verplaatst, wordt een foutbericht weergegeven wanneer u het bestand incheckt. Zorg ervoor dat het uitgecheckte bestand niet wordt verplaatst of verwijderd via de AEM webinterface.

### Bestanden uitgecheckt in AEM weergave Hulplijnen

Wanneer u in meerdere mappen werkt, is het niet eenvoudig om te bepalen hoeveel bestanden in één weergave zijn uitgecheckt. AEM Hulplijnen bieden uitgecheckte bestanden in AEM weergave Hulplijnen die één volledige momentopname geven van momenteel uitgecheckte bestanden. Met deze weergave kunt u gemakkelijk achterhalen welke bestanden door u in AEM opslagplaats zijn gecontroleerd met behulp van AEM hulplijnen. Voer de volgende stappen uit om toegang te krijgen tot en te werken met deze weergave:

1. Klikken **Venster** \> **Weergave tonen** \> **Bestanden uitgecheckt in AEM hulplijnen**.

   De uitgecheckte bestanden in AEM weergave Hulplijnen worden weergegeven.

   ![uitgecheckte bestanden](images/files-checkedout-view.png){width="550" align="left"}

1. Klik met de rechtermuisknop op een bestand in deze weergave voor de volgende opties:

   - [Openen](#id195GH0V30KX)
   - [Openen in](#id195GH0V30KX)
   - Uitchecken annuleren
   - [Inchecken](#id182CF0J0FHS)
   - [Inchecken met afhankelijke personen](#id182CF0J0FHS)
   - [Metagegevens weergeven](#id195GHN0H05C)
   - [Versies weergeven](#id195GI000D5Q)

**Opmerkingen over uitgecheckte bestanden in AEM weergave Hulplijnen:**

- De *Bestanden uitgecheckt in AEM hulplijnen* De weergave houdt gebruikerssessies bij. Dit betekent dat bestanden die door de huidige gebruiker zijn uitgecheckt, worden opgeslagen en onderhouden in de weergave voor dezelfde gebruikerssessies \(of cache\).

- Als de gebruiker de aanmeldingsgegevens of de AEM server wijzigt, worden de gegevens \(of cache\) van het uitgecheckte bestand in de weergave opnieuw ingesteld. De gebruiker moet handmatig een *Uitgecheckte bestanden vernieuwen* gebruiken in elke map van waaruit de bestanden eerder zijn uitgecheckt. Om dit te vereenvoudigen, wordt aanbevolen uw werkmappen toe te voegen aan *Favorieten* vanaf waar u snel een map kunt vernieuwen.

- U kunt de bestandslijst sorteren op basis van de bestandsnamen, titel of pad. Als een nieuw bestand is uitgecheckt, wordt het bestand in gesorteerde volgorde weergegeven in de weergave.


### Bestanden en mappen uploaden {#id195HC03F03J}

Voer de volgende stappen uit om bestanden of mappen te uploaden:

1. Klik met de rechtermuisknop op een map in het deelvenster Hulplijnen AEM.
1. Selecteer een van de volgende opties:
   - **Bestand\(en\) uploaden**: Selecteer deze optie om een of meerdere bestanden te uploaden naar de geselecteerde map in de AEM. Selecteer in het dialoogvenster Bestanden selecteren om bestanden te uploaden de bestanden en klik op **Openen**.
   - **Uploaden met afhankelijke personen**: Selecteer deze optie om een DITA-bestand met de afhankelijke componenten te uploaden. Selecteer in het dialoogvenster Bestand selecteren om te uploaden de bestanden en klik op **Openen**.
   - **Map uploaden**: Selecteer deze optie als u een map in de AEM wilt uploaden. Selecteer de map in het dialoogvenster Kies en klik op **Kies**.

**Aanvullende opmerkingen over het werken met UUID-bestanden**:

Bij het verplaatsen of kopiëren van inhoud van uw lokale systeem naar AEM opslagplaats moet rekening worden gehouden met de volgende punten:

- Bij het uploaden van een of meer bestanden wordt een nieuwe UUID gegenereerd voor bestanden zonder UUID. Deze UUID wordt toegevoegd in het dialoogvenster `topic id` van een DITA-bestand.

- Wanneer u een map kopieert, worden de verwijzingen naar de bestanden \(in de map\) automatisch bijgewerkt in alle DITA-toewijzingen die verwijzen naar bestanden in die map.

- Wanneer u een DITA-kaartbestand kopieert, worden de UUID-verwijzingen in het kaartbestand niet gewijzigd.

- Als een bestand of map een conflict heeft of een duplicaat heeft, wordt een unieke bestandsnaam gegenereerd voor het nieuwe bestand dat wordt gekopieerd of verplaatst.

- Geen twee bestanden kunnen dezelfde UUID hebben. Er wordt een unieke UID toegewezen aan alle nieuwe bestanden.

- Als een bestand door twee verschillende gebruikers tegelijk wordt geüpload, wordt het eerdere bestand overschreven door het bestand dat later wordt verwerkt. Een dergelijke praktijk moet echter worden vermeden.

- Wanneer u inhoud uitcheckt vanuit AEM opslagplaats en wijzigingen aanbrengt in uw lokale systeem, moet u ervoor zorgen dat de bestandsnaam niet wordt gewijzigd op het moment dat het bestand wordt geüpload.

- Als u een verwijzing invoegt in DITA Maps Manager of de Editor, wordt de titel van het bestand weergegeven en niet de UUID. Als de titel niet aanwezig is, dan toont het filename.

### Favorieten toevoegen of verwijderen {#id195HC04405P}

Voer de volgende stappen uit om een map toe te voegen aan of te verwijderen uit de map Favorieten in het deelvenster AEM.

- Klik met de rechtermuisknop op een map en selecteer **Toevoegen aan Favorieten**. U kunt een map toevoegen aan Favorieten als deze zich niet in Favorieten bevindt.
- U kunt een map op de volgende manieren uit Favorieten verwijderen:
   - Klik met de rechtermuisknop op een map in de **Favorieten** map en selecteer **Verwijderen uit Favorieten**.
   - Klik met de rechtermuisknop op een map in de AEM opslagplaats onder **DAM** map die al als favoriet is toegevoegd en selecteer **Verwijderen uit Favorieten**.

### De versiehistorie van een bestand weergeven {#id195GI000D5Q}

Voer de volgende stappen uit om de versiegeschiedenis van een bestand weer te geven:

1. Klik met de rechtermuisknop op een bestand in het deelvenster Hulplijnen AEM.

1. Selecteren **Versies weergeven** in het contextmenu.

   De versiegeschiedenis van het bestand wordt weergegeven in het dialoogvenster Versies.

   ![Versiehistorie](images/version-history.png){width="550" align="left"}


### De metagegevens van een bestand weergeven {#id195GHN0H05C}

Voer de volgende stappen uit om de metagegevens van een bestand weer te geven:

1. Klik met de rechtermuisknop op een bestand in het deelvenster Hulplijnen AEM.

1. Selecteren **Metagegevens weergeven** in het contextmenu.

   De metagegevens van het bestand, zoals de klasse DITA, de documentstatus, de wijzigingsdatum, de grootte, de titel en UUID, worden weergegeven in het dialoogvenster Metagegevens.

   ![Metagegevens weergeven](images/metadata.png){width="550" align="left"}


## Een onderwerp zoeken in de AEM {#id1826J20405Z}

Met de zoekbalk in het deelvenster Hulplijnen kunt u zoeken naar onderwerpen in de AEM opslagplaats. U kunt in de volledige DAM omslag zoeken of een omslag selecteren en dan naar een onderwerp in die omslag zoeken. Het onderzoeksresultaat toont de onderwerpen die tekst hebben die met uw onderzoeksvraag aanpassen.

Voer de volgende stappen uit om onderwerpen te zoeken:

1. Selecteer een omslag in de AEM bewaarplaats waar u een onderwerp wilt zoeken.
1. Voer de zoekquery in \(bijvoorbeeld `introduction`\) in de zoekbalk van de insteekmodule Zuurstof voor AEM hulplijnen.
1. Klik op de zoekknop of druk op Enter.

   Het resultaat wordt op het tabblad Zoekresultaten weergegeven als een lijst met het bestandspad. Als er geen overeenkomend resultaat voor uw zoekopdracht is gevonden, worden geen resultaten gevonden in &lt;path of=&quot;&quot; the=&quot;&quot; selected=&quot;&quot; folder=&quot;&quot;> bericht wordt weergegeven.

   ![Zoekresultaten](images/search.png){width="550" align="left"}

1. \(Optioneel\) Dubbelklik op een bestand in het zoekresultaat om het te openen in Oxygen XML Author.
1. Voer een van de volgende handelingen uit om terug te gaan naar de AEM Repository-weergave:
   - Als u de weergave AEM opslagplaats wilt weergeven zonder de zoekresultaten te wissen, klikt u op **Bladeren** tab.
   - Als u de zoekresultaten wilt wissen en de AEM Repository wilt weergeven, klikt u op het pictogram Zoekopdracht verwijderen.

## Open DITA-onderwerp in Oxygen XML Author vanuit AEM webinterface {#id182CE0I905Z}

U kunt uw onderwerp DITA in de Auteur van XML van Zuurstof van de AEM Webinterface openen en uitgeven. U moet een pakket in AEM installeren om deze optie in te schakelen. Zie voor meer informatie over de installatie van pakketten [Het pakket installeren om de functie voor het bewerken van documenten vanuit AEM webinterface in te schakelen](#id182CE0Q0TY4).

>[!NOTE]
>
>De **Bewerken in zuurstof** optie is toegankelijk van diverse plaatsen in AEM: wanneer een onderwerp wordt geselecteerd, wanneer een onderwerp, of van Onderwerpen en het lusje van Rapporten van DITA kaartconsole wordt voorvertoond. Als u meerdere onderwerpen selecteert, is de optie niet zichtbaar in de werkbalk.

**Een DITA-onderwerp openen**

Voer de volgende stappen uit om een onderwerp DITA in de Auteur van XML van Zuurstof te openen:

1. Selecteer een onderwerp in uw elementen en klik op **Bewerken in zuurstof** in de werkbalk.

   >[!NOTE]
   >
   >Als het onderwerp niet is uitgecheckt, wordt het eerst uitgecheckt en vervolgens in de bewerkingsmodus geopend in Zuurstof.

1. Oxygeen XML-auteur selecteren *&lt;version>* in de **Toepassing starten** berichtvenster. U kunt **Mijn keuze voor AEM koppelingen onthouden** opslaan van uw voorkeur.

**Een DITA-onderwerp bewerken**

Voer de volgende stappen uit om een onderwerp DITA in de Auteur van XML van Zuurstof uit te geven:

1. Selecteer en check een onderwerp in uw activa uit.
1. Klikken **Bewerken in zuurstof** in de werkbalk.

   >[!NOTE]
   >
   >Als het onderwerp niet is uitgecheckt, wordt het eerst uitgecheckt en vervolgens in de bewerkingsmodus geopend in Zuurstof.

1. Oxygeen XML-auteur selecteren *&lt;version>* in de **Toepassing starten** berichtvenster. U kunt **Mijn keuze voor AEM koppelingen onthouden** opslaan van uw voorkeur.
1. Bewerk het onderwerp in Oxygen XML Author.
1. Controleer het onderwerp van de insteekmodule Zuurstof voor AEM hulplijnen.

   Voor meer informatie over het inchecken van een onderwerp met de Zuurstofinsteekmodule voor AEM gidsen, zie [Een bestand inchecken](#id182CF0J0FHS).

   >[!NOTE]
   >
   >Controleer of u het onderwerp incheckt met de Oxygen-insteekmodule voor AEM hulplijnen. Als u incheckt vanuit de AEM webinterface, worden de wijzigingen die u aanbrengt in de Oxygen XML-auteur niet opgeslagen in de ingecheckte versie van het onderwerp.

**Voeg een verwijzing naar een onderwerp van de bewaarplaats van de Gidsen van de Experience Manager in**

U kunt een onderwerp ook slepen en laten vallen om de verwijzing in een onderwerp of een kaart op te nemen DITA.
>[!NOTE]
>
> U moet een bestand uitchecken voordat u er een verwijzing naar toevoegt.

De volgende elementen worden toegevoegd op basis van het type verwijzingen:

Als u aan de Redacteur met een open onderwerp laat vallen:
- Er wordt een verwijzing toegevoegd met `<image>` -element voor de afbeeldingen.
- Een objectelement wordt toegevoegd voor een video of audio.
- De `<xref>`  Het element wordt toegevoegd voor alle andere verwijzingen zoals onderwerp, kaart, DITAVAL, PDF, ZIP, en XML.

Als u naar Editor of DITA Maps Manager met een geopende Kaart daalt:
- De `<mapref>` element wordt toegevoegd voor kaartverwijzingen, die een kaart DITA, een boekkaart, of een OnderwerpRegeling omvatten.
- De `<topicref>` Het element wordt toegevoegd voor alle andere verwijzingen zoals onderwerp, kaart, DITAVAL, PDF, ZIP, en XML.


## Werken met kenmerkprofielen {#id1827JA002YK}

Met AEM hulplijnen kunt u eenvoudig voorwaardelijke kenmerken maken en koppelen met behulp van de relevante DITA-kenmerken. U kunt voorwaardelijke kenmerken definiëren op algemeen niveau of mapniveau. De globaal gedefinieerde voorwaarden zijn zichtbaar in alle projecten en mapniveauvoorwaarden zijn alleen zichtbaar in projecten die binnen de opgegeven map zijn gemaakt. Inhoudsauteurs kunnen deze voorwaardelijke kenmerken gebruiken om de inhoud in hun DITA-onderwerpen of -kaarten te conditionaliseren die ze maken of gebruiken. Voor meer informatie over het maken van voorwaardelijke kenmerken in AEM met behulp van de AEM hulplijnen raadpleegt u *Voorwaardelijke kenmerken voor algemene profielen of mapprofielen configureren* in Adobe Experience Manager-hulplijnen installeren en configureren.

>[!NOTE]
>
>Zorg ervoor dat u de voorwaardelijke kenmerken in AEM hebt toegevoegd en dat u deze hebt ingesteld [Voorkeur voor kenmerkaanpassing profileren](#id1827K0D0OHT) voordat u voorwaardelijke kenmerken aan uw inhoud toevoegt.

Voer de volgende stappen uit om voorwaardelijke kenmerken toe te voegen aan uw inhoud in Oxygen XML Author:

1. Uitchecken en een onderwerp openen vanuit het dialoogvenster *Zuurstofinsteekmodule voor AEM hulplijnen*.
1. Selecteer het gedeelte van de inhoud waarop u de voorwaardelijke kenmerken wilt toepassen.
1. Dubbelklik op het voorwaardelijke kenmerk in het deelvenster Kenmerken van de Oxygen XML-auteur.

   ![deelvenster Kenmerken](images/attribute-panel.png){width="300" align="left"}

1. In de **Beschikbaar** in het dialoogvenster Kenmerk bewerken selecteert u het kenmerk\(en\) en klikt u op **Toevoegen**.

   Het volgende scherm toont `audience` kenmerken.

   ![Dialoogvenster Kenmerken bewerken](images/edit-attributes.png){width="550" align="left"}

1. Klikken **OK**.

   De kenmerken worden toegevoegd aan de inhoud.


## Problemen met algemene problemen oplossen {#id188ABC00RY4}

Dit onderwerp behandelt enkele van de gemeenschappelijkste kwesties die u terwijl het werken met de Insteekmodule, samen met hun oplossingen zou kunnen ontmoeten.

### Ontbrekende AEM deelvenster Hulplijnen {#id192BH200ZAX}

**Probleem** - Als u het deelvenster Hulplijnen AEM niet ziet in de Oxygen XML-auteur, probeert u de volgende oplossingen:

Oplossing 1:

1. Schakel de plug-in in Oxygen XML Author.

   Klikken **Opties** \> **Voorkeuren** \> **Plug-ins** en selecteert u **Zuurstofinsteekmodule voor Adobe Experience Manager-hulplijnen.**

1. Start Oxygen XML Author opnieuw.


Oplossing 2:

1. Als het deelvenster Hulplijnen AEM nog steeds niet wordt weergegeven, schakelt u het venster Hulplijnen AEM in.

   Klik in Oxygen XML-auteur op **Venster** \> **Weergave tonen** \> **Hulplijnen AEM**.

Oplossing 3:

1. Verwijder de Oxygen-insteekmodule voor Adobe Experience Manager-hulplijnen en installeer deze opnieuw.

   - In Windows verwijdert u de insteekmodule uit **Software** lijst. Vervolgens installeert u de plug-in opnieuw.

   - Open in Mac de map aem-connector-x.x in de map plugins van Oxygen XML Author en verplaats deze naar **Prullenbak**. Maak vervolgens de **Prullenbak** map.


### Poort configureren voor DITA-OT-transformatie

**Probleem** - Wanneer u een DITA-OT-transformatie uitvoert op bestanden die door de insteekmodule worden verwerkt, mislukt de transformatie met de volgende fout:

![Transformatiefout DITA-OT](images/proxy-server-path-error-new.png){width="800" align="left"}

**Oplossing** - Dit probleem is opgelost door een proxyserver toe te voegen tussen DITA-OT en de insteekmodule. Deze proxyserver verwerkt en deelt alle bestanden die door DITA-OT zijn aangevraagd voor transformaties. De standaardpoort waarop deze server is geconfigureerd is: `5972`. Als u deze poort voor een andere server gebruikt, kunt u een andere poort voor de proxyserver opgeven.

Voer de volgende stappen uit om de standaardpoort van de proxyserver te wijzigen:

1. Blader naar de homemap van \(gebruiker&#39;s\).
1. Maak een bestand met de naam name\_connector\_proxy.
1. Open het bestand in een teksteditor en voeg een beschikbaar poortnummer toe aan de eerste regel van het bestand.
1. Sla het bestand op en sluit het.
1. Start Oxygen XML Author opnieuw en voer de DITA-OT transformation uit.


### AEM deelvenster Hulplijnen bladert niet naar de geopende bestandslocatie

Uitgave: wanneer u een bestand opent voor bewerking in de Oxygen XML-auteur van AEM server, wordt het bestand geopend voor bewerking in de Oxygen XML-auteur. AEM deelvenster Hulplijnen geeft echter niet de locatie van het bestand in de navigatiestructuur weer.

Oplossing: dit probleem is waargenomen in scenario&#39;s waarin het bestandspad tweemaal /content/dam bevat. Standaard worden alle elementen in AEM opgeslagen in de map /content/dam. Als u een mapstructuur uploadt of maakt die ook /content/dam bevat, wordt dit probleem waargenomen. U kunt alle normale bewerkingen op dergelijke bestanden uitvoeren, maar de locatie in de navigatiestructuur wordt niet standaard weergegeven. Als u dit bestand in de navigatiestructuur wilt openen, moet u handmatig naar de locatie van het bestand bladeren. Merk op dat in de navigatieboom de dubbele /content/dam weg door /content/assets wordt vervangen.

### Logboek configureren

Probleem: Standaard genereert de insteekmodule Zuurstof voor AEM hulplijnen geen logbestanden, waardoor het lastig is om fouten in een foutscenario op te sporen.

Oplossing: voer de volgende stappen uit om registreerapparaten voor Sygen en JxBrowser op te zetten:

1. Oxygen XML-auteur sluiten

1. Een bestand met de naam `logback.xml` met de volgende inhoud:

   ```xml
   <configuration>
       <appender name="R2" class="ch.qos.logback.core.rolling.RollingFileAppender">
           <file>${user.home}/Desktop/oxygenLog/oxygen.log</file>
           <rollingPolicy class="ch.qos.logback.core.rolling.FixedWindowRollingPolicy">
               <fileNamePattern>${user.home}/Desktop/oxygenLog/oxygen%i.log.gz</fileNamePattern>
               <minIndex>1</minIndex>
               <maxIndex>20</maxIndex>
           </rollingPolicy>
           <triggeringPolicy class="ch.qos.logback.core.rolling.SizeBasedTriggeringPolicy">
               <maxFileSize>100MB</maxFileSize>
           </triggeringPolicy>
           <encoder>
               <pattern>%r %marker %p [ %t ] %c - %m%n</pattern>
           </encoder>
       </appender> 
   
       <root level="debug">
           <appender-ref ref="R2" />
       </root>
   </configuration>   
   ```

1. Sla het bestand op in het dialoogvenster `Oxygen Author 25` directory. (Het pad zou bijvoorbeeld als volgt zijn: `C:\Program Files\Oxygen XML Author 25\logback.xml`)

1. Sluit het bestand. Hiermee worden Xygen-logs ingeschakeld, die beschikbaar zijn op het pad: `${user.home}/Desktop/oxygenLog/oxygen.log`
1. Open de `oxygenAuthor.bat` in een teksteditor.
1. Aan JxBrowser gerelateerde logbestanden instellen door de parameter toe te voegen
   `-Denable.aem.jx.log=true`. Hierdoor zijn aan JxBrowser gerelateerde logbestanden mogelijk, die u kunt weergeven op het pad: `${user.home}\AppData\Local\Temp\Oxygen_Plugin_Javax_Log.log`:




   ```java
   SET OXYGEN_JAVA=java.exe
   if exist "%JAVA_HOME%\bin\java.exe" set OXYGEN_JAVA="%JAVA_HOME%\bin\java.exe"
   if exist "%~dp0\jre\bin\java.exe" SET OXYGEN_JAVA="%~dp0\jre\bin\java.exe"
   rem Set environment variables
   call "%~dp0\env.bat"
   %OXYGEN_JAVA% -XX:-OmitStackTraceInFastThrow -XX:SoftRefLRUPolicyMSPerMB=10 -Djdk.module.illegalAccess=permit -Djava.ipc.external=true 
   -Denable.aem.jx.log=true -Dsun.java2d.noddraw=true -Dsun.awt.nopixfmt=true -Dsun.java2d.dpiaware=true -Dsun.io.useCanonCaches=true -Dsun.io.useCanonPrefixCache=true 
   -Dsun.awt.keepWorkingSetOnMinimize=true -Dcom.oxygenxml.app.descriptor=ro.sync.exml.AuthorFrameDescriptor
    -Dcom.oxygenxml.ApplicationDataFolder="%APPDATA%" -cp %CP% ro.sync.exml.Oxygen %*
   ```


Met de vorige stappen worden de logbestanden ingeschakeld en kunt u deze gebruiken om fouten op te sporen.
