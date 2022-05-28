---
title: Innkjøp av ikke-lagerførte materialer eller innkjøpskategorier som bruker en ventende leverandørfaktura
description: Dette emnet forklarer hvordan du registrerer ventende leverandørfakturaer.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e81f7a54e304ae6fc9a9f2637124579b6e7b54e9
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612669"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Innkjøp av ikke-lagerførte materialer eller innkjøpskategorier som bruker en ventende leverandørfaktura

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Når et selskap anskaffer ikke-lagerførte materialer eller innkjøpskategorier for et prosjekt, kan kostnadene umiddelbart registreres mot prosjektet. 

Contoso Robotics US utfører for eksempel et prosjekt for fornyelse av utstyr og trenger programvarelisenser. Disse lisensene anskaffes fra en tredjepartsleverandør.  Ved hjelp av Dynamics 365 Finance registrerer funksjonæren for leverandørgjelde et ventende fakturadokument for leverandør og tilskriver lisenskostnadene direkte mot utstyrsfornyelsesprosjektet. 

> [!IMPORTANT]
> Før du bruker funksjonaliteten som er beskrevet i dette emnet, må du se gjennom og bruke de nødvendige konfigurasjonene. Hvis du vil ha mer informasjon , kan du se [Konfigurer ikke lagerførte materialer og ventende leverandørfakturaer](configure-materials-nonstocked.md) og [Bruk innkjøpskategorier med prosjektbestillinger og ventende leverandørfakturaer](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Poster en prosjektrelatert ventende leverandørfaktura 

Ventende leverandørfakturaer kan registreres på siden **Ventende leverandørfakturaer** (**Leverandørgjeld** > **Fakturaer** > **Ventende leverandørfakturaer**). Fullfør følgende trinn for å postere en prosjektrelatert ventende leverandørfaktura:

1. Gå til **Leverandørgjeld** > **Fakturaer**, og velg **Ny**. 
1. I feltet **Leverandørkonto** velger du en leverandør, og deretter, i **Nummer**-feltet, angir du ID-en for leverandørkontoen.
1. Legg til en linje i leverandørfakturaen, og deretter, i **Varenummer**-feltet, velger du den ikke-lagerførte varen som ble kjøpt fra leverandøren. I **Innkjøpskategori**-feltet kan du også velge innkjøpskategorien som ble kjøpt fra leverandøren.   
1. Legg til antallet som ble kjøpt. Systemet fyller ut enhetsprisen basert på priskonfigurasjonen for den ikke-lagerførte varen. 
1. Kontroller totalbeløpet og andre nødvendige detaljer på linjen.
1. På **Prosjekt**-fanen velger du ID-en til prosjektet som denne varen skal føres i.
1. Valgfritt: Velg aktivitetsnummeret, og oppdater prosjektkategorien og linjeegenskapen.
1. Poster den ventende leverandørfakturaen. Når fakturaen er postert, registrerer systemet følgende informasjon:
    
    - Leverandørsaldobeløpet.
    - Salgsavgiftsbeløpet.
    - Kostnadene mot prosjektet registreres på integrasjonskontoen for innkjøp.
    - Den faktiske kostnadstransaksjonen for prosjektet i Dataverse.  Denne transaksjonen behandles videre ved hjelp av [journalen for Project Operations-integrering](../project-accounting/project-operations-integration-journal.md). Når du legger inn denne journalen, flyttes beløpet fra integrasjonskontoen for innkjøp til prosjektkostnadskontoen. 
    - Kjøp som faktureres til prosjektkunde ved hjelp av faktureringsmetoden for tid og materiell. I tillegg opprettes det ufakturerte salgstransaksjoner opprettet for bestillinger i Dataverse. Produktprislisten i Dataverse brukes for salgsprisene og beløpene for salgstransaksjon som ikke er fakturert.
