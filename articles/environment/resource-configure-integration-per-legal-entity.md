---
title: Konfigurere Project Operations-integrering per juridisk enhet
description: Dette emnet gir informasjon om hvordan du konfigurerer integrering per juridisk enhet i Project Operations.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 64606a20a49fd8e9602b6ac3c1ab1880796eb128
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585850"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Konfigurere Project Operations-integrering per juridisk enhet 

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Dette emnet veileder deg gjennom trinnene som kreves for å konfigurere Dynamics 365 Project Operations per juridisk enhet.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Aktiver funksjonsnøkler i Dynamics 365 Finance

Fullfør fremgangsmåten nedenfor for å aktivere nødvendige funksjoner.

1. I Dynamics 365 Finance går du til arbeidsområdet **Funksjonsbehandling**.
2. Søk etter og aktiver følgende funksjoner i **funksjonslisten**:
  
    - **Aktiver flere kontraktlinjer for et prosjekt**
    - **Aktiver Project Operations i Dynamics 365 Customer Engagement**

> [!NOTE]
> Hvis du ikke ser **Funksjonsnøkler**, må du kontrollere at Finance-versjonen oppfyller minimumskravene for versjon (programversjon 10.0.13 med alle kvalitets oppdateringer brukt, eller nyere). Velg **Se etter oppdateringer** for å oppdatere funksjonslisten.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Definere Project Operations-distribusjonsscenarioet for en juridisk enhet

Du kan aktivere Project Operations i Dynamics 365 Customer Engagement på et juridisk enhetsnivå. Du kan ha én juridisk enhet som bruker Project Operations i Dynamics 365 Customer Engagement for ressursbaserte/ikke-lagerbaserte scenarioer. I det samme miljøet kan du ha en ny juridisk enhet som bruker Project Operations til lagerførte scenarioer / produksjonsordrescenarier.

1. I Dynamics 365 Finance går du til **Prosjektstyring og regnskap** > **Oppsett** > **Globale parametere for prosjektstyring og regnskap**.
2. I listen over tilgjengelige juridiske enheter velger du enheter der flere kontraktlinjer og Project Operations-funksjoner i Dynamics 365 Customer Engagement skal bli aktivert. La juridiske enheter som skal bruke Project Operations for lagerførte scenarioer / produksjonsordrescenarioer, være umerket.

> [!NOTE]
> En juridisk enhet kan bare velges hvis den ikke har noen eksisterende prosjekter.

## <a name="configure-project-management-and-accounting-parameters"></a>Konfigurere parametere for prosjektstyring og regnskap

Hver juridisk enhet som bruker Project Operations i Dynamics 365 Customer Engagement, trenger et sett med standardparametere. Disse parameterne konfigureres på **Project Operations**-fanen på siden **Parametere for prosjektstyring og regnskap**. Parameterne er:

  - **Faktureringstypestandarder**: Project Operations bruker et fast sett med faktureringstypestandarder som må tilordnes til linjeegenskaper i Finance. Opprett en oppføring for hver faktureringstype: **Ikke angitt**, **Belastbar**, **Ikke-belastbar**, **Gratis** og **Ikke tilgjengelig**.
  - **Prosjektkategoristandarder**: Velg standard prosjektkategorier som skal brukes for hver transaksjonstype. Disse standardene brukes i **Journal for Project Operations-integrering** og i beregninger der det ikke er angitt en transaksjonskategori for det faktiske prosjektet.
  - **Prognoser**: Velg prognosemodellen som skal brukes for tids- og utgiftsestimater.


[!INCLUDE[footer-include](../includes/footer-banner.md)]