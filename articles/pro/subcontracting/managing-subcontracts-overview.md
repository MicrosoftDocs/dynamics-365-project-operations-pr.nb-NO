---
title: Administrasjon av underkontrakt i Project Operations
description: Dette emnet gir en oversikt over ende-til-ende-behandlingsprosessen for underkontrakter i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ffceb0886fdc841ea01a099243cf4eeb43e5374a18414576f3639a3e50857fd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994243"
---
# <a name="subcontract-management-in-project-operations"></a>Administrasjon av underkontrakt i Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Underkontrakt i Microsoft Dynamics 365 Project Operations støtter følgende forretningsprosessflyt.

![Prosessflyt for underkontrakt](../media/SubcontractingProcessFlow.png)

Her er en trinnvis beskrivelse av underkontraktprosessen.

1. Prosjektlederen oppretter en underkontrakt med en leverandør. Som standard brukes prislistene som er knyttet til leverandøroppføringen, for underkontrakten. Leverandørkontoen har relasjonstypen **Leverandør** eller **Forsyner**.
2. Prosjektlederen kan angi alle innkjøpene som linjeelementer på underkontrakten. Underkontraktlinjer kan være for klokkeslett, utgifter eller produkter. Transaksjonsklassen som velges på hver underkontraktlinje, avgjør hva linjen gjelder for.
3. Kontolederen for leverandøren og prosjektlederen kan gå over underkontrakten. Priser kan justeres i kjøpsprislister som er tilknyttet underkontrakten.
4. Hvis underkontraktlinjen gjelder et tidsskjema, knytter leverandørkontolederen kontakter til hver underkontraktlinje. Denne tilknytningen inneholder informasjon til prosjektlederen som arbeider med underkontrakten. Når en kontakt tilknyttes en underleverandørlinje, oppretter systemet automatisk en ressurs som kan reserveres fra kontakten, hvis en ressurs som kan reserveres, ikke allerede finnes.
5. Faktureringsmetoden for hver underkontraktlinje kan være **Fast pris** eller **Tid og materiell**. For underkontraktlinjer med fast pris kan du angi en milepælbasert fakturaplan.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
