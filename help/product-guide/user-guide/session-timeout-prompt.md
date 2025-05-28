---
title: Werken met sessietime-outs in Experience Manager Guides
description: Meer informatie over sessietime-outs in Experience Manager Guides.
feature: Authoring, Publishing
role: User
source-git-commit: a6e015817bc9a964e3ca6a83c50089e7fabcdd94
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 0%

---

# Waarom ondertekent Experience Manager Guides mij na een bepaalde periode?

Experience Manager Guides beëindigt een gebruikerssessie na een gedefinieerde periode van inactiviteit (inactieve time-out). Deze functie voor automatisch uitloggen is geconfigureerd in de Adobe Experience Manager. Wanneer de sessie verloopt, wordt een pop-upwaarschuwing weergegeven om de gebruiker op de hoogte te stellen van de verlopen sessie. Deze waarschuwing beperkt de gebruiker tot het aanbrengen van verdere wijzigingen in de inhoud.

**hoe het werk van sessieonderbreking?**

Experience Manager Guides verzendt om de 30 seconden een achtergrondverzoek `token.json` om de sessie te valideren. Als de sessie nog actief is, wordt een geldig token geretourneerd. Als de sessie is verlopen vanwege inactiviteit, wordt een leeg token geretourneerd en wordt de sessie als inactief beschouwd.

**wat gebeurt wanneer de zitting verloopt?**

Wanneer een inactieve sessie wordt gedetecteerd:

- Er verschijnt een pop-upwaarschuwing om aan te geven dat u bent afgemeld.

  ![](images/sign-out-prompt.png)

- Met de waarschuwing worden alle interacties met de toepassing uitgeschakeld.

- Het selecteren van **O.K.** verfrist browser en richt u aan de login pagina opnieuw.
- Wanneer u zich aanmeldt, wordt u omgeleid naar de laatst geopende pagina van Experience Manager Guides.

**Volgende stappen**

De waarschuwing bij het verlopen van de sessie helpt gegevensverlies te voorkomen doordat u tijdens een inactieve sessie geen wijzigingen in de toepassing hoeft aan te brengen. Als u wilt voorkomen dat inhoud per ongeluk verloren gaat, is het raadzaam uw werk regelmatig op te slaan in de Editor, vooral voordat u langere tijd van het systeem afstapt.





