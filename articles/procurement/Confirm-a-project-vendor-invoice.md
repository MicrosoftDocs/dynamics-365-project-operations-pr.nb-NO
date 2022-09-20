---
title: Bekreft prosjektleverandørfakturaer
description: Denne artikkelen forklarer hvordan du bekrefter en prosjektleverandørfaktura i Microsoft Dynamics 365 Project Operations og beskriver den økonomiske virkningen av å bekrefte en prosjektleverandørfaktura.
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475450"
---
# <a name="confirm-project-vendor-invoices"></a>Bekreft prosjektleverandørfakturaer

_ **Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer

Når parameteren **Prosjektleder må bekrefte manuelt** er aktivert, får leverandørfakturaer som opprettes i Microsoft Dataverse, statusen **Utkast**. Leverandørfakturaer som opprettes på denne måten, må gjennomgås og bekreftes manuelt. Når parameteren **Prosjektleder må bekrefte manuelt** er deaktivert, blir leverandørfakturaer som opprettes i Dataverse, automatisk bekreftet. Ingen flere handlinger kreves. 

Etter at du har kontrollert alle linjene i en leverandørfaktura i Dynamics 365 Project Operations, velger du **Bekreft** for å bekrefte leverandørfakturaen.

Når du velger **Bekreft** på en leverandørfaktura, skjer følgende:

1. Statusen for leverandørfakturaen oppdateres til **Bekreftet**.
1. Den bekreftede leverandørfakturaen og de relaterte oppføringene blir skrivebeskyttet og kan ikke redigeres eller slettes.
1. Hvis noen faktiske kostnader refererer til leverandørfakturalinjen som en del av samsvarsprosessen, reverseres alle faktiske kostnader som er tilknyttet linjen for leverandørfakturaen det refereres til.
1. Nye faktiske kostnader opprettes ved hjelp av informasjonen på leverandørfakturalinjen.
1. Du kan ikke lenger opprette rettelsesjournaler, behandle tilbakekalling av tidsoppføringer eller annullere godkjenning av opprinnelig tid, utgifter eller faktiske beløp som ble reversert.
1. I Dynamics 365 Finance oppdateres verdien for **Prosjektkostnad** ved hjelp av integreringsjournalen for prosjekt, og integrasjonskontoen for innkjøp *reverseres* etter at integreringsjournalen for prosjekt er postert.

> [!NOTE]
> Hvis en linje i en leverandørfaktura har en annen verifiseringsstatus enn **Fullført**, kan ikke leverandørfakturaen bekreftes.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
