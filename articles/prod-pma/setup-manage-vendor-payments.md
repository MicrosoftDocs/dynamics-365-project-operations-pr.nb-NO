---
title: Konfigurere og bruke Betal når betalt-leverandørbetalinger
description: Dette emnet forklarer hvordan du oppretter Betal når betalt-betingelser (PWP), slik at du kan frigi delvise leverandørbetalinger basert på kundebetalinger.
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: e872c4a2d35cef4cddc6851615c6c4d73b4e9d9a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081599"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Konfigurere og bruke Betal når betalt-leverandørbetalinger

[!include [banner](../includes/banner.md)]

Når du godkjenner at en leverandør skal arbeide som en underleverandør, kan det hende du vil tilbakeholde betalingen til leverandøren helt til kunden betaler deg for prosjektet. Hvis du vil støtte dette scenariet, kan du angi betingelser for Betal når betalt (PWP) når du angir at bestillingen skal mottas med leverandøren.

Når en kunde for eksempel betaler et beløp på en prosjektfaktura, kan du frigi noe av eller hele leverandørfakturabeløpet. Bare sett opp PWP-termer som angir at leverandøren skal betales etter at du har mottatt en prosentdel av den relaterte betalingen fra kunden. Hvis du mottar delbetaling fra en kunde, kan du manuelt frigi noen av de relaterte leverandørfakturaene for betaling.

Eksemplet nedenfor beskriver prosessen når PWP-termer brukes.

## <a name="example"></a>Eksempel

Organisasjonen din godtar å levere en kunde 100 datamaskiner som har programvare installert, til en pris på 150,00 USD per datamaskin. Deretter leier du inn en leverandør for å levere deg datamaskinene der programvaren er installert. Ifølge avtalen må kunden godkjenne kvaliteten på datamaskinene før de betaler organisasjonen din. Organisasjonens policy er å tilbakeholde betalingen til leverandører helt til kunden har betalt. Derfor konfigurerer du prosjektet slik at det har en PWP-prosentandel på 100 prosent.

Leverandøren sender deg de 100 datamaskinene som har programvaren installert, sammen med en faktura på 10 000,00 USD. Fordi PWP-termer er satt opp for prosjektet, betaler du ikke leverandøren ved mottak av datamaskinene. I stedet sender du datamaskinene til kunden sammen med en faktura på 15 000,00. Kunden inspiserer datamaskinene og godkjenner hele beløpet for prosjektfakturaen.

Når du har mottatt hele betalingen fra kunden, betaler du leverandøren 10 000,00, hele beløpet på leverandørfakturaen.

## <a name="set-up-pwp-terms-for-a-project"></a>Konfigurere PWP-termer for et prosjekt

Når du definerer PWP-betingelser for et prosjekt, må du angi, som en prosentandel, minimumsbeløpet som en kunde må betale for prosjektet før du kan betale leverandøren. Terskelbeløpet beregnes automatisk på kundefakturaene for prosjektet. Følg denne fremgangsmåten for å konfigurere terskelprosenten for PWP-termer.

1. Gå til **Prosjektstyring og regnskap** \> **Prosjekter** \> **Alle prosjekter**.
2. Finn og åpne prosjektet du vil angi PWP-termer for.
3. På hurtigfanen **Leverandøravtaler** velger du **Legg til linje**.
3. Velg ett av følgende alternativer i feltet **Kontokode** :

    - **Tabell** – PWP-betingelsene gjelder for én enkelt leverandør.
    - **Gruppe** – PWP-betingelsene gjelder for alle leverandører i en leverandørgruppe.
    - **Alle** – PWP-betingelsene gjelder for alle leverandører.

4. Hvis du valgte **Tabell** eller **Gruppe** i forrige trinn, velger du leverandøren eller leverandørgruppen som PWP-termene gjelder for, i feltet **Leverandør/leverandørgruppe**. Hvis du valgte **Alle** i forrige trinn, kan ikke feltet **Leverandør/leverandørgruppe** redigeres.
5. Hvis du har angitt tilbakeholdelsesbetingelser for leverandøren i prosjektet, velger du regel-ID-en for tilbakeholdelsesbetingelsene i feltet **Tilbakeholdelsesbetingelser for leverandør**.
6. Angi terskelprosenten for prosjektet i feltet **PWP-terskelprosent**. Prosentandelen du skriver inn for prosjektet, definerer minimumsbeløpet kunden må betale før du kan betale leverandøren.

## <a name="create-a-po-that-has-pwp-terms"></a>Opprette en bestilling som har PWP-termer

Hvis leverandøren er underlagt PWP-betingelser når du bokfører en faktura fra en leverandør, vises disse betingelsene på bestillingslinjene. Følg fremgangsmåten nedenfor for å opprette en bestilling som har PWP-termer.

1. Gå til **Innkjøp og leverandør** \> **Bestillinger** \> **Alle bestillinger**.
2. Velg **Ny** i handlingsruten. Deretter angir du den nødvendige informasjonen i dialogboksen **Opprett bestilling** , og deretter velger du **OK**.

    Du kan også åpne en eksisterende bestilling på listesiden **Alle bestillinger**.

4. Gå gjennom detaljene på bestillingslinjen for leverandøren på siden **Bestilling** på hurtigfanen **Bestillingslinjer**. Alternativet **Betal når betalt** velges automatisk, og verdien i feltet **PWP-terskelprosent** kopieres automatisk fra feltet **PWP-terskelprosent** på **Prosjekter** -siden.
6. Hvis du ikke vil bruke PWP-termer for leverandøren på en bestillingslinje, fjerner du merket for **Betal når betalt**. I dette tilfellet blir feltet **PWP-terskelprosent** for bestillingslinjen tilbakestilt til 0 (null).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Oppdatere en kundebetaling og betale leverandøren

Når en leverandør fullfører arbeidet på et prosjekt, og sender deg en faktura, må du gå gjennom prosjektstatusen og kundefakturaene for å finne ut om PWP-termene er oppfylt for prosjektet. Hvis PWP-betingelsene for leverandøren ble oppfylt, kan du bestemme hvilke linjer på leverandørfakturaen som skal betales, basert på kundebetalingene for prosjektet. Hvis du bestemmer deg for å betale leverandøren selv om PWP-termene ikke ble oppfylt, kan du overstyre PWP-termene på siden **Leverandørfaktura med Betal når betalt**.

1. Gå til **Prosjektstyring og regnskap** \> **Forespørsler og rapporter** \> **Forespørsler om tilbakeholding** \> **Leverandørfaktura med Betal når betalt**.
2. I søkefeltet på siden **Leverandørfakturaer med Betal når betalt** angir du verdier for å finne leverandørfakturaen du vil se gjennom, og deretter velger du **Søk**.
3. Velg linjene du vil endre, på hurtigfanen **Leverandørfakturalinjer**.
4. Hvis betingelsene for **Betal når betalt** er oppfylt for fakturalinjen, velger du **Frigi leverandørbetaling**. Merket for **Betal når betalt** fjernes, og verdien i feltet **Klar for betaling** endres til **Ja**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]