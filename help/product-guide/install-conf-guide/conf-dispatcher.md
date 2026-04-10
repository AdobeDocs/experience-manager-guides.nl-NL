---
title: Dispatcher configureren
description: Leer hoe u Dispatcher kunt configureren
feature: Installation
role: Admin
level: Experienced
source-git-commit: 834959a6a0e22cd5d2b2c5d0e57ceb6d45c0c666
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 3%

---

# Dispatcher configureren {#id213BCM0M05U}

Als u van plan bent om een Dispatcher op de instantie van de Auteur van AEM samen met AEM Guides te gebruiken, dan moet u de volgende extra configuraties uitvoeren om opstelling te voltooien:

>[!NOTE]
>
> Dispatcher is de Adobe Experience Manager-tool voor cache- en taakverdelingsbewerkingen. Voor meer details over het gebruiken van Dispatcher, zie [&#x200B; Overzicht van Dispatcher &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/dispatcher.html?lang=en).

## EnableEncodedSlashes in URLs inschakelen

URL&#39;s met gecodeerde slashes zijn niet standaard ingeschakeld in de installatie van AEM-dispatcher, maar als u in AEM Guides werkt, moet u deze optie inschakelen. Om dit te doen, moet u de `AllowEncodedSlashes` parameter aan **op** in configuratie Apache zoals aangetoond in het volgende fragment plaatsen:

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

Wanneer u een Dispatcher met AEM Guides gebruikt, moet u ervoor zorgen dat de DITA-kaart en onderwerpbestanden als HTML worden gerenderd zodat auteurs de inhoud kunnen bekijken zoals ze \(in plaats van onbewerkte tekstindeling\) verwachten.

Voer de volgende stappen uit om het `mime.types` -bestand bij te werken:

1. Maak verbinding met de Dispatcher-server met SSH en blader naar het `httpd.conf` -bestand.

1. Controleer het pad van het `mime.types` -bestand.

1. Open het bestand `mime.types` en zoek naar &#39;&#39;text/html&#39;&#39;. De standaardtoewijzing voor &quot; text/html&quot; is:

   `text/html html htm`

1. Werk de afbeelding bij door ditamap- en dita-extensies toe te voegen als:

   `text/html html htm ditamap dita`

1. Sla het bestand op en sluit het.


Deze configuratieupdate zorgt ervoor dat de kaart DITA en onderwerpdossiers die door Dispatcher worden teruggegeven als HTML in Assets UI worden getoond.

## Aanvraag-URL voor gebruikersvoorkeuren toestaan

Als u een Dispatcher met AEM Guides gebruikt en uw instantie Auteur een verzender op de voorgrond heeft, brengt u de volgende twee wijzigingen aan:

- Whitelist de URL van de POST-aanvraag. Hieronder ziet u een voorbeeldregel `/filters` : Voeg deze regel toe aan het configuratiebestand van de verzender:

```json
/xxxx {/type "allow" /method "POST" /url "/home/users/*/preferences"}
```

- Zorg ervoor dat het URL-patroon `/libs/cq/security/userinfo.json` niet in de cache wordt geplaatst bij Auteur-dispatcher, dus voeg een regel `\(like below\)` in `author\_dispatcher.any` toe

```json
/xxxx {
                /glob "/libs/cq/security/userinfo.json"
                /type "deny"
                }
```

