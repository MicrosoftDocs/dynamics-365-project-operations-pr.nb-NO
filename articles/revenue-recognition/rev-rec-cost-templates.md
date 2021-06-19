---
title: Konfigurere kostnadsmaler
description: Dette emnet gir informasjon om hvordan du oppretter og bruker kostnadsmaler i Project Operations.
author: sigitac
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f4a515db31a31028af4a60927ab360be6c261a3f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013903"
---
# <a name="set-up-cost-templates"></a>Konfigurere kostnadsmaler

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_


Dette emnet gir informasjon om hvordan du oppretter og bruker kostnadsmaler i Project Operations. En kostnadsmal bestemmer:

- Prosjektkategoriene for prognose og faktiske transaksjoner som skal tas med i en prosentdel av fullføringsberegningen for prosjektet. Verdien for prosent fullført brukes til å beregne hvor mye inntekt som blir gjenkjent.
- Hvorvidt fullføringsprosenten kan endres hvis den beregnes automatisk.
- Hvorvidt prosent fullført beregnes basert på beløp eller enheter.

## <a name="cost-template-example"></a>Eksempel på kostnadsmal

Du arbeider med et designprosjekt for en nettside for en kunde der du belaster et flatt gebyr på USD 10 000. Du beregner at det vil ta 100 timer (USD 5 000) for å fullføre prosjektet. Du beregner også inn to flybilletter og fire netter på hotell for å reise til kunden (USD 1 800). Dette fører til en samlet beregnet kostnad på USD 6 800.

Når du kjører inntektsføringen for fastpris for å opprette et estimat på slutten av måneden, oppdager du ut at du har arbeidet 35 timer på prosjektet. Dette inkluderer ennå ikke flyturer eller hotellkostnader. Du har også fått en assistent til å bruke fem timer på undersøkelser for prosjektet til en kostnad på USD 100, som du ikke hadde planlagt for.

Når du beregner verdien for prosent fullført for dette prosjektet, har du følgende valg å ta:

- Vil du ta med alle kostnader (timer og utgifter) eller bare timer?
- Vil du ta med alle timer eller bare planlagte timer?
- Vil du beregne prosent fullført basert på dollarkostnaden for de planlagte timene (USD 5 000) eller bare på antall timer (100)?

Svarene på disse spørsmålene avgjør alternativene du angir i kostnadsmalen, og kategoriene du velger på kostnadsmallinjene.

Tabellen nedenfor illustrerer resultatene av forskjellige metoder for beregning av prosent fullført-verdien for dette scenariet.

| Fullføring basert på | Dollarkostnad eller enheter | Prosent fullført | Beregning |
| --- | --- | --- | --- |
| Alle timer, ingen utgifter | Dollarkostnad | 37 % 35 x USD 50 + USD 100 = USD 1 850 USD 1 850 / USD 5 000 |
| Alle timer, ingen utgifter | Enheter | 40 % | 40 timer / 100 timer (inkludert fem ikke-planlagte timer) |
| Planlagte timer, ingen utgifter | Dollarkostnad eller enhet | 35 % | 35/100 timer eller 35 x USD 50 / 5 000 |
| Alle timer og utgifter | Dollarkostnad | 27,2 % | USD 1 850 / USD 6 800 |

Hvilken fremgangsmåte du bestemmer deg for når du skal opprette en kostnadsmal kan avhenge av ulike hensyn:

- Hvis du inkluderer ikke-planlagte timer i kostnadsmalen, risikerer du å nå 100 prosent fullført før prosjektet er ferdig. Dette skyldes at faktiske timer blir høyere enn planlagte timer. Hvis du bruker én av de to første metodene som er oppført i tabellen, må du endre planen (beregnede enheter) når du blir oppmerksom på avvik. I dette tilfellet kan du legge til eller trekke fra timer basert på hva som kreves for å fullføre prosjektet. Hvis prosjektet kommer til å kreve ytterligere 65 timer for å fullføres, legger du til fem timer i planen og får totalt 105. Hvis du vet at assistenten kommer til å bruke ytterligere fem timer på undersøkelser, blir totalen 110 timer.
- Hvis du bruker den tredje metoden som er oppført i tabellen, må du bare oppdatere de planlagte timene for din egen tid for å holde beregningen for prosent fullført nøyaktig. Lønnsomheten endrer seg når ikke-planlagt tid registreres, men du vil bli værende på en kjent bane for prosent fullført.
- Hvis du bruker den fjerde metoden som er oppført i tabellen, er risikoen at utgiftene vil dukke opp på uregelmessige tidspunkt, og reflekteres kanskje ikke i løpet av fullføringsfremdriften. Hvis utgiftene er inkludert, kan de derfor føre til at prosent fullført-verdien varierer mer enn ønskelig. Hvis du for eksempel ikke har vært på en flytur ennå, var fullføringsprosenten 27 prosent i stedet for 35 prosent eller 37 prosent hvis du skulle basere beregningen på kun tid. Hvis du hadde tatt én reise på to netter og har anslått kostnadene for flyturer og hotell riktig, ville prosent fullført ha vært 40,4 prosent (USD 1850 for arbeid og USD 900 for utgifter = USD 2750 / USD 6800 = 40,4 prosent). Derfor vil det å bruke utgiftene for bare én flytur endre prosent fullført fra 27 prosent til 40 prosent.

## <a name="create-cost-templates"></a>Opprette kostnadsmaler
Følg denne fremgangsmåten for å opprette kostnadsmaler:

1. Hvis du vil ha tilgang til kostnadsmaler i Dynamics 365 Finance, går du til **Prosjektstyring og regnskap** > **Oppsett** > **Estimater** > **Kostnadsmal**.
2. Velg **Ny** for å opprette en ny kostnadsmal. Angi et navn og en beskrivelse.
3. Oppgi kostnadslinje-ID for hver transaksjonstype.
4. Velg en standard fullføringsmetode:

  - **Automatisk**: Fullføringsprosenten beregnes automatisk i et prosjekt. Resultatverdien kan ikke endres.
  - **Manuell**: Fullføringsprosenten beregnes automatisk i et prosjekt. Resultatverdien kan endres.

  > [!NOTE]
  > Når det gjelder manuelle beregninger, opprettholdes fullføringsprosenten i **Manuell beregning** på **Generelt**-fanen på **Estimat**-siden.

5. I **Fullføring basert på** kan du velge én av følgende verdier:

  - **Beløp**: Beløpet i regnskapsvaluta beregner fullføringsprosenten.
  - **Enhet**: Antallet beregner fullføringsprosenten.
  - **Rett linje**: Systemet beregner fullføringsprosenten på et proporsjonalt grunnlag ved hjelp av start- og sluttdatoene for prosjektet for å bestemme lengden på prosjektet.

6. Velg **Kostnadslinjer** for å gjennomgå kostnadslinjene i kostnadsmalen. Det kreves minst én kostnadslinje for hver transaksjonstype. Du kan imidlertid opprette flere kostnadslinjer for de samme transaksjonstypene og angi ønskede attributter for disse linjene.
7. På **Kategorier**-fanen velger du prosjektkategoriene som skal tas med på kostnadsmallinjen.
8. På **Generelt**-fanen velger du om denne linjen skal tas med i beregningen av fullføringsprosent.
9. Velg ferdigstillelseskostnad-metoden ved beregning av fullføringsprosenten.


[!INCLUDE[footer-include](../includes/footer-banner.md)]