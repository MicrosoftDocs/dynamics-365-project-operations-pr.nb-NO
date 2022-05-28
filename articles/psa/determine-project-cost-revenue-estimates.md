---
title: Fastsette kostnads- og omsetningsestimater for prosjekt
description: Slik fastsetter du kostnads- og omsetningsestimater for prosjekt i Project Service
author: ruhercul
ms.prod: ''
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 5d1bdde3c376a74952d54a1e7fade1f48e675d2f
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580238"
---
# <a name="determine-project-cost-and-revenue-estimates"></a>Fastsette kostnads- og omsetningsestimater for prosjekt 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Prosjektestimater gir en økonomisk oversikt for arbeid beregnet og planlagt i prosjektets arbeidsnedbrytningsstruktur. Estimatvisningen informerer deg om kostnads- og omsetningspåvirknignen for det planlagte arbeidet. Estimatvisningen inneholder et verktøy for å se informasjonen på en rekke forhåndsdefinerte dimensjoner for å informere deg på beste måte om den økonomiske innvirkningen av prosjektet.  
  
## <a name="cost-and-sales-value-of-the-project"></a>Kostnad og salgsverdi for prosjektet  
[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-prislister definerer kostnads- og fakturasatser for roller som prosjekter bruker. Basert på rollene som er tilknyttet aktiviteter i prosjektets arbeidsnedbrytningsstruktur, kan du angi kostnads- og omsetningspåvirknignen av det involverte arbeidet.  
  
## <a name="cost-price-defaulting"></a>Standard kostpris  
Hvert prosjekt tilhører en organisasjon (angitt i **Eiende enhet** i prosjektet). Prislisten som er forbundet med den eiende organisasjonsenheten, bestemmer kostprisen for enheten. [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] bestemmer kostpriser for roller ved å søke etter en kombinasjon av rolle, enhet og organisasjonsenhet i kostprislisten for å hente riktig kostpris for datoen som gjelder for estimatlinjer.  
  
Hvis kombinasjonen av rolle, enhet og organisasjonsenhet ikke fører til en kostpris fra den eiende enhetens prisliste, ignoreres enheten til fordel for kombinasjonen av rolle og organisasjonsenhet. Hvis det er en kostpris, konverteres denne prisen til enheten du velger på estimatlinjen.  
  
Hvis kombinasjonen av rolle og organisasjonsenhet ikke resulterer i en kostpris, ignoreres organisasjonsenheten til fordel for kombinasjonen av rolle og enhet, og prisen standardiseres etter å ha brukt en konvertering, om nødvendig.  
  
 Hvis det ikke finnes en pris for rollen, angis kostprisen som standard til 0,00 på estimatlinjen.  
  
 Alle kostnadsbeløp på estimatlinjer for prosjektkostnader er i valutaen for den eiende organisasjonsenheten.  
  
## <a name="sales-price-defaulting"></a>Standard salgsprisliste  
Salgsprislisten er basert på salgsenhet som prosjektet er knyttet til. Salgsprislisten som er forbundet med tilbudet eller kontrakten, bestemmer salgsprisen for enheten. Hvis tilbudet eller kontrakten har en egendefinert prisliste, er det standard salgsprisliste for prosjektestimater. Hvis det ikke finnes noen tilknytning til salgsenhetene, blir standard salgsprisliste som er konfigurert i parameterinnstillinger, standard salgsprisliste for prosjektet. Hver estimatlinje har en organisasjonsenheten for ressurs tilknyttet for å angi organisasjonsenheten der ressursene skal bestilles fra, for å fullføre oppgaven. Salgsprisen for de tilknyttede rollene bestemmes ved å søke etter en kombinasjon av rolle, enhet og organisasjonsenhet for ressurs i salgsprislisten for å hente riktig salgspris for datoen som gjelder for estimatlinjene.  
  
Hvis kombinasjonen av rolle, enhet og organisasjonsenhet for ressurs ikke resulterer i en salgsprise fra salgsprislisten, vil systemet se bort fra enheten og søke etter kombinasjonen av rolle og organisasjonsenhet for ressurs. Hvis en salgspris funnes, blir den konvertert til enheten du velger på salgsestimatlinjen.  
  
Hvis systemet ikke finner en pris for rollen, må salgsprisen angis til 0,00 som standard på estimatlinjen.  
  
Estimatvisningen har en rutenettvisning som viser et flat rutenett med estimatlinjer med enhet og total kostpris og salgspris.  
  
## <a name="time-phased-view-of-project-estimates"></a>Tidsinndelt visning av prosjektestimater  
I den tidsinndelte visningen for prosjektestimater pivoteres estimatdataene fra rutenettvisningen som standard etter rolle og viser spredning av estimatdataene på tvers av tidslinjen i den valgte tidsskalaen.  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a>Tildeling av estimat for innsats basert på oppgavemodus  
I den tidsinndelte visningen distribueres total innsats som er beregnet for oppgaven, ved å tildele et bestemt antall innsatstimer per enhetstidsperiode i den valgte tidsskalaen. I Project Service avgjør oppgavemodusen hvordan innsats fordeles gjennom varigheten til oppgaven. De to typene tildeling er jevn tildeling og tildeling basert på arbeidstimer. 
  
## <a name="work-hours-based-allocation"></a>Tildeling basert på arbeidstimer  
Oppgavemodusen automatisk planlegging for en oppgave styrer at for antallet ressurser som er estimert for oppgaven, estimeres de å bli utnyttet for alle arbeidstimene per dag. Dette gjelder også når innsatsen tildeles ved å dele den opp gjennom varigheten for oppgaver i den tidsinndelte visningen. Eksempel: For tidsskalaen "Dag", for en oppgave estimert å bli fullført av én ressurs, vil innsatsen som tildeles per dag, ikke overskride antallet arbeidstimer per dag som er definert i prosjektets kalender. Derfor sørger tildelingen av innsats alltid for at ressursene er estimert til å utnyttes hele dagen.  
  
## <a name="even-distribution"></a>Jevn fordeling  
Manuelt planlagt oppgavmodus overholder ikke arbeidstimer, prosjektkalenderen eller antallet ressurser som er definert for oppgaven. Tidsplanen for oppgaven er basert på brukerinndata. For slike oppgaver har tildelingen av innsats per enhetstidsperiode for den valgte tidsskalaen ingen begrensende faktorer. Den totale innsatsen for oppgaven deles i like deler og tildeles for hver enhetstidsperiode i den valgte tidsskalaen.  
  
På denne måten bestemmer oppgavemodusen som er definert for oppgaven, innsatsfordelingen eller tildelingen av innsats per enhetstidsperiode i tidsinndelte estimater.  
  
## <a name="grouping-and-time-phasing-options"></a>Alternativer for gruppering og tidsinndeling  
Denne visningen hjelper deg med å forstå fordelingen av innsats, kostnader og salgsestimater basert på per dag, uke, måned eller år. Grupper etter-alternativet kan pivotere estimatdataene på to andre dimensjoner: kategori og ressurs. Du kan velge feltene som skal vises, både i rutenettvisningen og i den tidsinndelte visningen. Totalsummer for hver av tidsblokkene vises nederst, noe som indikerer totalt estimert innsats, kostnad og salg for dagen, uken, måneden eller året.  
  
Standarden for kostnads- og salgspris er datobasert. Når satsene for rollene endres, vil det være mer gjennomsiktig i den tidsinndelte visningen ved visning av estimatdata pivoteres etter "Ressurs" og tidsinndeles etter uke.  
  
## <a name="expense-estimates"></a>Utgiftsestimater  
Alle utgifter som vil påløpe i prosjektet som ikke er direkte relatert til arbeidskraft som skal brukes opp, kan registreres i prosjektestimatene i rutenettvisning. Du kan utføre dette ved å bruke alternativet **Legg til utgiftsestimat** i rutenettvisning. Utgiftsestimatene kan registreres for en bestemt oppgave eller for hele prosjektet. Du kan velge utgiftskategorier på disse linjene og velge en dato for når kostnadene forventes å bli pådratt. Hvis den tilknyttede kostnads- og salgsprislisten har standardpriser eller markeringsprosenter definert for utgiftskategorier, angis den til en standard på estimatlinjen ved tilknytning.  
  
### <a name="see-also"></a>Se også  
 [Prosjektlederhåndbok](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
