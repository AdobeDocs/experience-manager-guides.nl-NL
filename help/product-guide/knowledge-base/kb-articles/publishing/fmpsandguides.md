---
title: Publiceren met gebruik van FrameMaker Publishing Server (FMPS) in AEM Guides
description: Publiceren met FMPS met AEM Guides
exl-id: 05d4d876-f83b-473c-bf31-14d6565e80e2
feature: AEM Guides FrameMaker Publishing Server
author: Pulkit Nagpal(punagpal)
role: User, Admin
source-git-commit: f971be4be9e2d32618616727cd9c682941dd3fb2
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 0%

---

# Publiceren met gebruik van FrameMaker Publishing Server (FMPS) in AEM Guides

AEM Guides-integratie met FrameMaker Publishing Server kan uw oplossing zijn als u op zoek bent naar geautomatiseerde publicatie van hoge kwaliteit.\
Met artikel kunt u FMPS instellen en uitvoeren met AEM Guides.

## Verenigbaarheid van FMPS met AEM Guides

- Verenigbaarheid met 4.1 AEM Guides: [ 4.1 verenigbaarheidsmatrijs ](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/tutorials/release-info/release-notes/on-prem-release-notes/release-notes-4.1.html?lang=en/#compatibility-matrix)
- Verenigbaarheid met 4.0 AEM Guides: [ 4.0 verenigbaarheidsmatrijs ](https://helpx.adobe.com/xml-documentation-for-experience-manager/release-note/release-notes-xml-documentation-solution-4-0.html/#Compatibility%20matrix)
- Laatste Versie: [ Latest versie info ](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/tutorials/release-info/latest-release-info.html?lang=en)

## Installatie

Raadpleeg de volgende secties voor installatie en configuratie van AEM Guides en FMPS

### AEM Guides

De installatie en de configuratie verwijzen: [ 4.1 installatie &amp; configuraties ](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/4-1-2/Adobe-Experience-Manager-Guides_Installation-Configuration-Guide_EN.pdf)

### FMPS

Voor installatie FMPS kunt u bepaalde [ verbinding van YouTube ](https://www.youtube.com/watch?v=2deelyM5VA8&amp;t) of [ installatie FMPS en configuratie ](https://help.adobe.com/en_US/framemaker/server/index.html#t=fmps-user-guide%2Finstall_config_fmps.html%23install_config_fmps&amp;rhtocid=_2) verwijzen

## Vereiste configuraties

U kunt FrameMaker Publishing Server (FMPS) gebruiken om uw DITA-inhoud te genereren. FMPS ondersteunt een groot aantal uitvoerindelingen. Wijzig de volgende eigenschappen van de bundel &quot;com.adobe.fmdita.config.ConfigManager&quot; in de Console van het Web om AEM Guides te vormen om FMPS te gebruiken.

Ga naar http://\&lt;servernaam\>:\&lt;poort\>/system/console/configMgr om de webconsole te openen.

**de eigenschappen van de Configuratie en hun beschrijving** [ 4.1 installatie en configuratie ](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/4-1-2/Adobe-Experience-Manager-Guides_Installation-Configuration-Guide_EN.pdf#page=89)

## Test uitvoeren:

Gebruikend FMPS, kunt u **PDF, Responsieve HTML**, en **Epub** voor uw DITA en FM Assets automatisch publiceren.

Kies FrameMaker Publishing Server in het menu &quot;PDF genereren met&quot;.

De gebruiker kan &quot;settings File(.sts)&quot; en &quot;ditaval&quot; opgeven. Filteren wordt uitgevoerd met ditaval op basis van de voorwaarden die u opgeeft.

- **plaatsend dossier**: Een FrameMaker /FMPS Publish die dossier plaatst dat alle montages bevat die u FMPS wilt respecteren wanneer het publiceren. U kunt bijvoorbeeld uitvoer maken met een aangepaste sjabloon, markeringen en aflooptekens maken (PDF) en PDF maken met inhoudsopgave.
- **vooraf ingesteld FMPS:** Het is vooraf bepaalde combinatie van ditaval en montageendossier. In plaats van afzonderlijke bestanden voor bewerkingen en instellingen te geven, kan de gebruiker vooraf een FMPS-voorinstelling maken die opnieuw kan worden gebruikt voor publicatiedoeleinden.

**Nota:** het standaardsysteem plaatsen wordt gebruikt door FMPS om te publiceren als u om het even welke montages of vooraf ingesteld FMPS niet kiest.

Dit is een conflict als u de FMPS-voorinstelling hebt gekozen en ook aangepaste instellingen of een tijdelijk bestand van AEM hebt opgegeven. In dit geval heeft de FMPS-voorinstelling voorrang op de aangepaste instellingen of het ditaval-bestand.

### Publiceren van basislijnen met FMPS:

U kunt uw reeds gemaakte basislijnen publiceren met versie FMPS2020.0.2 of hoger.

**de montageendossier van de Steekproef FMPS (.sts) om begonnen te worden:** [ de montagesdossier van de Steekproef FMPS ](https://acrobat.adobe.com/link/track?uri=urn:aaid:scds:US:ef750752-7a7e-4e51-923e-6b7d9861ed54) (unzip dit dossier)

## Veelgestelde vragen en problemen oplossen:

- ### FMPS-publicatie mislukt met &quot;Timeout Exception&quot;

>Controleer en verhoog de waarde van &quot;FMPS timeout&quot; (Seconden) in /system/console/configMgr/com.adobe.fmdita.config.ConfigManager&quot;

- ### Kan FMPS-voorinstelling niet ophalen in vervolgkeuzelijst

>Zorg ervoor dat er een vooraf gedefinieerde FMPS-voorinstelling op de server is gemaakt en dat de verbindingsinstellingen correct zijn.

- ### Ik krijg Lege PDF wanneer ik publiceer

>Als u UUID gebruikt, moet u de optie &quot;UUID-gebaseerde verwijzing gebruiken&quot; inschakelen in de voorkeuren voor FrameMakers bewerken en omgekeerd voor niet-UUID-AEM.

- ### Mijn instellingen/bewerkingen worden niet toegepast in de uiteindelijke gepubliceerde uitvoer

>Controleer of u niet tegelijkertijd de FMPS-voorinstelling en het instellings-/diaval-bestand kiest. Gebruik FrameMaker om de uitvoer handmatig te controleren.

- ### De basislijn wordt niet gepubliceerd vanuit FMPS

>FMPS2020.0.2 of latere versies zijn compatibel met publiceren op basislijn.
>Zorg ervoor dat uw basislijn correct is gemaakt; ga naar het Kaartdashboard— Onderwerpen— Download  Wijs en kies Basislijn gebruiken toe.
>- ### Publish-taken van FMPS nemen meer tijd in beslag dan andere engines
>Wanneer u publiceert vanuit FMPS, is de ideale vaste headertijd ongeveer 3-4 minuten. Neem contact op met uw FMPS-beheerder of neem contact op met de ondersteuning voor Adoben als u denkt dat deze langer duurt.

## Overige bronnen:

[ FMPS leren en Steun ](https://helpx.adobe.com/support/framemaker-publishing-server.html)

[ AEM Guides Leren en Steun ](https://helpx.adobe.com/in/support/xml-documentation-for-experience-manager.html)

[ FrameMaker en gemeenschap FMPS ](https://community.adobe.com/t5/framemaker/ct-p/ct-framemaker?page=1&amp;sort=latest_replies&amp;lang=all&amp;tabid=all)

[ Gemeenschap van AEM Guides ](https://experienceleaguecommunities.adobe.com/t5/experience-manager-guides/ct-p/aem-xml-documentation)
