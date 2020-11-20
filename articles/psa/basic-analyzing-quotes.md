---
title: Analyse av prosjekttilbud
description: Dette emnet gir informasjon om analyse av prosjekttilbud.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6ed900620f92e76d293f6b533b101be94b25cff3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127035"
---
# <a name="analysis-of-project-quotes"></a>Analyse av prosjekttilbud

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation analyserer prosjekttilbud for å beregne lønnsomhet. Det analyseres også hvor godt tilbudet er justert mot kundens forventninger om leveringsdato eller fullføringsdato, og om budsjettbegrensningene.

## <a name="profitability-analysis"></a>Lønnsomhetsanalyse

Project Service Automation analyserer lønnsomhet ved å bruke bruttofortjenesten og den justerte bruttofortjenesten.

- Bruttofortjeneste beregnes ved å bruke følgende formel:

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- Den justerte bruttofortjenesten beregnes ved å bruke følgende formel:

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

Hvis verdiene for bruttofortjeneste og justert bruttofortjeneste varierer med en stor margin, blir mye av arbeidet i tilbudet klassifisert som ikke-belastbart.

## <a name="analysis-of-customer-expectations"></a>Analyse av kundeforventninger

Du kan analysere tilbud og generere diagrammer for kundeforventninger om tidsplanen og budsjettet hvis du angir verdier for følgende felt:

- **Ønsket leveringsdato**-feltet i tilbudshodet.
- **Kundebudsjett**-feltet for hver tilbudslinje (for prosjektrelaterte linjer og produktbaserte linjer).

Analyse av kundeforventninger om tidsplanen utføres ved å sammenligne den siste sluttdatoen for tilbudslinjedetaljene med den ønskede leveringsdatoen i alle tilbudslinjene i tilbudet.

Analyse av kundeforventninger til budsjettet gjøres ved å sammenligne summen av det totale kundebudsjettet med det tilbudte beløpet på tvers av alle tilbudslinjer.
