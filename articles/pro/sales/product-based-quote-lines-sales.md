---
title: Oversikt over produktbaserte tilbudslinjer – Lite
description: Dette emnet inneholder informasjon om arbeid med produktbaserte tilbudslinjer.
author: rumant
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 8b904f9abd3d2505c5397906f63a5ae8ff4be41b
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369838"
---
# <a name="product-based-quote-lines-overview---lite"></a>Oversikt over produktbaserte tilbudslinjer – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Du kan opprette produktbaserte tilbudslinjer i Dynamics 365 Project Operations. Produktbaserte tilbudslinjer kan være manuelt lagt til, eller de kan være elementer fra produktkatalogen.

## <a name="product-catalog"></a>Produktkatalog

Hvert produkt i produktkatalogen har en standardenhet og enhetsgruppe. Hvis flere produkter deler samme attributtsett, kan du opprette en produktserie som deler disse attributtene. 

Et selskap selger for eksempel abonnementslisenser for en ulike typer programvare. All abonnementsprogramvare har følgende to attributter:

- Antall brukere
- En abonnementsvarighet målt i måneder

For å opprettholde denne typen katalog må du opprette en produktserie kalt **Abonnementsprogramvare** og legge til et antall brukere og abonnementsvarighet som attributter. Deretter kan du legge til enkeltprodukter i **Abonnementsprogramvare**-produktserien.

## <a name="add-product-catalog-items-to-a-project-quote"></a>Legge til produktkatalogvarer i et prosjekttilbud

Sidene **Prosjekttilbud** og **Prosjektkontrakt** har deler for prosjektbaserte linjer og produktbaserte linjer. For produktbaserte linjer inkluderer rullegardinlisten på tilbudslinjen eller prosjektkontraktlinjen inkluderer alle produkter og enheter i produktprislisten. Du kan også legge til produkter som ikke er del av produktprislisten.

Du kan også velge produkter fra andre prislister, eller direkte fra produktkatalogen. Når du velger produkter direkte fra en produktkatalog, brukes standardprislisten for dette produktet til å hente produktets salgspris. Hvis det ikke er angitt en standardprisliste, settes prisen til null (0).

Når en tilbudslinje er basert på en produktkatalog, kan du overstyre salgsprisen direkte i tilbudslinjen. En tilbudslinje i **Priser**-feltet med to tilgjengelige verdier:

- **Overstyr pris**
- **Bruk standard**

Hvis du velger **Overstyr pris**, blir ikke standardprisen angitt. I stedet må du angi en pris for produktet på tilbudslinjen. Hvis du velger **Bruk standard**, brukes standard salgspris, og feltet låses for redigering.

Standard salgspriser angis på de produktbasert linjene i et tilbud. **Pris**-feltet angis deretter til **Overstyr pris**, slik at du kan redigere standardprisen på tilbudslinjene. Dette er en Project Operations-spesifikk overstyring til den produktbaserte linjefunksjonaliteten i Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]