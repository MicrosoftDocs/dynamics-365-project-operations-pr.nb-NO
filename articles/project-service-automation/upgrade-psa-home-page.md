---
title: Startsiden for oppgradering
description: Dette emnet viser hvor du finner viktig informasjon om nye og endrede funksjoner i Dynamics 365 Project Service Automation, og prosessen med å oppgradere til nyeste versjon.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 for Project Service 3.x
author: rumant
ms.assetid: c92d0849-e40c-4a56-9719-34030fbf5991
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 55f544636f39fc4faae06fdd512f859800bb7b44
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754151"
---
# <a name="upgrade-home-page"></a>Startsiden for oppgradering

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>Oppgradere fra PSA-versjon 2.x eller 1.x til versjon 3.x

### <a name="new-instances"></a>Nye forekomster

Fra og med 17. mai 2019, når Project Service Automation velges under klargjøring av en ny forekomst, installeres versjon 3. x som standard.

### <a name="existing-instances"></a>Eksisterende forekomster

Før måtte kunder som har en forekomst av PSA versjon 2.x og måtte oppgradere til versjon 3.x, som er UCI-versjonen (Unified client interfaced-based) av PSA, kontakte Microsofts kundestøtte og angi detaljene for deres forekomst, slik at kundestøtten kunne aktivere forekomsten for oppgradering til versjon 3.x. Fra og med 1. mars 2020, kan kunder som har en forekomst av PSA versjon 2.x, og som må oppgradere til versjon 3.x, oppgradere forekomstene direkte fra administrasjonsportalen uten å måtte kontakte Microsofts kundestøtte.  

> [!NOTE]
> PSA versjon 3. x inneholder omfattende endringer. Den er bygd på Enhetlig grensesnitt-rammeverket for å hjelpe deg med å gi en forbedret brukeropplevelse. Den nyutviklede appen leverer et ensartet og gjennomført brukergrensesnitt som følger responsive utformingsprinsipper på best mulig måte for optimal visning på alle skjermstørrelser og enheter. Det har vært andre endringer i hele programmet. Noen av områdene som er endret, er priser, bestilling og tilordning av ressurser, tid, utgifter og godkjenninger.

Før du begynner oppgraderingsprosessen, anbefaler vi at du fullfører følgende oppgaver:

- Kontroller om både Dynamics 365 Field Service og Project Service Automation er installert på den identifiserte forekomsten. Hvis begge løsningene er installert, må du planlegge å oppgradere begge før du gjenopptar vanlig bruk av forekomsten.
- Se nøye gjennom følgende emner. Bevissthet og forståelse rundt endringene mellom versjonene hjelper deg med oppgraderingsprosessen. Disse emnene inneholder informasjon om de viktigste endringene i PSA, sammen med hensyn og anbefalinger for planlegging av oppgraderingen til versjon 3. x.

    - [Hva er nytt eller endret i Project Service Automation versjon 3](whats-new-changed-v3.md)
    - [Hensyn ved oppgradering – Project Service Automation versjon 2.x eller 1.x til versjon 3.x](upgrade-v3.md)

- Oppgrader sandkasseforekomsten din for å evaluere endringene i implementeringen før du oppgraderer produksjonsforekomsten din.

Når du har sett gjennom emnene som ble nevnt tidligere, og er klar til å oppgradere til PSA versjon 3. x eller den UCI-baserte versjonen, sender du en forespørsel til Microsoft kundestøtte for å gjøre oppgraderingen tilgjengelig fra administrasjonssenteret. Angi detaljene for forekomsten i forespørselen.

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>Eldre versjoner av PSA (PSA version 2. x) i en nyopprettet forekomst

Fra og med 17. mai 2019 vil alle nye forekomster ha UCI som standardklient. Når det gjelder justering til denne endringen, blir PSA-versjon 3. x og Field Service versjon 8.x klargjort som standard, fordi disse versjonene er utformet for å fungere med UCI-klienten.

Fra og med 1. mars 2020 kan ikke Dynamics PSA-kunder lenger opprette nye miljøer med eldre versjoner av PSA, for eksempel PSA versjon 2.x eller lavere. Alle nye miljøer vil bare få versjon 3.x av PSA.

> [!NOTE]
> For å få best mulig utbytte når du bruker eldre versjoner av Field Service og PSA, går du til siden **Systeminnstillinger**, og for feltet **Bruk bare det nye enhetlige grensesnittet (anbefales)** velger du **Nei**, fordi disse versjonene ikke er utformet for å lastes inn på riktig måte i UCI. Når du har deaktivert UCI, kan du åpne og kjøre disse versjonene av Field Service og PSA ved å bruke den gamle webklienten. Hvis du vil ha informasjon om hvordan du deaktiverer UCI-klienten, kan du se [Aktiver bare det enhetlige grensesnittet](../admin/enable-unified-interface-only.md).
