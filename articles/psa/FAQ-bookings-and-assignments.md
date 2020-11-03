---
title: Ressursbestillinger og hvordan de er relatert til oppgavetilordninger
description: Dette emnet gir informasjon om hvordan du behandler navngitte ressurser, ressursbestillinger og oppgavetilordninger, samt hvordan de er relatert til hverandre.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 03285d324e855ecf933b155559e5a4826420ab25
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081807"
---
# <a name="resource-bookings-and-how-they-relate-to-task-assignments"></a>Ressursbestillinger og hvordan de er relatert til oppgavetilordninger


Navngitte ressurser kan bestilles til et prosjektteam og tilordnes prosjektoppgaver på to måter:

- Ressursen kan bestilles direkte til et prosjekt og deretter tilordnes til prosjektoppgaver.
- Oppgavene kan tilordnes til en generisk ressurs , som deretter brukes til å søke etter og erstatte den generiske med en navngitt ressurs. 

I begge tilfeller reserverer bestillingen ressursens kapasitet.

Prosjektlederen som planlegger prosjektet, eier prosjektplanen og planen. Prosjektlederen kan reservere ressurser på prosjektet med omfang som er angitt i prosjektplanen, ved hjelp av den generelle ressursen for tilordning, og deretter generere en ressursforespørsel fra den. De kan reservere ressurser til et prosjekt og deretter tilordne dem til oppgaver, men det finnes ingen måte å justere bestillingsomfanget med omfanget for oppgavene. Bestillinger påvirker ikke prosjektplanen.

Vurder et komplekst prosjekt med flere overlappende oppgaver der flere ressurser av samme type skal arbeide samtidig. Hvis en ressurs har fått et omfang som er forskjellig fra det til aggregatet av tilordningene, er det vanskelig å endre oppgavene for å tilpasse omfanget av bestillingene til deres enkelte oppgaver og deres opprinnelige omfang.

I eksemplet nedenfor er den totale innsatsen som kreves av den samme ressursen fra et sett med fire oppgaver, 62 timer over en toukers periode, og det finnes et bestemt omfang. Hvis ressursen Bjørn er bestilt i 62 timer i løpet av de samme to ukene, men med et annet omfang, er kravet og bestillinger på linje.

| **Oppgaveomfang**    | **Totalt antall timer** | Ma 4/6 | Ti 5/6 | On 6/6 | To 7/6 | Fr 8/6 | Lø 9/6 | Sø 10/6 | Ma 11/6 | Ti 12/6 | On 13/6 | To 14/6 | Fr 15/6 |
|----------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Oppgave 1               | 24              | 8      | 8      | 4      |        |        |        |         |         |         | 4       |         |         |
| Oppgave 2               | 16              |        |        | 4      | 4      |        |        |         | 8       |         |         |         |         |
| Oppgave 3               | 10              |        |        |        |        | 4      |        |         |         | 4       |         | 2       |         |
| Oppgave 4               | 12              |        |        |        |        |        |        |         |         |         | 4       |         | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |         |         |
| **Totalt**           | 62              | 8      | 8      | 8      | 4      | 4      |        |         | 8       | 4       | 8       | 2       | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |

### <a name="bobs-availability"></a>Bjørns tilgjengelighet
| **Ressursbestilling** | **Totalt antall timer** | Ma 4/6 | Ti 5/6 | On 6/6 | To 7/6 | Fr 8/6 | Lø 9/6 | Sø 10/6 | Ma 11/6 | Ti 12/6 | On 13/6 | To 14/6 | Fr 15/6 |
|------------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Bjørn                    | 62              | 4      | 4      | 8      | 8      | 8      |        |         | 4       | 4       | 8       | 8       | 6       |

Det finnes imidlertid ingen systematisk måte å tilordne omfanget av bestilte timer til oppgaver på en per dag-basis. Hvis prosjektlederen er villig til å endre prosjektplanen for å oppfylle tilgjengeligheten til ressursen, må de fjerne tilordningen og revidere alle oppgavene for å samsvare med bestillingsomfanget.

I tilfellet der en organisasjon har gitt oppgaven med prosjektplanlegging til både en prosjektleder og en ressursleder, angir prosjektlederen tidsplanen, og denne inneholder omfanget av arbeidet som kreves. Ressurslederen skal ikke kunne påvirke planen uten at prosjektlederen kjenner til dette, ved å endre innsatsomfang under bestilling av virkelige ressurser. Hvis ressurslederen fullfører noe annet enn det prosjektlederen forespurte, må de komme til enighet om hvilke endringer som er nødvendige i prosjektplanen.

Siden bestillinger og tilordninger ikke er tett sammenknyttet, er det mulig å bestille omfang som er forskjellig fra oppgaveomfanget, eller endre tilordninger som fører til situasjoner der bestillinger og tilordninger ikke er samstemt.

Med **avstemmingsvisningen** kan prosjektlederen se bestillinger og tilordninger for hvert prosjektteammedlem. Visningen bruker farger og skyggelegging for å vise der det ikke er samsvar mellom et teammedlems bestillinger og tilordninger. Basert på denne informasjonen kan prosjektlederen korrigere og enten utvide ressursbestillinger i tilfeller der det fins tilordninger og ingen bestillinger, eller annullere bestillinger der ressurser er bestilt, men det mangler tilordninger.

> [!NOTE]
> Hvis du flytter en oppgave du har opprettet omfang for selv, kan ikke dette omfanget opprettholdes. Omfanget genereres på nytt i henhold til prosjektkalenderen for å ta hensyn til endringer i arbeidstimer og ferier. Dette er fordi systemet ikke vet hensikten med det opprinnelige omfanget og kan ikke avgjøre om det er fornuftig å beholde dette omfanget i en ny tidsperiode. Siden bestillinger og tilordninger ikke er knyttet sammen, beholder bestillingene de opprinnelige bestillingsomfangene. I dette tilfellet må du annullere og bestille på nytt til det nye tilordningsomfanget.
