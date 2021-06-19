---
title: Godkjenningssett
description: Dette emnet inneholder informasjon om godkjenningssett, forespørsler og delsettene for disse operasjonene.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116883"
---
# <a name="approval-sets"></a>Godkjenningssett

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Godkjenningssett grupperer godkjenningsforespørsler sammen i mindre delsett av operasjoner. Denne grupperingen tillater at godkjenninger kan behandles i prosjektrekkefølge og tillater nytt forsøk og sekvensering. Gruppering forbedrer påliteligheten og sporbarheten ved godkjenningsbehandling for store godkjenningsvolumer.

Godkjenningssett angir den totale behandlingstilstanden for de relaterte oppføringene. Når en godkjenningsoppføring behandles ved hjelp av et godkjenningssett, flyttes oppføringen fra **Sendt** til **Godkjent**, og koblingen fra godkjenningssettet oppheves. Hvis en oppføring mislykkes når den sendes til godkjenning, beholdes statusen **Sendt**, og godkjenningssettet merkes som mislykket. Godkjenningssettet logger feilmeldingen om feilen.

## <a name="processing-approvals-and-approval-sets"></a>Behandle godkjenninger og godkjenningssett
Godkjenninger som ligger i kø for behandling, vises i visningen **Godkjenninger under behandling**. Systemet prøver å behandle alle oppføringene flere ganger asynkront, inkludert å prøve en godkjenning på nytt hvis tidligere forsøk mislyktes.

Feltet for **godkjenningssett for levetid** registrerer antall forsøk som gjenstår for å behandle settet før det er merket som mislykket.

## <a name="failed-approvals-and-approval-sets"></a>Mislykkede godkjenninger og godkjenningssett
Visningen **Mislykkede godkjenninger** viser alle godkjenninger som krever brukerinngripen. Åpne de tilknyttede godkjenningssettloggene for å identifisere årsaken til feilen.
Når du velger **Prøv på nytt**, legges levetidsantallet til, og godkjenningssettet flyttes tilbake til statusen **Behandling** og prøver å behandle de gjenstående oppføringene.

## <a name="configure-approval-sets"></a>Konfigurere godkjenningssett

###  <a name="enable-the-approval-sets-feature"></a>Aktiver funksjonen Godkjenningssett
Før du aktiverer funksjonen Godkjenningssett, kontrollerer du at det ikke er noen godkjenninger som blir behandlet.

- Gå til siden **Prosjektparametere**, og velg **Funksjonskontroll** > **Aktiver moderne godkjenninger**.

### <a name="turn-off-the-approval-sets-feature"></a>Deaktiver funksjonen Godkjenningssett
Før du deaktiverer funksjonen Godkjenningssett, kontrollerer du at det ikke er noen godkjenninger som blir behandlet.

- Gå til siden **Prosjektparametere**, og velg **Funksjonskontroll** > **Deaktiver moderne godkjenninger**.

### <a name="configuring-the-asynchronous-threshold"></a>Konfigurere den asynkrone terskelen 
Når det opprettes godkjenningssett, flyttes behandlingen til bakgrunnen når det valgte antallet oppføringer til godkjenning overskrider det angitte terskelen. Bruk feltet **Asynkron terskel** for å konfigurere når godkjenningsbehandling skal kjøres synkront eller asynkront.
Gyldige verdier er:

  - Null: Alle forespørsler må behandles asynkront. 
  - Tall som er større enn null: Godkjenninger behandles asynkront bare når det sendte antallet godkjenninger overskrider denne verdien.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
