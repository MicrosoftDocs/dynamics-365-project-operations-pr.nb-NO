---
title: Innstillinger for prosjekttilbud
description: Dette emnet gir informasjon om informasjonen og innstillingene som gjelder for og virker inn på prosjekttilbud.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3f11188a47c6f0c7de9fb591fd3be3e22f8f7d842fb6d075c1f43d9baea4d225
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993478"
---
# <a name="header-details-for-project-based-quotes"></a>Overskriftsdetaljer for prosjektbaserte tilbud

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_


Denne artikkelen forklarer informasjonen som gjelder for et prosjekttilbud. Dette omfatter innstillingene som påvirker alle tilbudslinjene, og informasjon om tilbudet som oppsummeres på tvers av alle linjeelementene, for å drive KPI-ene til prosjekttilbudet.

Tabellen nedenfor viser sammendragsinformasjonsfeltene i et prosjekttilbud som er unike for Dynamics 365 Project Operations, eller som har noen viktige endringer i virkemåten fra Dynamics 365 Sales-tilbud.

| **Felt** | **Plassering** | **Beskrivelse** | **Nedstrøms påvirkning** |
| --- | --- | --- | --- |
| Type | Kategorien Sammendrag (skjult) | Dette alternativsettfeltet inneholder følgende alternativer:</br>- Arbeidsbasert (bare tilgjengelig når Project Operations er installert)</br>- Varebasert (bare tilgjengelig når Project Operations og Sales er installert)</br>- Basert på service og vedlikehold (tilgjengelig når Dynamics 365 Field Service er installert) | Når du bruker Project Operations, settes verdien for dette feltet automatisk til **Arbeidsbasert**. Dette klassifiserer tilbudet som et prosjektbasert tilbud. Et tilbud må være prosjektbasert for å aktivere alle prosjektspesifikke utvidelser og funksjoner. |
| Eiende firma | Sammendrag | Den juridiske enheten som skal stå for kostnadene og inntektene som påløper fra dette prosjektet eller prosjektene som er tilknyttet dette tilbudet. Når et tilbud er opprettet fra en salgsmulighet, kopieres dette feltet fra det tilsvarende feltet for salgsmuligheten. | Det eiende firmaet tilsvarer konseptet juridisk enhet i modulen **Prosjektstyring og regnskap** i Project Operations. Alle kostnader og inntekter som påløper fra dette prosjektet, blir regnskapsført i hovedboken til det eiende firmaet. |
| Potensiell kunde | Sammendrag-kategori | Referanse til kundens firma- eller forretningsforbindelsesoppføring. En gyldig kunde som skal refereres i prosjekttilbudet, må være definert som en kunde i det eiende firmaet i tilbudet. Det eiende firmaet viser listen over juridiske enheter, og disse er satt opp i modulen **Prosjektstyring og regnskap** i Project Operations. Når et tilbud er opprettet fra en salgsmulighet, kopieres dette feltet fra det tilsvarende feltet for salgsmuligheten. | Valutaen i prosjekttilbudet blir som standard basert på valutaen til kunden. Dette kan imidlertid ikke endres før tilbudet er lagret. |
| Kontoadministrator | Sammendrag-kategori | Navnet på kontoadministratoren for denne avtalen. Når et tilbud er opprettet fra en salgsmulighet, kopieres dette feltet fra det tilsvarende feltet for salgsmuligheten. | Kontoadministratoren er ansvarlig for å administrere relasjonen med kunden gjennom fullføringen av dette prosjektet. Basert på oppføringen av den bestillbare ressursen som er knyttet til kontoadministratoren, blir kontraktenheten som standard i prosjekttilbudet.|
| Kontraktsenhet | Sammendrag-kategori | Organisasjonsenheten som er ansvarlig for levering av prosjektene tilknyttet dette tilbudet. Når et tilbud er opprettet fra en salgsmulighet, kopieres dette feltet fra det tilsvarende feltet for salgsmuligheten. | Kontraktenheten er avdelingen i firmaet som skal kjøre prosjektene etter at avtalen er lukket. Hver kontraktenhet har en valuta, og denne valutaen brukes til å rapportere beregnet og faktisk kostnad som påløpte under kjøringen av prosjektet. |
| Produktprisliste | Sammendrag-kategori | Dette er prislisten som brukes til standardpriser på de produktbaserte tilbudslinjene. Listen over alternativer for dette feltet viser en liste over prislister der prislistevalutaen samsvarer med valutaen i tilbudet. Når et tilbud er opprettet fra en salgsmulighet, kopieres dette feltet fra det tilsvarende feltet for salgsmuligheten. Dette feltet på salgsmuligheten hentes som standard fra kontooppføringen, men kan endres. | Når et tilbud er vunnet, kopieres feltverdien til prosjektkontrakten som opprettes. |
| Valuta | Sammendrag-kategori | Dette angir valutaen som skal brukes ved rapportering av verdien for denne avtalen. Dette er også valutaen som kunden blir fakturert i, hvis avtalen er vunnet. Når et tilbud er opprettet fra en salgsmulighet, kopieres dette feltet fra det tilsvarende feltet for salgsmuligheten. Dette feltet på salgsmuligheten hentes som standard fra kontooppføringen, men kan endres av brukeren.  | Når et tilbud er lagret, kan ikke dette feltet lenger redigeres. Dette brukes til å standardisere produktet og prosjektprislistene i tilbudet. Valutaen i tilbudet brukes til å samsvare valutaen i prislisten. |
| Må ikke overskrides-grense | Sammendrag-kategori | Dette angir det forhandlede taket for den endelige verdien som kunden godtar for denne avtalen. | Dette taket evalueres under kjøring og gjelder på tvers av alle linjeelementer og prosjekter som er tilknyttet denne avtalen. |
| Ønsket leveringsdato | Sammendrag-kategori | Når et tilbud er opprettet fra en salgsmulighet, kopieres dette feltet fra det tilsvarende feltet for salgsmuligheten. | Denne datoen brukes som sluttdato for generering av fakturaplaner. |

Nedenfor finner du kategoriene og KPI-ene som er tilgjengelige for et prosjekttilbud som er unikt for Project Operations, eller som har noen viktige endringer i virkemåten fra tilbud:

| **Felt** | **Plassering** | **Beskrivelse** |
| --- | --- | --- |
| Lønnsomhetsanalyse | Fane i tilbudet | Fanen viser følgende måledata:</br>- Total belastbar kostnad</br></br>- Total ikke-belastbar kostnad</br>- Total omsetning</br>- Total omsetning (standardvaluta)</br>- Bruttofortjeneste</br>- Justert bruttofortjeneste|
| Sammenligning med kundens forventninger | Fane i tilbudet | Denne fanen viser følgende måledata:</br>- Beregnet fullføring</br>- Ønsket fullføring</br>- Kundebudsjett</br>- Tilbudsverdi |
| Tilbudsanalyse | Fane i tilbudet | Denne kategorien oppsummerer følgende topo KPI-er for et prosjekttilbud</br>- Sammenligning med kundens forventninger for budsjett og tidsplan</br>- Bruttofortjeneste</br>- Justert bruttofortjeneste |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
