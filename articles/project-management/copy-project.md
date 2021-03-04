---
title: Kopiere et prosjekt
description: Dette emnet gir informasjon om kopiering av prosjekter i Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 53c72e5fd680eb28128644788752368705440445
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131805"
---
# <a name="copy-a-project"></a>Kopiere et prosjekt

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Med Dynamics 365 Project Operations kan du raskt utvikle nye prosjekter ved å velge **Kopier prosjekt** i **Prosjekter**-skjemaet. Hvis du vil kopiere et prosjekt, åpner du prosjektet du vil kopiere, og deretter velger du **Kopier prosjekt**. Handlingen kopierer følgende:

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

Hvis du vil ha informasjon om hvordan du programmatisk får tilgang til Kopier Project, kan du se [Utvikle prosjektmaler med Kopier prosjekt](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]