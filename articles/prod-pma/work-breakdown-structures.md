---
title: Oversikt over arbeidsnedbrytningsstrukturer
description: En arbeidsnedbrytningsstruktur er en beskrivelse av arbeidet som skal fullføres for et prosjekt. Det er et hierarki av oppgaver som representerer prosjektteamets forståelse av arbeidssammensetningen, og størrelsen, kostnad og varighet for hver enkelt komponent eller oppgave.
author: Yowelle
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 093f9901aec0db1fa8f920533c0084f877f26445fd07159e8e1ae0cf53849641
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998833"
---
# <a name="work-breakdown-structures-overview"></a>Oversikt over arbeidsnedbrytningsstrukturer

[!include [banner](../includes/banner.md)]

En arbeidsnedbrytningsstruktur er en beskrivelse av arbeidet som skal fullføres for et prosjekt. Det er et hierarki av oppgaver som representerer prosjektteamets forståelse av arbeidssammensetningen, og størrelsen, kostnad og varighet for hver enkelt komponent eller oppgave. En WBS har tre overordnede formål:

-   Beskriv nedbrytingen eller sammensetningen av arbeid i oppgaver.
-   Planlegg prosjektarbeidet.
-   Estimere kostnaden for hver oppgave.

Graden av detaljer i en WBS avhenger av det nøyaktige nivået som kreves i estimater, samt sporingsnivået som kreves mot disse beregningene. Prosjekter som har svært lav toleranse for avvik i tidsplan eller kostnad, krever vanligvis en mer detaljert WBS, og flittig sporing av arbeidsfremdrift og kostnad i henhold til WBS. Denne typen prosjekt er vanlig i bygg- og ingeniørbransjer. 

Prosjekter i bransjer som medier og reklame, programvare og IT-infrastruktur pleier imidlertid å være enestående, og produktiviteten står i forhold til erfaringen og kompetansen til hver enkelt som utfører oppgaven. Disse bransjene bruker derfor en WBS-struktur til å få en tilnærmet størrelse på et prosjekt, og ikke til å spore fremdriften for prosjektet i detalj. 

Bygging av en WBS er en intensiv prosess som vanligvis utføres over en lang periode, og som krever samarbeid og informasjon fra en rekke ulike personer. Dette emnet beskriver hvordan du kan bruke WBS-forbedringer til å oppfylle dine behov for estimater og sporing.

## <a name="prerequisites-for-creating-a-wbs"></a>Forutsetninger for å opprette en WBS
Hvis du vil opprette en WBS, må du kunne opprette en arbeidstidsplan og estimere kostnadene for arbeidet.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Forhåndskrav for å opprette en arbeidstidsplan

Hvis du vil bruke de fullstendige planleggingsfunksjonene i WBS-funksjonene, fyller du ut følgende oppsett:

1.  Opprette en standardkalender og en prosjektkalender:
    1.  Klikk **Prosjektstyring og regnskap** &gt; **Oppsett** &gt; **Parametere for prosjektstyring og regnskap** &gt; **Planlegging**. Angi en standardkalender i feltet **Standard arbeidskalender**. Dette blir standard arbeidskalender for eventuelle nye prosjekter som opprettes.
    2.  Du kan endre standardkalenderen for et bestemt prosjekt. Klikk detaljsiden for prosjektet, og deretter, på hurtigkategorien **Prosjektteam og planlegging**, oppdaterer du feltet **Planleggingskalender** ved å velge en annen kalender.

2.  Angi standard arbeidsdager og arbeidstid. Kalenderen som du angir som arbeidskalender for prosjektet, blir brukt i WBS for å finne følgende informasjon:

-   Arbeidsdager og ferier
-   Antall arbeidstimer per dag

Hvis du vil sette opp arbeidsdager og arbeidstimer for en kalender, eller hvis du vil opprette en ny kalender, klikker du på **Organisasjonsadministrasjon** &gt; **Felles** &gt; **Kalendere**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Forhåndskrav for beregning av arbeidskostnader

Hvis du vil bruke full kostnadsberegningsfunksjonaliteten i WBS, må du sette opp kostnadene og salgsprisene for ansatte, kategorier av arbeid, utgifter og gebyrer og varer.

-   Hvis du vil sette opp kostnad og salgspris for arbeids-, utgifts- og gebyrkategorier, klikker du på **Prosjektstyring og regnskap** &gt; **Oppsett** &gt; **Priser**.
-   Hvis du vil sette opp kostnad og salgspris for varer, kan du bruke siden **Vareavtaler** for hvert element på listesiden **Frigitte produkter** i behandling av produktinformasjon.

## <a name="creating-a-wbs"></a>Oppretter et WBS
Oppretting av en WBS inkluderer tre aktiviteter:

1.  **Arbeidsnedbryting** – Opprett en oversikt over arbeid til administrerbare deler eller oppgaver.
2.  **Arbeidsplan** – Beregn hvor lang tid som kreves for å fullføre en oppgave, angi gjensidige avhengigheter, og velg start- og sluttdatoene for aktiviteter.
3.  **Kostnadsberegning** – Beregn kostnader for hver oppgave.

I avsnittene nedenfor diskuteres det hvordan WBS-funksjonene kan hjelpe med hver av disse aktivitetene.

### <a name="work-decomposition"></a>Nedbryting av arbeid

Det første trinnet i prosessen med å opprette en WBS er å opprette en nedbrytning av arbeidet. WBS-funksjonaliteten støtter følgende grunnleggende konstruksjoner for arbeidsnedbrytning. 

**Prosjektrotoppgave** Prosjektrotoppgaven er sammendragsaktiviteten på øverste nivå for et prosjekt. Alle andre prosjektoppgaver opprettes under den. Navnet på rotoppgaven er alltid angitt til navnet på prosjektet. Innsatsen, datoer og varighet for rotnoden oppsummerer verdiene for oppgavene under rotoppgaven. Du kan ikke endre egenskapene for rotnoden eller slette den.

**Hovedaktiviteter eller beholderoppgaver** En hovedaktivitet er en oppgave som har underordnede oppgaver eller konstituentoppgaver under. En hovedaktivitet har ikke arbeidsinnsats eller kostnader selv. I stedet er arbeidsoppgaven og kostnaden for et aktivitetssammendrag summen av arbeidet og kostnadene for konstituentoppgavene. Den tidligste startdatoen for konstituentoppgaver brukes som startdatoen for hovedaktiviteten, og den siste sluttdatoen for konstituentoppgavene brukes som sluttdato. Du kan endre navnet på en hovedoppgave, men du kan ikke endre planleggingsegenskaper for innsats, datoer og varighet. Hvis du sletter en hovedoppgave, slettes også alle konstituentoppgavene. 

**Bladnodeoppgaver** En bladnodeoppgave representerer den mest detaljerte arbeidspakken på prosjektet. En bladnode har en beregnet arbeidsinnsats, et planlagt antall ressurser, en planlagt startdato og sluttdato, og varighet. 

Du kan fullføre følgende hierarkioperasjoner for å gjøre det mulig å opprette et arbeidshierarki eller nedbryting for et prosjekt. 

**Ny oppgave** En ny oppgave du oppretter, blir automatisk lagt til i rotnoden, og et WBS-nummer tildeles automatisk til oppgaven. WBS-nummeret representerer oppgavenivå i hierarkiet. For oppgaver på det første nivået under prosjektrotoppgaven brukes det et nummereringssett på 1, 2, 3 og så videre. For oppgaver under det første nivået brukes det et nummereringssett på 1.1, 1.2, 1.3 og så videre. For hvert nivå som legges til under et tidligere nivå, blir det lagt til en ny prikket serie med tall. 

Du kan ikke tilpasse WBS-nummereringen for øyeblikket. 

**Rykk inn aktivitet** Når du rykker inn en aktivitet, blir den en underordnet aktivitet for aktiviteten som kommer foran den. WBS-nummeret for den nye underordnede aktiviteten beregnes automatisk på nytt basert på WBS-nummeret til den nye overordnede. Den overordnede oppgaven er nå et sammendrag eller en beholderoppgave og blir derfor en opprullering av konstituentoppgavene. 

> [!NOTE] 
> Når du rykker inn oppgaver under en oppgave som var en bladnode før inn rykket, mister den nylig opprettede hovedaktiviteten sine egne datoer, innsats og antall ressurser. Nå brukes det et sammendrag av verdiene i de nye konstituentoppgavene. 

**Reduser innrykk for aktivitet** Når du reduserer innrykket for en aktivitet, er den ikke lenger en del av den overordnede aktiviteten. WBS-nummeret for denne oppgaven beregnes automatisk på nytt for å vise det nye nivået til aktiviteten i hierarkiet. Innsats, kostnader og datoer for oppgavens forrige overordnede oppgave beregnes på nytt for å utelukke oppgaven. 

**Flytt opp og Flytt ned** Når du klikker **Flytt opp** og **Flytt ned**, endrer du plasseringen til en oppgave innenfor det overordnede hierarkiet. Plasseringen til en oppgave påvirker ikke oppgavens innsats, kostnader, datoer eller varighet. WBS-nummeret for denne oppgaven beregnes imidlertid automatisk på nytt for å vise oppgavens nye posisjon.

### <a name="schedule-estimation"></a>Tidsplanestimat

Tidsplanestimat er vanligvis det andre trinnet i opprettelsen av en WBS. Som en god fremgangsmåte bør du fullføre planleggingsberegningen etter at du har opprettet oppgavene. Siden **Arbeidsnedbrytningsstruktur** i Finance har to deler. Den øvre ruten er beregnet på tidsplananslag, og den nedre ruten inneholder kategorien **Beregnede kostnader og inntekter**, som du kan bruke til kostnadsberegning. 
**Aktivitetsavhengigheter** I en WBS-aktivitet kan du opprette en foregående relasjon mellom aktiviteter. Når du tilordner foregående oppgaver til en oppgave, kan oppgaven bare starte etter at de foregående oppgavene er fullført. Planlagt startdato for aktiviteten angis automatisk til siste dato for alle forgjengere. 

**Oppgaveplanlegging** Følgende faktorer avgjør planleggingen av bladnodeoppgaver:

-   Foregående krav
-   Innsats
-   Antall ressurser
-   Start- og sluttdatoer

Startdatoen for en bladnodeoppgave som ikke har foregående oppgaver, settes automatisk til planlagt startdato for prosjektet. Varigheten av en bladnodeoppgave er alltid beregnet som antall arbeidsdager mellom start- og sluttdatoen. 

*<strong><em>Planleggingsregler</em></strong>* Når automatisk planleggingshjelp er aktivert, gjelder følgende regler for oppgaveplanlegging for bladnodeoppgaver:

-   Start- og sluttdatoene for en oppgave må alltid være virkedager i henhold til prosjektets planleggingskalender.
-   Startdatoen for en oppgave som har foregående oppgaver, settes automatisk til den seneste sluttdatoen for foregående oppgaver.
-   Innsatsen for en oppgave beregnes automatisk på denne måten:

Antall personer × varighet × antall timer i en standard arbeidsdag i prosjektkalenderen. 

I noen tilfeller vil du kanskje avvike fra disse reglene. Du kan deaktivere automatisk planlegging for å forhindre at Finance automatisk angir eller korrigerer egenskaper for bladnodeoppgaver. Når du angir informasjon for en oppgave som forårsaker et brudd på planleggingsregler, vises det et planleggingsfeilikon for oppgaven. Hvis du ikke vil at planleggingsfeil skal vises, klikker du **Planleggingsfeil vises** for å deaktivere funksjonen. 

> [!NOTE] 
> Verdiene for en sammendrags- eller beholderoppgave vil fortsette å bli beregnet som summen av verdiene i konstituentoppgaver, uansett om automatisk planleggingshjelp er aktivert eller deaktivert. 

**Rette planlegginsfeil** Når automatisk planleggingshjelp er aktivert, oppstår det sannsynligvis ingen planleggingsfeil. Hvis du imidlertid deaktiverer automatisk planleggingshjelp og deretter slår den på igjen senere, kan det hende at planleggingsfeilikoner vises i WBS. 

**Rette planleggingsfeil etter oppgave** Når du dobbeltklikker ikonet for tidsplanfeil for en bestemt oppgave, viser en dialogboks alle planleggingsfeilene for oppgaven. Du kan avgjøre hvilke planleggingsfeil som skal løses for oppgaven. 

**Rette alle planleggingsfeil** Hvis du vil at Finance skal rette opp alle planleggingsfeil i WBS, klikker du **Reparer alle planleggingsavvik**. 

> [!NOTE] 
> Denne funksjonen kan føre til omfattende endringer i WBS. Feilene rettes i følgende rekkefølge:

1.  Den antatte innsatsen for alle oppgavene blir endret, slik at den er lik kapasiteten som er definert i prosjektkalenderen.
2.  Startdatoen for hver enkelt oppgave endres, slik at aktiviteten starter etter at alle de foregående aktivitetene er fullført.
3.  Startdatoen for hver oppgave blir endret for å fjerne tomrom i startdatoene for foregående oppgaver.

### <a name="cost-estimation"></a>Kostnadsberegning

Som var nevnt tidligere i dette dokumentet angir du kostnadsestimeringen for hver bladnodeoppgave ved å bruke kategorien **Beregnede kostnader og inntekter** i den nedre ruten på siden **Arbeidsnedbrytningsstruktur**. 

> [!NOTE] 
> Du kan ikke endre kostnadsberegningen for en sammendrags- eller beholderoppgave. Kostnadsberegningen for en sammendragsoppgave er lik summen av kostnadsberegningen for bladnodeoppgavene. De beregnede totale kostnadene for hver oppgave beregnes som summen av de estimerte kostnadsbeløpene for følgende transaksjonstyper:

-   Arbeid
-   Vare eller materiell
-   Utgifter

En **Gebyr**-transaksjonstype brukes til å beregne gebyrbasert omsetning. Denne transaksjonstypen har ikke en kostnadskomponent og vurderes derfor ikke når kostnader beregnes. 

En **A konto**-transaksjonstype brukes til å registrere den avtalte salgsverdien i en prosjekttype med fast verdi. Denne transaksjonstypen tas heller ikke med når kostnader beregnes. 

Når du beregner kostnader for arbeid, materialer og utgifter for hver aktivitet, må du tilordne en prosjektkategori til den beregnede kostnaden. 

**Beregne arbeidskostnader** For hver bladnodeoppgave tilordner du arbeidsinnsats i timer og en standardkategori. Når du setter opp en tidsplan for en oppgave, blir derfor arbeidskostnadsberegningen for oppgaven automatisk lagt til i standardkategorien for arbeid. Dette kostnadsestimatet vises i kategorien **Estimerte kostnader og omsetning** i rutenettet **Linjedetaljer** for oppgaven. Hvis du trenger flere arbeidskostnadsoverslag, kan du legge dem til i denne kategorien. Hvis du øker eller reduserer antall timer i kostnadsberegningen, beregnes oppgaven automatisk på nytt. 

**Beregne utgifter og materialkostnader** Kategorien **Estimerte kostnader og omsetning** gjør det også mulig å estimere utgifter og materialkostnader for en oppgave hvis du krever estimater. 

Kost- og salgsprisen for hver enkelt arbeids- eller utgiftsestimatlinje er basert på oppsettet som er definert for hver kategori i pristabellene i **Prosjektstyring og regnskap** &gt; **Oppsett** &gt; **Prissetting**. For varer legges kostnads- og salgspriser til som standard fra vare- eller handelsavtaler på listesiden **Frigitte produkter** i behandling av produktinformasjon.

## <a name="tracking-progress-on-the-wbs"></a>Sporingsfremdrift i WBS
Noen bransjer sporer fremdriften for et prosjekt mot en WBS på et svært detaljert nivå, mens andre sporer fremdriften på et høyere nivå av WBS. Denne delen beskriver hvordan du kan bruke WBS-sporing for prosjektkravene. 

Finance har tre visninger for WBS for et prosjekt: prosjektplanleggingsvisning, innsatssporingsvisning og kostnadssporingsvisning.

### <a name="planning-view"></a>Planleggingsvisning

Planleggingsvisningen viser planlagt eller grunnlinjeberegning for tidsplan- og kostnadsinformasjon. Selv om det ikke finnes noen funksjoner for sporing av versjon og basislinje for en prosjekt-WBS, er verdiene i denne visningen ment å representere basislinjeversjonen. I delene Tidsplanestimat og Kostnadsberegning i dette emnet beskrives denne visningen og hvordan den brukes til å opprette en WBS.

### <a name="effort-tracking-view"></a>Visning av innsatssporing

Innsatssporingsvisningen viser sporingsfremdriften for oppgavene i WBS. Den sammenligner de akkumulerte faktiske innsatstimene for en oppgave med de planlagte innsatstimene. Følgende formler gir verdiene i visningen for innsatssporing:

-   Fremdriftsprosent = faktisk innsats til dato ÷ planlagt innsats for oppgaven
-   Gjenstående innsats (også kalt Estimat for fullføring \[ETC\]) = planlagt innsats – faktisk innsats til dato
-   Estimat ved fullføring (EAC) = resterende innsats + faktisk innsats til dato
-   Forventet innsatsavvik = planlagt innsats – EAC

Visningen for innsatssporing viser en projeksjon av innsatsvariansen for aktiviteten, basert på om EAC er mer eller mindre enn det planlagte arbeidet:

-   Hvis EAC er større enn den planlagte innsatsen, blir oppgaven beregnet til å ta mer tid enn det som opprinnelig ble planlagt, og er etter tidsplanen.
-   Hvis EAC er mindre enn den planlagte innsatsen, blir oppgaven beregnet til å ta mindre tid enn det som opprinnelig ble planlagt, og er foran tidsplanen.

**Prosjektlederens nye projisering av innsats** Fra tid til annen vil prosjektlederen eller en annen person som sporer fremdriften for et prosjekt, revidere de opprinnelige beregningene på en aktivitet. Oppgaven kan gå raskere eller saktere enn opprinnelig forventet av ulike årsaker. Omfanget er for eksempel redusert, eller ansatte har mindre erfaring enn opprinnelig planlagt. Projeksjoner er prosjektleders oppfatning av estimater, basert på gjeldende status på et prosjekt. Generelt bør du ikke endre tallene i den opprinnelige planen, fordi den opprinnelige planen representerer et velpublisert dokument for prosjektets tidsplan og kostnadsestimater som alle interessenter i prosjektet har godtatt. 

Det er to måter prosjektledere kan endre innsats på aktiviteter:

-   Endre det gjenstående arbeidet som automatisk er angitt til å oppdatere den faktiske gjenstående innsatsen for oppgaven.
-   Endre fremdriftsprosenten som automatisk er angitt til å oppdatere den virkelige fremdriften på oppgaven.

Begge disse metodene forårsaker en ny beregning av aktivitetens ETC, EAC og fremdriftsprosent samt beregnet innsatsavvik for aktiviteten. EAC, ETC- og fremdriftsprosenten på aktivitetssammendragene beregnes også på nytt, og det projiserte innsatsavviket oppdateres. 

**Modifisert arbeid i aktivitetssammendrag** Du kan endre innsatsen på sammendrags- eller beholderoppgaver. Uansett om du endrer disse verdiene ved hjelp av gjenstående innsats eller fremdriftsprosenten for aktivitetssammendraget, starter beregningene automatisk i følgende rekkefølge:

1.  EAC, ETC og fremdriftsprosent for aktiviteten beregnes.
2.  Den nye EAC fordeles i de underordnede aktivitetene i samme proporsjon som det opprinnelige EAC-beløpet.
3.  Den nye EAC for hver bladnodeoppgave beregnes.
4.  Den gjenværende innsatsen og fremdriftsprosenten beregnes på nytt for alle de berørte underordnede aktivitetene basert på den nye EAC-verdien. Innsatsvariansen for oppgavene beregnes også på nytt.
5.  EAC for aktivitetssammendraget beregnes også på nytt fra bladnodene.

Klikk **Utvid til nivå** i visning av innsatssporing for å angi nivået for sporing og vedlikehold av WBS-en. WBS-koden utvides automatisk til dette nivået i visningen for innsatssporing når du åpner den.

### <a name="cost-tracking-view"></a>Kostnadssporingsvisning

Kostnadssporingsvisningen viser sporing av kostnadsforbruk for en oppgave. I denne visningen sammenlignes de faktiske kostnadene som er brukt mot en aktivitet til dags dato, med de planlagte kostnadene for aktiviteten. Følgende formler gir verdiene i visningen for kostnadssporing:

-   Prosentandel av kostnadene som brukes = faktisk kostnad til dato ÷ planlagt kostnad for aktiviteten
-   Kostnad for fullføring (CTC) = planlagt kostnad – faktisk kostnad til dato
-   Estimat ved fullføring (EAC) = CTC + faktisk kostnad til dato
-   Beregnet kostnadsavvik = planlagt kostnad – EAC

Visningen for kostnadssporing viser en projeksjon av kostnadsvariansen for aktiviteten, basert på om EAC er mer eller mindre enn den planlagte kostnaden:

-   Hvis EAC er større enn den planlagte kostnaden, blir oppgaven beregnet til å bruke mer penger enn det som opprinnelig ble planlagt, og er over budsjettet.
-   Hvis EAC er mindre enn den planlagte kostnaden, blir oppgaven beregnet til å bruke mindre penger enn det som opprinnelig ble planlagt, og er under budsjettet.

**Prosjektlederens nye projisering av kostnad** Prosjektledere må bruke CTC for å revidere det opprinnelige kostnadsestimatet for en oppgave. Prosjektlederen kan endre CTC-verdien til kostnaden som kreves for å fullføre oppgaven. Hvis du endrer CTC-verdien, beregnes oppgavens CTC, EAC og prosent av kostnad brukt og beregnet kostnadsavvik for en aktivitet, på nytt. EAC, ETC- og prosent av kostnad som er brukt på aktivitetssammendragene beregnes også på nytt, og det projiserte kostnadsavviket oppdateres. 

> [!NOTE] 
> Når du reviderer innsats for en WBS-oppgave i visningen for innsatssporing, beregnes oppgavens CTC, EAC, prosent av forbrukt kostnad og beregnet kostnadsavvik på nytt i kostnadssporingsvisningen. Kostnadsrevisjoner påvirker imidlertid ikke verdiene i visningen for innsatssporing, siden kostnad etter transaksjonstype (arbeid, materiale eller utgift) eller prosjektkategorien ikke er revidert. 

**Projeksjonsrevisjon for kostnader i sammendragsaktiviteter** Du kan revidere kostnader i sammendragsaktiviteter, og beregningene utføres automatisk i følgende rekkefølge:

1.  EAC, CTC og prosentandelen av kostnadene som brukes på aktiviteten, beregnes på nytt.
2.  Den nye EAC fordeles til de underordnede aktivitetene i samme proporsjon som den opprinnelige EAC på aktivitetene.
3.  Den nye EAC for hver oppgave blir beregnet.
4.  CTS og prosentsats for forbrukte kostnader beregnes på nytt for de berørte underordnede aktivitetene basert på EAC-verdien. Kostnadsvariansen for oppgavene beregnes også på nytt.
5.  EAC for alle sammendragsoppgaver beregnes på nytt basert på denne endringen.

Klikk **Utvid til nivå** i visning av kostnadssporing for å angi nivået for sporing og vedlikehold av WBS-en. WBS-koden utvides til dette nivået i visningen for kostnadssporing når du åpner den.

### <a name="earned-value-management"></a>Behandling av opptjent verdi

Du kan bruke metoden for opptjent verdi (EVM) til å spore fremdriften for et prosjekt. Du kan vise opptjente verdimålinger i rollesenteret til prosjektlederen. Diagramkomponenten for opptjent verdi viser tidsfasede verdier for planlagt verdi og faktisk kostnad. Opptjent verdi per gjeldende dato vises som et punkt. Tidsinndelte data for opptjent verdi er for øyeblikket ikke tilgjengelig. 

Tidsfasen i diagrammet for opptjent verdi vises etter uke eller måned. Denne delen beskriver de tre søylene i EVM: planlagt verdi, opptjent verdi og faktisk kostnad. 

**Planlagt verdi** EVM-teorien angir at den planlagte verditegningen representerer hvor raskt prosjektets team har planlagt å opptjene verdi på prosjektet. 

Finance bruker opptjeningsregelen 0:100 ved fastsetting av planlagt verdi. Under denne regelen blir verdien for oppgaven postert til oppgaven i henhold til sluttdatoen. Ingen verdi blir postert før oppgaven er 100 prosent fullført. 

I prosjektstyring og regnskap angir du sluttdatoen for bladnoder og de planlagte kostnadene for den. Når grafen for planlagt verdi vises etter uke, oppsummeres den planlagte verdien etter uke for alle bladnodeoppgaver i prosjektets varighet. 

**Opptjent verdi** EVM-teorien angir at den opptjente verditegningen representerer hvor raskt prosjektets team faktisk tjener opp verdi på prosjektet. 

Finance bruker opptjeningsregelen 0:100 ved fastsetting av opptjent verdi. Under denne regelen blir verdien for oppgaven postert til oppgaven i henhold til sluttdatoen. Ingen verdi blir postert før oppgaven er 100 prosent fullført. 

Når opptjent verdi beregnes, vurderes fremdriftsprosenten for hver oppgave. Under opptjeningsregelen 0:100 tas det hensyn til bare oppgaver som er fullført i en bestemt periode, for beregning av opptjent verdi per slutten av perioden. Opptjent verdi i prosjektet beregnes for alle oppgaver som ble fullført da grafen ble opprettet. 

> [!NOTE] 
> Systemet for WBS-sporing har for øyeblikket ikke datastrukturer for å lagre historiske fremdriftsprosenter for hver aktivitet. Opptjent verdi kan derfor bare rapporteres på samme tid som kuben behandles. Behandle kuben regelmessig for å oppdatere dataene for opptjent verdi som vises i rollesenteret. 

**Faktisk kostnad** EVM-teori angir at den faktiske kostnadstegningen representerer frekvensen av penger som brukes på prosjektet. 

Transaksjoner som blir postert til et prosjekt, brukes til å tegne inn i den faktiske kostnadslinjen. Kostnadene oppsummeres etter dato. Disse dataene brukes til å lage en grafisk fremstilling av faktiske kostnader etter uke eller måned i diagrammet for opptjent verdi.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Slik bruker du konseptene for planlagt verdi, opptjent verdi og faktisk kostnad

**Tidsplanavvik** I løpet av planleggingen oppretter du en prognose for arbeid på en tidslinje. Derfor er planlagt verdi hastigheten som prosjektplanleggerne tenkte arbeidet ville bli fullført på prosjektet. Når et prosjekt pågår, blir arbeidet fullført, og prosjektet får verdi. Ved å sammenligne planlagt verdi med opptjent verdi kan du vise hvordan arbeid på et prosjekt pågår. Resultatet av denne sammenligningen kalles tidsplanavvik. 

Hvis den planlagte verdien for en periode er større enn den opptjente verdien, er mengden arbeid som er utført på et prosjekt, mindre enn det planlagte arbeidet. Derfor er prosjektet etter tidsplanen. Siden planlagt verdi og opptjent verdi er uttrykt i monetære termer, får forsinkelsestiden på prosjektet også en pengeverdi. 

Hvis den planlagte verdien for en periode er mindre enn den opptjente verdien, er mengden arbeid som er utført på et prosjekt, mer enn det planlagte arbeidet. Derfor er prosjektet foran tidsplanen. Denne ledetiden får også en pengeverdi.

**Kostnadsavvik** Fordi opptjent verdi bruker kostprisen som multiplikator, indikerer opptjent verdi kostnadene for arbeidet som utføres på et prosjekt. Etter hvert som prosjektet skrider frem, gir transaksjonsloggen en oversikt over penger som faktisk brukes på prosjektet. Ved å sammenligne opptjent verdi i faktiske kostnader kan du vise pengebeløpet som brukes i forhold til verdien som er opptjent. Resultatet av denne sammenligningen kalles kostnadsavvik. 

Hvis de faktiske kostnadene som brukes for en periode, er større enn den opptjente verdien, ble det brukt mer penger enn opptjent. Derfor er prosjektet over budsjett. 

Hvis de faktiske kostnadene som brukes for en periode, er mindre enn den opptjente verdien, ble det brukt mer penger enn opptjent. Derfor er prosjektet under budsjett.

## <a name="wbs-templates"></a>WBS-maler
Du kan bruke funksjonaliteten for WBS-maler til å opprette standardmaler for prosjekter. Hvis prosjektene som firmaet tilbyr, omfatter masse gjentakende arbeid, bør du vurdere å opprette en WBS-mal. 

Du kan opprette en WBS-mal fra WBS for et eksisterende prosjekt, slik at kunnskapsmetoder og gode fremgangsmåter som du samlet inn under planleggingen av prosjektet, kan brukes på nytt på lignende prosjekter i fremtiden. Noen ganger kan det imidlertid være fornuftig å lagre hele WBS som en mal. Derfor kan du også opprette maler fra deler av WBS for et prosjekt.

### <a name="saving-a-projects-wbs-as-a-template"></a>Lagre et prosjekts WBS som en mal

Når du har opprettet en mal, kan du importere den til et nytt prosjekts WBS under rotnoden eller under alle aktiviteter i prosjektets WBS.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>Importere en WBS-mal til et prosjekts WBS

Når du importerer oppgaver, ordnes oppgavene i malen basert på startdatoen for oppgaven de importeres under. Under importen brukes foregående relasjoner på maloppgavene til å beregne startdatoene for de importerte oppgavene. Standard arbeidskalender for målprosjektet brukes til å beregne sluttdatoene for de importerte aktivitetene, slik at arbeidsdager og standard arbeidstimer som er definert i arbeidskalenderen til gjeldende prosjekt, beholdes. 

Kostnadsbeløp og salgspriser på estimatlinjene brukes for å garantere at priser som er spesifikke for prosjektet eller prosjektkontrakten, har gyldige datoer.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Forskjeller mellom et prosjekts WBS og en WBS-mal

-   Oppgavene i WBS-maler har ikke startdatoer og sluttdatoer.

Arbeidsdager og fridager er ikke angitt for WBS-maler.

-   WBS-maler bruker alltid planleggingskalenderen som er angitt som standardkalender for alle prosjekter.

Standard planleggingskalender brukes bare til å finne timer på en standard arbeidsdag.

-   Foregående relasjoner kopieres ikke til en WBS-mal.

I og med at WBS-maler ikke har datoer, er ikke startdatologikken som er basert på sluttdato for en foregående aktivitet, nødvendig.

-   En arbeidskostnadsoverslagslinje opprettes automatisk når en oppgave opprettes i en WBS-mal. Salgsprisen og kostnadsbeløpet kopieres fra den valgte arbeideren.

Utgift og varekostnad kan opprettes manuelt, på samme måte som i et prosjekts WBS.

-   Planleggingsfeil vises når det er avvik fra følgende formel:

Innsats = antall ressurser × varighet x antall timer på en standard arbeidsdag 

Du kan rette opp alle planleggingsfeil samtidig ved å klikke **Reparer alle planleggingsavvik**. 

Du kan også korrigere planleggingsfeil enkeltvis ved å klikke advarselsikonet for hver enkelt oppgave.





[!INCLUDE[footer-include](../includes/footer-banner.md)]