---
title: Hva er nytt eller endret i Project Service Automation Update Release 15, V3
description: Dette emnet inneholder informasjon om hva som er nytt i Project Service Automation Update Release 15, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 26b9ee0a6ff1ad81d6c77a6a7091733667c493ff
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585160"
---
# <a name="project-service-automation-update-release-15-v3"></a>Project Service Automation, Update Release 15, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for å annonsere den nyeste oppdateringen av Dynamics 365 Project Service Automation (PSA)-programmet. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Denne versjonen er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for PSA V3, Update Release 15. Denne versjonen har buildnummer V3.10.5.28 og er vanligvis tilgjengelig via en egen oppdatering i januar 2020.

## <a name="update-release-15"></a>Update Release 15 

### <a name="enhancements"></a>Forbedringer

- Prosjektledelse

### <a name="bug-fixes"></a>Feilrettinger

- Tid og utgift

  - Fikset: Legg til feilbehandling ved innlasting i avstemmingsvisningen.
  - Fikset: Prosjektressurshub: Endre navn på **Beløp** for å redusere tvetydighet.
  - Fikset: Juster visningen **Kopier tidsoppføringskolonner** for å inkluderer typen.
  - Fikset: Redigering av tidsoppføringsvarighet i rutenettvisningen ved hjelp av desimaltall resulterer i en ukjent feil for noen tall.

- Prosjektledelse

  - Fikset: Rullegardinmenyen for **Bruk i sporingsvisning** utvides nå basert på bredden på alternativene.
  - Fikset: Ved administrasjon av prosjekter i +13-tidssonen kan oppgaveberegninger vise unøyaktige resultater.
  - Fikset: **Sluttid for teammedlemmer** er rettet opp ved bruk av 24-timers kalender.
  - Fikset: Reaktiverte **BPF** i **msdyn_project**-hovedskjemaet.
  - Fikset: Tildelingsberegning ignorerer ikke lenger én dag.
  - Fikset: Et nytt varslingsbanner er lagt til i prosjektskjemaet når tidssonen er forskjellig mellom brukeren og prosjektet.

- Sales

  - Fikset: Oppslagsvisning for utgiftsestimat kan brukes til å filtrere duplikater.
  - Fikset: Kode i **PluginDomain.ExecuteInTryCatchBlock(..)** skjuler ikke lenger opprinnelsen til unntaket.
  - Fikset: Feilmelding vises ikke lenger i **Prosjektoppslag** i skjemaet **Tilbudslinje** når det er mer enn 1000 prosjekter.
  - Fikset: **Estimater**-rutenett for arbeidsberegninger og utgiftsoverslag viser nå riktig valutasymbol.
  - Fikset: Når en organisasjon oppdaterer PSA fra Update Release 14 til Update Release 15, vises ikke lenger kategorien **Planlegg** som tom i skjemaet **Prosjekt**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
