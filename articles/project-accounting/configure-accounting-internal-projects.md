---
title: Konfigurere regnskap for interne prosjekter
description: Dette emnet gir informasjon om hvordan du konfigurerer regnskapspraksiser for interne prosjekter i Project Operations.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: be1dcd1b6b18591c99c904e0013d9870c7cafe1077fa6e9634f2e9f495190848
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005538"
---
# <a name="configure-accounting-for-internal-projects"></a>Konfigurere regnskap for interne prosjekter

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Interne prosjekter gjør det mulig for selskaper å spore kostnader relatert til aktiviteter som ikke blir fakturert til en kunde. Eksempler på interne prosjekter er:

- Utvikling av et produkt, for eksempel en mobilapp, og sporing av kostnadene som er knyttet til utviklingen.
- Behandle tid og utgifter før salg. Dette interne prosjektet før salg kan konverteres til et fakturerbart prosjekt senere hvis tilbudet er vunnet.

Prosjekter som ikke er knyttet til en kontrakt i Dynamics 365 Project Operations, behandles som interne. Prosjektkostnads- og omsetningsprofiler brukes ikke til å fastsette regnskapsregler for prosjektet. Interne prosjektkostnader bokføres alltid ved hjelp av resultatprinsipper. Hovedbokkontoer for inn bokføringer defineres på siden **Finansposteringsoppsett**.

- Tidstransaksjoner bokføres ved å debitere **Kostnad**-kontoen og kreditere **Lønnstildeling**-kontoen.
- Utgiftstransaksjoner bokføres ved å debitere **Kostnad**-kontoen og kreditere kontoen **Forskyvningskonto for utgift**.
- Varetransaksjoner posteres ved å debitere kontoen **Kostnad** og kreditere kontoen **Kostnad – Vare**.

Når transaksjoner er bokført til prosjektet, tilbakefører systemet alle akkumulerte transaksjoner og oppretter nye fakturerbare transaksjoner hvis prosjektet er tilknyttet en prosjektkontrakt. De fakturerbare transaksjonene følger regnskapsreglene som er definert i den respektive kostnads- og omsetningsprofilen for prosjektet.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
