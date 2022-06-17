---
title: Inntektsestimat for fastprisprosjekter
description: Denne artikkelen inneholder informasjon om fastprisinntekt på prosjekter.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3febb22397faa31222015231481d43fb0449d0a2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928398"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Inntektsestimat for fastprisprosjekter 

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Når du oppretter en prosjektkontraktlinje med følgende attributter i Dynamics 365 Project Operations på Microsoft Dataverse, oppretter systemet automatisk et inntektsestimat for fastprisprosjekt. Informasjonen i dette prosjektet er basert på følgende:

  - En faktureringsmåte med fast pris.
  - Et tilknyttet prosjekt.
  - Minst én milepæl som er definert i kategorien **Fakturaplan** på **Prosjektkontraktlinje**-siden.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Gjennomgå inntektsestimater for fastprisprosjekter
Følg fremgangsmåten nedenfor for å gjennomgå inntektsestimater for fastprisprosjekter:

1. I Dynamics 365 Finance-miljøet går du til **Prosjektstyring og regnskap** > **Prosjekter** > **Estimatprosjekter for fastprisomsetning**.
2. Velg prosjektet du vil vise, og dobbeltklikk på **Estimatprosjekt-ID** for å åpne oppføringen og gjennomgå detaljene for prosjektet.
3. Utvid **Prosjekt**-fanen. Du vil se ett prosjekt i **Valgte prosjekter**-rutenettet. Systemet bruker dette som standardprosjektet fordi det er prosjektet som er knyttet til prosjektkontraktlinjen. 
4. Hvis du vil endre tilknytningen, velger du flere prosjekter og legger dem til i **Valgte prosjekter**-rutenettet. Hvis flere prosjekter er valgt i dette rutenettet, blir prosjektets prosentfullføring og inntektsestimater beregnet sammen for alle de valgte prosjektene.

  Prosjektkostnad, inntektsprofil, kostnadsmal og periodekode kan angis manuelt. Hvis de ikke angis manuelt, blir verdiene som angitt som standard i den første estimatberegningen for prosjektet ved hjelp av reglene som er konfigurert for prosjektkostnad og inntektsprofiler.



[!INCLUDE[footer-include](../includes/footer-banner.md)]