---
title: Prosjektkostnader og -omsetning
description: Dette emnet gir informasjon om beregning av prosjektkostnader og -omsetning.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 48f313b15f788645b88a4d878e3bece419d63126
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009178"
---
# <a name="project-costs-and-revenue"></a>Prosjektkostnader og -omsetning

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Prosjektestimater gir en økonomisk oversikt for arbeid som beregnet og planlagt i prosjektetplanen. Kategorien **Estimater** på **Prosjekter**-siden viser kostnadene og omsetningen for arbeidet du planlegger. Den inneholder også informasjon om mange forhåndsdefinerte dimensjoner. 

> ![Kategorien Estimater](media/project-5.png)

## <a name="cost-and-sales-values-of-the-project"></a>Kostnads- og salgsverdier for prosjektet

Prislister definerer kostnads- og fakturasatser for roller i et prosjekt. Du kan bestemme kostnadene for og omsetningen av arbeidet basert på rollene som er knyttet til stillingsnavnet og den navngitte ressursen som er tilordnet til en oppgave. Hvis det finnes oppgaver som ikke har tilordninger (generelle eller navngitte), kan du ikke hente kostnads- eller salgsestimater. Kostnads- og salgsverdier tar hensyn til datoen som er definert i prislistene.

### <a name="default-cost-price"></a>Standard kostpris  

Alle prosjekter tilhører en organisasjon. Denne organisasjonen vises i feltet **Kontraktsenhet** i prosjektet. Prislisten som er knyttet til kontraktsenheten, brukes til å fastsette enhetskostprisen. For å bestemme riktige kostpriser for roller for datoen som er definert på steimatlinjer, kan du søke etter en kombinasjon av rolle, enhet og organisasjonsenhet i kostprislisten. 

For at kostnadsprisene kan beregnes, må alle oppgaver tildeles en ressurs. Alle ikke-tilordnede oppgaver har en kostpris på 0,00.

Hvis kombinasjonen av rolle, enhet og organisasjonsenhet ikke returnerer en kostpris fra prislisten til kontraktsenheten, ignorerer systemet enheten. I stedet søker det etter kombinasjonen bare av rolle og organisasjonsenhet. Hvis det blir funnet en kostpris, brukes omregningsfaktorre til å konvertere den til enheten du valgte på estimatlinjen.

Hvis kombinasjonen av rolle og og organisasjonsenhet ikke returnerer en kostpris, ignorerer systemet organisasjonsenheten. I stedet søker det etter kombinasjonen av rolle og enhet for å angi standardprisen (etter eventuell omregning).

Hvis systemet ikke finner en pris for rollen, settes kostprisen på estimatlinjen til en standardverdi på **0,00**. Alle kostnadsbeløp på estimatlinjer for prosjektkostnader er oppført i valutaen for kontraktsenheten.

> [!NOTE]
> Som standard lagrer Microsoft Dynamics 365 kostnadsbeløp i standardvalutaen. Kostnadsbeløpene som vises i kategorien **Estimater**, er imidlertid i valutaen som er angitt i kontraktsenheten.  

### <a name="default-sales-price"></a>Standard salgspris 

Salgsprislisten bestemmes av salgsenheten som prosjektet er knyttet til, eller prosjektkunden. Når en salgsenhet, for eksempel salgsmulighet, tilbud eller kontrakt, er knyttet til prosjektet, bestemmes salgsprisen for salgsenheten av prislisten som er knyttet til tilbudet eller kontrakten. Hvis tilbudet eller kontrakten har en egendefinert prisliste, blir denne prislisten brukt som standard salgsprisliste for prosjektestimater. Hvis det ikke finnes en tilknytning til salgsenheter, brukes standardprislisten for salg fra parameterne som prosjektets standard salgsprisliste som samsvarer med kundevalutaen som er definert i prosjektet.

Hver estimatlinje har en ressursenhet som er knyttet til den. Ressursenheten angir organisasjonsenheten som ressursene er bestilt fra, for å fullføre oppgaven. Hvis du vil finne salgsprisen for de tilknyttede rollene, søker du etter kombinasjonen av rolle, enhet og ressursenhet i salgsprislisten. Hvis det ikke finnes tildelinger i oppgaven, er salgs prisen for oppgaven 0,00.

Hvis kombinasjonen av rolle, enhet og ressursenhet ikke returnerer en salgspris fra salgsprislisten, ignorerer systemet enheten. I stedet søker det etter kombinasjonen bare av rolle og ressursenhet. Hvis det blir funnet en salgspris, brukes omregningsfaktorre til å konvertere den til enheten du valgte på salgsestimatlinjen. 

Hvis kombinasjonen av rolle og ressursenhet ikke returnerer en salgspris fra salgsprislisten, ignorerer systemet ressursenheten. I stedet søker det etter kombinasjonen av rolle og enhet for å angi standardprisen (etter eventuell omregning).

Hvis systemet ikke finner en pris for rollen, settes salgsprisen på estimatlinjen til en standardverdi på **0,00**.

Kategorien **Estimater** har en rutenettvisning som viser estimatlinjer. Rutenettet inneholder kolonner for enheten, den totale kostprisen og den totalsalgsprisen, som vist i følgende illustrasjon. 

> ![Rutenettvisning i kategorien Estimater](media/project-6.png)

## <a name="time-phased-view-of-project-estimates"></a>Tidsinndelt visning av prosjektestimater

Den tidsfasede visningen av prosjektestimater viser estimatdataene fra rutenettvisningen i løpet av tidslinjen, i en tidsskala som du velger. Som standard er estimatdataene pivotert i **Rolle**-dimensjonen.

> ![Tidsinndelt visning for prosjektestimater](media/project-7.png)

## <a name="allocating-estimated-effort-based-on-the-task-mode"></a>Tildele estimert innsats basert på oppgavemodusen

I den tidsinndelte visningen distribuerer du den totale innsats som er beregnet for oppgaven, ved å tildele innsatstimer per enhetstidsperiode i den valgte tidsskalaen. Oppgavemodusen avgjør hvordan innsats fordeles gjennom varigheten til oppgaven. De to typene tildeling er **Jevn** og **Arbeidstidsbasert**.

### <a name="work-hours-based-allocation"></a>Tildeling basert på arbeidstimer
 
I modus for automatisk planlegging av oppgaver angis de daglige standardtimene for oppgaveressurser med timeprisen for full arbeid. Denne virkemåten gjelder også når innsatsen tildeles ved å dele den opp gjennom varigheten for oppgaven i den tidsinndelte visningen. Hvis du for eksempel estimerer at en oppgave blir fullført av én ressurs i **Dag**-tidsskalaen, vil innsatsen som tildeles per dag, ikke oversride arbeidstimene per dag som er definert i prosjektkalenderen. Derfor sørger tildelingen av innsats alltid for at ressursene er estimert til å brukes hele dagen.

### <a name="even-allocation"></a>Jevn tildeling

I manuelt planlagt oppgavemodus brukes ikke arbeidstimene fra prosjektkalenderen. I stedet er tidsplanen for oppgaven er basert på brukerinndata. For disse oppgavene har tildelingen av innsats per enhetstidsperiode i den valgte tidsskalaen ingen begrensende faktorer. Den totale innsatsen for oppgaven deles i like deler og tildeles for hver enhetstidsperiode i den valgte tidsskalaen. Derfor bestemmer oppgavemodusen som er definert for oppgaven, innsatsfordelingen eller tildelingen av innsats per enhetstidsperiode i tidsinndelte estimater.

## <a name="grouping-and-time-phasing-options"></a>Alternativer for gruppering og tidsinndeling

Den tidsinndelte visningen viser fordelingen av innsats, kostnader og salgsestimater basert på per dag, uke, måned eller år. Som standard er estimatdataene pivotert i **Rolle**-dimensjonen. Du kan imidlertid bruke alternativet **Grupper etter** til å pivotere på to andre dimensjoner: **Kategori** og **Ressurs**.

I både rutenettvisningen og den tidsinndelte visningen kan du velge hvilke felt som skal vises. Totalsummer for hver tidsblokk vises nederst i prosjektet. De viser totalt estimaert innsats, kostnader og salg for dagen, uken, måneden eller året. Standard kostpris og salgspris er datobasert. De endres med andre ord for hver ressurs basert på den tidsinndelte visningen du velger.

## <a name="expense-estimates"></a>Utgiftsestimater

Med knappen **Legg til nytt utgiftsestimat** i rutenettvisningen kan du registrere eventuelle utgifter som er påløpt i prosjektet, men som ikke er direkte relatert til arbeid. Du kan registrere utgiftsestimatene for en bestemt oppgave eller for hele prosjektet. Velg utgiftskategorier og den foreløpige datoen da utgiften forventes å påløpe. Hvis den tilknyttede kostprislisten og salgsprislisten har standardpriser (eller hvis påslagsprosenter er definert for utgiftskategorier), angis de automatisk på estimatlinjen ved når tilknytningen skjer.


[!INCLUDE[footer-include](../includes/footer-banner.md)]