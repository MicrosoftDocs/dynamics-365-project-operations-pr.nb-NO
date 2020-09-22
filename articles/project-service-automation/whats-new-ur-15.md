---
title: Hva er nytt i Project Service Automation Update Release 15, V3
description: Dette emnet inneholder informasjon om hva som er nytt i Project Service Automation Update Release 15, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: 75117934-8042-448b-91dc-b43f1f677e4f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 68e0faa4c1afdb0d1520388253671330f9b7d334
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754113"
---
# <a name="project-service-automation-v3-update-release-15"></a>Project Service Automation V3, Update Release 15

Vi er glade for å annonsere den nyeste oppdateringen av Dynamics 365 Project Service Automation (PSA)-programmet. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Denne versjonen er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

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
