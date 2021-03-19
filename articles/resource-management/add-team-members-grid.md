---
title: Legg til teammedlemmer fra rutenettet for teammedlemmer
description: Dette emnet gir informasjon om hvordan du kan administrere ressurser for teammedlemmer.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: cacf3913c3893dd09509cd02361c4a21bed59825
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280095"
---
# <a name="add-team-members-from-the-team-member-grid"></a>Legg til teammedlemmer fra rutenettet for teammedlemmer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Dynamics 365 Project Operations inkluderer et instrumentbord for ressursledere som gir en visuell oversikt over ressursbehov og -utnyttelse gjennom hele organisasjonen. Du kan bruke diagrammene på dette instrumentbordet til å visualisere følgende informasjon:

- **Ressursbehov**: Diagrammet **Aktive ressursforespørsler** viser ressurser som er sendt. Ressursene samles av rolle eller prosjekt.
- **Ressursbehov som ikke er sendt**: Diagrammet **Ikke-tilordnet ressursbehov** viser alle ressursbehovene som ikke er sendt. Dette diagrammet hjelper ressursansvarlige med å vise behov som ikke er fast, og kan sendes via en ressursforespørsel.
- **Fakturerbar utnyttelse for forrige uke**: Diagrammet **Utnyttelse etter rolle** viser prosentandelen av organisasjonens faktiske fakturerbare utnyttelse etter rolle mot fakturerbar utnyttelse av rolle for rolle.

    > [!NOTE]
    > For å gjøre diagrammet **Utnyttelse etter rolle** tilgjengelig må du opprette en jobb som kjører **UpdateRoleUtilization**-arbeidsflyten. Denne regelmessige jobben kjører hver sjuende dag for å beregne fakturerbar utnyttelse for de siste sju dagene. Resultatene samles etter rolle.

## <a name="manage-project-team-members"></a>Administrere prosjektteammedlemmer

Prosjektledere kan bruke Resource Manager-instrumentbordet til å administrere ressursene på prosjekter. De kan for eksempel legge til et teammedlem direkte i et prosjekt og bestille et teammedlem for å oppfylle ressurskravene som ble registrert av en generell ressurs.

### <a name="add-a-team-member-directly-to-a-project"></a>Legge til et teammedlem direkte i et prosjekt

Hvis du vil legge til et teammedlem direkte i et prosjekt, går du til **Prosjekter**-skjemaet og **Team**-kategorien og velger **Ny**. Dialogboksen **Hurtigoppretting: Prosjektteammedlem** vises. I denne dialogboksen kan du utføre disse oppgavene:

- **Bestille en navngitt ressurs**: Velg navnet på ressursen i feltet **Bestillbar ressurs**. Velg deretter rollen, angi perioden, og velg en tildelingsmetode. Den navngitte ressursen du har valgt, blir lagt til i prosjektet ved hjelp av den valgte tildelingsmetoden og ressurskalenderen.
- **Legg til en generell ressurs**: La feltet **Bestillbar ressurs** være tomt, og velg deretter rollen, angi perioden, og velg den foretrukne tildelingsmetoden. En generell ressurs blir lagt til i teamet som en plassholder. Plassholderen inneholder behovsmønsteret som brukes til å bestille navngitte ressurser i teamet. Kravet utføres i henhold til prosjektkalenderen.
- **Legg til en navngitt ressurs i teamet uten å ta i bruk ressurskapasitet**: I feltet **Bestillbar ressurs** velger du en ressurs. Velg perioden, og velg deretter **Ingen** som tildelingsmetode. Ressursen legges til i teamet, men ressursens kapasitet forbrukes ikke via en bestilling.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Bestille et teammedlem for å oppfylle ressurskrav for en generell ressurs

I Project Operations kan du reservere en generell ressurs i et prosjektteam. Du kan også angi rollen, den nødvendige kapasiteten og hvordan denne kapasiteten skal distribueres. For ressurskravet kan du angi attributter som er tilknyttet den generelle ressursen. Disse attributtene inkluderer nødvendige ferdigheter, den foretrukne organisasjonsenheten og foretrukne ressurser.

Følg fremgangsmåten nedenfor for å angi nødvendige ferdigheter på en generell ressurs for en utvikler.

1. På skjemaet **Prosjekter** i kategorien **Team** velger du **Ny** for å reservere en generell ressurs.
2. I visningen **Alle teammedlemmer**, i kolonnen **Ressurskrav** velger du koblingen for å legge til nødvendige ferdigheter for den generelle ressursen.
3. På skjemaet **Ressurskrav** i **Ferdigheter**-rutenettet, velger du ellipsen (**...**) og velger deretter **Legg til nytt kravkjennetegn** for å legge til de nødvendige ferdighetene for utvikleren.
4. I dialogskjemaet **Hurtigoppretting: Kravkjennetegn** velger du den ønskede ferdigheten i **Kjennetegn**-feltet.
5. I feltet **Rangeringsverdi** velger du kompetansenivået for ferdigheten. 
6. I feltet **Ressurskrav**, angir du kravet for kilderessurser fra organisasjonsenheter eller navngitte ressurser. Velg **Lagre** når du er ferdig.
7. På skjemaet **Ressurskrav** velger du **Bestill** for å oppfylle ressurskravet. Du kan også velge den generelle ressursen i rutenettet **Alle teammedlemmer** og deretter velge **Bestill**.

    > [!NOTE]
    > I dette eksemplet er det 40 obligatoriske timer, men ingen faktisk bestilte timer, fordi generelle ressurser ikke har bestillinger. I tillegg er det ingen tildelte timer fordi den generelle ressursen ble lagt til direkte i teamet i stedet for å bli lagt til ved å bruke oppgavetildeling.

    På skjemaet **Planleggingsassistent** kan du filtrere tilgjengelige ressurser etter kravene som er angitt i ressurskravet. Ressurser sorteres i henhold til sorteringsparameterne som er angitt på planleggingstavlen.

   Her er noen av de mest brukte filtrene:

    - **Kjennetegn sammen med en rangering**: Filtrer etter ferdigheter, sertifiseringer og andre ressurskvaliteter, i tillegg til vurdering av kompetanse.
    - **Roller**: Filtrer etter standardrollene som er tilordnet bestillbare ressurser.
    - **Organisasjonsenheter**: Filtrer bestillbare ressurser etter organisasjonsenhetene de er tilordnet til.

8. Hvis du ikke er fornøyd med resultatene av det første kravsøket, kan du endre filtervilkårene. Utvid ruten **Filtervisning** til venstre, og velg deretter **Søk** for å finne flere ressurser. Hvis du vil endre måten resultatene sorteres på, velger du **Sorter**.
9. Velg ressurser i henhold til behovet som er angitt i kravet, som angitt øverst i rutenettet. Du kan fjerne merkingen av celler i rutenettet og la den ressurskapasiteten være åpen. Bare én ressurs om gangen kan velges som bestilt.
10. Velg **Bestill** for å reservere den valgte ressursen og la planleggingstavlen være åpen, slik at du kan velge flere ressurser. Du kan også velge **Bestill og avslutt** for å reservere den valgte ressursen og lukke planleggingstavlen.
11. Gå tilbake til visningen **Alle teammedlemmer**. Legg merke til at den generelle ressursen er erstattet med den navngitte ressursen i rutenettet, og 40 timer vises som bestilt for den ressursen.

    > [!NOTE]
    > Ingen tildelte timer vises fordi de ble bestilt direkte i teamet. De ble ikke bestilt ved hjelp av oppgavetilordning.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Tilordne generelle ressurser til oppgaver og generere ressurskrav

I Project Operations kan du opprette oppgaver og deretter tilordne generelle ressurser til dem. Ressursbehovet kan dermed representeres av plassholdere når du beregner tidsplanen og de finansielle tallene. Deretter kan du generere ressurskrav for de generelle ressursene og fullføre dem.

1. På skjemaet **Prosjekter** i kategorien **Tidsplan** velger du **Legg til** for å opprette en oppgave.
2. I **Ressurser**-feltet velger du **Ressursvelger**-symbolet. Ressursvelgeren vises med eksisterende teammedlemmer for prosjektet.
3. Skriv inn navnet på den nye generelle ressursen, og velg deretter **Opprett**.
4. I dialogboksen **Hurtigoppretting: Prosjektteammedlem** som vises, velger du rollen for den generelle ressursen i **Rolle**-feltet. 
5. I feltet **Ressursenhet** velger du organisasjonsenheten for den generelle ressursen. Velg deretter **Lagre**. Det generelle teammedlemmet tilordnes nå til oppgaven.

   I kategorien **Team** vil du se det nye generelle teammedlemmet. Legg merke til at det bare har tildelte timer. Disse timene er summen av alle oppgaver som er tilordnet det generelle teammedlemmet. Det generelle teammedlemmet har ikke nødvendige timer eller et ressurskrav.

6. Du kan nå tilordne det generelle teammedlemmet til andre oppgaver ved hjelp av ressursvelgeren.

   Når du er ferdig med å tilordne den generelle ressursen til oppgaver, kan du generere et ressurs krav for den generelle ressursen.

7. I kategorien **Team** velger du den generelle ressursen, og deretter velger du **Generer krav**. Når kravet er generert, vil det generelle team medlemmet ha nødvendige timer og en kobling for ressurskravet.

  Når du har bestilt en navngitt ressurs, fjernes den generelle ressursen fra teamet og erstattes av den navngitte ressursen. I kategorien **Tidsplan** blir de generelle ressurstilordningene fjernet og erstattet av den navngitte ressursen.

  > [!NOTE]
  > Denne virkemåten inntreffer bare når en navngitt ressurs er fullstendig bestilt for det generelle ressurskravet. Når en navngitt ressurs delvis erstatter det generelle ressurskravet eller flere navngitte ressurser erstatter det generelle ressurskravet, forblir den generelle ressursen tilordnet til oppgaven.

Project Operations tilordner ikke begge ressursene til oppgaven fordi denne funksjonaliteten vil gi en mindre forutsigbar tidsplan. I dette enkle eksemplet er det enkelt å dele opp timene likt mellom to ressurser. I mer komplekse scenarier som involverer flere oppgaver og flere ressurser, må imidlertid PSA opprette antagelser om hvordan det skal fordele bestillinger som er mottatt for flere ressurser på tvers av flere oppgaver.

I disse scenariene er prosjektlederen derfor ansvarlig for å analysere flere bestillinger og tilordne dem etter behov. For å kunne tildele bestillinger tilordner prosjektlederen oppgavene fra de generelle ressursene til de navngitte ressursene, og deretter brukes **Avstemming**-visningen til å sikre at tildelingen fungerer med bestillinger.

### <a name="edit-a-resource-requirement"></a>Redigere et ressurskrav

Når et ressurskrav er opprettet, kan det hende at en prosjektleder eller ressursleder vil redigere detaljene for å finjustere søkevilkårene når planleggingstavlen brukes. Følg fremgangsmåten nedenfor for å redigere ressurskravet.

1. På skjemaet **Prosjekter** i kategorien **Team** velger du koblingen til et krav for en generell ressurs.
2. På skjemaet I **Ressurskrav** som vises, angir du nødvendig informasjon om feltet.

   På skjemaet **Ressurskrav** kan prosjektlederen eller ressursbehandleren også definere ferdigheter, roller, ressurspreferanser og foretrukket organisasjonsenhet.

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Oppdatere ressursbestillinger etter at de er bestilt på et prosjekt

Når du har lagt til en generell eller navngitt ressurs i et prosjektteam, kan du endre ressursens bestillinger.

1. På **Prosjekter**-skjemaet i kategorien **Team** velger du et teammedlem og velger deretter **Vedlikehold bestillinger**.
 
   Planleggingstavlen vises med bestillingene til prosjektteammedlemmet. Utvid teammedlemmets oppføring for å vise timene som er bestilt mot dette prosjektet, og andre prosjekter som bruker kapasiteten til teammedlemmet.

2. Merk og dra bestillingen for å utvide den eller redusere den. Dialogboksen **Opprett ressursbestilling** vises, der du kan justere bestillingen.
3. Høyreklikk bestillingen. Du kan deretter bruke hurtigmenyen til å utføre følgende handlinger:

    - Endre bestillingsstatusen
    - Redigere bestillingen
    - Erstatte en ressurs i prosjektteamet

### <a name="change-the-booking-status"></a>Endre bestillingsstatusen

Du kan endre enhver standard eller egendefinert bestillingsstatus.

Følgende statuser er inkludert i Project Operations:

- **Annullert**: Annullerer en bestillingen av en ressurs og frigjør kapasiteten for ressursen.
- **Forpliktende bestilling**: Bruker kapasiteten til en ressurs. En bestilling har vanligvis denne statusen når du åpner **Vedlikehold bestillinger** fra rutenettet **Alle teammedlemmer** på **Prosjekter**-skjemaet.
- **Ikke-forpliktende bestilling**: Legger til en ressurs i et team, men forbruker ikke kapasiteten til ressursen. Denne statusen angir at ressursen er reservert for potensielt arbeid, men fremdeles har kapasitet hvis det er nødvendig for andre jobber. Når det gjelder generell ressurstilgjengelighet, har ikke-forpliktende bestillinger en annen status enn forpliktende bestillinger.
- **Foreslått**: Representerer et forslag for en ressurs fra en ressursleder eller prosjektleder. Forslag forbruker ikke kapasiteten til en ressurs, og ressursen blir ikke lagt til i prosjektteamet. Hvis du vil ha en forpliktende bestilling av ressursen i teamet, må prosjektlederen godta forslaget.

### <a name="submit-resource-requests"></a>Sende ressursforespørsler

Ressursforespørsler brukes til å utføre behovet, eller ressurskravet, som må oppfylles av en ressursleder. For en generell ressurs som allerede er i teamet, kan du sende en ressursforespørsel direkte. En ressursforespørsel kan gjennomføres på to måter:

- Ressurslederen oppfyller forespørselen direkte. I dette tilfellet blir den generelle ressursen erstattet av en forpliktende bestilling som har en navngitt ressurs.
- Ressurslederen foreslår en ressurs til prosjektlederen, og prosjektlederen godkjenner eller forkaster den foreslåtte ressursen.

#### <a name="direct-fulfillment-of-resource-requests"></a>Direkte oppfylling av ressursforespørsler

Når et ressurskrav er generert, kan en prosjektleder sende en ressursforespørsel om en generell ressurs ved å velge ressursen og deretter velge **Send forespørsel**. Kommentarer om ressursen kan sendes til ressurslederen som oppfyller forespørselen. Når forespørselen er sendt, blir **Status**-feltet for teammedlemmet endret til **Sendt**. Når ressurslederen oppfyller forespørselen, blir det generelle teammedlemmet erstattet av den navngitte ressursen i rutenettet **Alle teammedlemmer**.

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Bruke et ressursforslag for ressursforespørsler

I stedet for å reservere en ressurs direkte på en ressursforespørsel kan en ressursleder foreslå en ressurs til prosjektlederen. En ressursleder kan bruke dette alternativet når et identisk treff for kravene ikke er tilgjengelige. Når en ressursleder foreslår en ressurs, ser prosjektlederen at **Status**-feltet for det generelle teammedlemmet blir endret til **Må gjennomgås**.

Du kan vise den foreslåtte ressursen sammen med en visualisering for effekten av forslagets bestilling. 

1. Dobbeltklikk teammedlemmet som har statusen **Må gjennomgås**. 
2. Velg kategorien **Foreslåtte ressurser**.
3. Velg **Godta alle forslag** for å godta alle foreslåtte ressurser eller **Avvis alle forslag** for å avvise dem. Hvis du godtar de foreslåtte ressursene, blir de forpliktende på prosjektet som teammedlemmer og erstatter de generelle ressursene.

> [!NOTE]
> Du må enten godta eller forkaste alle foreslåtte ressurser. Du kan ikke delvis godta eller forkaste dem.

### <a name="substitute-a-resource-on-the-project-team"></a>Erstatte en ressurs i prosjektteamet

Noen ganger må en prosjektleder erstatte et teammedlem i et prosjekt.

1. På **Prosjekter**-skjemaet i kategorien **Team** velger du ressursen som trenger erstatning, og velger deretter **Vedlikehold bestillinger**.
2. Utvid ressursen for å vise prosjektene den er tilordnet til.
3. Høyreklikk prosjektet, og velg deretter **Erstatt ressurs**.
4. Hvis du vet ressursen du vil erstatte den gjeldende ressursen med, velger du eller skriver inn navnet, og deretter velger du **Tilordne på nytt**.

Eller Hvis du må søke etter en ressurs, fullfører du fremgangsmåten nedenfor.

1. Velg **Finn erstatning**.

   Planleggingsassistente returnerer en liste over tilgjengelige erstatninger. I planleggingsassistenten kan du ytterligere filtrere de tilgjengelige ressursene for å finne en passende erstatning.

2. Hvis du vil erstatte ressursen, velger du ønsket ressurs, og deretter velger du **Erstatt**.   

   Bestillingene og tildelingene erstattes med den nye ressursen.

## <a name="reconcile-team-member-bookings-and-assignments"></a>Avstemme tilordninger og bestillinger for teammedlemmer

For teammedlemmer er bestillinger og tildelinger løst sammenkoblet. Ressurser kan med andre ord ha tilordninger, men ikke bestillinger, eller de kan ha bestillinger, men ikke tilordninger. Ideelt sett bør bestillinger og tilordninger rettes inn mot hverandre, slik at ressurser har forpliktet kapasitet til å utføre oppgavetilordningene. Det kan imidlertid hende at bestillinger blir basert på tilgjengelighet, og det kan hende at oppgavetidspunkter endres etter hvert som prosjektet fortsetter. Derfor gir den løse koblingen av bestillinger og tildelinger fleksibilitet.

Project Operations har en **Avstemming**-kategori som gjør at prosjektledere kan avstemme teammedlemmenes bestillinger og deres tildelinger for prosjektteam.

Kategorien **Avstemming** viser bestillinger og tilordninger nedover til nivået for den individuelle oppgavetilordningen for hvert teammedlem. Den viser timer i celler som representerer tidsperioder, fra måneder til dager.

Kategorien viser også en total nettosum for prosjektet, sammen med en totalsumkolonne.

For hver ressurs beregner kategorien forskjellen mellom teammedlemmenes bestillinger og en beregnet verdi teammedlemmets oppgavetilordninger. Ideelt sett bør denne forskjellen være 0 (null). Det bør med andre ord ikke være forskjell mellom bestillinger og tildelinger. Forskjellene er fargelagt og skyggelagt for å rette oppmerksomheten mot to betingelser:

- **Få bestillinger**: Inntreffer når en ressurs har flere tildelinger enn bestillinger. Ettersom denne kapasiteten ikke er reservert, kan det hende at en prosjektleder vil korrigere denne betingelsen ved å utvide ressursens bestillinger for å dekke underskuddet.
- **Overflødige bestillinger**: Skjer når en ressurs er bestilt til prosjektet, men ikke er tilordnet til aktiviteter. Denne tilstanden kan være akseptabel i saker der ressursen ble bestilt til prosjektet før oppgavetilordningen ble utført. I andre tilfeller er det imidlertid ikke planlagt at ressursen skal tilordnes til oppgaver. I slike tilfeller bør prosjektlederen vurdere å annullere ressursens bestillinger, slik at kapasiteten kan brukes for et annet prosjekt.

Når du i noen tilfeller viser tid på høyere nivå enn dagnivået, for eksempel månedsnivået, kan det hende du ser en netto differanse på null for en ressurs. Med andre ord bestillinger = tilordninger. Hvis du imidlertid viser tid på ukenivå, ser du at det er tildelinger på null timer og bestillinger på 40 timer i den første uken, men tildelinger på 40 timer og bestillinger på null timer i den andre uken. Totalt er bestillingene og tilordningene avstemte, men de skiller seg fra én uke til den neste.

Når du viser tid på høyere nivåer, har celler i **Avstemming**-kategorien en indikator som informerer deg om at det er forskjeller på lavere nivåer. Dobbeltklikk i en celle for å zoome inn og vise forskjellen. Du kan deretter høyreklikke for å zoome ut. Ved å velge en ressurs og deretter velge **Neste forskjell** på verktøylinjen i rutenettet for å gå til den neste forskjellen mellom bestillinger og tildelinger for denne ressursen. Velg **Forrige forskjell** for å gå tilbake. Du kan også slå av forskjellsindikatoren og virkemåten for navigasjon under **Innstillinger**.

Hvis du har oppgavetildelinger for en ressurs, men ingen bestillinger, går du til **Prosjekter**-skjemaet, i kategorien **Avstemming** og velger **Utvid bestilling**. Dialogboksen **Utvid bestilling** vises med bestillingen som er nødvendig for å løse ressursens underskudd. Dialogboksen viser også ressursens eksisterende bestillinger på tvers av alle prosjekter eller andre enheter som kan planlegges. Hvis du velger **OK** for å opprette en bestilling for ressursen, uavhengig av om ressursen er tilgjengelig, kan det oppstå overbestilling.

Prosjektlederen eller ressurslederen kan deretter bruke planleggingstavlen til å behandle eventuelle situasjoner der en ressurs er overbestilt utover dens kapasitet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]