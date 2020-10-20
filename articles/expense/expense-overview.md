---
title: Oversikt over utgifter
description: Dette emnet gir information om Utgift-funksjonaliteten i Project Operations.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 6da831fef5dba060b8019d7689645405c7ebdbed
ms.sourcegitcommit: 0874b3d89e1dc0e65a51cedb82bf8f80831ca0bb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/06/2020
ms.locfileid: "3967378"
---
# <a name="expense-home-page"></a>Startside for utgift

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_


Dynamics 365 Project Operations støtte behandling av utgifter. Utgiftsbehandling forekommer med eller uten prosjekter ved å bruke en tilpassbar arbeidsflyt med policyer, transaksjonskategorier og godkjenninger.

I Project Operations finnes det to støttede distribusjonsmodeller for utgifter: 

- **Fullstendig**: Fullstendig distribusjon er tilgjengelig for **Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer** eller **Project Operations for produksjonsordrebaserte scenarioer**.
- **Standard**: Standard distribusjon er tilgjengelig for **Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer** og **Lite-distribusjon – avtale til proformafakturering**.

## <a name="full"></a>Fullstendig 
Fullstendig utgiftsdistribusjon gir en fullstendig håndheving av en policy som inkluderer muligheten til å opprette policyer, for eksempel følgende:

  - Grenser for utgiftskategori
  - Reise
  - Kostgodtgjørelse
  - Kredittkortimporter
  - Optisk tegngjenkjenning for kvittering

## <a name="basic"></a>Standard 
Et scenario med standard utgiftsdistribusjons tillater bare registrering av grunnleggende utgifter mot et prosjekt. 

Hvis du vil ha mer informasjon, kan du se [Utgiftsregistrering (Lite)](basic-expense.md)

## <a name="determine-your-expense-deployment"></a>Fastslå utgiftsdistribusjonen
For å finne ut om du kjører standard distribusjon av utgiftshåndtering, må du kontrollere at URL-adressen for adressen slutter på **.crm.dynamics.com**. 
