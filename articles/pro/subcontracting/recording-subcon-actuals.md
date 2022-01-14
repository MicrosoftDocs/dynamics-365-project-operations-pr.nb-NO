---
title: Registrering av tid, utgifter og materialbruk for underkontraktkomponenter
description: Dette emnet forklarer hvordan tids-, utgifts- og materialbruk som er registrert på prosjekter fra komponenter med underordnede komponenter, spores av Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 04c78dd48367c3720b8f5ad5d924ed106da6a128
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903485"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Registrering av tid, utgifter og materialbruk på prosjekter for underkontraktkomponenter

[!include [banner](../../includes/dataverse-preview.md)]

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Dette emnet forklarer hvordan tids-, utgifts- og materialbruk som er registrert på prosjekter fra komponenter med underordnede komponenter, spores av Microsoft Dynamics 365 Project Operations.

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
