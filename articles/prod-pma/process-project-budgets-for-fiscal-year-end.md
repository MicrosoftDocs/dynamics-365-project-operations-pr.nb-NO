---
title: Overføre prosjektbudsjetter ved regnskapsårets slutt
description: Denne artikkelen inneholder informasjon om hvordan gjenstående budsjettbeløp skal overføres til fremtidige år, og oppretting av detaljer for budsjettregisteret.
author: Yowelle
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 74b2831a19688636f5c4863036adf7043c80d49829737b56c131abb6998d6cb3
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007383"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Overføre prosjektbudsjetter ved regnskapsårets slutt

[!include [banner](../includes/banner.md)]

Når du arbeider med et prosjekt over flere år, kan det hende at gjenstående budsjett vises på slutten av regnskapsåret. Du kan overføre de gjenstående budsjettbeløpene til et fremtidig år, og du kan opprette budsjettregisterdetaljer for beløpene i de tilknyttede kontoene i hovedboken. Før du overfører de resterende beløpene, kan du se gjennom og analysere de gjenstående budsjettbeløpene.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Se gjennom og analysere gjenstående budsjettbeløp

Fullfør fremgangsmåten nedenfor for å se gjennom budsjettbeløpene ved årets slutt for prosjekter, men ikke overføre beløpene.

1. Gå til **Prosjektstyring og regnskap** > **Periodisk** > **Budsjetter** > **Viderefør budsjetter**. 
2. På siden **Videreføringsprosess for prosjektbudsjett**, på fanen **Alternativer for årsavslutning**, verifiserer du at **Viderefør gjenstående prosjektbudsjettbeløp** ikke er aktivert.
3. På **Parametere**-fanen, i **Prosjektbudsjettår**-feltet, velger du regnskapsåret du vil vise det resterende budsjettbeløpet for. 
4. I feltet **Første regnskapsår** velger du regnskapsåret du vil vise det resterende budsjettbeløpet for. 
5. I feltet **Fra prognosemodell** velger du **Gjenstående budsjett**. 
6. Hvis du vil inkludere prosjekter som oppfyller de valgte vilkårene, og som ikke har noe gjenstående budsjett, velger du **Vis null gjenstående**.  
7. I kategorien **Velg budsjetter** velger du **Hent alle budsjetter** for å laste alle budsjetter som samsvarer emd de valgte kriteriene, og velg deretter **Behandle**. 
8. Hvis du vil utforme en databasespørring som laster inn et bestemt sett med budsjetter iruten, velger du **Hent valgte budsjetter**.

Hvis du vil ha mer informasjon om en bestemt linje i ruten, velger du linjen, og deretter velger du **Vis budsjettdetaljer** eller **Vis kontoer**.

## <a name="carry-forward-remaining-budget-amounts"></a>Videreføre gjenstående budsjettbeløp 

Når du behandler gjenstående budsjettbeløper, kan du opprette transaksjoner i hovedboken for beløpene du viderefører. Hvis du vil opprette hovedboktransaksjoner, full fører du trinnene i delen [Videreføre budsjettbeløp og opprette hovedboktransaksjoner](#carry-forward). 

> [!NOTE]
> Budsjettbeløp som videreflres, overføres til prognosemodellen som er valgt på siden **Prognosemodeller** som prognosemodellen for videreføringen.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Videreføre budsjettbeløp og opprette hovedboktransaksjoner

1.  Velg **Prosjektstyring og regnskap** > **Periodisk** > **Budsjetter** > **Viderefør budsjetter**. 
2. På siden **Videreføringsprosess for prosjektbudsjett** velger du **Årsavslutning**, og aktiver deretter **Viderefør gjenstående prosjektbudsjettbeløp** og **Opprett budsjettregisteroppføringer i hovedbok**. 
3. På **Parametere**-fanen, i feltgruppen **Prosjektparametere**, velger du følgende:

   - **Prosjektbudsjettår**: Velg begynnelsen for regnskapsåret du vil vise de resterende budsjettbeløpene for. 
   - **Resultat**: Opprett resultattransaksjoner i hovedboken. 
   -  **VIA**: Opprett VIA-transaksjoner (varer i arbeid) i hovedboken.
   -  **Lønn**: Opprett lønnstildelingstransaksjoner i hovedboken. 

5. I feltgruppen **Hovedbok** oppgir du følgende informasjon: 

   - I feltet **Første regnskapsår** velger du regnskapsåret du vil overføre de resterende budsjettbeløpene til, for prosjektene. Standardverdien er ett år etter verdien i feltet **Prosjektbudsjettår**.
   -  I feltet **Videreføringsperiode** velger du perioden du vil opprette budsjettregisterdetaljer for, i hovedboken. Dette er vanligvis den første perioden i det første regnskapsåret.

6. I feltgruppen **Kopier fra/til** oppgir du følgende informasjon:

   - I feltet **Fra prognosemodell** velger du prosjektbudsjettprognosemodellen som er knyttet til de gjenstående budsjettbeløpene du vil overføre for prosjektene. 
   - I feltet **Til hovedbokbudsjettmodell** velger du hovedbokbudsjettmodellen som er knyttet til de gjenstående budsjettbeløpene du vil overføre til hovedboken. 
   -  Velg **Overfør salgsvaluta** for å bruke prosjektets salgsvaluta for hovedboktransaksjonene som opprettes når du overfører budsjettbeløpene for prosjektene. Når det ikke er merket av for alternativet, bruker transaksjonene regnskapsvalutaen. 
   -  Velg **Vis null gjenstående** for å inkludere prosjekter som ikke har gjenstående budsjettbeløp, men som oppfyller de andre kriteriene du velger i prosjektene som vises i den nederste ruten.

7. I kategorien **Velg budsjetter** velger du **Hent alle budsjetter** for å laste alle budsjetter som samsvarer med kriteriene du har valgt. Hvis du foretrekker å utforme en databasespørring som laster inn et bestemt sett med prosjektbudsjetter i ruten, velger du **Hent valgte budsjetter**.
8. For hvert prosjekt du vil behandle, velger du alternativet i begynnelsen av linjen for prosjektet.

    > [!TIP]
    > Hvis du vil velge alle eller de fleste prosjektene, merker du av øverst til venstre. Hvis du vil utelate behandlingen av et prosjekt, fjerner du merket for dette prosjektet.

9. Hvis du vil overføre de gjenstående budsjettbeløpene for de valgte prosjektene til det valgte regnskapsåret og opprette budsjettregisterdetaljer i hovedboken, velger du **Behandle**.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Videreføre budsjettbeløp uten å opprette hovedboktransaksjoner

1. Gå til **Prosjektstyring og regnskap** > **Periodisk** > **Budsjetter** > **Viderefør budsjetter**.
2. På siden **Videreføringsprosess for prosjektbudsjett**, i feltet **Alternativer for årsavslutning**, velger du **Viderefør gjenstående prosjektbudsjettbeløp**.
3. I **Parametere**-gruppen, i **Prosjektbudsjettår**-feltet, velger du regnskapsåret du vil vise de resterende budsjettbeløpene for.
4. I gruppen **Kopier fra/til** oppgir du følgende informasjon:

   - I feltet **Fra prognosemodell** velger du prosjektbudsjettprognosemodellen som er knyttet til de gjenstående budsjettbeløpene du vil overføre for prosjektene. 
   - Velg **Vis null gjenstående** hvis du vil inkludere prosjekter ikke har noe gjenstående budsjett, men som oppfyller de andre kriteriene du har valgt.
   - I gruppen **Velg budsjetter** velger du **Hent alle budsjetter** for å laste alle budsjetter som samsvarer med kriteriene du har valgt. Hvis du vil utforme en databasespørring som laster inn et bestemt sett med prosjektbudsjetter i ruten, velger du **Hent valgte budsjetter**.

5. For hvert prosjekt du vil behandle, velger du alternativet i begynnelsen av linjen for prosjektet. 
6. Velg **Behandle** for å overføre de gjenstående budsjettbeløpene for de valgte prosjektene til det valgte regnskapsåret.



[!INCLUDE[footer-include](../includes/footer-banner.md)]