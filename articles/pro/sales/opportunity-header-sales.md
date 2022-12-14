---
title: Overskriftsdetaljer for prosjektsalgsmuligheter
description: Denne artikkelen inneholder informasjon om prosjektbaserte avtaler og prosjektbaserte salgsmulighetslinjer.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ec332e2fb97436d7ec3d31b75ee2383edcb5c7e4
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824592"
---
# <a name="header-details-for-project-opportunities"></a>Overskriftsdetaljer for prosjektsalgsmuligheter

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Toppteksten i salgsmuligheten registrerer den generelle informasjonen om en prosjektbasert avtale som gjelder for alle linjene i den prosjektbaserte salgsmuligheten.

Prosjektbaserte salgsmuligheter i Dynamics 365 Project Operations er utvidelser av salgsmuligheter i Dynamics 365 Sales. Disse utvidelsene tilbyr ytterligere funksjonalitet som er spesifikk for og som kreves for prosjektbaserte salgsmuligheter. Disse utvidelsene kan inneholde nye felt og båndhandlinger som er tilgjengelige i prosjektbaserte salgsmuligheter. Det kan hende at noen felt, funksjonalitet og standard logikk som er tilgjengelig i Sales, ikke er tilgjengelig i Project Operations.

Tabellen nedenfor inneholder feltene i en prosjektbasert salgsmulighet som er enten unike for Project Operations, eller som har viktige endringer i virkemåten fra salgsmulighetene i Sales.

| **Felt** | **Plassering** | **Beskrivelse** | **Nedstrøms påvirkning** |
| --- | --- | --- | --- |
| Type | Kategorien Generelt (skjult) | Dette alternativsettfeltet inneholder følgende alternativer:</br>- Arbeidsbasert (bare tilgjengelig med Project Operations)</br>- Varebasert (bare tilgjengelig når Project Operations og Sales er installert)</br>- Basert på service og vedlikehold (tilgjengelig når Field Service er installert) | Når du bruker Project Operations, settes denne feltverdien automatisk til **Arbeidsbasert**, som klassifiserer salgsmuligheten som prosjektbasert. En salgsmulighet må være prosjektbasert for å aktivere alle prosjektspesifikke utvidelser og funksjonalitet i den salgsprosessen nedstrøms for denne avtalen. |
| Kontakt | Generelt, kategori | Referanse til kundens hovedkontakt for denne avtalen. | |
| Konto | Generelt, kategori | Referanse til kundens firma- eller forretningsforbindelsesoppføring. | |
| Kontoadministrator | Generelt, kategori | Navnet på kontoadministratoren for denne prosjektbaserte salgsmuligheten. | Kontoadministratoren er ansvarlig for å administrere relasjonen med kunden gjennom fullføringen av dette prosjektet. Basert på oppføringen av den bestillbare ressursen som er knyttet til kontoadministratoren, blir kontraktenheten standard. |
| Kontraktsenhet | Generelt, kategori | Organisasjonsenheten som er ansvarlig for levering av prosjektene tilknyttet denne avtalen. | Kontraktenheten er avdelingen i firmaet som skal fullføre prosjektene etter at avtalen er lukket. Hver kontraktenhet har en valuta, og denne valutaen brukes til å rapportere beregnet og faktisk kostnad som påløpte under prosjektet. |

For alle andre felt og deler i kategorien **Sammendrag** for salgsmuligheten, se [Opprett og rediger salgsmuligheter (salg og salgssenter)](/dynamics365/sales-enterprise/create-edit-opportunity-sales)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
