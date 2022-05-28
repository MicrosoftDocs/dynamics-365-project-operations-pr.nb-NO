---
title: Fakturere et honorar eller forskudd
description: Dette emnet gir information om hvordan du fakturerer et honorar eller forskudd i Project Operations.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: aa659ebfa6d848f312caa1d197404d77b1f6ee21
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590588"
---
# <a name="invoice-a-retainer-or-an-advance"></a>Fakturere et honorar eller forskudd

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Dynamics 365 Project Operations støtter honorarbaserte kontrakter og engangsforskudd. I en prosjektkontrakt kan du registrere en plan for honorarer eller et engangsforskudd. Hvis du registrerer på prosjektkontraktnivået, blir imidlertid ikke et honorar eller forskudd umiddelbart tilgjengelig for bruk. Hvis du vil bruke et honorar eller forskudd på en faktura som faktisk belaster kunden, må honoraret eller forskuddet faktureres først.

Fullfør fremgangsmåten nedenfor for å fakturere et honorar eller et forskudd.

1. Velg **Salg** > **Fakturering** > **Honorarer og forskudd**. 
2. På siden **Honorarer og forskudd** bruker du filteret til å velge det spesifikke honoraret eller forskuddet som skal faktureres, og merk det deretter som **Klar for fakturering**.
3. Opprett en faktura manuelt fra listen **Prosjektkontrakt** eller detaljsiden. Honoraret eller forskuddet vises på fakturautkastet i delen **Forskudd og honorarer** på **Faktura**-siden.
4. Bekreft fakturaen. Dette vil gjøre honoratet eller forskuddet tilgjengelig for bruk. Du kan kontrollere fakturaen på listesiden **Honorarer og forskudd**. For et fakturert honorar eller forskudd vises det tilgjengelige beløpet i rutenettet.

## <a name="create-a-retainer-or-advance-from-the-invoice-grid"></a>Opprette et honorar eller forskudd fra fakturarutenettet

Du kan opprette et honorar eller forskudd direkte på en faktura.

1. På et fakturautkast, i delrutenettet **Forskudd og honorarer**, velger du **Ny** for å opprette et nytt honorar eller forskudd. 
2. På siden **Hurtigoppretting** legger du til den nødvendige informasjonen, og deretter velger du **Lagre**. Honoraret eller forskuddet opprettes på prosjektkontrakten som er relatert til fakturaen. Honoraret eller forskuddet blir automatisk merket som **Klar til fakturering** og deretter lagt til i delrutenettet **Forskudd og honorarer** på **Faktura**-siden.

## <a name="reconcile-an-invoiced-retainer-or-advance"></a>Avstemme et fakturert honorar eller forskudd

Når et honorar eller forskudd er fakturert, kan de brukes eller avstemmes på en faktura med tid, utgifter, milepæler eller andre prosjektrelaterte gebyrer. Kunden får se at fakturabeløpet er redusert med honorar- eller forskuddsbeløpet som er brukt på denne fakturaen.

På alle fakturaer som er generert for en prosjektkontrakt som har fakturerte honorarer eller forskudd, bruker Project Operations automatisk honoraret eller forskuddet på fakturaen.

Dette kan du se i rutenettet **Brukte honorarer og forskudd** på **Faktura**-siden. Følgende tabell inneholder informasjon om feltene i rutenettet **Brukte honorarer og forskudd** på **Prosjektfaktura**-siden.

| Felt | Sted | Beskrivelse | Nedstrøms påvirkning |
| --- | --- | --- | --- |
| Beskrivelse | Rutenettet **Brukte forskudd og honorarer** på **Prosjektfaktura**-siden |Dette skrivebeskyttede feltet inneholder en beskrivelse av honoraret eller forskuddet som er brukt på denne fakturaen. Denne verdien kan ikke endres på fakturaen. Denne verdien kan oppdateres i delrutenettet på **Prosjektkontrakter**-siden. | Dette feltet kan vises til kunden på den utskrevne fakturaen for å angi hvilket honorar eller forskudd som er brukt på fakturaen. |
| Levert den | Rutenettet **Brukte forskudd og honorarer** på **Prosjektfaktura**-siden  | Dette skrivebeskyttede feltet inneholder fakturadatoen for honoraret eller forskuddet som er brukt på denne fakturaen. Denne verdien kan ikke endres på fakturaen. Denne verdien kan oppdateres i delrutenettet på **Prosjektkontrakter**-siden. | Dette feltet kan vises til kunden på den utskrevne fakturaen for å angi datoen da honoraret eller forskuddet først ble fakturert til kunden. |
| Mengde | Rutenettet **Brukte forskudd og honorarer** på **Prosjektfaktura**-siden  | Dette skrivebeskyttede feltet inneholder beløpet for honoraret eller forskuddet som er brukt på denne fakturaen. Denne verdien kan ikke endres på fakturaen. Denne verdien kan oppdateres i delrutenettet på **Prosjektkontrakter**-siden. | Dette feltet kan vises til kunden på den utskrevne fakturaen for å angi originalbeløpet for honoraret eller forskuddet som ble betalt av kunden. |
| Brukt beløp | Rutenettet **Brukte forskudd og honorarer** på **Prosjektfaktura**-siden  | Dette skrivebeskyttede feltet inneholder den beregnede verdien som oppsummerer hvor mye av honoraret eller forskuddet som er brukt. | Dette feltet kan vises til kunden på den utskrevne fakturaen for å angi beløpet fra dette honoraret eller forskuddet som allerede er brukt. |
| Samlet beløp | Rutenettet **Brukte forskudd og honorarer** på **Prosjektfaktura**-siden  | Dette redigerbare feltet inneholder beløpet for honoraret eller forskuddet som brukes på denne prosjektfakturaen. Dette beløpet kan ikke være mer enn det som er tilgjengelig for forskuddet. Systemet beregner automatisk dette som differansen mellom feltene **Beløp** og **Brukt beløp** i rutenettet. Du kan redusere dette beløpet for å bruke mindre enn det som er tilgjengelig, men du kan ikke øke beløpet for å bruke mer enn det som er tilgjengelig. | Dette feltet kan vises til kunden på den utskrevne fakturaen for å angi beløpet fra dette honoraret eller forskuddet som brukes på fakturaen. |
| Saldohonorarbeløp. | Rutenettet **Brukte forskudd og honorarer** på **Prosjektfaktura**-siden  | Dette skrivebeskyttede feltet inneholder verdien for hvor mye av honoraret eller forskuddet som er igjen etter at fakturaen er bekreftet. | Dette feltet kan vises til kunden på den utskrevne fakturaen for å angi beløpet som vil være igjen fra dette honoraret eller forskuddet etter at fakturaen er bekreftet og betalt. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]