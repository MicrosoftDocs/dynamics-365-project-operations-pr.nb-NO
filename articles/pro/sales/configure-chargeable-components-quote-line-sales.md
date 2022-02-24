---
title: Konfigurere de belastbare komponentene i en tilbudslinje
description: Dette emnet gir informasjon om hvordan du konfigurerer belastbare og ikke-belastbare komponenter på en prosjektbasert tilbudslinje.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858305"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Konfigurere de belastbare komponentene i en tilbudslinje 

_**Gjelder for:** Lite-distribusjon – avtale til proformafakturering, Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

En prosjektbasert tilbudslinje har konseptet *inkluderte* komponenter og *belastbare* komponenter.

Inkluderte komponenter er underlagt følgende:

  - Faktureringsmetode og kundedelinger
  - Må ikke overskrides-grenser 
  - Innstillinger for fakturafrekvens som er definert på den prosjektbaserte tilbudslinjen

Et delsett av de inkluderte komponentene kan merkes som belastbarte ved hjelp av feltet **Faktureringstype**. Feltet **Faktureringstype** er et alternativsett som tillater følgende verdier i konteksten for en tilbudslinje:

  - Belastbar
  - Ikke-belastbar

Belastbare komponenter kan defineres for oppgaver, roller og transaksjonskategorier.

Belastbarhet er definert i oppgavene for en tilbudslinje og gjelder for alle transaksjonsklasser som finnes på denne linjen. Hvis feltet **Inkluder oppgaver** satt til **Hele prosjektet** eller er tomt, er ikke **Belastbare oppgaver**-fanen tilgjengelig.

Belastbarhet er definert for roller for en tilbudslinje og gjelder bare transaksjonsklassen **Tid**. Hvis feltet **Inkluder td** er satt til **Nei** på en prosjekttilbudslinje, er ikke **Belastbare roller**-fanen tilgjengelig.

Belastbarhet er definert for transaksjonskategorier for en tilbudslinje og gjelder bare transaksjonsklassen **Utgift**. Hvis feltet **Inkluder utgifter** er satt til **Nei** på en prosjekttilbudslinje, er ikke **Belastbare kategorier**-fanen tilgjengelig.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Oppdatere en prosjektoppgave til å være belastbar eller ikke-belastbar

En prosjektoppgave kan være belastbar eller ikke-belastbar i konteksten til en bestemt prosjektbasert tilbudslinje, noe som gjør følgende oppsett mulig.

Hvis en prosjektbasert tilbudslinje inkluderer **Tid** og oppgaven **T1**, knyttes oppgaven til tilbudslinjen som belastbar. Hvis det er en ny tilbudslinje som inkluderer **Utgifter**, kan du knytte til **T1**-oppgaven på tilbudslinjen som ikke-belastbar. Resultatet er at all tid som registreres på oppgaven, er belastbar, og at alle utgifter som registreres på oppgaven, er ikke-belastbare.

Du kan konfigurere faktureringstypen for en oppgave i kategorien **Belastbare oppgaver** på en prosjektbasert tilbudslinje ved å oppdatere **Fakturatype**-feltet i delrutenettet **Tilbudslinjeoppgaver**. Du kan også oppdatere faktureringstypen for en prosjektoppgave i **Faktureringstype**-feltet i delrutenettet på faktureringsoppsettet for oppgaven for prosjektet som viser tilbudslinjene som er knyttet til en oppgave.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Oppdatere en rolle til å være belastbar eller ikke-belastbar

En rolle kan være belastbar eller ikke-belastbar i konteksten for en bestemt prosjektbasert tilbudslinje.

Du kan konfigurere faktureringstypen for en rolle i kategorien **Belastbare roller** på en tilbudslinje ved å oppdatere **Fakturatype**-feltet i delrutenettet **Belastbare roller**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Oppdatere en transaksjonskategori til å være belastbar eller ikke-belastbar

En transaksjonskategori kan være belastbar eller ikke-belastbar på en bestemt tilbudslinje.

Du kan konfigurere faktureringstypen for en transaksjon i kategorien **Belastbare kategorier** på en tilbudslinje ved å oppdatere **Fakturatype**-feltet i delrutenettet **Belastbare kategorier**.

### <a name="resolve-chargeability"></a>Løse belastbarhet
Et estimat eller en faktisk verdi opprettet for tid regnes bare som belastbar hvis:

   - **Tid** er inkludert på tilbudslinjen.
   - **Rolle** er konfigurert som belastbar på tilbudslinjen.
   - **Inkluderte oppgaver** er satt til **Valgte oppgaver** på tilbudslinjen. 

Hvis disse tre tingene er oppfylt, er **oppgaven** også konfigurert som belastbar. 

Et estimat eller en faktisk verdi opprettet for utgift regnes bare som belastbar hvis: 

   - **Utgift** er inkludert på tilbudslinjen.
   - **Transaksjonskategori** er konfigurert som belastbar på tilbudslinjen.
   - **Inkluderte oppgaver** er satt til **Valgte oppgaver** på tilbudslinjen.

Hvis disse tre tingene er oppfylt, er **oppgaven** også konfigurert som belastbar. 

Et estimat eller en faktisk verdi opprettet for materialer regnes bare som belastbar hvis:

   - **Materialer** er inkludert på tilbudslinjen.
   - **Inkluderte oppgaver** er satt til **Valgte oppgaver** på tilbudslinjen.

Hvis disse to tingene er oppfylt, skal **oppgaven** også være konfigurert som belastbar. 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Inkluderer tid</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Inkluderer utgift</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Inkluder materialer</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
                    <strong>Inkluderte oppgaver</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Rolle</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Kategori</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Oppgave</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
                    <strong>Innvirkning på belastbarhet</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Hele prosjektet </p>
            </td>
            <td width="65" valign="top">
                <p>
Belastbar </p>
            </td>
            <td width="70" valign="top">
                <p>
Belastbar </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan ikke angis </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering på en faktisk tidsverdi: Belastbar </p>
                <p>
Faktureringstype for en faktisk utgiftsverdi: Belastbar </p>
                <p>
Faktureringstype for en faktisk materialeverdi: Belastbar </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Bare valgte oppgaver </p>
            </td>
            <td width="65" valign="top">
                <p>
Belastbar </p>
            </td>
            <td width="70" valign="top">
                <p>
Belastbar </p>
            </td>
            <td width="65" valign="top">
                <p>
Belastbar </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering på en faktisk tidsverdi: Belastbar </p>
                <p>
Faktureringstype for en faktisk utgiftsverdi: Belastbar </p>
                <p>
Faktureringstype for en faktisk materialeverdi: Belastbar </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Bare valgte oppgaver </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Ikke-belastbar</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Belastbar </p>
            </td>
            <td width="65" valign="top">
                <p>
Belastbar </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering på en faktisk tidsverdi: <strong>Ikke-belastbar</strong>
                </p>
                <p>
Faktureringstype for en faktisk utgiftsverdi: Belastbar </p>
                <p>
Faktureringstype for en faktisk materialeverdi: Belastbar </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Bare valgte oppgaver </p>
            </td>
            <td width="65" valign="top">
                <p>
Belastbar </p>
            </td>
            <td width="70" valign="top">
                <p>
Belastbar </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Ikke-belastbar</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering på en faktisk tidsverdi: <strong>Ikke-belastbar</strong>
                </p>
                <p>
Faktureringstype for en faktisk utgiftsverdi: <strong>Ikke-belastbar</strong>
                </p>
                <p>
Faktureringstype for en faktisk materialeverdi: <strong>Ikke-belastbar</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Bare valgte oppgaver </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Ikke-belastbar</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Belastbar </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Ikke-belastbar</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering på en faktisk tidsverdi: <strong>Ikke-belastbar</strong>
                </p>
                <p>
Faktureringstype for en faktisk utgiftsverdi: <strong>Ikke-belastbar</strong>
                </p>
                <p>
Faktureringstype for en faktisk materialeverdi: <strong>Ikke-belastbar</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Bare valgte oppgaver </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Ikke-belastbar</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Ikke-belastbar</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Belastbar </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering på en faktisk tidsverdi: <strong>Ikke-belastbar</strong>
                </p>
                <p>
Faktureringstype for en faktisk utgiftsverdi: <strong>Ikke-belastbar</strong>
                </p>
                <p>
Faktureringstype for en faktisk materialeverdi: Belastbar </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Hele prosjektet </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan ikke angis </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Belastbar</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan ikke angis </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering på en faktisk tidsverdi: <strong>Ikke tilgjengelig</strong>
                </p>
                <p>
Faktureringstype for en faktisk utgiftsverdi: Belastbar </p>
                <p>
Faktureringstype for en faktisk materialeverdi: Belastbar </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Hele prosjektet </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan ikke angis </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Ikke-belastbar</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan ikke angis </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering på en faktisk tidsverdi: <strong>Ikke tilgjengelig</strong>
                </p>
                <p>
Faktureringstype for en faktisk utgiftsverdi: <strong>Ikke-belastbar</strong>
                </p>
                <p>
Faktureringstype for en faktisk materialeverdi: Belastbar </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Hele prosjektet </p>
            </td>
            <td width="65" valign="top">
                <p>
Belastbar </p>
            </td>
            <td width="70" valign="top">
                <p>
Kan ikke angis </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan ikke angis </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering på en faktisk tidsverdi: Belastbar </p>
                <p>
Faktureringstype for en faktisk utgiftsverdi:<strong> Ikke tilgjengelig</strong>
                </p>
                <p>
Faktureringstype for en faktisk materialeverdi: Belastbar </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Hele prosjektet </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Ikke-belastbar</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Kan ikke angis </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan ikke angis </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering på en faktisk tidsverdi: <strong>Ikke-belastbar </strong>
                </p>
                <p>
Faktureringstype for en faktisk utgiftsverdi:<strong> Ikke tilgjengelig</strong>
                </p>
                <p>
Faktureringstype for en faktisk materialeverdi: Belastbar </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Hele prosjektet </p>
            </td>
            <td width="65" valign="top">
                <p>
Belastbar </p>
            </td>
            <td width="70" valign="top">
                <p>
Belastbar </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan ikke angis </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering på en faktisk tidsverdi: Belastbar </p>
                <p>
Faktureringstype for en faktisk utgiftsverdi: Belastbar </p>
                <p>
Faktureringstype for en faktisk materialeverdi: <strong>Ikke tilgjengelig</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Hele prosjektet </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Ikke-belastbar</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Ikke-belastbar</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan ikke angis </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering på en faktisk tidsverdi: <strong>Ikke-belastbar </strong>
                </p>
                <p>
Faktureringstype for en faktisk utgiftsverdi:<strong> Ikke-belastbar </strong>
                </p>
                <p>
Faktureringstype for en faktisk materialeverdi:<strong> Ikke tilgjengelig</strong>
                </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
