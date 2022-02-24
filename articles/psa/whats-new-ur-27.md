---
title: Hva er nytt eller endret i Project Service Automation Update Release 27, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 27, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 7f05b082e7c67937c78c82dcd9e094ee3b989e94
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948524"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Hva er nytt eller endret i Project Service Automation Update Release 27, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Denne versjonen er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for Project Service Automation V3, Update Release 27. Denne versjonen har buildnummer V3.10.45.98 og er vanligvis tilgjengelig via en egen oppdatering i januar 2021.

## <a name="update-release-27"></a>Update Release 27

### <a name="bug-fixes"></a>Feilrettinger

**Generelt**

Følgende problemer har blitt løst:

- Logger som genereres av plugin-moduler i Project Service Automation, er ikke satt til automatisk sletting.
- Automatisk oppgradering mislykkes fordi Project Service Automation-løsningen inneholder et eldre null NavBarArea- og tittelelement.

**Tid og utgift**

Følgende problemer har blitt løst:

- Rutenettet **Tidsoppføring** viser feil data for virkemåten for datoen **Tidssoneuavhengig**.
- Rutenettet **Tidsoppføring** oppretter feil tidspunkt for virkemåten for datoen **Tidssoneuavhengig**.
- Oppgaveoppslag er ikke begrenset til det valgte prosjektet på siden **Rediger tidsoppføring**.
- Tidsgodkjenning for ikke-prosjekttidsoppføringer blir blokkert fordi systemet ser etter en prosjektgodkjenner.
- Riktige oppføringer i Faktiske data viser en ugyldig feilmelding.
- Når en oppgave inneholder en nullverdi for faktisk kostnad og prosjekttotalene oppdateres, vises følgende feil: Gitt nøkkel finnes ikke i ordlisten.
- I bestemte forekomster viser ikke **Grupper etter**-filtre i kategorien **Prosjektestimat** utgiftsestimater.
- **Sommertid**-intervallet er ikke riktig for tidsoppføringer.

**Prosjektledelse**

Følgende problemer har blitt løst:

- Hurtigbufringsforbedringer, som forbedrer ytelsen ved lasting av **Prosjekt**-siden.
- Foreldet forretningsregel som hindrer at prosjektoppgaver blir fullført.
- Microsoft Project-tillegg respekterer ikke tilleggets kalender som fører til feil ressurskrav.
- Oppretting av prosjekter fra maler angir feil tilordningsdatoer og hindrer muligheten til å generere ressurskrav.
- Brukeren har ikke tilgang alternativene **Kategori**, **Beskrivelse** og **Status** ved hjelp av tastaturet.
- Faktiske salgsverdier for prosjektet inkluderer ikke salgsverdier for gebyr og materiell.
- Samling av faktisk salg og faktisk kostnad skjer på feil måte med ulike valutakurser.
- Beskrivelsen i **malen for standard arbeidstid** er misvisende.
- Når du rykker inn en oppgave, fjernes ikke **Kategori** i brukergrensesnittet før den er oppdatert.
- Manglende validering for å sikre at et prosjekt flyttes utover sluttdatoen, er ikke tillatt.

**Sales**

Følgende problemer har blitt løst:

- Det genereres et nullreferanseunntak på en prosjekttilbudslinje fordi **Importer fra prosjektberegningen** vises når et prosjekt ikke er valgt.
- Følgende feil: Objektreferanse er ikke satt til en objektforekomst oppstår når et tilbud lukkes som **Vunnet**.
- Justeringsstatusen blir ikke satt under faktisk tilbakeføring under opphevingen av kobling til et prosjekt fra en kontraktlinje.
- Når Dynamics 365 Field Service og Project Service Automation er installert, vises ikke alternativene **Lås prissetting** og **Bruk gjeldende priser** samtidig på **Faktura**-siden.
- For det japanske språket finnes det inkonsekvent oversetting med andre kalenderbaserte sider.
- **Aktiver** og **Deaktiver** er fjernet fra enehetene for **Prislistetilknytning** i Project Service Automation.


[!INCLUDE[footer-include](../includes/footer-banner.md)]