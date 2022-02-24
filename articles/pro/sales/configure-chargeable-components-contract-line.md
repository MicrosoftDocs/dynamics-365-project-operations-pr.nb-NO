---
title: Konfigurere belastbare komponenter for en prosjektbasert kontraktlinje
description: Dette emnet gir informasjon om hvordan du legger til belastbare komponenter i kontraktlinjer i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ddada2cb412ba7370fb0a750325a84772937d8d0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858485"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Konfigurere belastbare komponenter for en prosjektbasert kontraktlinje

_**Gjelder for:** Lite-distribusjon – avtale til proformafakturering, Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

En prosjektbasert kontraktlinje har *inkluderte* komponenter og *belastbare* komponenter.

Inkluderte komponenter er komponenter som er underlagt følgende:

  - Faktureringsmetode og kundedelinger
  - Må ikke overskrides-grenser 
  - Innstillinger for fakturafrekvens som er definert på den prosjektbaserte kontraktlinjen

Et delsett av de inkluderte komponentene kan merkes som belastbarte ved hjelp av feltet **Faktureringstype**. Feltet **Faktureringstype** er et alternativsett som tillater følgende verdier i konteksten for en kontraktlinje:

  - Belastbar
  - Ikke-belastbar

Belastbare komponenter kan defineres for oppgaver, roller og transaksjonskategorier.

Belastbar er definert i oppgaver for en prosjektkontraktlinje og gjelder for alle transaksjonsklasser som finnes på linjen. Hvis **Inkluder oppgaver**-feltet på en kontraktlinje er tomt eller satt til **Hele prosjektet**, er ikke **Belastbare oppgaver**-fanen tilgjengelig.

Belastbarhet definert for roller for en prosjektkontraktlinje gjelder bare transaksjonsklassen **Tid**. Hvis feltet **Inkluder td** på en kontraktlinje er satt til **Nei**, er ikke **Belastbare roller**-fanen tilgjengelig.

Belastbarhet definert for transaksjonskategorier for en prosjektkontraktlinje gjelder bare transaksjonsklassen **Utgift**. Hvis feltet **Inkluder utgifter** på en kontraktlinje er satt til **Nei**, er ikke **Belastbare kategorier**-fanen tilgjengelig.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Oppdatere en prosjektoppgave som belastbar eller ikke-belastbar

En prosjektoppgave kan være belastbar eller ikke-belastbar på en bestemt kontraktlinje, noe som gjør følgende oppsett mulig:

Hvis en prosjektbasert kontraktlinje inkluderer **Tid** og en bestemt oppgave, er **T1** knyttet til den som belastbar. Hvis det er en ny kontraktlinje som inkluderer **Utgift**, kan du knytte T1-oppgaven på kontraktlinjen som ikke-belastbar. Resultatet er at all tid som registreres på oppgaven, er belastbar, og at alle utgifter er ikke-belastbare.

Du kan konfigurere faktureringstypen for en oppgave i kategorien **Belastbare oppgaver** på kontraktlinjen ved å oppdatere **Fakturatype**-feltet i delrutenettet for kontraktlinjeoppgaver. Du kan også oppdatere **Faktureringstype**-feltet i delrutenettet for faktureringsoppsettet for oppgaven for prosjektet som viser kontraktlinjene som er knyttet til en oppgave.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Oppdatere en rolle som belastbar eller ikke-belastbar

En rolle kan være belastbar eller ikke-belastbar på en bestemt kontraktlinje.

Du kan konfigurere fakturerings typen for en rolle på **Belastbare roller**-fanen på en kontraktlinje. Dette gjør du ved å oppdatere **Faktureringstype**-feltet i delrutenettet **Belastbare roller**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Oppdatere en transaksjonskategori som belastbar eller ikke-belastbar

En transaksjonskategori kan være belastbar eller ikke-belastbar på en bestemt kontraktlinje.

Du kan konfigurere faktureringstypen for en transaksjon på **Belastbare kategorier**-fanen på en prosjektbasert kontraktlinje. Dette gjør du ved å oppdatere **Faktureringstype**-feltet i delrutenettet **Belastbare kategorier**.

### <a name="resolve-chargeability"></a>Løse belastbarhet

Et estimat eller en faktisk verdi opprettet for tid regnes bare som belastbar hvis:

   - **Tid** er inkludert på kontraktlinjen.
   - **Rolle** er konfigurert som belastbar på kontraktlinjen.
   - **Inkluderte oppgaver** er satt til **Valgte oppgaver** på kontraktlinjen.
 
 Hvis disse tre tingene er oppfylt, er oppgaven konfigurert som belastbar. 

Et estimat eller en faktisk verdi opprettet for utgift regnes bare som belastbar hvis:

   - **Utgift** er inkludert på kontraktlinjen.
   - **Transaksjonskategori** er konfigurert som belastbar på kontraktlinjen.
   - **Inkluderte oppgaver** er satt til **Valgt oppgave** på kontraktlinjen.
  
 Hvis disse tre tingene er oppfylt, er **oppgaven** konfigurert som belastbar. 

Et estimat eller en faktisk verdi opprettet for materialer regnes bare som belastbar hvis:

   - **Materialer** er inkludert på kontraktlinjen.
   - **Inkluderte oppgaver** er satt til **Valgte oppgaver** på kontraktlinjen.

Hvis disse to tingene er oppfylt, er **oppgaven** konfigurert som belastbar. 

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
Fakturering på en faktisk tidsverdi: <strong>Belastbar</strong>
                </p>
                <p>
Faktureringstype for en faktisk utgiftsverdi: <strong>Belastbar</strong>
                </p>
                <p>
Faktureringstype for en faktisk materialeverdi: <strong>Belastbar</strong>
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
Fakturering på en faktisk tidsverdi: <strong>Belastbar</strong>
                </p>
                <p>
Faktureringstype for en faktisk utgiftsverdi: <strong>Belastbar</strong>
                </p>
                <p>
Faktureringstype for en faktisk materialeverdi: <strong>Belastbar</strong>
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
