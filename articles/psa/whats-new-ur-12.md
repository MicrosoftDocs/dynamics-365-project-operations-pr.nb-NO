---
title: Hva er nytt eller endret i Project Service Automation Update Release 12, V3
description: Dette emnet inneholder informasjon om hva som er nytt i Project Service Automation Update Release 12, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: 62c3a0c5cfbecb568faef570da309c20afd86de9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081581"
---
# <a name="project-service-automation-update-release-12-v3"></a>Project Service Automation, Update Release 12, V3
Vi er glade for å annonsere den nyeste oppdateringen av Dynamics 365 Project Service Automation (PSA)-programmet. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Denne versjonen er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for Project Service Automation V3, Update Release 12. Denne versjonen har buildnummer V3.10.2.34 og er vanligvis tilgjengelig via en egen oppdatering i oktober 2019.

## <a name="update-release-12"></a>Update Release 12

### <a name="bug-fixes"></a>Feilrettinger

- Tid og utgift

    - Fikset: Timeregistreringsfeilmeldinger er oppdatert med mer relevant kontekst.
    - Fikset: Rutenett for tidsoppføring og tidsplan viser riktig loddrett rullefelt når det er nødvendig.
    - Fikset: Innsendte utgifts- og tidsoppføringer kan godkjennes.
    - Fikset: Dialogmelding for bekreftelse av annullering av bekreftelse er korrigert for å vise statusen til godkjenningen når den endres fra **Godkjent** til **Sendt**.
    - Fikset: Feltene **Pris** , **Enhet** og **Antall** er nå låst på utgiftsoppføringen etter at den er godkjent.

- Prosjektledelse

    - Fikset: **Ny** -handling på hovedskjemaet for **Teammedlem** er fjernet.
    - Fikset: Ressurstilordningene er oppdatert for å ta høyde for unøyaktige avrundingsfeil, noe som fører til endring av sluttdatoen for oppgaven.
    - Fikset: I oppgaverutenettet blir relevante feil på serversiden vist for brukeren.
    - Fikset: Navnet på teammedlemmet gjengis nå i personvelgeren for oppgave i stedet for posisjonsnavnet.

- Ressursbehandling

    - Fikset: Detaljer for ressurskrav for prosjekter som er opprettet fra en mal, bruker nå prosjektkalenderen.
    - Fikset: Kompetanse og ferdigheter går nå som standard fra rollehoveddata til ressurskravene som er opprettet for rollen.

- Sales

    - Fikset: Duplikate objekt-IDer ble funnet i hovedskjemaet for **Kontrakt**.
    - Fikset: Logikken er oppdatert slik at kategorien **Tilbudsanalyse** blir synlig og viser metadataoppsettet for kategorien.
    - Fikset: Regnskapsdato på den faktiske oppføringen kommer nå fra datoen for tids-/utgiftsoppføring og ikke fra godkjenningsdatoen.