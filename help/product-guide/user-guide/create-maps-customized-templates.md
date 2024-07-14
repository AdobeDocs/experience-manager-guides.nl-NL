---
title: Kaarten maken op basis van aangepaste sjablonen
description: Leer een aangepaste sjabloon te maken, deze te gebruiken om nieuwe kaartbestanden te maken en de gedefinieerde titel door te geven aan een DITA-kaart in AEM Guides.
exl-id: 9cb0035f-bf81-4ab5-a575-53851bbff494
feature: Authoring, Map Editor
role: User
source-git-commit: be06612d832785a91a3b2a89b84e0c2438ba30f2
workflow-type: tm+mt
source-wordcount: '1103'
ht-degree: 0%

---

# Kaarten maken op basis van aangepaste sjablonen {#id225VF0808MP}

U kunt aangepaste kaartmalplaatjes tot stand brengen en hen gebruiken om kaarten DITA samen met de onderwerpmalplaatjes en kaartmalplaatjes tot stand te brengen die in het kaartmalplaatje van verwijzingen worden voorzien

U kunt naar andere kaartmalplaatjes en onderwerpmalplaatjes van het aangepaste kaartmalplaatje verwijzen. De genoemde kaartmalplaatjes kunnen naar diverse kaartmalplaatjes, onderwerpmalplaatjes, onderwerpen, kaarten, beelden, video&#39;s, en andere activa verwijzen. Het aangepaste kaartsjabloon kan u zeer gemakkelijk helpen de kaartsjablonen en de volledige doorverwezen omslagstructuur te herhalen. Deze aangepaste sjablonen zijn vooral handig voor het maken en opnieuw maken van meerdere kaarten met recursieve structuren en verwijzingen.

>[!NOTE]
>
> Onderwerpsjablonen worden niet recursief gemaakt. Slechts onderwerpmalplaatjes die direct binnen het kaartmalplaatje zijn worden geproduceerd en om het even welk onderwerpmalplaatje binnen een onderwerpmalplaatje wordt eenvoudig bedoeld in de ouder direct.

## Aangepaste sjablonen maken

Met AEM Guides kunt u aangepaste mappen en onderwerpen maken in de map dita-templates. U kunt deze aangepaste malplaatjes gebruiken om uw kaart en onderwerp tot stand te brengen. U kunt deze sjablonen ook met uw auteurs delen en deze gebruiken om hun bestanden te maken. Met behulp van deze sjablonen kunt u de auteurs toestaan afzonderlijke kopieën te maken van bepaalde bronnen die zich in de sjabloonmap bevinden.

>[!NOTE]
>
> Bronnen die alleen worden doorverwezen naar en behouden over, moeten zich buiten de sjabloonmap bevinden.


U kunt kaart en onderwerpmalplaatjes op de volgende manieren tot stand brengen:
1. De ruit van Malplaatjes van het [ Linkerpaneel ](./web-editor-features.md#left-panel-id2051ea0m0hs)
1. [Sjablonen in gebruikersinterface van Assets](#templates-assets-ui)
1. [Menu Opties](#templates-in-assets-ui)

### Sjablonen in gebruikersinterface van Assets {#templates-assets-ui}

**malplaatje van het Onderwerp**

Voer de volgende stappen uit om een onderwerpmalplaatje tot stand te brengen:

1. In **Assets UI**, navigeer aan de dita-malplaatjemap.

   ![](images/dita-templates.png){width="800" align="left"}

1. Klik **onderwerpen** omslag om het te openen.Klik **creeer \> Sjabloon DITA**.
1. Voor de pagina van de Vervaging, selecteer **Onderwerp** en klik dan **daarna.**
1. Voor de pagina van Eigenschappen, specificeer de onderwerpmalplaatje **Titel**.
1. Specificeer het dossier **Naam**

   >[!NOTE]
   >
   > De bestandsnaam moet de extensie .dita hebben.

1. \(Optioneel\) Voeg een beschrijving toe.
1. Klik **creëren**. Het onderwerpmalplaatje creeerde bericht verschijnt. U kunt het onderwerpmalplaatje dan openen en het uitgeven.

**malplaatje van de Kaart**

Voer de volgende stappen uit om een kaartsjabloon te maken:

1. In **Assets UI**, navigeer aan de dita-malplaatjemap.
1. Klik **kaarten** omslag om het te openen.
1. Klik **creeer \> Sjabloon DITA.**

   ![](images/create-dita-template.png){width="300" align="left"}

1. Voor de pagina van de Vervaging, uitgezochte **Kaart** en klik **daarna**.
1. Voor de pagina van Eigenschappen, specificeer de kaartsjabloon **Titel**.
1. Specificeer het dossier **Naam**.

   >[!NOTE]
   >
   > De bestandsnaam moet de extensie .ditamap hebben.

1. (Facultatief \) voeg een beschrijving toe.Klik **creeer**. Het bericht voor het maken van de kaartsjabloon wordt weergegeven. Vervolgens kunt u de kaartsjabloon openen en bewerken. U kunt de verwijzingen voor de onderwerpmalplaatjes, kaartmalplaatjes, en ook andere activa in het kaartmalplaatje toevoegen.

### Menu Opties {#options-menu}

Voer de volgende stappen uit om een kaart- of onderwerpsjabloon te maken:

1. Selecteer de **omslag van de Kaart** of **Onderwerp** in de huidige malplaatjemap. Bijvoorbeeld de map `dita-templates`.
1. Van het **menu van Opties**, creeer **het Malplaatje van de Kaart** of **creeer het Malplaatje van het Onderwerp**.

   **creeer Nieuw Malplaatje van de Kaart** of **creeer Nieuw Malplaatje van het Onderwerp** dialoog opent.
1. Voer de titel en de naam van de nieuwe sjabloon in.
1. Kies het type van malplaatje dat u van de **drop-down lijst van het Malplaatje** wilt tot stand brengen.

Het bericht voor het maken van de kaartsjabloon wordt weergegeven. U kunt de sjabloon toevoegen aan uw algemene profiel of mapprofiel. Het nieuwe malplaatje verschijnt dan in het onderwerp of kaartverwezenlijking proces, en u kunt kaarten of onderwerpen tot stand brengen gebruikend het.


Uw beheerder kan ook een map maken en deze zo configureren dat deze de map is waarin u de sjablonen kunt maken en opslaan.

Gebaseerd op uw opstelling leert hoe te om de weg van de malplaatjeomslag van douaneDITA te vormen:
<details>
    <summary> Cloud Servicen </summary>

Leer hoe te om [ de weg van de malplaatjemap van douaneDITA ](../install-guide/conf-template-tags-custom-dita-topic-template.md#configure-custom-dita-template-folder-path-id191lcf0095z) in de Gids van de Installatie en van de Configuratie van Cloud Servicen te vormen.
</details>

<details>
    <summary> Software op locatie</summary>

Leer hoe te om [ de weg van de malplaatjeomslag van douaneDITA ](../cs-install-guide/conf-template-tags-custom-dita-topic-template.md#configure-custom-dita-template-folder-path-id191lcf0095z) in de Gids van de Installatie en van de Configuratie op locatie te vormen.
</details>

## De titel doorgeven die is gedefinieerd in de sjablonen

Als u de titel van het onderwerp of de kaart wilt doorgeven die binnen uw malplaatje wordt gebruikt aan de kaarten DITA die gebruikend dat malplaatje worden gecreeerd, gebruiks gekrulde steunen rond de titel.

Voorbeeld

```XML
<pubtitle>
   <mainpubtitle outputclass="booktitle">
   {title}
   </mainpubtitle>
   <subtitle>Subtitle</subtitle>
</pubtitle>

The resultant DITA map with title "Rootmap1" will look like as follows:
<pubtitle>
   <mainpubtitle outputclass="booktitle">Rootmap1
   </mainpubtitle>
   <subtitle>Subtitle</subtitle>
</pubtitle>
```

>[!NOTE]
> Alleen het eerste exemplaar van de accolade wordt vervangen door een titel.

Als u geen krullende haakjes rond de titel gebruikt zal de resulterende kaart DITA slechts het eerste element worden gekozen en het nesten van de titel zal niet van het malplaatje worden gekozen en het zal als volgt kijken:

```XML
<pubtitle> Rootmap1 </pubtitle>
```

>[!NOTE]
> U kunt ook de accolades rondom de tekst gebruiken om de geneste structuur van de aangepaste sjablonen door te geven aan uw DITA-kaarten.

Voorbeeld

```XML
<title>    
    <sub>        
        <b>{title}</b>    
    </sub>
</title>
```




## De kaartsjabloon gebruiken om nieuwe kaarten te maken

>[!NOTE]
>
> Het kaartmalplaatje moet voor creatie door uw beheerder worden gevormd en ter beschikking gesteld. Voor meer details, zie *authoring malplaatjes* sectie in installeer en vorm as a Cloud Service Adobe Experience Manager Guides.

Voer de volgende stappen uit om een kaart te creëren gebruikend het malplaatje van de douanekaart:

1. In **Assets UI,** navigeer aan de omslag waar u de kaart wilt tot stand brengen.
1. Klik **creeer \> Kaart DITA**.
1. Voor de pagina van de Vervaging, selecteer het kaartmalplaatje u **daarna** wilt gebruiken en klikken. Als u bijvoorbeeld een kaartsjabloon &#39;test-template&#39; hebt gemaakt, selecteert u deze.
1. Voor de pagina van Eigenschappen, specificeer de kaart **Titel**.
1. Specificeer het dossier **Naam**.

   >[!NOTE]
   >
   > De bestandsnaam moet de extensie .ditamap hebben.

1. Klik **creëren**. Het bericht dat de kaart heeft gemaakt, wordt weergegeven.


De kaart genereert alle elementen waarnaar in de sjabloonmap wordt verwezen. Sommige soorten activa die in een kaart worden bedoeld kunnen als volgt zijn:

- Als de kaart de verwijzing naar een onderwerpmalplaatje bevat, wordt een exemplaar van het gecreeerd binnen de omslag, in de zelfde hiërarchie zoals in de onderwerpenomslag in de `dita-templates` omslag.
- Als de kaart de verwijzing naar een kaartmalplaatje bevat, wordt een exemplaar van het gecreeerd binnen de omslag, in de zelfde hiërarchie zoals in de kaartomslag in de `dita-templates` omslag.
- Als de kaart de algemene verwijzing naar een onderwerp of kaart buiten de `dita-templates/topics` of `dita-templates/maps` omslag bevat, wordt het zelfde slechts bedoeld, en geen exemplaar wordt gecreeerd.

  >[!NOTE]
  >
  > `dita-templates/topics` en `dita-templates/maps` zijn de standaardpaden in hulplijnen en kunnen worden geconfigureerd.


  Als er een zeer belangrijke definitie van het onderwerpmalplaatje binnen het kaartmalplaatje is, wordt een nieuwe sleutel \ (daarom nieuw onderwerp \) gecreeerd en in de kaart bedoeld.

- Als een andere kaart of een onderwerp op het zelfde niveau in de omslag wordt gecreeerd, dan worden de namen van de pas gecreëerde activa toegevoegd met 0.1.2, etc. U kunt ervoor kiezen de kaart te openen om het kaartbestand te bewerken of op te slaan in de opslagplaats.

**Bovenliggend onderwerp:**[ Werk met de Redacteur van de Kaart ](map-editor.md)
