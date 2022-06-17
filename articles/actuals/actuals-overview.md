---
title: Faktiske verdier
description: Denne artikkelen inneholder informasjon om hvordan du arbeider med faktiske verdier i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2551b7d6d20df170c913e302e734583135265529
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924810"
---
# <a name="actuals"></a>Faktiske verdier

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Faktiske verdier representerer den gjennomgåtte og godkjente økonomiske og planlagte fremdriften for et prosjekt. De opprettes når tids-, utgifts- og materialbruksoppføringer, loggoppføringer og fakturaer godkjennes.

> [!IMPORTANT]
> Faktiske verdier bør ikke redigeres eller slettes fra systemet. Ellers kan økonomisk integritet og eventuell integrasjon med andre finansielle systemer og regnskapssystemer bli negativt påvirket. Microsoft Dynamics 365 Project Operations lar deg bruke reversering og erstatning av faktiske verdier for å redigere faktiske verdier på ulike punkter i prosjektenes forretningsprosesssyklus.

## <a name="recording-actuals-based-on-project-events"></a>Registrere faktiske verdier basert på prosjekthendelser

Project Operations registrerer de finansielle transaksjonene som forekommer i løpet av en livssyklus for prosjektengasjement som faktiske verdier. Opprettelsen av faktiske verdier ved ulike hendelser i livssyklusen varierer avhengig av om prosjektengasjementet bruker faktureringsmodellen for tid og materiell eller faktureringsmodellen med fast pris, og om den er i fasen før salg, eller om det er et internt prosjekt.

Artiklene nedenfor forklarer hva som skjer med tabellen Faktiske verdier ved ulike hendelser for ulike variasjoner:

- [Faktiske verdier virker inn på et tids- og materiellengasjement](ActualsonTM.md)
- [Faktiske verdier virker inn på et engasjement med fast pris](ActualonFP.md)
- [Faktiske verdier virker inn i løpet av førsalgsfasen av et engasjement](ActualonPreSales.md)
- [Faktiske verdier virker inn på et internt prosjekt](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
