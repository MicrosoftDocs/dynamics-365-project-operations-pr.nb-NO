---
title: Endringer i ressursbehandling (Project Service Automation 3.x)
description: Dette emnet inneholder informasjon om endringene i ressursbehandling.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 94f9adc67163254486387a1ce59d5d3e8e93c335
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148655"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>Endringer i ressursbehandling (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

Delene i dette emnet gir informasjon om endringene som er gjort i ressursbehandling i Dynamics 365 Project Service Automation versjon 3.x.

## <a name="project-estimates"></a>Prosjektestimater

I stedet for å være basert på enheten **msdyn\_projecttask** (**Prosjektoppgave**) er prosjektestimater basert på enheten **msdyn\_resourceassignment** (**Ressurstilordning**). Ressurstilordningene har blitt "kilden til sannheten" for oppgaveplanlegging og prising.

## <a name="line-tasks"></a>Linjeoppgaver

I PSA 3.x er linjeoppgaver foreldede (avskrevet). Tilordninger peker nå på hele oppgaven i stedet for linjeoppgavene.

Følgende eksempel viser hvordan en oppgave med navnet "Testoppgave" er tilordnet til teammedlemmer A og B i tidligere versjoner av PSA og i PSA 3.x.

- **Før PSA 3.x:**

    - Testoppgave

        - Testoppgave – linjeoppgave 1

            - Tilordning til A

        - Testoppgave – linjeoppgave 2

            - Tilordning til B

- **PSA 3.x:**

    - Testoppgave

        - Tilordning til A
        - Tilordning til B

## <a name="unassigned-assignment"></a>Ikke-tilordnet tilordning

I PSA 3.x er en ikke-tilordnet tilordning en tilordning som er tilordnet til et **NULLl**-teammedlem og en **NULL**-ressurs. Ikke-tilordnede tilordninger kan forekomme i noen scenarioer:

- Hvis en oppgave er opprettet, men ennå ikke er tilordnet til noen teammedlemmer, opprettes det alltid en tilordning som ikke er tilordnet. 
- Hvis alle tilordnede ressurser i en oppgave blir fjernet, blir en ikke-tilordnet tilordning opprettet på nytt for den oppgaven.

## <a name="scheduling-fields-on-the-project-task-entity"></a>Planlegge felt i Prosjektoppgave-enheten

Feltene i enheten **msdyn\_projecttask** er avskrevet eller flyttet til enheten **msdyn\_resourceassignment**, eller de blir referert til fra enheten **msdyn\_projectteam** (**Prosjektteammedlem**).

| Avskrevet felt i msdyn\_projecttask (Prosjektoppgave) | Nytt felt i msdyn\_resourceassignment (Ressurstilordning) | Kommentar |
|---|---|---|
| msdyn\_assignedresources | Ingen | |
| msdyn\_assignedteammembers | Ingen | |
| msdyn\_numberofresources | Ingen | |
| msdyn\_scheduledhours | Ingen | |
| msdyn\_effortcontour | msdyn\_plannedwork | Formatet på JSON-datastrukturen (JavaScript Object Notation) som er lagret i feltet, er endret. |

## <a name="schedule-contour"></a>Tidsplankontur

Tidsplankonturen er lagret i feltet **Planlagt arbeid** (**msdyn\_plannedwork**) i hver **Ressurstilordning**-enhet (**msdyn\_resourceassignment**).

### <a name="structure"></a>Struktur

Den nye strukturen i planleggingskonturen består av fleksible tidsdeler som er definert for hver dag i tidsplanen. Hver tidssektor har følgende egenskaper:

- **Start** – starten på arbeidstiden for dagen i henhold til prosjektkalenderen.
- **Slutt** – slutten på arbeidstiden for dagen i henhold til prosjektkalenderen.
- **Timer** – antall timer som er tilordnet på dagen.

**Eksempel**

Dette eksemplet bruker en prosjektkalender der arbeidsdagen er fra 9 til 17 i UTC-8-tidssonen.

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>Automatisk planlegging og manuell planlegging

Hvis en oppgave er automatisk planlagt, lastes timene inn, og oppgavevarigheten kan bli redusert.

**Eksempel**

Følgende oppgave planlegges automatisk til 18 timer i løpet av tre dager (3. desember 2018 til 5. desember 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

Hvis en oppgave planlegges manuelt, distribueres timene jevnt til alle datoene.

**Eksempel**

Følgende oppgave planlegges manuelt til 18 timer i løpet av tre dager (3. desember 2018 til 5. desember 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>Tilordningsenhet

Tilordningsenheten er avskrevet i PSA 3.x. Oppgaveinnsatstimene er nå likt delt per dag, blant alle de tildelte ressursene.

**Eksempel**

I dette eksemplet er oppgaven tilordnet to ressurser og planlagt automatisk i 36 timer over tre dager (3. desember 2018 til 5. desember 2018).

- Tilordning 1:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- Tilordning 2:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>Prisdimensjoner

I PSA 3.x er ressursspesifikke prisdimensjonsfelt (for eksempel **Rolle** og **Organisasjonsenhet**) fjernet fra enheten **msdyn\_projecttask**. Disse feltene kan nå hentes fra det tilsvarende prosjektteammedlemmet (**msdyn\_projectteam**) til ressurstilordningen (**msdyn\_resourceassignment**) når prosjektestimater genereres. Et nytt felt, **msdyn\_organizationalunit**, er lagt til i enheten **msdyn\_projectteam**.

| Avskrevet felt i msdyn\_projecttask (Prosjektoppgave) | Felt fra msdyn\_projectteam (Prosjektteammedlem) som brukes i stedet |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>Profiler

Feltene for prising og estimeringsprofil er avskrevet i enheten **msdyn\_projecttask**. De er flyttet til enheten **msdyn\_resourceassignment**.

| Avskrevet felt i msdyn\_projecttask (Prosjektoppgave) | Nytt felt i msdyn\_resourceassignment (Ressurstilordning) |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

Følgende felt er lagt til i enheten **msdyn\_resourceassignment**:

* msdyn\_plannedcost
* msdyn\_plannedsales

Følgende felt for planlagt, faktisk og gjenstående kostnad og salg er uendret i enheten **msdyn\_projecttask**:

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales


[!INCLUDE[footer-include](../../includes/footer-banner.md)]