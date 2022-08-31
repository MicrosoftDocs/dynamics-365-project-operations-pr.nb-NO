---
title: Registrering av tid, utgifter og materialbruk for underkontraktkomponenter
description: Denne artikkelen forklarer hvordan tids-, utgifts- og materialbruk som er registrert på prosjekter fra komponenter med underordnede komponenter, spores av Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 89fbbfcd1535660e92d0cc80beb91029331e990f
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261149"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Registrering av tid, utgifter og materialbruk på prosjekter for underkontraktkomponenter

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Denne artikkelen forklarer hvordan tids-, utgifts- og materialbruk som er registrert på prosjekter fra komponenter med underordnede komponenter, spores av Microsoft Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Kostnadsberegning for underleverandørtid på prosjekter
I Project Operations kan kontraktarbeidere registrere tid på prosjekter på samme måte som ansatte. Når en kontraktarbeider angir tid på prosjekter og/eller prosjektoppgaver, kan han eller hun velge en bestemt underkontrakt og underkontraktlinje.

Når tiden som er sendt av kontraktarbeidere, godkjennes, registreres prosjektkostnaden ved hjelp av enhetskostnadssatsen som er angitt for kontraktarbeiderressursen i **Rollepriser**-delen i innkjøpsprislisten i underkontrakten.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Kostnadsberegning for underkontraktutgifter på prosjekter
Når du angir utgifter som påløper for prosjekter, kan du velge en underkontrakt og underkontraktlinje på utgiftsoppføringen. 

Når denne utgiftsoppføringe er sendt og godkjent, registreres utgiftskostnaden på prosjektet basert på enhetskostnaden som er angitt for transaksjonskategorien i delen **Kategoripriser** i innkjøpsprislisten i underkontrakten.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Kostnadsberegning for underkontraktmaterialer på prosjekter
Når du angir materialbruk for prosjekter, kan du velge en underkontrakt og underkontraktlinje i materialbrukloggen. Når materialbrukloggen er sendt og godkjent, registreres materialkostnaden på prosjektet basert på enhetskostnaden som er angitt for produktet i delen **Prislisteelementer** i underkontraktprislisten.

Materialbruk kan også registreres for ikke-katalog-produkter på prosjekter. Denne typen materialbruk kan også kobles til en underkontrakt og underkontraktlinje. Når du registrerer materialbruk for ikke-katalog-produkter, må du angi enhetskostnaden for ikke-katalog-produktet. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
