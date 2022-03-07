---
title: Fakturering i Project Service Automation
description: Dette emnet inneholder informasjon om fakturering.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 58259c05939cfe870ce5e36b4a0221cd93b8e8d2b4be582efc9167e82579699e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985513"
---
# <a name="invoicing-in-project-service-automation"></a>Fakturering i Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Fakturering i Dynamics 365 Project Service Automation er nyttig fordi det gir prosjektledere et andre godkjenningsnivå før de oppretter fakturaer for kunder. Det første godkjenningsnivået fullføres når tids- og utgiftsoppføringene som prosjektteammedlemmene sender inn, godkjennes.

PSA er ikke utviklet for å generere kunderettede fakturaer av følgende årsaker:

- Det inneholder ikke skatteinformasjon.
- Det kan ikke konvertere andre valutaer til faktureringsvalutaen ved hjelp av riktig konfigurerte valutakurser.
- Den kan ikke formatere fakturaer riktig slik at de kan skrives ut.

I stedet kan du bruke et finans- eller regnskapssystem til å opprette kunderettede fakturaer som bruker informasjonen fra fakturaforslag som er generert i PSA.

## <a name="creating-project-invoices-in-psa"></a>Opprett prosjektfakturaer i PSA

Prosjektfakturaer kan opprettes én om gangen eller i et parti. Du kan opprette dem manuelt, eller de kan konfigureres slik at de genereres i automatiske kjøringer.

### <a name="manually-create-project-invoices-in-psa"></a>Opprette prosjektfakturaer manuelt i PSA

Fra listesiden **Prosjektkontrakter** kan du opprette prosjektfakturaer separat for hver prosjektkontrakt, eller du kan opprette fakturaer samlet for flere prosjektkontrakter.

Følg dette trinnet for å opprette en faktura for en bestemt prosjektkontrakt.

- Åpne en prosjektkontrakt på listesiden **Prosjektkontrakter**, og velg deretter **Opprett faktura**.

    ![Opprette prosjektfakturaer for en bestemt prosjektkontrakt.](media/CreateProjectInvoicesOneByOne.png)

    Det blir generert en faktura for alle transaksjoner for den valgte prosjektkontrakten som har statusen **Klar for fakturering**. Disse transaksjonene inkluderer tid, utgifter, milepæler og produktbaserte kontraktlinjer.

Følg disse trinnene for å opprette fakturaer samlet.

1. På listesiden **Prosjektkontrakter** velger du en eller flere prosjektkontrakter du må opprette en faktura for, og deretter velger du **Opprett prosjektfakturaer**.

    ![Opprette prosjektfakturaer samlet.](media/CreateProjectInvoicesBulk.png)

    En varselmelding informerer deg om at det kan være en forsinkelse før fakturaer opprettes. Prosessen vises også.

2. Velg **OK** for å lukke meldingsboksen.

    Det blir generert en faktura for alle transaksjoner på en kontraktlinje som har statusen **Klar for fakturering**. Disse transaksjonene inkluderer tid, utgifter, milepæler og produktbaserte kontraktlinjer.

3. Hvis du vil vise fakturaene som er generert, går du til **Salg** \> **Fakturering** \> **Fakturaer**. Du kan se én faktura for hver prosjektkontrakt.

### <a name="set-up-automated-creation-of-project-invoices-in-psa"></a>Konfigurere automatisk opprettelse av prosjektfakturaer i PSA

Følg denne fremgangsmåten for å konfigurere en automatisk fakturakjøring i PSA.

1. Gå til **Project Service** \> **Innstillinger** \> **Satsvise jobber**.
2. Opprett en satsvis jobb, og gi den navnet **Opprette fakturaer i PSA**. Navnet på den satsvise jobben må inneholde begrepet "Opprette fakturaer".
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
> Satsvis fakturering i Project Service Automation kjører bare for prosjektkontraktlinjer som konfigureres ved hjelp av fakturaplaner. En kontraktlinje med en faktureringsmetode for fast pris må ha milepæler konfigurert. Det må konfigureres en datobasert fakturaplan for en prosjektkontraktlinje med en faktureringsmetode for tid og materialer. Informasjon om hvordan du angir faktureringsfrekvenser i konteksten for et prosjekt som er basert på en tilbudslinje, finnes i emnet [Tilbud og tilbudslinjer](basic-quote-lines.md#invoice-schedule). Det samme gjelder for en prosjektbasert kontraktlinje.      
 
### <a name="edit-a-draft-psa-invoice"></a>Redigere et PSA-fakturautkast

Når du oppretter et fakturautkast for et prosjekt, trekkes alle ikke-fakturerte salgstransaksjoner som ble opprettet da tids- og utgiftsoppføringene ble godkjent, til fakturaen. Du kan foreta følgende justeringer mens fakturaen fremdeles er i en utkastfase:

- Slette eller redigere fakturalinjedetaljer.
- Redigere og justere antallet og faktureringstypen.
- Legge til tid, utgifter og avgifter direkte som transaksjoner på fakturaen. Du kan bruke denne funksjonen hvis fakturalinjen er tilordnet til en kontraktslinje som tillater disse transaksjonsklassene.

Velg **Bekreft** for å bekrefte en faktura. Bekreftelseshandlingen er en énveishandling. Når du velger **Bekreft**, blir fakturaen skrivebeskyttet, og det opprettes faktiske verdier for fakturert salg fra hver fakturalinjedetalj for hver fakturalinje. Hvis fakturalinjedetaljene refererer til en faktisk salgsordre, tilbakefører systemet også faktisk fakturert salg. (Alle fakturalinjedetaljer som ble opprettet fra en tids- eller utgiftsoppføring, vil referere til et ikke-fakturert salg.) Integrasjonssystemer for hovedboken kan bruke denne tilbakeføringen til å tilbakeføre prosjektarbeid som pågår, for regnskapsformål.

### <a name="correct-a-confirmed-psa-invoice"></a>Korrigere en bekreftet PSA-faktura

Bekreftede PSA-fakturaer kan redigeres (korrigeres). Når du korrigerer en bekreftet faktura, opprettes det et nytt korrigert fakturautkast. Fordi det antas at du vil tilbakeføre alle transaksjonene og antallene fra den opprinnelige fakturaen, inneholder denne korrigerte fakturaen alle transaksjonene fra den opprinnelige fakturaen, og alle antallene i den er 0 (null).

Hvis noen av transaksjonene ikke krever rettelser, kan du fjerne dem fra det korrigerte fakturautkastet. Hvis du vil tilbakeføre eller bare returnere et delvis antall, kan du redigere **Antall**-feltet i linjedetaljene. Hvis du åpner fakturalinjedetaljene, kan du se det opprinnelige fakturaantallet. Du kan deretter redigere det gjeldende fakturaantallet slik at det blir mindre enn eller større enn det opprinnelige fakturaantallet.

Når du bekrefter en korrigert faktura, tilbakeføres det opprinnelige faktiske fakturerte salget, og et nytt faktisk fakturert salg opprettes. Hvis antallet ble redusert, vil forskjellen føre til at et nytt, ikke-fakturert faktisk salg også opprettes. Hvis det opprinnelige fakturerte salget for eksempel var på åtte timer, og den korrigerte fakturalinjedetaljen har et redusert antall på seks timer, tilbakefører PSA den opprinnelige, fakturerte salgs linjen, og det opprettes to nye faktiske verdier:

- Et fakturert faktisk salg på seks timer.
- Et ikke-fakturert faktisk salg for de resterende to timene. Denne transaksjonen kan enten faktureres senere eller merkes som ikke-belastbar, avhengig av forhandlingene med kunden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]