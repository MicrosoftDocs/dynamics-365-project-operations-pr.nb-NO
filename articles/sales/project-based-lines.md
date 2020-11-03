---
title: Prosjektbaserte salgsmulighetslinjer
description: Dette emnet gir informasjon om arbeid med prosjektbaserte salgsmulighetslinjer.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7b255d607ac8180c249a9b9831db6f8d0cd3937b
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081481"
---
# <a name="project-based-opportunity-lines"></a>Prosjektbaserte salgsmulighetslinjer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_


Prosjektbaserte salgsmulighetslinjer er bare tilgjengelige i prosjektbaserte salgsmuligheter. Prosjektbasert salgsmulighetsoppføringer har verdien i **Type** -feltet satt til **Arbeidsbasertert**.

Prosjektbaserte salgsmulighetslinjer er linjeelementene som blir levert til kunden ved hjelp av et prosjekt. Et prosjekt kan imidlertid ikke være knyttet til en prosjektbasert salgsmulighetslinje. Prosjekter kan være knyttet til linjeelementer fra **Tilbud** -fasen og videre fordi salgsmuligheten er en tidlig fase i livssyklusen til en avtale. Fastsettelse av hvor mange prosjekter som skal brukes til å levere arbeidet til kunden, er en avgjørelse senere i salgsfasen. Bruk salgsmulighetsfasen til å identifisere de separate leveringskomponentene for kunden. Avgjørelsene rundt det faktiske antallet prosjekter som brukes til å levere disse komponentene, kan utsettes til mer informasjon er kjent med selve arbeidet.

Nedenfor vises feltene på en prosjektbasert salgsmulighetslinje:

| **Felt** | **Plassering** | **Relevans, formål og veiledning** | **Nedstrøms påvirkning** |
| --- | --- | --- | --- |
| Produkttype | Kategorien Generelt (skjult) | Dette er et felt med et alternativsett. Hvis du har Dynamics 365 Operations installert, er **Prosjektbasert tjeneste** et av de tilgjengelige alternativene.  | Verdien i dette feltet er satt til **Prosjektbasert tjeneste** når du oppretter en prosjektbasert salgsmulighetslinje fra rutenettet med prosjektbaserte linjer for salgsmuligheten. <br> Hvis du endrer eller overstyrer denne verdien, blir ikke prosjektfunksjonaliteten aktivert for de prosjektbaserte linjeelementene. |
| Salgsmulighet | Generelt, kategori | Dette feltet er skrivebeskyttet og refererer til den overordnede salgsmulighetsoppføringen som dette linjeelementet tilhører. | Dette feltet har ingen nedstrøms påvirkning. |
| Navn | Generelt, kategori | Dette er det redigerbar tekstfelt som kan brukes til å gi en kort identitet til dette linjeelementet. | Denne verdien overføres til tilbudslinjen når du oppretter et tilbud fra denne salgsmuligheten |
| Kundebudsjett | Generelt, kategori | Det redigerbare valutafeltet kan brukes til å spore beløpet som kunden er villig til å bruke for dette linjeelementet. | Denne verdien overføres til det tilsvarende feltet på tilbudslinjen når du oppretter et tilbud fra denne salgsmuligheten |
| Faktureringsmetode | Generelt, kategori | Dette redigerbare feltet har følgende verdier:</br>- Tid og materiale</br>- Fast pris | Denne verdien overføres til det tilsvarende feltet på tilbudslinjen når du oppretter et tilbud fra denne salgsmuligheten. Når tilbudslinjen er opprettet, er feltet låst og kan ikke endres. Tilordne denne feltverdien så nøyaktig som mulig. Hvis du må endre verdien i dette feltet på tilbudslinjen, sletter du tilbudslinjen og oppretter den på nytt. |
