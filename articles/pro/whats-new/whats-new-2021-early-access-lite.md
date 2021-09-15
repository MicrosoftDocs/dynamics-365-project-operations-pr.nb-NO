---
title: Nyheter i bølge 2 i 2021 for tidlig tilgang – Project Operations Lite-distribusjon
description: Denne emne inneholder informasjon om funksjoner som er tilgjengelige i utgivelsen for bølge 2 i 2021 for tidlig tilgang av Project Operations Lite-distribusjon.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a201e3e4333b8892eea72387222d64e18b74d71b
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323923"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>Nyheter i bølge 2 i 2021 for tidlig tilgang – Project Operations Lite-distribusjon

_Gjelder: Lite-distribusjon – avtale til proformafakturering_

Dette emnet gjelder for følgende Dynamics 365 Project Operations-komponenter og versjoner:

  - Project Operations på Dataverse-miljø versjon 4.23.0.4

Utgivelsen brukes bare når et miljø [er valgt i tidlig tilgang](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates).

## <a name="features-included-in-this-release"></a>Funksjoner som er inkludert i denne versjonen

[Administrasjon av underkontrakt](../subcontracting/subcontracting_EA_scope.md) – Denne funksjonen gir bedre synlighet og kontroll over alle aspekter av arbeidet med et prosjekt. Forhåndsversjonen av administrasjon av underkontrakt omfatter følgende funksjoner:

  - En prosjektlederen kan opprette en underkontrakt med en leverandør. Som standard brukes prislistene som er knyttet til leverandøroppføringen, for underkontrakten. Leverandørkontoen har relasjonstypen **Leverandør** eller **Forsyner**.
  - En prosjektlederen kan angi alle innkjøpene som linjeelementer på underkontrakten. Underkontraktlinjer kan være for klokkeslett, utgifter eller produkter. Transaksjonsklassen for underkontraktlinjen avgjør hva linjen gjelder.
  - Kontolederen for leverandøren og prosjektlederen kan gå over underkontrakten. Priser kan justeres i kjøpsprislister som er tilknyttet underkontrakten.
  - I løpet av prosessen hvis underkontraktlinjen gjelder et tidsskjema, kan leverandørkontolederen knytte kontakter til hver underkontraktlinje. Denne tilknytningen inneholder informasjon til prosjektlederen som arbeider med underkontrakten. Når en leverandørkontakt tilknyttes en underleverandørlinje, oppretter systemet automatisk en ressurs som kan reserveres fra kontakten, hvis en ressurs som kan reserveres, ikke allerede finnes.
  - Faktureringsmetoden for hver underkontraktlinje kan være fast pris eller tid og materiell. For underkontraktlinjer med fast pris angis en milepælbasert fakturaplan.
