---
title: Opprette prognosemodeller for prosjektbudsjetter
description: Dette emnet beskriver hvordan du oppretter en prognosemodell for gjenstående budsjetter.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
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
ms.openlocfilehash: 5a3b9d3c154a85b50536a67ae0eb45d9b4f25f15
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271050"
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