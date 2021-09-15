---
title: Underkontraktlinjer for utgiftskategorier
description: Dette emnet forklarer hvordan du registrerer underkontraktlinjer for utgifter og bruker feltene til å registrere kjøp av tid fra leverandører.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9e8e7bb66063dab6db1ac8da1753913aee0ef3fc
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323833"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Underkontraktlinjer for utgiftskategorier

[!include [banner](../../includes/dataverse-preview.md)]

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

En underkontrakt i Dynamics 365 Project Operations kan ha en linje for utgiftskategorier. Underkontraktlinjer for utgiftskategorier gjør det mulig for en prosjektleder å kjøpe kategorier av tjenester eller produkter fra leverandører som de kan belaste til et prosjekt.

Hvis du vil opprette en underkontraktlinje for utgiftskategorier i Project Operations, følger du fremgangsmåten nedenfor.

1. Velg **Underkontrakter** i navigasjonsruten, og åpne underkontrakten du vil arbeide med.
2. Velg **Ny** i fanen **Underkontraktlinjer** for å opprette en ny linje.
3. Velg **Utgift** i **Transaksjonsklasse**-feltet på **Hurtigoppretting**-siden, og angi eller velg eventuell annen nødvendig feltinformasjon.

Tabellen nedenfor inneholder informasjon om feltene på detaljsiden **Underkontraktlinje** og **Hurtigoppretting**.

| **Felt** |  **Beskrivelse** |
| ----------| ---------------- |
| Navn | Navnet på underkontraktlinjen. |
| Beskrivelse | En kort beskrivelse av tjenester eller produktkategorier som blir kjøpt på underkontraktlinjen. |
| Linjetype | Dette feltet har en standardverdi på **antallsbasert**.  |
| Faktureringsmetode | Faktureringsmetoden for underkontraktlinjen. Basert på faktureringsmetoden til linjen, gjøres en milepælbasert fakturaplan tilgjengelig for faktureringsmetoden med fast pris.  |
| Transaksjonsklasse | Dette feltet har en standardverdi på **tid**. Hvis du vil opprette underkontraktlinjer for innkjøp av produkter, angir du **Utgift** i **Transaksjonsklasse**-feltet. Denne feltverdien angir at underkontraktlinjen blir brukt til å registrere et kjøp av en kategori av produkter eller tjenester som skal brukes på prosjekter. |
| Transaksjonskategori | Velg transaksjonskategorien. |
| Ønsket start | Datoen da innkjøpskategoriene må være tilgjengelige fra leverandøren. Ønsket start brukes også til å velge en prosjektprisliste fra prosjektprislistene som er vedlagt underkontrakten. Kostnaden for kategorien på underkontraktlinjen brukes som standard fra den prislisten. |
| Ønsket slutt | Datoen da innkjøpskategoriene ikke lenger er nødvendige. Denne datoen kaller opp en advarsel når en prosjektleder knytter denne underkontraktlinjen til bestemte kostnadsestimater for prosjektene som er datert etter denne datoen. |
| Antall bestilt | Antall av kategorien som kjøpes fra leverandøren. Når en prosjektleder overtrekker fra kjøpsantallet, vises det en advarsel.  |
| Enhetsgruppe | Standardverdien for feltet er basert på standard enhetsgruppe som er angitt for den valgte kategorien. |
| Enhet | Standardverdien for feltet er basert på standardenhet som er angitt for den valgte kategorien. Kombinasjonen av kategori og enhet brukes til standard enhetspris for underkontraktlinjen. |
| Enhetspris | Standardverdien for enhetsprisen fra kombinasjonen av kategorien og enheten fra kategoriprisene knyttet til prosjektprislisten som gjelder for ønsket start for underkontraktlinjen.  |
| Delsum | Dette er et skrivebeskyttet felt som automatisk beregnes som antallsenhetspris hvis både antalls- og enhetsprisverdiene angis. Hvis et eller begge feltene er tomme, kan du angi en verdi i dette feltet manuelt.  |
| Merverdiavgift | Angi mva-beløpet.  |
| Totalbeløp | Totalbeløpet for underkontraktlinjen inkludert avgifter. Dette feltet beregnes som delsum + merverdiavgift.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
