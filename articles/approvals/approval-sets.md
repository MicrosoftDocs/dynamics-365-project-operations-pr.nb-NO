---
title: Godkjenningssett
description: Dette emnet forklarer hvordan du arbeider med godkjenningssett, forespørsler og delsettene for disse operasjonene.
author: stsporen
manager: tfehr
ms.date: 08/10/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 1d9333033eb2b03966c6531d0fd6ad5b878acd93
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323248"
---
# <a name="approval-sets"></a>Godkjenningssett

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Godkjenningssett grupperer godkjenningsforespørsler sammen i mindre delsett av operasjoner. Denne grupperingen tillater at godkjenninger kan behandles etter prosjekt i en bestemt rekkefølge, og gjør det mulig å prøve på nytt og å sekvensere. Gruppering av godkjenningsforespørslene sammen forbedrer påliteligheten og sporbarheten ved godkjenningsbehandling for store godkjenningsvolumer.

Godkjenningssett angir den totale behandlingstilstanden for de relaterte oppføringene. Når en godkjenningsoppføring behandles ved hjelp av et godkjenningssett, flyttes oppføringen fra **Sendt** til **Godkjent**, og den er ikke lenger koblet til godkjenningssettet. Hvis en oppføring mislykkes når den sendes til godkjenning, beholdes statusen **Sendt**, og godkjenningssettet merkes som mislykket. Godkjenningssettet logger feilmeldingen om feilen.

## <a name="processing-approvals-and-approval-sets"></a>Behandle godkjenninger og godkjenningssett
Godkjenninger som ligger i kø for behandling, vises i visningen **Godkjenninger under behandling**. Systemet behandler alle oppføringene flere ganger asynkront, inkludert å prøve en godkjenning på nytt hvis tidligere forsøk mislyktes.

Feltet for **godkjenningssett for levetid** registrerer antall forsøk som gjenstår for å behandle settet før det er merket som mislykket.

## <a name="failed-approvals-and-approval-sets"></a>Mislykkede godkjenninger og godkjenningssett
Visningen **Mislykkede godkjenninger** viser alle godkjenninger som krever brukerinngripen. Åpne de tilknyttede godkjenningssettloggene for å identifisere årsaken til feilen.
Når du velger **Prøv på nytt**, legges levetidsantallet til, og godkjenningssettet flyttes tilbake til statusen **Behandling** og prøver å behandle de gjenstående oppføringene.

## <a name="configure-approval-sets"></a>Konfigurere godkjenningssett

### <a name="enable-the-approval-sets-feature"></a>Aktiver funksjonen Godkjenningssett
Før du aktiverer funksjonen Godkjenningssett, kontrollerer du at det ikke er noen godkjenninger som blir behandlet.

- Gå til siden **Prosjektparametere**, og velg **Funksjonskontroll** > **Aktiver moderne godkjenninger**.

### <a name="turn-off-the-approval-sets-feature"></a>Deaktiver funksjonen Godkjenningssett
Før du deaktiverer funksjonen Godkjenningssett, kontrollerer du at det ikke er noen godkjenninger som blir behandlet.

- Gå til siden **Prosjektparametere**, og velg **Funksjonskontroll** > **Deaktiver moderne godkjenninger**.

### <a name="configuring-the-asynchronous-threshold"></a>Konfigurere den asynkrone terskelen 
Når det opprettes godkjenningssett, flyttes behandlingen til bakgrunnen når det valgte antallet oppføringer til godkjenning overskrider det angitte terskelen. Bruk feltet **Asynkron terskel** for å konfigurere når godkjenningsbehandling skal kjøres synkront eller asynkront. Velg en av følgende verdier:

  - Null: Alle forespørsler må behandles asynkront. 
  - Tall som er større enn null: Godkjenninger behandles asynkront bare når det sendte antallet godkjenninger overskrider denne verdien.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
