---
title: Oversikt over prosjekttilbudslinjer
description: Denne artikkelen inneholder informasjon om hvordan du bruker prosjektbaserte tilbudslinjer til prosjektarbeid.
author: rumant
ms.date: 03/30/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e6a67b5c37508085c9ec3d8385eaa6828536de00
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825671"
---
# <a name="project-quote-lines-overview"></a>Oversikt over prosjekttilbudslinjer 

_**Gjelder for:** Lite-distribusjon – avtale til proformafakturering, Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Prosjektbaserte tilbudslinjer er utformet for å bidra til å estimere prosjektarbeidet på et engasjement. Strukturen i en prosjektbasert tilbudslinje utvides for prosjektestimater med følgende konsepter:

- Faktureringsmetode
- Prosjekt- og oppgavetilordning
- Inkluderte transaksjonsklasser
- Må ikke overskrides-grense
- Belastbarhets-oppsett
- Estimering ved hjelp av tilbudslinjedetaljer
- Kunder for tilbudslinje

Tabellen nedenfor inneholder informasjon om feltene i kategorien **Generelt** på prosjektbaserte tilbudslinjer. Disse feltene bidrar til å definere grunnlaget for en detaljert grunnberegning for prosjektarbeid.

| **Felt** | **Beskrivelse** | **Nedstrøms påvirkning** |
| --- | --- | --- |
| Navn | Navnet på tilbudslinjen som gjør det enklere å identifisere den diskrete komponenten i tilbudet som blir beregnet. | Kopiert til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet. |
| Faktureringsmetode | På et tilbud som er opprettet fra en salgsmulighet, kopieres denne verdien fra det tilsvarende feltet på salgsmulighetslinjen. Dette feltet omfatter de to hovedkontraktsmodellene som støttes av Dynamics 365 Project Operations:</br>- Fast pris</br>- Tid og materiale.| Denne verdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet blir vunnet. |
| Project | Bruk dette valgfrie feltet til å identifisere prosjektet som skal brukes til å levere arbeidet med dette engasjementet. Når et prosjekt tilordnes til en tilbudslinje, hjelper det med å definere belastbare oppgaver og også med å hente inn et prosjektbasert estimat til tilbudslinjen som tilbudslinjedetaljer. Når et prosjekt ikke er tilordnet til en prosjektbasert tilbudslinje, bør estimatet opprettes manuelt ved å opprette hver tilbudslinjedetalj. | Denne verdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet blir vunnet.|
| Inkluderte oppgaver | Angir om denne tilbudslinjen brukes til alle eller noen av prosjektoppgavene for det valgte prosjektet. Dette feltet har følgende mulige verdier:</br>- Alle prosjektoppgaver</br>- Bare valgte prosjektoppgaver</br>En tom verdi i dette feltet tilsvarer alternativet **Alle prosjektoppgaver**. | Når **Bare valgte prosjektoppgaver** velges på prosjektsiden, kan du på fanen **Faktureringsoppsett for oppgave** velge spesifikke oppgaver og tilordne dem til denne tilbudslinjen. Denne verdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet blir vunnet. |
| Inkluder tid | En **Ja**/**Nei**-verdi angir om tidstransaksjoner eller arbeidskostnader for det valgte prosjektet skal tas med i estimatet på denne tilbudstlinjen. Verdien **Nei** angir at tidstransaksjoner eller lønnskostnader ikke inkluderes i estimatet på denne tilbudslinjen. Verdien **Ja** angir at tidstransaksjoner eller lønnskostnader inkluderes i estimatet på denne tilbudslinjen. | Denne verdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet blir vunnet. |
| Inkluder utgift | En **Ja**/**Nei**-verdi angir om utgiftskostnader for det valgte prosjektet skal tas med i estimatet på denne tilbudslinjen. Verdien **Nei** angir at utgiftskostnader ikke inkluderes i estimatet på denne tilbudslinjen. Verdien **Ja** angir at utgiftskostnader inkluderes i estimatet på denne tilbudslinjen. | Denne verdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet blir vunnet. |
| Inkluder materiale | En **Ja**/**Nei**-verdi angir om materialkostnader for det valgte prosjektet skal tas med i estimatet på denne tilbudslinjen. En **Nei**-verdi angir at materialkostnader ikke skal tas med i estimatet på denne tilbudslinjen. En **Ja**-verdi angir at materialkostnader skal tas med i estimatet på denne tilbudslinjen. | Denne verdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet blir vunnet. |
| Inkluder gebyr | En **Ja**/**Nei**-verdi angir om gebyrer for det valgte prosjektet skal tas med i estimatet på denne tilbudslinjen. Verdien **Nei** angir at gebyrer ikke inkluderes i estimatet på denne tilbudslinjen. Verdien **Ja** angir at gebyrer inkluderes i estimatet på denne tilbudslinjen. | Denne verdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet blir vunnet. |
| Tilbudsbeløp | Dette er beløpet som blir tilbudt kunden for alt arbeidet som beregnes på denne prosjektbaserte tilbudslinjen. På et tilbud som er opprettet fra en salgsmulighet, kopieres denne verdien fra feltet **Kundebudsjett** på salgsmulighetslinjen. Når den prosjektbaserte tilbudslinjen har linjedetaljer, er dette feltet låst for redigering og summeres fra beløpet i tilbudslinjedetaljene. | Denne verdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet blir vunnet. |
| Beregnet mva | Dette er et redigerbart felt for brukeren å legge til det estimerte mva-beløpet på tilbudslinjen. Når en prosjektbasert tilbudslinje har linjedetaljer, er dette feltet låst for redigering og summeres fra avgiftsbeløpet i tilbudslinjedetaljene. | Denne verdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet blir vunnet. |
| Tilbudsbeløp etter mva | Dette feltet er tilbudslinjebeløpet etter mva og er skrivebeskyttet. Beløpet i dette feltet beregnes som *Oppgitt beløp + mva*. | Denne verdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet blir vunnet. |
| Må ikke overskrides-grense | Dette feltet kan redigeres og er bare tilgjengelig på prosjektbaserte tilbudslinjer som har faktureringsmetoden **Tid og materialer**. | Denne verdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet blir vunnet. |
| Kundebudsjett | Feltet kan redigeres, og det kopieres fra det tilsvarende feltet på salgsmulighetslinjen hvis tilbudet ble opprettet fra en salgsmulighet. | Denne verdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet blir vunnet. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Valideringsregler for felt i kategorien Generelt på prosjektbaserte tilbudslinjer

**Regel 1**: Hvis feltet **Inkluderte oppgaver** er tomt, eller hvis det er satt til **Alle prosjektoppgaver**, inkluderes et prosjekt på tilbudslinjen.

**Regel 2**: Hvis feltet **Inkluderte oppgaver** er tomt, eller hvis det er satt til **Alle prosjektoppgaver**, kan et prosjekt og en bestemt transaksjonsklasse bare inkluderes på én prosjektbasert tilbudslinje i et tilbud.

**Regel 3**: Hvis feltet **Inkluderte oppgaver** er satt til **Bare valgte prosjektoppgaver**, kan et prosjekt og en bestemt transaksjonsklasse inkluderes på flere prosjektbaserte tilbudslinjer i et tilbud.

**Regel 4**: Hvis en salgsmulighet har flere tilbud, kan det finnes tilbudslinjer fra forskjellige tilbud som alle refererer til samme prosjekt og inkluderer samme transaksjonsklasse.

**Regel 5**: Hvis tilbudene ikke tilhører samme salgsmulighet, kan de ikke inneholde samme prosjekt- og transaksjonsklasse.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p>
                    <strong>Salgsmulighet</strong>
                </p>
            </td>
            <td width="39" valign="top">
                <p>
                    <strong>Tilbud</strong>
                </p>
            </td>
            <td width="40" valign="top">
                <p>
                    <strong>Tilbudslinje</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="77" valign="top">
                <p>
                    <strong>Inkluderte oppgaver</strong>
                </p>
            </td>
            <td width="45" valign="top">
                <p>
                    <strong>Inkluder tid</strong>
                </p>
            </td>
            <td width="46" valign="top">
                <p>
                    <strong>Inkluder utgift</strong>
                </p>
            </td>
            <td width="43" valign="top">
                <p>
                    <strong>Inkluder materiale</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Inkluder</strong>
                </p>
                <p>
                    <strong>Gebyr</strong>
                </p>
            </td>
            <td width="49" valign="top">
                <p>
                    <strong>Gyldig / ikke gyldig</strong>
                </p>
            </td>
            <td width="200" valign="top">
                <p>
                    <strong>Årsak</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. kvartal </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tomt </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Ikke gyldig </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Brudd på regel nr. 2. Tid, utgift og gebyrer i P1-prosjektet er inkludert på tilbudslinjene QL1 og QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. kvartal </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tomt </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. kvartal </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tomt </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Ikke gyldig </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Brudd på regel nr. 2. Tid, materiale og gebyrer i P1-prosjektet er inkludert på tilbudslinjene QL1 og QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. kvartal </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tomt </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. kvartal </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tomt </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Gyldig </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Tid, materiale og gebyrer for P1-prosjektet er inkludert på QL1 <br>
Utgift i P1-prosjektet er inkludert i QL2 <br>
Ingen overlapping i hva som inkluderes på hver tilbudslinje, og er derfor gyldig.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. kvartal </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tomt </p>
            </td>
            <td width="45" valign="top">
                <p>
No </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
No </p>
            </td>
            <td width="41" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. kvartal </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Bare valgte oppgaver </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Ikke gyldig </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Brudd på regel nr. 2 </p>
                <p>
Q1 inkluderer tid, materiale, utgifter og gebyrer for et delsett med oppgaver på prosjekt P1 </p>
                <p>
QL2 inkluderer tid, utgifter og gebyrer for hele prosjektet P1 og derfor overlapper med hva som inkluderes på Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. kvartal </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tomt </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. kvartal </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Bare valgte oppgaver </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Gyldig </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
I henhold til regel nr. 3 </p>
                <p>
Q1 inkluderer tid, materiale, utgifter og gebyrer for et delsett med oppgaver på prosjekt P1.
                </p>
                <p>
QL2 inkluderer tid, materialer, utgifter og gebyrer for et delsett med oppgaver på prosjekt P1.
                </p>
                <p>
Den eneste ekstra valideringen er rundt delsettet av oppgaver på QL1, som skiller seg fra delsettet av oppgaver på QL2, for å sikre at det ikke er noen overlapping. Dette gjøres av systemet når oppgaver er tilknyttet.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. kvartal </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Bare valgte oppgaver </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. kvartal </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Alle prosjektoppgaver eller tom </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Gyldig </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
I henhold til regel nr. 5, er Q1 og Q2 to tilbud på samme salgsmulighet, slik at begge kan estimeres for de samme komponentene i et prosjekt.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
2. kvartal </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Alle prosjektoppgaver eller tom </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. kvartal </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Alle prosjektoppgaver eller tom </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Ikke gyldig </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
I henhold til regel nr. 4, er Q1 og Q2 to tilbud på forskjellige salgsmuligheter, slik at de ikke kan estimeres for de samme komponentene i det samme prosjektet.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O2 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. kvartal </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Alle prosjektoppgaver eller tom </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
