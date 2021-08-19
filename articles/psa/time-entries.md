---
title: Opprette tidsoppføringer
description: Dette emnet gir informasjon om hvordan du oppretter tidsoppføringer.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0d0e21d0964788564d3db9173c3a0b3378cd0049b4455a23ccc1bccd1c21d9e7
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990418"
---
# <a name="create-time-entries"></a>Opprette tidsoppføringer

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

I tidligere versjoner av Dynamics 365 Project Service Automation ble tidsoppføringer angitt med en ukebasis. I versjon 3 av Project Service Automation registreres tidsoppføringer daglig. Etter at du har opprettet en oppføring, kan du imidlertid masseopprette eller kopiere dem.

## <a name="create-a-time-entry"></a>Opprette en tidsoppføring

Følg denne fremgangsmåten for å opprette en tidsoppføring.

1. På siden **Tidsoppføringer** velger du **Ny**.
2. I dialogboksen **Hurtigoppretting: Tidsoppføring** angir du varigheten til tidsoppføringen i minutter, timer eller dager. Varigheten må angis i følgende format: *x* minutter, *x* timer eller *x* dager. Timer og dager kan også angis som desimaler, for eksempel *x,x* timer eller *x,x* dager.
3. Velg type tidsoppføring og prosjektet du vil angi tidsoppføring for.
4. Finn aktiviteten for denne tidsoppføringen i feltet **Prosjektoppgave**.

    > [!NOTE]
    > Hvis du skal opprette en tidsoppføring for en oppgave som ikke er tilordnet til en bruker, går du til **Prosjektoppgave**, velger **Søk**-knappen, velger **Endre visning** og deretter **Alle aktive prosjektoppgaver** for å vise alle oppgavene.

5. Angi en beskrivelse hvis det kreves en beskrivelse, og velg deretter **Lagre og lukk**.

Når tidsoppføringen er opprettet og lagret, kan du redigere den i tidsrutenettet for tidsoppføringen. Tidsoppføringsrutenettet støtter to formater:

- Du kan angi tidsoppføringer i **tt:mm**-format. Dette formatet blir deretter konvertert til timer og brøker.
- Du kan skrive inn timer og brøker direkte.

Vær oppmerksom på at brøkene i en time ikke er minutter. Derfor representerer 1,5 timer 1 time og 30 minutter. Den samme regelen gjelder for deler av en dag. Én dag er 24 timer, og 0,5 dager representerer 12 timer.

## <a name="bulk-create-time-entries"></a>Masseopprette tidsoppføringer

Etter at du har opprettet noen få oppføringer, kan du bruke dem til å opprette flere tidsoppføringer samtidig.

1. På siden **Tidsoppføringer** velger du **Kopier uke**.
2. I feltgruppen **Fra periode** i feltene **Startdato** og **Sluttdato** definerer du datointervallet tidsoppføringer skal kopieres fra.
3. I feltgruppen **Til-periode** i feltet **Startdato** angir du datoen tidsoppføringer skal opprettes for.
4. Velg **Kopier** for å opprette en kopi av tidsoppføringene som samsvarer med ukedagen som er angitt i feltgruppen **Til periode**. Mandagens tidsoppføring fra forrige uke blir for eksempel kopiert til mandag for uken som er angitt i feltgruppen **Til-periode**.

## <a name="import-data-for-time-entries"></a>Importere data for tidsoppføringer

Du kan importere data fra prosjektbestillinger og -tilordninger. Når du importerer data, kan du angi datointervallet for bestillinger for å importere og deretter eksplisitt velge bestillinger som skal opprettes som **Utkast**-tidsoppføringer.

## <a name="group-by-sort-search-and-filter-capabilities"></a>Funksjoner for å gruppere etter, sortere, søke og filtrere

Du kan gruppere og filtrere tidsoppføringer etter dimensjonene som er angitt i kolonnene. I feltet **Grupper etter** velger du dimensjonen som skal brukes til å filtrere tidsoppføringer. Du kan også sortere tidsoppføringsregistreringer i stigende eller synkende rekkefølge ved å bruke sorteringspilen i kolonneoverskriftene. Du kan også vise eller skjule oppføringer ved å velge **Filter**-knappen på kolonneoverskriftene og deretter, i **Søk**-boksen, angi teksten som skal brukes til å søke etter tidsoppføringer etter prosjektnavn, prosjektoppgave, tidsoppføring eller ressurs.


[!INCLUDE[footer-include](../includes/footer-banner.md)]