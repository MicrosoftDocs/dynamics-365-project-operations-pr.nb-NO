---
title: Avbryte tidligere godkjente tids- og utgiftsoppføringer
description: Dette emnet gir informasjon om hvordan du annullerer en godkjent prosjekttid og en utgiftstransaksjon.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
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
ms.openlocfilehash: 0ea816040570cc8f6ddf3c5ec8a74ac092fc68b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081795"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a>Avbryte tidligere godkjente tids- eller utgiftsoppføringer

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

I den nyeste versjonen av Dynamics 365 Project Service Automation kan godkjennere annullere tids- eller utgiftsoppføringer de tidligere har godkjent.

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a>Avbryte en tidliger godkjent tids- eller utgiftsoppføring

Følg disse trinnene for å annullere en tids- eller utgiftsoppføring du har godkjent tidligere.

1. Gå til **Prosjekter** \> **Mitt arbeid** \> **Godkjenninger**.
2. På listesiden **Godkjenninger** endrer du visningen til **Mine tidligere godkjenninger**. En liste over tids- og utgiftsoppføringene du godkjente tidligere, vises.
3. Velg én eller flere oppføringer, og velg deretter **Kanseller godkjenning**. Du får en varselsmelding.
4. Velg **OK** for å annullere godkjenningen.

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a>Forstå virkningen av å annullere godkjenning av en tids- eller godkjenningsoppføring

Når en godkjenning annulleres, får dette både driftsinnvirkning og finansiell innvirkning.

### <a name="operational-impact"></a>Driftsinnvirkning

På driftssiden, når en godkjenning annulleres, tilbakestilles statusen for oppføringen til **Utkast** , og godkjenningen vises ikke lenger i visningen **Mine tidligere godkjenninger**. I stedet vises den annullerte godkjenningen i visningen **Tidsoppføringer for godkjenning** eller **Utgiftsoppføringer for godkjenning** , avhengig av om den var en tidsoppføring eller en utgiftsoppføring. I tillegg endres statusen for den relaterte tids- eller utgiftsoppføringen til **Sendt** , slik at den relaterte oppføringen samsvarer med godkjenninger som har statusen **Utkast**.

Som godkjenner kan du redigere noen av feltene i en godkjenning som har statusen **Utkast**. Disse feltene inkluderer **Faktureringstype** og **Fakturerbare timer for tidsoppføringer**. Når du har gjort endringer, kan du godkjenne oppføringen på nytt. Du kan også avvise oppføringen. Hvis du avviser godkjenningen av en tidsoppføring, blir statusen for oppføringen endret til **Returnert**. Hvis du avviser godkjenningen av en utgiftsoppføring, blir statusen endret til **Avvist**. Det vil si at både returnerte og avviste oppføringer fungerer på samme måte som en oppføring som har statusen **Utkast**. Et prosjektteammedlem kan enten gjøre de nødvendige endringene i oppføringen og deretter sende den på nytt for godkjenning, eller slette oppføringen helt.

### <a name="financial-impact"></a>Økonomisk innvirkning

Et prosjekt berøres også finansielt når en godkjenning annulleres. For det første oppdateres de tilsvarende faktiske verdiene for kost og salg på følgende måte:

- Justeringsstatusen settes til **Justert**.
- Faktureringsstatusen settes til **Kansellert**.

Deretter opprettes tilbakeføringsoppføringer i tabellen over faktiske verdier. For å opprette tilbakeføringsoppføringer kopierer systemet over feltverdiene fra de opprinnelige faktiske verdiene. De eneste verdiene som ikke kopieres over, er antallsverdiene. Disse verdiene reverseres i stedet. Reverserte faktiske verdier opprettes både for de faktiske verdiene **Kostnad** og **Ufakturert salg**. Feltet **Justeringsstatus** for de tilbakeførte faktiske verdiene settes til **Kan ikke justeres** , og faktureringsstatusen settes til **Annullert**.

Når du har gjort disse endringene, vil beløpet som er registrert som brukt på prosjektet, og restinntekten for prosjektet, ikke lengre regnes med for beløpene som disse faktiske verdiene representerer.
