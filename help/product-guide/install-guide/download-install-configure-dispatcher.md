---
title: Dispatcher configureren
description: Leer hoe u Dispatcher kunt configureren
exl-id: 525de1c3-5a79-4d65-89b4-ca05ae660c2c
feature: Installation
role: Admin
level: Experienced
source-git-commit: 0513ecac38840a4cc649758bd1180edff1f8aed1
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 3%

---

# Dispatcher configureren {#id213BCM0M05U}

Als u van plan bent om een Dispatcher op AEM instantie van de Auteur samen met AEM Guides te gebruiken, dan moet u de volgende extra configuraties uitvoeren om opstelling te voltooien:

>[!NOTE]
>
> Dispatcher is de Adobe Experience Manager-tool voor cache- en taakverdelingsbewerkingen. Voor meer details over het gebruiken van Dispatcher, zie [ Overzicht van Dispatcher ](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/dispatcher.html?lang=nl-NL).

## EnableEncodedSlashes in URLs inschakelen

URL&#39;s met gecodeerde schuine strepen zijn standaard niet ingeschakeld in AEM dispatcherinstellingen, maar als u in AEM Guides werkt, moet u deze optie inschakelen. Hiervoor moet u de parameter AllowEncodedSlashes instellen op Aan in Apache-configuratie, zoals in het volgende fragment wordt getoond:

```XML
<VirtualHost *:80>
                ServerName www.geometrixx-outdoors.com
                **AllowEncodedSlashes On**
                <Directory />
                <IfModule disp_apache2.c>
                SetHandler dispatcher-handler
                </IfModule>
                Options FollowSymLinks
                AllowOverride None
                </Directory>
                </VirtualHost>
            
```

## Het bestand mime.types configureren voor DITA

Wanneer u een Dispatcher met AEM Guides gebruikt, moet u ervoor zorgen dat de DITA-kaart en onderwerpbestanden worden gerenderd als HTML zodat auteurs de inhoud kunnen bekijken zoals ze \(in plaats van onbewerkte tekstindeling\) verwachten.

Voer de volgende stappen uit om het bestand mime.types bij te werken:

1. Maak verbinding met de Dispatcher-server met SSH en blader naar het bestand httpd.conf.

1. Controleer het pad van het bestand &quot; mime.types&quot;.

1. Open het bestand mime.types en zoek naar &quot; text/html&quot;. De standaardtoewijzing voor &quot; text/html&quot; is:

   `text/html html htm`

1. Werk de afbeelding bij door ditamap- en dita-extensies toe te voegen als:

   `text/html html htm ditamap dita`

1. Sla het bestand op en sluit het.


Deze configuratieupdate zorgt ervoor dat de kaart DITA en onderwerpdossiers die door Dispatcher worden teruggegeven als HTML in Assets UI worden getoond.

## Aanvraag-URL voor gebruikersvoorkeuren toestaan

Als u een Dispatcher met AEM Guides gebruikt en uw instantie Auteur een verzender op de voorgrond heeft, brengt u de volgende twee wijzigingen aan:

- Whitelist de POST verzoek URL. Hieronder ziet u een voorbeeldregel &quot; `/filters`&quot; - Deze regel toevoegen aan het configuratiebestand van de verzender:

```json
/xxxx {/type "allow" /method "POST" /url "/home/users/*/preferences"}
```

- Controleer of het URL-patroon &quot; /libs/cq/security/userinfo.json&quot; niet in de cache is opgeslagen bij de auteur-dispatcher. Voeg daarom een regel \(zoals hieronder\) toe in de auteur\_dispatcher.any

```json
/xxxx {
                /glob "/libs/cq/security/userinfo.json"
                /type "deny"
                }
```

**Bovenliggend onderwerp:**&#x200B;[ Download en installeer ](download-install.md)
