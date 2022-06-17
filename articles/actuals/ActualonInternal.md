---
title: Faktiske verdier virker inn på et internt prosjekt
description: Denne artikkelen inneholder informasjon om hva som skjer med tabellen Faktiske verdier ved ulike hendelser for et internt prosjekt i Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: de05714c079fe121ef68e28b1acb82c24bce095e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921360"
---
# <a name="actuals-impact-for-an-internal-project"></a>Faktiske verdier virker inn på et internt prosjekt

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Tabellen nedenfor viser de faktiske verdiene for ulike transaksjonstyper som opprettes for ulike hendelser i et internt prosjektengasjement.

| Seminar/konferanse | Faktisk kostnad | Eksempel |
|---|---|---|
| Klokkeslettet opprettes. | Ikke aktuelt | <p>Bob Kozack fra den amerikanske organisasjonsenheten Fabrikam, som har en kostnadssats på 100 amerikanske dollar (USD 100) per time, arbeider med et prosjekt med navnet "Arm Installation at Adatum". Dette prosjektet tilordnes en faktureringsmetode med fast pris på kontraktlinjen. Her er et eksempel på tidsoppføring fra Bob Kozak:</p><p>Bob Kozack - 8 timer</p> |
| Tiden sendes inn. | Ikke aktuelt | Det opprettes en kostnadsjournallinje for tidsoppføringen. Standard kostnadssats angis i journaloppføringen. |
| Tidsoppføringen hentes tilbake før den blir godkjent. | Ikke aktuelt | |
| Tiden er godkjent. | Det opprettes en faktisk kostnad. | <p>Ny faktisk verdi som opprettes:</p><ul><li>**Faktisk kostnad:** Bob Kozack, 8 timer, USD 800</li></ul> |
| Godkjenningen av klokkeslettet blir annullert. | <p>Justeringsstatusen for faktisk opprinnelig kostnad oppdateres til **Justert**.</p><p>Det opprettes en faktisk tilbakeføringskostnad som har justeringsstatusen **Kan ikke justeres**.</p> | <p>Eksisterende faktisk verdi som oppdateres:</p><ul><li>**Faktisk kostnad:** Bob Kozack, 8 timer, USD 800, *Justert*</li></ul><p>Ny faktisk verdi som opprettes for å reversere den tidligere økonomiske innvirkningen:</p><ul><li>**Faktisk kostnad:** Bob Kozack, (8 timer), (USD 800), *Kan ikke justeres*</li></ul> |
| Tidsoppføringen hentes tilbake etter at den er godkjent. | <p>Justeringsstatusen for faktisk opprinnelig kostnad oppdateres til **Justert**.</p><p>Det opprettes en faktisk tilbakeføringskostnad som har justeringsstatusen **Kan ikke justeres**.</p> | <p>Eksisterende faktisk verdi som oppdateres:</p><ul><li>**Faktisk kostnad:** Bob Kozack, 8 timer, USD 800, *Justert*</li></ul><p>Ny faktisk verdi som opprettes for å reversere den tidligere økonomiske innvirkningen:</p><ul><li>**Faktisk kostnad:** Bob Kozack, (8 timer), (USD 800), *Kan ikke justeres*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
