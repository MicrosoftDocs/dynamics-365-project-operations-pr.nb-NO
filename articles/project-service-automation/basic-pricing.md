---
title: Prosjektprising
description: Dette emnet inneholder informasjon om hvordan prising fungerer i Dynamics 365 Project Service Automation.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 010fe834-c449-46ee-9d45-7c91cd8e262a
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: fec4f24688a00cd019577460e948bef6b918f1b5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754135"
---
# <a name="project-pricing"></a>Prosjektprising 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation utvider prislisteenheten i Dynamics 365 Sales. 

## <a name="key-entities"></a>Viktige enheter

En prisliste inneholder informasjon fra fire ulike enheter:

- **Prisliste** – Denne enheten lagrer informasjon om kontekst, valuta, datogyldighet og tidsenhet for prisingstiden. Konteksten viser om prislisten uttrykker kostnadssatser eller salgssatser. 
- **Valuta** – denne enheten lagrer valutakursen i prislisten. 
- **Dato** – Denne enheten brukes når systemet prøver å angi en standardpris for en transaksjon. PSA-prising velger prislisten som har datogyldighet som inkluderer datoen for transaksjonen. Hvis PSA-prisingen finner mer enn én prisliste som er gyldig for transaksjonsdatoen som er knyttet til beslektet tilbud, kontrakt eller organisasjonsenhet, blir ingen pris angitt som standard. 
- **Tid** – denne entiteten lagrer tidsenheten som prisene er uttrykt for, for eksempel daglige eller timebaserte priser. 

Prislisteenheten har tre relaterte tabeller som lagrer priser:

  - **Rollepris** – Denne tabellen lagrer en sats for en kombinasjon av verdier for rolle og organisasjonsenhet, og brukes til å konfigurere rollebaserte priser for personale.
  - **Transaksjonskategoripris** – denne tabellen lagrer priser etter transaksjonskategori og brukes til å definere utgiftskategoripriser.
  - **Prislisteelementer** – denne tabellen inneholder priser for katalogprodukter.

> ![Konfigurere priser ved hjelp av en prisliste](media/basic-guide-12.png)
 
Prislisten er et rangeringskort. Et rangeringskort er en kombinasjon av prislisteenheten og relaterte rader i tabellene Rollepris, Transaksjonskategoripris og Prislisteelementer.

## <a name="resource-roles"></a>Ressursroller

Begrepet *ressursrolle* viser til en rekke ferdigheter, kompetanser og sertifiseringer som en person må ha for å utføre et bestemt sett med oppgaver i et prosjekt.

Personaltid tilbys vanligvis basert på rollen som en ressurs fyller, i et bestemt prosjekt. For personaltid støtter PSA kostnader og fakturering som er basert på ressursrolle. Tid kan prises i alle enheter i **Tid**-enhetsgruppen.

**Tid**-enhetsgruppen opprettes når PSA installeres. Den har **Time** som standardenhet. Du kan ikke slette, gi nytt navn til eller redigere attributter for **Tid**-enhetsgruppen eller **Time**-enheten. Du kan imidlertid legge til andre enheter i **Tid**-enhetsgruppen. Hvis du prøver å slette **Tid**-enhetsgruppen eller **Time**-enheten, kan det oppstå feil i PSA-forretningslogikken.

> ![Konfigurere priser etter rolle](media/basic-guide-13.png)
 
## <a name="transaction-categories-and-expense-categories"></a>Transaksjonskategorier og utgiftskategorier

Reiseutgifter og andre utgifter som påløper for prosjektkonsulenter, blir vanligvis fakturert til kunden. PSA støtter prising av utgiftskategorier ved hjelp av prislister. Flyreiser, hotell og leiebil er eksempler på utgiftskategorier. Hver prislistelinje for utgifter angir prising for en bestemt utgiftskategori. For prising av reiseutgiftskategorier støtter PSA følgende tre prisingsmetoder:

- **Kostnad** – utgiftskostnad faktureres til kunden, og ingen påslag brukes.
- **Påslagsprosent** – prosentandelen for den faktiske kostnaden som faktureres til kunden. 
- **Pris per enhet** – en faktureringspris er angitt for hver enhet i utgiftskategorien. Beløpet som blir fakturert til kunden, beregnes basert på antall utgiftsenheter som konsulenten rapporterer. Reisegodtgjørelse bruker pris per enhet. For eksempel kan utgiftskategorien for reisegodtgjørelse konfigureres for 30 USD per dag eller 2 USD per mile. Når en konsulent rapporterer reisegodtgjørelse i et prosjekt, beregnes beløpet til fakturering basert på antall kilometer som er rapportert av konsulenten.

> ![Konfigurere prising for utgiftskategorier](media/basic-guide-14.png)
 
## <a name="project-sales-pricing-and-overrides"></a>Prising og overstyringer av prosjektsalg

For prosjekttilbud og kontrakter har en prosjektprisliste et annet prisoverstyringsmønster enn en produktprisliste. På en produktkatalogbasert tilbudslinje kan du overstyre prisen for roller og kategorier direkte på tilbudslinjen, fordi hver tilbudslinje peker på nøyaktig ett katalogelement. På en prosjektbasert tilbudslinjen kan du imidlertid ikke overstyre prisen til roller og kategorier direkte på tilbudslinjen. For å støtte de to spesifikke overstyringsmønstrene har PSA innført en ny prislistetilknytning, prosjektprislisten.

> [!NOTE]
> Vi anbefaler at du har en egen prisliste for prosjektressursene og katalogelementene på grunn av virkemåteforskjellene mellom de to når du overstyrer prisen.

Hver av de følgende enhetene kan ha én eller flere tilknyttede salgsprislister for prosjektprising:

- Kunde (forretningsforbindelse) 
- Salgsmulighet 
- Tilbud 
- Prosjektkontrakt

Tilknytningen til disse enhetene og en prisliste angis av prosjektprislistene. Du kan knytte én eller flere prislister til salgsenhetene Kunde, Salgsmulighet, Tilbud og Prosjektkontrakt.

Det registreres ikke automatisk en standard prosjektprisliste i en kundeoppføring. Du kan imidlertid legge ved en prosjektprisliste manuelt i kundeoppføringen. Likevel bør du likevel legge ved en prosjekt prisliste manuelt bare når du har en egen definert prisingsavtale med kunden. 

Når en prosjektprisliste er knyttet til en salgsenhet, validerer PSA følgende informasjon:

- Prislisten som en kontekst for **Salg**. 
- Valutaen i prislisten samsvarer med kundevalutaen. 

I en prosjektkontrakt bruker PSA følgende prioritetsrekkefølge til automatisk å angi relaterte prosjektprislister:

1. Tilbud
2. Salgsmulighet
3. Kunde 
4. Globale innstillinger for PSA

Når en prosjektprisliste er angitt som standard, validerer PSA om valutaen samsvarer med kundens valuta, og om standardprislistene som er lagt inn, har en kontekst for **Salg**.

Du kan knytte flere prosjektprislister til enhetene Kunde, Salgsmulighet, Tilbud og Prosjektkontrakt. Denne funksjonen støtter datospesifikke standardpriser for en langvarig prosjektkontrakt, der du kan trenge mer enn én prisliste for å ta hensyn til prisoppdateringer som inntreffer på grunn av inflasjonen. Hvis prislistene som du knytter til enheten Kunde, Salgsmulighet, Tilbud eller Prosjektkontrakt, for eksempel har overlappende datogyldighet, kan standard prisene være feil. Derfor bør du sørge for at prosjektprislister som har overlappende datogyldighet, ikke er tilknyttet disse enhetene.

### <a name="deal-specific-price-overrides"></a>Avtalespesifikke prisoverstyringer

I PSA kan du opprette avtalespesifikke overstyringer for valgte priser i prosjektprislister som er angitt som standard i et tilbud eller en prosjektkontrakt.

Som standard får en prosjektkontrakt alltid en kopi av hovedprislisten for salg i stedet for en direkte kobling til den. Denne virkemåten bidrar til å garantere at prisavtaler som gjøres med en kunde for en arbeidserklæring, ikke endrer seg hvis hovedprislisten endres.

Du kan imidlertid bruke en hovedprisliste i et tilbud. Du kan også kopiere en hovedprisliste og redigere den for å opprette en egendefinert prisliste som bare gjelder for dette tilbudet. Hvis du vil opprette en ny prisliste som er spesifikk for et tilbud, går du til **Tilbud**-siden og velger **Opprett egendefinert prising**. Du kan bare få tilgang til den avtalespesifikke prosjektprislisten fra tilbudet. 

Når du oppretter en egendefinert prosjektprisliste, kopieres bare prosjektkomponentene i prislisten. Med andre ord opprettes det en ny prisliste som en kopi av den eksisterende prosjektprislisten som er knyttet til tilbudet, og denne nye prislisten har bare relaterte rollepriser og transaksjonskategoripriser.

> ![Vise og konfigurere egendefinerte priser for en prosjektkontrakt](media/basic-guide-15.png)
  
## <a name="tracking-costs"></a>Spore kostnader

PSA sporer kostnader for bruk av personaltid i prosjekter. Det sporer også kostnader for andre utgifter som er påløpt i løpet av prosjektet, for eksempel reiseutgifter.

På samme måte som fakturasatser defineres kostnadssatser for personale også ved hjelp av prislister. Her er hovedforskjellene i virkemåte for kostnadsprislisten og salgsprislisten:

- Kostnadssatsen for en ressurs kan ikke overstyres på et bestemt prosjekt, en kontrakt eller et bestemt tilbud. Kostnadssatser kan imidlertid overstyres av et per avtale-grunnlag hvis det blir gjort endringer som er spesifikke for typen avtale. 

- Følgende ordre brukes til å løse en kostnadsprisliste:

    1. Kostnadsprislisten som er knyttet til organisasjonsenheten.
    2. Kostnadsprislisten som er knyttet til Project Service-parameterne. Siden kostnadsprislister i mange ulike valutaer kan knyttes til Project Service-parametere, utføres det et valutasamsvar i PSA mellom valutaen til organisasjonsenheten med kontrakten i prosjektet, kontrakten eller tilbudet samt valutaen for kostnadsprislisten.
    3. For utgifter, gjelder ikke prisingsmetodene per kostnad og påslag over kostnad for kostnadsprislister. Selv om disse prisingsmetodene brukes på kostnadsprislistelinjer til å definere kostnad for transaksjonskategorier, ignorerer systemet dem, og det angis ingen standard kostpris.
