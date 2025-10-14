---
title: Schematron-ondersteuning voor webeditor
description: Werken met Schematron in de webeditor
exl-id: 3e61432f-d81e-446e-b0ad-560f5b9fa91a
feature: Web Editor
role: User, Admin
source-git-commit: be06612d832785a91a3b2a89b84e0c2438ba30f2
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# De kwaliteit van inhoud beheren in de webeditor

In dit artikel wordt een overzicht gegeven van de validatiemogelijkheden in de AEM Guides-webeditor.
Door ontwerp Web-redacteur hefboomwerkingen het DITA schema opstelling in het systeem om gebruikers af te dwingen om DITA volgzame inhoud tot stand te brengen. Met dit, is al inhoud die in het systeem wordt opgeslagen gestructureerd, herbruikbaar en geldige inhoud DITA.

Voorbij steun voor regels DITA, Web-redacteur steunt ook bevestiging van inhoud die op &quot;*Schematron*&quot;regels wordt gebaseerd.

&quot;*Schematron*&quot;verwijst naar een op regel-gebaseerde bevestigingstaal die wordt gebruikt om tests voor een dossier van XML te bepalen. U kunt de Schematron dossiers invoeren en hen ook uitgeven in de Redacteur van het Web. Gebruikend een &quot;Schematron&quot;dossier kunt u bepaalde regels bepalen en dan hen voor een DITA onderwerp of een kaart bevestigen. Regels voor schema kunnen de consistentie van de XML-structuur waarborgen door beperkingen op te leggen die als regels worden gedefinieerd. Deze beperkingen zijn ingegeven door KMO&#39;s die de kwaliteit en consistentie van de inhoud bezitten.

     NOTA: De redacteur van het Web steunt het Schematron van ISO.


## Kennis van hoe &quot;Schematron&quot; werkt in de webeditor

### Schematron-regels configureren

Verwijs sectie &quot;Steun voor de dossiers van Schematron&quot;in de [&#x200B; Gids van de Gebruiker &#x200B;](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/4-2/Adobe-Experience-Manager-Guides_UUID_User-Guide_EN.pdf#page=148)


### Validatieregels toepassen bij het opslaan van bestanden

Met de instellingen van Webeditor kunnen de stroomgebruikers Schematron-regels/bestanden instellen die worden uitgevoerd telkens wanneer een gebruiker de inhoud bijwerkt. Voor meer details verwijs sectie &quot;Bevestiging&quot;in [&#x200B; Gids van de Gebruiker &#x200B;](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/4-2/Adobe-Experience-Manager-Guides_UUID_User-Guide_EN.pdf#page=58)

![&#x200B; vastgestelde regels van Web-editor montages &#x200B;](../../../assets/authoring/schematron-editorsettings-validation-tab.png)


### Kan validatie handmatig worden uitgevoerd?

Ja, als auteur/gebruiker tijdens het maken van inhoud kunt u het deelvenster Schema in de webbrowser gebruiken om een schemabestand te uploaden en validaties uit te voeren voor het bestand dat is geopend in de editor.

     voor dit om te werken, moet de beheerder van het omslagprofiel alle gebruikers toestaan om de dossiers van het Schema in het paneel van de Bevestiging toe te voegen. Zie redacteursmontages (hierboven gegeven screenshot) 

![&#x200B; kies het dossier van het Schema &#x200B;](../../../assets/authoring/schematron-rightpanel-validation-addsch.png)
![&#x200B; bevestiging van de Looppas &#x200B;](../../../assets/authoring/schematron-rightpanel-validation-runsch.png)


### Ondersteunde regels

De huidige versie van AEM Guides biedt alleen ondersteuning voor validatie met behulp van &#39;Assertion&#39;-regels. (zie [&#x200B; activa vs rapport &#x200B;](https://schematron.com/document/205.html))
Regels die zijn gebaseerd op &#39;Rapporten&#39; worden nog niet ondersteund.


### Monsters en meer hulp bij de schoolregels

#### Gebruiksscenario&#39;s

- Controleren of een koppeling extern is en of het bereik &quot;extern&quot; is

  ```
  <sch:pattern>
      <sch:rule context="xref[contains(@href, 'http') or contains(@href, 'https')]">
          <sch:assert test="@scope = 'external' and @format = 'html'">
              All external xref links must be with scope='external' and format='html'
          </sch:assert>
      </sch:rule>
  </sch:pattern>
  ```

- Controleer of er minstens één &quot;topicref&quot; op een kaart staat of minstens één &quot;li&quot; onder een &quot;ul&quot;

  ```
  <sch:pattern>
      <sch:rule context="map">
          <sch:assert test="count(topicref) > 0">
              There should be atleast one topicref in map
          </sch:assert>
      </sch:rule>
  
      <sch:rule context="ul">
          <sch:assert test="count(li) > 1" >
              A list must have more than one item.
          </sch:assert>
      </sch:rule>
  </sch:pattern>
  ```

- Het element &quot;indexterm&quot; moet altijd voorkomen in een &quot;prolog&quot;

  ```
  <sch:pattern>
      <sch:rule context="*[contains(@class, ' topic/indexterm ')]">
          <sch:assert test="ancestor::node()/local-name() = 'prolog'">
              The indexterm element should be in a prolog.
          </sch:assert>
      </sch:rule>
  </sch:pattern>
  ```

#### Bronnen

- Het begrip [&#x200B; Basisprincipes van Schematron &#x200B;](https://da2022.xatapult.com/#what-is-schematron)
- Meer over [&#x200B; de regels van de Bevestiging in Schematron &#x200B;](https://www.xml.com/pub/a/2003/11/12/schematron.html#Assertions)
- [Voorbeeld van schemabestand](../../../assets/authoring/sample_schematron.sch)
