---
title: Oversikt over ressursavstemming
description: Dette emnet inneholder informasjon som vil hjelpe deg med å sikre at ressursbestillinger og tildelinger for prosjekter er justert.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 5c48589e745dbf6e3a51ae749b9b45491d26406e
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368218"
---
# <a name="resource-reconciliation-overview"></a>Oversikt over ressursavstemming

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

For teammedlemmer er bestillinger og tildelinger løst sammenkoblet. Ressurser kan med andre ord ha tilordninger og ikke bestillinger, eller de kan ha bestillinger og ikke tilordninger. Ideelt sett bør bestillinger og tilordninger rettes inn mot hverandre, slik at ressurser har forpliktet kapasitet til å utføre oppgavetilordningene. Det kan imidlertid hende at bestillinger blir basert på tilgjengelighet, og det kan hende at oppgavetidspunkter endres etter hvert som prosjektet fortsetter. Derfor gir den løse koblingen av bestillinger og tildelinger fleksibilitet.

I kategorien **Avstemming** på siden **Prosjekter** kan prosjektledere avstemme teammedlemmenes bestillinger og deres tildelinger for prosjektteam.

Kategorien **Avstemming** viser bestillinger og tilordninger nedover til nivået for den individuelle oppgavetilordningen for hvert teammedlem. Timer vises i celler som representerer perioder fra måneder til dager. Kategorien viser også en total nettosum for prosjektet, sammen med en **Total**-kolonne.

For hver ressurs beregner kategorien **Avstemming** forskjellen mellom teammedlemmenes bestillinger og en beregnet verdi av det teammedlemmets oppgavetilordninger. Ideelt sett bør denne forskjellen være 0 (null). Det bør med andre ord ikke være forskjell mellom bestillinger og tildelinger. Forskjellene er fargelagt og skyggelagt for å rette oppmerksomheten mot to betingelser:

- **Få bestillinger** – for få bestillinger inntreffer når en ressurs har flere tildelinger enn bestillinger. Ettersom kapasiteten ikke er reservert, kan det hende at en prosjektlederen vil korrigere denne betingelsen ved å utvide ressursens bestillinger for å dekke underskuddet.
- **Overflødige bestillinger** – Overflødige bestillinger skjer når en ressurs er bestilt til prosjektet, men ikke er tilordnet til aktiviteter. Denne tilstanden kan være akseptabel i saker der ressursen ble bestilt til prosjektet før oppgavetilordningen ble utført. I andre tilfeller der det ikke er noen plan for å tilordne ressursen til oppgaver, bør imidlertid prosjektlederen vurdere å annullere ressursbestillingene. På den måten kan kapasiteten brukes for et annet prosjekt.

Når du i noen tilfeller viser tid på høyere nivå enn dagnivået (for eksempel månedsnivået), kan det hende du ser en netto differanse på null for en ressurs (med andre ord bestillinger tilsvarer tildelinger). Hvis du imidlertid viser tid på ukenivå, ser du at det er tildelinger på null timer og bestillinger på 40 timer i den første uken, men tildelinger på 40 timer og bestillinger på null timer i den andre uken. Totalt er bestillingene og tilordningene avstemte, men de skiller seg fra én uke til den neste.

Når du viser tid på høyere nivåer, har celler i kategorien **Avstemming** en indikator som informerer deg om at det er forskjeller på lavere nivåer. Ved å trykke to ganger eller dobbeltklikke i en celle kan du zoome inn for å vise forskjellen. Du kan deretter merke og holde nede (eller høyreklikke) for å zoome ut. Ved å velge en ressurs og deretter bruke kontrollen **Neste forskjell** på verktøylinjen i rutenettet kan du gå til den neste forskjellen mellom bestillinger og tildelinger for denne ressursen. Deretter kan du bruke kontrollen **Forrige forskjell** til å gå tilbake. Du kan også slå av forskjellsindikatoren og virkemåten for navigasjon under **Innstillinger**.

Hvis du har oppgavetildelinger for en ressurs, men ingen bestillinger, velger du Få bestillinger i kategorien **Avstemming** på siden **Prosjekter**, og deretter velger du **Utvid bestilling**. Dialogboksen **Utvid bestilling** vises med bestillingen som kreves for å løse ressursens underskudd. Dialogboksen viser også ressursens eksisterende bestillinger på tvers av alle prosjekter eller andre enheter som kan planlegges. Hvis du velger **OK** for å opprette en bestilling for ressursen, uavhengig av om ressursen er tilgjengelig, kan det oppstå overbestilling.

Bestillinger som opprettes via handlingen **Utvid bestilling**, er knyttet til det primære prosjektkravet. Når en utvidelse startes, kan ikke det spesifikke kravet som må utvides, fastsettes, fordi ressursen kan være knyttet til mer enn ett krav for prosjektet.

Prosjektlederen eller ressurslederen kan deretter bruke planleggingstavlen til å behandle eventuelle situasjoner der en ressurs er overbestilt utover dens kapasitet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]