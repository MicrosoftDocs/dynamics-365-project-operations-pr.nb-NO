---
title: Oversikt over produktbaserte tilbudslinjer – Lite
description: Dette emnet inneholder informasjon om arbeid med produktbaserte tilbudslinjer.
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6aa428c486f149308ad078f9d7a80a0be0f0f04
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/30/2020
ms.locfileid: "4178200"
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
