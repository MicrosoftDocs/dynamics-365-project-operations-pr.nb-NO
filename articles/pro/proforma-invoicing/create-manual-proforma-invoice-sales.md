---
title: Proforma prosjektfakturaer
description: Dette emnet inneholder informasjon om proforma prosjektfakturaer i Project Operations.
author: rumant
manager: Annbe
ms.date: 04/06/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d08e2b0422a991aa4c98ae5d1e0f60aa0eb9daa6
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867188"
---
# <a name="proforma-project-pnvoices"></a>Proforma prosjektfakturaer

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Proforma prosjektfakturering gir prosjektledere et andre godkjenningsnivå før de oppretter fakturaer for kunder. Det første godkjenningsnivået fullføres når tids,- utgifts- og materialoppføringene som prosjektteammedlemmene sender inn, godkjennes.

Dynamics 365 Project Operations Lite-distribusjonen er ikke utformet for å generere kunderettede fakturaer. Følgende liste viser hvorfor fakturaer ikke kan genereres:

- Inneholder ikke skatteinformasjon.
- Kan ikke konvertere andre valutaer til faktureringsvalutaen.
- Kan ikke formatere fakturaer korrekt for utskrift.

I stedet kan du bruke et finans- eller regnskapssystem til å opprette kunderettede fakturaer som bruker informasjonen i genererte fakturaforslag.

## <a name="creating-project-invoices"></a>Opprette prosjektfakturaer

Prosjektfakturaer kan opprettes én om gangen eller i et parti. Du kan opprette dem manuelt, eller de kan konfigureres slik at de genereres i automatiske kjøringer.

### <a name="manually-create-project-invoices"></a>Opprette prosjektfakturaer manuelt 

På listesiden **Prosjektkontrakter** kan du opprette prosjektfakturaer separat for hver prosjektkontrakt, eller du kan opprette fakturaer samlet for flere prosjektkontrakter.

   - Hvis du vil opprette en faktura for en spesifikk prosjektkontrakt, går du til listesiden **Prosjektkontrakter**, åpner en prosjektkontrakt og velger deretter **Opprett faktura**.

   Det blir generert en faktura for alle transaksjoner for den valgte prosjektkontrakten som har statusen **Klar for fakturering**. Disse transaksjonene inkluderer tid, utgifter, materiell, milepæler, produktbaserte kontraktlinjer og andre ufakturerte salgsjournallinjer som kan ha blitt bekreftet.

Slik masseoppretter du fakturaer:

1. På listesiden **Prosjektkontrakter** velger du en eller flere prosjektkontrakter du skal opprette en faktura for, og deretter velger du **Opprett prosjektfakturaer**.
2. En varselmelding informerer deg om at det kan være en forsinkelse før fakturaer opprettes. Prosessen vises også. Velg **OK** for å lukke meldingsboksen.

   Det blir generert en faktura for alle transaksjoner på en kontraktlinje som har statusen **Klar for fakturering**. Disse transaksjonene inkluderer tid, utgifter, materiell, milepæler, produktbaserte kontraktlinjer og andre ufakturerte salgsjournallinjer som kan ha blitt bekreftet.

3. Du kan vise fakturaene som er generert, ved å gå til **Salg** \> **Fakturering** \> **Fakturaer**. Du kan se én faktura for hver prosjektkontrakt.

### <a name="set-up-automated-creation-of-project-invoices"></a>Konfigurere automatisk opprettelse av prosjektfakturaer 

Følg denne fremgangsmåten for å konfigurere en automatisk fakturakjøring.

1. Gå til **Innstillinger** \> **Satvise jobber**.
2. Opprett en satsvis jobb, og gi den navnet **Opprett fakturaer i Project Operations**. Navnet på den satsvise jobben må inneholde begrepet "Opprette fakturaer".
3. I **Jobbtype**-feltet velger du **Ingen**. Som standard er **Daglig intervall** og **Er aktiv** satt til **Ja**.
4. Velg **Kjør arbeidsflyt**. I dialogboksen **Oppslagsoppføring** vises følgende arbeidsflyter:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Velg **ProcessRunCaller**, og velg deretter **Legg til**.
6. Velg **OK** i den neste dialogboksen. Arbeidsflyten **Hvile** følges av arbeidsflyten **Prosess**.

    Du kan også velge **ProcessRunner** i trinn 5. Når du deretter velger **OK**, etterfølges en **Prosess**-arbeidsflyt av en **Hvile**-arbeidsflyt.

Arbeidsflytene **ProcessRunCaller** og **ProcessRunner** oppretter fakturaer. **ProcessRunCaller** kaller **ProcessRunner**. **ProcessRunner** er arbeids flyten som oppretter fakturaene. Denne arbeidsflyten går gjennom alle kontraktlinjene som fakturaer må opprettes for, og oppretter fakturaene. For å finne ut hvilke kontraktslinjer fakturaer må opprettes for, ser arbeidsflyten på fakturakjøredatoer for kontraktslinjene. Hvis kontraktslinjer som tilhører én kontrakt, har samme fakturakjøringsdato, kombineres transaksjonene til én faktura som har to fakturalinjer. Hvis det ikke finnes transaksjoner for å opprette fakturaer for, blir det ikke opprettet fakturaer.

Når **ProcessRunner** har kjørt ferdig, kaller den **ProcessRunCaller**, angir sluttidspunktet og lukkes. **ProcessRunCaller** starter deretter en tidtaker som kjører i 24 timer, fra det angitte sluttidspunktet. Når tidtakeren er ferdig, lukkes **ProcessRunCaller**.

Den satsvise prosessjobben for oppretting av fakturaer er en gjentakende jobb. Hvis denne satsvise prosessen kjører mange ganger, opprettes flere forekomster av jobben, og dette kan føre til feil. Du kan løse dette problemet ved å starte den satsvise prosessen bare én gang, og bare starte den på nytt hvis den slutter å kjøre.

> [!NOTE]
> Satsvis fakturering kjører bare for prosjektkontraktlinjer som er konfigurert ved hjelp av fakturaplaner. En kontraktlinje med en faktureringsmetode for fast pris må ha milepæler konfigurert. Det må konfigureres en datobasert fakturaplan for en prosjektkontraktlinje med en faktureringsmetode for tid og materialer. Det samme gjelder for en prosjektbasert kontraktlinje.      
 
### <a name="edit-a-draft-invoice"></a>Redigere et fakturautkast

Når du oppretter et fakturautkast for et prosjekt, trekkes alle ikke-fakturerte salgstransaksjoner som ble opprettet da tids- og utgiftsoppføringene ble godkjent, til fakturaen. Du kan foreta følgende justeringer mens fakturaen fremdeles er i en utkastfase:

- Slette eller redigere fakturalinjedetaljer.
- Redigere og justere antallet og faktureringstypen.
- Legge til tid, utgifter, materialer og avgifter direkte som transaksjoner på fakturaen. Du kan bruke denne funksjonen hvis fakturalinjen er tilordnet til en kontraktslinje som tillater disse transaksjonsklassene.

Velg **Bekreft** for å bekrefte en faktura. Denne handlingen er en énveishandling. Når du velger **Bekreft**, blir fakturaen skrivebeskyttet, og det opprettes faktiske verdier for fakturert salg fra hver fakturalinjedetalj for hver fakturalinje. Hvis fakturalinjedetaljene refererer til en faktisk salgsordre, blir den ufakturerte faktiske salgsverdien tilbakeført. Alle fakturalinjedetaljer som er opprettet fra en tids-, utgifts- eller materialbrukoppføring, refererer til en ufakturert faktisk salgsverdi. Finansintegreringssystemer kan bruke denne reverseringen for å reversere pågående prosjektarbeid (WIP) for regnskapsformål.

### <a name="correct-a-confirmed-invoice"></a>Korrigere en bekreftet faktura

Bekreftede fakturaer kan redigeres. Når du korrigerer en bekreftet faktura, opprettes det et nytt korrigert fakturautkast. Fordi det antas at du vil tilbakeføre alle transaksjonene og antallene fra den opprinnelige fakturaen, inneholder denne korrigerte fakturaen alle transaksjonene fra den opprinnelige fakturaen, og alle antallene i den er null.

Hvis det er transaksjoner som ikke krever rettelser, kan du fjerne dem fra det korrigerte fakturautkastet. Hvis du vil tilbakeføre eller bare returnere et delvis antall, kan du redigere **Antall**-feltet i linjedetaljene. Hvis du åpner fakturalinjedetaljene, kan du se det opprinnelige fakturaantallet. Du kan deretter redigere det gjeldende fakturaantallet slik at det blir mindre enn eller større enn det opprinnelige fakturaantallet.

Når du bekrefter en korrigert faktura, tilbakeføres det opprinnelige faktiske fakturerte salget, og et nytt faktisk fakturert salg opprettes. Hvis antallet ble redusert, vil forskjellen føre til at et nytt, ikke-fakturert faktisk salg opprettes. Hvis det opprinnelige fakturerte salget for eksempel var på åtte timer, og den korrigerte fakturalinjedetaljen har et redusert antall på seks timer, tilbakeføres den opprinnelige, fakturerte salgslinjen, og det opprettes to nye faktiske verdier:

- Et fakturert faktisk salg på seks timer.
- Et ikke-fakturert faktisk salg for de resterende to timene. Denne transaksjonen kan faktureres senere eller merkes som ikke-belastbar, avhengig av forhandlingene med kunden.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
