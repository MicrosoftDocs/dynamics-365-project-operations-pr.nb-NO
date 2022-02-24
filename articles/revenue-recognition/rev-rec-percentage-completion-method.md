---
title: Inntektsestimat for fastprisprosjekter
description: Dette emnet gir informasjon om fastprisinntekt i prosjekter.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 80fe1d4171d80ca39e8b7ebb1eefaa524a4f2b07
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531510"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Inntektsestimat for fastprisprosjekter 

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Når du oppretter en prosjektkontraktlinje med følgende attributter i Dynamics 365 Project Operations på Microsoft Dataverse, oppretter systemet automatisk et inntektsestimat for fastprisprosjekt. Informasjonen i dette prosjektet er basert på følgende:

  - En faktureringsmåte med fast pris.
  - Et tilknyttet prosjekt.
  - Minst én milepæl som er definert i kategorien **Fakturaplan** på **Prosjektkontraktlinje**-siden.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Gjennomgå inntektsestimater for fastprisprosjekter
Følg fremgangsmåten nedenfor for å gjennomgå inntektsestimater for fastprisprosjekter:

1. I Dynamics 365 Finance-miljøet går du til **Prosjektstyring og regnskap** > **Prosjekter** > **Inntektsestimat for fastprisprosjekter**.
2. Velg prosjektet du vil vise, og dobbeltklikk på **Estimatprosjekt-ID** for å åpne oppføringen og gjennomgå detaljene for prosjektet.
3. Utvid **Prosjekt**-fanen. Du vil se ett prosjekt i **Valgte prosjekter**-rutenettet. Systemet bruker dette som standardprosjektet fordi det er prosjektet som er knyttet til prosjektkontraktlinjen. 
4. Hvis du vil endre tilknytningen, velger du flere prosjekter og legger dem til i **Valgte prosjekter**-rutenettet. Hvis flere prosjekter er valgt i dette rutenettet, blir prosjektets prosentfullføring og inntektsestimater beregnet sammen for alle de valgte prosjektene.

  Prosjektkostnad, inntektsprofil, kostnadsmal og periodekode kan angis manuelt. Hvis de ikke angis manuelt, blir verdiene som angitt som standard i den første estimatberegningen for prosjektet ved hjelp av reglene som er konfigurert for prosjektkostnad og inntektsprofiler.

