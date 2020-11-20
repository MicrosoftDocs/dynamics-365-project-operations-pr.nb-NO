---
title: Innstillinger for salgsmulighet – Lite
description: Dette emnet inneholder informasjon om prosjektrelaterte avtaler og prosjektbaserte salgsmulighetslinjer.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c34817181b75b1b0079974f536e4d7b032ae87dd
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181058"
---
# <a name="opportunity-header---lite"></a>Topptekst for salgsmulighet – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Toppteksten i salgsmuligheten registrerer den generelle informasjonen om en prosjektbasert avtale som gjelder for alle linjene i den prosjektbaserte salgsmuligheten.

Prosjektrelaterte salgsmuligheter i Dynamics 365 Project Operations er utvidelser av salgsmuligheter i Dynamics 365 Sales. Disse utvidelsene tilbyr ytterligere funksjonalitet som er spesifikk for og som kreves for prosjektbaserte salgsmuligheter. Disse utvidelsene kan inneholde nye felt og båndhandlinger som er tilgjengelige i prosjektbaserte salgsmuligheter. Det kan hende at noen felt, funksjonalitet og standard logikk som er tilgjengelig i Sales, ikke er tilgjengelig i Project Operations.

Tabellen nedenfor inneholder feltene i en prosjektbasert salgsmulighet som er enten unike for Project Operations, eller som har viktige endringer i virkemåten fra salgsmulighetene i Sales.

| **Felt** | **Plassering** | **Beskrivelse** | **Nedstrøms påvirkning** |
| --- | --- | --- | --- |
| Type | Kategorien Generelt (skjult) | Dette alternativsettfeltet inneholder følgende alternativer:</br>- Arbeidsbasert (bare tilgjengelig med Project Operations)</br>- Varebasert (bare tilgjengelig når Project Operations og Sales er installert)</br>- Basert på service og vedlikehold (tilgjengelig når Field Service er installert) | Når du bruker Project Operations, settes denne feltverdien automatisk til **Arbeidsbasert**, som klassifiserer salgsmuligheten som prosjektbasert. En salgsmulighet må være prosjektbasert for å aktivere alle prosjektspesifikke utvidelser og funksjonalitet i den salgsprosessen nedstrøms for denne avtalen. |
| Kontakt | Generelt, kategori | Referanse til kundens hovedkontakt for denne avtalen. | |
| Konto | Generelt, kategori | Referanse til kundens firma- eller forretningsforbindelsesoppføring. | |
| Kontoadministrator | Generelt, kategori | Navnet på kontoadministratoren for denne prosjektbaserte salgsmuligheten. | Kontoadministratoren er ansvarlig for å administrere relasjonen med kunden gjennom fullføringen av dette prosjektet. Basert på oppføringen av den bestillbare ressursen som er knyttet til kontoadministratoren, blir kontraktenheten standard. |
| Kontraktsenhet | Generelt, kategori | Organisasjonsenheten som er ansvarlig for levering av prosjektene tilknyttet denne avtalen. | Kontraktenheten er avdelingen i firmaet som skal fullføre prosjektene etter at avtalen er lukket. Hver kontraktenhet har en valuta, og denne valutaen brukes til å rapportere beregnet og faktisk kostnad som påløpte under prosjektet. |

For alle andre felt og deler i kategorien **Sammendrag** for salgsmuligheten, se [Opprett og rediger salgsmuligheter (salg og salgssenter)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales)
