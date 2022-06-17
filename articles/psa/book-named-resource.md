---
title: Bestille navngitte ressurser fra ressurskrav
description: Denne artikkelen inneholder informasjon om bestilling av navngitte ressurser for et generisk ressurskrav.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 9598490da1905227e517da8ba90f8ffd1df88566
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916254"
---
# <a name="book-named-resources-from-resource-requirements"></a>Bestille navngitte ressurser fra ressurskrav

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Du kan bestille en navngitt ressurs som erstatter en generisk ressurs som har et ressurskrav.

1. I Project Service Automation (PSA), på **Prosjekter**-siden, klikker du på kategorien **Team**.
2. Velg den generelle ressursen som har et ressurskrav, fra listen, og klikk deretter **Bestill**. Du kan også åpne ressurskravet og deretter klikke **Bestill**.


![Bestille et generisk teammedlem.](media/RM-how-to-14.png)


3. På siden **Planleggingsassistent** velger du en navngitt ressurs som skal reserveres til prosjektteamet, og deretter klikker du **Bestill**.

![Reservere et generisk teammedlem ved hjelp av planleggingsassistenten.](media/RM-how-to-15.png)

Når bestillingen er fullført og oppfylt med en navngitt ressurs, erstattes den generelle ressursen med den navngitte ressursen.

![Navngitt teammedlem erstatter et generisk teammedlem.](media/RM-how-to-16.png)

Tilordningene i tidsplanen oppdateres også med den navngitte ressursen.

![Navngitt teammedlem tilordnet til prosjektoppgaver.](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Oppfylle en generisk ressurs med flere navngitte ressurser
Å oppfylle et krav for en generell ressurs med flere navngitte ressurser ligner på å tilordne én enkelt navngitt ressurs. Det er for eksempel en oppgave med en varighet på fem dager, og 120 timer arbeid. Denne oppgaven kan ikke full føres av én ressurs som arbeider med en vanlig 8-timers dag i løpet av en uke på fem dager. 

![En oppgave som krever 120 arbeidstimer over fem dager.](media/RM-how-to-21.png)

Kravet er for 120 timer i løpet av fem dager, som er 24 timer per dag.

![Krav per dag.](media/RM-how-to-22.png)

Dette er et eksempel på når flere navngitte ressurser er nødvendige for å oppfylle en generisk ressursforespørsel. Du må reservere flere ressurser for å oppfylle behovet.

![Bestille flere ressurser for å oppfylle behovet.](media/RM-how-to-23.png)

Hovedforskjellen i dette scenariet er at den generelle ressursen beholdes i teamet som er tilordnet til oppgaven, og medlemmer av ressursteamet som er bestilt, blir ikke tilordnet som en del av posisjonen. Prosjektlederen kan tilordne arbeidet slik det passer til de navngitte ressursene. **Avstemming**-visningen kan hjelpe en prosjektleder med å dele opp bestillinger på tvers av flere ressurser i oppgavetildelinger. Dette gjøres ikke automatisk fordi et scenario som er mer komplisert enn det enkle eksemplet ovenfor, for eksempel hvor du har en gruppe oppgaver som utgjør behovet, må intensjonen av hvordan prosjektlederen vil tilordne, antas av systemet. Siden systemet ikke kan forstå hensikt, er det sannsynlig at antakelsene vil være forskjellige fra tiltenkt, og det skjer et uriktig eller uforutsigbart resultat. Det forutsigbare resultatet er at den generelle ressursen holdes tilordnet til prosjektlederen med hensikt oppretter tildelinger, med hjelp av **Avstemming**-visningen.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
