---
title: Ondersteuning voor Schematron-bestanden
description: Leer hoe te om een DITA- onderwerp in te voeren en te bevestigen, de verklaringen van het gebruiksrapport gebruiken om regels te controleren, regex uitdrukkingen te gebruiken, en abstracte patronen in de dossiers van Schematron van AEM Guides te bepalen.
feature: Authoring, Features of Web Editor
role: User
source-git-commit: 76c731c6a0e496b5b1237b9b9fb84adda8fa8a92
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 0%

---

# Ondersteuning voor Schematron-bestanden

&quot;Schematron&quot; verwijst naar een op regels gebaseerde validatietaal die wordt gebruikt om tests voor een XML-bestand te definiëren. De redacteur van het Web steunt dossiers Schematron. U kunt de Schematron dossiers invoeren en hen ook uitgeven in de Redacteur van het Web. Met behulp van een Schematron-bestand kunt u bepaalde regels definiëren en deze vervolgens valideren voor een DITA-onderwerp of een kaart.

>[!NOTE]
>
> De redacteur van het Web steunt ISO Schematron.


## Schematron-bestanden importeren

Voer de volgende stappen uit om de Schematron-bestanden te importeren:

![](images/scematron-panel-add.png){width="300" align="left"}

1. Navigeer aan de vereiste omslag (waar u de dossiers) in *Mening van de Bewaarplaats wilt uploaden*.
1. Klik het **pictogram van Opties** om het contextmenu te openen en **te kiezen uploadt Assets**.
1. In **uploadt Assets** dialoog, kunt u de bestemmingsomslag in het **Uitgezochte gebied van de Omslag van Activa** veranderen.
1. Klik **kiezen Dossiers** en doorblader om de dossiers van het Schema te selecteren. U kunt één of meerdere dossiers selecteren Schematron en dan **klikken uploadt**.

## Een DITA-onderwerp of -kaart valideren met Schematron

Na het invoeren van de dossiers van het Schema, kunt u hen in de Redacteur van het Web uitgeven. U kunt de dossiers Schematron gebruiken om de onderwerpen of een kaart te bevestigen DITA. Bijvoorbeeld, kunt u de volgende regels voor een kaart DITA of een onderwerp tot stand brengen:

* Een titel wordt bepaald voor een kaart DITA.
* Er is een korte beschrijving van een bepaalde lengte toegevoegd.
* De kaart moet ten minste één actuele referentie bevatten.

Wanneer u een onderwerp in de Redacteur van het Web opent, verschijnt een paneel van de Bevestiging van het Schema in het recht. Voer de volgende stappen uit om een onderwerp of een kaart met een dossier toe te voegen en te bevestigen Schematron:
![](images/schematron-validate.png){width="300" align="left"}

1. Klik op het pictogram Schematron () om het deelvenster Schema te openen.
1. Gebruik Schematron-bestand toevoegen om Schematron-bestanden toe te voegen.
1. Als het Schematron-bestand geen fouten bevat, wordt het toegevoegd en weergegeven in het deelvenster Validatie. Er wordt een foutbericht weergegeven voor het Schematron-bestand dat fouten bevat.
   >[!NOTE]
   >
   >U kunt het kruispictogram bij de naam van het Schematron-bestand gebruiken om het te verwijderen.
1. Klik Valideren met Schematron om het onderwerp te bevestigen.

   * Als het onderwerp geen regels breekt, wordt het bericht van het bevestigingssucces getoond voor het dossier.
   * Als het onderwerp een regel breekt, bijvoorbeeld, als het geen titel bevat en voor het bovengenoemde Schematron bevestigd is, toont het een bevestigingsfout.

1. Klik het foutenbericht om het element te benadrukken dat de fout in het geopende onderwerp/de kaart bevat.

De steun van het Schematron in de Redacteur van het Web helpt u in het bevestigen van de dossiers tegen een reeks regels en het handhaven van consistentie en correctheid over de onderwerpen.

## Instructies voor bevestigen en rapporteren gebruiken om op regels te controleren{#schematron-assert-report}

AEM Guides steunt ook de verklaringen van Schematron. Deze verklaringen helpen u uw onderwerpen DITA bevestigen.

### Instructie Assert

Een herhalingsinstructie genereert een bericht wanneer een testinstructie false oplevert. Als u bijvoorbeeld wilt dat de titel vet wordt, kunt u een instructie voor een claim definiëren.

```XML
<sch:rule context="title"> 
    <sch:assert test = "b"> Title should be bold </sch:assert>
  </sch:rule>
```

Wanneer u uw onderwerpen DITA met Schematron bevestigt, krijgt u een bericht voor de onderwerpen waar de titel niet gewaagd is.

### Instructie Rapport

Een rapportverklaring produceert een bericht wanneer een testverklaring aan waar evalueert. Als u bijvoorbeeld wilt dat de korte beschrijving uit maximaal 150 tekens bestaat, kunt u een rapportinstructie definiëren om de onderwerpen te controleren waarvoor de korte beschrijving uit meer dan 150 tekens bestaat.
Wanneer u uw onderwerpen DITA met Schematron bevestigt, krijgt u een volledig rapport van de regels waar de rapportverklaring aan waar evalueert. U krijgt dus een bericht voor de onderwerpen waarin de korte beschrijving meer dan 150 tekens bevat.


```XML
<sch:rule context="shortdesc"> 
        <sch:let name="characters" value="string-length(.)"/> 
        <sch:report test="$characters &gt; 150">  
        The short description has <sch:value-of select="$characters"/> characters. It should contain more than 150 characters.      
        </sch:report>   
    </sch:rule> 
```

>[!NOTE]
>
> Gebruik alleen Xpath 2.0-expressies bij het schrijven van de Schematron-regels.

## Regex-expressies gebruiken{#schematron-regex-espressions}

U kunt Regex-expressies ook gebruiken om een regel met de functie match() te definiëren en vervolgens validatie uit te voeren met het Schematron-bestand.

U kunt dit bijvoorbeeld gebruiken om een bericht weer te geven als de titel slechts één woord bevat.

```XML
<assert test="not(matches(.,'^\w+$'))"> 
No one word titles.
</assert>  
```


## abstracte patronen definiëren{#schematron-abstract-patterns}

AEM Guides ondersteunt ook abstracte patronen in Schematron. U kunt generische abstracte patronen bepalen hergebruik deze abstracte patronen.  U kunt plaatsaanduidingsparameters maken die het werkelijke patroon opgeven.


Het gebruiken van abstracte patronen kan uw schema van het Schema vereenvoudigen door de duplicatie van regels te verminderen en het gemakkelijker te maken om uw bevestigingslogica te beheren en bij te werken. Het kan uw schema gemakkelijker maken te begrijpen, aangezien u complexe bevestigingslogica in één enkel abstract patroon kunt bepalen dat door het schema opnieuw kan worden gebruikt.


Met de volgende XML-code wordt bijvoorbeeld een abstract patroon gemaakt en het werkelijke patroon verwijst ernaar met de id.

```XML
<sch:pattern abstract="true" id="LimitNoOfWords"> 

<sch:rule context="$parentElement"> 

<sch:let name="words" value="string-length(.)"/> 

<sch:assert test="$words &lt; $maxWords"> 

You have <sch:value-of select="$words"/> letters. This should be lesser than <sch:value-of select="$maxWords"/>. 

</sch:assert>  

<sch:assert test="$words &gt; $minWords"> 

You have <sch:value-of select="$words"/> letters. This should be greater than <sch:value-of select="$minWords"/>. 

</sch:assert>  

</sch:rule> 

</sch:pattern> 

<sch:pattern is-a="LimitNoOfWords" id="extend-LimitNoOfWords"> 

<sch:param name="parentElement" value="title"/> 

<param name="minWords" value="1"/> 

<param name="maxWords" value="8"/> 

</sch:pattern> 
```
