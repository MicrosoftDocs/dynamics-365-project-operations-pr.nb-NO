---
title: Faktiske verdier virker inn i løpet av førsalgsfasen av et engasjement
description: Dette emnet inneholder informasjon om hva som skjer med tabellen Faktiske verdier mens et engasjement er i førsalgsfasen i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ad62639b345d5519b103d4bde3fbb033b9a7a519
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577248"
---
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>Faktiske verdier virker inn i løpet av førsalgsfasen av et engasjement

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Tabellen nedenfor viser de faktiske verdiene for ulike transaksjonstyper som opprettes for ulike hendelser under førsalgsfasen i et prosjektengasjement.

| Seminar/konferanse | Faktisk kostnad | Eksempel |
|---|---|---|
| Klokkeslettet opprettes. | Ikke aktuelt | <p>Bob Kozack fra den amerikanske organisasjonsenheten Fabrikam, som har en kostnadssats på 100 amerikanske dollar (USD 100) per time, arbeider med et prosjekt med navnet "Arm Installation at Adatum". Dette prosjektet tilordnes en faktureringsmetode med fast pris på kontraktlinjen. Her er et eksempel på tidsoppføring fra Bob Kozak:</p><p>Bob Kozack - 8 timer</p> |
| Tiden sendes inn. | Ikke aktuelt | Det opprettes en kostnadsjournallinje for tidsoppføringen. Standard kostnadssats angis i journaloppføringen. |
| Tidsoppføringen hentes tilbake før den blir godkjent. | Ikke aktuelt | |
| Tiden er godkjent. | Det opprettes en faktisk kostnad. | <p>Ny faktisk verdi som opprettes:</p><ul><li>**Faktisk kostnad:** Bob Kozack, 8 timer, USD 800</li></ul> |
| Tidsgodkjenningen blir annullert. | <p>Justeringsstatusen for faktisk opprinnelig kostnad oppdateres til **Justert**.</p><p>Det opprettes en faktisk tilbakeføringskostnad som har justeringsstatusen **Kan ikke justeres**.</p> | <p>Eksisterende faktisk verdi som oppdateres:</p><ul><li>**Faktisk kostnad:** Bob Kozack, 8 timer, USD 800, *Justert*</li></ul><p>Ny faktisk verdi som opprettes for å reversere den tidligere økonomiske innvirkningen:</p><ul><li>**Faktisk kostnad:** Bob Kozack, (8 timer), (USD 800), *Kan ikke justeres*</li></ul> |
| Tidsoppføringen hentes tilbake etter at den er godkjent. | <p>Justeringsstatusen for faktisk opprinnelig kostnad oppdateres til **Justert**.</p><p>Det opprettes en faktisk tilbakeføringskostnad som har justeringsstatusen **Kan ikke justeres**.</p> | <p>Eksisterende faktisk verdi som oppdateres:</p><ul><li>**Faktisk kostnad:** Bob Kozack, 8 timer, USD 800, *Justert*</li></ul><p>Ny faktisk verdi som opprettes for å reversere den tidligere økonomiske innvirkningen:</p><ul><li>**Faktisk kostnad:** Bob Kozack, (8 timer), (USD 800), *Kan ikke justeres*</li></ul> |
| Tilbudet blir vunnet, og det opprettes en kontrakt. | <p>Justeringsstatusen for de gamle opprinnelige kostnadene oppdateres til **Justert**.</p><p>Tilbakeføring av faktiske kostnader opprettes som har justeringsstatusen **Kan ikke justeres**.</p><p>Nye faktiske kostnader opprettes etter at kontraktsreglene er evaluert på nytt.</p> | <p>Eksisterende faktisk verdi som oppdateres:</p><ul><li>**Faktisk kostnad:** Bob Kozack, 8 timer, USD 800, *Justert*</li></ul><p>Ny faktisk verdi som opprettes for å reversere den tidligere økonomiske innvirkningen:</p><ul><li>**Faktisk kostnad:** Bob Kozack, (8 timer), (USD 800), *Kan ikke justeres*</li></ul><p>Nye faktiske verdier som opprettes for den reevaluerte økonomiske innvirkningen når tilbudet blir vunnet og kontrakten opprettes:</p><ul><li>**Faktisk kostnad:** Bob Kozack, 8 timer, USD 800</li><li>**Ufakturert faktisk salg:** Bob Kozack, 8 timer, USD 1600</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
