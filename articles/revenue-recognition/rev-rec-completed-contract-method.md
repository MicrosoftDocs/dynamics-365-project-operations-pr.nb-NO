---
title: Administrere inntektsestimater
description: Dette emnet gir informasjon om hvordan du arbeider med inntektsestimater for prosjekter.
author: sigitac
ms.date: 11/04/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 6f91a0eb6fa0d13ebe8dfb6e837dae0bbff3eb5e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595878"
---
# <a name="manage-revenue-estimates"></a>Administrere inntektsestimater

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Du kan opprette, beregne, postere, tilbakeføre eller eliminere inntektsestimater. Du kan gjøre dette manuelt eller ved hjelp av en periodisk prosess. Dette emnet gir informasjon om hvordan du arbeider med inntektsestimater for prosjekter.

### <a name="manage-revenue-estimates-manually"></a>Administrere inntektsestimater manuelt

På estimatprosjekt for fastprisinntekt eller **Estimatforespørsel**-siden (**Prosjektstyring og regnskap** > **Rapporter og forespørsler** > **Estimatforespørsler og rapporter**), velger du **Estimater**.

### <a name="manage-revenue-estimates-using-a-periodic-process"></a>Administrere inntektsestimater ved hjelp av en periodisk prosess

Gå til **Prosjektstyring og regnskap** > **Periodisk** > **Estimater**, og velg den tilsvarende prosessen.

## <a name="create-a-revenue-estimate"></a>Opprette et inntektsestimat

Følg fremgangsmåten nedenfor for å opprette et inntektsestimat. 

1. Gå til **Prosjektstyring og regnskap** > **Periodisk** > **Estimater**.
2. Velg **Ny**. På **Estimatoppretting**-siden velger du følgende parametere:

   - **Periodekode** : Denne koden avgjør hvor ofte estimater skal posteres.
   - **Dato for estimat**: Datoen estimatet behandles.
   - **Kontinuerlig**: Merk av i denne boksen for å opprette estimater bare hvis estimater ble postert i forrige periode, eller hvis estimatet er det første estimatet som er opprettet. Hvis det ikke er merket av for dette alternativet, opprettes estimater selv om det ikke ble postert estimater i forrige periode.
   - **Metode for ferdigstillingskostnad**: Definer hvordan det gjenstående prosjektarbeidet skal estimeres. Hvis du vil ha mer informasjon, kan du se [Metoder for ferdigstillingskostnad](cost-complete-methods.md).
   - **Fullføringsmetode**: Velg en fullføringsmetode fra følgende alternativer:
     - **Automatisk**: Fullføringsprosenten beregnes automatisk og baseres på kostnadslinjene som er inkludert i beregningen. Kostnadsmalen definerer kostnadslinjene som er inkludert.
     - **Manuell**: Fullføringsprosenten tilsvarer fullføringsprosenten for det siste estimatet. Når du har opprettet estimatet, kan du endre den **Manuelle beregningen** på **Estimater**-siden.
     - **Fra kostnadsmal**: En kombinasjon av den automatiske og manuelle metoden. Dette alternativet angis automatisk eller manuelt, avhengig av standardverdien i kostnadsmalen.
   - **Prognosemodell**: Velg en prognosemodell for estimatet.
   - **Skriv ut estimatliste**: Opprett og vis en estimatliste. Listen inneholder statusen for gjeldende funksjon. Du kan skrive ut alle advarsler om estimatet på rapporten. Følgende betingelser fører til at advarsler vises i estimatlisten:
     - En fullføringsprosent på mer enn 100 prosent.
     - En fullføringsprosent på mindre enn null prosent.
     - Et negativt beløp i **Som skal fylles ut**-kolonnen.
     - Et estimat uten tilsvarende kontraktbeløp.
     - Et estimat uten et tilknyttet kostnadsestimat.
   - **Vis infologg**: Velg dette alternativet for å motta en melding som inneholder informasjon om estimatprosjektene som ble behandlet da jobben ble kjørt.


## <a name="post-wip-or-accruals"></a>Postere VIA eller avsetninger

Når estimatene er evaluert, blir de vedlikeholdt, redusert eller økt. Du kan deretter postere VIA-en når du arbeider med **Fullført kontrakt**-oppgjørsprinsippet, eller du kan postere avsetningene når du arbeider med **Fullføringsprosent**-oppgjørsprinsippet.
  
Statusen for estimatperioden endres fra **Opprettet** til **Postert**.

## <a name="reverse-wip-or-accruals"></a>Tilbakefør VIA eller avsetninger

Bruk tilbakefør-alternativet for å kreditere allerede posterte VIA eller avsetninger, og opprett deretter estimater for perioden.

> [!NOTE]
> Hvis du vil tilbakeføre en periode som er mellom andre perioder, tilbakefører du de nødvendige estimatperiodene og posterer dem på nytt. Siden alle påfølgende perioder avhenger av estimatene fra forrige periode, kan du ikke hoppe over perioder.

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a>Eliminere estimatprosjektet og fullføre prosjektet

Det siste trinnet i estimatprosessen er å eliminere estimatprosjektet og avslutte fastprisprosjektet når fullføringsprosenten når 100 prosent.

Dette skjer når du kjører elimineringen:

- For et fastprisprosjekt med et fullført prosjekt, fjernes VIA-verdiene fra balansekontoene og posteres til resultatkontoene.
- For et fastprisprosjekt med en fullføringsprosent, blir avsetningene fjernet fra resultatkontoene.

Estimatet endrer statusen til **Eliminert**.

> [!NOTE]
> I spesielle tilfeller kan prosentandelen gå over 100 prosent. Når dette skjer, reduserer du fullføringsprosenten ved å bruke **Sett kostnaden som skal fullføres, til null-metoden** til å nå 100 prosent.

## <a name="reverse-elimination"></a>Tilbakefør eliminering

1. Gå til **Prosjektstyring og regnskap** > **Periodisk** > **Estimater** > **Tilbakefør eliminering**. 
2. På Handlingsruten på **Prosess**-fanen i **Vedlikehold**-gruppen, velger du **Estimer**. 
3. Velg **Tilbakefør eliminering**.

Bruk denne siden til å tilbakeføre alle elimineringer med en bestemt estimatdato og med estimatstatusen **Eliminert**. Transaksjonsstatusen endres etter at du har valgt de riktige feltene.

Dette endrer også prosjektstatusen til **Pågår** hvis prosjektfasen er satt til ferdig. Estimatstatusen for prosjektperioden endres tilbake til **Postert**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]