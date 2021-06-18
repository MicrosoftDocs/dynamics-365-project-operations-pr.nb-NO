---
title: Hva er nytt eller endret i Project Service Automation Update Release 25, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 25, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 92dd74378457cf877e8ec26eb85a7883dda97d51
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000223"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Hva er nytt eller endret i Project Service Automation Update Release 25, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Denne versjonen er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Dette emnet viser funksjonene og reparasjonene som er nye eller endret for Project Service Automation V3, Update Release 25. Denne versjonen har et buildnummer V 3.10.43.76 og er allment tilgjengelig via en egen oppdatering i oktober 2020.

## <a name="update-release-25"></a>Update Release 25

### <a name="bug-fixes"></a>Feilrettinger

**Tid og utgift**

Følgende problem er løst:

- Tidsregistreringsdiagrammet viser ytterligere data basert på for stor intervall som hentes.

**Ressursbehandling**

Følgende problem er løst:

- Lagt til Package Deployer for å hoppe over Universal Resource Scheduling-oppdateringsimporten hvis det allerede finnes en oppdatering med høyere versjon.

**Prosjektledelse**

Følgende problemer har blitt løst:

- Korrigerte avrundings- og valutakursavvik som fører til feil planlagt kostnad i prosjektsporingsrutenettet.
- Støtter muligheten til å vise to eller flere reaksjonsrutenett i **Prosjekt**-skjemaet.
- Gitt validering for å gi mulighet til å tilordne en aktivitet etter sluttdatoen for kalenderen, noe som fører til en mislykket ressurstilordning.
- Forbedret feilhåndtering for å løse nullreferanseunntak som genereres fra følgende:

    - Plugin-modul **PreValidateProjectTeamMemberCreate**
    - **PreValidateProjectTaskCreate** når en prosjektoppgave opprettes uten et tilknyttet prosjekt
    - Plugin-modul **PreProjectTeamMemberCreate**
    - Plugin-modul **PostProjectTeamMemberDelete**
    - Plugin-modul **PreValidateProjectTaskDelete**

**Sales**

Følgende problemer har blitt løst:

- Forbedret feilbehandling for å løse nullreferanseunntak generert fra **Kopier prosjekt: estimering av administrasjon av hjelperessurser**.
- **Ikke klar til fakturering** på en **Faktureringsrestanse for Tid og materiale** fjerner ikke faktureringsstatus.
- Korrigerte **Pris**-knapper med feiletikett i kategorien **Rollepris** og **Katalogelementer**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]