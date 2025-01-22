---
title: Contextual Content Variables (CCVAR) inschakelen in AEM Sites via AEM Guides
description: Werken met Contextual Content Variables (CCVAR) in AEM Sites via AEM Guides
feature: Web Editor
role: User, Admin
source-git-commit: cd5b8329153f598365a640f50d2c003af72dac50
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 1%

---

# Contextual Content Variables (CCVAR) inschakelen in AEM Sites via AEM Guides

Contextual Content Variables (CCVAR) is een ACS-commons-functie waarmee auteurs dynamische inhoudsvariabelen rechtstreeks in hun geschreven tekst kunnen gebruiken. Terwijl CCVAR algemeen in AEM Sites wordt gebruikt, verklaart dit artikel hoe te om gelijkaardige functionaliteit via pagina&#39;s te bereiken die van inhoud worden geproduceerd die in **wordt geschreven AEM Guides *hoofdzakelijk door sleutelwoorden te gebruiken die in de kaart DITA* worden bepaald.**


## Wat zijn Contextual Content Variables (CCVAR)?

Met CCVAR kunnen auteurs dynamische variabelen invoegen in hun inhoud, die bij uitvoering worden omgezet op basis van de context. Variabelen zoals `((page_properties.pageTitle))` kunnen bijvoorbeeld dynamisch de paginatitel trekken tijdens het renderen van inhoud.


## Hoe te om CCVAR in AEM Sites toe te laten Gegenereerd van AEM Guides?

Als AEM Guides wordt gebruikt als de bron van alle inhoud (inclusief AEM Sites, PDF of HTML5), om CCVAR&#39;s in te schakelen op pagina&#39;s die worden gegenereerd vanuit AEM Guides, moet u trefwoorden gebruiken om de CCVAR-naam te definiëren. Om dit in Gidsen te doen, bepaal **sleutelwoorden** in uw kaart DITA gebruikend `<keydef>` elementen. Deze sleutelwoorden kunnen aan dynamische waarden (of namen CCVAR) beantwoorden, toestaand u om hen in uw onderwerpen van DITA van verwijzingen te voorzien.


## Voorwaarden

Controleer voordat u verdergaat of aan de volgende voorwaarden is voldaan:

1. **AEM Geïnstalleerde ACSCommons**:
   - Zorg ervoor dat **ACS AEM Commons** op uw AEM instantie geïnstalleerd is. Dit is vereist voor het gebruik van CCVAR.

2. **Contextafhankelijke Configuratie van de Variabelen van de Inhoud**:
   - Voltooi de opstelling voor **Contextuele Variabelen van de Inhoud** in AEM gebruikend de [ officiële documentatie ](https://adobe-consulting-services.github.io/acs-aem-commons/features/contextual-content-variables/index.html). Dit omvat:
      - Toelatend **de Samenvoeging van het Bezit**.
      - Het vormen **HTML die** herschrijven (als het gebruiken van HTML output).
      - Het vormen **JSON die** herschrijft (als het gebruiken van output JSON).



## Stappen om CCVAR in AEM Guides toe te laten

### 1. Definieer trefwoorden in de DITA-kaart

- Definieer trefwoorden in AEM Guides met behulp van `<keydef>` -elementen in de DITA-kaart die overeenkomen met de CCVAR.
- Bijvoorbeeld:

```xml
  <keydef keys="product">
    <topicmeta>
      <keywords>
        <keyword>((page_properties.pageTitle))</keyword>
      </keywords>
    </topicmeta>
  </keydef>
```

- Het `keys` attribuut (`product` in dit voorbeeld) zal worden gebruikt om naar deze variabele in uw onderwerpen te verwijzen DITA.


## 2. Trefwoorden gebruiken in DITA-onderwerpen

- In het onderwerp, gebruik het sleutelwoord waar CCVar moet worden gebruikt.
- Bijvoorbeeld:

```xml
  <p>This is the title of the product: <keyword keyref="product"/> </p>
```

- Het attribuut `keyref` verwijst naar de `keys` -waarde die in het element `<keydef>` is gedefinieerd (`product` in dit geval).
- Tijdens outputproductie, zal het sleutelwoord met de overeenkomstige waarde worden vervangen CCVar.


## 3. Uitvoer genereren

- Wanneer u uitvoer genereert voor AEM Sites, worden de trefwoordverwijzingen omgezet naar de corresponderende dynamische waarden.
- Bijvoorbeeld:
   - Als `((page_properties.pageTitle))` wordt omgezet in `My Product` , wordt de uitvoer weergegeven:

```xml
   This is the title of the product: My Product.
```


## Voorbeeld: hoofdletter gebruiken

Veronderstel u de taal van de pagina in uw onderwerpen dynamisch wilt opnemen DITA. Hieronder wordt beschreven hoe u dit kunt bereiken:

**bepaal het Sleutelwoord in de Kaart DITA**:

```xml
   <keydef keys="pageLanguage">
     <topicmeta>
       <keywords>
         <keyword>((inherited_page_properties.jcr:language))</keyword>
       </keywords>
     </topicmeta>
   </keydef>
```

**Verwijzing het Sleutelwoord in een Onderwerp DITA**:

```xml
   <p>The title of this page is: <keyword keyref="pageLanguage"/>.</p>
```

**Gegenereerde Output**:

Als `((inherited_page_properties.jcr:language))` wordt omgezet in `en` , wordt de uitvoer weergegeven:

```
     The language of this page is: en.
```


### Bronnen

Voor meer details op **Contextuele Variabelen van de Inhoud**, verwijs naar de officiële documentatie:\
[ Contextuele Variabelen van de Inhoud in AEMBevelen ](https://adobe-consulting-services.github.io/acs-aem-commons/features/contextual-content-variables/index.html)