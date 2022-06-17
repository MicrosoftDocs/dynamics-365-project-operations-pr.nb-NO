---
title: Konfigurere regnskap for interne prosjekter
description: Denne artikkelen inneholder informasjon om hvordan du konfigurerer regnskapspraksis for interne prosjekter i Project Operations.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7fc2b7247da699a194688b18aa0a695b06cc44c6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919474"
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
