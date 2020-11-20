---
title: Hva er nytt eller endret i Project Service Automation versjon 3
description: Dette emnet gir informasjon om hva som er nytt og endret i Project Service Automation versjon 3.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 46cbbc3ff3b0efcecd3cba30b265a782f6cdcf60
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120015"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3"></a>Hva er nytt eller endret i Project Service Automation versjon 3
[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Dette emnet gir informasjon om endringene i brukergrensesnitt (UI), funksjonalitet og terminologi i Project Service Automation mellom versjon 2 eller versjon 1 og versjon 3.

## <a name="project-scheduling"></a>Prosjektplanlegging
Prosjektplanen, som ble kalt arbeidsnedbrytningsstruktur (WBS) i tidligere versjoner, har nå fått navnet Tidsplan og åpnes ved å klikke på kategorien **Tidsplan**. 

![Prosjekttidsplan](media/psa-schedule-01.png)

Tidsplanen har nå en ny overflate for samhandling som er både moderne og tilgjengelig. Den underliggende planleggingsmotoren for Project Service Automation er ikke endret. Kontrollknappene i tidsplanrutenettets bånd gjør det mulig å samhandle med tidsplanen på lignende måte som i forrige versjon av Project Service Automation. Flere endringer i tidsplanen omfatter:

- **Gantt-diagram** – Gantt-diagrammet finnes ikke lenger. En ny Gantt-visualisering vil returnere i en fremtidig oppdatering.
- **Kolonneoverskrifter** – Du kan skjule kolonneoverskrifter i rutenettet ved å klikke på pil ned ved siden av kolonnetittelen. 
- **Kolonner** – Du kan vise skjulte kolonner ved å klikke **Legg til kolonne**. 
- **Transaksjonskategori** – Et **Transaksjonskategori**-oppslag er lagt til i tidsplanrutenettet og vises som standard. 
 
## <a name="project-templates"></a>Prosjektmaler
Følgende endringer er gjort i prosjektmalfunksjonen.

### <a name="create-a-project-template"></a>Opprette en prosjektmal 
Du kan opprette en prosjektmal i versjon 3 som ligner på forrige versjoner av Project Service Automation. Malen kan bare inneholde en tidsplan, og tidsplanen kan inneholde tilordninger, men de er ikke nødvendige. Hvis tidsplanen ikke har tilordninger, kan de bare være for generelle ressurser. Du kan generere ressurskrav for generelle ressurser, men de kan ikke reserveres med faktiske ressurser i malen. Du kan ikke reservere en faktisk ressurs til et team i en mal. 

### <a name="create-a-template-from-an-existing-template"></a>Opprette en mal fra en eksisterende mal
Når du oppretter en ny prosjektmal fra en eksisterende mal i Project Service Automation versjon 3, skjer følgende: 

- Tidsplanen for kildeprosjektet kopieres til malen. 
- Generelle ressurser kopieres til teamet, og eventuelle generiske ressurstilordninger kopieres over. Krav for de generelle ressursene blir ikke kopiert over. 

### <a name="create-a-template-from-an-existing-project"></a>Opprette en mal fra et eksisterende prosjekt
Når du oppretter en ny prosjektmal fra et eksisterende prosjekt, skjer følgende: 

- Tidsplanen for kildeprosjektet kopieres til malen. 
- Generelle ressurser kopieres til teamet, og eventuelle generiske ressurstilordninger beholdes. Krav for de generelle ressursene blir ikke kopiert over.    
- Navngitte ressurser, både tilordnede eller ikke tilordnede, blir fjernet fra teamet og erstattet med generelle ressurser.
- Eventuell kundeinformasjon fjernes. 
- Eventuelle referanser til tilbud og kontrakter fjernes. 

### <a name="create-a-project-from-a-template"></a>Opprette et prosjekt fra en mal
Når du oppretter et nytt prosjekt fra en mal i Project Service Automation versjon 3, skjer følgende:

- Tidsplanen, teamet og tilordningene kopieres til det nye prosjektet.   
- Startdatoen er enten kopieringsdato eller en dato brukeren har valgt.   
- For alle generiske teammedlemmer med ressurskrav i malen blir ikke kravene kopierte eller genererte automatisk. Du må generere dem. 

## <a name="copy-a-project"></a>Kopiere et prosjekt
Når du kopierer et prosjekt i Project Service Automation versjon 3, skjer følgende: 

- Beregnet startdato kopieres, men kan endres.  
- Prosjektplanen og oppgavene kopieres. 
- Generelle ressurser og deres tilordninger kopieres. Ressurskrav for de generelle ressursene blir ikke kopiert over. Du må generere dem på nytt. 
- Faktiske ressurser og deres tilordninger kopieres ikke. I stedet erstattes de av generelle ressurser. 
- Faktiske verdier kopieres ikke til det nye prosjektet. 

## <a name="move-a-scheduled-project"></a>Flytte et planlagt prosjekt
Når du flytter tidsplanen for eksisterende prosjekt fremover, skjer følgende: 

- Oppgavedatoer flyttes automatisk slik at de samsvarer med bevegelsesperioden. 
- Tilordnede generiske ressurser forblir tilordnet.   
- Hvis de genereres før prosjektet flyttes, forblir krav for den generelle ressursen uendret, og de genereres ikke automatisk på nytt. Du må generere dem på nytt for å gjenspeile de nye tilordningene på grunn av oppgaveflytting. 
- Tilordninger for faktiske ressurser endres til å stemme overens med flytting av oppgavedato. Bestillinger på faktiske ressurser endres ikke. Du må endre bestillinger ved hjelp av avstemmingsvisningen. 
- Teamressurser med bestillinger, men ingen tilordninger, endres ikke. 
- Faktiske verdier flytter ikke. 

## <a name="estimates"></a>Estimater
Estimater er delt inn i to kategorier, **Ressurstilordninger** og **Estimater**. Kategorien **Ressurstilordning** inneholder innsatsestimater og viser ressurstilordningene for oppgavene i en tidsinndelt visning. Du kan redigere estimatene basert på hva planleggingsmotoren har generert.

![Kategorien Ressurstilordninger med arbeidsestimater og ressurstilordninger for oppgaver](media/resource-assignments-tab-02.png)

Kategorien **Estimater** viser kostnadene og salgsbeløpene for ressurstilordningene. Beløpene er skrivebeskyttet. Kostnadene og salgsprisen er nå drevet fra teammedlemstilordningene i tidsplanen. Det betyr at hvis du har en oppgave uten noen tilordning, vil oppgaven vises under den ikke-tilordnede samlingen. Dette betyr også at uten **rolle**, som er en standard prisdimensjon, vil det ikke finnes beregnet kostnad eller salg hvis du har en kunde eller en kontrakt/tilbud knyttet til prosjektet. 

![Kategorien Estimater med kostnads- og salgsbeløp](media/estimates-tab-03.png)
  
Kategorien støttes også på aktiviteter i planleggingsvisningen. Gruppering etter kategori i den tidsinndelte visningen av estimater gir en bedre opplevelse, spesielt når du også har utgiftsberegninger i prosjektet. Utgiftsestimater angis ved hjelp av et rutenett i en egen kategori. 

Utgiftsestimater kan angis i rutenettet i kategorien **Utgiftsestimater**. 

![Kategorien utgiftsestimater som viser rutenettet for utgiftsestimater](media/expense-estimates-tab-04.png)

## <a name="resource-management"></a>Ressursbehandling
Ved hjelp av det nye enhetlige klientgrensesnittet i Project Service Automation versjon 3 og endringer i relasjonen mellom bestillinger og tilordninger, har bemanning av generelle og faktiske ressurser på et prosjekt blitt endret seg svært mye fra versjon 2 og versjon 1. Begrepene for ressurser som kan bestilles, både **faktiske** og **generelle**, er imidlertid de samme, som også gjelder for teammedlemmer, krav, tilordninger og bestillinger.   

![Bruke ressursvelgeren](media/resource-management-05.png)

### <a name="assign-a-real-bookable-resource"></a>Tilordne en faktisk ressurs som kan bestilles 
I Project Service Automation versjon 3 er ikke bestillinger og oppgavetilordninger like tett sammenkoblet som i tidligere versjoner av Project Service Automation. Du kan bruke grupperutenettet til å bestille et **faktisk** teammedlem, på samme måte som i markedet.

Ved hjelp av ressursvelgeren i tidsplanen kan du velge teammedlemmet som opprettes i teamvisningen, og deretter tilordne det til oppgaver. Du kan fortsette å tilordne oppgaver til dem, til og med etter bestillingene. Bruk kategorien **Avstemming** til å avstemme teammedlemmer som har forskjeller i bestillinger og tilordninger.

Ressursvelgeren viser teammedlemmene for prosjektet. Du kan også bruke ressursvelgeren til å søke etter og vise andre bestillbare ressurser som ikke er en del av prosjektteamet. Du kan tilordne dem til en oppgave, og de blir en del av prosjektteamet. Du må bestille dem ved å bruke kategorien **Planleggingstavle** eller **Avstemming**.

### <a name="assign-a-generic-bookable-resource-on-a-task-and-project-team-and-then-fulfill-with-a-real-resource-via-schedule-board"></a>Tilordne en generell ressurs som kan reserveres, til en oppgave og et prosjektteam, og oppfyll deretter med en faktisk ressurs via planleggingstavlen 
I Project Service Automation versjon 3 brukes ikke funksjonen for generer team for generelle ressurser. I stedet kan du opprette og direkte tilordne en generell ressurs fra tidsplanen ved å skrive inn posisjonsnavnet til den generelle ressursen i ressurscellen til tidsplanen. Du kan velge ressursikonet i cellen og deretter, ved å hjelp av ressursvelgeren, skrive inn navnet på den generelle ressursen du vil opprette. Dette åpner et hurtigopprettingspanel som gjør det mulig å angi rolle- og organisasjonsenhet for det generelle ressursteammedlemmet. Når du har opprettet ressursen, blir den tilordnet til oppgaven, og du kan fortsette å tilordne den generelle ressursen til andre oppgaver i tidsplanen.    
 
Når du har tildelt ressursen til alle de riktige oppgavene, kan du generere et ressurskrav og deretter oppfylle det ved å bestille det direkte via **Planleggingstavle** eller ved å sende inn en ressursforespørsel. Du kan også legge til generelle ressurser direkte i gruppemedlemsrutenettet. 

Generelle ressurser blir lagt til i prosjektteamet uten ressurskrav og med start- og sluttdatoene for prosjektet før ressurskrav genereres. Hvis du vil generere et krav, velger du den generelle ressursen og klikker **Generer**. Kravkoblingen vises nå, og de nødvendige timene fylles ut med de tildelte timene. Du kan klikke koblingen for å åpne og oppdatere kravet.
  
Når bestillingen er fullført og fullstendig oppfylt med en navngitt ressurs, erstattes den generelle ressursen med den navngitte ressursen, og tilordningen i tidsplanen oppdateres med den navngitte ressursen. 

Foreslåtte ressurser for krav lagres nå i en kategori i stedet for en egen del.

### <a name="multiple-named-resources-fulfilling-a-generic-resource"></a>Flere navngitte ressurser oppfyller en generell ressurs
Når et krav oppfylles med flere ressurser, beholdes den generelle ressursen i teamet og tildeles oppgaven. De navngitte teammedlemmene som er bestilt, blir ikke tilordnet som en del av stillingen. Prosjektlederen kan tilordne arbeidet etter behov til de faktiske ressursene.  Visningen **Avstemming** viser en oppdeling av bestillingene på tvers av flere ressurser i mange oppgavetildelinger. Dette gjøres ikke automatisk, fordi i mange kompliserte scenarioer, for eksempel der du har en gruppe oppgaver som utgjør kravet, må intensjonen av hvordan prosjektlederen vil tilordne, antas. Siden systemet ikke kan forstå hensikt, er det sannsynlig at antakelsene vil være forskjellige fra tiltenkt, og det skjer et uriktig eller uforutsigbart resultat. Det forutsigbare resultatet er at den generelle ressursen holdes tilordnet til prosjektlederen med hensikt tildeler ressurser med **Avstemming**-visningen.

### <a name="reconciliation"></a>Avstemming
Kategorien **Avstemming** viser bestillinger og alle tilordninger for hvert prosjektgruppemedlem. Visningen viser timer i celler som kan representere tidspunkter fra måneder til dager. Med denne visninger kan prosjektledere avstemme teammedlemsbestillinger og deres tilordninger for prosjektteamet. Dette er nyttig fordi bestillinger og oppgavetildelinger ikke er tett koblet sammen, noe som gir mer fleksibilitet under planlegging av et prosjekt. 

![Kategorien Avstemming med bestillinger og tilordninger for prosjektteammedlemmer](media/resource-reconciliation-tab-06.png)

For hver ressurs bruker visningen forskjellen mellom et teammedlems bestillinger og en beregnet verdi av oppgavetilordningene og viser følgende to forskjeller som kan oppstå med bestillinger og tildelinger i et prosjekt: 

- **Få bestillinger** – Få bestillinger inntreffer når en ressurs har flere tildelinger enn bestillinger. Ettersom denne kapasiteten ikke er reservert, kan det hende at en prosjektleder kan korrigere dette ved å utvide ressursens bestillinger for å dekke underskuddet. 
- **Overflødige bestillinger** – Overflødige bestillinger skjer når en ressurs er bestilt til prosjektet, men ikke er tilordnet til aktiviteter.  Denne tilstanden kan være akseptabel, for eksempel hvis ressursen er bestilt før oppgavetilordning. I andre tilfeller kan det imidlertid hende at ressursen ikke planlegges å være tilordnet, og prosjektlederen bør vurdere å annullere ressursens bestillinger for å tillate at kapasiteten kan brukes på et annet prosjekt. 

Når du har oppgavetildelinger for en ressurs uten bestillinger (en bestillingsmangel), kan du velge den samlede bestillingsmangelen og klikke **Utvid bestilling**. Herfra kan du vise bestillingen som er nødvendig for å løse ressursens manko og tilgjengeligheten. 
 
## <a name="time-and-expense"></a>Tid og utgift
Denne delen inneholder informasjon om endringer i tid, utgift og godkjenning i versjon 3 av Project Service Automation. Som en del av Dynamics 365 Project Service Automation-løsningen er funksjonen **Tidsoppføring** oppdatert til å dra nytte av Enhetlig grensesnitt-rammeverket. Dette gjør det mulig å levere et ensartet og gjennomført brukergrensesnitt som følger responsiv utforming på best mulig måte for optimal visning på alle skjermstørrelser og enheter. 

### <a name="landing-page"></a>Målside
Den ikke-utvidbare opplevelsen av egendefinert tidsoppføring er avskrevet i versjon 3. I stedet finnes det nå en utvidbar og tilgjengelig innebygd rutenettopplevelse. Du kan få tilgang til tidsoppføringsfunksjonaliteten ved å bruke områdekartet til venstre. Ved hjelp av denne endringen kan du ikke lenger angi tid for én uke om gangen. I stedet må du opprette en tidsoppføring for hver dag i rutenettet. Når det er opprettet noen få tidsoppføringer, kan brukere masseopprette tidsoppføringer med **Kopier**-funksjonen som forklares senere i dette emnet. 

![Landingsside for tidsoppføringer](media/time-entry-landing-page-07.png)
 
### <a name="create-new-time-entries"></a>Opprette nye tidsoppføringer 
Klikk **Ny** på båndet for å åpne en hurtigopprettingsside for tidsoppføring der du angir varighet i minutter, timer eller dager. Dette gjør du ved å bare begynne å skrive h, m eller d sammen med antallet.  

![Hurtigoppretting for tidsoppføring](media/quick-create-time-entry-08.png)

Oppslagsfelt blir støttet av systemvisninger. Når du for eksempel har angitt prosjektinformasjon, blir **Prosjektoppgave**-feltet angitt som standard til **Mine åpne prosjektoppgaver**. Hvis du vil opprette tidsoppføringer for oppgaver som ikke er tilordnet brukeren, klikker du **Endre visning** på oppslaget og velger **Alle aktive prosjektoppgaver**. Når tidsoppføringen er opprettet og vises i rutenettet, kan du redigere eventuelle linjeverdier direkte i rutenettet.  

### <a name="bulk-createcopy"></a>Masseopprette/-kopiere 
Etter at du har opprettet noen få oppføringer, kan du bruke kopieringsfunksjonaliteten til å opprette flere tidsoppføringer samtidig. Klikk **Kopier** for å åpne **Kopier**-dialogboksen. I **Fra-periode: Startdato**, angi datointervallet som tidsperiodene skal kopieres fra. I **Til-periode: Startdato** angir du datoen tidsoppføringer må opprettes. Klikk **Kopier** for å kopiere tidsoppføringene til den tilsvarende dagen i uken som er angitt i **Til-perioden**. Mandagens tidsoppføring fra forrige uke blir for eksempel kopiert til mandag for uken som er angitt i **Til-periode**. 

![Massekopiere tidsoppføringer](media/bulk-copy-time-entry-09.png)
 
### <a name="import-data"></a>Importer data 
Tilordninger og utveksling følger samme grensesnittmønster, noe som gjør det mulig for brukeren å angi datointervallet fra når bestillinger må importeres. Deretter må du eksplisitt velge bestillingene som må kopieres til **Utkast**-tidsoppføringer. I versjon 3 kan du ikke lenger se mønsteret for **Foreslått**-tidsoppføringer i rutenettet og kalenderen.  

### <a name="change-in-calendar-control"></a>Endre i kalenderkontroll
I versjon 3 har vi flyttet bort fra den egendefinerte kalenderkontrollen, og vi bruker nå UC-kalenderen til å vise tidsoppføringer for uken. Ved hjelp av denne kalenderen kan du vise dag, uke og måned. 

> [!NOTE]
> En begrensning på kalenderen er at denne kontrollen ikke støtter handlinger for individuelle kalenderelementer. Du kan for eksempel ikke velge ett eller flere kalenderelementer og sende eller slette disse elementene. Hvis du klikker på et kalenderelement, åpnes siden for **tidsoppføringsenhet** for flere handlinger. 

### <a name="extensibility"></a>Utvidbarhet
**Hent data bare i egendefinerte felt i tids- og utgiftsregistreringsenheter** – Tidsoppføring bruker et redigerbart rutenett, et skrivebeskyttet rutenett og kalenderkontroller fra plattformen. Alle disse kontrollene er innebygde og støtter derfor tilpassinger. I Project Service Automation versjon 3 kan du legge til flere egendefinerte felt, sette opp oppslagsfelt og ta sikkerhetskopi av dem med egendefinerte visninger. Du kan også angi egendefinert forretningslogikk basert på valgte verdier i egendefinerte felt.  

**Hent data i egendefinerte felt i tids- og utgiftsoppføring, og overfør dem via enheter som støtter innsendings- og godkjenningsflyten** – Typisk behandling av tidsoppføringer vises i diagrammet nedenfor.

![Behandling av tidsoppføringsflyt](media/process-time-entries-10.png)

Hvis forretningskrav stipulerer at tids- og utgiftsenheter må registrere egendefinerte prisdimensjoner og overføre verdiene som angis av en tids- og oppføringsressurs i den egendefinerte prisingsdimensjonen, via alle enhetene i den forrige grafikken, se [Konfigurere egendefinerte felt som prisdimensjoner](set-up-pricing-dimensions.md)

Hvis du vil støtte forretningskrav der tids- og utgiftsenheter må fange opp egendefinerte ikke-prisdimensjoner og overføre verdiene, kan du bruke oppsettet for prisdimensjoner og uttrykke de egendefinerte dimensjonene som prisdimensjoner uten kostnads- eller fakturasats. Et annet scenario vil være å legge til et egendefinert felt for hver enhet ved å bruke det samme feltnavnet på tvers av alle enheter. Egendefinerte plugin-moduler kan opprettes for å relatere oppføringer i enhetene som deltar i innsendings- og godkjenningsflyten, ved hjelp av enhetene for transaksjonsopprinnelse og transaksjonstilkobling.  

### <a name="delegate-time-and-expense-entry"></a>Delegere tids- og utgiftsoppføringer
Common Data Service-plattformen støtter ikke at én bruker representerer en annen bruker, noe som betyr at det i versjon 3 av Project Service Automation ikke er støtte for delegert tids- og utgiftsoppføring. Partnere og kunder har imidlertid tatt i bruk en løsning for å aktivere støtte for delegerte tidsoppføringsopplevelser i versjon 3. Dette er bare en omgåelse og ikke en fullstendig løsning, så det er viktig å forstå begrensningene og bare bruke denne metoden hvis begrensningene er akseptable. 

> [!IMPORTANT]
> Denne informasjonen bør bare betraktes som foreslått veiledning for tilpasset implementering av en partner/kunde. Produktteamet vil ikke tilby formell støtte for denne funksjonaliteten via noen av kundestøttekanalene våre.

### <a name="customization-details"></a>Tilpassingsdetaljer 
Tilpassing gjør det mulig å legge til **Ressurs som kan reserveres** for å opprette og redigere erfaringer, noe som gjør det mulig for en bruker å arbeide som representant ved å endre feltet **Ressursbestilling** til en annen bruker som tids- og utgiftsoppføringer må registreres for. Fremgangsmåten nedenfor viser tidsoppføringsdelegering. Den samme informasjonen gjelder for utgiftsoppføringsdelegering. 
 
1.  Kontroller at den delegerte brukeren har global sikkerhetstilgang for prosjekter og prosjektoppgaver. 
1.  Siden **Ressurs som kan reserveres**, som er et felt i enheten **Tidsoppføring**, ikke vises på siden **Hurtigoppføring**, må du legge den til.

    -eller-

    Opprett en egendefinert visning som inkluderer kolonnen **Ressurs som kan reserveres**, for å vise bare tidsoppføringer som er opprettet for ressursen. Publiser tilpassingene i appmodulutformingen, slik at denne visningen vises under **Visningsvelger** på siden **Tidsoppføringer**. Det finnes to plugin-moduler som håndterer angivelse av overordnet for tidsoppføringer som ikke er relatert til et prosjekt:

    - PreValidateTimeEntryCreate
    - PreValidateTimeEntryUpdate
 
1. Opprett en ny plugin-modul for å overskrive **Overordnet**-feltet til den overordnede til brukeren som er tilordnet i feltet **Ressurs som kan reserveres**. Bruk samme **Utføringsfase** som out-of-band-plugin-modulen (OOB), og bruk en **Utføringsrekkefølge** som er høyere enn OOB-plugin-modulene (større enn 1). Dette sikrer at den tilpassede plugin-modulen utføres etter OOB-plugin-modulene.  
 
### <a name="end-user-experience"></a>Sluttbrukeropplevelse
1.  Når du oppretter en tidsoppføring på hurtigopprettingssiden, angir du prosjekt- og prosjektoppgavedetaljene, og deretter velger du brukeren i feltet **Ressurs som kan reserveres** som tidsoppføringene må registreres for. 
2.  Dette feltet går som standard til den påloggede brukeren, men siden brukeren overstyrte dette feltet, opprettes det nå en tidsoppføring for valgt **Ressurs som kan reserveres**.
3.  Når du sender tidsoppføringene du har opprettet for disse oppføringene, blir oppføringene satt opp i kø for godkjenneren i prosjektet som forventet. 
4.  Når du tilbakekaller tidsoppføringer som er opprettet for den andre brukeren, returneres tidsoppføringene til tilstanden **Utkast** med feltet **Ressurs som kan reserveres** angitt til den andre brukeren. 
5.  Du kan eventuelt bytte til den egendefinerte visningen for å filtrere tidsoppføringer som er opprettet for den andre brukeren. 
 
### <a name="limitations"></a>Begrensninger
**Kopier**- og **Importer**-funksjonene fungerer bare i konteksten til brukeren som er logget på. Dette betyr at det ikke er mulig å kopiere eller importere tidsoppføringer som er opprettet for brukeren som er logget på som ressursen som kan reserveres.

Tidsoppføringer som ikke er for et prosjekt, blir bare distribuert til godkjenning til lederen for reserverbar ressurs hvis trinn 4 i delen **Tilpassingsdetaljer** over er fullført. Hvis ikke blir ikke tidsoppføringer for den andre brukeren som ikke er relatert til prosjektet, rutet riktig til den overordnede for den påloggede brukeren. 

### <a name="other-changes"></a>Andre endringer 
Funksjonaliteten **Bestillinger og oppgaver** er fjernet. 

## <a name="multidimensional-pricing"></a>Flerdimensjonale priser
For å oppnå maksimal fleksibilitet og oppfylle forskjellige forretningsbehov støtter versjon 3 av Project Service Automation diskret bruk av prisdimensjonssett på kostnads- og fakturasatser. Du kan angi dimensjonsverdier som standard og deretter overføre dem til hele kostnads- og prissettingsprosessen fra ressursprofilering til tidsoppføring til faktiske prosjektdata. Kundespesifikk konfigurasjon og endring eller utvidelse benytter standard infrastruktur som kan tilpasses.

Project Service Automation leveres med et standard sett med prisdimensjoner og roller og ressursenheter og gjør det mulig å definere priser og kostnader for hver rolle- og organisasjonsenhetskombinasjon.

For kunder av Project Service Automation som vil fortsette å bruke disse standardfeltene som prisdimensjoner i versjon 3, vil det ikke være noen observerbar endring. Du kan fortsette å bruke Project Service Automation på vanlig måte. Hvis du imidlertid må ha pris eller kostnad for ressursene ved hjelp av andre tilleggsattributter, kan du i versjon 3 legge til egendefinerte prisdimensjoner i Project Service Automation. Utvidelse av egendefinerte prisdimensjoner er en komplisert konfigurasjonsopplevelse. 

## <a name="quotes-and-contracts"></a>Tilbud og kontrakter
I versjon 3 av Project Service Automation er aspekter av oppsett og administrasjon for tilbud og kontrakter endret. Avsnittene nedenfor inneholder mer detaljert informasjon.

### <a name="set-up-chargeability-options"></a>Definere alternativer for belastbarhet
I versjon 1 og 2 ble det utført oppsett for belastbarhet for roller og kategorier for bestemte tilbud og kontrakter ved hjelp visningen for **Belastbarhet**, som var øverst i navigasjonen i en tilbudslinje eller kontraktslinje. Dette var også der du kunne sette opp priser for disse rollene og utgiftskategoriene.

Fra og med versjon 3 utføres oppsett av belastbarhetsalternativer etter rolle og utgiftskategori på tilbuds- eller kontraktlinjenivå. Prisoppsett er atskilt fra belastbarhetsoppsett. Du finner **Belastbare roller** og **Belastbare kategorier** som kategorier på sidene **Tilbudslinje** og **Kontraktlinje** uten å måtte bruke toppnavigasjonen.

![Belastbare roller](media/chargeable-12.png)
 
Oppsettet av belastbare roller og belastbare kategorier benytter også den redigerbare rutenettkontrollen, som er standard. For hver rolle og kategori forblir de støttede alternativene for faktureringstype i tilbuds- og kontraktfasen uendret, som **Belastbar** og **Ikke-belastbar**, fra tidligere versjoner. **Gratis** støttes ikke under tilbuds- eller kontraktfasen. **Gratis** støttes bare i tids- eller utgiftsgodkjenningen.  
 
### <a name="create-and-edit-custom-pricing-for-a-project-service-automation-quote-and-project-contract"></a>Opprette og redigere egendefinerte priser for et Project Service Automation-tilbud og en prosjektkontrakt
I versjon 1 og 2 ble det brukt egendefinert prisliste for bestemte tilbud og kontrakter ved hjelp av **Rediger priser** i visningen **Belastbarhet**. Visningen **Belastbarhet** var plassert øverst i navigasjonen i en tilbudslinje eller kontraktslinje. Det var også der du kunne sette opp alternativene for belastbarhet for roller eller utgiftskategorier.

Fra og med versjon 3 er opprettelse og bruk av en egendefinert prosjektprisliste i et Project Service Automation-tilbud og en Project Service Automation-prosjektkontrakt atskilt fra belastbarhetsoppsettet. Project Service Automation-tilbud for Project Service Automation-prosjektkontrakter har en ny kategori kalt **Prosjektprislister**. Denne kategorien viser en tilknyttet visning av alle prosjektprislister som er knyttet til Project Service Automation-tilbudet eller prosjektkontrakten. Hvis du vil opprette en egendefinert prisliste fra en eksisterende prisliste som allerede er knyttet til prosjekttilbudet eller kontrakten, klikker du **Opprett egendefinert prising**. Dette tar en kopi av alle de tilknyttede prislistene og knytter dem til tilbudet eller kontrakten. Du kan nå åpne prislisten og redigere rollen eller utgiftskategoriprisen, slik at disse prisendringene bare gjelder for dette tilbudet eller denne kontrakten. 
  
Følgende grafikk er før egendefinerte prislister er opprettet.

![Før egendefinerte prislister](media/before-custom-price-lists-13.png)

Følgende grafikk er etter egendefinerte prislister er opprettet.

![Etter egendefinerte prislister](media/after-custom-price-lists-14.png)

> [!NOTE]
> En kort forsinkelse kan oppstå mellom når du klikker **Opprett egendefinert prising**, og når den egendefinerte prislisten opprettes. Vi anbefaler at du oppdaterer rutenettet i stedet for å klikke flere ganger. En egendefinert prisliste er opprettet hvis det tilknyttede prislistenavnet har tilbudsnavnet eller prosjektkontraktnavnet tilknyttet.
