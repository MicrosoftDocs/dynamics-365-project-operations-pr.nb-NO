---
title: Konfigurere konsernintern fakturering
description: Dette emnet gir informasjon og eksempler på hvordan du konfigurerer konserninterne fakturaer for prosjekter.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bb39e212d00f8874254d4255f310217cdf46eb5a
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949691"
---
# <a name="configure-intercompany-invoicing"></a>Konfigurere konsernintern fakturering

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Fullfør fremgangsmåten nedenfor for å konfigurere konsernintern fakturering for prosjekter i Dynamics 365 Project Operations. Konserninterne transaksjoner er tid- og utgiftstransaksjoner fra en prosjektkontrakt som tilhører et firma eller en organisasjonsenhet, mens ressursene på prosjektkontrakten er en del av et annet firma eller en annen organisasjonsenhet.

## <a name="example-configure-intercompany-invoicing"></a>Eksempel: Konfigurere konsernintern fakturering

I det følgende eksemplet er Contoso Robotics USA (USPM) den juridiske enheten som låner, og Contoso Robotics UK (GBPM) den juridiske enheten som låner ut. 

1. **Konfigurere konserninternt regnskap mellom juridiske enheter**. Hvert enkelt par av juridiske enheter som låner og låner ut må konfigureres på Økonomimodul [Konserninternt regnskap](/dynamics365/finance/general-ledger/intercompany-accounting-setup)-siden.
    
    1. I Dynamics 365 Finance går du til **Økonomimodul** > **Posteringsoppsett** > **Konserninternt regnskap**. Opprett en oppføring med følgende informasjon:

        - **Opprinnelig firma** = **GBPM**
        - **Målfirma** = **USPM**

2. **Konfigurere handelsforbindelsen mellom juridiske enheter**. Kundeposten som representerer den juridiske enheten som låner, må opprettes i den juridiske enheten som låner ut. Leverandøren som representerer den juridiske enheten som låner ut, må opprettes i den juridiske enheten som låner.

     1. I Finance velger du den juridiske enheten **GBPM**.
     2. Gå til **Kundefordringer** > **Kunder** > **Alle kunder**. Opprett en ny post for den juridiske enheten, **USPM**.
     3. Utvid **Navn**, filtrer postene etter **Type** og velg **Juridiske enheter**. 
     4. Finn og velg kundeoppføringen for **Contoso Robotics USA (USPM)**.
     5. Velg **Bruk treff**. 
     6. Velg kundegruppen **50 – konserninterne kunder**, og lagre deretter oppføringen.
     7. Velg den juridiske enheten **USPM**.
     8. Gå til **Leverandørgjeld** > **Leverandører** > **Alle leverandører**. Opprett en ny post for den juridiske enheten, **GBPM**.
     9. Utvid **Navn**, filtrer postene etter **Type** og velg **Juridiske enheter**. 
     10. Finn og velg kundeoppføringen for **Contoso Robotics UK (GBPM)**.
     11. Velg **Bruk treff**, velg leverandørgruppen, og lagre deretter posten.
     12. I leverandørposten velger du **Generelt** > **Sett opp** > **Konserninternt**.
     13. På **Handelsforbindelse**-fanen angir du **Aktiv** til **Ja**.
     14. Sett feltet **Kundefirma** til **GBPM**, og velg kundeposten du opprettet tidligere i prosedyren, under **Min kontooppføring**.

3. **Konfigurere konserninterne innstillinger i Parametere for prosjektstyring og regnskap**. 

    1. Velg den juridiske enheten **USPM**, og gå til **Prosjektstyring og regnskap** > **Oppsett** > **Parametere for prosjektstyring og regnskap**.
    2. På **Konsernintern**-fanen velger du innkjøpskategorien for å samsvare leverandørfakturaer som genereres automatisk.
    3. I **Standardkategori** velger du **Konserninterne ressurser**.
    4. Velg den juridiske enheten **GBPM**, og gå til **Prosjektstyring og regnskap** > **Oppsett** > **Parametere for prosjektstyring og regnskap**.
    5. På **Konsernintern**-fanen velger du en standard prosjektkategori for hver transaksjonstype. Prosjektkategorier brukes for avgiftskonfigurasjon når den fakturerte kategorien i konserninterne transaksjoner bare eksisterer i den juridiske låneenheten. Du kan velge å avsette omsetning for konserninterne transaksjoner. Avsetning skjer når transaksjonene er postert via integreringsjournalen for Project Operations i den juridiske enheten som låner ut. Journalen reverseres når den konserninterne fakturaen blir postert.
    6. I **Ved utlån av ressurser**-gruppen velger du **...** > **Ny**. 
    7. I rutenettet velger du følgende informasjon:

          - **Juridisk enhet som låner** = **USPM**
          - **Avsett inntekt** = **Ja**
          - **Standard timeregistreringskategori** = **Standard – time**
          - **Standard utgiftskategori** = **Standard – utgift**

4. **Angi konserninterne kostnads- og inntektskontoer i Finansposteringsoppsett**. Den konserninterne inntektskontoen blir kreditert når den konserninterne kundefakturaen posteres i den juridiske enheten som låner ut. Den konserninterne kostnadskontoen blir debitert når den samsvarende leverandørfakturaen posteres i den juridiske enheten som låner. Disse kontoene er konfigurert i samsvarende juridiske enheter. 
      
     1. I Finance velger du den juridiske enheten som låner **USPM**. 
     2. Gå til **Prosjektstyring og regnskap** > **Oppsett** > **Postering** > **Finansposteringsoppsett**. 
     3. På **Kostnadskontoer**-fanen i **Finanskontotype** velger du **Konsernintern kostnad**. Opprett en ny post med følgende informasjon:
      
        - **Juridisk enhet som låner ut** = **GBPM**
        - **Hovedkonto** = Velg hovedkontoen for konsernintern kostnad. Dette oppsettet er obligatorisk. Oppsettet brukes for selskapets flyter i Økonomi, men ikke i prosjektrelaterte, midlertidige flyter. Dette valget har ingen nedstrømspåvirkning. 
        
     4. Velg den juridiske enheten som låner ut, **GBPM**. 
     5. Gå til **Prosjektstyring og regnskap** > **Oppsett** > **Postering** > **Finansposteringsoppsett**. 
     6. På **Inntektskontoer**-fanen i **Finanskontotype** velger du **Konsernintern inntekt**. Opprett en ny post med følgende informasjon:

        - **Juridisk enhet som låner** = **USPM**
        - **Hovedkonto** = Velg hovedkontoen for konsernintern inntekt. Dette oppsettet er obligatorisk. Oppsettet brukes for selskapets flyter i Økonomi, men ikke i prosjektrelaterte, midlertidige flyter. Dette valget har ingen nedstrømspåvirkning. 

5. **Konfigurere overføringspriser for arbeid**. Prissetting for konsernintern overføring er konfigurert i Project Operations på Dataverse. Konfigurere [kostnadssatser for arbeid](../pricing-costing/set-up-labor-cost-rate.md#transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity) og [fakturasats for arbeid](../pricing-costing/set-up-labor-bill-rate.md#transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions) for konsernintern fakturering. Overføringspriser støttes ikke for konserninterne utgiftstransaksjoner. Den interorganisatoriske salgsenhetsprisen vil alltid bli satt til den samme verdien som kostnadsprisen for ressursenheten.

      Utviklerressurskostnaden for Contoso Robotics UK er 88 GBP per time. Contoso Robotics UK fakturerer Contoso Robotics USA 120 USD for hver time denne ressursen arbeidet med prosjekter i USA. Contoso Robotics USA fakturerer kunden Adventure Works 200 USD for arbeidet som er gjort av utviklerressursen Contoso Robotics UK.

      1. I Project Operations på Dataverse går du til **Salg** > **Prislister**. Opprett en ny kostprisliste kalt **Contoso Robotics UK-kostnadssatser.** 
      2. Opprett en post med følgende informasjon i kostprislisten:
         - **Rolle** = **Utvikler**
         - **Kostnad** = **88 GBP**
      3. Gå til **Innstillinger** > **Organisasjonsenheter**, og knytt denne kostprislisten til organisasjonsenheten **Contoso Robotics UK**.
      4. Gå til **Salg** > **Prislister**. Opprett en ny kostprisliste kalt **Contoso Robotics USA-kostnadssatser**. 
      5. Opprett en post med følgende informasjon i kostprislisten:
          - **Rolle** = **Utvikler**
          - **Ressursstyringsfirma** = **Contoso Robotics UK**
          - **Kostnad** = **120 USD**
      6. Gå til **Innstillinger** > **Organisasjonsenheter**, og knytt kostprislisten for **Contoso Robotics USA-kostnadssatser** til organisasjonsenheten **Contoso Robotics USA**.
      7. Gå til **Salg** > **Prislister**. Opprette en salgsprisliste kalt **Fakturasatser for Brusefoss industrier**. 
      8. Opprett en post med følgende informasjon i salgsprislisten:
          - **Rolle** = **Utvikler**
          - **Ressursstyringsfirma** = **Contoso Robotics UK**
          - **Fakturasats** = **200 USD**
      9. Gå til **Salg** > **Prosjektkontrakter** og knytt **Fakturasatser for Brusefoss industrier**-prislisten til Brusefoss industrier-prosjektprislisten for prosjektkontrakten.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
