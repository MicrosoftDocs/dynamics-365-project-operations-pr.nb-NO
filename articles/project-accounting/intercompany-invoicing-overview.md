---
title: Oversikt over konsernintern fakturering
description: Dette emnet gir informasjon og eksempler på konsernintern fakturering for prosjekter.
author: sigitac
ms.date: 11/19/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b7bb4384657c71552390bbc3d60f3c5d0e4136b4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586264"
---
# <a name="intercompany-invoicing-overview"></a>Oversikt over konsernintern fakturering

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Det kan hende at organisasjonen har flere divisjoner, datterselskaper og andre juridiske enheter som overfører produkter og servicer til hverandre for prosjekter. Den juridiske enheten som tilbyr servicen eller produktet, kalles den *juridiske enheten som låner ut*. Den juridiske enheten som mottar servicen eller produktet, kalles den *juridiske enheten som låner*.

Illustrasjonen nedenfor viser et typisk scenario der to juridiske enheter, Contoso Robotics USA (den juridiske enheten som låner) og Contoso Robotics UK (den juridiske enheten som låner ut) deler ressurser for å levere et prosjekt for kunden, Brusefoss industrier. I dette scenarioet er Contoso Robotics USA kontraktert for å levere arbeidet til Brusefoss industrier.

![Konsernintern fakturering.](./media/IntercompanyScenario.png) 

Dynamics 365 Project Operations bruker følgende flyt til å behandle konserninterne transaksjoner:

1. Ressurser fra den juridiske enheten som låner ut registrerer konsernintern tids- eller utgiftstransaksjoner ved å postere tid og utgifter opp mot prosjektet i den juridiske enheten som låner.
2. Tids- og utgiftskostnader registreres i utlånsfirmaet ved hjelp av prislisten over enhetskostnad til firmaet som låner.
3. Interkonserne ufakturerte salgstransaksjoner registreres i utlånsfirmaet ved hjelp av prislisten over enhetskostnaden til firmaet som låner.
4. Ufakturert inntekt registreres i firmaet som låner ved hjelp av salgsprislisten for prosjektkontrakten. Kunden kan faktureres når ufakturert inntekt registreres. Kunden trenger ikke å vente til konsernintern fakturabehandling er fullført.
5. Konserninterne kundefakturaer opprettes regelmessig i utlånsfirmaet. Fakturaene opprettes manuelt eller ved hjelp av en periodisk automatisert prosess. Én enkelt faktura kan opprettes for hver juridiske enhet som låner, eller separate fakturaer kan opprettes etter prosjekt.
6. Når den konserninterne kundefakturaen blir postert i den juridiske enheten som låner ut, opprettes den tilsvarende ventende leverandørfakturaen i den juridiske enheten som låner. Kostnadene i den ventende leverandørfakturaen blir registrert i prosjektets underfinans når fakturaen er postert.

Følgende diagram illustrerer konsernintern fakturering som det relaterer til regnskapshendelser og forventede posteringer til økonomimodulen.

![Konsernintern flyt.](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>Ytterligere ressurser

- [Konfigurer konsernintern fakturering](configure-intercompany-invoicing.md)
- [Registrere konserninterne transaksjoner](create-intercompany-transactions.md)
- [Opprette konserninterne kunde- og leverandørfakturaer](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]