---
title: Bestille til et prosjekt
description: Denne artikkelen inneholder informasjon om bestilling av en ressurs til et prosjekt.
author: ruhercul
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dca9d722eae595af7a81c2b4684729d7658ed012
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928536"
---
# <a name="book-to-a-project"></a>Bestille til et prosjekt

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Det er tilfeller der en prosjektleder eller ressursleder må tildele en ressurs til et prosjekt uten at et bestemt krav er definert fra et generelt teammedlem. Dette kan oppnås på én av tre måter.

- Bestille fra teammedlemsrutenettet
- Bestille fra planleggingstavlen
- Bestille fra **Prosjekt**-skjemaet

## <a name="book-from-the-team-member-grid"></a>Bestille fra teammedlemsrutenettet

Hvis organisasjonen din opererer i hybrid ressursallokeringsmodus, kan prosjektlederen reservere en ressurs direkte i prosjektet ved å utføre følgende trinn.

1. Fra prosjektet går du til teammedlemsrutenettet og velger **Ny**.
2. Definer stillingsnavnet og rollen for ressursen.
3. Velg den bestillbare ressursen fra det tilgjengelige oppslaget.
4. Etter at du har valgt ressursen, definerer du følgende feltinformasjon for å bestille ressursen:

    - Startdato
    - Sluttdato
    - Tilordningsmetode
    - Eventuelle timer
    - Prosjektgodkjenner

6. Velg **Lagre og lukk**

## <a name="book-from-the-schedule-board"></a>Bestille fra planleggingstavlen

Når en ressursleder må reservere en ressurs direkte til et prosjekt, kan de bruke planleggingstavlen og prosjektkravet. Prosjektkravet er et ressurskrav som alltid er tilgjengelig for bestilling. Fullfør fremgangsmåten nedenfor for å bestille direkte til et prosjekt fra planleggingstavlen.

1. Naviger til planleggingstavlen og filtrer etter ressursene du vurderer for kravet, på venstre side.
2. Velg **Prosjekt**-fanen i den nederste ruten for å vise en liste over prosjektkrav.
3. Dra kravet til en ressurs, og definer følgende informasjon:

    - Startdato
    - Sluttdato
    - Bestillingsstatus
    - Bestillingsmetode
    - Duration
   
   > [!NOTE]
   > For tiden støtter ikke Dynamics 365 Project Operations planleggingstavlen.   

## <a name="book-from-the-project-form"></a>Bestille fra Prosjekt-skjemaet

Som prosjektleder må du kanskje reservere en ressurs til et prosjekt, men du kjenner bare til vilkårene i stedet for navnet på ressursen. Fullfør fremgangsmåten nedenfor for å bruke planleggingsassistenten til å finne en ressurs basert på eventuelle tilgjengelige attributter for ressursen. 

1. Naviger til prosjektet, og velg **Bestill** for å åpne planleggingsassistenten.
2. Bruk filtrene på venstre side av planleggingsveiviseren til å begrense vilkårene, og velg **Søk.**
3. Basert på ressurser som returneres i resultatet, kan du reservere en ressurs.

> [!NOTE]
> Denne metoden oppretter ingen bestillinger for ressursen. I stedet legges ressursen til for teamet. Når teammedlemmene er lagt til i prosjektet, kan prosjektlederen bruke vedlikehold av bestillinger eller utvide bestillinger til å legge til de nødvendige bestillingerne i ressursen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
