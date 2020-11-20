---
title: Ressursestimater
description: Dette emnet gir informasjon om hvordan ressursestimater beregnes i Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 454b8931db53739a7bc19364911109802a1ed087
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127384"
---
# <a name="resource-estimates"></a>Ressursestimater

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Ressursestimater kommer fra tidsfaset innsats som er definert i arbeidsnedbrytningsstrukturen, sammen med aktuelle prisdimensjoner. Beregningen er vanligvis **sats/time for hver rolle x timer.** Den tidsfasede innsatsen for hver ressurs lagres i ressurstildelingsoppføringen. Prissettingen er lagret i en forhåndsdefinert prisliste. Enhetsomregning brukes basert på den aktuelle prislisten.

![Ressursestimater](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Standard kostpris og kostnadsvaluta

Kostpriser hentes som standard fra organisasjonsenheten.

## <a name="default-bill-rate-and-sales-currency"></a>Standard fakturasats og salgsvaluta

Salgspriser brukes én gang per avtale. Hierarkiet for salgsprisliste er som standard følgende:

1. Organisasjonen
2. Kunde
3. Tilbud/kontrakt
