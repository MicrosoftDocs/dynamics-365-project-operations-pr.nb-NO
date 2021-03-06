---
title: Oversikt over planleggingsassistent
description: Dette emnet inneholder informasjon om hvordan du arbeider med planleggingsassistenten for å bestille ressurser.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908420"
---
# <a name="schedule-assistant-overview"></a>Oversikt over planleggingsassistent

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Planleggingsassistenten brukes til å reservere ressurser basert på behov som er definert av prosjektlederen. Planleggingsassistenten er avhengig av parameterne som er angitt i ressurskravet for å finne ressursen. Planleggingsassistenten anbefaler ressurser som samsvarer med relevante krav, for eksempel hvilke tidsvinduer eller ferdigheter som kreves.

Når egnede ressurser er identifisert, kan ressurs- eller prosjektlederen reservere ressursen i arbeidet.

## <a name="prerequisites"></a>Forutsetninger

Planleggingsassistenten er en del av Universal Resource Scheduling-løsningen. Denne løsningen er inkludert og installert med Dynamics 365 Project Operations, Dynamics 365 Field Service og Dynamics 365 Customer Service.

## <a name="matching-requirements-and-resources"></a>Samsvare krav og ressurser

Et generert ressurskrav er basert på detaljer som for eksempel:

-   Kjennetegn
-   Roller
-   Forretningsenheter
-   Ressurspreferanser
-   Innsatsomfang
-   Tidssone

Planleggingsassistenten bruker disse detaljene til å filtrere ressurser.

## <a name="launch-the-schedule-assistant"></a>Start planleggingsassistenten.

Det er to måter å starte planleggingsassistenten på. Hvis du bruker hybrid modus, kan du velge et teammedlem med et ressurskrav som ikke er oppfylt, i rutenettet for teammedlemmer, og deretter velge **Bestill**. Hvis du bruker sentral modus, er det ressurslederen som finner og velger ressursen.

## <a name="schedule-assistant-filters"></a>Filtre i planleggingsassistenten

Når planleggingsassistenten kjører, vises detaljene fra ressurskravet som filtrerte verdier i den venstre ruten. Ressurslederen eller prosjektlederen kan finjustere resultatene ved å justere filtrene, slik at de dekker planleggingsbehovene.

Filterruten viser arbeidsrelaterte alternativer, blant annet følgende:

-   Start og slutt for arbeidet
-   Kjennetegn
-   Roller
-   Organisasjonsenheter
-   Ressursstyringsfirma
-   Ressurstyper
-   Foretrukne ressurser
