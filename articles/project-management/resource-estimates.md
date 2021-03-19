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
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286530"
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]