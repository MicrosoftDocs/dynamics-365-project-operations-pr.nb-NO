---
title: Periodetyper
description: Dette emnet gir informasjon om hvordan du konfigurerer periodetyper for inntektsestimat.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 07cc9cde5fab10accb1fd6efede58926918f614c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013498"
---
# <a name="period-types"></a>Periodetyper

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

En periodetype definerer hvor ofte inntekten på et prosjekt estimeres. Dette emnet gir informasjon om hvordan du konfigurerer periodetyper for inntektsestimat. 

## <a name="create-and-work-with-period-types"></a>Opprette og arbeide med periodetyper
Fullfør fremgangsmåten nedenfor for å opprette og arbeide med periodetyper:

1. I Dynamics 365 Finance-miljøet går du til Gå til **Prosjektstyring og regnskap** > **Oppsett** > **Estimater** > **Periodetyper**.
2. Hvis du vil opprette en ny periodetype, velger du **Ny**. Angi et navn og en beskrivelse.
3. Angi en verdi i feltet **Hyppighet**:

    - Hvis du velger **Uke**, **Annenhver uke**, **Halvmånedlig**, **Måned**, **Dag**, **Kvartal** eller **År**, brukes kalenderen til å generere periodene. 
    - Hvis du velger **Finansperiode**, brukes finansperioder fra Økonomimodul-konfigurasjonen til å generere perioder.
    - Hvis du velger **Ubegrenset**, kan du angi egendefinerte perioder.
4. Velg oppføring for periodetype, og velg deretter **Generer perioder** for å opprette perioder for periodetypen. Avhengig av periodefrekvensen du valgte, kan det hende at du har mulighet til å spesifisere en startdato eller antall perioder som skal genereres.
5. Velg **Perioder** for å gjennomgå genererte perioder.



[!INCLUDE[footer-include](../includes/footer-banner.md)]