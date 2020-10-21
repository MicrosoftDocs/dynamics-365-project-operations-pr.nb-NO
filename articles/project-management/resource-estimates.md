---
title: Ressursestimater
description: Dette emnet gir informasjon om hvordan ressursestimater beregnes i Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: f255b2cbf290973ce62fe2c1c121bd1df15a7392
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3928592"
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
