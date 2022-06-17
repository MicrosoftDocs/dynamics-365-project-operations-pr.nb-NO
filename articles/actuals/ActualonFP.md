---
title: Faktiske verdier virker inn på et engasjement med fast pris
description: Denne artikkelen inneholder informasjon om hva som skjer med tabellen Faktiske verdier ved ulike hendelser i løpet av livssyklusen til en avtale med fast pris i Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 50819d77d56935bfe5438d7d9dae99562bcc0b49
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918140"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Faktiske verdier virker inn på et engasjement med fast pris

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Tabellen nedenfor viser de faktiske verdiene for ulike transaksjonstyper som opprettes for ulike hendelser i et engasjement med fast pris.

| Seminar/konferanse | Faktisk kostnad | Ufakturert faktisk salg | Fakturert faktisk salg | Eksempel |
|---|---|---|---|---|
| Klokkeslettet opprettes. | Ikke aktuelt | Ikke aktuelt | Ikke aktuelt | <p>Bob Kozack fra den amerikanske organisasjonsenheten Fabrikam, som har en kostnadssats på 100 amerikanske dollar (USD 100) per time, arbeider med et prosjekt med navnet "Arm Installation at Adatum". Dette prosjektet tilordnes en faktureringsmetode med fast pris på kontraktlinjen. Her er et eksempel på tidsoppføring fra Bob Kozak:</p><p>Bob Kozack - 8 timer</p> |
| Tiden sendes inn. | Ikke aktuelt | Ikke aktuelt | Ikke aktuelt | Det opprettes en kostnadsjournallinje for tidsoppføringen. Standard kostnadssats angis i journaloppføringen. |
| Tidsoppføringen hentes tilbake før den blir godkjent. | Ikke aktuelt | Ikke aktuelt | Ikke aktuelt | |
| Tiden er godkjent. | Det opprettes en faktisk kostnad. | Ikke aktuelt | Ikke aktuelt | <p>Ny faktisk verdi som opprettes:</p><ul><li>**Faktisk kostnad:** Bob Kozack, 8 timer, USD 800</li></ul> |
| Tidsgodkjenningen blir annullert. | <p>Justeringsstatusen for faktisk opprinnelig kostnad oppdateres til **Justert**.</p><p>Det opprettes en faktisk tilbakeføringskostnad som har justeringsstatusen **Kan ikke justeres**.</p> | Ikke aktuelt | Ikke aktuelt | <p>Eksisterende faktisk verdi som oppdateres:</p><ul><li>**Faktisk kostnad:** Bob Kozack, 8 timer, USD 800, *Justert*</li></ul><p>Ny faktisk verdi som opprettes for å reversere den tidligere økonomiske innvirkningen:</p><ul><li>**Faktisk kostnad:** Bob Kozack, (8 timer), (USD 800), *Kan ikke justeres*</li></ul> |
| Tidsoppføringen hentes tilbake etter at den er godkjent. | <p>Justeringsstatusen for faktisk opprinnelig kostnad oppdateres til **Justert**.</p><p>Det opprettes en faktisk tilbakeføringskostnad som har justeringsstatusen **Kan ikke justeres**.</p> | Ikke aktuelt | Ikke aktuelt | <p>Eksisterende faktisk verdi som oppdateres:</p><ul><li>**Faktisk kostnad:** Bob Kozack, 8 timer, USD 800, *Justert*</li></ul><p>Ny faktisk verdi som opprettes for å reversere den tidligere økonomiske innvirkningen:</p><ul><li>**Faktisk kostnad:** Bob Kozack, (8 timer), (USD 800), *Kan ikke justeres*</li></ul> |
| Kontrakten er bekreftet. | <p>Justeringsstatusen for de gamle opprinnelige kostnadene oppdateres til **Justert**.</p><p>Tilbakeføring av faktiske kostnader opprettes som har justeringsstatusen **Kan ikke justeres**.</p><p>Nye faktiske kostnader opprettes etter at kontraktsreglene er evaluert på nytt.</p> | Ikke aktuelt | Ikke aktuelt | <p>Eksisterende faktisk verdi som oppdateres:</p><ul><li>**Faktisk kostnad:** Bob Kozack, 8 timer, USD 800, *Justert*</li></ul><p>Ny faktisk verdi som opprettes for å reversere den tidligere økonomiske innvirkningen:</p><ul><li>**Faktisk kostnad:** Bob Kozack, (8 timer), (USD 800), *Kan ikke justeres*</li></ul><p>Ny faktisk verdi som opprettes for den reevaluerte økonomiske innvirkningen:</p><ul><li>**Faktisk kostnad:** Bob Kozack, 8 timer, USD 800</li></ul> |
| En faktura opprettes. | Ikke aktuelt | Ikke aktuelt | Ikke aktuelt | |
| Fakturaen bekreftes med en milepæl. | Ikke aktuelt | Ikke aktuelt | Nye milepælbaserte faktiske salg som er fakturert, opprettes. | <p>Eksisterende faktiske verdier som forblir uendret:</p><ul><li>**Faktisk kostnad:** Bob Kozack, 8 timer, USD 800</li></ul><p>Ny faktisk verdi som opprettes for å registrere de fakturerte salgsverdiene:</p><ul><li>**Fakturert faktisk salg:** Milepæl, USD 5000</li></ul> |
| Fakturaen er korrigert for å kreditere milepælen. | Ikke aktuelt | Ikke aktuelt | Faktiske beløp for tilbakeføring av fakturert salg opprettes. | <p>Eksisterende faktiske verdier som forblir uendret:</p><ul><li>**Faktisk kostnad:** Bob Kozack, 8 timer, 800 USD</li></ul><p>Eksisterende faktisk verdi som oppdateres:</p><ul><li>**Fakturert faktisk salg:** Milepæl, USD 5000 *Justert*</li></ul><p>Ny faktisk verdi som opprettes for å reversere de tidligere fakturerte salgsverdiene:</p><ul><li>**Fakturert faktisk salg:** Milepæl, (USD 5000), *Kan ikke justeres*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
