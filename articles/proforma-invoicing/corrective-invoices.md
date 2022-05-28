---
title: Korrigerte prosjektbaserte fakturaer
description: Dette emnet inneholder informasjon om hvordan du oppretter og bekrefter korrigerte prosjektbaserte fakturaer i Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 71bf10518c22ce2ad6aa43b710c68d0d46f93e77
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8594636"
---
# <a name="corrective-project-based-invoices"></a>Korrigerte prosjektbaserte fakturaer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

En bekreftet prosjektfaktura kan korrigeres mot prosessendringer eller kreditter som forhandlet med kunden og prosjektlederen.

Hvis du vil redigere en bekreftet faktura, åpner du den bekreftede fakturaen og velger **Rett opp denne fakturaen**. 

> [!NOTE]
> Dette valget er ikke tilgjengelig med mindre en prosjektfaktura er bekreftet, eller den prosjektbaserte fakturaen har forskudd eller honorarer eller avstemminger av forskudd eller honorarer.

Det opprettes en ny utkastfaktura fra den bekreftede fakturaen. Alle fakturalinjedetaljer fra den tidligere bekreftede fakturaen kopieres til det nye utkastet. Her følger noen av nøkkelpunktene for å forstå linjedetaljene i den nye korrigerte fakturaen:

- Alle antall blir oppdatert til null. Dynamics 365 Project Operations forutsetter at alle fakturerte elementer er kreditert fullt ut. Du kan om nødvendig oppdatere disse antallene manuelt, slik at de gjenspeiler antallet som blir fakturert, og ikke det antallet som krediteres. Basert på antallet du angir, beregner programmet det krediterte antallet. Dette beløpet gjenspeiles i de faktiske verdiene som opprettes når den rettede fakturaen er bekreftet. Hvis du gjør endringer i avgiftsbeløpet, må du angi riktig avgiftsbeløp og ikke avgiftsbeløpet som krediteres.
- Milepælrettelser behandles alltid som fulle kreditter.


> [!IMPORTANT]
> For fakturalinjedetaljer som er rettelser i andre allerede fakturerte omkostnader, er feltet **Korrigering** satt til **Ja**. For fakturaer som har korrigerte fakturalinjedetaljer, er feltet **Har korrigeringer** satt til **Ja**.

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a>Faktiske verdier opprettet ved bekreftelse av en korrigert faktura

Tabellen nedenfor viser de faktiske verdiene som opprettes når en korrigeringsfaktura bekreftes.

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
Fakturering av den fulle kreditten for en tidligere fakturert materialtransaksjon.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En fakturert tilbakeføring av salg for antallet og beløpet i den opprinnelige fakturalinjedetaljer for material.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ufakturert faktisk salgsverdi for antallet og beløpet i den opprinnelige fakturalinjedetaljer for material.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturering av delvis kreditt på en materialtransaksjon.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En fakturert tilbakeføring av salg for antallet og beløpet som var fakturert i den opprinnelige fakturalinjedetaljen for material.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ufakturert faktisk salgsverdi som er belastbar for antallet og beløpet på de redigerte fakturalinjedetaljen, en reversering av dette og tilsvarende fakturert faktisk salgsverdi.
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
Fakturastatusen for milepælen oppdateres fra en <b>kundefaktura som er postert</b> som <b>Klar for fakturering</b>.
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
Dette scenarioet støttes ikke.
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
