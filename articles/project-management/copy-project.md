---
title: Kopier et prosjekt
description: Denne artikkelen inneholder informasjon om kopiering av prosjekter i Dynamics 365 Project Operations.
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: b358f9e45278d886f3e6e8e8cd747fc0ea30212b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925776"
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
- Prosjektsjekklister
- Prosjektsamlinger

## <a name="project-properties"></a>Prosjektegenskaper

Når prosjektet kopieres, blir verdiene i følgende felter kopiert.

| Felt | Ikke-lagerførte materialer i Project Operations | Project Operations Lite | Project for the Web |
|-------|------------------------------------------|-------------------------|---------------------|
| Name | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Bekrivelse | :heavy_check_mark: | :heavy_check_mark: | |
| Kunde | :heavy_check_mark: | :heavy_check_mark: | |
| Kalendermal | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Valuta | :heavy_check_mark: | :heavy_check_mark: | |
| Kontraktsenhet | :heavy_check_mark: | :heavy_check_mark: | |
| Eiende firma | :heavy_check_mark: | | |
| Prosjektleder | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Status | :heavy_check_mark: | :heavy_check_mark: | |
| Generell prosjektstatus | :heavy_check_mark: | :heavy_check_mark: | |
| Kommentarer | :heavy_check_mark: | :heavy_check_mark: | |
| Estimater | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Beregnet startdato</p><p><strong>Obs!</strong> Dette feltet angir datoen da prosjektet ble opprettet fra kopien. | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Beregnet sluttdato</p><p><strong>Obs!</strong> Datoen i dette feltet justeres basert på startdatoen for det nye prosjektet som ble laget fra kopien.</p> | :heavy_check_mark: | :heavy_check_mark: | |
| Innsats (timer) | :heavy_check_mark: | :heavy_check_mark: | |
| Estimert arbeidskostnad | :heavy_check_mark: | :heavy_check_mark: | |
| Estimert utgiftskostnad | :heavy_check_mark: | :heavy_check_mark: | |
| Estimert materialkostnad | | :heavy_check_mark: | |

> [!NOTE]
> Kopieringsprosjektet kjører lenge. Prosjektoppføringer, de relevante attributtene og mange relaterte enheter kopieres også. På grunn av hvor lenge operasjonen har kjørt, låses målprosjektsiden for redigering til kopioperasjonen er fullført.

## <a name="work-breakdown-structure"></a>Arbeidsnedbrytningsstruktur

Når prosjektet kopieres, blir hele den ressurslastede arbeidsnedbrytningsstrukturen kopiert. Navngitte ressurser erstattes av generelle ressurser. Hvis de navngitte ressursene ikke har samme arbeidstid som den generelle ressursen, beregnes tidsplanen på nytt, og aktivitetsvarighetene kan endres.

## <a name="project-team-members"></a>Prosjektteammedlemmer

Når et prosjektteam kopieres fra kildeprosjektet, kopieres de generelle ressursene. Tildeling av generelle ressurser blir også vedlikeholdt slik som i kildeprosjektet. Navngitte ressurser konverteres til generelle teammedlemmer.

> [!NOTE]
> Teammedlemmer og tildelinger kopieres ikke i Project for the Web.

## <a name="estimates"></a>Estimater

Når prosjektet kopieres, kopieres ressurs-, utgifts- og materialestimatlinjer fra kildeprosjektet. 

Hvis du vil ha informasjon om hvordan du programmatisk får tilgang til Kopier Project, kan du se [Utvikle prosjektmaler med Kopier prosjekt](dev-copy-project.md).

## <a name="quotes-and-contracts"></a>Tilbud og kontrakter

Tilbud og kontrakter er ikke koblet til målprosjektet.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
