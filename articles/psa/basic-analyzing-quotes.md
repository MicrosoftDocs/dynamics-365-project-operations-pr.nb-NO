---
title: Analyse av prosjekttilbud
description: Dette emnet gir informasjon om analyse av prosjekttilbud.
author: rumant
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
ms.openlocfilehash: acb3f1a2020cfd59f60f828e9092bd7ccde00077
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012463"
---
# <a name="analysis-of-project-quotes"></a>Analyse av prosjekttilbud

[!include [banner](../includes/psa-now-project-operations.md)]

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]