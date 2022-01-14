---
title: Standardverdier for finansdimensjon
description: Dette emnet gir informasjon om hvordan du konfigurerer standardverdier for finansdimensjon.
author: sigitac
ms.date: 12/14/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8c1eb71d13ca7fc59118d15fef7ac914577b3b0e
ms.sourcegitcommit: fe5610464fdb5be756aa6a6a5b3c9a991dea0ed8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/15/2021
ms.locfileid: "7922950"
---
# <a name="financial-dimension-defaults"></a>Standardverdier for finansdimensjon

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations bruker [Finansdimensjoner](/dynamics365/finance/general-ledger/financial-dimensions)-rammeverket i Dynamics 365 Finance for å gi ytterligere innsikt i prosjekters underfinansjournal- og økonomimodultransaksjoner.

Standard finansdimensjoner kan angis for en kunde, et prosjektfinansieringskilde, milepæl, prosjektkontraktlinje eller prosjekt.

## <a name="define-default-financial-dimensions-for-a-customer"></a>Definere standard finansdimensjoner for en kunde

Kundedimensjonsstandarder er angitt i Finance. Fullfør følgende trinn for å konfigurere dimensjonsstandarder.

1. Gå til **Utestående fordringer** > **Kunder** > **Alle kunder**.
2. På siden **Kunder** i kategorien **Finansdimensjoner** angir du finansdimensjonsverdiene for en bestemt kunde.

## <a name="define-default-financial-dimensions-for-project-contracts"></a>Definere standard finansdimensjoner for prosjektkontakter

Prosjektkontrakter opprettes og vedlikeholdes i Common Data Service (CDS). Regnskapsattributter for prosjektkontrakter angis i **Prosjektstyring og regnskap**-modulen i Finance.

### <a name="set-financial-dimensions-for-a-project-funding-source"></a>Angi finansdimensjoner for en prosjektfinansieringskilde

1. Gå til **Prosjektstyring og regnskap** > **Prosjekter** > **Prosjektkontrakter**.
2. Velg oppføringen du vil oppdatere, og i kategorien **Prosjektkontrakt** velger du **Vis standardregnskap**.
3. Utvid **Relatert informasjon**, og velg kategorien **Finansieringskilder**.
4. Angi finansdimensjonsstandarder. Legg merke til at finansdimensjonene angis som standard fra kundekontoen.

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>Angi finansdimensjoner for en prosjektkontaktlinje

1. Gå til **Prosjektstyring og regnskap** > **Prosjekter** > **Prosjektkontrakter**.
2. Velg oppføringen du vil oppdatere, og i kategorien **Prosjektkontrakt** velger du **Vis standardregnskap**.
3. Utvid **Relatert informasjon**, og velg kategorien **Kontraktlinjer**.
4. Angi finansdimensjonsstandarder. Finansdimensjonsstandardene er relevante og kan bare brukes med kontraktlinjer med fast pris (milepæl).

Disse standardene brukes på relaterte prosjekt a konto-transaksjoner og fakturalinjer.

## <a name="define-default-financial-dimensions-for-projects"></a>Definere standard finansdimensjoner for prosjekter

Prosjekter opprettes og vedlikeholdes i CDS. Regnskapsattributter for prosjekter angis i **Prosjektstyring og regnskap**-modulen i Finance.

1. Gå til **Prosjektstyring og regnskap** > **Prosjekter** > **Alle prosjekter**.
2. Velg oppføringen du vil oppdatere, og i kategorien **Prosjekt** velger du **Vis standardregnskap**.
3. Utvid **Relatert informasjon**, og velg kategorien **Oppsett**.
4. Angi finansdimensjonsstandarder. Legg merke til at finansdimensjonene angis som standard fra kundekontoen. Hvis prosjektet er knyttet til en kontraktlinje med flere prosjektkontraktkunder, brukes hovedkunden som standard for finansdimensjoner.

Standardfinansdimensjoner for prosjekt brukes til å angi standarder for journallinje for tid, utgift og avgiftstransaksjoner i **Journal for Project Operations-integrering** og på relaterte prosjektfakturalinjer.

## <a name="apply-financial-dimensions-for-project-time-entries"></a>Bruke finansdimensjoner for prosjekttidsoppføringer
Hvis du vil bruke finansdimensjoner for prosjekttidsoppføringer, må du være oppmerksom på at standard dimensjonsverdi er basert på følgende rekkefølge:

1. Ressurs
2. Project
3. Finansieringskilde

Hvis standarddimensjonen for eksempel er angitt for en ressurs, brukes den over en standard som er angitt på prosjektet. På samme måte brukes en standard prosjektdimensjon over standardinnstillingen som er angitt i finansieringskilden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
