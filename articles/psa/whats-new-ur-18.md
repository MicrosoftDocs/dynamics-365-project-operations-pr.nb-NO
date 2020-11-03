---
title: Hva er nytt eller endret i Project Service Automation Update Release 18, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 18, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: 1d7ea200531dd24d56a829f879e3a2532a9b38dc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081574"
---
# <a name="project-service-automation-update-release-18-v3"></a>Project Service Automation, Update Release 18, V3

Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Denne versjonen er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for Project Service Automation V3, Update Release 18. Denne versjonen har et build-nummer på V3.10.8.12 og er generelt tilgjengelig via en egen oppdatering i april 2020.

## <a name="update-release-18"></a>Update Release 18

### <a name="bug-fixes"></a>Feilrettinger

**Tid og utgift**

- Løst: Flytene **Tilbake** , **Forespørsel** og **Avbryt godkjenning** bruker unntak med uklare feilmeldinger.
- Løst: Når **Avbryt godkjenning** mislykkes for en utgift, brukes det ikke en relevant unntaksfeil.
- Løst: Rutenettet Tidsoppføring håndterer feilaktig ikke-arbeidsdager i Australia etter bytte til sommertid (DST) i oktober.
- Løst: Feil standardlogikk forhindrer sending av utgifter.
- Løst: Når tidsoppføringsgodkjenning mislykkes, beholdes godkjenningen i tilstanden **Ventende**.
- Løst: SQL-feil ved massegodkjenninger (vranglås/tidsavbrudd).
- Løst: Betydelige ytelsesproblemer i brukeropplevelsen forårsaket av oppdatering av teammedlemmer under godkjenning av tidsoppføringer.

**Prosjektledelse**

- Løst: Tidssonevarsel flyttet fra **Avstemming** -visningen til **Prosjekt** -hovedskjemaet.
- Løst: Kalendermalen brukes ikke som standard når et nytt prosjektskjema åpnes.
- Løst: For Chromium-baserte nettlesere kan ikke brukere enkelt velge foregående oppgaver de vil slette.
- Løst: Oppretting eller kopiering av **Prosjekt fra tom mal** henter urelaterte tilordninger.
- Løst: I bestemte kanttilfeller fører oppretting av en ny oppgave fra oppgaverutenettet at dupliserte oppføringer blir opprettet.
- Løst: I manuell modus kan ikke brukere oppdatere oppgavestartdatoer til senere enn gjeldende dato lagret.

**Ressursbehandling**

- Løst: **Avstemming** -visningens rad for delsum beregner feilaktig bestillingsavvik etter at bestillinger er utvidet.
- Løst: **Avstemming** -visningen viser feilaktig ressurstilordninger når ressursen som kan bestilles, har en kalender som ikke samsvarer med prosjektkalenderen.

**Sales**

- Løst: Når tidsoppføringer godkjennes på nytt ( **Godkjenn > Avbryt >** godkjenn på nytt), blir det opprettet en duplikat faktisk ikke-belastbar.
