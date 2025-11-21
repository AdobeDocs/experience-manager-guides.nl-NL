---
title: Publiceren met FrameMaker Publishing Server(FMPS) in AEM Guides
description: Publiceren met FMPS met AEM Guides
exl-id: 05d4d876-f83b-473c-bf31-14d6565e80e2
feature: AEM Guides FrameMaker Publishing Server
author: Pulkit Nagpal(punagpal)
role: User, Admin
source-git-commit: 6e23f52fc9124d0f07f8108da1b5fe574f553469
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 0%

---

# Publiceren met FrameMaker Publishing Server(FMPS) in AEM Guides

AEM Guides-integratie met FrameMaker Publishing Server kan uw oplossing zijn als u op zoek bent naar geautomatiseerde publicatie van hoge kwaliteit.\
Met artikel kunt u FMPS instellen en uitvoeren met AEM Guides.

## Verenigbaarheid van FMPS met AEM Guides

- Verenigbaarheid met 4.1 AEM Guides: [&#x200B; 4.1 verenigbaarheidsmatrijs &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/tutorials/release-info/release-notes/on-prem-release-notes/release-notes-4.1.html?lang=nl-NL/#compatibility-matrix)
- Verenigbaarheid met 4.0 AEM Guides: [&#x200B; 4.0 verenigbaarheidsmatrijs &#x200B;](https://helpx.adobe.com/xml-documentation-for-experience-manager/release-note/release-notes-xml-documentation-solution-4-0.html/#Compatibility%20matrix)
- Laatste Versie: [&#x200B; Latest versie info &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/tutorials/release-info/latest-release-info.html?lang=nl-NL)

## Installatie

Raadpleeg de volgende secties voor installatie en configuratie van AEM Guides en FMPS

### AEM Guides

De installatie en de configuratie verwijzen: [&#x200B; 4.1 installatie &amp; configuraties &#x200B;](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/4-1-2/Adobe-Experience-Manager-Guides_Installation-Configuration-Guide_EN.pdf)

### FMPS

Voor installatie FMPS kunt u bepaalde [&#x200B; verbinding van YouTube &#x200B;](https://www.youtube.com/watch?v=2deelyM5VA8&t) of [&#x200B; installatie FMPS en configuratie &#x200B;](https://help.adobe.com/en_US/framemaker/server/index.html#t=fmps-user-guide%2Finstall_config_fmps.html%23install_config_fmps&rhtocid=_2) verwijzen

## Vereiste configuraties

FrameMaker Publishing Server (FMPS) kan worden gebruikt om uw DITA-inhoud te genereren. FMPS ondersteunt een groot aantal uitvoerindelingen. Wijzig de volgende eigenschappen van de bundel &quot;com.adobe.fmdita.config.ConfigManager&quot; in de Console van het Web om AEM Guides te vormen om FMPS te gebruiken.

Ga naar http://\&lt;servernaam\>:\&lt;poort\>/system/console/configMgr om de webconsole te openen.

**de eigenschappen van de Configuratie en hun beschrijving** [&#x200B; 4.1 installatie en configuratie &#x200B;](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/4-1-2/Adobe-Experience-Manager-Guides_Installation-Configuration-Guide_EN.pdf#page=89)

## Test uitvoeren:

Gebruikend FMPS, kunt u **PDF, Responsieve HTML5**, en **Epub** voor uw DITA en FM Assets automatisch publiceren.

Kies FrameMaker Publishing Server in het menu &#39;PDF genereren met&#39;.

De gebruiker kan &quot;settings File(.sts)&quot; en &quot;ditaval&quot; opgeven. Filteren wordt uitgevoerd met ditaval op basis van de voorwaarden die u opgeeft.

- **plaatsend dossier**: Een FrameMaker /FMPS publiceert plaatsend dossier dat alle montages bevat die u FMPS wilt respecteren wanneer het publiceren. U kunt bijvoorbeeld uitvoer maken met een aangepaste sjabloon, Markeringen en aflooptekens maken (PDF) en PDF maken met inhoudsopgave.
- **vooraf ingesteld FMPS:** Het is vooraf bepaalde combinatie van ditaval en montageendossier. In plaats van afzonderlijke bestanden voor bewerkingen en instellingen te geven, kan de gebruiker vooraf een FMPS-voorinstelling maken die opnieuw kan worden gebruikt voor publicatiedoeleinden.

**Nota:** het standaardsysteem plaatsen wordt gebruikt door FMPS om te publiceren als u om het even welke montages of vooraf ingesteld FMPS niet kiest.

Dit is een conflict als u de FMPS-voorinstelling hebt gekozen en ook aangepaste instellingen of een tijdelijk bestand uit AEM hebt opgegeven. In dit geval heeft de FMPS-voorinstelling voorrang op de aangepaste instellingen of het ditaval-bestand.

### Publiceren van basislijnen met FMPS:

U kunt uw reeds gemaakte basislijnen publiceren met versie FMPS2020.0.2 of hoger.

**de montageendossier van de Steekproef FMPS (.sts) om begonnen te worden:** [&#x200B; de montagesdossier van de Steekproef FMPS &#x200B;](https://acrobat.adobe.com/link/track?uri=urn:aaid:scds:US:ef750752-7a7e-4e51-923e-6b7d9861ed54) (unzip dit dossier)

## Veelgestelde vragen en problemen oplossen:

- ### FMPS-publicatie mislukt met &quot;Timeout Exception&quot;

>Controleer en verhoog de waarde van &quot;FMPS timeout&quot; (Seconden) in /system/console/configMgr/com.adobe.fmdita.config.ConfigManager&quot;

- ### Kan FMPS-voorinstelling niet ophalen in vervolgkeuzelijst

>Zorg ervoor dat er een vooraf gedefinieerde FMPS-voorinstelling op de server is gemaakt en dat de verbindingsinstellingen correct zijn.

- ### Ik krijg lege PDF&#39;s bij publicatie

>Als u UUID gebruikt, moet u de optie &quot;Op UUID gebaseerde verwijzing gebruiken&quot; in de voorkeuren voor FrameMaker-bewerking inschakelen en omgekeerd voor niet-UUID AEM-hulplijnen.

- ### Mijn instellingen/bewerkingen worden niet toegepast in de uiteindelijke gepubliceerde uitvoer

>Controleer of u niet tegelijkertijd de FMPS-voorinstelling en het instellings-/diaval-bestand kiest. Gebruik FrameMaker om de uitvoer handmatig te controleren.

- ### De basislijn wordt niet gepubliceerd vanuit FMPS

>FMPS2020.0.2 of latere versies zijn compatibel met publiceren op basislijn.
>Zorg ervoor dat uw basislijn correct is gemaakt; ga naar het Kaartdashboard— Onderwerpen— Download  Wijs en kies Basislijn gebruiken toe.

- ### Het publiceren van taken van FMPS kost meer tijd dan andere engines

>Wanneer u publiceert vanuit FMPS, is de ideale vaste headertijd ongeveer 3-4 minuten. Neem contact op met uw FMPS-beheerder of neem contact op met de ondersteuning van Adobe als u denkt dat deze langer duurt.

## Overige bronnen:

[&#x200B; FMPS leren en Steun &#x200B;](https://helpx.adobe.com/nl/support/framemaker-publishing-server.html)

[&#x200B; AEM Guides Leren en Steun &#x200B;](https://helpx.adobe.com/in/support/xml-documentation-for-experience-manager.html)

[&#x200B; FrameMaker en gemeenschap FMPS &#x200B;](https://community.adobe.com/t5/framemaker/ct-p/ct-framemaker?page=1&sort=latest_replies&lang=all&tabid=all)

[&#x200B; Gemeenschap van AEM Guides &#x200B;](https://experienceleaguecommunities.adobe.com/t5/experience-manager-guides/ct-p/aem-xml-documentation)
