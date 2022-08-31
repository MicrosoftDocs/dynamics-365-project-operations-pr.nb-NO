---
title: Bekrefte en prosjektleverandørfaktura
description: Denne artikkelen forklarer hvordan du bekrefter en prosjektleverandørfaktura i Microsoft Dynamics 365 Project Operations og den økonomiske virkningen av å bekrefte en prosjektleverandørfaktura.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4dafbe64e0727957068d68f510202a12871b62aa
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261525"
---
# <a name="confirm-a-project-vendor-invoice"></a>Bekrefte en prosjektleverandørfaktura

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Når du har kontrollert alle linjene i en leverandørfaktura i Microsoft Dynamics 365 Project Operations, kan du bruke handlingen Bekreft til å bekrefte leverandørfakturaen.

Når du velger **Bekreft** på en leverandørfaktura, skjer følgende:

1. Statusen for leverandørfakturaen oppdateres til **Bekreftet**.
2. Den bekreftede leverandørfakturaen og de relaterte oppføringene blir skrivebeskyttet og kan ikke redigeres eller slettes.
3. Hvis noen faktiske kostnader refererer til leverandørfakturalinjen som en del av samsvarsprosessen, reverseres alle faktiske kostnader som er tilknyttet linjen for leverandørfakturaen det refereres til.
4. Nye faktiske kostnader opprettes ved hjelp av informasjonen på leverandørfakturalinjen.
5. Når leverandørfakturaen er bekreftet, kan du ikke lenger opprette rettelsesjournaler, hente inn oppføringer for prosesstid eller annullere godkjenning av opprinnelig klokkeslett, utgifter eller faktiske beløp som ble reversert.

> [!NOTE]
> Hvis en linje i en leverandørfaktura har en annen verifiseringsstatus enn **Fullført**, kan ikke leverandørfakturaen bekreftes.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
