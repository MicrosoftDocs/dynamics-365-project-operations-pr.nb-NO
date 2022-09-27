---
title: Betal når betalt-leverandørbetalinger
description: Dette emnet forklarer hvordan du bruker betal når betalt-scenarioet (PWP).
author: mukumarm
ms.date: 08/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: mukumarm
ms.openlocfilehash: d1fe8d92663b31b22dc405fc1f3e06d976e6c5dc
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525342"
---
# <a name="pay-when-paid-vendor-payments"></a>Betal når betalt-leverandørbetalinger

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Dette emnet forklarer hvordan du bruker betal når betalt-scenarioet (PWP).

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Opprette en innkjøpsordre som har PWP-betingelser

Hvis leverandøren er underlagt PWP-betingelser når du bokfører en faktura fra en leverandør, vises disse betingelsene på bestillingslinjene. Følg fremgangsmåten nedenfor for å opprette en bestilling som har PWP-termer.

1. Følg ett eller flere av disse trinnene i Microsoft Dynamics 365 Finance:

    - Gå til **Innkjøp og leverandør** \> **Bestillinger** \> **Alle bestillinger**. Velg **Ny** i handlingsruten. I dialogboksen **Opprett bestilling** velger du leverandøren som PWP-betingelser er definert for i prosjektet, angir annen nødvendig informasjon, og deretter velger du **OK**.
    - Gå til **Prosjektstyring og regnskap** \> **Prosjekter** \> **Alle prosjekter**. Gå til **Administrer**-fanen i handlingsruten, og velg deretter **Vareoppgave**. Velg bestillingen. Velg leverandøren som PWP-betingelser er definert for i prosjektet, og velg deretter **OK**.

2. På siden **Bestilling**, på hurtigfanen **Bestillingslinjer** velger du **Legg til linje** for å opprette en bestillingslinje.
3. Velg varenummeret eller innkjøpskategorien, og angi de andre obligatoriske detaljene. Se gjennom detaljene for bestillingslinjen for leverandøren.

    Alternativet **Betal når betalt** velges automatisk, og verdien i feltet **PWP-terskelprosent** kopieres automatisk fra feltet **PWP-terskelprosent** på **Prosjekter**-siden.

4. Hvis du ikke vil bruke PWP-termer for leverandøren på en bestillingslinje, fjerner du merket for **Betal når betalt**. I dette tilfellet blir feltet **PWP-terskelprosent** for bestillingslinjen tilbakestilt til **0** (null).
5. På **Bestilling order**-siden, i handlingsruten på **Kjøp**-fanen, i velger du **Bekreft** for å bekrefte bestillingen.
6. I handlingsruten på fanen **Faktura** velger du **Faktura** for å generere fakturaen for bestillingen.

## <a name="create-a-project-invoice-proposal"></a>Opprette et forslag om prosjektfaktura

Forslag om prosjektfakturaer brukes til å opprette prosjektfakturaer for kunden. I PWP-scenarioet er leverandørbetalinger avhengige av kundebetalinger i henhold til PWP-innstillingene. Det finnes imidlertid alternativer der du kan frigi betalinger uten kundebetalinger ved behov. Gjør følgende for å opprette en prosjektfaktura for kunden.

1. I Customer Engagement-appen går du til **Prosjekt** \> **Prosjekter** og velger prosjektet.
2. I kategorien **Faktiske verdier** velger du den faktiske linjen som genereres av bestillingen som har transaksjonstypen **Ufakturert salg**. Deretter velger du **Klar for faktura**.
3. Gå til **Salg** \> **Salg** \> **Prosjektkontrakt**, og velg prosjektkontrakten.
4. I handlingsruten velger du **Fakturer** for å generere kundefakturaen.
5. I Finance går du til **Prosjektstyring og regnskap** \> **Periodisk** \> **Import fra oppsamlingstabell** og velger **OK** for å generere journalen for Project Operations-integrering.
6. Gå til **Prosjektstyring og regnskap** \> **Prosjektfakturaer** \> **Prosjektfakturaforslag**, og velg **Poster** for å postere fakturaforslaget som ble generert for prosjektet.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Oppdatere en kundebetaling og betale leverandøren

Når en leverandør fullfører arbeidet på et prosjekt, og sender deg en faktura, må du gå gjennom prosjektstatusen og kundefakturaene for å finne ut om PWP-termene var oppfylt for prosjektet. Hvis PWP-betingelsene for leverandøren ble oppfylt, kan du bestemme hvilke linjer på leverandørfakturaen som skal betales, basert på kundebetalingene for prosjektet. Hvis du bestemmer deg for å betale leverandøren selv om PWP-termene ikke ble oppfylt, kan du overstyre PWP-termene på siden **Leverandørfaktura med Betal når betalt**.

1. I Finance går du til **Prosjektstyring og regnskap** \> **Prosjekter** \> **Alle prosjekter** og velger prosjektet.
2. Velg **Kontroll** i handlingsruten, og velg deretter **Leverandørfakturaer** for å vise alle leverandørfakturaer som er generert for prosjektet.
3. I søkefeltet på siden **Leverandørfakturaer med Betal når betalt** angir du verdier for å finne leverandørfakturaen du vil se gjennom, og deretter velger du **Søk**.
4. Velg alternativet **Betal når betalt** for å vise kun PWP-fakturaer.
5. Velg linjene du vil frigi for betaling, på hurtigfanen **Leverandørfakturalinjer**.
6. Velg **Frigi leverandørbetaling**. Merket for **Betal når betalt** fjernes, og verdien i feltet **Klar for betaling** endres til **Ja**.
