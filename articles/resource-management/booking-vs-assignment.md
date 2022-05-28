---
title: Bestillinger i forhold til tildelinger
description: Dette emnet inneholder informasjon om forskjellene mellom ressursbestillinger og ressurstildelinger.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: b06555ec48e50f88c11872336539ca88c5cef34a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591279"
---
# <a name="bookings-vs-assignments"></a>Bestillinger i forhold til tildelinger

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Bestillinger er forpliktende eller ikke-forpliktende tildeling av ressurser i et prosjekt. Forpliktende bestillinger bruker kapasiteten til en ressurs. Bestillinger representerer organisasjonskonsepter for team, slik at de kan forstå hvordan ressurser skal fordeles på forskjellige prosjekter. Dynamics 365 Project Operations vurderer bestillinger som et konsept på prosjektnivå. 

I motsetning til bestillinger er tilordninger ressursforpliktelser til prosjektoppgaver i prosjektplanen. Ressursene kan navngis eller være generiske.  Når et ressurskrav avledes av prosjektoppgavetilordningene, bruker Project Operations innsatsen for ressurstilordningen til å bygge opp ressurskravdetaljene. Ressurstilordningene blir imidlertid ikke opprettholdt. Oppdateringer for bestillinger som er avledet fra ressurskravet, oppdaterer ikke ressurstilordninger.

Vanligvis vil summen av bestillinger for en ressurs tilsvare summen av ressursens tilordninger på tvers av én eller flere oppgaver. Project Operations håndhever imidlertid ikke denne avtalen. **Avstemming**-visningen viser en prosjektleder steder der bestillingene og tildelingene til en ressurs ikke er de samme.




[!INCLUDE[footer-include](../includes/footer-banner.md)]