---
title: Bekrefte en prosjektkontrakt
description: Dette emnet gir informasjon om hvordan du bekrefter en kontrakt i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24da0887c0266d51bddcbbf8efd6f2644b6d0f4f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128295"
---
# <a name="confirm-a-project-contract"></a>Bekrefte en prosjektkontrakt

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

En prosjektkontrakt i Dynamics 365 Project Operations kan være aktiv med årsaken **Bekreftet** eller lukket med årsaken **Tapt**. Når du bekrefter en prosjektkontrakt, oppdateres statusen fra **Utkast** til **Aktiv**, og statusårsaken er **Bekreftet**. En aktiv eller lukket kontrakt kan ikke redigeres eller åpnes på nytt. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Økonomisk innvirkning av å bekrefte en prosjektkontrakt

Når en prosjektkontrakt er bekreftet, vil programmet kostnadene på nytt ved å reversere de eldre faktiske kostnadsverdiene og opprette nye faktiske kostnadsverdier. Disse nye faktiske kostnadsverdiene behandles deretter basert på faktureringsmetoden for den tilknyttede prosjektkontraktlinjen. Hvis de faktiske kostnadsverdiene refererer til en kontraktlinje av typen Tid og materiale, oppretter programmet automatisk de tilsvarende ufakturerte faktiske salgsverdiene på nytt. Hvis de faktiske kostnadsverdiene refererer til en kontraktlinje med fast pris, slutter programmet å behandle de faktiske kostnadene på nytt.

Grenser som ikke må overskrides, oppsett av belastbarhet og priser og kostnadsberegning for de faktiske verdiene evalueres og oppdateres deretter som en del av bekreftelsesprosessen.

## <a name="close-a-project-contract-as-lost"></a>Lukke en prosjektkontrakt som tapt

Når du lukker en prosjektkontrakt som tapt, oppdateres kontraktstatusen til **Lukket**, og statusårsaken er **Tapt**. Prosjektkontrakten blir skrivebeskyttet. Det finnes en bekreftelsesdialogboks før endringene fullføres, fordi du ikke kan åpne en lukket prosjektkontrakt på nytt.

Hvis prosjektkontrakten som er lukket som tapt, refererer til et prosjekt på sine linjer, blir dette prosjektet også merket som lukket. Eventuelle ressursbestillinger fra den dagen og fremover annulleres. Eventuelle ikke-fakturerte faktiske salgsverdier i prosjektkontrakten som ikke allerede er på en faktura, blir tilbakeført.

> [!NOTE]
> I Dynamics 365 Project Operations vil lukking av en prosjektkontrakt som tapt ikke påvirke denne statusen for den tilknyttede salgsmuligheten. Salgsmuligheten forblir åpen og må lukkes manuelt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]