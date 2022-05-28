---
title: Konfigurere automatisk fakturaoppretting
description: Dette emnet inneholder informasjon om konfigurasjon av automatisk oppretting av proformafakturaer.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 027cc711d53c7dd8512e6ef416b54e320357dd26
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584102"
---
# <a name="set-up-automatic-invoice-creation"></a>Konfigurere automatisk fakturaoppretting 
 
_**Gjelder for:** Lite-distribusjon – avtale til proformafakturering, Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Du kan konfigurere automatisk fakturaoppretting i Dynamics 365 Project Operations. Systemet oppretter et utkast til en proformafaktura basert på fakturaplanen for hver prosjektkontrakt og kontraktlinje. Fakturaplaner konfigureres på kontraktlinjenivå. Hver linje i en kontrakt kan ha en atskilt faktureraplan, eller den samme fakturaplanen kan tas med i hver linje i kontrakten.

Når du oppretter en faktura, oppretter systemet alltid minst én faktura per prosjektkontrakt. I noen tilfeller kan det hende det opprettes flere fakturaer. Hvis for eksempel kontrakten har flere kunder, blir det samme antallet fakturaer opprettet som antall kunder som har fakturerbare transaksjoner å fakturere på den aktuelle prosjektkontrakten.

## <a name="understand-how-transactions-are-included-on-an-invoice"></a>Forstå hvordan transaksjoner tas med på en faktura 

Noen ganger angir hver prosjektbaserte kontraktlinje en separat fakturaplan. Implementeringstjenester for Adatum-kontrakten har for eksempel følgende kontraktlinjer:

- Prototypearbeid som er en fast pris med to manuelt opprettede milepæler.
- Implementeringsarbeid som inkluderer tid, og som faktureres annenhver uke på mandager.
- Påløpte utgifter som må faktureres månedlig den første mandagen i hver måned.

Fakturaplaner som er definert for hvert av disse to linjeelementene, ser ut som følgende tabell:

| Kontraktlinje | Dato for fakturakjøring | Transaksjonsfrist | Milepældato | Milepælbeløp |
| --- | --- | --- | --- | --- |
| Prototypearbeid | Mandag 5. oktober | - | Mandag 5. oktober | 5000 USD |
| - | Tirsdag 3. november | - | Tirsdag 3. november | 12,000 USD |
| Implementeringsarbeid | Mandag 5. oktober | Søndag 4. oktober | - | - |
| - | Mandag 19. oktober | Søndag 18. oktober | - | - |
| - | Mandag 2. november | Søndag 1. november | - | - |
| - | Mandag 16. november | Søndag 15. november | - | - |
| Påløpte utgifter | Mandag 5. oktober | Søndag 4. oktober | - | - |
| - | Mandag 2. november | Søndag 1. november | - | - |

I dette eksemplet når den automatiske faktureringen kjører på:

- **4. oktober eller en hvilken som helst dato før**: det genereres ingen faktura for denne kontrakten fordi tabellen **Fakturaplan** for hver av disse kontraktlinjene ikke fremhver søndag 4. oktober som en dato for fakturakjøring.
- **Mandag 5. oktober**: Én faktura genereres for:

    - Prototypearbeid som inkluderer milepælen, hvis den er merket som **klar for fakturering**.
    - Implementeringsarbeid som inneholder alle tidstransaksjoner som er opprettet før transaksjonfristen søndag 4. oktober, som er merket som **Klar for fakturering**.
    - Påløpt utgift som inneholder alle utgiftstransaksjoner som er opprettet før transaksjonfristen søndag 4. oktober, som er merket som **Klar for fakturering**.
  
- **6. oktober eller en hvilken som helst dato før 19. oktober**: Det genereres ingen faktura for denne kontrakten fordi tabellen **Fakturaplan** for hver av disse kontraktlinjene ikke fremhver 6. oktober eller en dato før 19. oktober som en dato for fakturakjøring.
- **Mandag 19. oktober**: Én faktura genereres for implementeringsarbeid som inneholder alle tidstransaksjoner som er opprettet før transaksjonfristen søndag 18. oktober, som er merket som **Klar for fakturering**.
- **Mandag 2. november**: Én faktura genereres for:

    - Implementeringsarbeid som inneholder alle tidstransaksjoner som er opprettet før transaksjonfristen søndag 1. november, som er merket som **Klar for fakturering**.
    - Påløpt utgift som inneholder alle utgiftstransaksjoner som er opprettet før transaksjonfristen søndag 1. november, som er merket som **Klar for fakturering**.

- **Tirsdag 3. november**: Én faktura genereres for prototypearbeid, som inkluderer milepælen for 12 000 USD, hvis den er merket som **Klar for fakturering**.

## <a name="configure-automatic-invoicing"></a>Konfigurer automatisk fakturering

Fullfør fremgangsmåten nedenfor for å konfigurere en automatisk fakturakjøring.

1. I **Project Operations** går du til **Innstillinger** > **Regelmessig fakturaoppsett**.
2. Opprett en satsvis jobb, og gi den navnet **Opprett fakturaer i Project Operations**. Navnet på den satsvise jobben må inneholde ordene "opprett fakturaer".
3. I **Jobbtype**-feltet velger du **Ingen**. Som standard er feltene **Daglig intervall** og **Er aktiv** satt til **Ja**.
4. Velg **Kjør arbeidsflyt**. I dialogboksen **Oppslagsoppføring** vises tre arbeidsflyter:

- ProcessRunCaller
- ProcessRunner
- UpdateRoleUtilization

5. Velg **ProcessRunCaller**, og velg deretter **Legg til**.
6. Velg **OK** i den neste dialogboksen. Arbeidsflyten **Hvile** følges av arbeidsflyten **Prosess**. 

> [!NOTE]
> Du kan også velge **ProcessRunner** i trinn 5. Når du deretter velger **OK**, etterfølges en **Prosess**-arbeidsflyt av en **Hvile**-arbeidsflyt.

Arbeidsflytene **ProcessRunCaller** og **ProcessRunner** oppretter fakturaer. **ProcessRunCaller** kaller **ProcessRunner**. **ProcessRunner** er arbeids flyten som faktisk oppretter fakturaene. Arbeidsflyten går gjennom alle kontraktslinjene som fakturaer må opprettes for, og den oppretter fakturaer for disse linjene. For å finne ut hvilke kontraktslinjer fakturaer må opprettes for, ser jobben på fakturakjøredatoer for kontraktslinjene. Hvis kontraktslinjer som tilhører én kontrakt, har samme fakturakjøringsdato, kombineres transaksjonene til én faktura som har to fakturalinjer. Hvis det ikke finnes transaksjoner for å opprette fakturaer for, hopper jobben over fakturaopprettelsen.

Når **ProcessRunner** har kjørt ferdig, kaller den **ProcessRunCaller**, angir sluttidspunktet og lukkes. **ProcessRunCaller** starter deretter en tidtaker som kjører i 24 timer, fra det angitte sluttidspunktet. Når tidtakeren er ferdig, lukkes **ProcessRunCaller**.

Den satsvise prosessjobben for oppretting av fakturaer er en gjentakende jobb. Hvis denne satsvise prosessen kjører mange ganger, opprettes flere forekomster av jobben, og dette fører til feil. Derfor bør du starte den satsvise prosessen bare én gang, og du bør bare starte den på nytt hvis den slutter å kjøre.

> [!NOTE]
> Satsvis fakturering i Project Operations kjører bare for prosjektkontraktlinjer som er konfigurert ved hjelp av fakturaplaner. En kontraktlinje med en faktureringsmetode for fast pris må ha milepæler konfigurert. Det må konfigureres en datobasert fakturaplan for en prosjektkontraktlinje med en faktureringsmetode for tid og materialer.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
