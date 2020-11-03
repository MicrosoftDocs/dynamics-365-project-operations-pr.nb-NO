---
title: Oppdatere et prosjekt
description: Dette emnet gir informasjon om oppdatering av prosjekter i Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5c9cd0c7c6886bd454c5f2ef2ae7f20d1707293f
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081475"
---
# <a name="update-a-project"></a>Oppdatere et prosjekt

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Nedenfor vises et sammendrag av feltene som kan oppdateres i et prosjekt etter at det er opprettet, og eventuelle gjeldende implikasjoner av oppdateringene.

## <a name="project-detail-fields"></a>Felt for prosjektdetaljer

- **Navn** : Tittelen på prosjektet.
- **Beskrivelse** : En oversikt over prosjektet.
- **Kunde** : Firmaet som prosjektet skal leveres til.
- **Kalendermal** : Arbeidstiden til prosjektet. Når feltet endres, beregnes hele tidsplanen på nytt.
- **Valuta** : Valutaen for prosjektet. Standardverdien i dette feltet er basert på valutaen som er definert i kontraktenheten. Når kontraktenheten oppdateres, oppdateres også feltet.
- **Kontraktenhet** : Organisasjonsenheten som representerer firmagruppen eller divisjonen som er primært ansvarlig for å vinne salget og administrere levering av arbeid og tjenester til kunden. 
- **Prosjektleder** : Prosjektteammedlemmet som har autoriteten til å se gjennom og godkjenne tidsoppføringer og utgifter.

## <a name="estimate-fields"></a>Estimatfelt

- **Estimer startdato** : Datoen når prosjektet skal starte. Når dette feltet oppdateres, flyttes eventuelle oppgaver i prosjektet proporsjonalt med den nye startdatoen.
- **Sluttdato** : Datoen prosjektet er planlagt å avsluttes.
- **Innsats** : Den beregnede arbeidsinnsatsen for prosjektet. Når det legges til oppgaver i prosjektet, kan ikke dette feltet lenger redigeres.
- **Estimert arbeidskostnad** : Den estimerte arbeidskostnaden for prosjektet. Når det legges til arbeidskostnader i prosjektet, kan ikke dette feltet lenger redigeres.
- **Estimerte utgifter** : De estimerte utgiftene for prosjektet. Når det legges til utgifter i prosjektet, kan ikke dette feltet lenger redigeres.

## <a name="project-actual-fields"></a>Felt for faktiske verdier for prosjekt
- **Faktisk start** : Datoen da prosjektet startet.
- **Faktisk slutt** : Oppdateres når et prosjekt er fullført.

## <a name="project-status-fields"></a>Felt for prosjektstatus

- **Generell prosjektstatus** : Den generelle prosjekttilstanden oppgitt av prosjektlederen.
- **Kommentarer** : Informasjon om gjeldende tilstand for prosjektet fra prosjektlederen.

