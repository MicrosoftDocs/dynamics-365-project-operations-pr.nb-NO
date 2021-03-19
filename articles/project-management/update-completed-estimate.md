---
title: Oppdatere estimat for kostnad
description: Dette emnet gir informasjon om oppdatering av projeksjonen av innsats for et prosjekt.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
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
ms.openlocfilehash: 0e63bdb815a6f758c57d055c8c03d92e04700445
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286440"
---
# <a name="update-estimate-at-completion"></a>Oppdatere estimat for kostnad

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Det er vanlig at en prosjektleder kan revidere de opprinnelige beregningene på en aktivitet. Reprojisering av prosjekter er en prosjektleders oppfatning av estimater, gitt gjeldende status for et prosjekt. Vi anbefaler imidlertid ikke at prosjektledere endrer tallene i den opprinnelige planen, fordi den opprinnelige planen for prosjektet er den etablerte sannhetskilden for prosjektets tidsplan og kostnadsestimat, som alle interessenter i prosjektet har godtatt.

Det er to måter en prosjektleder kan reprojisere innsats på aktiviteter:

- Overstyr standard anslagstid med ny beregning av gjenstående gjenstående innsats for aktiviteten. 
- Overstyr standard fremdriftsprosent med ny beregning av den virkelige fremdriften for aktiviteten.

Hver av disse metodene forårsaker en ny beregning av aktivitetens ETC, EAC og fremdriftsprosent samt beregnet innsatsavvik for en aktivitet. EAC, ETC- og fremdriftsprosenten på aktivitetssammendragene beregnes på nytt, og det lages en ny projisering av innsatsavvik.


[!INCLUDE[footer-include](../includes/footer-banner.md)]