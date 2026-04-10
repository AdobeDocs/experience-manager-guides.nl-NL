---
title: Versiebeheer
description: Leer hoe u versies beheert
feature: Version Management
role: Admin
level: Experienced
source-git-commit: b416334318a83e882c32318bc4769d24268cdd1c
workflow-type: tm+mt
source-wordcount: '2293'
ht-degree: 0%

---

# Versiebeheer {#id181GB000XY4}

Versioning is een belangrijk aspect van elk contentbeheersysteem. Hiermee kunt u een momentopname van uw digitale middel op een bepaald tijdstip maken. Met een versie van een digitaal middel kunt u de vereiste versie van het middel herstellen en bijwerken. Doorgaans kunt u voor het maken van een versie van een element het vereiste element uitchecken en inchecken.

Als beheerder kunt u regels afdwingen die gebruikers beperken om een bestand te bewerken zonder het uit te checken. Op dezelfde manier kunt u ervoor zorgen dat alle uitgecheckte bestanden worden ingecheckt om gegevensverlies te voorkomen.

In een omgeving voor meerdere toepassingen is het ook belangrijk ervoor te zorgen dat gebruikers geen bestanden van het systeem verwijderen. Deze vereiste is belangrijker voor bestanden die door andere gebruikers zijn uitgecheckt. AEM Guides biedt een configuratie die u kunt gebruiken om te voorkomen dat uitgecheckte bestanden per ongeluk door gebruikers worden verwijderd. Naast uitgecheckte bestanden kunt u ook het verwijderen van bestanden besturen die verwijzingen bevatten of waarnaar wordt verwezen vanuit andere bestanden.

## Nieuwe versie maken voor geüploade bestand

>[!NOTE]
>
> Deze configuratie is alleen van toepassing tijdens het uploaden van bestanden.

De volgende lusjes verstrekken instructies om **toe te laten creëren nieuwe versie voor geupload dossier** optie die op uw opstelling van Experience Manager Guides wordt gebaseerd: Cloud Service of Op locatie.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

1. Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-config-override.md#) om het configuratiedossier tot stand te brengen.
1. In het configuratiedossier, verstrek de volgende \ (bezit \) details om **te vormen creeer nieuwe versie voor geupload dossier** optie:


   | PID | Eigenschappensleutel | Waarde van eigenschap |
   |---|------------|--------------|
   | `com.adobe.fmdita.confi g.ConfigManager` | `create.ver.new.content` | Boolean \(true/false\).<br> **Standaardwaarde**: `true` |

>[!NOTE]
>
> Als de optie is geselecteerd, wordt er een nieuw versiebeheermechanisme toegepast dat het standaarduploadgedrag overschrijft dat bij elke volgende upload wordt toegepast, wordt de inhoud van het geüploade bestand als een nieuwe versie opgeslagen. Als deze optie is uitgeschakeld, gebruikt AEM Guides het standaardversiebeheermechanisme van AEM.

>[!TAB  Op locatie ]

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.config.ConfigManager** bundel.

1. Selecteer **creëren Nieuwe Versie voor Geüploade Dossier** optie.

   Deze optie is standaard uitgeschakeld.

   Als de optie is geselecteerd, wordt er een nieuw versiebeheermechanisme toegepast dat het standaarduploadgedrag overschrijft dat voor elke volgende upload wordt gebruikt. Hierdoor wordt de inhoud van het geüploade bestand als een nieuwe versie opgeslagen. Als deze optie is uitgeschakeld, gebruikt AEM Guides het standaardversiebeheermechanisme van AEM.

1. Klik **sparen**.


>[!NOTE]
>
> U kunt dossiers in partijen van 70 of minder uploaden, als u het bezit **toelaat creeer Nieuwe Versie voor Geüploade Dossier** \ (create.ver.new.content\) en gebruik **Assets UI** aan bulkupload activa.

>[!ENDTABS]


## Instellingen configureren om het bewerken van uitgecheckte bestanden toe te staan

Met de AEM Guides Web Editor kunt u DITA-onderwerpen maken en bijwerken. U kunt de Redacteur van het Web vormen om het uitgeven van slechts die documenten toe te staan die uit de bewaarplaats zijn gecontroleerd. Dit zorgt ervoor dat geen andere schrijver per ongeluk een onderwerp overschrijft dat voor het uitgeven door een andere schrijver wordt geopend. Zodra een onderwerp voor het uitgeven wordt geopend, kan een auteur het dossier op het tijdstip van het sluiten van het dossier inchecken.

Een andere belangrijke regel is ervoor te zorgen dat de dossiers die zijn gecontroleerd terug in het systeem worden gecontroleerd. Zo voorkomt u dat gebruikers per ongeluk de bestanden sluiten zonder ze weer in te checken.

Op de volgende tabbladen vindt u instructies voor het configureren van instellingen voor het bewerken van uitgecheckte bestanden op basis van uw Experience Manager Guides-instellingen: Cloud Service of On-Premise.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\) gegevens op om het bewerken van uitgecheckte bestanden te configureren:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.autocheckout` | Boolean \(true/false\).<br> **Standaardwaarde**: `false` |

Bovendien kunt u configureren om een waarschuwingsbericht weer te geven wanneer een uitgecheckt bestand wordt gesloten zonder het op te slaan of terug te controleren in de opslagplaats.

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.checkin` | Boolean \(true/false\).<br> **Standaardwaarde**: `false` |

>[!NOTE]
>
> Ongeacht of u deze functie in- of uitschakelt, zijn de opties voor het uitchecken en inchecken van bestanden altijd beschikbaar in een voorvertoning van een onderwerp.

>[!TAB  Op locatie ]

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.xmleditor.config.XmlEditorConfig** bundel.

1. Selecteer **onbruikbaar maken uitgeven zonder Controle** optie.

   ![](assets/xml-editor-config.png){width="650" align="left"}

   Met deze optie zien gebruikers de optie Bewerken pas op de werkbalk nadat ze een bestand hebben uitgecheckt.

1. Selecteer **vragen om Controle-binnen op Sluiten** optie om een waarschuwingsbericht te tonen wanneer een gecontroleerd dossier wordt gesloten zonder het op te slaan of terug in de bewaarplaats te controleren.

1. Klik **sparen**.

>[!NOTE]
>
> Ongeacht of u deze functie in- of uitschakelt, zijn de opties voor het uitchecken en inchecken van bestanden altijd beschikbaar in een voorvertoning van een onderwerp.

>[!ENDTABS]

## Uitgecheckt bestand tijdens uploaden overschrijven

>[!NOTE]
>
> *deze configuratie is van toepassing slechts wanneer u dossiers van Assets UI creeert en niet wanneer u dossiers uploadt gebruikend het hulpmiddel WebDAV.*

Op de volgende tabbladen vindt u instructies waarmee gebruikers het uploadbestand kunnen overschrijven dat door hen of een andere gebruiker is uitgecheckt op basis van uw Experience Manager Guides-instellingen: Cloud Service of On-Premise.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

1. Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-config-override.md#) om het configuratiedossier tot stand te brengen.
1. In het configuratiedossier, verstrek de volgende \(bezit \) details om het **overschrijven Uitgecheckt Dossier op Upload** optie te vormen:


| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `overwrite.checkout.onupload` | Boolean \(true/false\).<br> **Standaardwaarde**: `false` |

>[!NOTE]
>
> Deze optie is standaard uitgeschakeld. Als deze optie is geselecteerd, kunnen gebruikers uitgecheckte bestanden overschrijven. Als de optie niet is geselecteerd, kan het bestand niet worden overschreven als het door de gebruiker of een andere gebruiker is uitgecheckt.

>[!TAB  Op locatie ]

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.config.ConfigManager** bundel.

1. Selecteer het **Uitgecheckte Dossier van de Overschrijving op Upload** optie.

   Deze optie is standaard ingeschakeld. Als deze optie is geselecteerd, kunnen gebruikers uitgecheckte bestanden overschrijven. Als de optie niet is geselecteerd, kan het bestand niet worden overschreven als het door de gebruiker of een andere gebruiker is uitgecheckt.

1. Klik **sparen**.

>[!ENDTABS]


## Verwijderen van uitgecheckte bestanden voorkomen

Op de volgende tabbladen vindt u instructies om te voorkomen dat gebruikers per ongeluk bestanden verwijderen die door hen of een andere gebruiker zijn uitgecheckt op basis van uw Experience Manager Guides-instelling: Cloud Service of On-Premise.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\) gegevens op om te voorkomen dat gebruikers per ongeluk uitgecheckte bestanden verwijderen:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.preventcheckedoutcontentdeletion` | Boolean \(true/false\). <br> **Standaardwaarde**: `true` |

>[!TAB  Op locatie ]

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.xmleditor.config.XmlEditorConfig** bundel.

1. Selecteer de **Voorkomen Schrapping van Uitgecheckte Inhoud** optie.

   Deze optie is standaard ingeschakeld. Als deze optie is geselecteerd, kunnen gebruikers uitgecheckte bestanden niet verwijderen.

1. Klik **sparen**.


Ter ondersteuning van deze functie wordt een nieuwe index-eigenschap `drivelock` toegevoegd in `oak:index` :

`/oak:index/damAssetLucene/indexRules/dam:Asset/properties/drivelock`

![](assets/index-property-oak-index-drivelock.png){width="800" align="left"}

Controleer, naast de nieuwe eigenschap index, of de volgende eigenschappen zijn ingesteld op `/oak:index/damAssetLucene` :

- `jcr:primaryType`=`"oak:QueryIndexDefinition"`
- `async`=`"async"`
- `compatVersion`=`"{Long}2"`
- `evaluatePathRestrictions`=`"{Boolean}true"`
- `reindex`=`"{Boolean}false"`
- `reindexCount`= `"{Long}3"` *\ (dit is het aantal keren opnieuw indexeren wordt gedaan, wordt het vervangen met de installatie van ons pakket \)*
- `type`=`"lucene"`

>[!NOTE]
>
> U kunt de waarde van `reindex` wijzigen in `"{Boolean}true"` . Hierdoor worden sneller zoekresultaten mogelijk voor de uitgecheckte bestanden in een hiërarchie met mappen.

>[!ENDTABS]

## Verwijderen van bestanden waarnaar wordt verwezen voorkomen

Als beheerder kunt u bepalen wie bestanden uit de AEM-opslagplaats mag verwijderen. Als een bestand verwijzingen bevat of door een ander bestand wordt genoemd, kunt u met name bepalen wie dergelijke bestanden kan verwijderen.

Met deze configuratie kunt u toestaan of weigeren dat alle gebruikers bestanden verwijderen of alleen een bepaalde gebruikersgroep bestanden laten verwijderen. Als het verwijderen van een bestand is toegestaan, wordt het volgende proces uitgevoerd:

- Als u een map verwijdert, die alle bestanden bevat waarnaar wordt verwezen en waarnaar wordt verwezen, worden alle bestanden verwijderd. Het proces verwijdert eerst alle bestanden die geen verwijzingen bevatten, gevolgd door de bestanden die verwijzingen bevatten of waarnaar wordt verwezen.

- Als u een map verwijdert en naar een bestand in de map wordt verwezen door een bestand buiten die map, wordt u gevraagd de verwijzing te verwijderen voordat u het bestand verwijdert.

Op de volgende tabbladen vindt u instructies voor het verwijderen van een bestand dat verwijzingen bevat of waarnaar wordt verwezen door andere bestanden op basis van de Experience Manager Guides-instellingen: Cloud Service of On-Premise.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

Gebruik de instructies die in [&#x200B; worden gegeven met voeten treedt van de Configuratie &#x200B;](download-install-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\)-details op om te bepalen wie een bestand kan verwijderen dat verwijzingen bevat of waarnaar wordt verwezen door andere bestanden:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `block.unsafe.delete` | Mogelijke waarden zijn: <br> - allow\_unsafe\_delete\_for\_all <br> -   allow\_unsafe\_delete\_for\_delete\_assets\_group <br> - block\_unsafe\_delete\_for\_all <br> **Standaardwaarde**: `allow_unsafe_delete_for_delete_assets_group` <br> De details van deze constanten worden hieronder gegeven. |

Afhankelijk van wie u toegang voor verwijdering wilt geven, geeft u een van de volgende constanten op:

- allow\_unsafe\_delete\_for\_all: geef alle gebruikers toestemming om bestanden te verwijderen. In dit geval kunt u dergelijke bestanden ook met kracht verwijderen als het bestand\(en\) verwijzingen bevat of door andere bestanden wordt genoemd. Voordat u het bestand verwijdert, verschijnt er een bericht met de referenties waarin u wordt gevraagd of u de verwijderbewerking wilt annuleren, de verwijzingen wilt verwijderen en vervolgens het bestand wilt verwijderen. U kunt ook het bestand of de bestanden zonder geweld verwijderen zonder de referenties te verwijderen.

  ![](assets/allow_unsafe_delete-force-delete.PNG)

- allow\_unsafe\_delete\_for\_delete\_assets\_group: Een beheerder of een gebruiker die tot de *schrapping-activa* groep behoort wordt toegestaan om dossiers te schrappen. Als een andere gebruiker bestanden met verwijzingen probeert te verwijderen, is het hem niet toegestaan deze bestanden te verwijderen totdat alle referenties zijn verwijderd. De volgende schermafbeelding wordt weergegeven wanneer een gebruiker die geen machtigingen heeft, bestanden probeert te verwijderen.

  ![](assets/allow_unsafe_delete_for_delete_assets_group.PNG)

- block\_unsafe\_delete\_for\_all: Sta alle gebruikers \(inclusief beheerders\) niet toe bestanden te verwijderen totdat de verwijzingen naar en van het bestand\(en\) zijn verwijderd.

>[!TAB  Op locatie ]

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.config.ConfigManager** bundel.

1. Bepaal de plaats van de **Schrapping van het Blok voor Verwezen Assets** optie.

1. Afhankelijk van wie u toegang voor verwijdering wilt geven, geeft u een van de volgende constanten op:

   - allow\_unsafe\_delete\_for\_all: geef alle gebruikers toestemming om bestanden te verwijderen. In dit geval kunt u dergelijke bestanden ook met kracht verwijderen als het bestand\(en\) verwijzingen bevat of door andere bestanden wordt genoemd. Voordat u het bestand verwijdert, verschijnt er een bericht met de referenties waarin u wordt gevraagd of u de verwijderbewerking wilt annuleren, de verwijzingen wilt verwijderen en vervolgens het bestand wilt verwijderen. U kunt ook het bestand of de bestanden zonder geweld verwijderen zonder de referenties te verwijderen.

     ![](assets/allow_unsafe_delete-force-delete.PNG){width="550" align="left"}

   - allow\_unsafe\_delete\_for\_delete\_assets\_group: Een beheerder of een gebruiker die tot de *schrapping-activa* groep behoort wordt toegestaan om dossiers te schrappen. Als een andere gebruiker bestanden met verwijzingen probeert te verwijderen, is het hem niet toegestaan deze bestanden te verwijderen totdat alle referenties zijn verwijderd. De volgende schermafbeelding wordt weergegeven wanneer een gebruiker die geen machtigingen heeft, bestanden probeert te verwijderen.

     ![](assets/allow_unsafe_delete_for_delete_assets_group.PNG){width="550" align="left"}

   - block\_unsafe\_delete\_for\_all: Sta alle gebruikers \(inclusief beheerders\) niet toe bestanden te verwijderen totdat de verwijzingen naar en van het bestand\(en\) zijn verwijderd.

1. Klik **sparen**.

>[!ENDTABS]

## Oudere versies van DITA-bestanden wissen

Wanneer u inhoud bijwerkt en nieuwe versies maakt, blijven de vorige versies van DITA-bestanden behouden in de opslagplaats. Veel versies worden mogelijk gemaakt voor uw DITA-bestanden over een bepaalde periode en kunnen samen een grote hoeveelheid ruimte innemen in uw opslagplaats. Met AEM Guides kunt u de oudere versies configureren die uit de opslagplaats moeten worden verwijderd.

U hebt toegang tot dit hulpprogramma via de opgegeven URL als u beheerdersrechten hebt:

`<server folder path> /libs/fmdita/clientlibs/xmleditor_version_purge/page.html`

De versie van een DITA-bestand die aan een van de opgegeven criteria voldoet, blijft behouden en wordt niet gewist:

- Is de eerste versie van een bestand
- Is opgenomen in een basislijn
- Is inbegrepen in om het even welke vertaling of revisiewerkschema
- Er is een label op toegepast
- Voldoet aan de gedefinieerde leeftijd of het gedefinieerde aantal versiecriteria

Voer de volgende stappen uit om de oudere versies leeg te maken:

1. Voer de volgende gegevens in over de bestanden die u wilt leegmaken:

   ![](assets/preview-purge-report.png)

1. &#x200B;
   - **Aantal Versies om van de Laatste Versie** te behouden: ga het aantal versies in die zouden moeten worden behouden en niet worden gezuiverd. Als we bijvoorbeeld 5 invoeren, blijven de laatste 5 versies behouden en worden de versies vóór die versies gekwalificeerd om te worden gewist als aan andere zuiveringsvoorwaarden wordt voldaan.
   - **Behoud Versies die binnen Tijdopnemer \ (in Dagen \)** worden gecreeerd: Ga de maximumleeftijd van een versie in dagen in. De versies ouder dan het opgegeven aantal dagen zijn gekwalificeerd om te worden gewist als aan andere zuiveringsvoorwaarden wordt voldaan. Als we bijvoorbeeld 100 invoeren, kunnen alle versies die vóór 100 dagen zijn gemaakt, worden gewist als aan andere zuiveringsvoorwaarden wordt voldaan.
   - **Weg**: Selecteer de weg van het dossier of de omslag waarvan dossiers u wilt zuiveren.

     >[!NOTE]
     >
     > U kunt alleen DITA-bestanden leegmaken.

1. Klik **het Rapport van de Schoonmaak van de Voorproef**.

   >[!NOTE]
   >
   > Er kan slechts één zuiveringstaak tegelijk zijn. U kunt geen andere versiezuivering in werking stellen als één bezig is.

   Het rapport voor het verwijderen van de versie wordt gegenereerd.

1. Rapport voor het opschonen van versies downloaden en de bestanden en versies controleren die worden gewist.
1. U kunt verkiezen om **te annuleren Wissen** of **Wissen van het Begin**.

   ![](assets/download-purge-report.png)

   De status van leegmaken wordt weergegeven.

   Klik **Rapport van de Opruiming van de Versie van de Download** om de gezuiverde versies te bekijken. Dit rapport bevat de opschonende status voor alle versies, samen met de redenen waarom een bepaalde versie is behouden of waarom deze is gewist.


>[!NOTE]
>
> Het rapport wordt gedownload op de volgende locatie: `/var/dxml/versionpurge`
