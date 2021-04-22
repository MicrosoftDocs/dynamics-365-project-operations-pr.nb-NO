---
title: Hode/sammendrag for salgsmulighet
description: Dette emnet gir informasjon om prosjektrelaterte avtaler og de prosjektrelaterte salgsmulighetslinjene.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ab8016014c0af60d1c0dfd37fdd457f279fb8059
ms.sourcegitcommit: df30839484ef278675c5c712af0f7ba66ed9cdd3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/17/2021
ms.locfileid: "5664101"
---
# <a name="header-details-for-project-based-opportunities"></a>Overskriftsdetaljer for prosjektbaserte salgsmuligheter

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_


Toppteksten i salgsmuligheten, eller sammendraget, registrerer den generelle informasjonen om en prosjektbasert avtale som gjelder for alle linjene i en prosjektbasert salgsmulighet.

Prosjektbaserte salgsmuligheter i Dynamics 365 Project Operations er utvidelser av salgsmuligheter i Dynamics 365 Sales. Disse utvidelsene tilbyr ytterligere funksjonalitet som er spesifikk for og som kreves for prosjektbaserte salgsmuligheter. Disse utvidelsene kan inneholde nye felt og båndhandlinger som er tilgjengelige i prosjektbaserte salgsmuligheter. Det kan hende at noen felt, funksjonalitet og standard logikk som er tilgjengelig i Sales, ikke er tilgjengelig i Project Operations.

Tabellen nedenfor inneholder feltene i en prosjektbasert salgsmulighet som er enten unike for Project Operations, eller som har viktige endringer i virkemåten fra salgsmulighetene i Sales.

| **Felt** | **Plassering** | **Beskrivelse** | **Nedstrøms påvirkning** |
| --- | --- | --- | --- |
| Type | Kategorien Generelt (skjult) | Dette alternativsettfeltet inneholder følgende alternativer:</br>- Arbeidsbasert (bare tilgjengelig med Project Operations)</br>- Varebasert (bare tilgjengelig når Project Operations og Sales er installert)</br>- Basert på service og vedlikehold (tilgjengelig når Field Service er installert) | Når du bruker Project Operations, settes denne feltverdien automatisk til **Arbeidsbasert**, som klassifiserer salgsmuligheten som prosjektbasert. En salgsmulighet må være prosjektbasert for å aktivere alle prosjektspesifikke utvidelser og funksjonalitet i den salgsprosessen nedstrøms for denne avtalen. |
| Eiende firma | Generelt, kategori | Dette er firmaet eller den juridiske enheten som skal levere prosjektet for kunden. | Denne feltinformasjonen kopieres til det tilsvarende feltet i prosjekttilbudet, som opprettes fra denne salgsmuligheten. |
| Kontakt | Generelt, kategori | Referanse til kundens hovedkontakt for denne avtalen. | |
| Konto | Generelt, kategori | Referanse til kundens firma- eller forretningsforbindelsesoppføring. | |
| Kontoadministrator | Generelt, kategori | Navnet på kontoadministratoren for denne prosjektbaserte salgsmuligheten. | Kontoadministratoren er ansvarlig for å administrere relasjonen med kunden gjennom fullføringen av dette prosjektet. Basert på oppføringen av den bestillbare ressursen som er knyttet til kontoadministratoren, blir kontraktenheten standard. |
| Kontraktsenhet | Generelt, kategori | Organisasjonsenheten som er ansvarlig for levering av prosjektene tilknyttet denne avtalen. | Kontraktenheten er avdelingen i firmaet som skal fullføre prosjektene etter at avtalen er lukket. Hver kontraktenhet har en valuta, og denne valutaen brukes til å rapportere beregnet og faktisk kostnad som påløpte under prosjektet. |

For alle andre felt og deler i kategorien **Sammendrag** for salgsmuligheten, se [Opprett og rediger salgsmuligheter (salg og salgssenter)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
