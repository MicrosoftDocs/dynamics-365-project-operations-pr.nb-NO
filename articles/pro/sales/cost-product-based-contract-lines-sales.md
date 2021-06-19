---
title: Produktbaserte kontraktlinjer for kostberegning – Lite
description: Dette emnet gir informasjon om oppretting
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9458a57863244a68359f57185325c03a46bd6569
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003553"
---
# <a name="cost-product-based-contract-lines---lite"></a>Produktbaserte kontraktlinjer for kostberegning – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_


Produktbaserte kontraktlinjer i Dynamics 365 Project Operations inneholder feltet **Kostnadspris**, som lagrer kostnadsprisen på produktet for beregninger av nedstrømslønnsomhet.

Når en produktbasert kontraktlinje opprettes for et katalogprodukt, brukes standardkostnaden for linjen fra feltet **Standardkostnad** i produktkatalogen. Feltet **Standardkostnad** i produktkatalogen konfigureres i organisasjonens standardvaluta. Når enhetskostnaden er angitt som standard på kontraktlinjen, blir den konvertert til salgsvalutaen i kontrakten.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Enhetskostnad på en produktbasert kontraktlinje

Ved å ha en enhetskostnad på en produktbasert kontraktlinje er det mulig med ulike produktkostnader for hvert salg av en enhet. Selv om dette ikke alltid er nødvendig, er det enkelte tilfeller der kunden kan få rabatt på kostnaden for produktet av leverandøren. Tenk deg følgende scenario:

Fabrikam Robotics installerer robotarmer på samlebåndene til Adatum Corporation. Fabrikam tilbyr installasjonstjenester, men robotarmene kommer fra Trey Research. Hvis installasjonen av robotarmer hos Adatum Corporation åpner en ny bransjevertikal for Trey Research, kan de tilby en spesiell rabatt på denne avtalen til Fabrikam. I dette tilfellet oppretter Fabrikam en produktbasert kontraktlinje for robotarmer. Det angis en enhetskostnad per for denne kontrakten. Kostnaden er forskjellig fra kostnaden for robotarmer fra Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]