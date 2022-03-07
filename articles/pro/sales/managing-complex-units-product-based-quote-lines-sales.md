---
title: Administrasjon av komplekse enheter, for eksempel per bruker, per måned for produktbaserte tilbudslinjer – Lite
description: Dette emnet gir informasjon om administrasjon av komplekse enheter for produktbaserte tilbudslinjer.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2ee46da2f663ef4f5f8fc7f9f89b6fcfd09a1798
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175588"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a>Administrasjon av komplekse enheter, for eksempel per bruker, per måned for produktbaserte tilbudslinjer – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Dynamics 365 Project Operations bruker antallsfaktorer til å støtte salg av abonnementsbasert produkter. Når det gjelder abonnementsbaserte produkter, uttrykkes antallet på tilbuds- eller prosjektkontraktlinjen som antall brukermåneder.

Vanligvis lagres prisen på abonnementsprogramvaren i katalogen som prisen per bruker per måned. I løpet av salgsprosessen er prisen på tilbudslinjen vanligvis prisen per bruker per måned som ble forhandlet og diskontert av IT-salgsrepresentanten. Hver avtale har et forskjellig antall brukere og et forskjellig antall abonnementsmåneder. Antallet som brukes til å beregne tilbudslinjen, er et produkt av antall brukere og antall abonnementsmåneder.

Project Operations har innført konseptet antallsfaktorer for å støtte denne typen salg. Antallsfaktorer er avhengig av produktattributter i Dynamics 365. Når du konfigurerer bestemte egenskaper for et produkt, kan du bruke Project Operations til å flagge et delsett av, eller alle egenskapene, som antall faktorer.

Project Operations validerer at bare numeriske egenskaper eller produktegenskaper som har numeriske datatyper, blir flagget som antallsfaktorer. Når du legger til et produkt med antallsfaktorer i en tilbudslinje, **Antall**-feltet skrivebeskyttet. Etter at du har angitt verdier for produktegenskaper som er antallsfaktorer, beregner Project Operations antallet på tilbudslinjen.

Dynamics 365 Sales kan for eksempel ha følgende egenskaper:

- **Antall brukere**: Antall brukere
- **Antall måneder**: Antall abonnementsmåneder
- **Produkt-SKU**

Du kan flagge egenskapene **Antall brukere** og **Antall måneder** som antallsfaktorer ved å redigere egenskapene for produktlinjen.

Følg denne fremgangsmåten for å opprette antallsfaktorer fra produktegenskaper:

1. I den venstre navigasjonsruten i Project Operations går du til **Salg** > **Produkter**.
2. Åpne produktet du må konfigurere antallsfaktorer for. Kontroller at produktet har egenskaper som allerede er konfigurert.
3. På siden **Prosjektinformasjon** for produktet velger du kategorien **Antallsfaktorer**.
4. I delrutenettet velger du **+ Ny feltberegning**.
5. Angi navnet på antallsfaktoren, og velg egenskapsverdien som tilordnes feltberegningen.
6. Lagre og lukk skjemaet. Gjenta disse trinnene for alle egenskaper som skal brukes til å beregne antallet for den produktbaserte tilbudslinjen.

Når du oppretter en produktbasert tilbudslinje for et produkt, blir antallet på tilbudslinjen låst. Antallet beregnes som et produkt av egenskapsverdiene som du har lagt inn for tilbudslinjen.
