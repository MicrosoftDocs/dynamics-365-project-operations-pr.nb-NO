---
title: Hva er nytt eller endret i Project Service Automation Update Release 17, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 17, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 7ba685568692dafe117de42a71bb14d391cd7cc4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081576"
---
# <a name="project-service-automation-update-release-17-v3"></a>Project Service Automation, Update Release 17, V3

Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet.  Denne versjonen er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for PSA V3, Update Release 17. Denne versjonen har buildnummer V3.10.6.34 og er generelt tilgjengelig via en egen oppdatering fra mars 2020.


## <a name="update-release-17"></a>Update Release 17

### <a name="bug-fixes"></a>Feilrettinger

**Generelt**

- Løst: Oppdatert Project Service Automation for å håndheve teammedlemmers lisenser (prosjektressurshuben vil inkludere tjenesteplanmetadata 3.x for teammedlem)
 
**Tid og utgift**

- Fast: Det er ikke mulig å endre et utgiftsestimat til null (0) fra en annen pris enn null. Endringen ignoreres.

**Prosjektledelse**

- Løst: En kontroll for nullverdier i stillingsnavnet for et teammedlem er lagt til.
- Løst: Feltet **msdyn_userresourceid** for enheten **msdyn_resourceassignment** er avskrevet.
- Løst: Oppgradering fra 2.x til 3.x håndterer nå tomme innsatsprofiler på oppgavetilordninger.

**Sales**

- Løst: **Invoice.PreValidateInvoiceUpdate** behandler nå scenarioet for å tilordne oppføringseiere på nytt på riktig måte.
- Løst: Når transaksjonsklassen er **Tidspunkt** , er **UnitGroup** ikke redigerbart for alle enheter, inkludert **QuoteLineDetails** , **JournalLine** , **InvoiceLineDetail** og **ContractLineDetails**. Imidlertid er **Enhet** ikke-redigerbart kun for **JournalLine** og **InvoiceLineDetails**.


