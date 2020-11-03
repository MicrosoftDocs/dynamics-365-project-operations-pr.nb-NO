---
title: Konfigurere automatisk fakturaoppretting
description: Dette emnet gir informasjon om hvordan du konfigurerer systemet til å generere fakturaer automatisk.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4e7572f2bc6201960ac01ce521adf39ac2577dbe
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081513"
---
# <a name="configure-automatic-invoice-creation"></a>Konfigurere automatisk fakturaoppretting

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_


Fullfør fremgangsmåten nedenfor for å konfigurere en automatisk fakturakjøring i Dynamics 365 Project Operations.

1. Gå til **Innstillinger** > **Satvise jobber**.
2. Opprett en satsvis jobb, og gi den navnet **Opprett fakturaer i Project Operations**. Navnet på den satsvise jobben må inneholde ordene "opprett fakturaer".
3. I **Jobbtype** -feltet velger du **Ingen**. Som standard er **Daglig intervall** og **Er aktiv** satt til **Ja**.
4. Velg **Kjør arbeidsflyt**. I dialogboksen **Oppslagsoppføring** vises tre arbeidsflyter:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Velg **ProcessRunCaller** , og velg deretter **Legg til**.
6. Velg **OK** i den neste dialogboksen. Arbeidsflyten **Hvile** følges av arbeidsflyten **Prosess**.

  > [!NOTE]
  > Du kan også velge **ProcessRunner** i trinn 5. Når du deretter velger **OK** , etterfølges en **Prosess** -arbeidsflyt av en **Hvile** -arbeidsflyt.

Arbeidsflytene **ProcessRunCaller** og **ProcessRunner** oppretter fakturaer. **ProcessRunCaller** kaller **ProcessRunner**. **ProcessRunner** er arbeids flyten som faktisk oppretter fakturaene. Det går gjennom alle kontraktslinjene som fakturaer må opprettes for, og det opprettes fakturaer for disse linjene. For å finne ut hvilke kontraktslinjer fakturaer må opprettes for, ser jobben på fakturakjøredatoer for kontraktslinjene. Hvis kontraktslinjer som tilhører én kontrakt, har samme fakturakjøringsdato, kombineres transaksjonene til én faktura som har to fakturalinjer. Hvis det ikke finnes transaksjoner for å opprette fakturaer for, hopper jobben over fakturaopprettelsen.

Når **ProcessRunner** har kjørt ferdig, kaller den **ProcessRunCaller** , angir sluttidspunktet og lukkes. **ProcessRunCaller** starter deretter en tidtaker som kjører i 24 timer, fra det angitte sluttidspunktet. Når tidtakeren er ferdig, lukkes **ProcessRunCaller**.

Den satsvise prosessjobben for oppretting av fakturaer er en gjentakende jobb. Hvis denne satsvise prosessen kjører mange ganger, opprettes flere forekomster av jobben, og det fører til feil. Derfor bør du starte den satsvise prosessen bare én gang, og du bør bare starte den på nytt hvis den slutter å kjøre.

> [!NOTE]
> Satsvis fakturering kjører bare for prosjektkontraktlinjer som er konfigurert ved hjelp av fakturaplaner. En kontraktlinje med en faktureringsmetode for fast pris må ha milepæler konfigurert. Det må konfigureres en datobasert fakturaplan for en prosjektkontraktlinje med en faktureringsmetode for tid og materialer. Det samme gjelder for en prosjektbasert kontraktlinje.     
