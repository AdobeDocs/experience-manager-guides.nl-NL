---
title: Inhoud vertalen in AEM Guides
description: Leer hoe u inhoud kunt vertalen
exl-id: 0d3a909c-3499-4ef4-b033-02e412dae959
feature: Translation
role: Admin
level: Experienced
hidefromtoc: true
source-git-commit: 3aadc59f5034828cf319992b7acb32d5a88eaf93
workflow-type: tm+mt
source-wordcount: '985'
ht-degree: 0%

---

# Inhoud vertalen {#id181GB0400UI}

Automatiseer de vertaling van pagina-inhoud, elementen en door de gebruiker gegenereerde inhoud om meertalige websites te maken en te onderhouden. Om vertaalworkflows te automatiseren, integreert u de leveranciers van vertaaldiensten met AEM en creeert u projecten voor het vertalen van inhoud in veelvoudige talen. AEM ondersteunt workflows voor het vertalen van mensen en machines.

- Menselijke vertaling: de inhoud wordt naar uw vertaalbureau verzonden en door professionele vertalers vertaald. Wanneer de vertaalde inhoud is voltooid, wordt deze geretourneerd en in AEM geïmporteerd. Wanneer uw vertaalprovider is geïntegreerd met AEM, wordt inhoud automatisch uitgewisseld tussen AEM en de vertaalprovider

- Machinevertaling: de vertaalservice zet uw inhoud direct om


Voor het vertalen van inhoud worden de volgende stappen uitgevoerd:

1. Verbind AEM met uw [ leverancier van de vertaaldienst ](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/tc-tic.html#ConnectingtoaTranslationServiceProvider) en creeer [ configuraties van het kader van de vertaalintegratie ](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/tc-tic.html#CreatingaTranslationIntegrationConfiguration).

1. Koppel de pagina&#39;s van uw taalmeester met de [ vertaaldienst en kaderconfiguraties ](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/tc-tic.html#ConfiguringPagesforTranslation).

1. Identificeer het type van [ te vertalen inhoud ](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/tc-rules.html).

1. [ bereidt de inhoud voor vertaling ](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/tc-prep.html) voor door de taalmeester te ontwerpen en de wortelpagina&#39;s van taalexemplaren te creëren.

1. Creeer [ vertaalprojecten ](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/tc-manage.html) om de inhoud te verzamelen om te vertalen en het vertaalproces voor te bereiden.

1. Gebruik de vertaalprojecten om [ het proces van de inhoudsomzetting ](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/tc-manage.html) te beheren.


Als uw vertaalservicebureau geen aansluiting voor integratie met AEM biedt, biedt AEM ondersteuning voor het handmatig exporteren en importeren van vertaalde inhoud in XML-indeling.

>[!TIP]
>
> Zie de *Vertaling* sectie in de Beste praktijken gids voor beste praktijken rond het vertalen van inhoud.

## Het tabblad Vertaling op het dashboard voor de DITA-kaart configureren

De optie van het Lusje van de Vertaling van de Huid wordt niet toegelaten door gebrek en u moet dit van configMgr toelaten. Voer de volgende stappen uit om het tabblad Vertaling op het dashboard voor de DITA-kaart te verbergen:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.config.ConfigManager** bundel.

1. Selecteer de **optie van het Lusje van de Vertaling van de Huid**, om het vertaallusje op het kaartdashboard te verbergen.

   >[!NOTE]
   >
   > Deze eigenschap is standaard uitgeschakeld en het tabblad Vertalen is beschikbaar op het kaartdashboard.

1. Klik **sparen**.

## Op componenten gebaseerde vertaalworkflow configureren

Als de schakelaar voor de vertaalverkoper geen inhoud DITA steunt, dan moet de op component-gebaseerde vertaalwerkschema worden toegelaten. Als deze optie is ingeschakeld, wordt de vertaalbare inhoud verzonden als metagegevens over elementen. Deze workflow werkt alleen als de connector ondersteuning biedt voor het vertalen van metagegevens van elementen.

Op basis van de vertaalworkflow die in uw installatie wordt gebruikt, moet de optie voor de vertaalworkflow op basis van componenten als volgt worden geconfigureerd:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.config.ConfigManager** bundel.

1. Vorm de **Component-Gebaseerde optie van het Werkschema van de Vertaling DITA** zoals per uw opstelling:

   - Als u menselijke vertaling gebruikt, dan *maak* **op component-Gebaseerde optie van het Vertaalwerkschema** onbruikbaar.

   - Als u machinevertaling gebruikt, dan *laat* toe de **op component-Gebaseerde optie van het Vertaalwerkschema**.

   >[!NOTE]
   >
   > Als u vertaalschakelaar gebruikt, dan zorg ervoor dat u de schakelaar zoals die in *[wordt beschreven het Vormen van het Kader van de Integratie van de Vertaling ](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/tc-tic.html)* onderwerp in de documentatie van AEM hebt gevormd.

1. Klik **sparen**.

>[!IMPORTANT]
>
> Nadat u de vertaalconfiguraties hebt ingesteld, dient u de juiste Cloud Configuration in te stellen voor de taalmappen.

## De workflow voor veroudering configureren

>[!IMPORTANT]
> 
> Het wordt aanbevolen de nieuwste vertaalworkflow, die beschikbaar is in AEM Guides 4.6.0 en hoger, te gebruiken voor betere prestaties. Nochtans, als u om het even welke aanpassing in het vertaalproces hebt toegelaten en het door het nieuwe werkschema wordt beïnvloed, denk na terugkerend aan de erfenisvertaalwerkstroom als oplossing.



Standaard is de optie voor de verouderde vertaalworkflow uitgeschakeld. U kunt deze optie configureren door de volgende stappen uit te voeren:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.config.ConfigManager** bundel.

1. Configureer de workflowoptie voor veroudering van verouderde vertalingen volgens uw instellingen:

   - (*Gebrek*) als u het recentste vertaalwerkschema wilt gebruiken, dan maak de **optie van het de vertaalwerkschema van de Looppas erfenis** onbruikbaar.
   - Als u het erfenisvertaalwerkschema wilt gebruiken, dan laat de **optie van het de erfenisvertaalwerkschema van de Looppas** toe.

1. Klik **sparen**.

## Het gedrag voor eerste vertaling configureren

Wanneer u voor het eerst een vertaling uitvoert, worden standaard lege XML-bestanden gemaakt voor de doeltaal. Deze bestanden worden pas na goedkeuring vertaald. U kunt de instelling `Initialize destination language copy with source content` als volgt inschakelen om dit gedrag te beheren:

>[!NOTE]
>
> Deze instelling is alleen van toepassing wanneer de verouderde vertaalworkflow is uitgeschakeld.

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik **com.adobe.fmdita.config.ConfigManager** bundel.

1. Selecteer de instelling `Initialize destination language copy with source content` .

   - Wanneer deze optie is ingeschakeld, wordt een niet-versioned kopie met de broninhoud gemaakt op basis van de werkkopie in plaats van tijdens de eerste vertaling lege XML-bestanden te genereren.
   - (*Gebrek*) wanneer onbruikbaar gemaakt, is het standaardgedrag van toepassing en de lege dossiers van XML worden gecreeerd voor de bestemmingstaal tijdens de eerste - tijdvertaling.

1. Klik **sparen**.





<!---

This was added for 2406 CS IG

## Configure the legacy translation workflow 

It is recommended that you use the latest translation workflow, which provides enhanced performance. However, you can configure the legacy translation workflow if necessary.

Based on the translation workflow used in your setup, provide the following (property) details to configure the legacy translation workflow: the component-based translation workflow option should be configured as follows:

1.  Open the Adobe Experience Manager Web Console Configuration page.

    The default URL to access the configuration page is:

    ! Add the syntax of http as given in previous config

    Note: Configure htttp code as given in previous sample
    

1.  Search for and click on the **com.adobe.fmdita.config.ConfigManager** bundle.



1.  Configure the **Run legacy translation workflow** option as per your setup:

    -   If you use the latest translation workflow, then *Disable* \( `false`\) the **Run legacy translation workflow** option. The latest translation workflow is enabled by default. <br> 

    -   If you use the legacy translation, then *Enable \( `true`\)* the **Run legacy translation workflow** option.

1.  Click **Save**.


--->


## Nabewerking van tijdelijke taalkopieën configureren

Wanneer u de vertaalworkflow start, maakt het systeem tijdelijke taalkopieën van de broninhoud. U kunt de nabewerking voor deze tijdelijke bestanden in- of uitschakelen. In de naverwerkingstransactie worden de inkomende en uitgaande referenties van de bestanden opgelost, wordt de documentstatus ingesteld, samen met andere bewerkingen. Als u naverwerking voor deze tijdelijke bestanden inschakelt, kan het voltooien van het vertaalproces langer duren. Daarom wordt aangeraden de optie voor nabewerking uit te schakelen.

De optie voor naverwerken van tijdelijke bestanden is standaard uitgeschakeld. U kunt deze optie configureren door de volgende stappen uit te voeren:

1. Open de Adobe Experience Manager Web Console Configuration-pagina.

   De standaard-URL voor toegang tot de configuratiepagina is:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Onderzoek naar en klik op **com.adobe.fmdita.config.ConfigManager** bundel.

1. Vorm de **post-procestaal taalexemplaren** optie zoals per uw opstelling:

   - \ (*Gebrek* \) als u niet de post-verwerkingsverrichting op de tijdelijke dossiers wilt in werking stellen, dan ** onbruikbaar maken **na-procestaalexemplaren** optie.

   - Als u de post-verwerkingsverrichting op de tijdelijke dossiers wilt in werking stellen, dan *laat* de **na-procestaalexemplaren** optie toe.

1. Klik **sparen**.
