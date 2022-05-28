---
title: Hva er nytt eller endret i Project Service Automation Update Release 30, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 30, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: f99d2df3f9f6c0752109c39132c2401e0130d5df
ms.sourcegitcommit: 577fa51e0892625f98f17ff39874ed1a09444421
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/06/2022
ms.locfileid: "8723552"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Hva er nytt eller endret i Project Service Automation Update Release 30, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Denne versjonen er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for Project Service Automation V3, Update Release 30. Denne versjonen har et build-nummer på V3.10.51.61 og er generelt tilgjengelig via en egen oppdatering i april 2021.

## <a name="update-release-30"></a>Update Release 30

### <a name="bug-fixes"></a>Feilrettinger

**Tid og utgift**

Følgende problemer har blitt løst:

- Det oppstår en feil når du oppretter og lagrer en tidsoppføring på **Hurtigoppretting**-siden hvis **Rolle**-feltet er fjernet.
- Tidsregistrering-filteret bruker feil filteroperator.
- Kopierte timeregistreringer vises ikke automatisk når du velger **Kopier uke** på tidsregistreringskontrollen.

**Ressursbehandling**

Følgende problemer har blitt løst:

- Når du utvider en bestilling, er bestillingsstatusen som er tilordnet den forpliktende bestillingen, feil. Hvis du utvider en bestilling, respekteres bestillingsstatusen definert som **Utført** i metadataene for bestillingsoppsettet.
- Når en gyldig bestillingsstatus ikke er angitt, er ikke feilmeldingen riktig lokalisert.

**Prosjektledelse**

Følgende problemer har blitt løst:

- Prosjekter kan ikke opprettes i én valuta og inkludere relaterte oppgaver i en annen valuta.

**Salg**

Følgende problemer har blitt løst:

- Når en prisliste kopieres, oppdateres ikke prisene.
- Lukking av et tilbud som vunnet mislykkes når kostnadsdetaljene har en verdi for opprinnelse.
- I enheten **Prosjektoppgave** har **Estimert kostnad** fått endret navnet til **Planlagt kostnad (standardvaluta)**.
- Det genereres et nullreferanseunntak når fakturaer opprettes eller slettes.
