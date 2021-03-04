---
title: Tilbud – nøkkelkonsepter – Lite
description: Dette emnet gir informasjon om hvordan du bruker prosjekttilbud i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e86f1a5a7b2859df5bf9569ee9ca306c6dcc6293
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/30/2020
ms.locfileid: "4178018"
---
# <a name="quotes---key-concepts---lite"></a>Tilbud – nøkkelkonsepter – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_


Følgende er nøkkelkonsepter du må være klar over før du begynner å bruke prosjekttilbud i Dynamics 365 Project Operations:

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

- Handlingene **Revider** og **Aktiver** støttes ikke.
- Project Operations-tilbud har to forskjellige typer linjer. Den ene er for prosjekter, og den andre er for produkter.
- Project Operations-tilbud har sitt eget format og sine egne UI-elementer, forretningsregler, plugin-moduler for forretningslogikk og skript på klientsiden som gjør dem unike fra Sales-tilbud.

Av disse grunnene anbefales det at du ikke bruker et Sales-tilbud og et Project Operations-tilbud om hverandre.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]