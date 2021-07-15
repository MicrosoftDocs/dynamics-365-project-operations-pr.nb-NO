---
title: Ytelse for prosjektfakturaforslag
description: Dette emnet inneholder informasjon om ytelsesforbedringer av prosjektfakturaforslag.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269802"
---
# <a name="project-invoice-proposal-performance"></a>Ytelse for prosjektfakturaforslag

[!include [banner](../includes/banner.md)]

Når du oppretter et nytt fakturaforslag, kan det oppstå ytelsesproblemer etter hvert som antall prosjekter og delprosjekter øker. For å forbedre ytelsen er en funksjon tilgjengelig som reduserer tiden du trenger for å opprette et nytt fakturaforslag for posterte prosjekttransaksjoner.

## <a name="enable-project-invoice-proposal-performance-enhancement"></a>Aktiver ytelsesforbedringen for prosjektfakturaforslag
Fullfør fremgangsmåten nedenfor for å aktivere funksjonen for ytelsesforbedring av prosjektfakturaforslaget.

1.  Gå til **Funksjonsbehandling** > **Alle**. Finn **Ytelsesforbedring for prosjektfakturaforslag** i funksjonslisten.
2.  Velg **Aktiver nå**.
3.  Oppdater nettleseren, og opprett deretter et nytt fakturaforslag.

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a>Deaktiver ytelsesforbedringen for prosjektfakturaforslag
Fullfør fremgangsmåten nedenfor for å deaktivere funksjonen for ytelsesforbedring av prosjektfakturaforslaget.

1.  Gå til **Funksjonsbehandling** > **Alle**. Finn **Ytelsesforbedring for prosjektfakturaforslag** i funksjonslisten.
2.  Velg **Deaktiver**.
3.  Oppdater nettleseren din.

> [!NOTE]
> Ytelse for fakturaforslag kan ikke brukes når faktureringsregler er aktivert.
> 
> I løpet av den satsvise prosessen for å opprette fakturaforslag deler antall delaktiviteter oppgavene til et maksimumsantall basert på antall kontrakter med fakturerbare transaksjoner, uavhengig av hva du har angitt. Hvis du for eksempel angir **3** for antall delaktiviteter for oppretting av fakturaforslaget satsvis, og det bare er to kontrakter med fakturerbare transaksjoner, opprettes det bare to delaktiviteter.
