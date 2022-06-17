---
title: Oversikt over produktbaserte kontraktlinjer – Lite
description: Denne artikkelen inneholder informasjon om produktbaserte kontraktlinjer.
author: rumant
ms.date: 10/07/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4ad1fe6d5d56468d887535ddf107eefed3cbd28d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919888"
---
# <a name="product-based-contract-lines-overview---lite"></a>Oversikt over produktbaserte kontraktlinjer – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Du kan opprette produktbaserte kontraktlinjer i Dynamics 365 Project Operations. Produktbaserte kontraktlinjer kan være manuelt opprettede linjer, eller de kan være elementer fra produktkatalogen.

## <a name="product-catalog"></a>Produktkatalog

Produktene i produktkatalogen har en standardenhet og enhetsgruppe. Hvis flere produkter deler samme attributtsett, kan du opprette en produktserie som også har disse attributtene. Alle produktene i en produktserie arver samme attributtsett.

Et selskap selger for eksempel abonnementslisenser for en ulike typer programvare. All abonnementsprogramvare har følgende to attributter:

- Antall brukere
- Abonnementsvarighet (i måneder)

Hvis du vil opprettholde denne typen katalog, oppretter du en produktfamilie med navnet **Abonnementsprogramvare**. Legg til attributtene **Antall brukere** og **Abonnementsvarighet** i produktfamilien. Deretter legger du til enkeltprodukter i produktfamilien **Abonnementsprogramvare**.

## <a name="add-product-catalog-items-to-a-project-contract"></a>Legge til produktkatalogvarer i en prosjektkontrakt

Prosjektkontrakter har deler for to linjetyper: prosjektbaserte linjer og produktbaserte linjer. Produktbaserte linjer inkluderer alle produktene og enhetene i produktprislisten i kontrakten. Produkter som ikke er en del av kontraktens produktprisliste, kan legges til.

Du kan velge produkter fra andre prislister eller direkte fra produktkatalogen. Når du velger produkter direkte fra en produktkatalog, brukes standardprislisten for dette produktet for produktets salgspris. Hvis det ikke er angitt en standardprisliste, settes prisen til 0 (null).

Hvis en kontraktlinje er basert på en produktkatalog, kan du overstyre salgsprisen direkte i linjen. En kontraktlinje har **Priser**-feltet med de to verdiene:

- **Overstyr pris**
- **Bruk standard**

Hvis du angir **Priser**-feltet til **Overstyr pris**, angis ikke standardprisen. Angi en pris for produktet på kontraktlinjen. Hvis du setter feltet til **Bruk standard**, brukes standard salgspris, og feltet kan ikke redigeres.

Når du har installert Project Operations, blir standard salgspriser angitt på de produktbasert linjene i en kontrakt. **Priser**-feltet angis til **Overstyr pris**, slik at du kan redigere standardprisen på kontraktlinjene. Dette er en spesifikk overstyring i Project Operations av virkemåten for produktbaserte linjer i Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]