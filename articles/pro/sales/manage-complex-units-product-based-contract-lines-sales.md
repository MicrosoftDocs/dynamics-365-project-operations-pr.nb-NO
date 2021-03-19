---
title: Administrere komplekse enheter for produktbaserte kontraktlinjer – Lite
description: Dette emnet inneholder informasjon om hvordan du kan støtte salg av abonnementsbaserte produkter.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 029d2aa4fd20fc036a34ae6136fe12454f3b7703
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273345"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a>Administrere komplekse enheter for produktbaserte kontraktlinjer – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Dynamics 365 Project Operations bruker antallsfaktorer til å støtte salg av abonnementsbasert produkter. Når det gjelder abonnementsbaserte produkter, uttrykkes antallet på kontrakt- eller prosjektkontraktlinjen som antall brukermåneder.

Prisen på abonnementsprogramvaren lagres i katalogen som prisen per bruker per måned. I løpet av salgsprosessen er prisen på kontraktlinjen vanligvis prisen per bruker per måned som ble forhandlet og diskontert av salgsrepresentanten. Hver avtale har et forskjellig antall brukere og et forskjellig antall abonnementsmåneder. Antallet som brukes til å beregne beløpet for kontraktlinjen, er et produkt av antall brukere og antall abonnementsmåneder.

Project Operations støtter konseptet *antallsfaktorer* for å støtte denne typen salg. Antallsfaktorer er avhengig av produktattributter. Når du konfigurerer bestemte egenskaper for et produkt, kan du flagge et delsett av disse egenskapene, eller alle egenskapene, som antall faktorer.

Project Operations validerer at bare numeriske egenskaper eller produktegenskaper som har numeriske datatyper, blir flagget som antallsfaktorer. Når det legges til et produkt med konfigurerte antallsfaktorer på en kontraktlinje, blir **Antall**-feltet skrivebeskyttet. Etter at du har angitt verdier for produktegenskaper som er antallsfaktorer, beregner Project Operations antallet på kontraktlinjen.

Dynamics 365 Sales kan for eksempel ha følgende egenskaper:

- **Antall brukere**: Antall brukere.
- **Antall måneder**: Antall abonnementsmåneder.
- **Produkt-SKU** Vareopptellingsenheter (Stock Keeping Unit – SKU) for produktet.

Egenskapene **Antall brukere** og **Antall måneder** kan flagges som antallsfaktorer ved å redigere egenskapene for produktlinjen.

Følg fremgangsmåten nedenfor for å opprette antallsfaktorer fra produktegenskaper.

1. Velg **Salg-Produkter** i **Project Operations**.
2. Åpne produktet du vil definere antallsfaktorer for. Kontroller at produktet allerede har konfigurert egenskaper.
3. På **Prosjektinformasjon**-siden velger du kategorien **Antallsfaktorer**.
4. I delrutenettet velger du **+ Ny feltberegning**.
5. Angi navnet på **Antallsfaktor**, og velg egenskapsverdien som tilordnes feltberegningen.
6. Lagre og lukk skjemaet.
7. Gjenta trinn 2-6 for alle egenskapene som samlet utgjør antallet for den produktbaserte kontraktlinjen.

Når antallsfaktorer er konfigurert og brukeren oppretter en kontraktlinje for dette produktet, blir antallet for kontraktlinjen låst. Antallet beregnes deretter som et produkt av egenskapsverdiene for denne kontraktlinjen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]