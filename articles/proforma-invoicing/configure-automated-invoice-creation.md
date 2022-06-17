---
title: Konfigurere automatisk fakturaoppretting
description: Denne artikkelen inneholder informasjon om hvordan du konfigurerer systemet for å generere fakturaer automatisk.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 273e00e7841c8a34e249e54a7d868034bc34a1f7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920624"
---
# <a name="configure-automatic-invoice-creation"></a>Konfigurere automatisk fakturaoppretting

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_


Fullfør fremgangsmåten nedenfor for å konfigurere en automatisk fakturakjøring i Dynamics 365 Project Operations.

1. Gå til **Innstillinger** > **Satvise jobber**.
2. Opprett en satsvis jobb, og gi den navnet **Opprett fakturaer i Project Operations**. Navnet på den satsvise jobben må inneholde ordene "opprett fakturaer".
3. I **Jobbtype**-feltet velger du **Ingen**. Som standard er **Daglig intervall** og **Er aktiv** satt til **Ja**.
4. Velg **Kjør arbeidsflyt**. I dialogboksen **Oppslagsoppføring** vises tre arbeidsflyter:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Velg **ProcessRunCaller**, og velg deretter **Legg til**.
6. Velg **OK** i den neste dialogboksen. Arbeidsflyten **Hvile** følges av arbeidsflyten **Prosess**.

  > [!NOTE]
  > Du kan også velge **ProcessRunner** i trinn 5. Når du deretter velger **OK**, etterfølges en **Prosess**-arbeidsflyt av en **Hvile**-arbeidsflyt.

Arbeidsflytene **ProcessRunCaller** og **ProcessRunner** oppretter fakturaer. **ProcessRunCaller** kaller **ProcessRunner**. **ProcessRunner** er arbeids flyten som faktisk oppretter fakturaene. Det går gjennom alle kontraktslinjene som fakturaer må opprettes for, og det opprettes fakturaer for disse linjene. For å finne ut hvilke kontraktslinjer fakturaer må opprettes for, ser jobben på fakturakjøredatoer for kontraktslinjene. Hvis kontraktslinjer som tilhører én kontrakt, har samme fakturakjøringsdato, kombineres transaksjonene til én faktura som har to fakturalinjer. Hvis det ikke finnes transaksjoner for å opprette fakturaer for, hopper jobben over fakturaopprettelsen.

Når **ProcessRunner** har kjørt ferdig, kaller den **ProcessRunCaller**, angir sluttidspunktet og lukkes. **ProcessRunCaller** starter deretter en tidtaker som kjører i 24 timer, fra det angitte sluttidspunktet. Når tidtakeren er ferdig, lukkes **ProcessRunCaller**.

Den satsvise prosessjobben for oppretting av fakturaer er en gjentakende jobb. Hvis denne satsvise prosessen kjører mange ganger, opprettes flere forekomster av jobben, og det fører til feil. Derfor bør du starte den satsvise prosessen bare én gang, og du bør bare starte den på nytt hvis den slutter å kjøre.

> [!NOTE]
> Satsvis fakturering kjører bare for prosjektkontraktlinjer som er konfigurert ved hjelp av fakturaplaner. En kontraktlinje med en faktureringsmetode for fast pris må ha milepæler konfigurert. Det må konfigureres en datobasert fakturaplan for en prosjektkontraktlinje med en faktureringsmetode for tid og materialer. Det samme gjelder for en prosjektbasert kontraktlinje.     


[!INCLUDE[footer-include](../includes/footer-banner.md)]