---
title: Hva er nytt eller endret i Project Service Automation Update Release 28, V3
description: Denne artikkelen viser funksjoner og rettelser i Project Service Automation Update Release 28 V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 56a87bce55c560e541e20709b10d38b9512ffcee
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930606"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Hva er nytt eller endret i Project Service Automation Update Release 28, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Denne versjonen er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Denne artikkelen viser funksjoner og rettelser som er nye eller endret for Project Service Automation V3, Update Release 28. Denne versjonen har build-nummeret V3.10.46.32 og er allment tilgjengelig via en egenoppdatering i januar 2021.

## <a name="update-release-28"></a>Update Release 28

### <a name="bug-fixes"></a>Feilrettinger

**Tid og utgift**

Følgende problemer har blitt løst:

- Brukere kan bruke **Masseredigering** til å oppdatere tidsoppføringer som er godkjent og sendt.

**Prosjektledelse**

Følgende problemer har blitt løst:

- I tilfeller der oppgave-GUID tolkes som et tall, kan ikke oppgaver åpnes for redigering ved hjelp av **Rediger oppgave** på båndet på siden **Arbeidsnedbrytningsstruktur**.

**Sales**

Følgende problemer har blitt løst:

- Det genereres et nullreferanseunntak når programtillegget **GetEstimatesForProject** startes.
- **Merk som klar for fakturering** i milepælrutenettet oppdaterer bare attributter delvis, med unntak av attributtet **InvoiceStatus**, som blir oppdatert.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
