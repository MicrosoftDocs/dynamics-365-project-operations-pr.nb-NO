---
title: Oppgraderingshensyn for moderne godkjenninger
description: Artikkelen dekker punktene som administratorer bør vurdere når de aktiverer funksjonalitet for moderne godkjenninger.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 44a933c92d4ef8dff40f20200d74c4bbdf8caa76
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931756"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Oppgraderingshensyn for moderne godkjenninger 

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Som en del av lanseringen i bølge 1 fra april 2022 blir funksjonen for moderne godkjenninger aktivert som standard. Denne funksjonaliteten forbedrer påliteligheten til godkjenningslogikken og sikrer at du kan finne årsaken hvis godkjenningslogikken mislykkes.

Som en del av denne endringen oppdateres statusendringer for prosjektgodkjenninger. Statusen går nå direkte fra **Sendt inn** til **Godkjent**. **Ventende** er ikke lenger en status for godkjenninger. Hvis du vil finne ut om en godkjenning venter, kontrollerer du at godkjenningen er en del av et godkjenningssett, og ser gjennom tilstanden til det vedlagte godkjenningssettet.

## <a name="before-you-upgrade"></a>Før du oppgraderer

Før du oppgraderer til moderne godkjenninger, må du kontrollere at du ikke har ventende godkjenninger. Moderne godkjenninger bruker ikke statusen **Ventende**. Godkjenninger som fremdeles er merket som **Ventende** etter oppgraderingen, blir derfor ikke behandlet.

## <a name="after-you-upgrade"></a>Etter oppgraderingen

Når du har oppgradert til moderne godkjenninger, må en administrator validere at skyflyten som behandler godkjenninger, er aktivert.

1. Logg på [flow.microsoft.com](https://flow.microsoft.com)
2. Bytt miljø til miljøet du har oppgradert, øverst til høyre på siden.
3. Velg **Løsninger** for å vise løsningene som er installert i miljøet.
4. Velg **Project Operations** eller **Project Service** i løsningslisten.
5. Endre filteret fra **Alle** til **Skyflyter**.
6. Kontroller at alternativet **Project Service – Planlegg prosjektgodkjenningssett til gjentakelse** er satt til **På**. Hvis den ikke er det, velger du flyten og velger deretter **Aktiver**.
7. Kontroller at behandlingen skjer hvert 5. minutt ved å se gjennom listen **Systemjobber** i **Innstillinger**-området.

## <a name="short-term-rollback"></a>Kortsiktig tilbakerulling

Hvis du ikke kan utføre endringene, eller hvis du opplever alvorlige problemer med denne funksjonen, kan du midlertidig gå tilbake til den opprinnelige godkjenningsflyten ved å utføre følgende trinn:
1. Logg på miljøet, og kontroller at det ikke finnes ventende godkjenninger.
2. Gå til **Innstillinger** > **Prosjektparametere**.
3. Velg **Funksjonskontroll**, og velg deretter **Moderne godkjenninger** for å deaktivere funksjonen.

## <a name="removing-the-feature-flag"></a>Fjerning av funksjonsflagget

I oppdateringen i bølge 2 fra oktober 2022 blir muligheten til å slå av denne funksjonen fjernet.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
