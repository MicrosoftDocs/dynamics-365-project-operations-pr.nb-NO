---
title: Overskriftsdetaljer for leverandørfakturaer
description: Dette emnet forklarer funksjonaliteten i leverandørfakturaoverskriften i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 17be106d5486358ff0bbf011af3da26a4c85a274
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575592"
---
# <a name="header-details-for-vendor-invoices"></a>Overskriftsdetaljer for leverandørfakturaer

[!include [banner](../../includes/dataverse-preview.md)]

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Dette emnet forklarer funksjonaliteten i leverandørfakturaoverskriften i Microsoft Dynamics 365 Project Operations.

Når prosjektledere planlegger og kjører prosjekter, kan de bruke underleverandører og kjøpe produkter og servicer fra leverandører. Under utførelse av et prosjekt påløper kostnader for kategorier for service, materiell og utgifter som er innkjøpt for underleverandører med leverandører. Leverandører fakturerer disse kostnadene til prosjekter ved å opprette leverandørfakturaer.

Tabellen nedenfor inneholder informasjon om feltene i leverandørfakturahoder i Project Operations.

| Felt | Bekrivelse | Funksjonsinnvirkning |
| --- | --- | --- |
| Name | Navnet på leverandørfakturaen. | I alle rullegardinlister for leverandørfakturaer vises navnet på leverandørfakturaen i den første kolonnen for å hjelpe deg med å identifisere leverandørfakturaen. Når en leverandørfaktura opprettes fra en underleverandør, settes **Navn**-feltet i leverandørfakturaen som standard til en verdi som består av navnet på underkontrakten pluss gjeldende dato. |
| Bekrivelse | En kort beskrivelse av servicene og produktene som faktureres på leverandørfakturaen. | None |
| Forhandler | Navnet på firmaet som fakturering for produktene og servicene. Dette firmaet må være en forretningsforbindelsesoppføring som har relasjonstypen **Leverandør** eller **Tilveiebringer**. | <p>Basert på leverandøren som er valgt, angis det automatisk standardverdier i følgende felter:</p><ul><li>Valuta</li><li>Prislister</li><li>Betalingsbetingelser</li><li>Betalingsadresse</li></ul> |
| Underkontrakt | En referanse til underkontrakten for leverandørfakturaen. | <p>Basert på underkontrakten som er valgt, angis det automatisk standardverdier i følgende felter:</p><ul><li>Valuta</li><li>Prislister</li><li>Betalingsbetingelser</li><li>Betalingsadresse</li></ul><p>Underkontrakten som er valgt i leverandørfakturaoverskriften, angis som standard på leverandørfakturalinjene og kan ikke endres der.</p> |
| Fakturadato | Datoen for faktiske kostnader som opprettes når leverandørfakturaen bekreftes. | Fakturadatoen brukes også til å velge riktig innkjøpsprisliste fra prislistene som er knyttet til den relaterte leverandøren eller fra prosjektparametere. |
| Statusårsak | Statusen for leverandørfakturaen. | <p>Statusen avgjør hvor leverandørfakturaen er i forretningsprosessen, og om den kan redigeres. Her er noen av de tilgjengelige verdiene:</p><ul><li>**Utkast** – Leverandørfakturaen kan redigeres.</li><li>**Bekreftet** – Leverandørfakturaen ble kontrollert og bekreftet. Leverandørfakturaer med denne statusen kan ikke redigeres eller slettes.</li><li>**Under behandling** – Leverandørfakturaen blir gjennomgått. Leverandørfakturaer med denne statusen kan redigeres, men de kan ikke slettes.</li><li>**Annullert** – Leverandørfakturaen ble annullert. Leverandørfakturaer med denne statusen kan ikke redigeres eller slettes.</li></ul> |
| Valuta | Valutaen som leverandøren fakturerer for produktene og servicene i leverandørfakturaen. | I en leverandørfaktura som refererer til en underkontrakt, angis valutaen for underkontrakten som standard som valuta for leverandørfakturaen. I en leverandørfaktura som ikke refererer til en underleverandør, angis standardverdien fra oppføringen for leverandørkontoen og kan endres. Når du har lagret en leverandørfaktura, kan du ikke lenger redigere valutaen. |
| Kontraktsenhet | Divisjonen i selskapet som er ansvarlig for å motta tjenestene og/eller produktene fra leverandøren. | None |
| Betalingsbetingelser | Betalingsbetingelsene på leverandørfakturaer som er utstedt. Standardverdien angis automatisk fra oppføring for leverandørkontoen. | Betalingsbetingelser fra en underkontrakt kopieres til alle leverandørfakturaer som er relatert til underkontrakten. Betalingsbetingelser kan oppdateres hvis leverandørfakturaen har statusen **Utkast**. |
| Betalingsadresse | Adressen til leverandøren som betalinger må sendes til. Standardverdien angis automatisk fra oppføring for leverandørkontoen. | Betalingsadressen fra en underkontrakt kopieres som betalingsadressen til alle leverandørfakturaer som er opprettet for underkontrakten. Betalingsadressen kan oppdateres hvis leverandørfakturaen har statusen **Utkast**. |
| Delsum | Hvis leverandørfakturaen ikke har noen linjer, angir du delsummen for faktruaen før avgifter. Hvis leverandørfakturaen har linjer, er dette feltet skrivebeskyttet. I slike tilfeller er beløpet som vises, delsumbeløpet fra alle linjene på leverandørfakturaen. | None |
| Avgifter totalt | Hvis leverandørfakturaen ikke har noen linjer, angir du de totale avgiftene i underkontrakten. Hvis leverandørfakturaen har linjer, er dette feltet skrivebeskyttet. I slike tilfeller er beløpet som vises, summen av avgiftsbeløpene fra alle linjene på leverandørfakturaen. | None |
| Totalbeløp | Dette beregnede feltet viser totalbeløpet for leverandørfakturaen etter at avgifter er inkludert. | None |

> [!NOTE]
> Følgende felter på en leverandørfaktura kan ikke endres etter at leverandørfakturaen er lagret: **Leverandør**, **Underkontrakt**, **Valuta**, **Kontraktsenhet** og **Betalingsbetingelser**. Hvis det kreves endringer i disse feltene på en leverandørfaktura, må du slette leverandørfakturaen og opprette en ny leverandørfaktura.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
