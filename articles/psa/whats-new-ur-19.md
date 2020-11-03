---
title: Hva er nytt eller endret i Project Service Automation Update Release 19, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 19, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: ecc923cccfad21985025ab9d8006aaff16afc25f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081573"
---
# <a name="project-service-automation-update-release-19-v3"></a>Project Service Automation, Update Release 19, V3

Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Denne versjonen er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for PSA V3, Update Release 19. Denne versjonen har et build-nummer på V3.10.30.41 og er generelt tilgjengelig via en egen oppdatering i mai 2020.

## <a name="update-release-19"></a>Update Release 19

### <a name="bug-fixes"></a>Feilrettinger

**Tid og utgift**

Følgende problemer har blitt løst: 

- Feil avledet av import av tidsoppføringer som ikke vises riktig.
- Timeregistreringsrutenettet støtter ikke **Bare dato** -feltvirkemåte.
- Prosjektressurser kan ikke opprette en utgift med et prosjekt.

**Prosjektledelse**

Følgende problemer har blitt løst: 

-  Oppgaver to nivåer lengre ned forårsaker feil beregning av arbeidstid ved fullføring (EAC).

**Sales**

Følgende problemer har blitt løst: 

- Handlingen **Beregn på nytt** virker ikke med detaljer for utgiftkontraktlinje eller tilbudslinjedetaljer.
- **Oppdater priser** mangler for utgiftsestimater.
-  Kunder kan ikke velge egendefinerte kontraktstatusårsaker fra **Prosjektkontrakt** -siden.
- Kunder opplever redusert ytelse ved oppretting av en egendefinert prisliste fra et tilbud.
- Kunder opplever inkonsekvens med **enhet** -standarder på **Tilbudslinjedetaljer** - og **Kontraktlinjedetaljer** -sidene.
- Hvis du legger til kategorivarer i ikke-belastbare transaksjoner på en belastbar kontraktlinje, respekterer den ikke **Ikke-belastbar** -faktureringstype for transaksjonskategorien.
- Kunder kan ikke bruke de nylig tillagte rollene og kategoriene i tidligere opprettede kontrakter.
- Kunder opplever redusert ytelse, henter unødvendig inn PreValidateProjectTeamMemberUpdate.cs
- Roller som ikke er belastbare i **Ressurskategorier** -listen, må legges til i **Belastbare roller** -fanen som **Ikke-belastbare** på kontraktlinjen for et prosjekt.
- Kunder kan oppleve redusert ytelse ved oppretting av et prosjekt fordi **GetBookableResourceIdFromUser** henter alle kolonner med ressurser som kan reserveres, i stedet for bare primær-ID-en.
- **TransactionType** -enheten mangler plugin-modulen for oppdatering av forhåndsvalidering for å hindre brukere i å skrive inn **Enheter** og **UnitGroups** som ikke er gyldige for transaksjonstyper.
- **Fjern** -trinnet fungerer ikke for import av tidsoppføringer.