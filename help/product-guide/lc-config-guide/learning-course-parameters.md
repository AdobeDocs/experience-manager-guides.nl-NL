---
title: SCORM-sleutelgegevens voor voortgang en voltooiing van de cursus
description: Meer informatie over de belangrijkste SCORM-meetgegevens voor de voortgang en voltooiing van de cursus
feature: Authoring
role: Admin
level: Experienced
source-git-commit: 0dff380131dadc971f257eb464700392328164e5
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# SCORM-sleutelgegevens voor voortgang en voltooiing van de cursus

Het artikel bevat een lijst met de belangrijkste parameters die in een SCORM-pakket zijn vastgelegd, samen met de bijbehorende velden, en voorbeelden. Deze parameters bieden belangrijke inzichten in de voortgang van de studenten, de voltooiing van de cursus, de interactiedetails en de quizprestaties. Beheerders kunnen deze informatie gebruiken om het bijhouden van gegevens te valideren, rapportage te configureren en nauwkeurige analyses in de LMS-omgeving te garanderen. Hieronder vindt u voorbeeldwaarden voor elke parameter zoals deze in het SCORM-pakket wordt weergegeven.

| **naam van de Parameter** | **Beschrijving** | **Gebieden** | **Voorbeeld** |
|---|---|---|---|
| **de voltooiingsstatus van de cursus** | Geeft aan of de cursus is voltooid | cmi.completion_status | onvolledig |
| **Aantal van de Poging** | Aantal pogingen van de leerling | LMS-side poogingsteller/inhoud | Pogingen: 1 |
| **Plaats van pakket SCORM** | Huidige bladwijzer of locatie in de cursus | cmi.location | - |
| **voltooiing van de Voortgang** | Voortgang van de leerling | cmi.progress_measure | 0,87 |
| **Totale tijd (poging)** | Totale tijd die is doorgebracht in de huidige poging | cmi.total_time | 0000 :01: 9.87 |
| **zicht van TOC en onderwerptelling** | Toont de zichtbaarheid van de inhoudsopgave en de details van de onderwerpvoltooiing | Project.HideTOC, Project.TotalTopics, Project.TopicsCompleted | - |
| **per onderwerpstatus** | Voltooiing en status doorgeven voor elk onderwerp | Aangepaste status per les | - |
| **per vraagkeuzestaat** | Volgt de geselecteerde keuzes van de leerling per vraag | value, generated_id, checked | - |
| **Globale vraag het scoren** | Op vraagniveau behaalde score en aggregaat | {&quot;score&quot;:0, &quot;maxScore&quot;:1 en % | &quot;score&quot;:33.33, &quot;maxScore&quot;:100, &quot;minScore&quot;:0 |
| **Interacties op elk vraagniveau** | Details van studenteninteractie per vraag | id/type/timestamp/correct_response/learner_response/result/latentie | - |
| **Algemene cursusstatus** | Geeft de voortgang voor slagen en afwijzen aan | success_status, completion_status, score, progress_measurement | Of geslaagd of mislukt |
| **de details van de Student** | Identificeert leerling op identiteitskaart en naam | cmi.learner_id, cmi.learner_name | Albert |
| **de parameters van de Quiz** | Configuraties voor quiztiming en voldoende score | cmi.max_time_allowed, cmi.scaled_score, cmi.time_limit_action | Ongedefinieerde of geconfigureerde waarden |