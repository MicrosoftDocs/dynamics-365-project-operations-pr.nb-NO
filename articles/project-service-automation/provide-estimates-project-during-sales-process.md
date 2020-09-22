---
title: Gi arbeidsestimater for et prosjekt under salgsprosessen
description: Slik gir du arbeidsestimater for et prosjekt under salgsprosessen i Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 8e6fbba8-2908-4555-9470-43c37e66efea
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8edb91010dd1227bc7947b59664d08430c219638
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754173"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a>Gi arbeidsestimater for et prosjekt under salgsprosessen (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Under salgsprosessen, kan du arbeide ut salgsestimater fra grunnen med tilbudslinjene. [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-funksjoner i [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] gir en mer vitenskapelig og deterministisk måte å komme opp med salgsestimater på ved å bryte ned arbeidselementer og knytte sammen relevante attributter, som bidrar til estimater for prosjektet i arbeidsnedbrytningsstrukturen.  
  
 Når du vinner salget, kan du bruke den tilknyttede arbeidsnedbrytningsstrukturen i prosjektplanen og forbedre den etter behov for vellykket fullføring av prosjektet.  
  
## <a name="link-a-project-to-a-quote-line"></a>Koble et prosjekt til en tilbudslinje  
 Når du oppretter en prosjektbasert tilbudslinje, kan du opprette et nytt prosjekt fra tilbudslinjen. Deretter kan du bruke prosjektmaler som er forhåndskonfigurerte standard prosjektplaner og økonomiske estimater som er felles for organisasjonen, eller en kopi av en prosjektplan og estimater fra et tidligere prosjekt. Når du oppretter et prosjekt, velge en prosjektmal gir grunnlag for å finjustere planen, estimater og rollekravene. Ved å opprette prosjektet fra tilbudet er prosjektet automatisk knyttet til tilbudslinjen.  
  
## <a name="project-estimate-components"></a>Komponenter for prosjektestimat  
 Arbeidsnedbrytningsstrukturen i et prosjekt er en måte å dele opp arbeidet i aktiviteter, opprettholde et hierarki av aktiviteter og tilordne et overslag over innsats som kreves for å fullføre hver aktivitet. Du kan også knytte roller til en aktivitet for å angi et estimat av typen ressurs som kreves for å fullføre en aktivitet og en tidsplan.  
  
 Arbeidsnedbrytningsstrukturen hjelper deg med å bestemme arbeidsinnsats- og tidsplanestimater. Som standard bruker prosjektet standard prislister du definerte tidligere. Kostnadene og salgsprisene som er definert i prislistene, hjelper med å bestemme økonomiske estimater for prosjektets arbeidsnedbryting.  
  
 Hvis prosjektet er knyttet til et tilbud, og tilbudet har en annen prisliste enn standard, brukes tilbudets prisliste for økonomiske beregninger.  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a>Importere estimater fra et prosjekt til et tilbud  
 Når du har prosjektestimater i prosjektet, kan du importere disse estimatene til tilbudslinjen:  
  
-   I **Tilbudslinjedetaljer** klikker du **Importer fra estimater**. 

-   Velg om du vil importere prosjektestimater summert etter nodenivået transaksjonstype, rolle eller arbeidsnedbrytingsstruktur.  
  
### <a name="see-also"></a>Se også  
 [Prosjektlederhåndbok](../project-service/project-manager-guide.md)
