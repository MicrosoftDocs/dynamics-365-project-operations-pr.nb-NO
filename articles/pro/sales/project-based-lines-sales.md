---
title: Prosjektbaserte salgsmulighetslinjer – Lite
description: Dette emnet gir informasjon om prosjektbaserte salgsmulighetslinjer. (Pro)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1978b452b84486cabd5b6b4e550261e2c8f76cd89a140709b137ac184c8967c1
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999013"
---
# <a name="project-based-opportunity-lines---lite"></a>Prosjektbaserte salgsmulighetslinjer – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Prosjektbaserte salgsmulighetslinjer er bare tilgjengelige i prosjektbaserte salgsmuligheter. Prosjektbasert salgsmulighetsoppføringer har verdien i **Type** -feltet satt til **Arbeidsbasertert**.

Prosjektbaserte salgsmulighetslinjer er linjeelementene som blir levert til kunden ved hjelp av et prosjekt. Et prosjekt kan imidlertid ikke være knyttet til en prosjektbasert salgsmulighetslinje. Prosjekter kan være knyttet til linjeelementer fra **Tilbud**-fasen og videre fordi salgsmuligheten vanligvis er en tidlig fase i livssyklusen til en avtale. Fastsettelse av hvor mange prosjekter som skal brukes til å levere arbeidet til kunden, er en avgjørelse senere i salgsfasen. Du kan bruke salgsmulighetsfasen til å identifisere de separate leveringskomponentene for kunden. Avgjørelsene rundt det faktiske antallet prosjekter som brukes til å levere disse komponentene, kan utsettes til mer informasjon er kjent med selve arbeidet.

Nedenfor vises feltene på en prosjektbasert salgsmulighetslinje:

| **Felt** | **Plassering** | **Beskrivelse** | **Nedstrøms påvirkning** |
| --- | --- | --- | --- |
| Produkttype | Kategorien Generelt (skjult) | Du kan velge ett av følgende alternativer:</br>- Prosjektbasert tjeneste (bare tilgjengelig når Dynamics 365 Project Operations er installert)</br>- Produktbasert (bare tilgjengelig når Project Operations og Dynamics 365 Sales er installert) | Verdien i dette feltet er satt til **Prosjektbasert tjeneste** når du oppretter en prosjektbasert salgsmulighetslinje fra rutenettet med prosjektbaserte linjer for salgsmuligheten. <br> Hvis du endrer eller overstyrer denne verdien, blir ikke prosjektfunksjonaliteten aktivert for de prosjektbaserte linjeelementene. |
| Salgsmulighet | Generelt, kategori | Dette feltet er skrivebeskyttet og refererer til den overordnede salgsmulighetsoppføringen som dette linjeelementet tilhører. | Dette feltet har ingen nedstrøms påvirkning. |
| Navn | Generelt, kategori | Dette redigerbare tekstfeltet kan brukes til å gi en kort identitet til linjeelementet. | Denne verdien overføres til tilbudslinjen når du oppretter et tilbud fra denne salgsmuligheten. |
| Kundebudsjett | Generelt, kategori | Det redigerbare valutafeltet kan brukes til å spore beløpet som kunden er villig til å bruke for dette linjeelementet. | Denne verdien overføres til det tilsvarende feltet på tilbudslinjen når du oppretter et tilbud fra denne salgsmuligheten. |
| Faktureringsmetode | Generelt, kategori | Dette redigerbare feltet har følgende verdier:</br>- Tid og materiale</br>- Fast pris | Denne verdien overføres til det tilsvarende feltet på tilbudslinjen når du oppretter et tilbud fra denne salgsmuligheten. Når tilbudslinjen er opprettet, er feltet låst og kan ikke endres. Tilordne denne feltverdien så nøyaktig som mulig. Hvis du må endre verdien i dette feltet på tilbudslinjen, sletter du tilbudslinjen og oppretter den på nytt. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]