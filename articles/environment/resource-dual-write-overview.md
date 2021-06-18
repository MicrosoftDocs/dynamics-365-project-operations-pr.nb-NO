---
title: Integrering av dobbel skriving for Project Operations
description: Dette emnet gir en oversikt over integrering av dobbel skriving for Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ce4f7bf8185e6f3f942df14d30d7b8d0a3e4444a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998693"
---
# <a name="project-operations-dual-write-integration-overview"></a>Oversikt over integrering av dobbel skriving for Project Operations

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Project Operations bruker [funksjoner for dobbel skriving](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) til å synkronisere data på tvers av Microsoft Dataverse og Dynamics 365 Finance.

Illustrasjonen nedenfor viser hvordan data synkroniseres som en del av denne integrasjonen mellom Dataverse og Finance.

![Oversikt over dataflyter for Project Operations](./media/ProjectOperationsFlows.jpg)

Project Operations i Dataverse gi et moderne brukergrensesnitt (UI) og enkel utvidelse med ingen kode / lav kode ved hjelp av Power Platform-funksjoner. Prosjektledere, ressursledere, prosjektteammedlemmer og andre personer på kontoret utfører aktivitetene sine i Project Operations på Dataverse.

Project Operations i Finance gir støtte for prosjektregnskap og inntektsføring. Project Operations kobles inn i det økonomiske rammeverket i Finance for beregning av salgsavgift, valutakurser, rapportering av finansielle dimensjoner og mer. Opplevelsene til prosjektregnskapsføreren er for det meste basert i Finans.

Integrering av Project Operations består av følgende komponentintegrering:


- [Integrering av Project Operations-oppsett og -konfigurasjonsdata](resource-dual-write-setup-integration.md) 
- [Prosjektestimater og faktiske verdier](resource-dual-write-estimates-actuals.md)
- [Prosjektfakturaer](resource-dual-write-project-invoice.md)
- [Utgiftshåndtering](resource-dual-write-expense.md)
- [Leverandørfaktura](resource-dual-write-vendor-invoice.md)
