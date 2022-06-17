---
title: Bekrefte en proforma prosjektfaktura
description: Denne artikkelen inneholder informasjon om hvordan du bekrefter proforma prosjektfakturaer i Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 101e4564fcf57cbbfc713773ed760291b9d28410
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922234"
---
# <a name="confirm-a-proforma-project-invoice"></a>Bekrefte en proforma prosjektfaktura 

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_


Når en proformafaktura er bekreftet, oppdateres statusen for prosjektfakturaen til **Bekreftet**. Når en faktura er bekreftet, blir den skrivebeskyttet. Fremover kan fakturaen bare korrigeres hvis det er noen kundestartede rettelser eller kreditter.

Tabellen nedenfor viser de faktiske verdiene som opprettes av systemet. Disse faktiske verdiene opprettes når bestemte operasjoner utføres på utkastfakturaen for prosjektet før den er bekreftet.

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
Fakturere et forskudd eller honorar </p>
            </td>
            <td width="408" valign="top">
                <p>
E fakturert salgsverdi av typen <strong>Honorar</strong> opprettes for beløpet for forskuddet eller honoraret.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ikke-fakturert faktisk salgsverdi av et negativt beløp for honoraret eller forskuddet som skal brukes til avstemming.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Etter fullstendig avstemming av et honorar eller forskudd på en faktura.
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
En fakturert faktisk salgsverdi for beløpet på denne fakturaen.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Etter delvis avstemming av et honorar eller forskudd på en faktura.
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
En fakturert faktisk salgsverdi for beløpet på denne fakturaen.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En negativ, ikke-fakturert faktisk salgsverdi av resten av beløpet for honoraret eller forskuddet som skal brukes til avstemming på fremtidige fakturaer.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturering av en tidstransaksjon uten redigeringer på fakturautkastet.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En ikke-fakturert salgsreversering for timene og beløpet på den opprinnelige tidsgodkjenningen.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En fakturert faktisk salgsverdi for timene og beløpet på den opprinnelige tidsgodkjenningen.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturering av en tidstransaksjon som ble redigert for å redusere antallet.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En ikke-fakturert salgsreversering for timene og beløpet på den opprinnelige tidsgodkjenningen.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-fakturert faktisk salgsverdi som er belastbar for timene og beløpet på den redigerte fakturalinjedetaljen, en reversering av den faktiske salgsverdien og en tilsvarende fakturert faktisk salgsverdi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-fakturert faktisk salgsverdi som er ikke-belastbar for resten av timene og beløpet etter å ha trukket fra de korrigerte tallene på den redigerte fakturalinjedetaljen, en reversering av den faktiske salgsverdien og en tilsvarende fakturert faktisk salgsverdi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturering av en tidstransaksjon som ble redigert for å øke antallet.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En ikke-fakturert salgsreversering for timene og beløpet på den opprinnelige tidsgodkjenningen.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-fakturert faktisk salgsverdi som er belastbar for timene og beløpet på den redigerte fakturalinjedetaljen, en reversering av den ikke-fakturerte faktiske salgsverdien og en tilsvarende fakturert faktisk salgsverdi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturering av en utgiftstransaksjon uten redigeringer på fakturautkastet.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En ikke-fakturert salgsreversering for antallet og beløpet på den opprinnelige utgiftsgodkjenningen.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En fakturert faktisk salgsverdi for antallet og beløpet på den opprinnelige utgiftsgodkjenningen </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturering av en utgiftstransaksjon som ble redigert for å redusere antallet.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En ikke-fakturert salgsreversering for antallet og beløpet på den opprinnelige utgiftsgodkjenningen.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-fakturert faktisk salgsverdi som er belastbar for antallet og beløpet på den redigerte fakturalinjedetaljen, en reversering av den faktiske, ikke-fakturerte salgsverdien og en tilsvarende fakturert faktisk salgsverdi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-fakturert faktisk salgsverdi som er ikke-belastbar for resten av antallet og beløpet etter å ha trukket fra de korrigerte tallene på den redigerte fakturalinjedetaljen, en reversering av den faktiske, ikke-fakturerte salgsverdien og en tilsvarende fakturert faktisk salgsverdi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturering av en utgiftstransaksjon som ble redigert for å øke antallet.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En ikke-fakturert salgsreversering for antallet og beløpet på den opprinnelige utgiftsgodkjenningen.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-fakturert faktisk salgsverdi som er belastbar for antallet og beløpet på den redigerte fakturalinjedetaljen, en reversering av den faktiske, ikke-fakturerte salgsverdien og en tilsvarende fakturert faktisk salgsverdi. 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturering av en materialtransaksjon uten redigeringer i utkastfakturaen.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En ufakturert tilbakeføring av salg for antallet og beløpet i den opprinnelige godkjenningen av materialbruk.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En fakturert faktisk salgsverdi for antallet og beløpet i den opprinnelige godkjenningen av materialbruk.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturering av en materialtransaksjon som ble redigert for å redusere antallet.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En ufakturert tilbakeføring av salg for antallet og beløpet i den opprinnelige godkjenningen av tidsbruk.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-fakturert faktisk salgsverdi som er belastbar for antallet og beløpet på den redigerte fakturalinjedetaljen, en reversering av den faktiske, ikke-fakturerte salgsverdien og en tilsvarende fakturert faktisk salgsverdi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-fakturert faktisk salgsverdi som er ikke-belastbar for resten av antallet og beløpet etter å ha trukket fra de korrigerte tallene på den redigerte fakturalinjedetaljen, en reversering av den faktiske, ikke-fakturerte salgsverdien og en tilsvarende fakturert faktisk salgsverdi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturering av en materialtransaksjon som ble redigert for å øke antallet.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En ufakturert tilbakeføring av salg for antallet og beløpet i den opprinnelige godkjenningen av materialbruk.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-fakturert faktisk salgsverdi som er belastbar for antallet og beløpet på den redigerte fakturalinjedetaljen, en reversering av den faktiske, ikke-fakturerte salgsverdien og en tilsvarende fakturert faktisk salgsverdi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturering av et gebyr.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En ikke-fakturert salgsreversering for gebyrbeløpet på den opprinnelige journallinjen.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En fakturert faktisk salgsverdi for antallet og beløpet på den opprinnelige gebyrjournallinjen.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Fakturering av en milepæl.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En fakturert faktisk salgsverdi for milepælbeløpet på den opprinnelige milepælen på prosjektkontraktlinjen.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Fakturering av en produktbasert kontraktlinje.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En fakturert faktisk salgsverdi for produktlinjen med antallet og beløpet som kommer fra den produktbaserte kontraktlinjen.
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
