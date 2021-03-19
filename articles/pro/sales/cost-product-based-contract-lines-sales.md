---
title: Produktbaserte kontraktlinjer for kostberegning – Lite
description: Dette emnet gir informasjon om oppretting
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 001b0b54abcdd5fcd1eca7f3271cc78392f68860
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273705"
---
# <a name="cost-product-based-contract-lines---lite"></a>Produktbaserte kontraktlinjer for kostberegning – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_


Produktbaserte kontraktlinjer i Dynamics 365 Project Operations inneholder feltet **Kostnadspris**, som lagrer kostnadsprisen på produktet for beregninger av nedstrømslønnsomhet.

Når en produktbasert kontraktlinje opprettes for et katalogprodukt, brukes standardkostnaden for linjen fra feltet **Standardkostnad** i produktkatalogen. Feltet **Standardkostnad** i produktkatalogen konfigureres i organisasjonens standardvaluta. Når enhetskostnaden er angitt som standard på kontraktlinjen, blir den konvertert til salgsvalutaen i kontrakten.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Enhetskostnad på en produktbasert kontraktlinje

Ved å ha en enhetskostnad på en produktbasert kontraktlinje er det mulig med ulike produktkostnader for hvert salg av en enhet. Selv om dette ikke alltid er nødvendig, er det enkelte tilfeller der kunden kan få rabatt på kostnaden for produktet av leverandøren. Tenk deg følgende scenario:

Fabrikam Robotics installerer robotarmer på samlebåndene til Adatum Corporation. Fabrikam tilbyr installasjonstjenester, men robotarmene kommer fra Trey Research. Hvis installasjonen av robotarmer hos Adatum Corporation åpner en ny bransjevertikal for Trey Research, kan de tilby en spesiell rabatt på denne avtalen til Fabrikam. I dette tilfellet oppretter Fabrikam en produktbasert kontraktlinje for robotarmer. Det angis en enhetskostnad per for denne kontrakten. Kostnaden er forskjellig fra kostnaden for robotarmer fra Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]