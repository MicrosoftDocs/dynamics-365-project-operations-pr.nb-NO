---
title: Konsepter som er unike for prosjektbaserte tilbud
description: Denne artikkelen inneholder informasjon om prosjekttilbud i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 89867cfbe92f47d58b16da40b62d3d9dd6a15b64
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824340"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Konsepter som er unike for prosjektbaserte tilbud

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Før du begynner å bruke prosjekttilbud i Microsoft Dynamics 365 Project Operations, må du være oppmerksom på følgende nøkkelkonsepter.

## <a name="owning-company"></a>Eiende firma

Det eiende firmaet representerer den juridiske enheten som eier prosjektleveringen. Kunden i tilbudet skal være en gyldig kunde i denne juridiske enheten i økonomi- og driftsapper. Valutaen til det eiende firmaet og valutaen til kontraktenheten som er valgt i et prosjektbasert tilbud, må samsvare.

## <a name="contracting-unit"></a>Kontraktsenhet

En kontraktenhet representerer avdelingen eller praksisen som eier prosjektleveringen. Du kan definere ressurskostnader for hver enkelt kontraktsenhet. Når du angir ressurskostnader for en ressurs i en kontraktenhet, kan du også konfigurere forskjellige kostnadssatser for ressurser som kontraktenheten låner fra, eller for andre avdelinger eller praksiser i virksomheten. Disse kostnadssatsene kalles overføringspriser, ressurslån eller vekslingspriser. Når du angir kostnadene ved å låne ressurser fra andre avdelinger, kan du konfigurere disse kostnadssatsene i valutaen for den utlånende avdelingen.

## <a name="cost-currency"></a>Kostnadsvaluta

Kostnadsvalutaen i Project Operations er valutaen som kostnader rapporteres i. Denne valutaen utledes fra valutaen som er knyttet til feltet **Kontraktenhet** i tilbudet, kontrakten og prosjektet. Kostnader mot et prosjekt kan registreres i enhver valuta. Det foretas imidlertid valutaomregning fra valutaen som kostnadene ble registrert i, til kostnadsvalutaen i prosjektet.

Siden valutakursene på Dataverse-plattformen (CDS) ikke kan være datoeffektive, kan totalene på skjermen for kostnader endres over tid hvis du oppdaterer valutakursen. Kostnader som registreres i databasen, forblir imidlertid uendret, siden beløpene lagres i valutaen de ble pådratt i.

## <a name="sales-currency"></a>Salgsvaluta

Salgsvalutaen i Project Operations er valutaen som de beregnede og faktiske salgsbeløpene registreres og vises i. Dette er også valutaen som kunden blir fakturert i for avtalen. Når det gjelder et prosjekttilbud, angis en standard salgsvaluta fra kunde- eller forretningsforbindelsesoppføringen, og kan endres når tilbudet opprettes. Salgsvalutaen kan imidlertid ikke endres etter at tilbudet er lagret. Standard produkt- og prosjektprislister angis basert på salgsvalutaen i tilbudet.

I motsetning til kostnader kan salgsverdier **bare** registreres i salgsvalutaen.

## <a name="billing-method"></a>Faktureringsmetode

Prosjekter har vanligvis kontraktmodeller basert på faste gebyrer og forbruk. I Project Operations representeres kontraktmodellen for et prosjekt av faktureringsmetoden. Faktureringsmetoden har to verdier: tid og materiale og fast pris.

- **Tid og materiale** – En forbruksbasert kontraktmodell der hver kostnad som påløper, støttes av den tilsvarende omsetningen. Etter hvert som du beregner eller oppfører flere kostnader, øker også det tilhørende estimerte og faktiske salget. Du kan angi grenser som ikke må overskrides, på tilbudslinjer som har denne faktureringsmetoden. På denne måten kan du sette et tak på den faktiske omsetningen. Beregnet omsetning påvirkes ikke av grensene som ikke må overskrides.
- **Fast pris** – En kontraktmodell med fast gebyr der salgsverdiene er uavhengige av kostnadene som påløper. Salgsverdien er fast og endres ikke etter hvert som du beregner eller oppfører flere kostnader.

## <a name="project-price-lists"></a>Prosjektprislister

Prosjektprislister er prislister som brukes til å angi standardpriser, ikke kostnadssatser, for tid, utgifter og andre prosjektrelaterte komponenter. Det kan være flere prislister, og hver liste kan ha sin egen datogyldighet for hvert prosjekt tilbud. Project Operations støtter ikke overlappende gyldighetsdatoer for prosjektprislister.

## <a name="product-price-lists"></a>Produktprislister

Produktprislister er prislister som brukes til å angi standardpriser, ikke kostnadssatser, for produktbaserte linjer i et tilbud. Det finnes bare én produktprisliste per tilbud.

## <a name="transaction-classes"></a>Transaksjonsklasser

Project Operations støtter fire typer transaksjonsklasser:

- Tid
- Utgift
- Materiale
- Gebyr

Kostnads- og salgsverdier kan beregnes og påløpes for transaksjonsklasser av typen **Tid**, **Utgift** og **Materiale**. **Gebyr** er en transaksjonsklasse bare for omsetning.

## <a name="work-entities-and-billing-entities"></a>Arbeidsenheter og faktureringsenheter

Prosjekter og Oppgaver er enheter som representerer arbeid. Tilbudslinjer og Kontraktlinjer er enheter som representerer fakturering. Du kan koble ulike arbeidsenheter til faktureringsalternativer ved å knytte dem til Tilbudslinjer eller Kontraktlinjer.

## <a name="multi-customer-deals"></a>Avtaler for flere kunder

Avtaler for flere kunder skjer når det er flere enn én kunde per faktura. Her er noen typiske eksempler:

- **Opprinnelige utstyrsfabrikanter (OEM) og partnerne deres** – Partnere og forhandlere selger et produkt med tjenester som gir ekstra verdi. I løpet av en avtale med en kunde tilbyr OEM-en vanligvis å finansiere en del av prosjektet.
- **Prosjekter for offentlig sektor** – Flere avdelinger hos lokale myndigheter godtar å finansiere et prosjekt, og de faktureres i henhold til en tidligere avtalt deling. Eksempel: Et skoledistrikt og byen eller de lokale myndighetene er enige om å finansiere byggingen av et svømmebasseng.

## <a name="invoice-schedules"></a>Fakturaplaner

Faktureringsplaner er spesifikke for hver tilbudslinje og valgfrie. Fakturaplaner opprettes basert på bestemte start- og sluttdatoer og en fakturahyppighet. De brukes i kontraktfasen når automatisk oppretting av fakturaer er konfigurert. Fakturaplaner er valgfrie i tilbudsfasen. Hvis de opprettes i tilbudsfasen, kopieres de til prosjektkontrakten som opprettes når et prosjekttilbud blir vunnet.

## <a name="differences-from-dynamics-365-sales-quotes"></a>Forskjeller fra tilbud i Dynamics 365 Sales

Project Operations-tilbud er basert på Dynamics 365 Sales-tilbud. Det er imidlertid noen viktige forskjeller i funksjonaliteten du bør være oppmerksom på:

- Project Operations-tilbud har to ulike typer linjer: én for prosjekter og én for produkter.
- Project Operations-tilbud har en egen side og egne brukergrensesnittelementer, forretningsregler, programtillegg for forretningslogikk og skript på klientsiden som skiller dem fra Sales-tilbud.
- I Sales kan du knytte flere ordrer til ett salgstilbud. I Project Operations kan du bare knytte én prosjektkontrakt til et prosjekttilbud.
- Når du vinner et tilbud, kan den relaterte salgsmuligheten forbli åpen. Når et prosjekttilbud er vunnet, blir den relaterte salgsmuligheten lukket.
- Et salgstilbud inkluderer ikke enkelte felter og konsepter som et prosjekttilbud omfatter. Feltene omfatter **Kontraktenhet**, **Forretningsforbindelsesansvarling** og **Navn på kontakt for fakturering**.
- Salgstilbud og prosjekttilbud identifiseres ved hjelp av feltet **Type** som er basert på et alternativsett. For et salgstilbud er verdien i dette feltet **Varebasert**. For et prosjekttilbud er verdien **Arbeidsbasert**.

På grunn av disse forskjellene anbefaler vi at du ikke bruker Sales-tilbud og Project Operations-tilbud om hverandre.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
