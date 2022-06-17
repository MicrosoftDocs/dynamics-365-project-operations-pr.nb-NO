---
title: Nyheter i bølge 2 i 2021 for tidlig tilgang – Project Operations Lite-distribusjon
description: Denne artikkelen inneholder informasjon om funksjonene som er tilgjengelige i utgivelsen av Project Operations Lite-distribusjon i bølge 2 i 2021 for tidlig tilgang.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d245868c8bd9ff332707a81c074d6c7ae3649378
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924120"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>Nyheter i bølge 2 i 2021 for tidlig tilgang – Project Operations Lite-distribusjon

_Gjelder: Lite-distribusjon – avtale til proformafakturering_

Denne artikkelen gjelder følgende komponenter og versjoner av Dynamics 365 Project Operations:

  - Project Operations på Dataverse-miljø versjon 4.23.0.4

Utgivelsen brukes bare når et miljø [er valgt i tidlig tilgang](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates).

## <a name="features-included-in-this-release"></a>Funksjoner som er inkludert i denne versjonen

[Administrasjon av underkontrakt](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview) – Denne funksjonen gir bedre synlighet og kontroll over alle aspekter av arbeidet med et prosjekt. Forhåndsversjonen av administrasjon av underkontrakt omfatter følgende funksjoner:

  - En prosjektlederen kan opprette en underkontrakt med en leverandør. Som standard brukes prislistene som er knyttet til leverandøroppføringen, for underkontrakten. Leverandørkontoen har relasjonstypen **Leverandør** eller **Forsyner**.
  - En prosjektlederen kan angi alle innkjøpene som linjeelementer på underkontrakten. Underkontraktlinjer kan være for klokkeslett, utgifter eller produkter. Transaksjonsklassen for underkontraktlinjen avgjør hva linjen gjelder.
  - Kontolederen for leverandøren og prosjektlederen kan gå over underkontrakten. Priser kan justeres i kjøpsprislister som er tilknyttet underkontrakten.
  - I løpet av prosessen hvis underkontraktlinjen gjelder et tidsskjema, kan leverandørkontolederen knytte kontakter til hver underkontraktlinje. Denne tilknytningen inneholder informasjon til prosjektlederen som arbeider med underkontrakten. Når en leverandørkontakt tilknyttes en underleverandørlinje, oppretter systemet automatisk en ressurs som kan reserveres fra kontakten, hvis en ressurs som kan reserveres, ikke allerede finnes.
  - Faktureringsmetoden for hver underkontraktlinje kan være fast pris eller tid og materiell. For underkontraktlinjer med fast pris angis en milepælbasert fakturaplan.
