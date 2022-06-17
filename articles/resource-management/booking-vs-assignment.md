---
title: Bestillinger i forhold til tildelinger
description: Denne artikkelen inneholder informasjon om forskjellene på ressursbestillinger og ressurstilordninger.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 3410a45ce8401905dc162db66b0975e4aa3350dc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918600"
---
# <a name="bookings-vs-assignments"></a>Bestillinger i forhold til tildelinger

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Bestillinger er forpliktende eller ikke-forpliktende tildeling av ressurser i et prosjekt. Forpliktende bestillinger bruker kapasiteten til en ressurs. Bestillinger representerer organisasjonskonsepter for team, slik at de kan forstå hvordan ressurser skal fordeles på forskjellige prosjekter. Dynamics 365 Project Operations vurderer bestillinger som et konsept på prosjektnivå. 

I motsetning til bestillinger er tilordninger ressursforpliktelser til prosjektoppgaver i prosjektplanen. Ressursene kan navngis eller være generiske.  Når et ressurskrav avledes av prosjektoppgavetilordningene, bruker Project Operations innsatsen for ressurstilordningen til å bygge opp ressurskravdetaljene. Ressurstilordningene blir imidlertid ikke opprettholdt. Oppdateringer for bestillinger som er avledet fra ressurskravet, oppdaterer ikke ressurstilordninger.

Vanligvis vil summen av bestillinger for en ressurs tilsvare summen av ressursens tilordninger på tvers av én eller flere oppgaver. Project Operations håndhever imidlertid ikke denne avtalen. **Avstemming**-visningen viser en prosjektleder steder der bestillingene og tildelingene til en ressurs ikke er de samme.




[!INCLUDE[footer-include](../includes/footer-banner.md)]