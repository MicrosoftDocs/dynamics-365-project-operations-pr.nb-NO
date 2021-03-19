---
title: Hva er nytt eller endret i Project Service Automation Update Release 24, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 24, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c789a65f1996d082410b3d8dd9e76e5065e708a2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280500"
---
# <a name="project-service-automation-update-release-24-v3"></a>Project Service Automation, Update Release 24, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Denne versjonen er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for Project Service Automation V3, Update Release 24. Denne versjonen har buildnummer V3.10.42.43 og er generelt tilgjengelig via en egen oppdatering i oktober 2020.

## <a name="update-release-24"></a>Update Release 24

### <a name="bug-fixes"></a>Feilrettinger

**Sales**

Følgende problemer har blitt løst:

- Problem under angivelse av standard prisliste for produkter.
- Ytelsen til vunnet tilbud er treg på grunn av den innebygde kopien av prisliste- og rolleprisoppføringene.
- **Prosjektkontrakt/Salgshub** > **Produktlinjevare/Ordrelinjeantall** rundes automatisk av til nærmeste heltall.
- Utvid til systemrettigheter ved lesing av prislister.
- Kopier kundeadressefeltene **address1_freighttermscode** og **address1_shippingmethodcode** til tilbud/ordre. 


**Tid og utgift**

Følgende problemer har blitt løst:

- **Rutenett for tidsoppføring** støtter ikke tidsvirkemåten for **Bare dato**.
- **Tidsoppføring** oppdateres ikke automatisk. Det kreves en manuell oppdatering.
- Kan ikke importere tidsoppføringer fra en tilordning når det er en pause (0 timer) i tilordningene for en ressurs.
- Når du oppretter en tidsoppføring, angir du starten til den samme som **msdyn_date**.
- Aktiver masseredigering for tidsregistrering på nytt.

**Ressursbehandling**

Følgende problemer har blitt løst:

- Hvis du prøver å oppdatere statusen for en bestilling mellom flere dager uten et krav, blir det iverksatt et nullreferanseunntak.
- Feil under innlasting av **avstemmingsvisningen**.


**Prosjektledelse**

Følgende problemer har blitt løst:

- I **Prosjekttidsplan**, når du bytter fra **Manuell** til **Automatisk**, fullføres ikke automatisk lagring.
- Utgiftskostnader bør ikke beregnes mot varians i **rutenettet for prosjektsporing**.
- Inkonsekvent virkemåte for **Estimatmerke**-kolonner under innlasting, i forhold til endring av **Tidsfase**-typen.
- De faktiske kostnadene i et prosjekt gjenspeiler kanskje ikke totalverdiene fra **Faktiske verdier**.
- **Beregnet sluttdato** i kategorien **Sammendrag** samsvarer ikke med **WBS-plan**.
- **Oppdater faktiske timer** ved redusering av innrykk fungerer ikke riktig.
- En prosjektleder utenfor rot-**BU** kan ikke opprette et prosjekt.
- Endringer i oppgaven eller kategorien i **Utgiftsestimater** beholdes ikke.
- **Kopi av kontrakt** kopierer faktureringsplanene og kjørestatusen.
- Knappen **Oppdater faktiske verdier** beregner aktivitetssammendrag på feil måte.
- Microsoft Project-tillegg: Reparer nullreferansefeil hvis et teammedlem har en tom ressursenhet.



[!INCLUDE[footer-include](../includes/footer-banner.md)]