---
title: Tilstandsoverganger på en leverandørfaktura
description: Dette emnet forklarer tilstandsovergangene for en leverandørfaktura i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7efb52621ee325d5025dfad0b45218d1fe20a063
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584700"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Tilstandsoverganger på en leverandørfaktura

[!include [banner](../../includes/dataverse-preview.md)]

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Dette emnet forklarer tilstandsovergangene for en leverandørfaktura i Microsoft Dynamics 365 Project Operations. Følgende tilstander brukes: **Utkast**, **Til gjennomgang**, **Bekreftet**, **På vent** og **Annullert**.

Illustrasjonene nedenfor viser tilstandsovergangene.

![Modell for tilstandsoverganger på underkontrakt](../media/VI_State_Model.jpg)

Tabellen nedenfor forklarer hva hver tilstand representerer i livssyklusen til en leverandørkontrakt i Project Operations.

| State | Bekrivelse | Tillatte overføringer |
| --- | --- | --- |
| Kladd | Denne tilstanden er starttilstanden for en leverandørfaktura. Linjene og prisene kan endres. En leverandørfaktura i denne tilstanden kan redigeres eller slettes. | Pågår |
| Til gjennomgang | Denne tilstanden representerer behandlingstilstanden for en leverandørfaktura. Minst én leverandørfakturalinje har verifiseringsstatusen **Pågår**. | Bekreftet, På vent |
| Bekreftet | Denne tilstanden representerer fasen i en leverandørfaktura der appen har opprettet faktiske kostnader for hver leverandørfakturalinje. Alle koblede faktiske kostnader som samsvarte med leverandørfakturalinjene, er reversert og erstattet med faktiske kostnader fra disse leverandørfakturalinjene. En leverandørfaktura i denne tilstanden kan ikke redigeres eller slettes. Du kan bruke **Annuller**-knappen til å annullere en bekreftet leverandørfaktura. Annuller-handlingen reverserer virkningen av Bekreft-handlingen. | Kansellert |
| På vent | <p>Denne tilstanden representerer en fase i en leverandørfaktura der leverandørfakturaen ikke kan flytte på grunn av et problem med fakturaen eller leverandørens status. En leverandørfaktura i denne tilstanden kan ikke bekreftes, annulleres, redigeres eller slettes.</p><p>Du kan bruke handlingen Åpne på nytt til å flytte leverandørfakturaen til tilstanden **Utkast** eller **Til gjennomgang**. Hvis minst én linje på leverandørfakturaen har verifiseringsstatusen **Pågår** eller **Fullført**, åpnes leverandørfakturaen på nytt i tilstanden **Til gjennomgang**. Hvis alle linjene på leverandørfakturaen har verifiseringsstatusen **Ikke startet**, åpnes leverandørfakturaen på nytt i **Utkast**-tilstand.</p> | Utkast, Til gjennomgang |
| Kansellert | Denne tilstanden representerer fasen i en underkontrakt der faktisk levering av materiell og/eller arbeid med underordnede ressurser ikke lenger er nødvendig. En underkontrakt i denne tilstanden kan ikke brukes til å estimere og bemanne prosjektkrav for ressurser og materiell, og det kan heller ikke refereres til den ved tids-, utgifts- og materialbruk for et prosjekt. En underkontrakt i denne tilstanden kan ikke redigeres eller slettes. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]