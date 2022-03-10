---
title: Prosjektsalgsordrer for tids og materialprosjekter
description: Dette emnet forklarer hvordan du oppretter prosjektbaserte salgsordrer for tids- og materialprosjekter.
author: Yowelle
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: bec39790b0a41e72b4cc9798d37a01e87029e18335f77d895680aafbb74fac3b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992848"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Prosjektsalgsordrer for tids og materialprosjekter

[!include[banner](../includes/banner.md)]

Dette emnet beskriver hvordan du oppretter en salgsordre for et prosjekt. Salgsordrer kan bare opprettes for prosjekter av typen **tid og materiale**.

Hvis et tid og materiale-prosjekt har flere finansieringskilder i prosjektkontrakten, må du aktivere parameteren **Tillat salgsordrer for prosjekter med flere finansieringskilder** på siden **Parametere for prosjektstyring og regnskap**. 

> [!NOTE]
> - Støtte for prosjektsalgsordrer som har flere finansieringskilder, er tilgjengelig fra programutgivelse 10.0.2 og nyere.
> - Parameteren for å aktivere støtten for prosjektsalgsordrer med flere finansieringskilder, blir fjernet i april 2020-utgivelsesbølgen, og etter dette vil funksjonaliteten alltid være aktivert.

Du kan opprette prosjektbaserte salgsordrer på to måter:

- Gå til selve prosjektet. I handlingsruten velger du **Behandle > Vareoppgaver > Salgsordre**. Prosjektinformasjonen settes som standard til salgsordren fra prosjektet. Hvis prosjektkontrakten har mer enn én finansieringskilde, må du velge finansieringskilden for å angi kunden for salgsordren. Hvis det bare er én finansieringskilde for prosjektet, blir kunden angitt automatisk.
- Gå til listesiden **Alle salgsordrer**, og opprett en ny salgsordre. Du må velge prosjektet for salgsordren. Etter at du har valgt prosjektet, blir kunden angitt fra finansieringskilden, eller du må velge finansieringskilden hvis prosjektkontrakten har flere finansieringskilder.



[!INCLUDE[footer-include](../includes/footer-banner.md)]