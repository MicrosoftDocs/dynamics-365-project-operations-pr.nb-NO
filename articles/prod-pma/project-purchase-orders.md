---
title: Bestillinger for et prosjekt
description: Denne artikkelen beskriver de forskjellige metodene du kan bruke til å opprette bestillinger for et prosjekt. Metoden du bruker, er avhengig av formålet med bestillingen, og når de innkjøpte varene forbrukes og belastes på et prosjekt.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd891aec5bcab66c5801a5d9ca8abbbf632d662d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081608"
---
# <a name="purchase-orders-for-a-project"></a>Bestillinger for et prosjekt

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver de forskjellige metodene du kan bruke til å opprette bestillinger for et prosjekt. Metoden du bruker, er avhengig av formålet med bestillingen, og når de innkjøpte varene forbrukes og belastes på et prosjekt.

### <a name="methods-for-creating-a-purchase-order"></a>Metoder for å opprette en bestilling

Du kan bruke én av følgende metoder til å opprette en bestilling i Prosjektstyring og regnskap. Formålet med bestillingen avgjør når bestillingen skal forbrukes, og derfor når varer skal belastes til et prosjekt.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Metode</th>
<th>Formål</th>
<th>Forbruk av varer</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Opprette en bestilling direkte fra et prosjekt.</td>
<td>Bruk denne metoden for å kjøpe varer fra en ekstern leverandør for forbruk på et prosjekt. Du kan opprette bestillingen på følgende to måter:
<ul>
<li>Fra selve prosjektet. I dette tilfellet er prosjektet allerede definert for bestillingen.</li>
<li>Ved å navigere til prosjektbestillingen. Du må velge både leverandøren og prosjektet som bestillingen skal opprettes for.</li>
</ul></td>
<td>Varene forbrukes når leverandørfakturaen oppdateres.</td>
</tr>
<tr class="even">
<td>Opprett en bestilling fra en salgsordre.</td>
<td>Bruk denne metoden for å kjøpe varer når du oppretter en salgsordre fra et prosjekt.</td>
<td>Varene forbrukes når salgsordren faktureres til kunden.</td>
</tr>
<tr class="odd">
<td>Opprett en bestilling fra et varebehov.</td>
<td>Bruk denne metoden for å kjøpe varer når du oppretter et varebehov fra et prosjekt.</td>
<td>Varer forbrukes når følgeseddelen for varebehovet er oppdatert.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Når du oppdaterer leverandørfakturaen eller følgeseddelen, blir du bedt om å oppdatere følgeseddelen på varebehovet.

Hvis du vil ha mer informasjon, kan du se [Motta varer på bestilling fra varebehov](tasks/receive-items-purchase-order-item-requirement.md).
