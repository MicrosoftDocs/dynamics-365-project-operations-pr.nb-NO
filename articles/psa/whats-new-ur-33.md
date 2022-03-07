---
title: Hva er nytt eller endret i Project Service Automation Update Release 33, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 33, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334578"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Hva er nytt eller endret i Project Service Automation Update Release 33, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for å kunngjøre den nyeste oppdateringen for Microsoft Dynamics 365 Project Service Automation-appen. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Den er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, kan du gå til siden for administrasjonssenteret for Dynamics 365 Online-løsninger og installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for Project Service Automation V3, Update Release 33. Denne versjonen har et build-nummer på V3.10.54.98 og er allment tilgjengelig via en egenoppdatering i juli 2021.

## <a name="update-release-33"></a>Update Release 33

### <a name="bug-fixes"></a>Feilrettinger

**Tid og utgift**

Følgende problemer har blitt løst:

- To låste felter, **msdyn_description** og **msdyn_externaldescription** kan redigeres etter sending.
- Det vises en feilmelding hvis det opprettes en utgift som ikke er relatert til et prosjekt.
- Når det opprettes en tidsoppføring, brukes en inaktiv rolle som standard i ressursrollen.
- Journallinjer som er knyttet til en tilbakekalt og slettet utgift, slettes ikke.
- Oppdater visningen **Prosjektoppgaveliste** i **Hurtigopprettingsskjema for tidsoppføring** for å endre datoen som vises som standard, til startdatoen for oppgaven.
- Når du oppretter en tidsoppføring fra fanen **Relatert** for ressursen som kan reserveres, opprettes tidsoppføringen feil for den påloggede brukeren i stedet for den overordnede ressursen som kan reserveres.
- Nye felter er lagt til i dialogboksen **MDD for massegodkjenning**.

**Prosjektplanlegging**

Følgende problemer har blitt løst:
- Treg prosjektopprettingsytelse når maler for prosjektarbeidstimer brukes med komplekse kalendere.
- Når startdatoen er større enn sluttdatoen, vises det en feil i kopieringsprosjektmalen på grunn av forskjeller i tidskomponenten i hvert felt.

**Ressursstyring**

Følgende problemer har blitt løst:
- En feil parameter brukes i spørringen om ressursutnyttelse, og XML fører til feil filterresultater i rutenettet **Ressursutnyttelse**.
- Bekreftelsen **Utvid bestillinger** viser feil sluttdato for bestillinger.

**Salg**

Følgende problemer har blitt løst:
- Det vises en feilmelding hvis en kategoripris opprettes med manglende verdier.
- Det vises en feilmelding hvis en kontraktlinjemilepæl opprettes uten en ordrelinje.
