---
title: Kjøpe ikke lagerførte materialer ved hjelp av en ventende leverandørfaktura
description: Dette emnet forklarer hvordan du registrerer ventende leverandørfakturaer.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ce9f244eaa549742aeb55024ca9ef4d82cde1bd4a5b9c7f8c762cf72e0da83f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009048"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>Kjøpe ikke lagerførte materialer ved hjelp av en ventende leverandørfaktura

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Når et selskap anskaffer ikke-lagerført materiell for et prosjekt, kan kostnadene umiddelbart registreres mot prosjektet. 

For eksempel utfører Contoso Robotics US et prosjekt for fornyelse av utstyr og trenger programvarelisenser. Disse lisensene anskaffes fra en tredjepartsleverandør.  Når du bruker Dynamics 365 Finance, registrerer assistenten for leverandørgjeld et ventende leverandørfakturadokument og attributterer lisenskostnadene direkte mot prosjektet for fornyelse av utstyr. 

> [!IMPORTANT]
> Før du bruker funksjonaliteten som er beskrevet i dette emnet, må du se gjennom og bruke de nødvendige konfigurasjonene. Hvis du vil ha mer informasjon, kan du se [Aktivere ikke-lagerførte materialer og ventende leverandørfakturaer](configure-materials-nonstocked.md). 

## <a name="post-a-project-related-pending-vendor-invoice"></a>Poster en prosjektrelatert ventende leverandørfaktura 

Ventende leverandørfakturaer kan registreres på siden **Ventende leverandørfakturaer** (**Leverandørgjeld** > **Fakturaer** > **Ventende leverandørfakturaer**). Fullfør følgende trinn for å postere en prosjektrelatert ventende leverandørfaktura:

1. Gå til **Leverandørgjeld** > **Fakturaer** og velg **Ny**. 
2. I **Fakturakonto**-feltet velger du en leverandør i **Nummer**-feltet og angir leverandørfaktura-IDen.
3. Legg til en linje i leverandørfakturaen, og velg varen som ikke er på lager fra leverandøren i **Varenummer**-feltet. 

    > [!NOTE]
    > Leverandørfakturalinjer som er basert på en innkjøpskategori, kan ikke registreres mot prosjektet. 
    
5. Legg til innkjøpmengden. Enhetsprisen fylles ut i systemet basert på konfigurasjonen av varepris som ikke er på lager. 
6. Kontroller totalbeløpet og andre nødvendige detaljer på linjen.
7. Velg IDen for prosjektet som varen skal registreres til, i kategorien **Prosjekt** i linjedetaljene.
8. Du kan eventuelt velge aktivitetsnummeret og oppdatere prosjektkategorien og linjeegenskapen.
9. Poster ventende leverandørfaktura. Når fakturaen posteres, registrerer systemet følgende:
    
    - Leverandørsaldobeløpet.
    - Salgsavgiftsbeløpet.
    - Kostnadene mot prosjektet registreres på integrasjonskontoen for innkjøp.
    - Den faktiske transaksjonen for prosjekt i Dataverse. Denne transaksjonen behandles videre ved hjelp av [journalen for Project Operations-integrering](../project-accounting/project-operations-integration-journal.md). Når du legger inn denne journalen, flyttes beløpet fra integrasjonskontoen for innkjøp til prosjektkostnadskontoen.
