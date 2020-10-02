---
title: Prosjektprislister
description: Denne emnet gir informasjon om Project-prislisteenheten.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d09a0dd8234641ca106c37a38d1d721dfb07236c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898678"
---
# <a name="project-price-lists"></a>Prosjektprislister

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Dynamics 365 Project Operations utvider prislisteenheten i Dynamics 365 Sales. 

## <a name="key-entities"></a>Viktige enheter

En prisliste inneholder informasjon fra fire ulike enheter:

- **Prisliste**: Denne enheten lagrer informasjon om kontekst, valuta, datogyldighet og tidsenhet for prisingstiden. Konteksten viser om prislisten uttrykker kostnadssatser eller salgssatser. 
- **Valuta**: Denne enheten lagrer valutakursen i prislisten. 
- **Dato**: Denne enheten brukes når systemet prøver å angi en standardpris for en transaksjon. Det velges en prislisten som har datogyldighet som inkluderer datoen for transaksjonen. Hvis mer enn én prisliste blir funnet som er gyldig for transaksjonsdatoen og er knyttet til beslektet tilbud, kontrakt eller organisasjonsenhet, blir ingen pris angitt som standard. 
- **Tid**: Denne entiteten lagrer tidsenheten som prisene er uttrykt for, for eksempel daglige eller timebaserte priser. 

Prislisteenheten har tre relaterte tabeller som lagrer priser:

  - **Rollepris**: Denne tabellen lagrer en sats for en kombinasjon av verdier for rolle og organisasjonsenhet, og brukes til å konfigurere rollebaserte priser for personale.
  - **Transaksjonskategoripris**: Denne tabellen lagrer priser etter transaksjonskategori og brukes til å definere utgiftskategoripriser.
  - **Prislisteelementer**: Denne tabellen inneholder priser for katalogprodukter.
 
Prislisten er et rangeringskort. Et rangeringskort er en kombinasjon av prislisteenheten og relaterte rader i tabellene Rollepris, Transaksjonskategoripris og Prislisteelementer.

## <a name="resource-roles"></a>Ressursroller

Begrepet *ressursrolle* viser til en rekke ferdigheter, kompetanser og sertifiseringer som en person må ha for å utføre et bestemt sett med oppgaver i et prosjekt.

Personaltid tilbys basert på rollen som en ressurs fyller, i et bestemt prosjekt. For personaltid er kostnader og fakturering basert på ressursrolle. Tid kan prises i alle enheter i **Tid**-enhetsgruppen.

**Tid**-enhetsgruppen opprettes når du installerer Project Operations. Den har **Time** som standardenhet. Du kan ikke slette, gi nytt navn til eller redigere attributter for **Tid**-enhetsgruppen eller **Time**-enheten. Du kan imidlertid legge til andre enheter i **Tid**-enhetsgruppen. Hvis du prøver å slette **Tid**-enhetsgruppen eller **Time**-enheten, kan det oppstå feil i forretningslogikken.
 
## <a name="transaction-categories-and-expense-categories"></a>Transaksjonskategorier og utgiftskategorier

Reiseutgifter og andre utgifter som påløper for prosjektkonsulenter, blir fakturert til kunden. Prising av utgiftskategorier fullføres ved hjelp av prislister. Flyreiser, hotell og leiebil er eksempler på utgiftskategorier. Hver prislistelinje for utgifter angir prising for en bestemt utgiftskategori. Følgende tre metoder brukes til prisutgiftskategorier:

- **Kostnad**: Utgiftskostnaden faktureres til kunden, og ingen påslag brukes.
- **Påslagsprosent**: Prosentandelen for den faktiske kostnaden som faktureres til kunden. 
- **Pris per enhet**: En faktureringspris er angitt for hver enhet i utgiftskategorien. Beløpet som blir fakturert til kunden, beregnes basert på antall utgiftsenheter som konsulenten rapporterer. Reisegodtgjørelse bruker pris per enhet. For eksempel kan utgiftskategorien for reisegodtgjørelse konfigureres for 30 USD per dag eller 2 USD per mile. Når en konsulent rapporterer reisegodtgjørelse i et prosjekt, beregnes beløpet til fakturering basert på antall kilometer som er rapportert av konsulenten.
 
## <a name="project-sales-pricing-and-overrides"></a>Prising og overstyringer av prosjektsalg

For prosjekttilbud og kontrakter har en prosjektprisliste et annet prisoverstyringsmønster enn en produktprisliste. På en produktkatalogbasert tilbudslinje kan du overstyre prisen for roller og kategorier direkte på tilbudslinjen, fordi hver tilbudslinje peker på nøyaktig ett katalogelement. På en prosjektbasert tilbudslinjen kan du imidlertid ikke overstyre prisen til roller og kategorier direkte på tilbudslinjen. Bruk prosjektprislisten til å støtte de to spesifikke overstyringsmønstrene.

> [!NOTE]
> Vi anbefaler at du har en egen prisliste for prosjektressursene og katalogelementene på grunn av virkemåteforskjellene mellom de to når du overstyrer prisen.

Hver av de følgende enhetene kan ha én eller flere tilknyttede salgsprislister for prosjektprising:

- Kunde (forretningsforbindelse) 
- Salgsmulighet 
- Tilbud 
- Prosjektkontrakt

Tilknytningen til disse enhetene og en prisliste angis av prosjektprislistene. Du kan knytte én eller flere prislister til salgsenhetene Kunde, Salgsmulighet, Tilbud og Prosjektkontrakt.

Det registreres ikke automatisk en standard prosjektprisliste i en kundeoppføring. Du kan imidlertid legge ved en prosjektprisliste manuelt i kundeoppføringen. Likevel bør du likevel legge ved en prosjekt prisliste manuelt bare når du har en egen definert prisingsavtale med kunden. 

Når en prosjektprisliste er knyttet til en salgsenhet, valideres følgende informasjon:

- Prislisten som en kontekst for **Salg**. 
- Valutaen i prislisten samsvarer med kundevalutaen. 

I en prosjektkontrakt brukes følgende prioritetsrekkefølge til automatisk å angi relaterte prosjektprislister:

1. Tilbud
2. Salgsmulighet
3. Kunde 
4. Globale innstillinger 

Når en prosjektprisliste er angitt som standard, validerer systemet at valutaen samsvarer med kundens valuta, og at standardprislistene som er lagt inn, har en kontekst for **Salg**.

Du kan knytte flere prosjektprislister til enhetene Kunde, Salgsmulighet, Tilbud og Prosjektkontrakt. Denne funksjonen støtter datospesifikke standardpriser for en langvarig prosjektkontrakt, der du kan trenge mer enn én prisliste for å ta hensyn til prisoppdateringer som inntreffer på grunn av inflasjonen. Hvis prislistene som du knytter til enheten Kunde, Salgsmulighet, Tilbud eller Prosjektkontrakt, for eksempel har overlappende datogyldighet, kan standard prisene være feil. Derfor bør du sørge for at prosjektprislister som har overlappende datogyldighet, ikke er tilknyttet disse enhetene.

### <a name="deal-specific-price-overrides"></a>Avtalespesifikke prisoverstyringer

Du kan opprette avtalespesifikke overstyringer for valgte priser i prosjektprislister som er angitt som standard i et tilbud eller en prosjektkontrakt.

Som standard får en prosjektkontrakt alltid en kopi av hovedprislisten for salg i stedet for en direkte kobling til den. Denne virkemåten bidrar til å garantere at prisavtaler som gjøres med en kunde for en arbeidserklæring, ikke endrer seg hvis hovedprislisten endres.

Du kan imidlertid bruke en hovedprisliste i et tilbud. Du kan også kopiere en hovedprisliste og redigere den for å opprette en egendefinert prisliste som bare gjelder for dette tilbudet. Hvis du vil opprette en ny prisliste som er spesifikk for et tilbud, går du til **Tilbud**-siden og velger **Opprett egendefinert prising**. Du kan bare få tilgang til den avtalespesifikke prosjektprislisten fra tilbudet. 

Når du oppretter en egendefinert prosjektprisliste, kopieres bare prosjektkomponentene i prislisten. Med andre ord opprettes det en ny prisliste som en kopi av den eksisterende prosjektprislisten som er knyttet til tilbudet, og denne nye prislisten har bare relaterte rollepriser og transaksjonskategoripriser.
  
## <a name="tracking-costs"></a>Spore kostnader

Project Operations sporer kostnader for bruk av personaltid i prosjekter. Det sporer også kostnader for andre utgifter som er påløpt i løpet av prosjektet, for eksempel reiseutgifter.

På samme måte som fakturasatser defineres kostnadssatser for personale også ved hjelp av prislister. Her er hovedforskjellene i virkemåte for kostnadsprislisten og salgsprislisten:

- Kostnadssatsen for en ressurs kan ikke overstyres på et bestemt prosjekt, en kontrakt eller et bestemt tilbud. Kostnadssatser kan imidlertid overstyres av et per avtale-grunnlag hvis det blir gjort endringer som er spesifikke for typen avtale. 

- Følgende ordre brukes til å løse en kostnadsprisliste:

    1. Kostnadsprislisten som er knyttet til organisasjonsenheten.
    2. Kostnadsprislisten som er knyttet til Project Operations-parameterne. Siden kostnadsprislister i mange ulike valutaer kan knyttes til parameterne, utføres det et valutasamsvar mellom valutaen til organisasjonsenheten med kontrakten i prosjektet, kontrakten eller tilbudet samt valutaen for kostnadsprislisten.
    3. For utgifter, gjelder ikke prisingsmetodene per kostnad og påslag over kostnad for kostnadsprislister. Selv om disse prisingsmetodene brukes på kostnadsprislistelinjer til å definere kostnad for transaksjonskategorier, ignorerer systemet dem, og det angis ingen standard kostpris.
