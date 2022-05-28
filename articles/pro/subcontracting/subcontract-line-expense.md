---
title: Underkontraktlinjer for utgiftskategorier
description: Dette emnet forklarer hvordan du registrerer underkontraktlinjer for utgifter og bruker feltene til å registrere kjøp av tid fra leverandører.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9eba8b70aeb98389515ee679e4bfb1426736ee2c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591692"
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

| **Felt** | **Beskrivelse** | **Funksjonsinnvirkning** |
| --- | --- | --- |
| Navn | Navn på underkontraktlinjen for å hjelpe med identifisering. | Dette vises som den første kolonnen i alle oppslag basert på underkontraktlinjer. |
| Beskrivelse | En kort beskrivelse av utgiftskategoriene som blir kjøpt på underkontraktlinjen. | Ingen |
|Linjetype | Dette feltet har en standardverdi på **antallsbasert**. |Ingen |
| Faktureringsmetode | Dette er en alternativsett som representerer de to hovedkontraktsmodellene som støttes av Project Operations: **Fast pris** og **Tid og materiell**. | En milepælbasert fakturaplan gjøres tilgjengelig for underkontraktlinjer hvis faktureringsmetoden Fast pris er valgt. |
| Transaksjonsklasse | Dette feltet har en standardverdi på **tid**. Hvis du vil opprette underkontraktlinjer for innkjøp av produkter, angir du **Utgift** i **Transaksjonsklasse**-feltet.  | Dette angir at underkontraktlinjen brukes til å registrere kjøp av en utgiftskategori som skal brukes på prosjekter. |
| Transaksjonskategori | Viser en liste over aktive transaksjonskategorier i systemet. |Ingen |
| Ønsket start | Angi datoen da innkjøpskategoriene må være tilgjengelige fra leverandøren. | Ønsket start brukes til å velge en prosjektprisliste fra prosjektprislistene som er vedlagt underkontrakten. Kostnaden for kategorien på underkontraktlinjen kommer fra den prislisten. |
| Ønsket slutt | Angi datoen da innkjøpskategoriene ikke lenger var nødvendige. | Denne brukes til å vise advarsler når en prosjektleder knytter denne underkontraktlinjen til bestemte kostnadsestimater for prosjektet som kreves etter denne datoen. |
| Antall bestilt | Antall kategorier som kjøpes fra leverandøren. | Denne brukes til å vise advarsler når en prosjektleder overtrekker fra dette antallet.|
| Enhetsgruppe | Standardverdien er basert på standard enhetsgruppe som er konfigurert for den valgte kategorien. |Ingen |
| Enhet | Standardverdien er basert på standardenhet som er konfigurert for den valgte kategorien.  | Kombinasjonen av **Kategori** og **Enhet** brukes som standard eller beregnet for enhetsprisen for underkontraktlinjen.  |
| Enhetspris | Standardverdien bruker kombinasjonen av **Kategori** og **Enhet** fra kategoriprisene knyttet til prosjektprislisten, som gjelder ønsket startdato for underkontraktlinjen. |Ingen |
| Delsum | Dette er et skrivebeskyttet felt som beregnes som Antall x Enhetspris hvis det angis både antall- og enhetsprisverdier. Hvis begge feltene er tomme, kan du angi en verdi i dette feltet. |Ingen |
| Merverdiavgift | Angi mva-beløpet. |Ingen |
| Totalbeløp | Totalbeløpet for underkontraktlinjen inkludert avgifter. Dette feltet beregnes som delsum + merverdiavgift. |Ingen |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
