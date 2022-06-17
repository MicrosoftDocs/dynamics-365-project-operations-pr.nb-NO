---
title: Bekrefte en prosjektleverandørfaktura
description: Denne artikkelen forklarer hvordan du bekrefter en prosjektleverandørfaktura i Microsoft Dynamics 365 Project Operations og den økonomiske virkningen av å bekrefte en prosjektleverandørfaktura.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 092b3cd5981f7d9bb8767c7a2acb2f4952801d06
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932446"
---
# <a name="confirm-a-project-vendor-invoice"></a>Bekrefte en prosjektleverandørfaktura

[!include [banner](../../includes/dataverse-preview.md)]

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
