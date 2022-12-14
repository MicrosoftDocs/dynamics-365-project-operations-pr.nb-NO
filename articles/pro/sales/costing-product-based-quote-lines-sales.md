---
title: Produktbaserte tilbudslinjer for kostberegning
description: Denne artikkelen inneholder informasjon om hvordan du bruker en kostpris på en produktbasert tilbudslinje.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a8b3569ff217f6fc62606dae4292be14f9d3358c
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825624"
---
# <a name="costing-product-based-quote-lines"></a>Produktbaserte tilbudslinjer for kostberegning

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_


Produktbaserte tilbudslinjer i Dynamics 365 Project Operations har også et **Kostpris**-felt. Dette feltet brukes til å spore kostprisen for produktet i tilbudslinjen og for beregning av overskudd nedstrøms.

Når det opprettes en produktbasert tilbudslinje for et katalogprodukt, hentes kostnadene for den produktbaserte tilbudslinjen som standard fra feltet **Standardkostnad** i produktkatalogen. Feltet Standardkostnad i produktkatalogen konfigureres i organisasjonens standardvaluta. Standard enhetskostnad på den produktbaserte tilbudslinjen konverteres til salgsvalutaen i tilbudet.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Enhetskostnad på en produktbasert tilbudslinje

Formålet med å ha en enhetskostnad på en produktbasert tilbudslinje er å tillate ulike kostnader for et produkt for hvert salg. Dette er ikke et typisk scenario, men noen ganger kan det hende at prisen på produktet blir rabattert av leverandøren, avhengig av kunden for det endelige salget.

Eksempel:

Fabrikam Robotics installerer robotarmer på samlebåndene til A Datum Corporation. Fabrikam leverer installasjonstjenester, men robotarmene blir skaffet fra Trey Robotics. Hvis installasjonen av robotarmer hos A Datum Corporation åpner en ny bransjevertikal for Treys robotarmer, kan Trey gi en spesiell rabatt på denne avtalen til Fabrikam.

I dette tilfellet vil Fabrikam opprette en produktbasert tilbudslinje for robotarmer og angi en spesiell kostnad per enhet for dette tilbudet. Denne kostnaden er forskjellig fra standardkostnaden for Trey Robotic Arms.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
