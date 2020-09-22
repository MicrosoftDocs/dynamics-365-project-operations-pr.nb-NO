---
title: Bemanne prosjekter
description: Dette emnet gir informasjon om prosjektbemanning.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9352465f83abe19097945dd34eada365cd03b8f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754052"
---
# <a name="project-resourcing"></a>Bemanne prosjekter

[!include [banner](../includes/banner.md)]

Dette emnet gir informasjon om prosjektbemanning.

Én utfordring for prosjektledere og ressursansvarlige i løpet av planleggingen av prosjekt er ressursallokering, der de må fastsette og reservere den riktige ressursen til å arbeide med et prosjekt. I Dynamics 365 Finance kan bemanningsfunksjonene for prosjekter angi roller som behandles som midlertidige ressurser som kan reserveres for et bestemt engasjement eller del av et engasjement. Denne typen leverandør gjør det mulig for prosjektledere og ressursansvarlige å utføre følgende oppgaver:

- Definere en rolle som har de nødvendige kompetansene, slik at det blir enkelt å matche ressurser.
- Bruk roller til å definere en opprinnelig avtaletidsplan som er basert på reserverte ressurser.
- Beregn kostnader og bestem et opprinnelig budsjett basert på tilordnede roller og ressurser for et prosjekt.
- Bruk roller til å beregne antall ressursreservasjoner som kreves for hvert engasjement.
- Beregn antall ressurser som kreves for hele livssyklusen til et prosjekt.
- Lag utkast av en arbeidsnedbrytningsstruktur (WBS) ved å bruke de første ressurstilordningene.

[![Livssyklus for prosjekt](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

Etter hvert som prosjektplanleggingen fortsetter, kan planlagte ressurser erstattes med bemannede ressurser. Prosjektlederen kan også gå tilbake og oppdatere ressursreserveringene i løpet av et prosjekttrinn.

## <a name="set-up-project-resources"></a>Definere prosjektressurser
Du må sette opp en kalender og knytte den til en ansatt eller en arbeider. Kalenderen brukes til å planlegge prosjektet og arbeidstiden for ressursene som er reservert for prosjektet. Under kalenderinstallasjonen kan prosjektledere utføre ressursutjevning som en del av ressursoptimaliseringen. Restriksjoner kan brukes på ressurser basert på kalendertidsplanen. Du kan sette opp en kalender på **Kalenderere**-siden.

Når du definerer en arbeider som en prosjektressurs, kan du velge blant arbeidere som arbeider i firmaet som du konfigurerer ressurser for. Du kan også velge arbeidere fra andre selskaper i organisasjonen. Disse arbeiderne kalles konserninterne ressurser.

Fremgangsmåten nedenfor forklarer hvordan du konfigurerer en arbeider som en prosjektressurs i firmaet, og hvordan du oppretter en konsernintern prosjektressurs.

### <a name="set-up-a-worker-as-a-project-resource"></a>Konfigurere en arbeider som en prosjektressurs

1. På siden **Arbeidere** i listen **Arbeidere** velger du arbeideren som du legger til som prosjektressurs, og åpner arbeideroppføringen.
2. I handlingsruten velger du **Prosjekt** &gt; **Oppsett** &gt; **Prosjektoppsett**.
3. Velg en kalender, og lukk deretter siden.

Du kan også angi standardprosjekter for en ressurs som en type forhåndstilordning. Forhåndstildelinger kan brukes når ressurslederen eller prosjektlederen vet hvilke prosjekter ressursen skal jobbe med på forhånd. Forhåndstildelinger kan også være basert på forespørselen fra en prosjektsponsor eller kunde. Hvis du vil forhåndstilordne et prosjekt, velger du det gjeldende prosjektet på siden **Tilordne prosjekter** i kategorien **Prosjekter** på listen **Gjenværende prosjekter**.

### <a name="set-up-an-intercompany-resource"></a>Konfigurere en konsernintern ressurs

Når du definerer en arbeider som en konsernintern ressurs, må du fullføre oppsettet i både utlånsselskapet og lånefirmaet.

**I utlånsfirmaet**

1. Kontroller at utlånsfirmaet er valgt i Finance, og fullfør deretter fremgangsmåten i forrige del, "Konfigurere en arbeider som en prosjektressurs".
2. På siden **Konserninternt regnskap** velger du **Ny**.
3. I feltet **ID for juridisk enhet** velger du utlånsselskapet. Fyll ut de gjenværende feltene etter behov, og velg **Lagre**.
4. På siden **Overføringspris** velger du **Ny**.
5. I feltet **Juridisk enhet som låner** velger du riktig selskap.
6. Hvis du vil låne låneselskapet bare ressursen du opprettet i begynnelsen av denne delen, velger du navnet på ressursen du opprettet, i **Ressurs**-feltet. Hvis du vil gjøre alle ressursene i utlånsfirmaet tilgjengelige for lånefirmaet, lar du **Ressurs**-feltet stå tomt.
7. På siden **Parametere for prosjektstyring og regnskap**, i kategorien **Konsernintern**, setter du **Aktiver konsernintern ressursplanlegging og timeregistreringer** til **Ja**.

**I lånefirmaet**

- På siden **Ressursliste**, i søkefilteret, skriver du inn navnet på ressursen du opprettet for utlånsfirmaet, for å kontrollere at navnet er inkludert i ressurslisten for lånefirmaet.

## <a name="manage-resource-competencies"></a>Administrere ressurskompetanser
Ressurskompetanser er en viktig del av ressursbehandlingen. Kompetanser kan brukes som en basis for å avgjøre hvilke ressurser som har riktig balanse mellom ferdigheter, utdanning, sertifisering og prosjekterfaring. Du må angi denne informasjonen for hver ressurs og oppdatere den med jevne mellomrom. På denne måten kan du maksimere funksjonaliteten når bestemte ressurskompetanser samsvares under tildeling av prosjektressurser.

[![Eksempler på ferdigheter, sertifiseringer, utdanning og prosjekterfaring](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

Fremgangsmåtene nedenfor forklarer hvordan du konfigurerer noen av kompetansene for en ressurs.

Hvis du vil definere kompetanse for en arbeider, kan du bruke listesiden **Arbeidere** i Human resources eller **Ressurser**-listesiden i Prosjektstyring og regnskap. For fremgangsmåtene nedenfor brukes **Arbeidere**-listesiden i Human resources.

### <a name="set-up-competencies-certificates"></a>Konfigurere kompetanser: sertifikater

1. På listesiden **Arbeidere** velger du linjen for arbeideren du vil legge til sertifikatinformasjon for.
2. I handlingsruten i kategorien **Arbeider** i gruppen **Kompetanser** velger du **Sertifikater**.
3. Velg **Ny** og deretter, i feltet **Sertifikattype**, velger du **PMP**.
4. I feltet **Startdato** velger du **10/1/2015**, og deretter velger du **Lagre**.

### <a name="set-up-competencies-skills"></a>Konfigurere kompetanser: ferdigheter

1. På listesiden **Arbeidere** må du kontrollere at arbeideren du brukte i forrige prosedyre, fremdeles er valgt. Deretter, i handlingsruten i kategorien **Arbeider** i gruppen **Kompetanser**, velger du **Ferdigheter**.
2. Velg **Ny**.
3. I feltet **Ferdigheter** velger du **Prosjektledelse**.
4. I feltet **Nivå** velger du **5 Ekspert**.
5. I feltet **Nivådato** velger du **1-/14/2014**.
6. I feltet **År med erfaring** velger du **10**.
7. Velg **Lagre**, og lukk deretter siden.

## <a name="create-a-new-project"></a>Opprett et nytt prosjekt
1. På siden **Prosjektledelse** velger du **Nytt prosjekt**, og angi følgende verdier:

    - **Prosjekttype:** Tid og materiale
    - **Prosjektnavn:** XYZ-oppgraderingsfase 2
    - **Prosjektgruppe:** TM\_VIA
    - **Prosjektkontrakt-ID:** 00000002

2. Velg **Opprett prosjekt**.

### <a name="assign-a-resource-to-a-project"></a>Tilordne en ressurs til et prosjekt

1. På siden **Arbeidere** i listen **Arbeidere** velger du oppføringen for arbeideren som du tidligere konfigurerte kompentanser for, åpne arbeideroppføringen.
2. I handlingsruten i kategorien **Prosjekt** i gruppen **Oppsett** velger du **Tilordne prosjekter**.
3. På siden **Prosjekttilordninger for ressursvalidering** i kategorien **Prosjekt** i feltet **Legg til prosjekt i valgte prosjekter** filtrerer du på prosjektet **XYZ-oppgraderingsfase 2**.
4. I ruten **Gjenstående prosjekter** velger du et prosjekt, og deretter velger du pilknappen for å legge den til i ruten **Valgte prosjekter**.

Du kan også tilordne kategorier for en ressurs slik du ønsker. Kategoritypen er enten **Kostnad** eller **Omsetning**. Kategoritypen bestemmes av organisasjonen. Hvis ingen kategorier er tilordnet en ressurs, slår Finance opp standardkategorien på timepriser for kostnad og omsetning.

### <a name="set-up-project-resource-and-role-characteristics"></a>Konfigurere egenskaper for prosjektressurs og rolle

En prosjektleder kan bruke prosjektbemanningsfunksjonaliteten til å opprette rollene som kreves for prosjektet. Roller kan brukes hvis bekreftede ressurser fremdeles er ukjente når ressurser blir reservert. Roller kan være midlertidig reservert som planlagte ressurser, slik at du kan fortsette planleggingen av prosjektplanlegging.

[![Eksempel på en rolle](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenario:** Contoso ble engasjert for å fullføre et Tid og materiale-prosjekt som har et godkjent prosjektcharter. Juniorprosjektlederen holder fremdeles på med å ferdigstille prosjektomfanget. Ressurslederen identifiserer for øyeblikket bestemte ressurser som blir reservert for å arbeide med det nye prosjektet. På grunn av den kritiske prosjekttypen ba prosjektsponsoren om at den overordnede prosjektlederen kunne ha én av rollene. Ressurslederen må skaffe den nye ressursen og definere rollen i systemet i tilfelle juniorprosjektlederen krever ressursinformasjon under planleggingen av prosjektet.

Fremgangsmåten nedenfor viser hvordan ressurslederen kan konfigurere rollen som overordnet prosjektleder og knytte ressursegenskaper til den. Senere kan rollen brukes til å søke etter tilgjengelige ressurser som samsvarer med de nødvendige ressurskompetansene.

1. På siden **Konfigurer roller** velger du **Ny**, og angi følgende verdier:

    - **Rolle-ID:** Overordnet prosjektleder
    - **Beskrivelse:** Overordnet prosjektleder

2. Velg **Opprett**.
3. Velg rollen **Overordnet prosjektleder**, og velg deretter **Konfigurer egenskaper**.
4. I feltet for **Type kjennetegn** velger du **Ferdighet**.
5. I feltet **Tilgjengelige kjennetegn** angir du ferdigheten du vil søke etter.
6. I feltet for **Type kjennetegn** velger du **Sertifikat**.
7. I feltet **Tilgjengelige kjennetegn** angir du sertifikattypen du vil søke etter.

### <a name="assign-a-project-resource-to-a-project"></a>Tilordne en prosjektressurs til et prosjekt

1. På siden **Alle prosjekter** velger du **XYZ-oppgraderingsfase 2**-prosjektet.
2. I kategorien **Prosjektteam og planlegging** velger du **Legg til**.
3. I feltet **Rolle** velger du **Teammedlem**.
4. Velg **Bestill fra kalender**.
5. På siden **Ressurstilgjengelighet** velger du **Visningsinnstillinger**.
6. Angi følgende verdier på siden **Juster visningsinnstillinger**:

    - **Format for visning av datoområde:** Dag
    - **Vis tilgjengelighetsbeskrivelser:** Ja
    - **Vis gjenstående kapasitet:** Ja

7. Velg en ressurs fra listen over ressurser.
8. Velg **Forpliktende bestilling** og **Full kapasitet**.


### <a name="assign-a-resource-to-a-default-role"></a>Tilordne en ressurs til en standardrolle

For å hjelpe kan prosjekt- og ressursledere drille ned ytterligere på ressursene som kan reserveres for et prosjekt. Du kan knytte en standardrolle til en eksisterende ressurs eller en nylig innhentet ressurs. Når Daniel for eksempel ble leid inn, hadde han erfaringen og ferdighetene til å fylle rollen som forretningsanalytiker. Ressursbehandleren tilordnet denne rollen som Daniels standardrolle. Derfor har ressurslederen lagt til Daniel i en pulje av forretningsanalytikere som er tilgjengelige for å arbeide med prosjekter.

Under ressursreservasjon kan prosjektledere filtrere rolleressursene som er tilgjengelige for arbeid på prosjekter. De kan bruke denne informasjonen som ett vilkår når de utfører beslutningsanalyse med flere vilkår under ressursfullføring. De kan også legge til andre ressursegenskaper i filteret for å søke etter ressurser som har spesifikke ferdigheter, utdanning og erfaring for et gitt prosjekt.

**Scenario:** Et godkjent prosjekt har startet, og rollen overordnet prosjektleder er reservert som en planlagt ressurs i løpet av prosjektplanleggingsfasen. Ressursbehandleren har nå hentet en ressurs for å fullføre rollen overordnet prosjektleder.

1. På siden **Ressursliste** velger du **Daniel Goldschmidt**.
2. På siden **Ressursrolle** velger du **Ny**, og angi følgende verdier:

    - **Gyldig:** ngi gjeldende dato.
    - **Utløp:** Angi **Aldri**.
    - **Rolle-ID**: Angi **Overordnet prosjektleder**.

3. Velg **Lagre**, og lukk deretter siden.
4. I kategorien **Kompetanser** legger du til ferdigheten **ProjectMgmt** og sertifikatet **PMP**.

## <a name="set-up-role-based-pricing"></a>Konfigurere rollebaserte priser
Alle kostnader, salg og overføringspriser kan konfigureres for roller.

1. På siden **Salgspris (time)** velger du **Ny**, og angi deretter en ikrafttredelsesdato.
2. I kolonnen **Rolle** velger du en rolle.
3. I kolonnen **Priser** angir du en pris for den valgte ressursrollen.

## <a name="form-a-project-team"></a>Lag et prosjektteam
Hvis du vil bruke rollene som ble opprettet tidligere i et prosjekt, må en prosjektleder knytte rollene til prosjektet. Det kan tilordnes flere roller for et prosjekt. Disse rollene blir automatisk merket under reservering for å unngå forvirring. Hvis prosjektlederen for eksempel krever tre ingeniører, genereres det automatisk tre programvareingeniørroller som har **programvareingeniør 1**, **programvareingeniør 2** og **programvareingeniør 3** som etikett. Hvis rolleegenskaper er angitt tidligere for rollen, brukes de som et filter under søk etter en ressurs. Du kan legge til flere karakteristikker som kreves for å presisere søket ytterligere.

Visningsinnstillinger kan også tilpasses for å gi en bedre visning av ressurstilgjengelighet. Det finnes alternativer for å vise tilgjengelighet for time, dag, uke, måned, kvartal og år. Det finnes også et alternativ for å vise tilgjengelig og gjenstående kapasitet på ressurser. Dette alternativet er nyttig for tidsstyring når du beregner tilgjengelig tid for aktiviteter eller ressurstilgjengelighet.

Prosjektlederen kan velge en rolle på siden og deretter velge å reservere en ressurs som fyller rollen, hvis det er en tilgjengelig ressurs som passer til kravet. Vær oppmerksom på at ressursene ikke må reserveres på dette tidspunktet i planleggingsfasen. Når du oppretter en WBS, kan du erstatte roller med bemannede ressurser for prosjektet. Hvis roller erstattes med bemannede ressurser i WBS, oppdaterer ressursoppsettet automatisk prosjektgruppens liste og planlegging.

[![Prosjektteamoppføring som inkluderer både roller og faktiske ressurser](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Prosjektlederen har forskjellige alternativer for bestilling av en ressurs for et prosjekt, for eksempel **Gjenstående kapasitet**, **Full kapasitet**, **Kapasitet i prosent** og **Angi timer**. Disse bestillingsalternativene kan kanselleres når som helst hvis ressurstilordningene endres. To typer bestillinger støttes:

- **Forpliktende bestilling** – Ressursreservasjonen ble godkjent og bekreftet til å fungere på avtalene for den angitte varigheten.
- **Ikke-forpliktende bestilling** – Ressursreservasjonene ble foreløpig angitt til å fungere på avtalene for den angitte varigheten.

Fremgangsmåten nedenfor forklarer hvordan du oppretter et prosjektteam.

### <a name="create-a-project-team"></a>Opprette et prosjektteam

1. På listesiden **Alle prosjekter** velger du et prosjekt, og deretter velger du **Rediger**.
2. I kategorien **Prosjektteam og planlegging** i feltet **Planlegg sluttdato** angir du startdato pluss én måned. Hvis for eksempel startdatoen for tidsplanen er 24. juni 2017 (24/06/2017), angir du **24/07/2017**.
3. Velg **Legg til**.
4. I ruten **Legg til roller i prosjektet** i feltet **Rolle** velger du **Overordnet prosjektleder**.
5. Velg **Nødvendige kompetanser**.
6. På siden **Velg egenskaper** velges egenskapene som du tidligere har angitt for rollen overordnet prosjektleder, som standard. Velg **OK**.
7. På siden **Legg til roller i prosjektet**, i feltet **Antall ressurser**, angir du **1**.
8. I **Ressurs**-feltet viser oppslaget alle ressurser som har de nødvendige kompetansene. Velg **Daniel Goldschmid**, og velg deretter **Opprett**.
9. Velg **Legg til** på siden **Prosjekt**.
10. I ruten **Legg til roller i prosjektet** i feltet **Rolle** velger du **Teammedlem**. I feltet **Antall ressurser** angir du **5**.
11. Velg **Opprett**.
12. På siden **Prosjekter** velger du **Fullfør ressurs**.

## <a name="resource-capacity-synchronization"></a>Synkronisering av ressurskapasitet
Prosessene for hjelp for ressurssynkronisering garanterer at informasjon for kalenderen og basiskalenderen når frem til planleggingen av prosjektressurser. Hvis kalenderen endres, gjør prosessene de nødvendige oppdateringene for planleggingen av prosjektressurser. Prosessene bidrar også til å forbedre ytelsen fordi kalenderens ressursinformasjon er synkronisert på forhånd. Derfor skjer oppdatering av ressursplanleggingsinformasjonen raskere. Vi anbefaler at du planlegger prosessene som en bunke i stedet for én om gangen. Ellers er det en risiko for at noen vil glemme inklusivdatoene da informasjonen sist ble synkronisert. Hvis du ikke bruker noen datoer, kan det oppstå mellomrom under synkronisering av dato.

![Kalendersynkronisering](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Synkroniser opprullering av ressurskapasitet

Synkroniseringsprosessen er utformet for å synkronisere all ressurskalenderinformasjon. Denne informasjonen inkluderer informasjon om basiskalenderen for eventuelle endringer i prosjektets tabellkapasitet for ressurskalender. Hvis det legges til nye ressurser i prosjektet, bidrar synkroniseringen til å garantere at den oppdaterte kalenderinformasjonen er tilgjengelig. Denne synkroniseringen kan gjøres når som helst.

Vi anbefaler at du bruker en bunke. Alternativene er tilgjengelige under synkronisering av kapasitetsreservasjoner.

1. Velg **Prosjektstyring og regnskap** &gt; **Periodisk** &gt; **Kapasitetssynkronisering** &gt; **Synkroniser opprullering av ressurskapasitet**.
2. Angi alternativene i tabellen nedenfor.

    | Alternativ      | Beskrivelse |
    |-------------|-------------|
    | Periodekode | Du kan også velge datointervallkoden for økonomimodulen for å angi start- og sluttdatoene for synkroniseringsprosessen for opprullering av ressurskapasitet. |
    | Startdato  | Angi startdatoen for synkroniseringsprosessen for opprullering av ressurskapasitet. |
    | Sluttdato    | Angi sluttdatoen for synkroniseringsprosessen for opprullering av ressurskapasitet. |

[![Synkroniseringsfremdrift](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Konfigurere roller på WBS-maler
Prosjektledere kan konfigurere WBS-maler som de kan bruke når de oppretter en WBS for nye prosjekter. Prosjektledere kan legge til roller når de oppretter en mal. Bruk fremgangsmåten nedenfor for å tilordne en rolle til en WBS-mal.

1. Velg **Prosjektstyring og regnskap** &gt; **Oppsett** &gt; **Prosjekter** &gt; **Maler for arbeidsnedbrytningsstruktur**.
2. Velg **Detaljer** for en valgt WBS-mal.
3. Velg en oppgave i listen, og deretter, i feltet **Rolle**, velger du en rolle for å tilordne oppgaven.

### <a name="work-with-a-wbs"></a>Arbeide med en WBS

Du kan opprette en ny WBS, eller du kan kopiere en WBS fra en eksisterende WBS-mal. En prosjektleder kan enkelt administrere ressursene ved å tilordne roller til nye aktiviteter i WBS. Roller kan erstattes enten etter at en ressurs er anskaffet, eller etter at en bekreftet ressurs som skal arbeide på oppgaven, er identifisert. Denne fleksibiliteten gjør det mulig for prosjektledere å utføre følgende oppgaver:

- Identifiser antallet ressurser som kreves for WBS-arbeidspakker.
- Estimere prosjektkostnader.
- Fastslå et foreløpig budsjett.
- Estimer aktivitetsvarighet basert på roller og ressurser.
- Utvikle noen prosjektstyringsplaner basert på tilgjengelig prosjektinformasjon.

Det er lagt til flere alternativer i WBS for å bruke ressursfunksjonaliteten bedre.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Alternativ</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ressurstilordninger</td>
<td>Vis tildelte ressurser, datoer, antall timer og bestillingstype for aktiviteter i WBS.</td>
</tr>
<tr class="even">
<td>Generere team automatisk</td>
<td>Legg til planlagte ressurser automatisk ved hjelp av roller som er tilknyttet en oppgave. Finance foreslår automatisk planlagte ressurser ved hjelp av beslutningsanalyse med flere vilkår som er basert på roller. Når rollene og innsatsen (timer) er angitt for oppgavene i en WBS, og etter at strukturen er frigitt, velger du <strong>Generer team automatisk</strong>. Det nødvendige antallet planlagte ressurser blir lagt til i WBS og i kategorien <strong>Prosjektteam og planlegging</strong>.</td>
</tr>
<tr class="odd">
<td>Ressurs (rullegardinliste)</td>
<td>På siden <strong>Start ressurstilordning</strong> kan du velge ressurser du vil opprette forpliktende eller ikke-forpliktende bestilling for, basert på den angitte varigheten. Du kan justere visningsinnstillingene for å vise og angi varighet for ressursaktiviteter. Du kan velge og tilordne ressurser på arbeidspakkenivået ved å bruke følgende alternativer:
<ul>
<li><strong>Godta</strong> – Bekreft endringer av ressursen som er tilordnet til en aktivitet.</li>
<li><strong>Avbryt</strong> – Avbryt endringer av ressursen som er tilordnet til en aktivitet.</li>
<li><strong>Tilordne automatisk</strong> – En tilgjengelig bemannet ressurs som har en samsvarende rolle, blir automatisk valgt og tilordnet til den valgte aktiviteten.</li>
</ul></td>
</tr>
</tbody>
</table>

1. På siden **Alle prosjekter** velger du **XYZ-oppgraderingsfase 2**-prosjektet.
2. Velg **Plan** &gt; **Aktiviteter** &gt; **Arbeidsnedbrytningsstruktur**.
3. Velg **Ny** for å legge til følgende nivå én-aktiviteter i WBS:

    - Starter
    - Planlegging
    - Kjører
    - Overvåking og kontroll
    - Lukk

4. Angi datoer og innsats (timer), som vist i illustrasjonen nedenfor.

    [![Angi datoer og innsats](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Velg oppgavelinjen **Innledende**, og deretter, i feltet **Rolle**, velger du **Overordnet prosjektleder**.
6. Velg **Publiser**.
7. På samme linje, i feltet **Ressurs**, velger du **Daniel Goldschmidt**, og deretter velger du **Godta**.
8. Velg oppgavelinjen **Planlegging**, og deretter, i feltet **Rolle**, velger du **Forretningsanalytiker**.
9. Velg **Publiser**, og velg deretter **Generere team automatisk**.
10. Velg **Ja** i meldingsboksen som vises.
11. I feltet **Ressurser** kontrollerer du at verdien er **Forretningsanalytiker 1**.
12. For ressursen **Forretningsanalytiker 1** åpner du oppslaget og velger **Start ressurstilordninger**. Velg deretter en arbeider for oppgaven.
13. Velg **Tilordne uforpliktende** &gt; **Full kapasitet**.

    > [!NOTE] 
    > Du får ingen advarsel om at den angitte ressursen nå er 2, fordi antallet ressurser forblir 1.

14. På siden **Arbeidsnedbrytningsstruktur** validerer du ressurstilordningen på WBS, og deretter velger du **Lagre**.

## <a name="resource-fulfillment-for-planned-resources"></a>Ressursfullføring for planlagte ressurser
En prosjektleder kan planlegge nødvendige ressursroller for et prosjekt. Ressursansvarlig vil se disse planlagte ressursene som forespørsler på siden **Ressursfullføring** og kan tilordne faktiske ressurser.

1. På siden **Alle prosjekter** velger du **XYZ-oppgraderingsfase 2**-prosjektet.
2. Velg **Prosjekt**, og velg deretter **Rediger**.
3. I kategorien **Prosjektteam og planlegging** velger du **Legg til**.
4. I dialogboksen **Legg til roller** velger du rollen **Programvareutvikler**.
5. Velg **Opprett**, og lukk deretter prosjektsiden.
6. På siden **Ressursfullføring** velger **Programvareutvikler 1** for prosjektet **XYZ-oppgraderingsprosjekt fase 2**-prosjektet.
7. Velg en arbeider, og velg deretter **Tilordne**.
8. Kontroller at linjen for **Programvareutvikler 1** er fjernet for **XYZ-oppgraderingsprosjekt fase 2**-prosjektet.
9. I kategorien **Prosjektteam og planlegging** for prosjektet **XYZ-oppgraderingsfase 2** kontrollerer du at arbeideren du valgte i forrige trinn, er lagt til som **Programvareutvikler**.

## <a name="requests-for-project-resources"></a>Forespørsler om prosjektressurser
Funksjonaliteten for planlegging av prosjektressurser gjør det bare for ressursledere å distribuere bemannede ressurser på engasjementer eller prosjekter. Hvis du vil aktivere denne funksjonaliteten, må du utføre følgende oppgaver eller kontrollere at de er fullført:

- Angi nummerserier.
- Konfigurere prosjektstyrings- og regnskapsflyter.
- Aktivere ressursforespørselsflyter.

Når de foregående oppgavene er fullført, kan du utføre følgende oppgaver slik du ønsker:

- Opprett en ressursforespørsel fra en uforpliktende bemannet ressurs.
- Overvåk ressursforespørsler.
- Oppfyll ressursforespørsler.
- Be om en bemannet ressurs fra en WBS.
- Reserver ressurser til et prosjekt uten å ha en forespørsel om en bemannet ressurs.

## <a name="monitor-project-teams"></a>Overvåke prosjektteam
1. På siden **Alle prosjekter** velger du koblingen **Prosjekt-ID** for prosjektet **XYZ-oppgraderingsfase 2**.
2. På hurtigfanen **Prosjektteam og planlegging** kontrollerer du at prosjektressursene som vises, er riktige.
