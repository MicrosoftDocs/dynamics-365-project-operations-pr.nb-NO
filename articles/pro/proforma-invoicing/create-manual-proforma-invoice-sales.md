---
title: Opprette en manuell proformafaktura – Lite
description: Dette emnet gir informasjon om hvordan du oppretter en manuell proformafaktura i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a924de6efc377e28a20e038e7deac04616b95aa
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764515"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>Opprette en manuell proformafaktura – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

I Dynamics 365 Project Operations kan proformafakturaer opprettes manuelt etter behov. Du kan manuelt opprette en proformafaktura fra listesiden **Prosjektkontrakter** eller fra detaljsiden **Prosjektkontrakt**.

##  <a name="project-contracts-list-page"></a>Listesiden Prosjektkontrakter

Fra listesiden **Prosjektkontrakter** velger du én eller flere prosjektkontrakter, og opprett deretter fakturaer for alle de valgte oppføringene.

Systemet kontrollerer hvilke av de valgte prosjektkontraktene som er har en **Klar for fakturering**-restanse datert før dagens dato. Fra disse kontraktene oppretter systemet utkast til proformafakturaer. Hvis en prosjektkontrakt har flere kunder, kan det hende at det opprettes én faktura per kunde og flere fakturaer per prosjektkontrakt.

Alle de opprettede prosjektfakturaene er tilgjengelige på **Faktura**-siden i **Fakturering**-delen i **Salg**-området.

## <a name="project-contract-details-page"></a>Detaljsiden Prosjektkontrakt

En proformafaktura kan også opprettes fra detaljsiden **Prosjektkontrakt**. Systemet verifiserer at prosjektkontrakten har en **Klar for fakturering**-restanse datert før dagens dato. Fra disse kontraktene oppretter systemet utkast til proformafakturaer basert på antall kunder på hver kontraktlinje.

Når det er opprettet én enkelt proformafaktura, åpnes **Faktura**-siden. Hvis det opprettes flere fakturaer for den prosjektkontrakten, åpnes listesiden **Fakturaer** for å vise alle opprettede fakturaer.
