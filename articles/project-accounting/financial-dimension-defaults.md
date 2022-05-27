---
title: Standardverdier for finansdimensjon
description: Dette emnet gir informasjon om hvordan du konfigurerer standardverdier for finansdimensjon.
author: sigitac
ms.date: 12/14/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9f43fed57a1411a55dcd7929f34e87aed136a6b5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579502"
---
# <a name="financial-dimension-defaults"></a>Standardverdier for finansdimensjon

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_



Dynamics 365 Project Operations bruker rammeverket [Finansdimensjoner](/dynamics365/finance/general-ledger/financial-dimensions) i Dynamics 365 Finance til å gi ytterligere innsikt om underfinanstransaksjoner for prosjekter og økonomitransaksjoner.

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

[!INCLUDE[footer-include](../includes/footer-banner.md)]
