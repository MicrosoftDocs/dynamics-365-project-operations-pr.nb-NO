---
title: Kopiere et prosjekt
description: Denne emnet gir informasjon om kopiering av prosjekter i Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479531"
---
# <a name="copy-a-project"></a>Kopier et prosjekt

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Med Dynamics 365 Project Operations kan du raskt bygge nye prosjekter ved å velge **Kopier prosjekt** i **Prosjekter**-skjemaet. Hvis du vil kopiere et prosjekt, åpner du prosjektet du vil kopiere, og deretter velger du **Kopier prosjekt**. Handlingen kopierer følgende:

- Prosjektegenskaper (Beregnet startdato kopieres fra kildeprosjektet)
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

Hvis du vil ha informasjon om hvordan du programmatisk får tilgang til Kopier Project, kan du se [Utvikle prosjektmaler med Kopier prosjekt](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
