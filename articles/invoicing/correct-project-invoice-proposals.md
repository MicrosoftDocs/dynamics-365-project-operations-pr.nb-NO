---
title: Korriger regnskapet på utkast av prosjektfakturaforslag
description: Denne artikkelen forklarer hvordan du justerer regnskapsrelatert informasjon i et utkast til fakturaforslag.
author: sigitac
ms.date: 01/05/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32f566a798d07b698693392f3aa1823f91fe5408
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921222"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Korriger regnskapet på utkast av prosjektfakturaforslag

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

*Operasjonsdetaljer* for prosjektfakturaer vedlikeholdes av prosjektlederen på en promafaktura. Disse detaljene inkluderer avgjørelsen om timene, utgiftene, materiellet eller milepælene som må faktureres, priser og bruk av beløp for forskudd og honorar. Når du har kontrollert den opprinnelige promafakturaen, kan du justere operasjonsdetaljene ved å opprette og bekrefte en [korrigerende promafaktura](../proforma-invoicing/corrective-invoices.md).

*Regnskapsdetaljer* for prosjektfakturaer vedlikeholdes i et kunderettet fakturadokument. Disse detaljene inkluderer beregningen av merverdiavgift og finansdimensjonene som brukes på fakturaen. Denne artikkelen inneholder detaljer om hvordan disse regnskapsdetaljene kan justeres i et utkast til prosjektfakturaforslag.

## <a name="adjust-sales-tax"></a>Juster merverdiavgift

Standard mva-grupper for fakturering og mva-grupper for varer kan justeres direkte i fakturaforslagsdokumentet. Hvis du vil justere disse gruppene, velger du **Rediger**, og deretter angir du en ny verdi i feltet **Mva-gruppe** eller **Mva-gruppe for vare** på hver prosjektfakturaforslagslinje.

## <a name="adjust-financial-dimensions"></a>Juster finansdimensjoner

### <a name="header-dimensions"></a>Hodedimensjoner

Som standard avledes finansdimensjoner for fakturaer fra de ikke-fakturerte prosjekttransaksjonsoppføringene som faktureres. Systeminnstillinger gjør det imidlertid enkelt å bruke finansdimensjoner i hodet i prosjektfakturaforslag til å postere kundesaldoer. Hvis du vil aktivere denne funksjonaliteten, velger du **Tillat oppdateringer av prosjektdimensjoner for utestående fordringer** på **Økonomi**-fanen på siden **Parametere for prosjektstyring og regnskap**.

Finansdimensjoner i fakturahoder kan redigeres før en faktura posteres. På siden **Prosjektfakturaforslag** bytter du til **Hode**-visningen, og deretter redigerer du verdier på fanen **Finansdimensjoner**.

**Hode**-visningen er bare tilgjengelig etter at systemadministratoren har aktivert funksjonen **Bruk prosjektfakturaforslag og fakturajournalskjemaene med hode- og linjevisning** i arbeidsområdet **Funksjonsbehandling**. Denne funksjonen krever oppdatering 10.0.25 eller senere av Finance.

### <a name="line-dimensions"></a>Linjedimensjoner

Finansdimensjoner kan ikke redigeres direkte på en prosjektfakturaforslagslinje. Følg i stedet denne fremgangsmåten for å justere finansdimensjoner i et prosjektfakturaforslag.

1. I prosjektfakturaforslaget velger du **Slett alle** for å fjerne prosjektfakturaforslagslinjene.

    Knappen **Slett alle** er bare tilgjengelig når systemadministrator aktiverer funksjonen **Slett fakturaforslagslinjer ved bruk av Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer** i arbeidsområdet **Funksjonsbehandling**.

2. Juster finansdimensjonene:

    - **A konto-transaksjoner (faktureringsmilepæler):** Gå til **Alle prosjekter** \> **Administrer** \> **A konto-transaksjoner**, og velg milepælen som krever justering. Oppdater deretter verdiene etter behov i fanen **Finansdimensjoner**.
    - **Tids-, utgifts- og materialtransaksjoner:** Velg **Juster regnskap** på siden **Posterte prosjekttransaksjoner** for å oppdatere finansdimensjonene.

3. Når du er ferdig med å justere finansdimensjonsverdiene, går du til **Prosjektstyring og regnskap** \> **Periodisk** \> **Project Operations-integrering** og velger **Importer fra oppsamlingstabell** for å kjøre den periodiske prosessen. Denne prosessen bruker de oppdaterte finansdimensjonsverdiene til å opprette prosjektfakturaforslagslinjene på nytt. De oppdaterte verdiene brukes deretter i underhovedboken for prosjektet og hovedboken når prosjektfakturaen posteres.
