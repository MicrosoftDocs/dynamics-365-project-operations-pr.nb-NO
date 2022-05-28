---
title: Økonomiske estimater for ressurstid på prosjekter
description: Dette emnet inneholder informasjon om hvordan finansielle estimater for tid beregnes.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: aab5c11a7dc23331c935403a4f96ec7197ec1572
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592566"
---
# <a name="financial-estimates-for-resource-time-on-projects"></a>Økonomiske estimater for ressurstid på prosjekter

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Økonomiske estimater for tid beregnes basert på tre faktorer: 

- Typen generisk eller navngitt teammedlem som er tilordnet hver bladnodeoppgave i prosjektplanen. 
- Typen eller kompleksiteten til arbeidet.
- Innsatsspredningen for ressursens tilordning av aktiviteten 

De to første faktorene har innflytelse på enhetskostnaden eller fakturasatsen for tilordningen til en ressurs. Enhetskostnaden eller fakturasatsen for en ressurstilordning fastsettes av attributtene til den tilordnede ressursen. Disse attributtene inkluderer organisasjonsenheten som ressursen tilhører, og standardrollen for ressursen. Du kan også legge til egendefinerte attributter som er relevante for virksomheten for ressursen, for eksempel standardtittel eller erfaringsnivå, og få dem til å påvirke enhetskostnaden eller fakturasatsen for tilordningen.
I tillegg til attributtene for ressursen kan arbeidsattributter, for eksempel aktiviteten, også ha innflytelse på enhetsfakturasatsen eller kostnadssatsen for tilordningen. Når enkelte oppgaver for eksempel er mer komplekse, fører ressursens tilordning til de bestemte oppgavene til en høyere enhetskostnad eller fakturasats enn oppgaver som er mindre komplekse.   

Den tredje faktoren angir antall timer med denne satsen. I tilfeller der en aktivitet dekker to prisperioder, er det sannsynlig at den første delen av ressurstilordningen for den aktiviteten er kostnadskrevende og priset på en annen del av aktiviteten. Innsatsestimatet for hver ressurstilordning er en kompleks verdi lagret med den daglige distribusjonen av innsats per dag.

Hvis du vil ha detaljerte instruksjoner om hvordan du konfigurerer egendefinerte attributter for arbeid og ressurser som pris- og kostnadsdimensjoner, kan du se [Oversikt over prisdimensjoner](../pricing-costing/pricing-dimensions-overview.md).

Det økonomiske estimatet for hver ressurstilordning beregnes som **sats/time for tilordningen multiplisert med antall timer.**  På samme måte som innsatsestimatet er det økonomiske estimatet for kostnader og omsetning for hver ressurstilordning en kompleks verdi lagret med den daglige distribusjonen av pengebeløp per dag. 

## <a name="summarizing-financial-estimates-for-time"></a>Oppsummere finansielle estimater for tid
Et økonomisk estimat for tid på en bladnodeoppgave er summen av de økonomiske estimatene for alle ressurstilordninger for den oppgaven.

Et økonomisk estimat for tid på sammendragsoppgave eller overordnet oppgave er summen av alle de underordnede oppgavene. Dette er den estimerte arbeidskostnaden for prosjektet. 

![Ressursestimater.](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Standard kostpris og kostnadsvaluta

Standard kostnadspris kommer fra prislistene som er vedlagt kontraktenheten for prosjektet. Kostnadsvalutaen for et prosjekt er alltid valutaen til kontraktsenheten for prosjektet. I en ressurstilordning lagres det økonomiske kostnadsestimatet i kostnadsvalutaen for prosjektet. Noen ganger er valutaen som er definert for kostnadssatsen i prislisten, forskjellig fra prosjektkostnadsvalutaen. I slike tilfeller konverterer programmet valutaen som kostnadsprisen er angitt i, for valutaen for prosjektet. I **Estimater**-rutenettet vises alle kostnadsestimater og oppsummeres i prosjektets kostnadsvaluta. 

## <a name="default-bill-rate-and-sales-currency"></a>Standard fakturasats og salgsvaluta

Standard salgspris kommer fra prosjektprislistene som er vedlagt den relaterte prosjektkontrakten hvis avtalen blir vunnet, eller fra det relaterte prosjekttilbudet hvis avtalen fremdeles er i fasen før salg. Salgsvalutaen for prosjektet er alltid valutaen til prosjekttilbudet eller prosjektkontrakten. I en ressurstilordning lagres det økonomiske salgsestimatet i salgsvalutaen for prosjektet. I motsetning til kostnader kan ikke salgsprisen som er angitt i prislisten, være forskjellig fra salgsvalutaen for prosjektet. Det finnes ikke noe scenario der valutakonvertering er nødvendig. I **Estimater**-rutenettet vises alle salgsestimater og oppsummeres i prosjektets salgsvaluta. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
