---
title: Annuller en prosjektleverandørfaktura
description: Dette emnet forklarer hvordan du annullerer en prosjektleverandørfaktura i Microsoft Dynamics 365 Project Operations og den økonomiske virkningen av å annullere en prosjektleverandørfaktura.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 87f6bdca30c5779e3d70922e75609ff4cdfca167
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580652"
---
# <a name="cancel-a-project-vendor-invoice"></a>Annuller en prosjektleverandørfaktura

[!include [banner](../../includes/dataverse-preview.md)]

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Når en leverandørfaktura er bekreftet, kan den ikke redigeres eller slettes. Hvis det oppstod en feil på en leverandørfaktura som ble bekreftet, kan du bruke annulleringshandlingen til å reversere virkningen av leverandørfakturaen og opprette en ny leverandørfaktura.

Når du velger **Annuller** på en leverandørfaktura, skjer følgende:

1. Statusen for leverandørfakturaen oppdateres til **Annullert**.
2. Den annullerte leverandørfakturaen og de relaterte oppføringene blir skrivebeskyttet og kan ikke redigeres eller slettes.
3. Eventuelle kostnader som ble opprettet basert på leverandørfakturalinjer som en del av bekreftelsen på leverandørfakturaen, reverseres.
4. Hvis noen faktiske kostnader ble koblet til leverandørfakturalinjene som en del av samsvarsprosessen, reverserte den opprinnelige leverandørfakturabekreftelsen dem. Under annullering av leverandørfaktura blir de faktiske kostnadene opprettet på nytt. Opprinnelsen peker til tids-, utgifts- eller materialbruksoppføringer.
5. Når leverandørfakturaen er annullert, kan du igjen opprette rettelsesdagboker, hente inn oppføringer for prosesstid og annullere godkjenning av opprinnelig klokkeslett, utgifter eller faktiske beløp.

> [!NOTE]
> Bare bekreftede prosjektleverandørfakturaer kan annulleres. Leverandørfakturaer i andre byer kan ikke annulleres.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
