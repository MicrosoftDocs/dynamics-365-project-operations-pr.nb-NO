---
title: Integrering av dobbel skriving for Project Operations
description: Dette emnet gir en oversikt over integrering av dobbel skriving for Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: b65c40e8aaa9524c1c634738dadd23f21e86e2ec095c47bc849467c8806addbc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007923"
---
# <a name="project-operations-dual-write-integration-overview"></a>Oversikt over integrering av dobbel skriving for Project Operations

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Project Operations bruker [funksjoner for dobbel skriving](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) til å synkronisere data på tvers av Microsoft Dataverse og Dynamics 365 Finance.

Illustrasjonen nedenfor viser hvordan data synkroniseres som en del av denne integrasjonen mellom Dataverse og Finance.

![Oversikt over dataflyter for Project Operations.](./media/ProjectOperationsFlows.jpg)

Project Operations i Dataverse gi et moderne brukergrensesnitt (UI) og enkel utvidelse med ingen kode / lav kode ved hjelp av Power Platform-funksjoner. Prosjektledere, ressursledere, prosjektteammedlemmer og andre personer på kontoret utfører aktivitetene sine i Project Operations på Dataverse.

Project Operations i Finance gir støtte for prosjektregnskap og inntektsføring. Project Operations kobles inn i det økonomiske rammeverket i Finance for beregning av salgsavgift, valutakurser, rapportering av finansielle dimensjoner og mer. Opplevelsene til prosjektregnskapsføreren er for det meste basert i Finans.

Integrering av Project Operations består av følgende komponentintegrering:


- [Integrering av Project Operations-oppsett og -konfigurasjonsdata](resource-dual-write-setup-integration.md) 
- [Prosjektestimater og faktiske verdier](resource-dual-write-estimates-actuals.md)
- [Prosjektfakturaer](resource-dual-write-project-invoice.md)
- [Utgiftshåndtering](resource-dual-write-expense.md)
- [Leverandørfaktura](resource-dual-write-vendor-invoice.md)
