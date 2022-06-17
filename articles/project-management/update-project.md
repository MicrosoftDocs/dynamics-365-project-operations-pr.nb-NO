---
title: Opprett og oppdater et prosjekt
description: Denne artikkelen inneholder informasjon om oppdatering av prosjekter i Project Operations.
author: ruhercul
ms.date: 10/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dcb822a726f94a7e8e8621dc7a04f9051168d361
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911102"
---
# <a name="create-and-update-a-project"></a>Opprett og oppdater et prosjekt

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Nedenfor vises et sammendrag av feltene som kan oppdateres i et prosjekt etter at det er opprettet. Dette inkluderer også eventuelle gjeldende implikasjoner basert på disse oppdateringene.

## <a name="project-detail-fields"></a>Felt for prosjektdetaljer

- **Navn**: Tittelen på prosjektet.
- **Beskrivelse**: En oversikt over prosjektet.
- **Kunde**: Firmaet som prosjektet skal leveres til.
- **Kalendermal**: Arbeidstiden til prosjektet. Når feltet endres, beregnes hele tidsplanen på nytt.
- **Valuta**: Valutaen for prosjektet. Standardverdien for dette feltet er basert på valutaen som er definert i kontraktsenheten. Når kontraktenheten oppdateres, oppdateres også feltet.
- **Kontraktenhet**: Organisasjonsenheten som representerer firmagruppen eller divisjonen som er primært ansvarlig for å vinne salget og administrere levering av arbeid og tjenester til kunden.  Når prosjektlederens organsasjonsenhet ikke er definert, brukes verdien som er definert i prosjektparameterne i dette feltet.
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
