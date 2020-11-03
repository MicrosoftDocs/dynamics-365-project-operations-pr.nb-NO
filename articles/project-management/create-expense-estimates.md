---
title: Utgiftsestimater
description: Dette emnet gir informasjon om hvordan du definerer eller beregner prosjektrelaterte utgifter.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2afe4ff2f84fc5426c409e6314da73b11a4de281
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081542"
---
# <a name="expense-estimates"></a>Utgiftsestimater
_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Sammen med å definere ressursbaserte estimater tillater Dynamics 365 Project Operations at prosjektledere definerer prosjektbasert utgifter for hvert prosjekt. Hvert utgiftselement kan tilknyttes en bestemt prosjektoppgave eller utgiftskategori. Utgiftskategorier defineres vanligvis på organisasjonsnivå. Priser for hver utgiftskategori defineres vanligvis i følgende hierarki:

- Organisasjonen
- Kunde
- Tilbud/kontrakt

Fullfør fremgangsmåten nedenfor for å vise, legge til eller slette en prosjektutgift.

1. Gå til **Prosjekter** , og velg prosjektet du vil arbeide med.
2. Velg kategorien **Prosjektestimater** , og vis listen over prosjektutgifter.
3. Velg **Ny utgift** for å legge til en utgift. Du kan også velge en utgift som skal slettes, og deretter velge **Slett utgift**.

Følgende attributter defineres for hvert utgiftslinjeelement:

- **Kategori** : Felles grupperinger som brukes til å beskrive alle utgifter som er påløpt i et prosjekt.
- **Startdato** : Datoen da utgiften er beregnet å påløpe.
- **Antall** : Det estimerte antallet utgiftselementer for en bestemt kategori.
- **Kostpris for enhet** : Enhetsprisen som brukes til å beregne kostnad for utgiften.
- **Salgspris for enhet** : Enhetsprisen som brukes til å beregne salgsprisen for utgiften.

