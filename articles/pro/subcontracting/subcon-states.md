---
title: Tilstandsoverganger på en underkontrakt
description: Dette emnet forklarer tilstandsovergangene for en underkontrakt i Microsoft Dynamics 365 Project Operations etter hvert som underkontrakten opprettes, utføres og lukkes.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d67f4a3cd834c25462304c2d75c824427fcbd034
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903486"
---
# <a name="state-transitions-on-a-subcontract"></a>Tilstandsoverganger på en underkontrakt 

[!include [banner](../../includes/dataverse-preview.md)]

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Dette emnet forklarer tilstandsovergangene for en underkontrakt i Microsoft Dynamics 365 Project Operations. Hver tilstand representeres som utkast, bekreftet, lukket eller annullert. Bildet nedenfor viser statusovergangene.

![Tilstandsmodell for underkontrakt](../media/SubconStates.png)  

Tabellen nedenfor viser en beskrivelse av hva hver tilstand representerer i livssyklusen til en underkontrakt i Project Operations.

| State | Description | Tillatte overføringer |
| --- | --- | --- |
| Kladd | Dette representerer starttilstanden for en underkontrakt. Forhandlinger med leverandøren pågår. Linjene og prisene kan endres. En underkontrakt i denne tilstanden kan brukes til å estimere og bemanne prosjektkrav for ressurser og materiell. Det kan også refereres til tids-, utgifts- og materialbruk for et prosjekt. En underkontrakt i denne tilstanden kan redigeres og slettes. | Bekreftet |
| Bekreftet | Dette representerer fasen i en underkontrakt etter at forhandlinger med leverandør om prissetting og linjeelementer som blir kjøpt, er fullført. Den faktiske materiellleveringen og/eller arbeidet med underkontraktressurser pågår imidlertid fremdeles. En underkontrakt i denne tilstanden kan brukes til å estimere og bemanne prosjektkrav for ressurser og materiell. Det kan også refereres til tids-, utgifts- og materialbruk for et prosjekt. En underkontrakt i denne tilstanden kan ikke redigeres eller slettes. Med **Avbryt**-knappen kan du annullere en bekreftet underkontrakt. **Åpne på nytt**-knappen gjør det mulig å åpne underkontrakten på nytt for å hente den tilbake til **Utkast**-status. Bruk **Lukk**-knappen til å lukke en bekreftet underkontrakt. | Avsluttet <br> Kansellert <br> Kladd |
| Avsluttet | Dette representerer fasen i en underkontrakt når faktisk levering av materiell og/eller arbeid med underordnede ressurser er fullført. En underkontrakt i denne tilstanden kan ikke lenger brukes til å estimere og bemanne prosjektkrav for ressurser og materiell. Den kan heller ikke lenger refereres til for tids-, utgifts- og materialbruk for et prosjekt. En underkontrakt i denne tilstanden kan ikke redigeres eller slettes. | None |
| Kansellert | Dette representerer fasen i en underkontrakt når faktisk levering av materiell og/eller arbeid med underordnede ressurser ikke lenger er nødvendig. En underkontrakt i denne tilstanden kan ikke brukes til å estimere og bemanne prosjektkrav for ressurser og materiell, og den kan heller ikke refereres til tids-, utgifts- og materialbruk for et prosjekt. En underkontrakt i denne tilstanden kan ikke redigeres eller slettes. | None |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
