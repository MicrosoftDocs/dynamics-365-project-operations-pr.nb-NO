---
title: Planleggingsmoduser
description: Dette emnet inneholder informasjon om planleggingsmoduser.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 508ff1df8f7e31066712fab6f8871dfdb107a43b
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116719"
---
# <a name="scheduling-modes"></a>Planleggingsmoduser

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_


Dynamics 365 Project Operations gjør det mulig for organisasjoner å definere hvordan de behandler endringer i viktige variabler i oppgaver i arbeidsnedbrytningsstrukturen. Basert på de spesielle behovene organisasjonen har, kan prosjektledere gjøre endringer i planleggingsmodusen når et prosjekt blir opprettet.

Det er tre planleggingsmoduser tilgjengelig i Project Operations:

  - Fast varighet (dette er standardmodusen)
  - Fast innsats (*Arbeid*)
  - Faste enheter

Verdiene som påvirkes av definisjonen av en bestemt planleggingsmodus, bestemmes av følgende formel:

  Innsats = Varighet x enheter

Når du definerer planleggingsmodusen for et prosjekt, angir du en av disse verdiene, som da ikke kan endres. Når du holder denne verdien som en konstant, prioriteres verdien, som varsler at systemet ikke skal endre den når de to andre verdiene endres. Tabellen nedenfor inneholder informasjon om virkningene ved valg av en bestemt modus.

| **I denne oppgaven**             | **Hvis du reviderer enheter**   | **Hvis du reviderer varighet** | **Hvis du reviderer innsats**  |
|----------------------|---------------------------|----------------------------|---------------------------|
| Faste enheter-oppgaver     | Varigheten beregnes på nytt. | Innsats beregnes på nytt.    | Varigheten beregnes på nytt. |
| Fast innsats-oppgave    | Varigheten beregnes på nytt. | Enheter beregnes på nytt.    | Varigheten beregnes på nytt. |
| Fast varighet-oppgave  | Innsats beregnes på nytt.   | Innsats beregnes på nytt.    | Enheter beregnes på nytt.   |

Hvis du vil ha mer informasjon om implikasjonene av en bestemt modus, kan du se [Endre oppgavetypen for å få mer nøyaktig planlegging](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72). I emnet brukes termen **Arbeid** i stedet for **Innsats**.

## <a name="change-the-organizations-scheduling-mode"></a>Endre organisasjonens planleggingsmodus

Fullfør trinnene nedenfor for å definere planleggingsmodusen for en organisasjon.

1. Gå til **Innstillinger** \> **Generelt** \> **Parametere**, og velg deretter prosjektparameteren. 
2. På siden **Prosjektparametere** velger du standard planleggingsmodus for organisasjonen, og deretter definerer du muligheten for at prosjektlederen skal kunne overstyre innstillingen når det opprettes et nytt prosjekt.

## <a name="change-the-scheduling-mode-setting-on-a-project"></a>Endre innstillingen for planleggingsmodus for et prosjekt

Hvis en organisasjon tillater at prosjektlederen overstyrer standard planleggingsmodus, kan prosjektlederen endre dette når de oppretter et nytt prosjekt. Når prosjektet er lagret, kan imidlertid ikke planleggingsmodusen endres.

## <a name="copied-projects"></a>Kopierte prosjekter

Siden et prosjekt opprettes når kopieringsprosjekthandlingen utføres, kan ikke prosjektlederen angi planleggingsmodus. Målprosjektet vil som standard alltid være i modusen definert på organisasjonsnivå.

## <a name="copied-tasks"></a>Kopierte oppgaver

Når en oppgave kopieres fra ett prosjekt til et annet, arver oppgaven planleggingsmodusen for målprosjektet.
