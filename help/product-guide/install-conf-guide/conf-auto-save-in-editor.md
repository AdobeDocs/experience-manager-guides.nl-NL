---
title: Bestanden automatisch opslaan in de webeditor configureren
description: Leer hoe te om dossier te vormen automatisch sparen in de Redacteur van het Web
feature: Web Editor Configuration
role: Admin
level: Experienced
exl-id: 142a588a-3d26-48ee-a3fe-23882922243c
source-git-commit: 9c53ac725618db1164b0ed310a47b258a7224778
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---

# Bestanden automatisch opslaan in de webeditor configureren {#id199CC0J0M5Z}

Een van de meest gebruikte functies in de op een browser gebaseerde editor is de mogelijkheid om gegevens na een bepaalde tijdsperiode op te slaan. De redacteur van het Web van AEM Guides steunt ook auto-sparen van onderwerp en kaartdossiers bij het gespecificeerde tijdinterval. Wanneer deze eigenschap wordt teweeggebracht, wordt het werkende exemplaar van het onderwerp of de kaart bewaard. Er wordt geen nieuwe versie van het onderwerp of de kaart gemaakt. Als u een nieuwe versie wilt maken, klikt u op het pictogram Revisie opslaan op de werkbalk van de webeditor.

De functie voor automatisch opslaan is niet standaard ingeschakeld en u moet deze functie inschakelen in het configuratiebestand voor Cloud Service en in het menu `configMgr` voor Op locatie.

Op de volgende tabbladen vindt u instructies voor het inschakelen van de functie voor automatisch opslaan in de webeditor op basis van uw Experience Manager Guides-instellingen: Cloud Service of Op locatie.

>[!BEGINTABS]

>[!TAB  Cloud Service ]

Gebruik de instructies die in [ worden gegeven met voeten treedt van de Configuratie ](download-install-config-override.md#) om het configuratiedossier tot stand te brengen. Geef in het configuratiebestand de volgende \(eigenschap\) gegevens op om het automatisch opslaan van het bestand en het automatisch opslaan van het tijdinterval te configureren:

| PID | Eigenschappensleutel | Waarde van eigenschap |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.autosave` | Boolean \(true/false\).<br> **Standaardwaarde**: vals |
| `xmleditor.autosaveinterval` | Geef het tijdsinterval in seconden op om de functie voor automatisch opslaan te activeren. |  |

>[!TAB  Op locatie ]

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.xmleditor.config.XmlEditorConfig** bundel.

1. In de *montages 0} XmlEditorConfig, selecteer* Auto sparen **optie.**

1. Op het **Auto sparen het gebied van het Interval**, specificeer het tijdinterval in seconden om de auto-sparen eigenschap teweeg te brengen.

1. Klik **sparen**.

>[!ENDTABS]
