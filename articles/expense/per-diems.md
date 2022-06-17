---
title: Kostgodtgjørelser
description: Denne artikkelen inneholder informasjon om kostgodtgjørelsesregler som brukes i Utgiftshåndtering.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 8fa634c23391c47c0c583647165dce2b396535e5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930192"
---
# <a name="per-diems"></a>Kostgodtgjørelser

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_


En kostgodtgjørelse er en godtgjørelse som betales til en arbeider som er på arbeidsreise. I Utgiftshåndtering kan du opprette regler for kostgodtgjørelse for forskjellige reisesituasjoner. Kostgodtgjørelsessatser kan baseres på tiden på året, reisestedet eller begge deler. Når du oppretter en kostgodtgjørelsesregel, kan du angi at en prosentsats av kostgodtgjørelsessatsen skal tilbakeholdes hvis en arbeider mottar gratis måltider eller tjenester. Du kan også angi et minimum og maksimum antall timer som kostgodtgjørelsessatsen kan gjelde for en arbeiders reise.

## <a name="configuration"></a>Konfigurasjon 

1. Hvis du vil legge til kostgodtgjørelser, går du til **Oppsett** > **Beregninger og koder** > **Steder for kostgodtgjørelse**.
2. For hvert av stedene som er lagt til over, velger du en kostgodtgjørelse og en valuta som er gyldig mellom en bestemt start- og sluttdato, for hotell, måltider og andre utgifter. Kostgodtgjørelsessatser og valutaer konfigureres under **Oppsett** > **Beregninger og koder** > **Kostgodtgjørelser**.
3. På siden **Steder for kostgodtgjørelse** konfigurerer du kostgodtgjørelsesnivåene. Kostgodtgjørelsesnivåer gir deg mulighet til å definere prosentandelen av en daglig grense for hotell, måltid og andre utgifter. 
4. Hvis du vil angi måltidsprosentreduksjonen for frokost, lunsj eller middag, må du oppdatere feltene på siden **Parametere for utgiftshåndtering** i kategorien **Kostgodtgjørelse**. 
    
## <a name="submit-expenses-using-per-diem"></a>Sende utgifter med kostgodtgjørelse
Hvis du vil sende utgifter ved hjelp av kostgodtgjørelse, bruker du utgiftskategorien **Kostgodtgjørelse** når du oppretter en reiseregning. Angi **Kostgodtgjørelse fra dato**, **Kostgodtgjørelse til dato** og **Sted for kostgodtgjørelse**. Beløpet beregnes basert på kostgodtgjørelsessatsene for den valgte lokasjonen, og måltidsreduksjonen beregnes basert på kostgodtgjørelsesnivåene.


[!INCLUDE[footer-include](../includes/footer-banner.md)]