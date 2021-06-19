---
title: Hva er nytt eller endret i Project Service Automation Update Release 21, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 21, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: dd894f27baac70238d0bd9e9b1a21a9a499e1ea7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002339"
---
# <a name="project-service-automation-update-release-21-v3"></a>Project Service Automation, Update Release 21, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Denne versjonen er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for Project Service Automation V3, Update Release 21. Denne versjonen har et build-nummer på V 3.10.32.50 og er generelt tilgjengelig via en egen oppdatering i juni 2020.

## <a name="update-release-21"></a>Update Release 21

### <a name="bug-fixes"></a>Feilrettinger

**Tid og utgift**

Følgende problemer har blitt løst:

- Når du bruker **Rutenett for tidsoppføring**-kontrollen på instrumentbordet, bruker ikke rutenettet full bredde på beholderen i instrumentbordrutenettet.
- Når det gjelder spesifikke tidssoner, viser ikke **Tidsoppføring**-rutenettkontrollen visningsoppføringer.
- Tidsoppføringer som er etter 9:00 PM, vises på feil dag.
- Brukere kan ikke sende utgifter hvis utgiftskategorien for **utgiftskvittering kreves** ikke har noen verdi.

**Ressursbehandling**

Følgende problemer har blitt løst:

- Inaktive bestillinger vises i **Avstemming**-visningen.
- Generell ressursfullføring mangler validering for å sikre at det finnes en gyldig bestillingsstatus.

**Prosjektledelse**

Følgende problemer har blitt løst:

- **Prosjekt**-skjemarutenettene (**Ressurstilordning**, **Oppgave**, **Avstemming**-visning, **Utgiftsestimater**) forblir redigerbare selv når et prosjekt ikke er aktivt.
- Dupliserte kunder kan ikke flettes med kunder som er koblet til bekreftede prosjektkontrakter.
- Når en ressurs som ikke har en gyldig kalender, blir lagt til, returnerer ikke systemet en brukervennlig feilmelding.
- Knappen **Legg til oppgave** i oppgaverutenettet er aktivert når prosjektet er koblet til **Microsoft Project-tillegget**.
- Innsatsen vokser ukontrollerbart når en oppgave med en kategori tilordnes en ressurs med en rolle som det er definert en kostnadspris for.

**Sales**

Følgende forbedringer er gjort:

- **Fakturafrekvens** og **Startdato for fakturering** er flyttet til kategorien **Fakturaplan**.

Følgende problemer har blitt løst:

- **Total salgspris** er null (0) for **Kategori** selv om **Rolle** har en total salgspris som ikke er null.
- Kunder kan ikke endre verdien i **Fakturastatus**-feltet til **Klar for fakturering** når en annen tilpasset prosess oppdaterer et ekstra felt.
- Knappen for **oppdatering av fakturalinjer** kan opprette flere dupliserte linjer hvis den velges gjentatte ganger.
- Knappen **Oppdater priser** fungerer ikke i delrutenettet **Rollepriser** i skjemaet **Hurtigvisning**.
- **Salgsprislisteoppløsning**-logikken håndterer tidssoner på feil måte, noe som resulterer i feil valg av prislister.
- En prosjekts **Total faktisk kostnad** kan avvike med en brøkdel når én enkelt tidsoppføring er godkjent.
- Logikken for **prisløsning** gir ikke en brukervennlig feilmelding hvis **innhentet rollepris** ikke har verdier i feltene **Primærenhet** og **Pris i primærenhet**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]