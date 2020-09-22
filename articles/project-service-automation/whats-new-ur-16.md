---
title: Hva er nytt i Project Service Automation Update Release 16, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 16, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: b890a7b6-1664-4812-8732-fed77653cc05
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 0f4c206fd5b7a36d940e966b28c2437525812a98
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754112"
---
# <a name="project-service-automation-v3-update-release-16"></a>Project Service Automation V3, Update Release 16
Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet.

Denne versjonen er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen. For mer informasjon, se [Installere eller oppdatere en foretrukket løsning](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page). Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for PSA V3, Update Release 16. Denne versjonen har buildnummer V3.10.6.34 og er vanligvis tilgjengelig via en egen oppdatering i januar 2020

## <a name="update-release-16"></a>Update Release 16

### <a name="bug-fixes"></a>Feilrettinger

-   Tid og utgift

    -   Løst: Brukere som forsøker å sende slettede tids- og utgiftsoppføringer til godkjenning, mottar nå relevante feilmeldinger.

-   Prosjektledelse

    -   Løst: Ressursenhetene som er definert for teammedlemmer i maler, overholdes når malene brukes på et nytt prosjekt.

    -   Løst: Forbedret håndtering av den nye tildelingen av oppføringseierskap.

    -   Løst: Prosjekter som er i ferd med å bli kopiert, har ikke tillatelse til å kopieres før alle kopieringsoperasjonene er fullført.

-   Ressursbehandling

    -   Løst: Utvid bestillinger håndterer nå korte varigheter på riktig måte, og det opprettes ikke lenger nulltimer for utvidede bestillinger.

    -   Løst: Avstemmingsvisningen gjengir nå når prosjektets tidssone er +5:30 GMT, og brukerens tidssone er forskjellig.

-   Sales

    -   Løst: Når et prosjekt som er tilordnet til en kontraktlinje, blir fjernet og et nytt prosjekt blir tilordnet, ble ikke de faktiske oppføringene i det nye prosjektet evaluert på nytt basert på fakturerings- og prisreglene som var definert i kontraktlinjen. Dette er løst i denne versjonen. Priser og faktiske oppføringer i det nylig tilordnede prosjektet blir tilbakeført og opprettet på nytt på riktig måte basert på priser og faktureringsregler for kontraktlinjen. De faktiske oppføringene i det ikke-tilordnede prosjektet blir også evaluert på nytt og opprettet på nytt som en følge av dette.

    -   Løst: Ytterligere validering er lagt til i **Beløp**-feltet for en estimatlinje for å sikre at nullverdier ikke beholdes.

    -   Løst: Når faktiske verdier er oppdatert i et prosjekt, er det lagt til en Oppdater-knapp i hovedskjemaet for prosjektet, slik at brukere kan synkronisere de faktiske verdiene på nytt.

    -   Løst: Når brukere oppgraderer fra 2.X til 3.X, blir prosjekter med NULL-verdi for prosjektnavn tillatt.

