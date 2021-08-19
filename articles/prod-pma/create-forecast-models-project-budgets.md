---
title: Opprette prognosemodeller for prosjektbudsjetter
description: Dette emnet beskriver hvordan du oppretter en prognosemodell for gjenstående budsjetter.
author: Yowelle
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: c4467bc1c687b028f1cce8280c3cf0b5ef492b6fd1a024d49f001ce5ff8a34cb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986008"
---
# <a name="create-forecast-models-for-project-budgets"></a>Opprette prognosemodeller for prosjektbudsjetter 

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du oppretter en prognosemodell for gjenstående budsjetter. Et prosjekt som er underlagt budsjettkontroll, bruker to typer budsjetter: opprinnelig og gjenstående. Når du oppretter et prosjektbudsjett, må du angi de opprinnelige og gjenværende budsjettprognosemodellene som ble opprettet på siden **Prognosemodeller**. Prosjektbudsjetter som er basert på de angitte modellene, blir opprettet når du vedtar prosjektbudsjettet.

> [!NOTE]
> En prognosemodell som brukes for budsjettkontroll, kan ikke ha en undermodell eller brukes som undermodell.

1. Velg **Prosjektstyring og regnskap** > **Oppsett** > **Prognoser**  > **Prognosemodeller**.
2. Velg **Ny** for å opprette en ny prognosemodell, og skriv deretter inn et ID-nummer for modellen og navnet på den nye modellen. 
3. Sett **Stoppet**-alternativet til **Ja** for å forhindre eventuelle endringer i prognoselinjer for prognosemodellen. 
4. Hvis prognoselinjene som modellen er knyttet til, må generere kontantstrømprognoser i hovedboken, må du sette **Inkluder i kontantstrømprognoser** til **Ja**. 
5. Hvis du vil bruke prosjektdatoen som fakturadato, setter du **Fakturadato for prognose** til **Ja**. 
6. I **Budsjettype**-feltet velger du én av følgende modelltyper:

   - **Opprinnelig budsjett**: Bruk de opprinnelige budsjettbeløpene som ble vedtatt da det opprinnelige budsjettet ble opprettet og godkjent.
   - **Gjenstående budsjett**: Bruk de gjenstående budsjettbeløpene i løpet av prosjektets levetid. Saldoene i denne prognosemodellen reduseres med faktiske transaksjoner, og økes eller reduseres etter budsjettendringer.
   - **Viderefør**: Bruk budsjettbeløpene for videreføring for prosjektet. Videreføring er en valgfri prosess som kan kjøres for å overføre ubrukte budsjettbeløp fra ett regnskapsår til et annet.

7. Angi følgende alternativer etter behov:

   - Aktiver **Fakturadato for prognose** hvis du vil bruke prosjektdatoen som fakturadato.
   - Aktiver **Prognose med VIA** for prognoser basert på varer i arbeid (VIA), og velg deretter type VIA. 
   - Du kan beholde standard **Budsjettype** som **Ingen** eller angi en ny type. Budsjettypen kan ikke endres etter at du har endret en oppføring.     
    > [!NOTE]
    > Hvis du endrer standard budsjettype, blir alle andre alternativer utilgjengelig for oppdateringer, og du kan ikke bruke denne prognosemodellen på nytt. 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]