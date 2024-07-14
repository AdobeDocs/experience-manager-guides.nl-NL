---
title: Inleiding
description: Inleiding tot de API Reference Guide voor AEM Guides
exl-id: d8ee9cf7-1d67-4b4a-aa80-64e893a99463
feature: API Introduction
role: Developer
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '725'
ht-degree: 0%

---

# Inleiding {#id1761C0007W7}

Adobe Experience Manager Guides \ (later die als *AEM Guides* wordt bedoeld \) is een oplossing van begin tot eind, ondernemingsoplossing die Adobe Experience Manager \ (AEM \) toelaat om componenteninhoudbeheeroplossing \ (CCMS \) mogelijkheden voor op DITA-Gebaseerde inhoudsverwezenlijking en levering te hebben. Klanten hebben via programmacode toegang tot AEM Guides-workflows om deze te integreren met andere bedrijfstoepassingen. Deze API&#39;s kunnen ook door Adobe partners worden gebruikt om de waardepositie van AEM Guides te verbeteren door de functionaliteit ervan uit te breiden of door deze te integreren met andere toepassingen of services.

## AEM Guides API&#39;s

De AEM Guides API&#39;s zijn in twee indelingen beschikbaar: HTTP en Java. Deze API&#39;s maken belangrijke functies van AEM Guides toegankelijk voor toepassingsontwikkelaars. Met deze functies kunnen ontwikkelaars hun eigen plug-ins maken om de workflows uit de doos uit te breiden. De API&#39;s zijn beschikbaar voor het beheren van uitvoer voor DITA-inhoud, het werken met DITA-kaarten, het toevoegen van voorwaardelijke kenmerken aan profielen op mapniveau en het converteren van HTML- en Word-documenten naar DITA-indeling.

## De JAR&#39;s installeren op uw lokale Apache Maven-opslagplaats {#install-jar-local}

Als u de JAR-bestanden wilt kunnen gebruiken die door AEM Guides beschikbaar zijn gesteld, moet u ze installeren in uw lokale Apache Maven-opslagruimte. Voer de volgende stappen uit om de JAR&#39;s te installeren op uw locatie in Maven-opslagplaats:

1. Pak de inhoud van het AEM Guides-pakket \(.zip\) uit op uw lokale systeem.

2. Navigeer naar de volgende map in het pad voor geëxtraheerde inhoud bij de opdrachtprompt:

   ```
   \jcr_root\libs\fmdita\osgi-bundles\install
   ```

3. Voer de volgende opdracht uit om de API-bundel te installeren in uw lokale Maven-opslagruimte:

   ```
   mvn install:install-file -Dfile=api-X.x.jar -DgroupId=com.adobe.fmdita -DartifactId=api -Dversion=X.x -Dpackaging=jar**
   ```

   >[!NOTE]
   >
   > In het bovenstaande bevel, zou X.x met het daadwerkelijke versieaantal in de parameters van Dfile en van de Versie moeten worden vervangen.

4. \ (*Facultatieve* \) installeert gebiedsdeel in uw lokale Gemaakt plaats van het project. U kunt dit bereiken door een map in uw Maven-project te maken en vervolgens de opdracht `mvn install` uit te voeren die in de vorige stap met de volgende aanvullende parameter is gegeven:

   ```
   -DlocalRepositoryPath=<path_to_project_repository>
   ```

   Vervolgens voegt u een `repository` -element toe aan het bovenliggende pom.xml-bestand als u de lokale opslagmap van het project toegankelijk wilt maken voor het Maven-constructieproces:

   ```XML
   <repositories>
      <repository>
         <id>project-repository</id>
         <url>file://${project.basedir}/repository</url>
      </repository>
   </repositories>
   ```


Dit proces installeert de API JARs in de lokale Maven bewaarplaats.

## De service-API JAR gebruiken in een Maven-project

Nadat u de API JAR&#39;s in uw lokale Maven-opslagruimte hebt geïnstalleerd, voert u de volgende stappen uit om de JAR in uw projecten te gebruiken:

1. Voeg JAR aan uw codebasis toe en bewijs het aan de gegevensopslagplaats van de codebasis onder een omslag, zoals &quot;gebiedsdelen&quot;. De mapnaam is afhankelijk van de basishiërarchie van de code.

2. Configureer de bestanden met projectpom.xml als volgt:

   Het bestand pom.xml van het bovenliggende project:

   >[!IMPORTANT]
   >
   > In het volgende codefragment moet X.x worden vervangen door het eigenlijke versienummer en de bestandsnaam van de API JAR. Deze informatie zal het zelfde als gegeven in Stap 3 van het [ installatieproces ](#install-jar-local) zijn.

   ```XML
   <plugin>
   
       <groupId>org.apache.maven.plugins</groupId>
   
      <artifactId>maven-install-plugin</artifactId>
   
       <version>2.5.2</version>
   
       <configuration>
   
               <groupId>com.adobe.fmdita</groupId>
   
               <artifactId>api</artifactId>
   
               <version>X.x</version>
   
               <file>${basedir}/dependencies/fmdita/api-X.x.jar</file>
   
               <packaging>jar</packaging>
   
               <generatePom>true</generatePom>
   
       </configuration>
   
       <executions>
   
           <execution>
   
               <id>inst_fmdita</id>
   
                   <goals>
   
                       <goal>install-file</goal>
   
                   </goals>
   
                   <phase>clean</phase>
   
           </execution>
   
       </executions>
   </plugin>
   ```

   Het bestand pom.xml van de onderliggende module:

   ```XML
   <plugin>
      <groupId>org.apache.maven.plugins</groupId>
   
      <artifactId>maven-install-plugin</artifactId>
   
      <configuration>
   
         <groupId>com.adobe.fmdita</groupId>
   
         <artifactId>api</artifactId>
   
         <version>3.6</version>
   
         <file>${basedir}/../dependencies/fmdita/api-3.6.jar</file>
   
         <packaging>jar</packaging>
   
         <generatePom>true</generatePom>
   
      </configuration>
   
      <executions>
   
         <execution>
   
            <id>inst_fmdita</id>
   
            <goals>
   
               <goal>install-file</goal>
   
            </goals>
   
            <phase>clean</phase>
   
         </execution>
   
      </executions>
   
   </plugin>
   ```


## De service-API JAR van de openbare Maven-opslagplaats configureren en gebruiken

Voer de volgende stappen uit om de dienst API JARs van de openbare Maven bewaarplaats in uw projecten te vormen en te gebruiken:

1. Als u de service-API JAR in een project wilt gebruiken, configureert u de openbare Maven-opslagruimte van AEM Guides in het bestand pom.xml.
2. Configureer de openbare Maven-opslagplaats in het bestand settings.xml van Maven als volgt:

   ```XML
   <repository>
      <id>fmdita-public</id>
      <name>fmdita-public</name>
      <url>https://repo.aem-guides.com/repository/fmdita-public</url>
   </repository>
   ```

3. Zodra de bewaarplaats opstelling is, voeg de dienst API JAR als projectgebiedsdeel in het pom.xml- dossier van het project toe.

   >[!NOTE]
   >
   > Gebruik dezelfde versie van de API JAR als het AEM Guides-pakket dat u op de server hebt geïnstalleerd.

4. Vorm de Geweven gebiedsdeel zoals hieronder getoond:

   ```XML
   <dependency>
      <groupId>com.adobe.fmdita</groupId>
      <artifactId>api</artifactId>
      <version>4.0</version>
   </dependency>
   ```


Zodra de dienst API JAR als projectgebiedsdeel in het pom.xml- dossier van het project wordt toegevoegd, kunt u AEM Guides Java APIs in uw project bouwen en gebruiken.

## API JAR gebruiken vanuit de Maven Central-opslagplaats voor AEM Guides as a Cloud Service

Voor AEM Guides as a Cloud Service is de API JAR geïmplementeerd in Maven Central. U kunt de API JAR zonder enige installatie gebruiken.

>[!NOTE]
>
> De naamgevingsconventie van de API-jar is bijgewerkt volgens de naamgevingsconventie voor invoegtoepassingen voor cloud.

Om API JAR te gebruiken, moet u het gebiedsdeel aan pom.xml van uw project toevoegen zoals hieronder getoond:

```XML
<dependency>
   <groupId>com.adobe.aem</groupId>
   <artifactId>aem-guides-sdk-api</artifactId>
   <version>2022.5</version>
</dependency>
```

>[!NOTE]
>
> Aangezien de pakketten in de API JAR nog steeds hetzelfde zijn, is geen codewijziging vereist om deze API JAR in de bestaande wolkenprojecten te gebruiken.

## Aanvullende bronnen

Na is een lijst van andere nuttige middelen van AEM Guides, die op [ ](https://helpx.adobe.com/support/xml-documentation-for-experience-manager.html) pagina Leren &amp; van de Steun beschikbaar zijn:

- Handboek
- Installatie- en configuratiehandleiding
- Handleiding voor snel starten
- [ de Archiefpagina van het Archief van de Hulp ](https://helpx.adobe.com/xml-documentation-for-experience-manager/archive.html) \ (de documentatie van de toegangsoudere versie \)
