---
title: Nyheter mars 2022 – Project Operations Lite-distribusjon
description: Denne artikkelen inneholder informasjon om kvalitetsoppdateringene som er tilgjengelige i utgivelsen av Project Operations Lite-distribusjon fra mars 2022.
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 321d59568bfd33bb00a1500afe514fbecf9a0250
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934240"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>Nyheter mars 2022 – Project Operations Lite-distribusjon

_Gjelder: Lite-distribusjon – avtale til proformafakturering_

Denne artikkelen gjelder følgende komponenter og versjoner av Microsoft Dynamics 365 Project Operations:

- Project Operations i et Dataverse-miljø, versjon 4.30.0.99

## <a name="features-included-in-this-release"></a>Funksjoner som er inkludert i denne versjonen

- Underkontrakter: Oppretting av leverandørfaktura og samsvarsopplevelser

## <a name="quality-updates"></a>Kvalitetsoppdateringer

| Funksjonsområdet | Referansenummer | Kvalitetsoppdatering |
| --- | --- | --- |
| Tid og utgifter | 2388011 | Vis avslagskommentarer til innsendere av tidsoppføringer under massegodkjenning. |
| Prosjektplanlegging og sporing | 2495294 | Prosjektdetaljer kan ikke redigeres på **Oppgavedetaljer**-siden. |
| Fakturering og prising | 2499605 | Kontraktmilepæler som opprettes fra tilbudsmilepæler, er feilmarkert som skrivebeskyttet. |
| Prosjektplanlegging og sporing | 2506050 | Operasjonssettet står på vent i én time hvis det ikke er endringer som skal lagres. Settet merkes deretter som **Mislykket**, mens det skulle vært fullført umiddelbart. |
| Fakturering og prising | 2507401 | Standard kontraktsenheter er feil angitt på prosjekter på grunn av feil hurtigbufring. |
| Fakturering og prising | 2541660 | **Validering av oppretting av salgsordre** i dobbel skriving skal bare være for prosjektbaserte ordrer. |
| Fakturering og prising | 2552745 | Avgifter deles ikke mellom kunder som har konfigurert delte faktureringsregler. |
| Fakturering og prising | 2558859 | Forbedrede feilmeldinger når prisdimensjoner er konfigurert. |
| Fakturering og prising | 2558933 | **Import fra prosjektestimater** mislykkes når **msdyn\_project** er lagt til som en prisdimensjon. |
| Fakturering og prising | 2559101 | Sletting av prosjektparametere er ikke blokkert og forårsaker problemer. |
|   Administrasjon av salgsmuligheter | 2570390 | Programtillegget for dobbel skriving tvinger kontotypen i tilbud, bestillinger og muligheter til å være **Kunde**, selv når denne kontotypen ikke er korrekt. |
| Fakturering og prising | 2586097 | Deling av fakturerte faktiske kostnader reverseres ikke når et prosjekt fjernes fra en prosjektkontraktlinje. |
| Fakturering og prising | 2589619 | Avgifter på materiell som ikke er i katalogen, overføres til ufakturert faktisk salg og til fakturaen. |
|   Administrasjon av salgsmuligheter | 2594015 | Et tilbud kan ikke lukkes som vunnet for kunder som har **Net60**-betalingsbetingelser. |
| Prosjektplanlegging og sporing | 2595841 | I Project for the Web mottar brukerne en feilmelding om en manglende **msdyn\_actualstart** når de oppretter en ny ressursforespørsel. |
| Tid og utgift | 2602511 | Feltet **Avvist av** for tidsoppføringer viser **System** i stedet for en navngitt bruker som avviser. |
| Tid og utgift | 2602528 | En prosjektgodkjenner kan godkjenne tid på prosjekter der de ikke er oppført som godkjennere. |
| Fakturering og prising | 2608550 | En korrigeringsfaktura kan bekreftes selv om det ikke er endringer i originalen. |

## <a name="removed-and-deprecated-features"></a>Funksjoner som er fjernet og avskrevet

Artikkelen [Fjernede eller avskrevne funksjoner i Project Operations](../../whats-new/removed-depreciated-features-project.md) beskriver funksjoner som er fjernet eller avskrevet for Dynamics 365 Project Operations.

- En fjernet funksjon er ikke lenger tilgjengelig i produktet.
- En avskrevet funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.

En kunngjøring om avskrivning vil vises i artikkelen [Fjernede eller avskrevne funksjoner i Project Operations](../../whats-new/removed-depreciated-features-project.md) 12 måneder før en funksjon blir fjernet fra produktet.
