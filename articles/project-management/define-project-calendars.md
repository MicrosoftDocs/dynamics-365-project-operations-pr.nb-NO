---
title: Definer prosjektkalendere
description: Dette emnet gir informasjon om hvordan du bruker en kalendermal på et prosjekt til å følge opp prosjektplanen.
author: ruhercul
manager: AnnBe
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d5642d7a2246dc878b2bc4f504f138b71d29a69
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981312"
---
# <a name="define-project-calendars"></a>Definer prosjektkalendere

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Hvis du vil opprette og administrere et prosjekt, må du bruke en kalendermal på prosjektet. Kalendermalen definerer følgende prosjektattributter:

- Arbeidstid, inkludert start- og sluttidspunkt
- Arbeidsdager
- Kalenderunntak, for eksempel fridager

Kalendermalen som brukes på et prosjekt, er en kopi av kalendermalen som er definert i organisasjonens innstillinger.

> [!NOTE]
> Hvis du endrer kalendermalen, overføres ikke disse endringene til arbeidstiden for prosjektet. Hvis du vil endre arbeidstiden for prosjektet, må du bruke en ny mal.

Hvis du vil opprette en kalendermal for organisasjonen, er det to viktige krav:

- Definer ønsket arbeidstid for malen ved hjelp av en ny eller eksisterende ressurs som kan reserveres.
- Opprett en ny kalendermal, og knytt malen til ressursen som kan reserveres.

**Definer arbeidstimene for malen**

1. Gå til **Ressurser** \> **Ressurser**.
2. Opprett en ny ressurs som skal refereres til i kalendermalen, eller velg en eksisterende ressurs.
3. Velg kategorien **Arbeidstimer** for ressursen, og fullfør instruksjonene i [Angi arbeidstimer for en ressurs](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) for å konfigurere kalenderreglene.

**Opprett en ny kalendermal**

1. Gå til **Innstillinger** \> **Kalendermal**.
2. Velg **Ny**, og skriv inn et navn, en beskrivelse og en malressurs.

> [!NOTE]
> Når det refereres til en ressurs i en kalendermal, knyttes en kopi av ressursens kalender til kalendermalen. Hvis arbeidstimene for den kopierte malen endres, overføres ikke disse endringene til kalendermalen.

Du kan nå knytte arbeidsmalen til en prosjektkKalendermal.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

