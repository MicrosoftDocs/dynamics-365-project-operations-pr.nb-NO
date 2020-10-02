---
title: Oppdatere estimat for kostnad
description: Dette emnet gir informasjon om oppdatering av projeksjonen av innsats for et prosjekt.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 42824cc4cfc2b934f69d319944fe7ee43183955c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897778"
---
# <a name="update-estimate-at-completion"></a>Oppdatere estimat for kostnad

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Det er vanlig at en prosjektleder kan revidere de opprinnelige beregningene på en aktivitet. Reprojisering av prosjekter er en prosjektleders oppfatning av estimater, gitt gjeldende status for et prosjekt. Vi anbefaler imidlertid ikke at prosjektledere endrer tallene i den opprinnelige planen, fordi den opprinnelige planen for prosjektet er den etablerte sannhetskilden for prosjektets tidsplan og kostnadsestimat, som alle interessenter i prosjektet har godtatt.

Det er to måter en prosjektleder kan reprojisere innsats på aktiviteter:

- Overstyr standard anslagstid med ny beregning av gjenstående gjenstående innsats for aktiviteten. 
- Overstyr standard fremdriftsprosent med ny beregning av den virkelige fremdriften for aktiviteten.

Hver av disse metodene forårsaker en ny beregning av aktivitetens ETC, EAC og fremdriftsprosent samt beregnet innsatsavvik for en aktivitet. EAC, ETC- og fremdriftsprosenten på aktivitetssammendragene beregnes på nytt, og det lages en ny projisering av innsatsavvik.
