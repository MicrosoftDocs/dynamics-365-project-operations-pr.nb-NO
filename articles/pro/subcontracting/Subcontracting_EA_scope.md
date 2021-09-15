---
title: Underkontrakter i utgivelsen for tidlig tilgang for oktober 2021
description: Dette emnet gir en oversikt over funksjonene for underkontrakt i Project Operations som er en del av utgivelsen for tidlig tilgang i oktober 2021.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 21ec8355487b5e69fc5b68b11dca029e6dc04f3c
ms.sourcegitcommit: c7f891adb5c81654c01d00c6b39beed403058eb1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/14/2021
ms.locfileid: "7383707"
---
# <a name="subcontracting-in-october-2021-early-access-release"></a>Underkontrakter i utgivelsen for tidlig tilgang for oktober 2021

[!include [banner](../../includes/dataverse-preview.md)]

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Dette emnet gir en oversikt over funksjonene for underkontrakt i Dynamics 365 Project Operations som er en del av utgivelsen for tidlig tilgang i oktober 2021. Dette funksjonssettet er ikke klart for produksjons- eller direktemiljøer, så disse funksjonene forblir i utgivelsen tidlig tilgang før det fullstendige funksjonssettet blir utgitt. Vi anbefaler på det sterkeste at du ikke bruker underkontraktsfunksjonssettet for direkte produksjonsscenarioer før forhåndsversjonsbanneret er fjernet. 

Følgende liste gir en oversikt over hva som er tilgjengelig i utgivelsen for tidlig tilgang for oktober 2021:

1. Prosjektlederen oppretter en underkontrakt med en leverandør. Som standard brukes prislistene som er knyttet til leverandøroppføringen, for underkontrakten. Leverandørkontoen har relasjonstypen **Leverandør** eller **Forsyner**.

2. Prosjektlederen kan angi alle innkjøpene som linjeelementer på underkontrakten. Underkontraktlinjer kan være for klokkeslett, utgifter eller produkter. Transaksjonsklassen for underkontraktlinjen avgjør hva linjen gjelder.

3. Kontolederen for leverandøren og prosjektlederen kan gå over underkontrakten. Priser kan justeres i kjøpsprislister som er tilknyttet underkontrakten.

4. Hvis underkontraktlinjen gjelder et tidsskjema, knytter leverandørkontolederen leverandørkontakter til hver underkontraktlinje. Denne tilknytningen inneholder informasjon til prosjektlederen som arbeider med underkontrakten. Når en leverandørkontakt tilknyttes en underleverandørlinje, oppretter systemet automatisk en ressurs som kan reserveres fra kontakten, hvis en ressurs som kan reserveres, ikke allerede finnes.

5. Faktureringsmetoden for hver underkontraktlinje kan være **Fast pris** eller **Tid og materiell**. For underkontraktlinjer med fast pris angis en milepælbasert fakturaplan.

De resterende trinnene i forretningsprosessflyt for underkontrakt som er beskrevet i oversikten, er for øyeblikket ikke tilgjengelige. Etter hvert som nye funksjoner legges til, blir dette emnet oppdatert. 

Illustrasjonen nedenfor viser utgivelsen for tidlig tilgang for underkontrakter sammenlignet med hele forretningsprosessen.

![Prosessflyt for underkontrakt](../media/SubcontractingEAFlow.png)  


## <a name="quantity-based-and-work-based-subcontract-lines-early-access-release"></a>Antallsbaserte og arbeidsbaserte underkontraktlinjer med tidlig tilgang
I utgivelsen for tidlig tilgang for oktober 2021 støttes bare antallsbaserte underkontraktlinjer. Dette betyr at en underkontraktlinje kan brukes til å kjøpe tid, utgifter eller materiell fra en leverandør, men ikke et helt arbeid. Dette betyr også at antallet som kjøpes (tidsenheter, utgifter eller antall materiale) på en underkontraktlinje kan brukes på et hvilket som helst prosjekt i systemet.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
