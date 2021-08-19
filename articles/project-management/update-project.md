---
title: Oppdatere et prosjekt
description: Dette emnet gir informasjon om oppdatering av prosjekter i Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: b0ec03a2c4dd7bc833b22b7a93fed810b4998a2788f4ff40234e3dd163bd9eb6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000903"
---
# <a name="update-a-project"></a>Oppdatere et prosjekt

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Nedenfor vises et sammendrag av feltene som kan oppdateres i et prosjekt etter at det er opprettet, og eventuelle gjeldende implikasjoner av oppdateringene.

## <a name="project-detail-fields"></a>Felt for prosjektdetaljer

- **Navn**: Tittelen på prosjektet.
- **Beskrivelse**: En oversikt over prosjektet.
- **Kunde**: Firmaet som prosjektet skal leveres til.
- **Kalendermal**: Arbeidstiden til prosjektet. Når feltet endres, beregnes hele tidsplanen på nytt.
- **Valuta**: Valutaen for prosjektet. Standardverdien i dette feltet er basert på valutaen som er definert i kontraktenheten. Når kontraktenheten oppdateres, oppdateres også feltet.
- **Kontraktenhet**: Organisasjonsenheten som representerer firmagruppen eller divisjonen som er primært ansvarlig for å vinne salget og administrere levering av arbeid og tjenester til kunden. 
- **Prosjektleder**: Prosjektteammedlemmet som har autoriteten til å se gjennom og godkjenne tidsoppføringer og utgifter.

## <a name="estimate-fields"></a>Estimatfelt

- **Estimer startdato**: Datoen når prosjektet skal starte. Når dette feltet oppdateres, flyttes eventuelle oppgaver i prosjektet proporsjonalt med den nye startdatoen.
- **Sluttdato**: Datoen prosjektet er planlagt å avsluttes.
- **Innsats**: Den beregnede arbeidsinnsatsen for prosjektet. Når det legges til oppgaver i prosjektet, kan ikke dette feltet lenger redigeres.
- **Estimert arbeidskostnad**: Den estimerte arbeidskostnaden for prosjektet. Når det legges til arbeidskostnader i prosjektet, kan ikke dette feltet lenger redigeres.
- **Estimerte utgifter**: De estimerte utgiftene for prosjektet. Når det legges til utgifter i prosjektet, kan ikke dette feltet lenger redigeres.

## <a name="project-actual-fields"></a>Felt for faktiske verdier for prosjekt
- **Faktisk start**: Datoen da prosjektet startet.
- **Faktisk slutt**: Oppdateres når et prosjekt er fullført.

## <a name="project-status-fields"></a>Felt for prosjektstatus

- **Generell prosjektstatus**: Den generelle prosjekttilstanden oppgitt av prosjektlederen.
- **Kommentarer**: Informasjon om gjeldende tilstand for prosjektet fra prosjektlederen.



[!INCLUDE[footer-include](../includes/footer-banner.md)]