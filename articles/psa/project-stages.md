---
title: Prosjektfasetyper
description: Denne emnet gir informasjon om prosjektfaser.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 521bf4b3090473a603626a99fded53906b644a7a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081671"
---
# <a name="project-stage-types"></a>Prosjektfasetyper 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Prosjektfaser skal vise statusen til prosjektet etter hvert som det pågår. Tilpassinger kan brukes til automatisk å oppdatere fasene med forretningsprosessflyter, Power Automate eller plugin-modulutvidelser.

Følgende faser er definert i standard BPF:

- Nytt
- Tilbud
- Plan
- Lever
- Fullstendig
- Lukk 

## <a name="new"></a>Ny

Når du oppretter et prosjekt, er prosjektfasen satt til **Ny**. Hvis prosjektet ble opprettet fra en mal, kan det ha tidsplan-, estimat- og teamdata. Ellers er det bare en disposisjon av prosjektet, og de resterende komponentene må registreres.

## <a name="quote"></a>Tilbud

Når du knytter et prosjekt til et tilbud, eller når du oppretter et prosjekt fra et tilbud, er prosjektfasen satt til **Tilbud** , og de estimerte start- og sluttdatoene oppdateres også. Når prosjektet er i **Tilbud** -fasen, vises detaljene for tilbudet i kategorien **Salg** på **Prosjektenhet** -siden.

## <a name="plan"></a>Plan

Når du har vunnet et tilbud som er tilknyttet et prosjekt, og når dette engasjementet går videre til **Kontrakt** -fasen, oppdateres prosjektfasen til **Plan**. Når prosjektet er i **Plan** -fasen, vises detaljene for kontrakten på **Prosjektenhet** -siden.

## <a name="deliver"></a>Lever

Når prosjektplanen er fullført, og du er klar til å starte prosjektet, skal prosjektlederen oppdatere prosjektfasen til **Lever** for å vise at prosjektet har startet.

## <a name="complete"></a>Fullstendig 

Når arbeidet for prosjektet er fullført, kan prosjekt lederen oppdatere fasen til **Fullfør**. Ved å oppdatere prosjektstadiet til **Fullfør** angir prosjektlederen at arbeidet er 100 prosent fullført, men at prosjektet holdes åpent slik at eventuelle ventende tids- eller utgiftsoppføringer kan registreres.

## <a name="close"></a>Lukk

Når alle transaksjoner er registrert for prosjektet, kan prosjektlederen oppdatere fasen til **Lukk**. På dette tidspunktet kan det ikke registreres noen transaksjoner, og prosjektet er skrivebeskyttet.