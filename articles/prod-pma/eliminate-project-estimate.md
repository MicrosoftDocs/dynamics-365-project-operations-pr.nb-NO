---
title: Eliminere et prosjektestimat
description: Dette emnet gir informasjon om å eliminere et prosjektestimat etter at det er fullført.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
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
ms.openlocfilehash: 000eabdac41f30a6e7dd37e34b8fd91d7c51f6c4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270690"
---
# <a name="eliminate-a-project-estimate"></a>Eliminere et prosjektestimat

[!include [banner](../includes/banner.md)]

Prosjektestimater gir en økonomisk oversikt for arbeid som beregnet og planlagt for et prosjekt. Hvis du vil arbeide med estimater for et prosjekt, må du legge ved prosjektet i et estimatprosjekt. Et estimatprosjekt er alltid basert på et eksisterende prosjekt, men flere prosjekter kan referere til et enkelt estimatprosjekt. Bare fastprisprosjekter og investeringsprosjekter kan knyttes til estimatprosjekter, og disse prosjektene må tilhøre samme prosjektgruppe som estimatprosjektet.

Hvis du vil eliminere et estimatprosjekt, må det være fullført. Fremgangsmåten nedenfor forklarer hvordan du eliminerer et estimat.

1. Gå til **Prosjektstyring og regnskap** > **Alle prosjekter**, og åpne prosjektet. 
2. På **Administrer**-fanen velger du **Estimatrs**, og på **Estimat**-siden velger du **Eliminer**.
3. På siden **Eliminer estimat**, på **Generelt**-fanen angir du følgende alternativer:

   - **Periodekode**: Velg periodekoden for å velge de aktuelle estimatprosjektene. 
   - **Estimatdato**: Velg den aktuelle estimatdatoen for eliminering.
   - **Eliminer med VIA-advarsler**: Aktiver dette alternativet for å gi beskjed når et estimat som er knyttet til pågående arbeid (VIA), blir eliminert. Når det ikke er merket av for dette alternativet, kan ikke eliminering fortsette hvis det ikke finnes noen ikke-estimerte transaksjoner. 
   > [!NOTE]
   > Dette alternativet er bare tilgjengelig når eliminering brukes på et estimatprosjekt. Det er ikke tilgjengelig hvis du bruker periodiske posteringer. Denne innstillingen fungerer med innstillingene på **Estimat**-fanen på siden **Prosjektparametere** i feltgruppen **Tillat eliminering når det finnes ikke-estimerte transaksjoner**.
   - **Angi fase til fullført**: Aktiver dette alternativet for å angi estimatprosjektets fase til **Fullført** etter at du har kjørt elimineringen.
   - **Skriv ut estimatliste**: Velg informasjonen som skal inkluderes når estimatlisten skrives ut.
   - **Vis infologg**: Aktiver dette alternativet for å vise infologgen.
   - **Bokføringsdato**: Velg bokføringsdatoen i hovedboken for estimatet.

4.  Velg **OK**.
5. Når elimineringsprosessen er fullført, vises det eliminerte estimatprosjektet med en negativ verdi. 

Hvis du ikke har tenkt å eliminere et estimat, kan du velge det eliminerte estimatet og velge **Gjør om eliminering**.   


[!INCLUDE[footer-include](../includes/footer-banner.md)]