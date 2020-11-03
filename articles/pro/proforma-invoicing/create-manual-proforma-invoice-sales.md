---
title: Opprette en manuell proformafaktura
description: Dette emnet gir informasjon om hvordan du oppretter en manuell proformafaktura i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5e93206737507bf6698a9746815c790d3dfc904
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/20/2020
ms.locfileid: "4081849"
---
# <a name="creating-a-manual-proforma-invoice"></a>Opprette en manuell proformafaktura

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

I Dynamics 365 Project Operations kan proformafakturaer opprettes manuelt etter behov. Du kan manuelt opprette en proformafaktura fra listesiden **Prosjektkontrakter** eller fra detaljsiden **Prosjektkontrakt**.

##  <a name="project-contracts-list-page"></a>Listesiden Prosjektkontrakter

Fra listesiden **Prosjektkontrakter** velger du én eller flere prosjektkontrakter, og opprett deretter fakturaer for alle de valgte oppføringene.

Systemet kontrollerer hvilke av de valgte prosjektkontraktene som er har en **Klar for fakturering** -restanse datert før dagens dato. Fra disse kontraktene oppretter systemet utkast til proformafakturaer. Hvis en prosjektkontrakt har flere kunder, kan det hende at det opprettes én faktura per kunde og flere fakturaer per prosjektkontrakt.

Alle de opprettede prosjektfakturaene er tilgjengelige på **Faktura** -siden i **Fakturering** -delen i **Salg** -området.

## <a name="project-contract-details-page"></a>Detaljsiden Prosjektkontrakt

En proforafaktura kan også opprettes fra detaljsiden **Prosjektkontrakt** , som oppretter fakturaen for den bestemte prosjektkontrakten. Systemet verifiserer at prosjektkontrakten har en **Klar for fakturering** -restanse som er datert før dagens dato. Fra disse kontraktene oppretter systemet utkast til proformafakturaer basert på antall kunder på hver kontraktlinje.

Når det er opprettet én enkelt proformafaktura, åpnes **Faktura** -siden. Hvis det finnes flere fakturaer som er opprettet for den aktuelle prosjektkontrakten åpnes listesiden **Fakturaer** for å vise alle fakturaene som er opprettet.
