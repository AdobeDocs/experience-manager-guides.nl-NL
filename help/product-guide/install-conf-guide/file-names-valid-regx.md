---
title: Regx configureren voor geldige bestandsnaamtekens
description: Leer hoe u Regx kunt configureren voor geldige bestandsnaamtekens
feature: Filename Configuration
role: Admin
level: Experienced
source-git-commit: 6f3f05419f4f5cdd45ab580cdee6fa869f20f01d
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# Regx configureren voor geldige bestandsnaamtekens {#id214BD0550E8}

Vanaf AEM Guides 3.8 kunt u als beheerder een lijst met geldige speciale tekens definiëren die zijn toegestaan in bestandsnamen. In eerdere versies mochten gebruikers bestandsnamen definiëren die speciale tekens bevatten, zoals `@` , `$` , `>` en meer. Deze speciale karakters resulteerden in kwesties terwijl het openen van onderwerpen van het dashboard van de kaart DITA of het klikken op de verbinding van onderwerp in TOC, die vaak in resulteerden dat de pagina niet wegens speciale karakters in URL werd geopend.

Gebruikend de configuratie die u toestaat om een regx voor geldige dossier te bepalen - noem karakters, hebt u volledige controle op hoe de dossiers intern in het systeem worden genoemd. U kunt een lijst met speciale tekens definiëren die zijn toegestaan in de bestandsnamen. Standaard bevat de geldige bestandsnaamconfiguratie &quot;`a-z A-Z 0-9 - _`&quot;. Tijdens het creëren van een nieuw dossier, kunt u om het even welk speciaal karakter in de titel van het dossier hebben, maar intern zal het met &quot;`-`&quot;in de dossiernaam worden vervangen. U kunt bijvoorbeeld de bestandstitel &quot;Introduction 1&quot; of &quot;Introduction@1&quot; hebben. De overeenkomstige bestandsnaam die voor beide gevallen wordt gegenereerd, is &quot;Introduction-1&quot;.

Wanneer u een lijst van geldige karakters bepaalt, herinner dat deze karakters &quot;`*/:[\]|#%{}?&<>"/+`&quot;altijd met &quot;`-`&quot;zullen worden vervangen.

Als u de geldige lijst met speciale tekens niet configureert, kan het maken van bestanden onverwachte resultaten opleveren. Om dergelijke fouten te vermijden, wordt sterk geadviseerd om deze configuratieverandering aan te brengen.

Op de volgende tabbladen vindt u instructies voor het configureren van Regx voor geldige bestandsnaamtekens op basis van uw Experience Manager Guides-instellingen: Cloud Service of On-Premise.


>[!BEGINTABS]

>[!TAB  Cloud Service ]

Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](download-install-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\) gegevens op om regex te configureren voor geldige bestandsnaamtekens:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `valid.characters` | De waarde is een regex-patroon. Het moet drie basistekens hebben en de lijst moet met een koppelteken \ (-\) beginnen.<br> **Standaardwaarde**: \[-a-zA-Z0-9\_\] |

>[!NOTE]
>
> Net als in de lijst met geldige bestandsnaamtekens kunt u ook een lijst met geldige bestandsnaamtekens opgeven voor uitvoer van de AEM-site. Voor meer details, zie [ geldige dossiernamen voor de output van de Plaats van AEM ](conf-file-names-valid-regx-aem-site-output.md#) vormen.

>[!TAB  Op locatie ]

Voer de volgende stappen uit om regx te configureren voor geldige \(of toegestane\) tekens in bestandsnamen:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op *com.adobe.fmdita.config.ConfigManager* bundel.

1. In **Regex voor Geldige het bezit van Karakters**, zorg ervoor dat het bezit aan \ [-a-zA-Z0-9 \ \ \ wordt geplaatst. U kunt meer tekens aan deze lijst toevoegen. De lijst moet echter deze basistekens hebben en de lijst moet beginnen met een koppelteken &quot;-&quot;.

   >[!NOTE]
   >
   > Deze eigenschap is alleen van toepassing op bestandsnamen en niet op mapnamen.

1. Klik **sparen**.


>[!NOTE]
>
> Net als in de lijst met geldige bestandsnaamtekens kunt u ook een lijst met geldige bestandsnaamtekens opgeven voor uitvoer van de AEM-site. Voor meer details, zie [ geldige dossiernamen voor de output van de Plaats van AEM ](conf-file-names-valid-regx-aem-site-output.md#) vormen.

>[!ENDTABS]
