---
title: Konfigurere en automatisk fakturaoppretting
description: Dette emnet gir informasjon om hvordan du konfigurerer systemet til å generere fakturaer automatisk.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898138"
---
# <a name="configure-automated-invoice-creation"></a>Konfigurere en automatisk fakturaoppretting

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Fullfør fremgangsmåten nedenfor for å konfigurere en automatisk fakturakjøring i Project Operations.

1. Gå til **Innstillinger** \> **Satvise jobber**.
2. Opprett en satsvis jobb, og gi den navnet **Opprett fakturaer i Project Operations**. Navnet på den satsvise jobben må inneholde begrepet "opprette fakturaer".
3. I **Jobbtype**-feltet velger du **Ingen**. Som standard er **Daglig intervall** og **Er aktiv** satt til **Ja**.
4. Velg **Kjør arbeidsflyt**. I dialogboksen **Oppslagsoppføring** vises tre arbeidsflyter:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Velg **ProcessRunCaller**, og velg deretter **Legg til**.
6. Velg **OK** i den neste dialogboksen. Arbeidsflyten **Hvile** følges av arbeidsflyten **Prosess**.

    Du kan også velge **ProcessRunner** i trinn 5. Når du deretter velger **OK**, etterfølges en **Prosess**-arbeidsflyt av en **Hvile**-arbeidsflyt.

Arbeidsflytene **ProcessRunCaller** og **ProcessRunner** oppretter fakturaer. **ProcessRunCaller** kaller **ProcessRunner**. **ProcessRunner** er arbeids flyten som faktisk oppretter fakturaene. Det går gjennom alle kontraktslinjene som fakturaer må opprettes for, og det opprettes fakturaer for disse linjene. For å finne ut hvilke kontraktslinjer fakturaer må opprettes for, ser jobben på fakturakjøredatoer for kontraktslinjene. Hvis kontraktslinjer som tilhører én kontrakt, har samme fakturakjøringsdato, kombineres transaksjonene til én faktura som har to fakturalinjer. Hvis det ikke finnes transaksjoner for å opprette fakturaer for, hopper jobben over fakturaopprettelsen.

Når **ProcessRunner** har kjørt ferdig, kaller den **ProcessRunCaller**, angir sluttidspunktet og lukkes. **ProcessRunCaller** starter deretter en tidtaker som kjører i 24 timer, fra det angitte sluttidspunktet. Når tidtakeren er ferdig, lukkes **ProcessRunCaller**.

Den satsvise prosessjobben for oppretting av fakturaer er en gjentakende jobb. Hvis denne satsvise prosessen kjører mange ganger, opprettes flere forekomster av jobben, og det fører til feil. Derfor bør du starte den satsvise prosessen bare én gang, og du bør bare starte den på nytt hvis den slutter å kjøre.

> [!NOTE]
> Satsvis fakturering kjører bare for prosjektkontraktlinjer som er konfigurert ved hjelp av fakturaplaner. En kontraktlinje med en faktureringsmetode for fast pris må ha milepæler konfigurert. Det må konfigureres en datobasert fakturaplan for en prosjektkontraktlinje med en faktureringsmetode for tid og materialer. Det samme gjelder for en prosjektbasert kontraktlinje.     
