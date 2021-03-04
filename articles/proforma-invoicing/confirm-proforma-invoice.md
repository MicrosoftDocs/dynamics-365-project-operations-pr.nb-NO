---
title: Bekrefte en proformafaktura
description: Dette emnet gir informasjon om å bekrefte en proformafaktura.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa1e6c17fbda76a283c2ec68760a00e846decf83
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128115"
---
# <a name="confirm-a-proforma-invoice"></a>Bekrefte en proformafaktura

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Når en proformafaktura er bekreftet, oppdateres statusen for prosjektfakturaen til **Bekreftet**. Når en faktura er bekreftet, blir den skrivebeskyttet. Derfra kan fakturaen bare korrigeres hvis det finnes kundeiverksatte rettelser eller kreditt, eller når den er merket som betalt.

Tabellen nedenfor viser de faktiske verdiene som opprettes av systemet. Disse faktiske verdiene opprettes når bestemte operasjoner utføres på utkastfakturaen for prosjektet før den er bekreftet.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p>
                    <strong>Scenario</strong>
                </p>
            </td>
            <td width="608" valign="top">
                <p>
                    <strong>Faktiske verdier opprettet ved bekreftelse</strong>
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
En ny ikke-fakturert faktisk salgsverdi som er belastbar for timene og beløpet på den redigerte fakturalinjedetaljen, en reversering av den ikke-fakturerte faktiske salgsverdien og en tilsvarende fakturert faktisk salgsverdi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-fakturert faktisk salgsverdi som er ikke-belastbar for resten av timene og beløpet etter å ha trukket fra de korrigerte tallene på den redigerte fakturalinjedetaljen, en reversering av den faktiske, ikke-fakturerte salgsverdien og en tilsvarende fakturert faktisk salgsverdi.
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
En fakturert faktisk salgsverdi for antallet og beløpet på den opprinnelige utgiftsgodkjenningen.
                </p>
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
En ny ikke-fakturert faktisk salgsverdi som er ikke-belastbar for resten av antallet og beløpet etter å ha trukket fra de korrigerte tallene på den redigerte fakturalinjedetaljen, en reversering av den faktiske, ikke-fakturerte salgsverdien og tilsvarende av den fakturerte faktiske salgsverdien.
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
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]