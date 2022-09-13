---
title: Aktiver og revider et prosjekttilbud
description: Denne artikkelen inneholder informasjon om hvordan du aktiverer og reviderer tilbud i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e71102078832ac7d5f8e5edb40cc484df927eda4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410353"
---
# <a name="activate-and-revise-a-project-quote"></a>Aktiver og revider et prosjekttilbud

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Aktiverings- og revisjonsfunksjoner gjør det enklere å holde oversikt over versjonskontroll for prosjektbaserte tilbud under beregnings- og forhandlingsfasene. Når et tilbudsutkast aktiveres, blir det skrivebeskyttet.

Med aktiverings- og revisjonsfunksjonene kan du utføre følgende oppgaver:

- Vinn eller tap tilbud bare etter aktivering.
- Revider et tilbud for å gjøre endringer i det eksisterende tilbudet eller opprette en ny versjon.

> [!NOTE]
> Etter at funksjonen for aktivering og revisjon av tilbud er aktivert, kan den ikke deaktiveres.

Følg denne fremgangsmåten for å aktivere og revidere prosjektbaserte tilbud.

1. Gå til **Innstillinger** \> **Parametere**.
1. Åpne oppføringen **Parametere**.
1. Velg **Aktiver aktivering og revisjoner av tilbud** i fanen **Funksjonskontroll** i handlingsruten.
1. Velg **OK** i bekreftelsesdialogboksen.
1. Oppdater nettleseren etter en liten stund. Aktiverings- og revisjonsfunksjoner skal nå være tilgjengelige. Du kan se at disse funksjonene er aktivert hvis knappen **Aktiver aktivering og revisjoner av tilbud** ikke lenger vises i handlingsruten.

## <a name="activating-a-quote"></a>Aktivering av et tilbud

Når funksjonen for aktivering og revisjon av tilbud er aktivert, er ikke knappene **Lukk tilbud som vunnet** og **Lukk tilbud som tapt** tilgjengelige for utkast til prosjekttilbud i handlingsruten. De er bare tilgjengelige etter at et tilbud er aktivert.

Aktivering representerer fasen i tilbudsprosessen der du vil forhindre ytterligere endring av tilbudet. På dette trinnet sendes tilbudet til intern gjennomgang eller til kunden.

Knappene **Lukk tilbud som vunnet** og **Lukk tilbud som tapt** er tilgjengelige for aktiverte tilbud i handlingsruten. Avhengig av resultatet av gjennomgangen som gjøres internt eller av kunden, kan du bruke en av disse knappene til å lukke et aktivert tilbud. Du kan gjøre forhandlinger og endringer i aktiverte tilbud ved å velge **Revider tilbud**.

## <a name="revising-a-quote"></a>Revidering av et tilbud

Hvis du må gjøre endringer i et aktivert tilbud, velger du **Revider tilbud**. Tilbudet lukkes, og årsakskoden **revidert** brukes. Det opprettes da et nytt tilbud med samme ID og et økt revisjonsnummer. Alle detaljene fra det opprinnelige tilbudet kopieres til det nye tilbudet. Det nye tilbudet har utkaststatus og kan redigeres etter behov.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
