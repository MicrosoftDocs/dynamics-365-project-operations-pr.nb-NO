---
title: Godkjenningssett
description: Dette emnet forklarer hvordan du arbeider med godkjenningssett, forespørsler og delsettene for disse operasjonene.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 6809e01d8c3c93841125d0100d898dc208577019
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576236"
---
# <a name="approval-sets"></a>Godkjenningssett

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Godkjenningssett grupperer godkjenningsforespørsler sammen i mindre delsett av operasjoner. Denne grupperingen tillater at godkjenninger kan behandles etter prosjekt i en bestemt rekkefølge, og gjør det mulig å prøve på nytt og å sekvensere. Gruppering av godkjenningsforespørslene sammen forbedrer påliteligheten og sporbarheten ved godkjenningsbehandling for store godkjenningsvolumer.

Godkjenningssett angir den totale behandlingstilstanden for de relaterte oppføringene. Når en godkjenningsoppføring behandles ved hjelp av et godkjenningssett, flyttes oppføringen fra **Sendt** til **Godkjent**, og den er ikke lenger koblet til godkjenningssettet. Hvis en oppføring mislykkes når den sendes til godkjenning, beholdes statusen **Sendt**, og godkjenningssettet merkes som mislykket. Godkjenningssettet logger feilmeldingen om feilen.

## <a name="processing-approvals-and-approval-sets"></a>Behandle godkjenninger og godkjenningssett
Godkjenninger som ligger i kø for behandling, vises i visningen **Godkjenninger under behandling**. Systemet behandler alle oppføringene flere ganger asynkront, inkludert å prøve en godkjenning på nytt hvis tidligere forsøk mislyktes.

Feltet for **godkjenningssett for levetid** registrerer antall forsøk som gjenstår for å behandle settet før det er merket som mislykket.

Godkjenningssett behandles gjennom den periodiske aktiveringen basert på en **skyflyt** kalt for **Project Service – Planlegg prosjektgodkjenningssett til gjentakelse**. Du finner dette i **løsningen** kalt for **Project Operations**. 

Kontroller at flyten aktiveres ved å utføre trinnene nedenfor.

1. Logg på som administrator på [flow.microsoft.com](https://powerautomate.microsoft.com).
2. Bytt til miljøet du bruker for Dynamics 365 Project Operations, i øvre høyre hjørne.
3. Velg **Løsninger** for å vise løsningene som er installert i miljøet.
4. Velg **Project Operations** i løsningslisten.
5. Endre filteret fra **Alle** til **Skyflyter**.
6. Kontroller at flyten **Project Service – Planlegg prosjektgodkjenningssett til gjentakelse** er satt til **På**. Hvis den ikke er det, velger du flyten og velger deretter **Aktiver**.
7. Kontroller at behandlingen utføres hvert femte minutt ved å se gjennom listen **Systemjobber** i **Innstillinger**-området i Project Operations Dataverse-miljøet.

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
