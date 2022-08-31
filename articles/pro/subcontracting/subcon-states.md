---
title: Tilstandsoverganger på en underkontrakt
description: Denne artikkelen forklarer tilstandsovergangene for en underkontrakt i Microsoft Dynamics 365 Project Operations etter hvert som underkontrakten opprettes, utføres og lukkes.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 02553099a6728c19c219659dff431ff9a5cf10fc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261287"
---
# <a name="state-transitions-on-a-subcontract"></a>Tilstandsoverganger på en underkontrakt 

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Denne artikkelen forklarer tilstandsovergangene for en underkontrakt i Microsoft Dynamics 365 Project Operations. Hver tilstand representeres som utkast, bekreftet, lukket eller annullert. Bildet nedenfor viser statusovergangene.

![Tilstandsmodell for underkontrakt](../media/SubconStates.png)  

Tabellen nedenfor viser en beskrivelse av hva hver tilstand representerer i livssyklusen til en underkontrakt i Project Operations.

| State | Description | Tillatte overføringer |
| --- | --- | --- |
| Kladd | Dette representerer starttilstanden for en underkontrakt. Forhandlinger med leverandøren pågår. Linjene og prisene kan endres. En underkontrakt i denne tilstanden kan brukes til å estimere og bemanne prosjektkrav for ressurser og materiell. Det kan også refereres til tids-, utgifts- og materialbruk for et prosjekt. En underkontrakt i denne tilstanden kan redigeres og slettes. | Bekreftet |
| Bekreftet | Dette representerer fasen i en underkontrakt etter at forhandlinger med leverandør om prissetting og linjeelementer som blir kjøpt, er fullført. Den faktiske materiellleveringen og/eller arbeidet med underkontraktressurser pågår imidlertid fremdeles. En underkontrakt i denne tilstanden kan brukes til å estimere og bemanne prosjektkrav for ressurser og materiell. Det kan også refereres til tids-, utgifts- og materialbruk for et prosjekt. En underkontrakt i denne tilstanden kan ikke redigeres eller slettes. Med **Avbryt**-knappen kan du annullere en bekreftet underkontrakt. **Åpne på nytt**-knappen gjør det mulig å åpne underkontrakten på nytt for å hente den tilbake til **Utkast**-status. Bruk **Lukk**-knappen til å lukke en bekreftet underkontrakt. | Avsluttet <br> Kansellert <br> Kladd |
| Avsluttet | Dette representerer fasen i en underkontrakt når faktisk levering av materiell og/eller arbeid med underordnede ressurser er fullført. En underkontrakt i denne tilstanden kan ikke lenger brukes til å estimere og bemanne prosjektkrav for ressurser og materiell. Den kan heller ikke lenger refereres til for tids-, utgifts- og materialbruk for et prosjekt. En underkontrakt i denne tilstanden kan ikke redigeres eller slettes. | None |
| Kansellert | Dette representerer fasen i en underkontrakt når faktisk levering av materiell og/eller arbeid med underordnede ressurser ikke lenger er nødvendig. En underkontrakt i denne tilstanden kan ikke brukes til å estimere og bemanne prosjektkrav for ressurser og materiell, og den kan heller ikke refereres til tids-, utgifts- og materialbruk for et prosjekt. En underkontrakt i denne tilstanden kan ikke redigeres eller slettes. | None |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
