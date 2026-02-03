---
title: Documentstatusfilters configureren
description: Leer hoe u documentstatusfilters configureert
feature: Web Editor Configuration
role: Admin
level: Experienced
source-git-commit: 4942b914ff278ebcf09d00da32d6f9c7cc4d7ff9
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 0%

---

# Documentstatusfilters configureren

Adobe Experience Manager Guides biedt de functie om een bestand te doorzoeken op basis van de huidige documentstatus. U kunt filterzoekopdrachten gebruiken om bestanden te zoeken vanuit de dataopslaginterface om door bestanden te bladeren.

Voer de volgende stappen uit om de documentstatusfilters te configureren:

1. Meld u als beheerder aan bij Adobe Experience Manager.
1. Selecteer de verbinding van Adobe Experience Manager bij de bovenkant en kies **Hulpmiddelen**.
1. Selecteer **Gidsen** van de lijst van hulpmiddelen en selecteer dan **Profielen van de Omslag**.
1. Open de **Globale tegel van het Profiel**. U kunt ook een specifieke mapprofieltegel selecteren als u deze wijzigingen alleen op die map wilt toepassen in plaats van op de algemene.
1. Navigeer aan **Configuratie van de Redacteur van XML**.
1. Selecteer **uitgeven** pictogram op de bovenkant.
1. Selecteer het **pictogram van de Download** om het `ui\_config.json` dossier op uw lokaal systeem te downloaden.
Raadpleeg de volgende sectie in het gedownloade `ui\_config.json` -bestand:

       &quot;
        &quot;repositoryFilters&quot;: [
        
        &quot;title&quot;: &quot;Documentstatus&quot;, 
        &quot;eigenschap&quot;: &quot;jcr:content/metadata/docstate&quot;, 
        &quot;children&quot;: [
       {
        &quot;title&quot;: &quot;Draft&quot;, 
        &quot;value&quot;: &quot;Draft&quot;
        
       {
        &quot;title&quot;: &quot;Edit&quot;, 
        &quot;waarde&quot;: &quot;geef uit&quot;
        ,
       {
        &quot;title&quot;: &quot;In-Review&quot;, 
        &quot;value&quot;: &quot;In-Review&quot;
        
       {
        &quot;title&quot;: &quot;Goedgekeurd&quot;, 
        &quot;waarde&quot;: &quot;Goedgekeurd&quot;
        
 ,       
{       
 &quot;title&quot;: &quot;Reviewed&quot;,        
 &quot;waarde&quot;: &quot;Gereviseerde&quot;       
 ,       
{       
 &quot;title&quot;: &quot;Done&quot;,        
 &quot;value&quot;: &quot;Done&quot;       
        
]       
      
   ]        &quot;
   Dit fragment vertegenwoordigt de standaarddocumentstatusfilters die beschikbaar zijn in Experience Manager Guides.

1. U kunt de filterwaarden aanpassen op basis van de workflow van uw organisatie. Bijvoorbeeld, om een staat van het douanedocument toe te voegen **in afwachting van**, neem de volgende ingang onder `children` op:

   ```
   {
       "title": "Pending",
       "value": "Pending"
   }
   ```

1. Sla het bestand op en upload het wanneer het is bijgewerkt.

De gevormde filters worden getoond in het **paneel van Filters** in Bewaarplaats op de pagina van het Huis.

**Bovenliggend onderwerp:**[ pas de Redacteur van het Web ](conf-web-editor.md) aan
