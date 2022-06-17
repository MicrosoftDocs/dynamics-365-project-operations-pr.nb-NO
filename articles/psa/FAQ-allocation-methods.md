---
title: Metoder for bestillingstildeling i Project Service Automation
description: Denne artikkelen inneholder informasjon om de forskjellige måtene du kan bestille tildelinger på.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: dff11de0726004653233c6b90e194825c3850e0c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929180"
---
# <a name="booking-allocation-methods-in-project-service-automation"></a>Metoder for bestillingstildeling i Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Om du legger til et teammedlem direkte i et prosjekt i kategorien **Team**, eller reserverer en ressurs for et prosjekt eller krav fra planleggingstavlen, fins det et par forskjellige bestillingstildelingsmetoder du kan bruke. Denne artikkelen forklarer hvordan hver metode fungerer, og hvilke metoder som kan føre til overbestillingsressurser.

## <a name="full-capacity"></a>Full kapasitet 
Metoden Full kapasitet bestiller ressursens fulle kapasitet for de angitte fra- og til-datoene. Hvis for eksempel en ressurs har en kalender som er satt til 8 timers arbeidstid per dag, 5 dager i uken, og du angir en start- og sluttdato som dekker 5 arbeidsdager, bestilles ressursen i 40 timer. Bestillingen utføres uavhengig av ressursens gjenværende kapasitet. Hvis en ressurs allerede er bestilt på andre prosjekter i denne perioden, blir de 40 timene registrert som ekstra timer og kan føre til overbestilling.

## <a name="remaining-capacity"></a>Gjenværende kapasitet
Metoden Gjenværende kapasitet er bare tilgjengelig når du bestiller direkte på et prosjekt ved hjelp av planleggingstavlen. Denne metoden bestiller ressursens tilgjengelige kapasitet i det angitte datointervallet. Hvis for eksempel en ressurs har en kapasitet på 40 timer i uken og allerede er bestilt 10 timer, vil en bestilling for den samme uken resultere i en bestilling av de gjenværende 30 timene med kapasitet denne uken.

## <a name="percentage-capacity"></a>Kapasitet i prosent
Metoden Kapasitet i prosent bestiller ressursen med en prosent kapasiteteb for de angitte fra- og til-datoene. Hvis for eksempel en ressurs har en kalender som er satt til 8 timers arbeidstid per dag, 5 dager i uken, og du angir en start- og sluttdato som dekker 5 arbeidsdager med 50 % kapasitet, bestilles ressursen i 20 timer. De enkelte bestillingene per dag fordeles likt på perioden, for eksempel 4 timer hver dag i dette eksemplet. Bestillingen utføres uavhengig av ressursens gjenværende kapasitet. Hvis ressursen allerede er bestilt på andre prosjekter i denne perioden, blir de 20 timene registrert som ekstra timer og kan føre til overbestilling.

## <a name="evenly-distribute-hours"></a>Distribuer timer jevnt
Metoden Distribuer timer jevnt bestiller ressursen for et bestemt antall timer og distribuerer tiden jevnt per dag over de angitte fra-/til-datoene. Hvis du for eksempel bestiller en ressurs 20 timer over en 5-dagers periode, distribueres de 20 timene jevnt med 4 timer per dag. Bestillingen utføres uavhengig av ressursens gjenværende kapasitet. Hvis ressursen allerede er bestilt på andre prosjekter i denne perioden, blir de 20 timene registrert som ekstra timer og kan føre til overbestilling.

## <a name="front-load-hours"></a>Frontbelast timer
Metoden Frontbelast timer bestiller ressursen for et bestemt antall timer og frontbelaster timene per dag over de angitte fra- og til-datoene. Frontbelastning bruker ressursens tilgjengelige kapasitet i rekkefølgen "først-inn-først-brukt". Hvis for eksempel arbeidstidsplanen til en ressurs er 8 timer om dagen, 5 dager i uken, og de har ingen gjeldende bestillinger, vil bestilling av ressursen i 20 timer over en periode på 5 arbeidsdager gi følgende daglige bestillingsmønster: 

|         Bestillinger          |    Dag 1    |    Dag 2    |    Dag 3    |    Dag 4    |    Dag 5    |    Totalt    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    Eksisterende bestillinger    |    0        |    0        |    0        |    0        |    0        |    0        |
|    Ny bestilling          |    8        |    8        |    4        |    0        |    0        |    20       |

Frontbelastningsmetoden tar hensyn til eksisterende bestillinger og tilgjengelig kapasitet. Hvis for eksempel den samme ressursen allerede har 20 timer med bestillinger i arbeidsuken, forbruker nye bestillinger gjenværende kapasitet på følgende måte:

|   Bestillinger          | Dag 1 | Dag 2 | Dag 3 | Dag 4 | Dag 5 | Totalt |
|---------------------|-------|-------|-------|-------|-------|-------|
| Eksisterende bestillinger | 8     | 8     | 4     | 0     | 0     | 20    |
| Ny bestilling       | 0     | 0     | 4     | 8     | 8     | 20    |

Fordi tilgjengelig kapasitet blir tatt hensyn til, kan du få en feilmelding hvis ressursen ikke har noen gjenværende kapasitet som kan absorberes av bestillingen. Med denne metoden kan du ikke overbestille.

## <a name="none"></a>Ingen
Metoden Ingen er bare tilgjengelig når du bestiller fra kategorien **Team** i et prosjekt. Denne metoden legger til ressursen som et teammedlem i prosjektet, men oppretter ikke en bestilling som absorberer ressursens kapasitet. Denne metoden brukes når standard teammedlem for prosjektleder legges til når det opprettes et prosjekt. Som standard legges prosjektlederbrukeren som opprettet prosjektet, til prosjektet, slik at prosjektenhetsoppføringen har en eier, og det finnes én godkjenner på prosjektet. Fordi denne brukeren ikke har noen bestillinger, og hvis du vil bestille ressursen, kan du enten slette og deretter legge dem til på nytt ved hjelp av en annen tildelingsmetode, eller legge til ressursen i oppgaver og deretter bruke **Utvid bestillinger** i kategorien **Avstemming** for å opprette bestillinger for tilordningene.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Tildelingsmetoder som fører til overbestilling
Følgende tildelingsmetoder fører altså til overbestilling hvis ressursen allerede er reservert på andre prosjekter (eller på andre arbeidsordrer eller planleggbare enheter):

- Full kapasitet
- Kapasitet i prosent
- Distribuer timer jevnt

Når du bruker en av disse tildelingsmetodene, blir du ikke varslet om at ressursen er overbestilt. Hvis du vil rette opp overbestillingen, må du bruke planleggingstavlen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
