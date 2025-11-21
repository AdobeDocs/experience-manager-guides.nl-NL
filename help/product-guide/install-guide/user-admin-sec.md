---
title: Beheer en beveiliging van gebruikers
description: Leer hoe gebruikersbeheer en beveiliging werken
exl-id: 1269a652-5261-413d-9ea0-b4f75003e9d8
feature: User Management
role: Admin
level: Experienced
source-git-commit: 6e23f52fc9124d0f07f8108da1b5fe574f553469
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 0%

---

# Beheer en beveiliging van gebruikers {#id181AED00G5Z}

Als u functies in AEM Guides wilt openen en configureren, moet u gebruikers maken. Aan deze gebruikers kunnen vervolgens machtigingen worden toegewezen voor toegang tot alle of specifieke functies in AEM Guides. Leer hoe u gebruikersautorisatie configureert en handhaaft en ook de theorie achter hoe verificatie en autorisatie in AEM werken.

De volgende onderwerpen in de documentatie van AEM zullen u helpen de gebruikersbeleid en veiligheid-gerelateerde concepten en eigenschappen begrijpen:

- [&#x200B; Gebruikers en Groepen in AEM &#x200B;](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/security.html#UsersandGroupsinAEM)

- [&#x200B; Toestemmingen in AEM &#x200B;](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/security.html#PermissionsinAEM)

- [&#x200B; het Leiden Gebruikers en Groepen &#x200B;](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/security.html#ManagingUsersandGroups)

- [&#x200B; het Leiden Toestemmingen &#x200B;](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/security.html#ManagingPermissions)


## Gebruikersgroepen gemaakt door AEM Guides {#id181TF0K0MHT}

AEM Guides biedt drie groepen buiten de doos. Deze groepen zijn: *Auteurs*, *Recensenten*, en *Uitgevers*. Afhankelijk van de groep waaraan een gebruiker is gekoppeld, mogen deze specifieke taken uitvoeren. Zo kan het publiceren alleen worden uitgevoerd door een uitgever, maar niet door een auteur of een revisor. Op dezelfde manier kan een auteur een nieuw onderwerp tot stand brengen, en een recensent kan slechts een onderwerp herzien.

>[!TIP]
>
> Zie de *sectie van Toestemmingen* in de Beste praktijken gids voor beste praktijken rond het plaatsen van gebruikerstoestemmingen.

De volgende lijst maakt een lijst van diverse taken en de groepen die die taken kunnen uitvoeren:

| Taak | Auteurs | Revisoren | Uitgevers |
|----|-------|---------|----------|
| DITA-onderwerp maken | Ja |   | Ja |
| DITA-kaart maken | Ja |   | Ja |
| Verzamelingen toewijzen | Ja |   | Ja |
| Revisietaak maken | Ja |   | Ja |
| Het Onderwerp van het overzicht [&#x200B; 1 &#x200B;](#fntarg_1) | Ja | Ja | Ja |
| Belangrijkste resolutie | Ja |   | Ja |
| Openen in FrameMaker | Ja |   | Ja |
| Uitchecken/Inchecken | Ja |   | Ja |
| Onderwerp bewerken | Ja |   | Ja |
| Onderwerp verplaatsen | Ja |   | Ja |
| Eigenschappen van onderwerp bewerken | Ja |   | Ja |
| Kopiëren | Ja |   | Ja |
| Verwijderen | Ja |   | Ja |
| Delen | Ja |   | Ja |
| **de staat van het Document** |  |  |  |
| Profiel documentstatus maken/bewerken |   |   | Ja |
| De documentstaat van de verandering [&#x200B; 2 &#x200B;](#fntarg_2) | Ja | Ja | Ja |
| **Eigenschappen beschikbaar in DITA kaartconsole \ (Output stelt lusje \ vooraf in)** |  |  |  |
| Genereren |   |   | Ja |
| Bewerken |   |   | Ja |
| Dupliceren |   |   | Ja |
| Maken |   |   | Ja |
| Voorinstelling verwijderen |   |   | Ja |
| **Eigenschappen beschikbaar in DITA kaartconsole \ (Output tabel \)** |  |  |  |
| Gegenereerde uitvoer weergeven | Ja |   | Ja |
| **Eigenschappen beschikbaar in DITA kaartconsole \ (Onderwerpen lusje \)** |  |  |  |
| Revisietaak maken | Ja |   | Ja |
| Bewerken | Ja |   | Ja |
| **Eigenschappen beschikbaar in DITA kaartconsole \ (het lusje van Basislijnen \)** |  |  |  |
| Maken |   |   | Ja |
| Bewerken |   |   | Ja |
| Dupliceren |   |   | Ja |
| Verwijderen |   |   | Ja |
| DITA-kaartconsole \(tabblad Rapporten\) | Ja |   | Ja |
| **Eigenschappen beschikbaar in DITA kaartconsole \ (Voorinstellingen van de Voorwaarde \)** |  |  |  |
| Voorinstelling voorwaarde maken/bewerken |   |   | Ja |

## Aanvullende opmerkingen over gebruikersgroepen

De volgende lijst bevat enkele aanbevelingen en punten die betrekking hebben op gebruikersgroepen en de bijbehorende machtigingen:

- Als u een gebruiker de vertaling of het overzichtswerkschema wilt beginnen, zorg ervoor dat de gebruiker een lid van de *Uitgevers* en *project-beheerders groep* is.

- Gebruikers moeten beschikken over de machtigingen voor lezen, maken, verwijderen en wijzigen die beschikbaar zijn in de mappen voor de bron- en doeltaal waaraan zij moeten werken.

- Als u een project creeert, bent u de eigenaar van het project met *toestemmingen van de Uitgevers*. Andere gebruikers in een project kunnen hun teamleden alleen zien, taken maken of workflows maken als ze lees- en schrijftoegang hebben op knooppunten `/home/users` en `/home/groups` . Een manier om leestoegang te geven op `/home/users` - en `/home/groups` -knooppunten is door leestoegang te geven tot de `projects-users` -groep.

- *de recensenten* kunnen tot revisiecommentaren op een onderwerp toegang hebben en toevoegen onder overzicht van de console van het Project of van inbox berichtverbinding. Deze toegang is ook alleen beschikbaar tot de tijd dat de revisietaak is geopend.

- Door gebrek, *worden de Uitgevers van 0&rbrace; toegang en toestemmingen verleend op de volgende omslagen in DAM:*

   - ``/var/dxml``-\> Lezen en schrijven

   - `/content/dam/fmdita-outputs` -\> Lezen en schrijven

   - `/content/output/sites` -\> Lezen en schrijven

  U moet expliciete lees- en schrijfmachtigingen aan uw uitgever geven als u een andere locatie gebruikt dan de hierboven vermelde standaardpublicatielocaties.

- Alle gebruikers onder *Auteurs*, *Recensenten*, en *Uitgevers* groepen hebben lees toegang op alle inhoud in DAM.

- Machtigingen op mapniveau moeten aan gebruikers worden toegewezen via de pagina voor gebruikersbeheer.

- Als u uw gebruikers onderzoeksverrichtingen op DAM wilt kunnen uitvoeren, dan maak uw gebruikers een lid van de *dam-gebruikers* groep.

- Als u beheerderrechten aan om het even welke gebruiker wilt geven, kunt u dit doen door hen toegang door AEM standaardgroepen zoals *te geven* beheerders *, of de configuratie \ van OSGI (de console \ van Felix).*

- Als u een gebruiker rechten wilt geven om een documentstatus te wijzigen, moet u de gebruiker toevoegen in het gedeelte over statusovergang van het documentstatusprofiel.

[&#x200B; 1 &#x200B;](#fnsrc_1) als *Auteurs* en *Uitgevers* voor een overzicht worden uitgenodigd.[&#x200B; 2 &#x200B;](#fnsrc_2) afhankelijk van de rechten die aan de gebruiker in het profiel van de documentstaat worden gegeven.
