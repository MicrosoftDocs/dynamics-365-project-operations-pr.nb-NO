---
title: Korriger regnskapet på utkast av prosjektfakturaforslag
description: Dette emnet forklarer hvordan du justerer regnskapsrelatert informasjon i et utkast av fakturaforslag.
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 387dc9a81db9c22f170b664152cbafeddf72d149
ms.sourcegitcommit: e93f436afbb92a312fc71b6371866f01927e49d5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/14/2021
ms.locfileid: "6251252"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Korriger regnskapet på utkast av prosjektfakturaforslag

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

*Operasjonsdetaljer* for prosjektfakturaer vedlikeholdes av prosjektlederen på en promafaktura. Disse detaljene inkluderer avgjørelsen om timene, utgiftene, materiellet eller milepælene som må faktureres, priser og bruk av beløp for forskudd og honorar. Når du har kontrollert den opprinnelige promafakturaen, kan du justere operasjonsdetaljene ved å opprette og bekrefte en [korrigerende promafaktura](../proforma-invoicing/corrective-invoices.md).

*Regnskapsdetaljer* for prosjektfakturaer vedlikeholdes i et kunderettet fakturadokument. Disse detaljene inkluderer beregningen av merverdiavgift og finansdimensjonene som brukes på fakturaen. Dette emnet inneholder detaljer om hvordan disse regnskapsdetaljene kan justeres i et utkast til prosjektfakturaforslag.

## <a name="adjust-sales-tax"></a>Juster merverdiavgift

Standard mva-grupper for fakturering og mva-grupper for varer kan justeres direkte i fakturaforslagsdokumentet. Hvis du vil justere disse gruppene, velger du **Rediger**, og deretter angir du en ny verdi i feltet **Mva-gruppe** eller **Mva-gruppe for vare** på hver prosjektfakturaforslagslinje.

## <a name="adjust-financial-dimensions"></a>Juster finansdimensjoner

Finansdimensjoner kan ikke redigeres direkte på en prosjektfakturaforslagslinje. Følg i stedet denne fremgangsmåten for å justere finansdimensjoner i et prosjektfakturaforslag.

1. I prosjektfakturaforslaget velger du **Slett alle** for å fjerne prosjektfakturaforslagslinjene.

    > [!NOTE]
    > Knappen **Slett alle** er bare tilgjengelig når systemadministrator aktiverer funksjonen **Slett fakturaforslagslinjer ved bruk av Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer** i arbeidsområdet **Funksjonsbehandling**.

2. Juster finansdimensjonene:

    - **A konto-transaksjoner (faktureringsmilepæler):** Gå til **Alle prosjekter** \> **Administrer** \> **A konto-transaksjoner**, og velg milepælen som krever justering. Oppdater deretter verdiene etter behov i fanen **Finansdimensjoner**.
    - **Tids-, utgifts- og materialtransaksjoner:** Velg **Juster regnskap** på siden **Posterte prosjekttransaksjoner** for å oppdatere finansdimensjonene.

3. Når du er ferdig med å justere finansdimensjonsverdiene, går du til **Prosjektstyring og regnskap** \> **Periodisk** \> **Project Operations-integrering** og velger **Importer fra oppsamlingstabell** for å kjøre den periodiske prosessen. Denne prosessen bruker de oppdaterte finansdimensjonsverdiene til å opprette prosjektfakturaforslagslinjene på nytt. De oppdaterte verdiene brukes deretter i underhovedboken for prosjektet og hovedboken når prosjektfakturaen posteres.
