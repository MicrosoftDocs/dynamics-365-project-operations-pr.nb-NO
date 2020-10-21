---
title: Kopiere et prosjekt
description: Dette emnet gir informasjon om kopiering av prosjekter i Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e35dc725e7938e9f59f7151dd1b37500fabf77a4
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908429"
---
# <a name="copy-a-project"></a>Kopiere et prosjekt

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Med Dynamics 365 Project Operations kan du raskt utvikle nye prosjekter ved hjelp av handlingen **Kopier prosjekt** i **Prosjekter**-skjemaet. Hvis du vil kopiere et prosjekt, velger du et prosjekt, og deretter velger du **Kopier**. Handlingen kopierer følgende:

- Prosjektegenskaper
- Arbeidsnedbrytningsstrukturen
- Prosjektteammedlemmer
- Prosjektestimater
- Prosjektets utgiftsestimater

## <a name="project-properties"></a>Prosjektegenskaper

Når prosjektet kopieres, blir verdiene i følgende felt kopiert:

- Navn
- Beskrivelse
- Kunde
- Kalendermal
- Valuta
- Kontraktsenhet
- Prosjektleder
- Status
- Generell prosjektstatus
- Kommentarer
- Estimater
- Beregnet startdato
- Sluttdato
- Innsats (timer)
- Estimert arbeidskostnad
- Estimert utgiftskostnad

## <a name="work-breakdown-structure"></a>Arbeidsnedbrytningsstruktur

Når prosjektet kopieres, blir hele den ressurslastede arbeidsnedbrytningsstrukturen kopiert. Navngitte ressurser erstattes av generelle ressurser. Hvis de navngitte ressursene ikke har samme arbeidstid som den generelle ressursen, beregnes planleggingen på nytt, og varigheten på oppgavene kan bli endret.

## <a name="project-team-members"></a>Prosjektteammedlemmer

Når et prosjektteam kopieres fra kildeprosjektet, kopieres de generelle ressursene. Tildeling av generelle ressurser blir også vedlikeholdt slik som i kildeprosjektet. Navngitte ressurser konverteres til generelle teammedlemmer.

## <a name="estimates"></a>Estimater

Når prosjektet kopieres, blir både ressurs- og kostnadsestimatlinjer kopiert fra kildeprosjektet.