---
title: Hva er nytt i Project Service Automation Update Release 14, V3
description: Dette emnet inneholder informasjon om hva som er nytt i Project Service Automation Update Release 14 V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c69eab3b-0bb9-4b52-b606-e8a96e893471
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 31134756a5f4bff3022fca7df8364c49217b9b55
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754114"
---
# <a name="project-service-automation-v3-update-release-14"></a>Project Service Automation V3, Update Release 14
Vi er glade for å annonsere den nyeste oppdateringen av Dynamics 365 Project Service Automation (PSA)-programmet. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Denne versjonen er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for PSA V3, Update Release 14. Denne versjonen har buildnummer V3.10.4.21 og er tilgjengelig i henhold til følgende tidsplan:

- **Generell tilgjengelighet (egen oppdatering):** januar 2020
- **Automatisk oppdatering:** februar 2020

## <a name="update-release-14"></a>Update Release 14

### <a name="enhancements"></a>Forbedringer

- Sales

     - Egendefinerte feltverdier fra **Tilbudslinjedetaljer** kopieres til **Detaljer for prosjektkontraktlinjer** når et tilbud blir oppdatert til **Lukket som vunnet**.
     - Bekreftede prosjekter kan bli **Lukket som tapte**.

- Ressursbehandling

     - Når du utvider bestillinger, blir brukerne bedt om å oppgi en bekreftelsesdialogboks for å summere bestillingsresultater og opprette en kobling for å vedlikeholde bestillinger.


### <a name="bug-fixes"></a>Feilrettinger

- Tid og utgift

     - Fikset: Forbedret brukeropplevelsen når brukeren ikke har valgt noen oppføringer som skal rettes opp.

- Ressursbehandling

     - Fikset: Bestilling av en ressurs flere ganger overflyter navnet på den bestillbare ressursen.

- Sales

     - Fikset: Total salgspris beregnes ikke før brukeren også har angitt en kostpris for utgiftsestimater i et prosjekt.
     - Fikset: Lukking av et tilbud som **Vunnet** mislykkes hvis den tilknyttede prosjektkontrakten ikke er i **Utkast**-tilstand.

