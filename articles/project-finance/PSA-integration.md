---
title: Oversikt over Project Service Automation
description: Dette emnet gir informasjon om Dynamics 365 Project Service Automation til Dynamics 365 Finance-integreringsløsningen.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 897e1a1c-d31c-42b8-bb59-6b67202d8d61
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 080a545d8713e52d9778367aec1969b815d683e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754138"
---
# <a name="project-service-automation-overview"></a>Oversikt over Project Service Automation

[!include[banner](../includes/banner.md)]

Project Service Automation til Finance-integreringsløsningen bruker funksjonen for dataintegrering til å synkronisere data på tvers av forekomster av Dynamics 365 Finance og Dynamics 365 Project Service Automation via Common Data Service. Integreringsmalene som er tilgjengelige med funksjonen for dataintegrering, muliggjør dataflyten om prosjekter, prosjektkontrakter, prosjektkontraktlinjer, milepæler for prosjektkontraktlinjer, prosjektoppgaver, utgiftstransaksjonskategorier, timeestimater og utgiftsestimater fra Project Service Automation til Finance.

> [!NOTE]
> - Hvis du bruker versjon 7.3.0, må du installere KB 4074835. Deretter kan du integrere fastprisprosjekter.
> - Hvis du bruker versjon 7.3.0 og overfører gebyrtransaksjoner fra Project Service Automation, må du installere KB 4345320 for å kunne ta med de avgiftene i prosjektfakturaen.
> - Hvis du bruker versjon 8.0, kan du bruke prosjektoppgaveintegrering, utgiftstransaksjonskategorier, timeoverslag, utgiftsoverslag og låsing av funksjoner.
> - Hvis du bruker versjon 8.0.1 eller senere, vil du kunne synkronisere faktiske verdier.

Før du kan integrere Project Service Automation Finance, må du konfigurere integrasjonsparameterne for Project Service Automation. For mer informasjon, se [Integrasjonsparametere for Project Service Automation](PSA-parameters.md).

Denne integreringsløsningen aktiverer direkte synkronisering i følgende scenarioer:

- Vedlikehold prosjektkontrakter i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.
- Opprett prosjekter i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.
- Vedlikehold prosjektkontraktlinjer i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.
- Vedlikehold milepæler for prosjektkontraktlinje i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.
- Vedlikehold prosjektoppgaver i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.
- Vedlikehold utgiftstransaksjonskategorier i Finance, og synkroniser dem direkte fra Finance til Project Service Automation.
- Opprett prosjekttimeestimater i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.
- Opprett prosjektutgiftestimater i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.
- Opprett faktiske verdier for prosjekttid, utgift og avgift i Project Service Automation, og opprett prosjekttransaksjoner i Project Service Automation-integrasjonsjournalen, slik at de kan posteres i Finance.

## <a name="data-synchronization"></a>Datasynkronisering

Illustrasjonen nedenfor viser hvordan data synkroniseres som en del av integrasjonen mellom Project Service Automation og Finance.

> [!NOTE]
> Ikke alle maler er tilgjengelige for øyeblikket. Maler blir frigjort etter hvert som de fullføres.

[![Project Service Automation-integrasjon med Finance](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Systemkrav for Finance

Hvis du vil bruke Project Service Automation til Finance-integrasjonsløsningen, må du installere Enterprise Edition 7.3 med Platform Update 12 eller senere.

## <a name="system-requirements-for-project-service-automation"></a>Systemkrav for Project Service Automation

Hvis du vil bruke Project Service Automation til Finance-integreringsløsningen, må du installere følgende komponenter:

- Dynamics 365 Project Service Automation9.0.0.0 eller nyere
- Kundeemne til kontantløsning for Dynamics 365 Sales, versjon 1.14.0.0 (v14) eller senere
- Project Service Automation til Finance-løsning for Dynamics 365 Project Service Automation versjon 1.0.0.0 eller senere

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Installer Project Service Automation til Finance-integreringsløsningen i Project Service Automation-forekomsten

Last ned Project Service Automation til Finance-integreringsløsningen fra [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), og følg instruksjonene som er inkludert i løsningen.
