---
title: Konfigurere regnskap for interne prosjekter
description: Dette emnet gir informasjon om hvordan du konfigurerer regnskapspraksiser for interne prosjekter i Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 504e7481cb2aee6310cb4ace2d0791d1c7fe360d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081554"
---
# <a name="configure-accounting-for-internal-projects"></a>Konfigurere regnskap for interne prosjekter

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Interne prosjekter gjør det mulig for selskaper å spore kostnader relatert til aktiviteter som ikke blir fakturert til en kunde. Eksempler på interne prosjekter er:

- Utvikling av et produkt, for eksempel en mobilapp, og sporing av kostnadene som er knyttet til utviklingen.
- Behandle tid og utgifter før salg. Dette interne prosjektet før salg kan konverteres til et fakturerbart prosjekt senere hvis tilbudet er vunnet.

Alle prosjekter som ikke er knyttet til en kontrakt i Dynamics 365 Project Operations, blir behandlet som interne. Prosjektkostnads- og omsetningsprofiler brukes ikke til å fastsette regnskapsregler for prosjektet. Interne prosjektkostnader bokføres alltid ved hjelp av resultatprinsipper. Hovedbokkontoer for inn bokføringer defineres på siden **Finansposteringsoppsett**.

- Tidstransaksjoner bokføres ved å debitere **Kostnad** -kontoen og kreditere **Lønnstildeling** -kontoen.
- Utgiftstransaksjoner bokføres ved å debitere **Kostnad** -kontoen og kreditere kontoen **Forskyvningskonto for utgift**.

Når transaksjoner er bokført til prosjektet, tilbakefører systemet alle akkumulerte transaksjoner og oppretter nye fakturerbare transaksjoner hvis prosjektet er tilknyttet en prosjektkontrakt. De fakturerbare transaksjonene følger regnskapsreglene som er definert i den respektive kostnads- og omsetningsprofilen for prosjektet.


