---
title: Kopiere et prosjekt
description: Denne emnet gir informasjon om kopiering av prosjekter i Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe76f59b315fd0f46b25e1d116acde1f6b2864d1753e01d6311ea93ae7d116fc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007203"
---
# <a name="copy-a-project"></a>Kopier et prosjekt

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Med Dynamics 365 Project Operations kan du raskt bygge nye prosjekter ved å velge **Kopier prosjekt** i **Prosjekter**-skjemaet. Hvis du vil kopiere et prosjekt, åpner du prosjektet du vil kopiere, og deretter velger du **Kopier prosjekt**. Handlingen kopierer følgende:

- Prosjektegenskaper 
- Arbeidsnedbrytningsstruktur
- Prosjektteammedlemmer
- Prosjektestimater
- Prosjektets utgiftsestimater
- Prosjektmaterialestimater

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
- Beregnet startdato: Dette er datoen da prosjektet ble opprettet fra kopien.
- Beregnet sluttdato: Denne datoen justeres basert på startdatoen for det nye prosjektet som ble gjort fra kopien.
- Innsats (timer)
- Estimert arbeidskostnad
- Estimert utgiftskostnad
- Estimert materialkostnad

> [!NOTE]
> Kopieringsprosjektet kjører lenge. Prosjektoppføringer, de relevante attributtene og mange relaterte enheter kopieres også. På grunn av hvor lenge operasjonen har kjørt, låses målprosjektsiden for redigering til kopioperasjonen er fullført.

## <a name="work-breakdown-structure"></a>Arbeidsnedbrytningsstruktur

Når prosjektet kopieres, blir hele den ressurslastede arbeidsnedbrytningsstrukturen kopiert. Navngitte ressurser erstattes av generelle ressurser. Hvis de navngitte ressursene ikke har samme arbeidstid som den generelle ressursen, beregnes planleggingen på nytt, og varigheten på oppgavene kan bli endret.

## <a name="project-team-members"></a>Prosjektteammedlemmer

Når et prosjektteam kopieres fra kildeprosjektet, kopieres de generelle ressursene. Tildeling av generelle ressurser blir også vedlikeholdt slik som i kildeprosjektet. Navngitte ressurser konverteres til generelle teammedlemmer.

## <a name="estimates"></a>Estimater

Når prosjektet kopieres, kopieres ressurs-, utgifts- og materialestimatlinjer fra kildeprosjektet. 

Hvis du vil ha informasjon om hvordan du programmatisk får tilgang til Kopier Project, kan du se [Utvikle prosjektmaler med Kopier prosjekt](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
