---
title: Oversikt over ressursutnyttelse
description: Dette emnet gir informasjon om ressursutnyttelse i Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a683931bcd6a357c5feec9198b190b948ad17a40
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000808"
---
# <a name="resource-utilization-overview"></a>Oversikt over ressursutnyttelse

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Ressurser kan ha fakturerbar utnyttelse som mål. Denne målutnyttelsen er definert som et attributt i standardrollen til en ressurs eller angitt i oppføringen for en enkelt bestillbar ressurs. Utnyttelsesberegninger er basert på de faktiske timene ressursene har rapportert ved hjelp av godkjente tidsoppføringer.

Følgende formler brukes til å beregne utnyttelse:

  - Fakturerbar utnyttelse = belastbare faktiske timer ÷ ressurskapasitet
  - Ikke-fakturerbar utnyttelse = faktisk tid med faktureringstype-ID = ikke-belastbar, komplementær eller ikke tilgjengelig ÷ ressurskapasitet
  - Intern = faktisk tid uten salgskontrakt ÷ ressurskapasitet
  - Ressurskapasitet = arbeidstimer for ressursen – fravær – ikke-arbeidsdager

Du kan finne visningen **Ressursutnyttelse** i **Ressurser**-ruten.

Hver celle i rutenettet representerer den fakturerbare utnyttelsesprosenten for ressursen i en periode, for eksempel en dag, uke eller måned. Følgende formler brukes til å fargelegge cellene:

  - **Grønn**: Fakturerbar utnyttelse >= Ressursmålutnyttelse
  - **Gul**: Målutnyttelse – 20 <= Fakturerbar utnyttelse < Målutnyttelse
  - **Rød**: Fakturerbar utnyttelse < Målutnyttelse – 20

Siden visningen **Ressursutnyttelse** er basert på planleggingstavlen, kan du bruke filtreringsfunksjonene på planleggingstavlen til å filtrere resultatene.

Rutenettet krever at du angir en målutnyttelse for rollen eller den individuelle ressursen. Du kan sette opp dette ved å gå til **Ressurser** > **Ressursroller**.

I tillegg må en standardrolle tilordnes til hver bestillbare ressurs. Gå til **Ressurser** > **Ressurser**. I kategorien **Project Service** kontrollerer du at det er definert en ressursrolle, og at **Er standard**-feltet er satt til **Ja**. Du kan legge til flere roller der **Er standard** = **Nei**. Rollen der **Er standard** = **Ja** brukes til å evaluere ressursens utnyttelse mot målet for den aktuelle rollen.

I kategorien **Project Service** kan du også angi en individuell målutnyttelse for ressursen. Beregningen av utnyttelsen bruker deretter denne målutnyttelsen til å evaluere ressursens mål i stedet for målet for standardrollen for ressursen.

Utnyttelse vises bare for en ressurs hvis ressursen har godkjent, belastbar tid i perioden som vises i rutenettet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]