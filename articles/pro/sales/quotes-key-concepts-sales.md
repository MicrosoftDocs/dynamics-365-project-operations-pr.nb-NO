---
title: Konsepter som er unike for prosjekttilbud
description: Denne artikkelen inneholder informasjon om bruk av prosjekttilbud i Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7f0a33f1d7d77f3b5aebfdcf8e6aeb14072cd596
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825906"
---
# <a name="concepts-unique-to-project-quotes"></a>Konsepter som er unike for prosjekttilbud

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_


Følgende er nøkkelkonsepter som du må være klar over før du begynner å prosjekttilbud i Dynamics 365 Project Operations:

## <a name="contracting-unit"></a>Kontraktsenhet

Kontraktenheten representerer avdelingen eller praksisen som eier prosjektleveringen. Du kan definere ressurskostnader for hver enkelt kontraktsenhet. Når du angir ressurskostnad for en ressurs i kontraktenheten, kan du også angi forskjellige kostnadssatser for ressurser som denne kontraktenheten låner fra, eller andre avdelinger eller praksiser i virksomheten. Disse henvises til som overføringspriser, ressurslån eller vekslingspriser. Når du angir kostnadene ved å låne ressurser fra andre avdelinger, kan du også velge å konfigurere disse kostnadssatsene i valutaen for den utlånende avdelingen.

## <a name="cost-currency"></a>Kostnadsvaluta

Kostnadsvaluta i Project Operations er valutaen som kostnader rapporteres i. Denne valutaen utledes fra valutaen som er knyttet til feltet **Kontraktenhet** i tilbudet, kontrakten og prosjektet. Kostnader kan registreres i alle valutaer mot et prosjekt. Det er imidlertid valutaomregning fra valutaen kostnadene ble registrert i, til kostnadsvalutaen i prosjektet.

Siden valutakursene i CDS-plattformen ikke være datoeffektive, kan totalene på skjermen for kostnader endres over tid hvis du oppdaterer valutakursen. Kostnader som er registrert i databasen, forblir imidlertid uendret, siden beløpene lagres i valutaen de ble pådratt i.

## <a name="sales-currency"></a>Salgsvaluta

Salgsvaluta i Project Operations er valutaen som de beregnede og faktiske salgsbeløpene registreres og vises i. Dette er også valutaen som kunden blir fakturert i for avtalen. I et prosjekttilbud kommer salgsvalutaen som standard fra kunde- eller forretningsforbindelsesoppføringen, og kan endres når tilbudet opprettes. Etter at tilbudet er lagret, kan ikke salgsvalutaen endres. Produkt- og prosjektprislister er som standard basert på salgsvalutaen i tilbudet.

I motsetning til kostnader kan salgsverdier bare registreres i salgsvalutaen.

## <a name="billing-method"></a>Faktureringsmetode

Prosjekter har vanligvis kontraktmodeller basert på faste gebyrer og forbruk. Dette representeres i Project Operations som **Faktureringsmetode** og har to verdier: tid og materiale og fast pris.

- **Tid og materiale**: Dette er en forbruksbasert kontraktmodell der hver kostnad som påløper, støttes av den tilsvarende omsetningen. Etter hvert som du beregner eller oppfører flere kostnader, øker også det tilhørende estimerte og faktiske salget. Du kan angi grenser som ikke må overskrides, på tilbudslinjer som har denne faktureringsmetoden. Dette setter et tak på den faktiske omsetningen. Beregnet omsetning påvirkes ikke av grensene som ikke må overskrides.
- **Fast pris:** Dette er en kontraktmodell med fast gebyr som angir at salgsverdiene er uavhengige av påløpte kostnader. Salgsverdien er fast og endres ikke etter hvert som du beregner eller oppfører flere kostnader.

## <a name="project-price-lists"></a>Prosjektprislister

Prosjektprislister er prislister som brukes til å standardisere priser, ikke kostnadssatser, for tid, utgifter og andre prosjektrelaterte komponenter. Det kan være flere prislister, og hver liste kan ha sin egen datogyldighet for hvert prosjekt tilbud. Overlapping av datogyldighet på prosjektprislister støttes ikke i Project Operations.

## <a name="product-price-lists"></a>Produktprislister

Produktprislister er prislister som brukes til å standardisere priser, ikke kostnadssatser, for produktbaserte linjer i et tilbud. Det er bare én produktprisliste per tilbud.

## <a name="transaction-classes"></a>Transaksjonsklasser

Project Operations støtter fire typer transaksjonsklasser:

- Tid
- Utgift
- Materiale
- Gebyr

Kostnads- og salgsverdier kan beregnes og påløpes for transaksjonsklasser av typen tid, utgifter og materialer. Avgift er en transaksjonsklasse bare for omsetning.

## <a name="work-entities-and-billing-entities"></a>Arbeidsenheter og faktureringsenheter

Enheter som representerer arbeid, er prosjekter og oppgaver. Enheter som representerer fakturering, er tilbudslinjer og kontraktlinjer. Du kan koble forskjellige arbeidsenheter til faktureringsalternativer ved å knytte dem til et tilbud eller kontraktlinjer.

## <a name="multi-customer-deals"></a>Avtaler for flere kunder

Avtaler for flere kunder inntreffer når det er flere enn én kunde å fakturere. Vanlige eksempler på dette inkluderer:

- **OEM-selskaper og deres partnere:** Partnere og forhandlere selger et produkt med tjenester som gir ekstra verdi. Dette er vanligvis et scenario der den opprinnelige utstyrsprodusenten tilbyr å finansiere en del av prosjektet, under løpet av en bestemt avtale med en kunde. 

- **Prosjekter for offentlig sektor:** Flere avdelinger hos lokale myndigheter godtar å finansiere et prosjekt, og de faktureres i henhold til en tidligere avtalt fordeling. Eksempel: Et skoledistrikt og byen eller de lokale myndighetene er enige om å finansiere byggingen av et svømmebasseng.

## <a name="invoice-schedules"></a>Fakturaplaner

Faktureringsplaner er spesifikke for hver tilbudslinje, og de er også valgfrie. Fakturaplaner opprettes basert på bestemte start- og sluttdatoer og fakturahyppighet. Fakturaplaner brukes i kontraktfasen når automatisk oppretting av fakturaer er konfigurert. Tidsplanene er valgfrie i tilbudsfasen. Når fakturaplaner opprettes i **Tilbud**-fasen, kopieres de til prosjektkontrakten som opprettes når et prosjekttilbud blir vunnet.

## <a name="changes-from-dynamics-365-sales-quote"></a>Endringer fra Dynamics 365 Sales-tilbud:

Project Operations-tilbud blir utformet basert på Dynamics 365 Sales-tilbud. Det er imidlertid noen viktige forskjeller i funksjonaliteten du bør være oppmerksom på:


- Project Operations-tilbud har to forskjellige typer linjer. Den ene er for prosjekter, og den andre er for produkter.
- Project Operations-tilbud har sitt eget format og sine egne UI-elementer, forretningsregler, programtillegg for forretningslogikk og skript på klientsiden som gjør dem unike fra Sales-tilbud.
- Salgstilbud lar deg knytte flere ordrer til et salgstilbud. I Project Operations kan bare én prosjektkontrakt knyttes til et prosjekttilbud.
- Når du vinner et tilbud, kan den relaterte salgsmuligheten forbli åpen. Når et prosjekttilbud er vunnet, blir den relaterte salgsmuligheten lukket.
- Et salgstilbud inkluderer ikke enkelte felt og konsepter som er inkludert i et prosjekttilbud. Feltene omfatter **Kontraktenhet**, **Forretningsforbindelsesansvarling** og **Navn på kontakt for fakturering**.  
- **Type**: Salgstilbud og prosjekttilbud identifiseres også ved hjelp av feltet basert på et alternativsett med navnet **Type**. For et salgstilbud har dette feltet verdien **Varebasert**. For et prosjekttilbud har det verdien **Arbeidsbasert**.

Av disse grunnene anbefales det at du ikke bruker et Sales-tilbud og et Project Operations-tilbud om hverandre.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
