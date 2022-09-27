---
title: Bokføre utgiftsrapporter
description: Denne artikkelen forklarer hvordan du bokfører utgiftsrapporter.
author: ramagadu
ms.date: 08/12/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ae4559a08553236158a663513401cb38cbe28f
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524882"
---
# <a name="post-expense-reports"></a>Bokføre utgiftsrapporter

Når en reiseregning er godkjent og overført til hovedboken, kan den bokføres. Når du bokfører en reiseregning, identifiseres utgifter som er kvalifisert for mva-fradrag. Oppgaven med å kontrollere og tilbakebetale mva-betalinger er tilordnet til den ansatte som er ansvarlig for å kontrollere reiseregningen.

Hvis utgifter i en reiseregning belastes et annet selskap enn selskapet som ansetter den ansatte, må du kontrollere både selskapet som disse utgiftene skyldes til, og selskapet de skylder fra. Den ansatte som sendte en reiseregning, arbeider for eksempel for DAT-firmaet, men belastet en utgift til DIR-firmaet. I dette tilfellet er DAT firmaet som utgiften skyldes til, og DIR er firmaet som utgiften skyldes fra. Når du har bekreftet disse journallinjene, kan du postere utgiftslinjene til hovedboken.

Hvis du vil postere en reiseregning, velger du reiseregningen på siden **Godkjente reiseregninger**, og deretter velger du **Bokfør** i handlingsruten.

Du kan også bokføre alle reiseregningene i listen samtidig. Velg alle reiseregningene, og velg deretter **Bokfør**.

## <a name="enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature"></a>Aktiver funksjonen Mulighet til å postere utgiftsansvar i leverandørvaluta for betalingsmetode for kontanter

Med funksjonen **Mulighet til å postere utgiftsansvar i leverandørvaluta for betalingsmetode for kontanter** blir det mulig å postere utgiftsrapporter i en leverandørvaluta for betalingsmetoden for kontanter.

Når du sender inn utgifter betalt med kontanter, posteres utgiftsrapporter i regnskapsvalutaen for øyeblikket. På grunn av beløpskonvertering mellom transaksjonsvalutaen, regnskapsvalutaen og leverandørvalutaen blir et feil beløp betalt til leverandører hvis transaksjonsdatoen for utgiften og den faktiske betalingsdatoen har forskjellige valutakurser.

Denne funksjonen sikrer at leverandørsaldoen registreres i leverandørvalutaen når utgiftsrapporten posteres.

1. Gå til **Arbeidsområder** \> **Funksjonsbehandling**.
2. I listen finner du og velger **Mulighet til å postere utgiftsansvar i leverandørvaluta for betalingsmetode for kontanter** og velger deretter **Aktiver nå**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
