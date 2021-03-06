---
title: Oppfyllelse av generelle ressurskrav
description: Dette emnet gir informasjon om bestilling av navngitte ressurser for et generisk ressurskrav.
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
ms.openlocfilehash: 76dd47fa2451b5cb61298ff332d77bae646a288a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897598"
---
# <a name="generic-resource-requirement-fulfillment"></a>Oppfyllelse av generelle ressurskrav

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Du kan bestille en navngitt ressurs som erstatter en generisk ressurs som har et ressurskrav.

1. På siden **Prosjekter** velger du kategorien **Team**.
2. Velg den generelle ressursen som har et ressurskrav, fra listen, og klikk deretter **Bestill**. Du kan også åpne ressurskravet og deretter klikke **Bestill**.
3. På siden **Planleggingsassistent** velger du en navngitt ressurs som skal reserveres til prosjektteamet, og deretter klikker du **Bestill**.

Når bestillingen er fullført og oppfylt med en navngitt ressurs, erstattes den generelle ressursen med den navngitte ressursen.

Tilordningene i tidsplanen oppdateres også med den navngitte ressursen.

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Oppfylle en generisk ressurs med flere navngitte ressurser
Å oppfylle et krav for en generell ressurs med flere navngitte ressurser ligner på å tilordne én enkelt navngitt ressurs. Det er for eksempel en oppgave med en varighet på fem dager, og 120 timer arbeid. Denne oppgaven kan ikke full føres av én ressurs som arbeider med en vanlig 8-timers dag i løpet av en uke på fem dager. 

Kravet er for 120 timer i løpet av fem dager, som er 24 timer per dag.

Dette er et eksempel på når flere navngitte ressurser er nødvendige for å oppfylle en generisk ressursforespørsel. Du må reservere flere ressurser for å oppfylle behovet.

Hovedforskjellen i dette scenariet er at den generelle ressursen beholdes i teamet som er tilordnet til oppgaven, og medlemmer av ressursteamet som er bestilt, blir ikke tilordnet som en del av posisjonen. Prosjektlederen kan tilordne arbeidet slik det passer til de navngitte ressursene. **Avstemming**-visningen kan hjelpe en prosjektleder med å dele opp bestillinger på tvers av flere ressurser i oppgavetildelinger. Dette gjøres ikke automatisk fordi et scenario som er mer komplisert enn det enkle eksemplet ovenfor, for eksempel hvor du har en gruppe oppgaver som utgjør behovet, må intensjonen av hvordan prosjektlederen vil tilordne, antas av systemet. Siden systemet ikke kan forstå hensikt, er det sannsynlig at antakelsene vil være forskjellige fra tiltenkt, og det skjer et uriktig eller uforutsigbart resultat. Det forutsigbare resultatet er at den generelle ressursen holdes tilordnet til prosjektlederen med hensikt oppretter tildelinger, med hjelp av **Avstemming**-visningen.


