---
title: Prosjektbaserte salgsmulighetslinjer (Pro)
description: Dette emnet gir informasjon om prosjektbaserte salgsmulighetslinjer. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a688b9bed5a38e7b5947cbcee1e3cb8ab211e98
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896383"
---
# <a name="project-based-opportunity-lines-pro"></a>Prosjektbaserte salgsmulighetslinjer (Pro)

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Prosjektbaserte salgsmulighetslinjer er bare tilgjengelige i prosjektbaserte salgsmuligheter. Prosjektbasert salgsmulighetsoppføringer har verdien i **Type** -feltet satt til **Arbeidsbasertert**.

Prosjektbaserte salgsmulighetslinjer er linjeelementene som blir levert til kunden ved hjelp av et prosjekt. Et prosjekt kan imidlertid ikke være knyttet til en prosjektbasert salgsmulighetslinje. Prosjekter kan være knyttet til linjeelementer fra **Tilbud**-fasen og videre fordi salgsmuligheten vanligvis er en tidlig fase i livssyklusen til en avtale. Fastsettelse av hvor mange prosjekter som skal brukes til å levere arbeidet til kunden, er en avgjørelse senere i salgsfasen. Du kan bruke salgsmulighetsfasen til å identifisere de separate leveringskomponentene for kunden. Avgjørelsene rundt det faktiske antallet prosjekter som brukes til å levere disse komponentene, kan utsettes til mer informasjon er kjent med selve arbeidet.

Nedenfor vises feltene på en prosjektbasert salgsmulighetslinje:

| **Felt** | **Plassering** | **Relevans, formål og veiledning** | **Nedstrøms påvirkning** |
| --- | --- | --- | --- |
| Produkttype | Kategorien Generelt (skjult) | Du kan velge ett av følgende alternativer:</br>- Prosjektbasert tjeneste (bare tilgjengelig når Dynamics 365 Project Operations er installert)</br>- Produktbasert (bare tilgjengelig når Project Operations og Dynamics 365 Sales er installert) | Verdien i dette feltet er satt til **Prosjektbasert tjeneste** når du oppretter en prosjektbasert salgsmulighetslinje fra rutenettet med prosjektbaserte linjer for salgsmuligheten. <br> Hvis du endrer eller overstyrer denne verdien, blir ikke prosjektfunksjonaliteten aktivert for de prosjektbaserte linjeelementene. |
| Salgsmulighet | Generelt, kategori | Dette feltet er skrivebeskyttet og refererer til den overordnede salgsmulighetsoppføringen som dette linjeelementet tilhører. | Dette feltet har ingen nedstrøms påvirkning. |
| Navn | Generelt, kategori | Dette redigerbare tekstfeltet kan brukes til å gi en kort identitet til linjeelementet. | Denne verdien overføres til tilbudslinjen når du oppretter et tilbud fra denne salgsmuligheten. |
| Kundebudsjett | Generelt, kategori | Det redigerbare valutafeltet kan brukes til å spore beløpet som kunden er villig til å bruke for dette linjeelementet. | Denne verdien overføres til det tilsvarende feltet på tilbudslinjen når du oppretter et tilbud fra denne salgsmuligheten. |
| Faktureringsmetode | Generelt, kategori | Dette redigerbare feltet har følgende verdier:</br>- Tid og materiale</br>- Fast pris | Denne verdien overføres til det tilsvarende feltet på tilbudslinjen når du oppretter et tilbud fra denne salgsmuligheten. Når tilbudslinjen er opprettet, er feltet låst og kan ikke endres. Tilordne denne feltverdien så nøyaktig som mulig. Hvis du må endre verdien i dette feltet på tilbudslinjen, sletter du tilbudslinjen og oppretter den på nytt. |
