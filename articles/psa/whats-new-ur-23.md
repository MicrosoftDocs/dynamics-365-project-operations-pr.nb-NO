---
title: Hva er nytt eller endret i Project Service Automation Update Release 23, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 23, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: ec27d2344f14e61a50be2771ee3d7952f16abd736927de7c3c5a019351a3e067
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996628"
---
# <a name="project-service-automation-update-release-23-v3"></a>Project Service Automation, Update Release 23, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Denne versjonen er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for Project Service Automation V3, Update Release 23. Denne versjonen har buildnummer V3.10.34.30 og er generelt tilgjengelig via en egen oppdatering i august 2020.

## <a name="update-release-23"></a>Update Release 23

### <a name="bug-fixes"></a>Feilrettinger

**Tid og utgift**

Følgende problemer har blitt løst:
- Håndtering av kantsak i **Slett prosjektteammedlem** for å gi et meningsfullt unntak.
- Import av tilordning fører til et tomt fjerningsskjermbilde.

**Ressursbehandling**

Følgende problemer har blitt løst:

- **Rutenettet for ressursutnyttelse** viser feil data når tidsskalane er mer enn fem dager.
- Når kunder oppretter en ressurs som kan reserverer, kan ikke plugin-modulen automatisk legge til ressursen i en Microsoft Office 365-gruppe.
- **Avstemming**-visningen viser manuelle konturer i **Uke**- eller **Måned**-visningen.

**Prosjektledelse**

Følgende problemer har blitt løst:

- Et stort antall **RetrieveMultiple for usersettings**-enheter forårsaker redusert ytelse for prosjektgodkjenninger og andre operasjoner.
- Ressursoppslaget for rutenettet **Oppgaveplanlegging** er begrenset til bare å vise opptil fem teammedlemmer fra prosjektteamet. 
- Ressursoppslaget for rutenettet **Oppgaveplanlegging** filtrerer ikke inaktive ressurser.
- Manuell modus fungerer ikke som forventet i arbeidsnedbrytingsstrukturen for prosjektplanlegging.
- Rutenettet **Oppgaveplanlegging** viser **inaktive transaksjonskategorier**.
- Rutenettet **Ressurstilordning** runder av på feil måte når en oppgave har flere tilordninger.
- Avrundingsverdier er forskjellige mellom planlagt kostnad og faktisk kostnad for én enkelt oppgave.

**Sales**

Følgende problemer har blitt løst:

- Dobbeltklikk på **Hent alle transaksjonskategorier** oppretter flere linjer.


[!INCLUDE[footer-include](../includes/footer-banner.md)]