---
title: Deaktiver prislister
description: Dette emnet forklarer hvordan du deaktiverer eller fjerner ubrukte eller gamle prislister.
author: rumant
manager: AnnBe
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3fa902e93815002be7d6915880cd7759dbbde5ef
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701958"
---
# <a name="deactivate-price-lists"></a>Deaktiver prislister 

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Hvis du vil fjerne gamle eller ubrukte prislister fra Dynamics 365 Project Operations, er det to trinn du må fullføre. 

1. Fjern eller slett prislisten fra bestemte sider.
2. Deaktiver eller slett prislisten fra de aktive prislistene på **Prislister**-siden.

>[!IMPORTANT]
> Du må fullføre begge trinnene for å fjerne en prisliste fullstendig. Bare å utføre trinn 2, som er å slette eller deaktivere prislisten direkte fra visningen Aktive prislister, er ikke tilstrekkelig. Du må også slette tilknytningen til denne prislisten fra alle stedene nevnt i trinn 1.

## <a name="delete-the-price-list-from-specific-pages"></a>Slett prislisten fra bestemte sider
1. Hvis du vil slette en prisliste fra Project Operations, går du til følgende sider:  

      - **Prosjektparametere**-siden > **Prislister**-fanen
      - **Organisasjonsenhet**-siden > **Prislister**-rutenettet
      - **Konto**-siden > **Prosjektprislister**-rutenettet
      - **Prosjekttilbud**-siden > **Prosjektprislister**-rutenettet: Dette gjelder for alle aktive prosjekttilbud.
      - **Prosjektkontrakter**-siden > **Prosjektprislister**-rutenettet: Dette gjelder for alle aktive prosjektkontrakter.

 2. For hver side må du velge prislisten du vil slette, og deretter velge **Slett**. 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a>Slett eller deaktiver prislisten fra Prislister-siden
 
1. Hvis du vil slette en prisliste fra de aktive prislistene, går du til **Salg** > **Kunder** > **Prislister**. 
2. Velg prislisten du vil slette, og velg deretter **Slett**. Hvis det refereres til prislisten for eksisterende transaksjoner, kan du ikke slette den. Hvis dette skjer, kan du deaktivere prislisten slik at den ikke vises i noen visninger. 
3. Hvis du vil deaktivere prislisten, velger du prislisten på nytt, og deretter velger du **Deaktiver**.   
