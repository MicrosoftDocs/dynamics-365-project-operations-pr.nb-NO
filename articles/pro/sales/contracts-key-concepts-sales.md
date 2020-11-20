---
title: Prosjektkontrakter – Nøkkelkonsepter – Lite
description: Dette emnet gir informasjon om nøkkelkonseptene for prosjektkontrakter.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ce37c9dd18fd01e599e8766389e42c066e182547
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177073"
---
# <a name="project-contracts---key-concepts---lite"></a>Prosjektkontrakter – Nøkkelkonsepter – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Dette emnet omtaler nøkkelkonseptene du må være klar over før du begynner å bruke prosjektkontrakter i Dynamics 365 Project Operations:

## <a name="contracting-unit"></a>Kontraktsenhet

Kontraktenheten representerer avdelingen eller praksisen som eier leveringen av prosjektet. Du kan definere ressurskostnader for hver enkelt kontraktsenhet. Når du angir ressurskostnaden for en ressurs, vil du også kunne angi forskjellige kostnadssatser for ressurser. Denne kontraktenheten låner disse ressursene fra andre avdelinger eller praksiser i virksomheten. Kostnadssatsene for ressursene henvises til som overføringspriser, ressurslån eller vekslingspriser. Når du angir kostnadssatsene for å låne ressurser fra andre avdelinger, bruker du valutaen for den utlånende avdelingen.

## <a name="cost-currency"></a>Kostnadsvaluta

Kostnadsvaluta er valutaen som kostnader rapporteres i, på skjermen. Denne valutaen utledes fra valutaen som er knyttet til feltet **Kontraktenhet** i kontrakten og prosjektet. Kostnader kan registreres i alle valutaer mot et prosjekt. Det er imidlertid valutaomregning fra valutaen kostnadene ble registrert i, til kostnadsvalutaen i prosjektet når den vises på skjermen.

Siden valutakursene i Common Data Service-plattformen (CDS) ikke kan være datoeffektive, kan totalene på skjermen for kostnader endres over tid hvis du oppdaterer valutakursen. Kostnader som er registrert i databasen, forblir imidlertid uendret, siden beløpene lagres i valutaen de ble pådratt i.

## <a name="sales-currency"></a>Salgsvaluta

Salgsvaluta i Project Operations er valutaen som de beregnede og faktiske salgsbeløpene registreres og vises i. Salgsvalutaen er også valutaen som kunden blir fakturert i for avtalen. I en prosjektkontrakt kommer salgsvalutaen som standard fra kunde- eller forretningsforbindelsesoppføringen, og kan endres når kontrakten opprettes. Når en kontrakt opprettes ved å lukke et tilbud som vunnet, hentes valutaen i kontrakten som standard fra valutaen i tilbudet.

Når du oppretter en prosjektkontrakt fra grunnen av, kan ikke feltet **Salgsvaluta** redigeres. Produkt- og prosjektprislister er som standard basert på denne valutaen i kontrakten.

I motsetning til kostnader kan salgsverdier bare registreres i salgsvalutaen.

## <a name="billing-method"></a>Faktureringsmetode

Det finnes vanligvis to typer kontraktmodeller for prosjekter, fast gebyr og forbruksbasert. Disse modellene er representert i Project Operations som faktureringsmetoder med to mulige verdier:

- Tid og materiale: En forbruksbasert kontraktmodell der hver kostnad som påløper, støttes av den tilsvarende omsetningen. Etter hvert som du beregner eller oppfører flere kostnader, øker også det tilhørende estimerte og faktiske salget. Angi grenser som ikke må overskrides, på kontraktlinjer som har denne faktureringsmetoden, som setter et tak på den faktiske omsetningen. Beregnet omsetning påvirkes ikke av grensene som ikke må overskrides.
- Fast pris: En kontraktmodell med fast gebyr som angir at salgsverdiene er uavhengige av påløpte kostnader. Salgsverdien er fast og endres ikke etter hvert som du beregner eller oppfører flere kostnader.

## <a name="project-price-lists"></a>Prosjektprislister

Prosjektprislister brukes til å standardisere priser, ikke kostnadssatser, for tid, utgifter og andre prosjektrelaterte komponenter. Det kan være flere prislister. Hver prisliste har sin egen datogyldighet for hver prosjektkontrakt. Overlapping av datogyldighet på prosjektprislister støttes ikke i Project Operations.

Når en prosjektkontrakt opprettes ved å vinne et prosjekttilbud, kopieres prosjektprislistene sammen med kontraktnavnet og den inkluderte datoen. Kopiering av denne informasjonen utgjør egendefinerte priser for prosjektkomponenter for denne prosjektkontrakten.

## <a name="product-price-lists"></a>Produktprislister

Produktprislister brukes til å standardisere priser, ikke kostnadssatser, for produktbaserte linjer i en kontrakt. Det er bare én produktprisliste per kontrakt.

## <a name="transaction-classes"></a>Transaksjonsklasser

Project Operations støtter fire typer transaksjonsklasser:

- Tid
- Utgift
- Materiale
- Gebyr

Kostnads- og salgsverdier kan beregnes og påløpes for transaksjonsklasser av typen tid, utgifter og materialer. Avgift er en transaksjonsklasse bare for omsetning.

## <a name="work-entities-and-billing-entities"></a>Arbeidsenheter og faktureringsenheter

Enheter som representerer arbeid, er prosjekter og oppgaver. Enheter som representerer faktureringsaspekter, er kontraktlinjer. Du kan binde forskjellige arbeidsenheter til faktureringsalternativer ved å binde dem til kontraktlinjer.

## <a name="multi-customer-deals"></a>Avtaler for flere kunder

Avtaler for flere kunder har flere enn én kunde å fakturere for en avtale. Noen vanlige eksempler:

- OEM-selskaper og deres partnere: Partnere og forhandlere selger et produkt med enkelte verdiøkende tjenester som vanligvis involverer en bestemt avtale med en kunde. OEM-en tilbyr å finansiere en del av prosjektet. 

- Prosjekter for offentlig sektor: Flere avdelinger hos lokale myndigheter godtar å finansiere et prosjekt, og de faktureres i henhold til en tidligere avtalt fordeling. Eksempel: Et skoledistrikt og de lokale myndighetene er enige om å finansiere byggingen av et svømmebasseng.

## <a name="invoice-schedules"></a>Fakturaplaner

Fakturaplaner er spesifikke for hver kontraktlinje, og de kreves for at automatisk fakturering skal fungere. Fakturaplaner opprettes basert på bestemte start- og sluttdatoer og fakturahyppighet. Planene brukes i kontraktfasen når automatisk oppretting av fakturaer er konfigurert. Når en prosjektkontrakt opprettes fra et tilbud, kopieres fakturaplanen til prosjektkontrakten fra tilbudet.

## <a name="changes-from-the-dynamics-365-sales-contract"></a>Endringer fra Dynamics 365 Sales-kontrakter

Project Operations-kontrakter blir utformet basert på Dynamics 365 Sales-kontrakter. Det er imidlertid noen viktige avvik og forskjeller i funksjonaliteten du bør være oppmerksom på:

- Project Operations-kontrakter har to ulike typer linjer, én for prosjekter og én for produkter.
- Project Operations-kontrakter har sitt eget format og sine egne UI-elementer, forretningsregler, plugin-moduler for forretningslogikk og skript på klientsiden som gjør dem unike fra salgskontrakter.

Av disse grunnene bør du ikke bruke en salgskontrakt og en prosjektkontrakt om hverandre.
