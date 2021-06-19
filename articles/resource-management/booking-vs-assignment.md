---
title: Bestillinger i forhold til tildelinger
description: Dette emnet inneholder informasjon om forskjellene mellom ressursbestillinger og ressurstildelinger.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c1a1003af0b23c4be44fefac0b3c4ea725f96b2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012778"
---
# <a name="bookings-vs-assignments"></a>Bestillinger i forhold til tildelinger

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Bestillinger er forpliktende eller ikke-forpliktende tildeling av ressurser i et prosjekt. Forpliktende bestillinger bruker kapasiteten til en ressurs. Bestillinger representerer organisasjonskonsepter for team, slik at de kan forstå hvordan ressurser skal fordeles på forskjellige prosjekter. Dynamics 365 Project Operations vurderer bestillinger som et konsept på prosjektnivå. 

I motsetning til bestillinger er tilordninger ressursforpliktelser til prosjektoppgaver i prosjektplanen. Ressursene kan navngis eller være generiske.  Når et ressurskrav avledes av prosjektoppgavetilordningene, bruker Project Operations innsatsen for ressurstilordningen til å bygge opp ressurskravdetaljene. Ressurstilordningene blir imidlertid ikke opprettholdt. Oppdateringer for bestillinger som er avledet fra ressurskravet, oppdaterer ikke ressurstilordninger.

Vanligvis vil summen av bestillinger for en ressurs tilsvare summen av ressursens tilordninger på tvers av én eller flere oppgaver. Project Operations håndhever imidlertid ikke denne avtalen. **Avstemming**-visningen viser en prosjektleder steder der bestillingene og tildelingene til en ressurs ikke er de samme.




[!INCLUDE[footer-include](../includes/footer-banner.md)]