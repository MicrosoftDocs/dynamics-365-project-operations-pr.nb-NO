---
title: Korrigerte fakturaer – Lite
description: Dette emnet gir informasjon om korrigerte fakturaer i Project Operations
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 55bec8ad1d9c2b55cabb453321f13df8b7cd1614
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176443"
---
# <a name="corrected-invoices---lite"></a>Korrigerte fakturaer – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

En bekreftet prosjektfaktura kan korrigeres mot prosessendringer eller kreditter som forhandlet med kunden og prosjektlederen.

Hvis du vil redigere en bekreftet faktura, åpner du den bekreftede fakturaen og velger **Rett opp denne fakturaen**. 

> [!NOTE]
> Dette valget er ikke tilgjengelig hvis ikke en prosjektfaktura er bekreftet.

Det opprettes en ny utkastfaktura fra den bekreftede fakturaen. Alle fakturalinjedetaljer fra den tidligere bekreftede fakturaen kopieres til det nye utkastet. Her følger noen av nøkkelpunktene for å forstå linjedetaljene i den nye korrigerte fakturaen:

- Alle antall blir oppdatert til null. Programmet forutsetter at alle fakturerte varer er fullt kreditert. Du kan om nødvendig oppdatere disse antallene manuelt, slik at de gjenspeiler antallet som blir fakturert, og ikke det antallet som krediteres. Basert på antallet du angir, beregner programmet det krediterte antallet. Dette beløpet gjenspeiles i de faktiske verdiene som opprettes når den rettede fakturaen er bekreftet. Hvis du gjør endringer i avgiftsbeløpet, må du angi riktig avgiftsbeløp og ikke avgiftsbeløpet som krediteres.
- Tidligere bekreftede produktbaserte kontraktlinjer kopieres ikke. Behandling av rettelser i en produktbasert prosjektfaktura støttes ikke.
- Milepælrettelser behandles alltid som fulle kreditter.
- Honorar- eller forskuddsbeløp kan korrigeres hvis kunden var fakturert for et feil beløp.
- Avstemminger av honorarer og forskudd kan korrigeres hvis et feilaktig beløp ble brukt til å avstemme mot kostnadene på en tidligere bekreftet faktura.

> [!IMPORTANT]
> Fakturalinjedetaljer som er rettelser i andre allerede fakturerte gebyrer,har feltet **Korrigering** angitt til **Ja**. Fakturaer som har korrigerte fakturalinjedetaljer, har et felt kalt **Har rettelser**, som også er angitt til **Ja**.

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>Faktiske verdier opprettet ved bekreftelse av en korrigert faktura:

Nedenfor finner du faktiske verdier som opprettes av programmet, ved bekreftelse av en korreksjon basert på operasjonene som ble utført på det korrigerte fakturautkastet før bekreftelse.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p>
                    <strong>Scenario</strong>
                </p>
            </td>
            <td width="808" valign="top">
                <p>
                    <strong>Faktiske verdier opprettet ved bekreftelse</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Bekreft rettelsen av et fakturert forskudd eller honorar.<strong></strong>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En tilbakeføring av ikke-fakturert salg for honoraret eller forskuddet som ble opprettet for avstemming. Dette beløpet er positivt fordi det er ment å nulle ut den negative verdien som ble opprettet da honoraret eller forskuddet ble fakturert.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En tilbakeføring av en faktisk salgsverdi opprettes for beløpet for honoraret eller forskuddet for å tilbakeføre det opprinnelige fakturerte salget.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny fakturert salgsverdi opprettes for det korrigerte beløpet for den korrigerte fakturalinjen som er basert på honoraret eller forskuddet.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ikke-fakturert faktisk salgsverdi av et negativt beløp for den korrigerte fakturalinjen som er basert på honoraret eller forskuddet, som skal brukes til avstemming.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
En bekreftelse av rettelsen av et tidligere avstemt honorar eller forskudd.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En tilbakeføring av ikke-fakturert salg for honoraret eller forskuddet som ble opprettet for avstemming. Dette beløpet er positivt og er ment å nulle ut den negative verdien som ble opprettet under den forrige avstemmingen.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En tilbakeført fakturert faktisk salgsverdi for beløpet på den forrige fakturaen.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny fakturert salgsverdi for det korrigerte honorarbeløpet som brukes i den korrigerte fakturaen.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ikke-fakturert faktisk salgsverdi med et negativt beløp fra den korrigerte honoraret eller forskuddet som er til overs, som skal brukes til avstemming på senere fakturaer.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturering av hele kreditten til en tidligere fakturert tidstransaksjon.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En fakturert salgsreversering for timene og beløpet på den opprinnelige fakturalinjedetaljen for tid.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-fakturert faktisk salgsverdi for timene og beløpet på den opprinnelige fakturalinjedetaljen for tid.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturering av den delvise kreditten på en tidstransaksjon.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En fakturert salgsreversering for timene og beløpet som er fakturert på den opprinnelige fakturalinjedetaljen for tid.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-fakturert faktisk salgsverdi som er belastbar for timene og beløpet på den redigerte fakturalinjedetaljen, en reversering av dette og en tilsvarende fakturert faktisk salgsverdi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-fakturert faktisk salgsverdi som er belastbar for gjenstående timer og beløp etter at de korrigerte tallene er trukket fra på fakturalinjedetaljene.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturering av hele kreditten til en tidligere fakturert utgiftstransaksjon.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En fakturert salgsreversering for antallet og beløpet som er fakturert på den opprinnelige fakturalinjedetaljen for utgiften.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-fakturert faktisk salgsverdi for antallet og beløpet som er fakturert på den opprinnelige fakturalinjedetaljen for utgiften.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturering av deler av kreditten til en tidligere fakturert utgiftstransaksjon.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En fakturert salgsreversering for antallet og beløpet som er fakturert på den opprinnelige fakturalinjedetaljen for en utgift.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-fakturert faktisk salgsverdi som er belastbar for antallet og beløpet på den korrigerte fakturalinjedetaljen, en reversering av dette og en tilsvarende fakturert faktisk salgsverdi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-fakturert faktisk salgsverdi som er belastbar for gjenstående antall og beløp etter at de korrigerte tallene er trukket fra på fakturalinjedetaljene.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturering av hele kreditten til en tidligere fakturert gebyrtransaksjon.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En fakturert salgsreversering for antallet og beløpet som er fakturert på den opprinnelige fakturalinjedetaljen for gebyret.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-fakturert faktisk salgsverdi for antallet og beløpet som er fakturert på den opprinnelige fakturalinjedetaljen for gebyret.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturering av deler av kreditten til en tidligere fakturert gebyrtransaksjon.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En fakturert salgsreversering for antallet og beløpet som er fakturert på den opprinnelige fakturalinjedetaljen for gebyret.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-fakturert faktisk salgsverdi som er belastbar for antallet og beløpet på den redigerte fakturalinjedetaljen, en reversering av dette og en tilsvarende fakturert faktisk salgsverdi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Fakturering av hele kreditten til en tidligere fakturert milepæl.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En fakturert salgsreversering for beløpet på den opprinnelige fakturalinjedetaljen for milepælen.
                </p>
                <p>
Faktura- eller faktureringsstatusen for milepælen på prosjektkontraktlinjen er oppdatert til **Klar for fakturerring**.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Fakturering av deler av kreditten til en tidligere fakturert milepæl.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Støttes ikke </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Kreditter og rettelser for en tidligere fakturert produktbasert kontraktlinje.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Støttes ikke </p>
            </td>
        </tr>
    </tbody>
</table>
