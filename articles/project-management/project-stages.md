---
title: Prosjektfaser
description: Dette emnet gir informasjon om prosjektstadier som er tilgjengelige i Microsoft Dynamics Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: aa3d692a46165b01eafbd7619578cead8dd912d6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127485"
---
# <a name="project-stages"></a>Prosjektfaser

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Prosjektfaser skal vise statusen til prosjektet etter hvert som det pågår. Tilpassinger kan brukes til automatisk å oppdatere fasene med forretningsprosessflyter, Power Automate eller plugin-modulutvidelser.

Følgende faser er definert i standard forretningsprosessflyt:

- Nye
- Tilbud
- Planlegg
- Lever
- Fullført
- Lukk 

## <a name="new"></a>Nye

Når du oppretter et prosjekt, er prosjektfasen satt til **Ny**. Hvis prosjektet ble opprettet fra en mal, kan det ha tidsplan-, estimat- og teamdata. Ellers er det en disposisjon av prosjektet, og de resterende komponentene må registreres.

## <a name="quote"></a>Tilbud

Når du knytter et prosjekt til et tilbud, eller når du oppretter et prosjekt fra et tilbud, er prosjektfasen satt til **Tilbud**, og de estimerte start- og sluttdatoene oppdateres også. Når prosjektet er i **Tilbud**-fasen, vises detaljene for tilbudet i kategorien **Salg** på **Prosjektenhet**-siden.

## <a name="plan"></a>Plan

Når du har vunnet et tilbud som er tilknyttet et prosjekt, og når dette engasjementet går videre til **Kontrakt**-fasen, oppdateres prosjektfasen til **Plan**. Når prosjektet er i **Plan**-fasen, vises detaljene for kontrakten på **Prosjektenhet**-siden.

## <a name="deliver"></a>Lever

Når prosjektplanen er fullført, og du er klar til å starte prosjektet, skal prosjektlederen oppdatere prosjektfasen til **Lever** for å vise at prosjektet har startet.

## <a name="complete"></a>Fullstendig 

Når arbeidet for prosjektet er fullført, kan prosjekt lederen oppdatere fasen til **Fullfør**. Ved å oppdatere prosjektstadiet til **Fullfør** angir prosjektlederen at arbeidet er 100 prosent fullført, men at prosjektet holdes åpent slik at eventuelle ventende tids- eller utgiftsoppføringer kan registreres.

## <a name="close"></a>Lukk

Når alle transaksjoner er registrert for prosjektet, kan prosjektlederen oppdatere fasen til **Lukk**. På dette tidspunktet kan det ikke registreres noen transaksjoner, og prosjektet er skrivebeskyttet.



[!INCLUDE[footer-include](../includes/footer-banner.md)]