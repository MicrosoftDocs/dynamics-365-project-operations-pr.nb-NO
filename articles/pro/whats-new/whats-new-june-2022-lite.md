---
title: Nyheter juni 2022 – Project Operations Lite-distribusjon
description: Denne artikkelen inneholder informasjon om kvalitetsoppdateringene som er tilgjengelige i utgivelsen av Microsoft Dynamics 365 Project Operations Lite-distribusjon fra juni 2022.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8313288ecf7ff1350cd82c62d3d0c291d8a3ded4
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031205"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>Nyheter juni 2022 – Project Operations Lite-distribusjon

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Denne artikkelen gjelder følgende komponenter og versjoner av Microsoft Dynamics 365 Project Operations:

- Project Operations i et Dataverse-miljø, versjon 4.43.0.77 eller 4.43.0.119

## <a name="quality-updates"></a>Kvalitetsoppdateringer

| Funksjonsområdet | Referansenummer | Kvalitetsoppdatering |
| --- | --- | --- |
| Utsetting | 2708885 | Rettet feilmeldingen som vises når en bruker oppretter en oppføring for overskrift for bestilling av ressurs som kan reserveres, der ingen ressurs som kan reserveres, er fylt ut. |
| Prosjektplanlegging og sporing | 2629441 | Rettet logikken for utløsing av arbeidsflyt for å forhindre en uendelig løkke når prosjektoppgaver oppdateres. |
| Tid og utgifter | 2641209 | Import av tidsoppføringer fra tilordninger/bestillinger må beholde en ressursreferanse som kan reserveres. |
| Prosjektplanlegging og sporing | 2651148 | Prosjektdokumenttoppteksten må beskyttes.|
| Prosjektplanlegging og sporing | 2653145 | La til valideringer for å sikre at det ikke kan opprettes en prosjektoppføring med ugyldige tegn i navnet. |
| Tid og utgifter | 2654710 | Rettet filtreringen på **Godkjenninger**-siden. |
| Fakturering og prising | 2667805 | La til valideringer for å forhindre at fakturerte faktiske salg opprettes hvis det ikke finnes støttende ufakturerte faktiske salg. |
| Fakturering og prising | 2668378 | La til valideringer for å forhindre at en egendefinert prisdimensjon legges til, med mindre et logisk navn og et feltnavn fylles ut. |
| Tid og utgifter | 2700428 | Forbedret godkjenningslogikken for å sikre at andre godkjenningssett for prosjektet kan behandles selv om et av godkjenningssettene står fast i systemjobber. |
