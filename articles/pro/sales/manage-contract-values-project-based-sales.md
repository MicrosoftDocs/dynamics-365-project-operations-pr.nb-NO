---
title: Oversikt over prosjektbaserte kontraktlinjer
description: Dette emnet inneholder informasjon om arbeid med prosjektbaserte kontraktlinjer.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 7da8a7f898e6f0bb46d4cf6de65812e3aabb7416a2fdf2f9d9c8bad07e77cd85
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999058"
---
# <a name="project-based-contract-lines-overview"></a>Oversikt over prosjektbaserte kontraktlinjer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Prosjektbaserte kontraktlinjer i Dynamics 365 Project Operations er utformet for å inneholde estimat- og faktureringsavtaler for bestemte komponenter av prosjektarbeid for et engasjement. Strukturen til en prosjektbasert kontraktlinje utvides for prosjektestimater og faktureringsscenarioer med følgende konsepter:

- Faktureringsmetode
- Prosjekt- og oppgavetilordning
- Inkluderte transaksjonsklasser
- Må ikke overskrides-grense
- Belastbarhets-oppsett
- Estimater ved hjelp av kontraktlinjedetaljer
- Kontraktlinjekunder

Følgende tabell inneholder feltene i kategorien **Generelt** i prosjektbaserte kontraktlinjer som hjelper deg med å sette opp grunnlaget for et detaljert grunnleggende estimat og faktureringsordninger for prosjektbasert arbeid.

| Felt | Beskrivelse | Nedstrøms påvirkning |
| --- | --- | --- |
| **Navn** | Navnet på kontraktlinjen. Dette identifiserer den separate komponenten i kontrakten som blir estimert. For en prosjektkontrakt som opprettes fra et tilbud, kopieres denne verdien fra en tilsvarende verdi av den prosjektbaserte tilbudslinjen. | Navnet som kopieres over prosjektfakturalinjen som opprettes fra denne kontraktlinjen når fakturaen opprettes. |
| **Faktureringsmetode** | På en prosjektkontrakt som opprettes fra et tilbud, kopieres denne verdien fra det tilsvarende feltet på tilbudslinjen. Dette er et alternativsett som representerer de to hovedkontraktmodellene som støttes av Project Operations:</br>- **Fast pris**</br>- **Tid og materiale** | Basert på faktureringsmetoden for den refererte kontraktlinjen blir den faktiske transaksjonen behandlet. Hvis kontraktlinjen som den faktiske verdien refererer til, har en faktureringsmetode for tid og materialer, opprettes det poster for kostnader og ufakturerte faktiske salgsverdier. Hvis kontraktlinjen som den faktiske verdien refererer til, har en faktureringsmetode for fast pris, blir bare en faktisk kostnad opprettet. |
| **Project** | Bruk dette feltet til å identifisere prosjektet som skal brukes til å levere arbeidet på dette engasjementet. | Denne verdien brukes sammen med **Inkluderte oppgaver** og **Inkluderte transaksjonsklasser** til å løse kontraktlinjereferansen for en faktisk verdi eller estimatlinjeoppføring. |
| **Inkluderte oppgaver** | Angir om denne kontraktlinjen inneholder alle prosjektoppgaver for det valgte prosjektet eller bare et delsett av oppgavene. Dette er et alternativsett som har følgende mulige verdier:</br>- **Alle prosjektoppgaver**</br>- **Bare valgte prosjektoppgaver**. En tom verdi i dette feltet er det samme som å velge **Alle prosjektoppgaver**. | Hvis **Bare valgte oppgaver** er valgt, kan du velge bestemte oppgaver og knytte dem til denne kontraktlinjen i kategorien **Faktureringsoppsett for oppgave** på siden **Prosjekt**. Verdien brukes sammen med klassene **Prosjekt** og **Inkludert transaksjon** for å løse kontraktlinjereferansen på en linjeoppføring for faktisk eller beregnet verdi. |
| **Inkluder tid** | En **Ja**/**Nei**-verdi angir om tidstransaksjoner eller arbeidskostnader for det valgte prosjektet skal tas med på denne kontraktlinjen. En **Nei**-verdi angir at tidstransaksjonene eller arbeidskostnader ikke skal tas med på denne kontraktlinjen. En **Ja**-verdi angir at de tas med. | Denne verdien brukes sammen med prosjektet for å løse kontraktlinjereferansen for en faktisk verdi eller estimatlinjeoppføring. |
| **Inkluder utgift** | En **Ja**/**Nei**-verdi angir om utgiftskostnader for det valgte prosjektet skal tas med på denne kontraktlinjen. En **Nei**-verdi angir at utgiftskostnaden ikke skal tas med på denne kontraktlinjen. En **Ja**-verdi angir at den tas med. | Denne verdien brukes sammen med prosjektet for å løse kontraktlinjereferansen for en faktisk verdi eller estimatlinjeoppføring. |
| **Inkluder materialer** | En **Ja**/**Nei**-verdi angir om materialkostnader for det valgte prosjektet skal tas med på denne kontraktlinjen. En **Nei**-verdi angir at materialkostnader ikke skal tas med på denne kontraktlinjen. En **Ja**-verdi angir at den tas med. | Denne verdien brukes sammen med prosjektet for å løse kontraktlinjereferansen for en faktisk verdi eller estimatlinjeoppføring. |
| **Inkluder gebyr** | En **Ja**/**Nei**-verdi angir om gebyrer for det valgte prosjektet skal tas med på denne kontraktlinjen. En **Nei**-verdi angir at avgiftene ikke skal tas med på denne kontraktlinjen. En **Ja**-verdi angir at de tas med. | Denne verdien brukes sammen med prosjektet for å løse kontraktlinjereferansen for en faktisk verdi eller estimatlinjeoppføring. |
| **Avtalt beløp** | På en kontraktlinje med fast pris er dette beløpet den avtalte verdien som skal faktureres til kunden for alle arbeidskomponentene som er tilknyttet denne kontraktlinjen. På en kontraktlinje for tid og materialer er dette beløpet en estimert verdi av hva som skal faktureres til kunden for alle arbeidskomponentene som er tilknyttet denne kontraktlinjen. På en prosjektkontrakt som opprettes fra et tilbud, kopieres denne verdien fra det tilsvarende feltet på tilbudslinjen. Når en prosjektbasert kontraktlinje har linjedetaljer, er dette feltet låst for redigering og oppsummeres fra beløpet på kontraktlinjedetaljene. | Når kontraktlinjen har linjedetaljer, kan denne verdien endres ved å endre beløpene i linjedetaljene. På en fastpriskontraktlinje brukes denne verdien til å generere beløpet før avgift på periodiske faktureringsmilepæler. |
| **Beregnet mva** | Brukeren kan redigere dette feltet for å angi det estimerte avgiftsbeløpet på kontraktlinjen. Når en prosjektbasert kontraktlinje har linjedetaljer, er dette feltet låst for redigering og oppsummeres fra avgiftsbeløpet på kontraktlinjedetaljene. | Når kontraktlinjen har linjedetaljer, kan denne verdien endres ved å endre avgiftsbeløpene i linjedetaljene. På en fastpriskontraktlinje brukes denne verdien til å generere avgiften på periodiske faktureringsmilepæler. |
| **Avtalt beløp etter mva** | Kontraktlinjebeløpet etter mva. Dette feltet er skrivebeskyttet og beregnes som **Avtalt beløp + avgift**. | På en fastpriskontraktlinje brukes denne verdien til å generere periodiske faktureringsmilepæler. |
| **Må ikke overskrides-grense** | Brukeren kan redigere dette feltet, og det er bare tilgjengelig i prosjektbaserte kontraktlinjer der faktureringsmetoden er satt til tid og materiale. | Brukeren kan redigere dette feltet. Når en faktisk verdi for tid og materiale refererer til denne kontraktlinjen for tid og materialer, evalueres beløpet på den faktiske verdien mot grensen som ikke må overskrides på denne kontraktlinjen. Denne evalueringen er fullført etter at de allerede brukte og beregnede beløpene er inkludert. |
| **Kundebudsjett** | Dette feltet er redigerbart og kopieres fra det tilsvarende feltet på tilbudslinjen, hvis kontrakten ble opprettet fra et tilbud. | Dette feltet brukes bare til informasjon og har ikke noen nedstrøms signifikans. |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Valideringsreglene for alternativene i kategorien Generelt for prosjektbaserte kontraktlinjer

Regel 1: Hvis feltet **Inkluderte aktiviteter** er tomt eller satt til **Alle prosjektoppgaver**, inkluderes alle oppgavene for prosjektet på kontraktlinjen.

Regel 2: Når feltet **Inkluderte oppgaver** er tomt eller eksplisitt satt til **Alle prosjektoppgaver**, kan et prosjekt og en bestemt transaksjonsklasse bare tas med på én prosjektbasert kontraktlinje i en kontrakt.

Regel 3: Når feltet **Inkluderte oppgaver** er satt til **Bare valgte prosjektoppgaver**, kan et prosjekt og en bestemt transaksjonsklasse tas med på flere prosjektbasert kontraktlinjer i en kontrakt.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p>
                    <strong>Kontrakt</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Kontraktlinje</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="67" valign="top">
                <p>
                    <strong>Inkluderte oppgaver</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Inkluder tid</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Inkluder utgift</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Inkluder materialer</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Inkluder</strong>
                </p>
                <p>
                    <strong>Gebyr</strong>
                </p>
            </td>
            <td width="53" valign="top">
                <p>
                    <strong>Gyldig / ikke gyldig</strong>
                </p>
            </td>
            <td width="250" valign="top">
                <p>
                    <strong>Årsak</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tomt </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Ikke gyldig </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Brudd på regel nr. 2. Tid, utgifter, materialer og gebyrer for P1-prosjektet er inkludert både på kontraktlinje CL1 og CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tomt </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tomt </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Ikke gyldig </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Brudd på regel nr. 2. Tid, materialer og gebyrer for P1-prosjektet er inkludert både på kontraktlinje CL1 og CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tomt </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tomt </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Gyldig </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Tid, materialer og gebyrer for P1-prosjektet er inkludert på CL1.
                </p>
                <ul>
                    <li>
Utgift i P1-prosjektet er inkludert i CL2.
                    </li>
                </ul>
                <p>
Ingen overlapping i hva som inkluderes på hver kontraktlinje, og er derfor gyldig.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tomt </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Bare valgte oppgaver </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Ikke gyldig </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Brudd på regel nr. 2 </p>
                <p>
C1 inkluderer tid, materialer, utgifter og gebyrer for et delsett med oppgaver på prosjekt P1.
                </p>
                <p>
CL2 inkluderer tid, materialer, utgifter og gebyrer for hele prosjekt P1, og overlapper derfor med det som er inkludert på C1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tomt </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Bare valgte oppgaver </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Gyldig </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
I henhold til regel nr. 3 </p>
                <p>
C1 inkluderer tid, utgifter, materialer og gebyrer for et delsett med oppgaver på prosjekt P1.
                </p>
                <p>
CL2 inkluderer tid, utgifter, materialer og gebyrer for et delsett med oppgaver på prosjekt P1.
                </p>
                <p>
Den eneste ekstra valideringen er om delsettet av oppgaver på CL1 skiller seg fra delsettet av oppgaver på CL2, for å sikre at det ikke overlapper der. Dette gjøres av systemet når oppgaver er tilknyttet.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Bare valgte oppgaver </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
