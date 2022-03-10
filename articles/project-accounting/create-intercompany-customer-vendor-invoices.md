---
title: Opprette konserninterne kunde- og leverandørfakturaer
description: Dette emnet gir informasjon om hvordan du oppretter konserninterne kunde- og leverandørfakturaer.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7d32d7a0b96daf9a2a48e16d62de8319636737740601481b85ee887948e31110
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989276"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a>Opprette konserninterne kunde- og leverandørfakturaer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

En prosjektregnskapsfører i en juridisk enhet for utlån oppretter en konsernintern kundefaktura for prosjektkostnadene som blir overført til enheten som låner. Når den konserninterne kundefakturaen godkjennes og posteres, sender den juridiske enheten for utlån den konserninterne fakturaen til den juridiske enheten som låner.

Prosjektregnskapsføreren for den juridiske enheten som låner ut kan konfigurere en partiprosess for å generere konserninterne fakturaer regelmessig. Prosjektregnskapsføreren angir vilkårene, for eksempel bestemte prosjekter, for å opprette konserninterne fakturaer i en bunke.

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a>Opprette en konsernintern kundefaktura manuelt for prosjekttransaksjoner 

For å opprette en konsernintern kundefaktura manuelt for prosjekttransaksjoner, bruker du denne fremgangsmåten. Søk etter timer som ble postert av arbeidere på prosjekter i de juridiske enhetene som låner, og for utgifter som var påløpt av den juridiske enheten på vegne av juridiske enheter som låner. Du kan søke etter navn på juridisk enhet, prosjektkontraktnummer, prosjektnummer, datointervall eller en hvilken som helst kombinasjon av disse alternativene. I søkeresultatene velger du transaksjonene som skal legges til på en konsernintern faktura. 

Følgende trinn må utføres i den juridiske utlånsenheten. 

1. I Dynamics 365 Finance går du til **Prosjektstyring og regnskap** > **Prosjektfakturaer** > **Konserninterne kundefakturaer**. På **Konserninterne kundefakturaer**-listesiden på Handlingsruten velger du **Ny.**
2. På **Opprett konsernintern faktura**-siden i **Juridisk enhet**-feltet velger du en juridisk enhet som låner.
3. Valgfritt: Angi en bestemt prosjektkontrakt og et prosjektnummer.
4. Begrens søket ved å velge et datointervall. Angi bestemte datoer i **Startdato**- og **Sluttdato**-feltene. Bare konserninterne transaksjoner som er postert innenfor dette datointervallet vises i søkeresultatene.
5. Angi **Avansert parameter for journallinje** til **Ja**, og velg **Søk**.
6. I søkeresultatene velger du transaksjonene som skal tas med i det konserninterne fakturaforslaget, og deretter velger du **OK**.
7. På **Konsernintern kundefaktura**-siden vises de konserninterne prosjekttransaksjonene du har valgt fra søkeresultatene. Hvis du vil endre transaksjonene før du sender fakturaen til den juridiske enheten som låner, gjør du følgende:
  
    1. Åpne fakturadetaljene på siden **Konsernintern kundefaktura**, og velg deretter **Legg til linje**.
    2. Du kan fjerne en linje ved å velge den og deretter velge **Fjern**.
    3. Vis kommentarer, årsaker, finansdimensjoner og annen informasjon om en valgt linje i fakturalinjedetaljene.
    
8. Du posterer den konserninterne kundefakturaen på Handlingsruten ved å velge **Poster**.

> [!NOTE]
> Hvis organisasjonen krever at konserninterne fakturaer gjennomgås før de posteres, kan det hende at en systemadministrator må konfigurere en arbeidsflyt for konserninterne fakturaer. Hvis en arbeidsflyt ikke er konfigurert for konserninterne fakturaer, kan du postere den konserninterne fakturaen.

## <a name="create-a-batch-job-for-intercompany-invoices"></a>Opprette en satsvis jobb for konserninterne fakturaer

Du kan opprette flere konserninterne fakturaer samtidig for alle juridiske enheter som låner ut. Ved hjelp av søkefunksjonalitet kan du for eksempel søke etter alle transaksjoner som er postert av lånte arbeidere, og som er relatert til prosjekter som administreres av andre juridiske enheter. For hver juridiske enhet som låner, kan du deretter opprette en konsernintern faktura for transaksjonene som er angitt i søkeresultatene.

1. Gå til **Prosjektstyring og regnskap** > **Periodisk** > **Prosjektfakturaer** > **Opprett konserninterne kundefakturaer**.
2. På **Opprett konsernintern kundefaktura**-siden i **Firma**-feltet velger du en juridisk enhet som skal faktureres. Hvis du ikke velger et firma, vises alle transaksjoner som oppfyller søkevilkårene, for alle juridiske enheter som låner.
3. I **Opprett én faktura per** velger du om du vil opprette en faktura for konserninterne transaksjoner basert på et prosjekt, eller basert på en juridisk enhet som låner.
4. Valgfritt: Hvis du vil velge et bestemt prosjekt og en prosjektkontrakt å opprette konserninterne fakturaer for, klikker du på **Velg**. På **Forespørsel**-siden i **Vilkår**-feltet velger du prosjektkontrakten, prosjektnummeret eller begge, og deretter velger du **OK**.
5. På **Bunke**-fanen konfigurerer du en partiprosess for å opprette konserninterne fakturaer regelmessig. Hvis du vil ha mer informasjon, kan du se [Sende en satsvis behandlet jobb fra et skjema](/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).
6. Du posterer de konserninterne fakturaene på Handlingsruten ved å velge **Poster**.

> [!NOTE]
> Hvis organisasjonen krever at konserninterne fakturaer gjennomgås før de posteres, kan det hende at en systemadministrator må konfigurere en arbeidsflyt for konserninterne fakturaer. Hvis en arbeidsflyt ikke er konfigurert for konserninterne fakturaer, kan du postere de konserninterne fakturaene.

## <a name="post-the-intercompany-vendor-invoice"></a>Postere den konserninterne leverandørfakturaen

En prosjektrevisor i den juridiske enheten som låner kan gjennomgå ventende konserninterne leverandørfakturaer når den korresponderende konserninterne kundefakturaen er postert. I Finance, i den juridiske enheten som låner, går du til **Leverandørgjeld** > **Fakturaer** > **Ventende leverandørfaktura**. Det ventende fakturanummeret vil samsvare med det konserninterne kundefakturanummeret. Kontroller at fakturaen er riktig, og poster deretter fakturaen. Postering av konsernintern leverandørfaktura oppretter en underfinans- og en økonomimodultransaksjon for prosjektet som gjenspeiler transaksjonskostnadene i den juridiske enheten låner.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
