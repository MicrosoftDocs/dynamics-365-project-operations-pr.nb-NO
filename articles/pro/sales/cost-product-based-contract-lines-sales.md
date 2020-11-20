---
title: Produktbaserte kontraktlinjer for kostberegning – Lite
description: Dette emnet gir informasjon om oppretting
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e961bcf32a5dd662b7cd27a23eb5f664c45c292
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177253"
---
# <a name="cost-product-based-contract-lines---lite"></a>Produktbaserte kontraktlinjer for kostberegning – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_


Produktbaserte kontraktlinjer i Dynamics 365 Project operations omfatter feltet **Kostpris**, som lagrer kostprisen for produktet for beregninger av lønnsomhet nedstrøms.

Når det opprettes en produktbasert kontraktlinje for et katalogprodukt, hentes kostnadene for den produktbaserte kontraktlinjen som standard fra feltet **Standardkostnad** i produktkatalogen. Feltet **Standardkostnad** i produktkatalogen konfigureres i organisasjonens standardvaluta. Når enhetskostnaden er angitt som standard på kontraktlinjen, blir den konvertert til salgsvalutaen i kontrakten.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Enhetskostnad på en produktbasert kontraktlinje

Ved å ha en enhetskostnad på en produktbasert kontraktlinje er det mulig med ulike produktkostnader for hvert salg av en enhet. Selv om dette ikke alltid er nødvendig, er det enkelte tilfeller der kunden kan få rabatt på kostnaden for produktet av leverandøren. Tenk deg følgende scenario:

Fabrikam Robotics installerer robotarmer på samlebåndene til Adatum Corporation. Fabrikam leverer installasjonstjenester, men robotarmene blir skaffet fra Trey Research. Hvis installasjonen av robotarmer hos Adatum Corporation åpner en ny bransjevertikal for Trey Research, kan de tilby en spesiell rabatt på denne avtalen til Fabrikam. I dette tilfellet oppretter Fabrikam en produktbasert kontraktlinje for robotarmer og angir en kostnad per enhet for denne kontrakten, som er forskjellig fra standardkostnaden for robotarmer fra Trey Research.
