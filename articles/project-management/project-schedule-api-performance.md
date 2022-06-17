---
title: API-ytelse for prosjektplan
description: Denne artikkelen inneholder informasjon om ytelsestestetestene for API-ene for prosjektplanen og viser gode fremgangsmåter for optimal bruk.
author: ruhercul
ms.date: 11/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1ee1bd8e4412ee1d10f445628c5dc87cc9fa91d3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911194"
---
# <a name="project-schedule-api-performance"></a>API-ytelse for prosjektplan

_**Gjelder:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering, Project for the web_

Denne artikkelen inneholder informasjon om ytelsestestetestene for API-ene (Application Programming Interface) for prosjektplanen og viser gode fremgangsmåter for optimalisering av bruk.

## <a name="project-scheduling-service"></a>Prosjektplanleggingstjeneste
Prosjektplanleggingstjeneste er en flerleiertjeneste som kjører i Microsoft Azure. Den er utformet for å forbedre samhandlingen ved å gi en rask og sømløs opplevelse når brukerne arbeider med prosjekter. Denne forbedringen oppnås ved å godta endringsforespørsler, behandle dem og deretter umiddelbart returnere resultatet. Tjenesten forblir asynkron mot Dataverse og blokkerer ikke brukere fra å utføre andre operasjoner.

API-ene for prosjektplanlegging er avhengig av at prosjektplanleggingstjenesten kjører forespørsler, som er beskrevet mer detaljert i senere deler av denne artikkelen.

API-ene for prosjektplan er utformet for å fungere med følgende enheter for arbeidsnedbrytningsstruktur (WBS-enheter):

  - Project
  - Prosjektoppgave
  - Avhengighet for prosjektoppgaver
  - Prosjektteammedlem
  - Ressurstilordning
  
Både standardfelter og egendefinerte felter støttes. Med mindre annet er angitt, støttes alle vanlige operasjoner, for eksempel oppretting, oppdatering og sletting. Hvis du vil ha mer informasjon, kan du se [Bruk API-er for prosjektplan til å utføre operasjoner og planlegge enheter](schedule-api-preview.md).

Som en del av API-ene for prosjektplan er det lagt til et arbeidsenhetsmønster. Dette mønsteret er kjent som et OperationSet, og kan brukes når flere forespørsler må behandles i én enkelt transaksjon.

Illustrasjonen nedenfor viser flyten som en partner vil oppleve når denne funksjonen brukes.

![Dataverse og tjenesteflyten for prosjektplanlegging.](./media/dataverse-project-scheduling-service-flow.png)

**Trinn 1**: En klient foretar et API-kall til et OData-endepunkt (Open Data Protocol) i Dataverse for å opprette et OperationSet.

**Trinn 2**: Når det nye OperationSet er opprettet, returneres en **OperationSetId**-verdi.

**Trinn 3**: Klienten bruker **OperationSetId**-verdien til å utføre en annen API-forespørsel for prosjektplanen. Resultatet er en forespørsel om oppretting, oppdatering eller sletting for en planleggingsenhet. Når denne forespørselen er foretatt, blir metadatavalidering utført. Hvis valideringen mislykkes, avsluttes forespørselen, og det returneres en feil.

**Trinn 4a–4c**: Disse trinnene representerer GODTA-fasen. Klienten kaller API-en **ExecuteOperationSetV1**, som sender alle endringene til prosjektplanleggingstjenesten i én gruppe. Prosjektplanleggingstjenesten kjører sine egne valideringer på forespørsler i bunken. Eventuelle valideringsfeil tilbakestiller bunken og returnerer et unntak til oppkalleren. Hvis bunken blir godtatt av prosjektplanleggingstjenesten, oppdateres OperationSet-statusen for å gjenspeile det faktum at OperationSet blir behandlet av prosjektplanleggingstjenesten.

**Trinn 5**: Dette trinnet representerer VEDVARE-fasen. Prosjektplanleggingstjenesten skriver bunken asynkront til Dataverse i en transaksjon. Hvis skriveoperasjonen er vellykket, blir OperationSet merket som **Fullført**. Eventuelle feil ruller tilbake transaksjonen og bunken, og OperationSet blir merket som **Mislykket**.

## <a name="performance-methodology"></a>Ytelsesmetodikk
Utførelsestiden defineres som tiden fra kallet til API-en **ExecuteOperationSetV1** til prosjektplanleggingstjenesten er ferdig med å skrive til Dataverse. Alle operasjoner kjører til sammen 2200 ganger, og målingene for P99-utførelsestiden rapporteres. Operasjoner med én oppføring og masseoperasjoner måles.

For en operasjon med én oppføring inneholder OperationSet én forespørsel. For masseoperasjoner inneholder det 20, 50 eller 100 forespørsler. Hver bunkestørrelse rapporteres separat.

Disse operasjonene kjører på en UR 15 Project Operations Lite-distribusjon i Nord-Amerika.

## <a name="results"></a>Resultater
### <a name="create-operations"></a>Opprett operasjoner
#### <a name="single-record-create-operations"></a>Opprett operasjoner med én oppføring
Tabellen nedenfor viser utførelsestidene for oppretting av én enkelt oppføring. Tidene er i sekunder.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Oppføringstype&nbsp;&nbsp;&nbsp;</th>
    <th class="tg-0lax" colspan="2">Tid</th>
  </tr>
  <tr>
    <th class="tg-0lax">Obligatoriske felter</th>
    <th class="tg-0lax">Alle støttede felter</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">2.5</td>
    <td class="tg-0lax">3.78</td>
  </tr>
  <tr>
    <td class="tg-0lax">Oppgave</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Oppgave</td>
    <td class="tg-0lax">9.19</td>
    <td class="tg-0lax">9.19</td>
  </tr>
  <tr>
    <td class="tg-0lax">Teammedlem</td>
    <td class="tg-0lax">0.84</td>
    <td class="tg-0lax">4.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">Avhengighet</td>
    <td class="tg-0lax">8.84</td>
    <td class="tg-0lax">8.84</td>
  </tr>
</tbody>
</table>

#### <a name="bulk-create-operations"></a>Masseopprettingsoperasjoner
Tabellen nedenfor viser utførelsestidene for oppretting av mange oppføringer. Microsoft målte spesifikt utførelsestiden for oppretting av 20, 50 og 100 oppføringer i ett enkelt OperationSet. Tidene er i sekunder.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Oppføringstype&nbsp;&nbsp;&nbsp;</th>
    <th class="tg-0lax" colspan="6">Tid</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 oppføringer</th>
    <th class="tg-0lax" colspan="2">50 oppføringer</th>
    <th class="tg-0lax" colspan="2">100 oppføringer</th>
  </tr>
  <tr>
    <th class="tg-0lax">Obligatoriske felter</th>
    <th class="tg-0lax">Alle støttede felter</th>
    <th class="tg-0lax">Obligatoriske felter</th>
    <th class="tg-0lax">Alle støttede felter</th>
    <th class="tg-0lax">Obligatoriske felter</th>
    <th class="tg-0lax">Alle støttede felter</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Oppgave</td>
    <td class="tg-0lax">19.92</td>
    <td class="tg-0lax">38.35</td>
    <td class="tg-0lax">36.67</td>
    <td class="tg-0lax">99.13</td>
    <td class="tg-0lax">116.77</td>
    <td class="tg-0lax">174.06</td>
  </tr>
  <tr>
    <td class="tg-0lax">Oppgave</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">69.38</td>
    <td class="tg-0lax">69.38</td>
  </tr>
  <tr>
    <td class="tg-0lax">Avhengighet</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">176.89</td>
    <td class="tg-0lax">176.89</td>
  </tr>
</tbody>
</table>

> [!NOTE] 
> Masseopprettingsoperasjoner i enhetene **Prosjekt** og **Teammedlem** er ikke inkludert i denne tabellen fordi kjøretiden for disse operasjonene ligner på kjøretiden når API-en for oppretting av én oppføring kalles flere ganger. Disse API-ene kjøres umiddelbart i Dataverse.

Illustrasjonen nedenfor viser handlingen for utførelsestiden for enhetene **Oppgave**, **Tilordning** og **Avhengighet** når 20, 50 og 100 oppføringer opprettes og alle de støttede feltene brukes.

![Graf for utførelsestid ved oppretting av oppføringer.](./media/create-record-execution-time.png)

### <a name="update-operations"></a>Oppdater operasjoner
#### <a name="single-record-update-operations"></a>Oppdater operasjoner med én oppføring
Tabellen nedenfor viser utførelsestidene for oppdateringer av én enkelt oppføring. Tidene er i sekunder.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Oppføringstype&nbsp;&nbsp;&nbsp;</th>
    <th class="tg-0lax" colspan="2">Tid</th>
  </tr>
  <tr>
    <th class="tg-0lax">Obligatoriske felter </th>
    <th class="tg-0lax">Alle støttede felter</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">9.53</td>
    <td class="tg-0lax">13.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Oppgave</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Teammedlem</td>
    <td class="tg-0lax">9</td>
    <td class="tg-0lax">8.96</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Oppdateringsoperasjoner for enhetene **Ressurstilordninger** og **Avhengighet for prosjektoppgaver** støttes ikke.

#### <a name="bulk-update-operations"></a>Masseoppdateringsoperasjoner
Tabellen nedenfor viser utførelsestidene for oppdatering av mange oppføringer. Microsoft målte spesifikt utførelsestiden for oppdatering av 20, 50 og 100 oppføringer i ett enkelt OperationSet. Tidene er i sekunder.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Oppføringstype&nbsp;&nbsp;&nbsp;</th>
    <th class="tg-0lax" colspan="6">Tid</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 oppføringer</th>
    <th class="tg-0lax" colspan="2">50 oppføringer</th>
    <th class="tg-0lax" colspan="2">100 oppføringer</th>
  </tr>
  <tr>
    <th class="tg-0lax">Obligatoriske felter</th>
    <th class="tg-0lax">Alle støttede felter</th>
    <th class="tg-0lax">Obligatoriske felter</th>
    <th class="tg-0lax">Alle støttede felter</th>
    <th class="tg-0lax">Obligatoriske felter</th>
    <th class="tg-0lax">Alle støttede felter</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Oppgave</td>
    <td class="tg-0lax">8.91</td>
    <td class="tg-0lax">38.71</td>
    <td class="tg-0lax">20.92</td>
    <td class="tg-0lax">87.13</td>
    <td class="tg-0lax">36.68</td>
    <td class="tg-0lax">190.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Teammedlem</td>
    <td class="tg-0lax">20.52</td>
    <td class="tg-0lax">26.06</td>
    <td class="tg-0lax">41.93</td>
    <td class="tg-0lax">44.51</td>
    <td class="tg-0lax">38.63</td>
    <td class="tg-0lax">66.53</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Oppdateringsoperasjoner for enhetene **Ressurstilordninger** og **Avhengighet for prosjektoppgaver** støttes ikke.

Illustrasjonen nedenfor viser handlingen for utførelsestiden for enhetene Oppgave og Teammedlem når 20, 50 og 100 oppføringer oppdateres og alle de støttede feltene brukes.

![Graf for utførelsestid ved oppdatering av oppføringer.](./media/update-record-execution-time.png)

### <a name="delete-operations"></a>Slett operasjoner
#### <a name="single-record-delete-operations"></a>Slett operasjoner med én oppføring
Tabellen nedenfor viser utførelsestidene for sletting av én enkelt oppføring. Tidene er i sekunder.

| Oppføringstype | Tid  |
|-------------|-------|
| Oppgave        | 20.12 |
| Oppgave  | 10.86 |
| Teammedlem | 12.52 |
| Avhengighet  | 20.89 |

> [!NOTE]
> Sletting av operasjoner i **Prosjekt**-enheten støttes ikke.

#### <a name="bulk-delete-operations"></a>Masseslettingsoperasjoner
Tabellen nedenfor viser utførelsestidene for sletting av mange oppføringer. Microsoft målte spesifikt utførelsestiden for sletting av 20, 50 og 100 oppføringer i ett enkelt OperationSet. Tidene er i sekunder.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Oppføringstype&nbsp;&nbsp;&nbsp;</th>
    <th class="tg-0lax" colspan="3">Tid</th>
  </tr>
  <tr>
    <th class="tg-0lax">20 oppføringer</th>
    <th class="tg-0lax">50 oppføringer</th>
    <th class="tg-0lax">100 oppføringer</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Oppgave</td>
    <td class="tg-0lax">20.91</td>
    <td class="tg-0lax">67.43</td>
    <td class="tg-0lax">71.96</td>
  </tr>
  <tr>
    <td class="tg-0lax">Oppgave</td>
    <td class="tg-0lax">11.75</td>
    <td class="tg-0lax">25.79</td>
    <td class="tg-0lax">47.66</td>
  </tr>
  <tr>
    <td class="tg-0lax">Teammedlem</td>
    <td class="tg-0lax">9.78</td>
    <td class="tg-0lax">39.73</td>
    <td class="tg-0lax">24.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">Avhengighet</td>
    <td class="tg-0lax">24.61</td>
    <td class="tg-0lax">54.9</td>
    <td class="tg-0lax">109.16</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Sletting av operasjoner i **Prosjekt**-enheten støttes ikke.

Illustrasjonen nedenfor viser handlingen for utførelsestiden for enhetene **Oppgave**, **Tilordning**, **Teammedlem** og **Avhengighet** når 20, 50 og 100 oppføringer slettes.

![Graf for utførelsestid ved sletting av oppføringer.](./media/delete-record-execution-time.png)

## <a name="observations"></a>Observasjoner
For hver oppføringsoperasjon bruker API-en **ExecuteOperationSet** ca. 800 millisekunder på å sende en forespørsel til prosjektplanleggingstjenesten. Prosjektplanleggingstjenesten bruker deretter omtrent fem sekunder tiø å behandle nyttelasten og kalle opp Dataverse. Resten av utførelsestiden brukes til å kjøre forretningslogikk og skrive data til databasen i Dataverse.

Når 100 oppføringer er opprettet, oppdatert eller slettet, bruker API-en **ExecuteOperationSet** ca. tre sekunder på å sende forespørselen til prosjektplanleggingstjenesten. Prosjektplanleggingstjenesten bruker deretter omtrent fem sekunder til å behandle forespørslene og kalle opp Dataverse. Masseoperasjoner må betale en **engangsavgift for prosjektplanleggingstjenesten** for alle oppføringene i OperationSet. Derfor har masseoperasjoner betydelig lavere gjennomsnittlig utførelsestid enn operasjoner med enkeltoppføringer.

## <a name="scenarios"></a>Scenarioer
Tabellen nedenfor viser utførelsestidene når API-er for prosjektplaner brukes til å oppnå bestemte scenarioer. Tidene er i sekunder.

| Scenario                                                                   | Tid  |
|----------------------------------------------------------------------------|-------|
| Opprett et prosjekt med 40 oppgaver.                                      | 36.01 |
| Opprett et prosjekt med 40 oppgaver og 20 avhengigheter.                  | 38.11 |
| Opprett et prosjekt med 40 oppgaver og 30 tilordninger.                   | 60.17 |
| Opprett et prosjekt med 40 oppgaver, 20 avhengigheter og 30 tilordninger. | 60.27 |

## <a name="best-practices"></a>Anbefalte fremgangsmåter
Basert på scenarioresultatene ovenfor yter API-ene best under følgende forhold:

  - Grupper så mange operasjoner sammen som mulig. Gjennomsnittlig kjøretid for masseoperasjoner er bedre enn den gjennomsnittlige kjøretiden for operasjoner med enkeltoppføringer. Jo mindre antall OperationSets som er i bruk, jo raskere blir den gjennomsnittlige utførelsestiden.
  - Angi bare minimumsattributtene som kreves for å oppnå scenarioet. Vær selektiv angående typene ikke-obligatoriske felt som er inkludert i en OperationSet-forespørsel. Felter som inneholder sekundærnøkler eller felter for beregnet verdi, vil ha negativ innvirkning på ytelsen.
