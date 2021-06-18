---
title: Proformafakturaer
description: Dette emnet inneholder informasjon om proformafakturaer i Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3eaf2f19506c5464c302176fc620aad5f29b4ae7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000673"
---
# <a name="proforma-invoices"></a>Proformafakturaer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Proformafakturering gir prosjektledere et andre godkjenningsnivå før de oppretter fakturaer for kunder. Det første godkjenningsnivået fullføres når tids,- utgifts- og materialoppføringene som prosjektteammedlemmene sender inn, godkjennes. Bekreftede proformafakturaer er tilgjengelige i Prosjektregnskap-modulen i Project Operations. Prosjektregnskapsførere kan utføre flere oppdateringer, for eksempel oppsett av salgsavgifter, regnskap og fakturaer.


## <a name="creating-project-invoices"></a>Opprette prosjektfakturaer

Prosjektfakturaer kan opprettes én om gangen eller i et parti. Du kan opprette dem manuelt, eller de kan konfigureres slik at de genereres i automatiske kjøringer.

### <a name="manually-create-project-invoices"></a>Opprette prosjektfakturaer manuelt 

Fra listesiden **Prosjektkontrakter** kan du opprette prosjektfakturaer separat for hver prosjektkontrakt, eller du kan opprette fakturaer samlet for flere prosjektkontrakter.

Følg dette trinnet for å opprette en faktura for en bestemt prosjektkontrakt.

- Åpne en prosjektkontrakt på listesiden **Prosjektkontrakter**, og velg deretter **Opprett faktura**.

    Det blir generert en faktura for alle transaksjoner for den valgte prosjektkontrakten som har statusen **Klar for fakturering**. Disse transaksjonene inkluderer tid, utgifter, materialer, milepæler og andre ufakturerte salgsjournallinjer.

Følg disse trinnene for å opprette fakturaer samlet.

1. På listesiden **Prosjektkontrakter** velger du en eller flere prosjektkontrakter du må opprette en faktura for, og deretter velger du **Opprett prosjektfakturaer**.

    En varselmelding informerer deg om at det kan være en forsinkelse før fakturaer opprettes. Prosessen vises også.

2. Velg **OK** for å lukke meldingsboksen.

    Det blir generert en faktura for alle transaksjoner på en kontraktlinje som har statusen **Klar for fakturering**. Disse transaksjonene inkluderer tid, utgifter, materialer, milepæler og andre ufakturerte salgsjournallinjer.

3. Hvis du vil vise fakturaene som er generert, går du til **Salg** \> **Fakturering** \> **Fakturaer**. Du kan se én faktura for hver prosjektkontrakt.

### <a name="set-up-automated-creation-of-project-invoices"></a>Konfigurere automatisk opprettelse av prosjektfakturaer 

Følg denne fremgangsmåten for å konfigurere en automatisk fakturakjøring.

1. Gå til **Innstillinger** \> **Satvise jobber**.
2. Opprett en satsvis jobb, og gi den navnet **Opprett fakturaer i Project Operations**. Navnet på den satsvise jobben må inneholde begrepet "Opprette fakturaer".
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
 
### <a name="edit-a-draft-invoice"></a>Redigere et fakturautkast

Når du oppretter et fakturautkast for et prosjekt, trekkes alle ikke-fakturerte salgstransaksjoner som ble opprettet da tids-, utgifts- og materialbruksoppføringene ble godkjent, til fakturaen. Du kan foreta følgende justeringer mens fakturaen fremdeles er i en utkastfase:

- Slette eller redigere fakturalinjedetaljer.
- Redigere og justere antallet og faktureringstypen.

Velg **Bekreft** for å bekrefte en faktura. Bekreftelseshandlingen er en énveishandling. Når du velger **Bekreft**, blir fakturaen skrivebeskyttet, og det opprettes faktiske verdier for fakturert salg fra hver fakturalinjedetalj for hver fakturalinje. Hvis fakturalinjedetaljene refererer til en faktisk salgsordre, tilbakefører systemet også faktisk fakturert salg. (Alle fakturalinjedetaljer som ble opprettet fra en tids- eller utgiftsoppføring, vil referere til et ikke-fakturert salg.) Integrasjonssystemer for hovedboken kan bruke denne tilbakeføringen til å tilbakeføre prosjektarbeid som pågår, for regnskapsformål.

### <a name="correct-a-confirmed-invoice"></a>Korrigere en bekreftet faktura

Bekreftede fakturaer kan redigeres (korrigeres). Når du korrigerer en bekreftet faktura, opprettes det et nytt korrigert fakturautkast. Fordi det antas at du vil tilbakeføre alle transaksjonene og antallene fra den opprinnelige fakturaen, inneholder denne korrigerte fakturaen alle transaksjonene fra den opprinnelige fakturaen, og alle antallene i den er 0 (null).

Hvis noen av transaksjonene ikke krever rettelser, kan du fjerne dem fra det korrigerte fakturautkastet. Hvis du vil tilbakeføre eller bare returnere et delvis antall, kan du redigere **Antall**-feltet i linjedetaljene. Hvis du åpner fakturalinjedetaljene, kan du se det opprinnelige fakturaantallet. Du kan deretter redigere det gjeldende fakturaantallet slik at det blir mindre enn eller større enn det opprinnelige fakturaantallet.

Når du bekrefter en korrigert faktura, tilbakeføres det opprinnelige faktiske fakturerte salget, og et nytt faktisk fakturert salg opprettes. Hvis antallet ble redusert, vil forskjellen føre til at et nytt, ikke-fakturert faktisk salg også opprettes. Hvis det opprinnelige fakturerte salget for eksempel var på åtte timer, og den korrigerte fakturalinjedetaljen har et redusert antall på seks timer, tilbakeføres den opprinnelige, fakturerte salgslinjen, og det opprettes to nye faktiske verdier:

- Et fakturert faktisk salg på seks timer.
- Et ikke-fakturert faktisk salg for de resterende to timene. Denne transaksjonen kan enten faktureres senere eller merkes som ikke-belastbar, avhengig av forhandlingene med kunden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
