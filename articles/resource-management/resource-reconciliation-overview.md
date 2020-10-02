---
title: Oversikt over ressursavstemming
description: Dette emnet gir informasjon om hvordan du sørger for justering av ressursbestillinger og tilordninger til prosjekter.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1b60ed9d15f51ff01f27bcc231f5db27513a838f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897463"
---
# <a name="resource-reconciliation-overview"></a>Oversikt over ressursavstemming

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

For teammedlemmer er bestillinger og tildelinger løst sammenkoblet. Ressurser kan med andre ord ha tilordninger, men ikke bestillinger, eller de kan ha bestillinger, men ikke tilordninger. Ideelt sett bør bestillinger og tilordninger rettes inn mot hverandre, slik at ressurser har forpliktet kapasitet til å utføre oppgavetilordningene. Det kan imidlertid hende at bestillinger blir basert på tilgjengelighet, og det kan hende at oppgavetidspunkter endres etter hvert som prosjektet fortsetter. Derfor gir den løse koblingen av bestillinger og tildelinger fleksibilitet.

**Avstemming**-kategorien i **Prosjekt**-skjemaet gjør at prosjektledere kan avstemme teammedlemmenes bestillinger og deres tildelinger for prosjektteam.

Kategorien **Avstemming** viser også bestillinger og tilordninger nedover til nivået for den individuelle oppgavetilordningen for hvert teammedlem. Timer vises i celler som representerer tidsperioder, fra måneder til dager.

Kategorien viser også en total nettosum for prosjektet, sammen med en **Total**-kolonne.

For hver ressurs beregner kategorien forskjellen mellom teammedlemmenes bestillinger og en beregnet verdi teammedlemmets oppgavetilordninger. Ideelt sett bør denne forskjellen være 0 (null). Det bør med andre ord ikke være forskjell mellom bestillinger og tildelinger. Forskjellene er fargelagt og skyggelagt for å rette oppmerksomheten mot to betingelser:

- **Få bestillinger** – for få bestillinger inntreffer når en ressurs har flere tildelinger enn bestillinger. Ettersom denne kapasiteten ikke er reservert, kan det hende at en prosjektleder vil korrigere denne betingelsen ved å utvide ressursens bestillinger for å dekke underskuddet.
- **Overflødige bestillinger** – Overflødige bestillinger skjer når en ressurs er bestilt til prosjektet, men ikke er tilordnet til aktiviteter. Denne tilstanden kan være akseptabel i saker der ressursen ble bestilt til prosjektet før oppgavetilordningen ble utført. I andre tilfeller er det imidlertid ikke planlagt at ressursen skal tilordnes til oppgaver. I slike tilfeller bør prosjektlederen vurdere å annullere ressursens bestillinger, slik at kapasiteten kan brukes for et annet prosjekt.

Når du i noen tilfeller viser tid på høyere nivå enn dagnivået (for eksempel månedsnivået), kan det hende du ser en netto differanse på null for en ressurs (med andre ord bestillinger = tildelinger). Hvis du imidlertid viser tid på ukenivå, ser du at det er tildelinger på null timer og bestillinger på 40 timer i den første uken, men tildelinger på 40 timer og bestillinger på null timer i den andre uken. Totalt er bestillingene og tilordningene avstemte, men de skiller seg fra én uke til den neste.

Når du viser tid på høyere nivåer, har celler i **Avstemming**-kategorien en indikator som informerer deg om at det er forskjeller på lavere nivåer. Ved å dobbeltklikke i en celle kan du zoome inn for å vise forskjellen. Du kan deretter høyreklikke for å zoome ut. Ved å velge en ressurs og deretter bruke kontrollen **Neste forskjell** på verktøylinjen i rutenettet kan du gå til den neste forskjellen mellom bestillinger og tildelinger for denne ressursen. Deretter kan du bruke kontrollen **Forrige forskjell** til å gå tilbake. Du kan også slå av forskjellsindikatoren og virkemåten for navigasjon under **Innstillinger**.


Hvis du har oppgavetildelinger for en ressurs, men ingen bestillinger, går du til **Prosjekter**-siden, i kategorien **Avstemming** og velger **Utvid bestilling**. Dialogboksen **Utvid bestilling** vises med bestillingen som er nødvendig for å løse ressursens underskudd. Den viser også ressursens eksisterende bestillinger på tvers av alle prosjekter eller andre enheter som kan planlegges. Hvis du velger **OK** for å opprette en bestilling for ressursen, uavhengig av om ressursen er tilgjengelig, kan det oppstå overbestilling.

Prosjektlederen eller ressurslederen kan deretter bruke planleggingstavlen til å behandle eventuelle situasjoner der en ressurs er overbestilt utover dens kapasitet.

