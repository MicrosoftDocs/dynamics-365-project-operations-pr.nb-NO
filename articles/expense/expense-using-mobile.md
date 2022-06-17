---
title: Utgiftsapp for mobil
description: Denne artikkelen inneholder informasjon om det mobile arbeidsområdet Utgiftshåndtering.
author: suvaidya
ms.date: 11/15/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1ba7ccae04fbb02252e3ceb01f123ce1e85375b7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930238"
---
# <a name="mobile-expense-app"></a>Utgiftsapp for mobil

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Denne artikkelen inneholder informasjon om det mobile arbeidsområdet **Utgiftshåndtering**. Dette arbeidsområdet gjør det mulig for brukere å registrere og laste opp en kvittering, slik at de kan legge den ved en reiseregning senere. Brukere kan også raskt opprette en utgiftslinje ved hjelp av en tilknyttet kvittering og opprette og administrere reiseregningene sine. Godkjennere kan også bruke det mobile arbeidsområdet **Reiseregning og utlegg** til å vise reiseregninger som er tilordnet dem, og enten godkjenne eller avvise reiseregninger.

Dette mobile arbeidsområdet er ment å skulle brukes med en Dynamics 365 Unified OPS-mobilapp.

Mange organisasjoner krever at en kopi av en kvittering blir lagt ved en reiserelatert eller forretningsrelatert reiseregning som en ansatt sender inn for refusjon. Det mobile arbeidsområdet **Reiseregning og utlegg** gjør det mulig for brukere raskt å opprette nye utgiftslinjer på den valgte mobilenheten ved hjelp av et vedlagt bilde av en kvittering. Brukere kan også ta et bilde av en kvittering og deretter legge det ved en reiseregning senere. Ansatte kan også opprette og administrere reiseregninger, og deretter sende dem til godkjenning og refusjon ved hjelp av den mobile enheten.

Ved hjelp av det mobile arbeidsområdet **Reiseregning og utlegg** kan brukere utføre følgende oppgaver:

- Ta bilde av en kvittering. Laste opp kvitteringsbildet, og legge det ved en reiseregning senere.
- Laste opp en fil som en registrert kvittering. Du kan deretter legge ved denne filen i en reiseregning senere.
- Opprett en ny utgiftslinje ved hjelp av en tilknyttet kvittering. Du kan deretter legge til linjeelementet i en reiseregning senere og sende det til godkjenning og refusjon.

Du kan også bruke disse funksjonene:

- Opprette en ny reiseregning.
- Legge ved kredittkorttransaksjoner og andre tidligere opprettede utgifter i en reiseregning.
- Opprette nye utgifter for en reiseregning.
- Knytte en kvittering til enhver utgift for en reiseregning, enten ved å ta et bilde av kvitteringen eller ved å laste opp en fil som en registrert kvittering.
- Avhengig av selskapets utgiftspolicy, legger du til listen over gjester i en utgift.
- Spesifisere utgifter avhengig av firmaets utgiftspolicy.
- Sende en reiseregning for godkjenning og refusjon.
- Godkjenne eller avvise reiseregninger som du er tilordnet til godkjenner.

## <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Forutsetninger hvis du bruker Dynamics 365 Finance

Hvis Finance er distribuert for organisasjonen, må systemetadministrator publisere det mobile arbeidsområdet **Reiseregning og utlegg**. 

## <a name="download-and-install-the-dynamics-365-unified-ops-mobile-app"></a>Last ned og installer Dynamics 365 Unified Ops-mobilappen
Last ned og installer Dynamics 365 Unified Ops-mobilappen:

- [For Android-telefoner](https://go.microsoft.com/fwlink/?linkid=850662)
- [For iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Logge på mobilappen
1. Start appen på mobilenheten.
2. Angi Dynamics 365-URL-en din.
4. Første gang du logger deg på, blir du bedt om å oppgi brukernavn og passord. Angi legitimasjonen din.
5. Etter at du har logget på, vises de tilgjengelige arbeidsområdene for firmaet. Hvis systemetadministrator publiserer et nytt arbeidsområde senere, må du oppdatere listen over mobile arbeidsområder.

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Registrere en kvittering ved å bruke det mobile arbeidsområdet Reiseregning og utlegg

1. Åpne det mobile arbeidsområdet **Reiseregning og utlegg** på mobilenheten.
2. Velg **Registrer en kvittering**.
3. Velg **Ta bilde** eller **Velg bilde**.
4. Følg hvilket som helst av disse trinnene:

    - Hvis du valgte **Ta bilde**, følger du denne fremgangsmåten:

        1. Du går til kameraet på mobilenheten slik at du kan ta et bilde av kvitteringen. 
        2. Når du er ferdig med å ta bilde, velger du **OK** for å godta bildet.
        3. Valgfritt: Angi et navn for bildet, og skriv inn eventuelle notater.

    - Hvis du valgte **Velg bilde**, følger du denne fremgangsmåten:

        1. Velg et bilde fra listen.
        2. Valgfritt: Angi et navn for bildet, og skriv inn eventuelle notater.

5. Velg **Ferdig**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Registrere utgifter raskt ved å bruke det mobile arbeidsområdet Reiseregning og utlegg

1. Åpne det mobile arbeidsområdet **Reiseregning og utlegg** på mobilenheten.
2. Velg **Hurtigoppføring av utgift**.
3. Velg utgiftskategorien. Du ser en liste over utgiftskategorier som lastes inn i appen for bruk i frakoblet modus. Som standard lastes 50 elementer inn, men en utvikler kan endre dette antallet. Hvis utviklere vil ha mer informasjon, kan de se [Mobile-plattform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) Hvis kategorien din ikke finnes i listen, velger du **Søk** for å utføre et nettsøk. Søk etter utgiftskategori, eller bytt for å søke etter utgiftstype.
4. Angi transaksjonsdatoen for utgiften.
5. Valgfritt: Angi forhandleren for utgiften.
6. Angi beløpet for utgiften.
7. Velg valutaen for utgiften. Du ser en liste over valutakoder som lastes inn i appen for bruk i frakoblet modus. Som standard lastes 400 valutaer inn, men en utvikler kan endre dette antallet. Hvis utviklere vil ha mer informasjon, kan de se [Mobile-plattform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) Hvis valutaen din ikke finnes i listen, velger du **Søk** for å utføre et nettsøk. Søk etter valuta, eller bytt for å søke etter navn.
8. Velg **Ta bilde** eller **Velg bilde**.
9. Følg hvilket som helst av disse trinnene:

    - Hvis du valgte **Ta bilde**, går til kameraet på mobilenheten slik at du kan ta et bilde av kvitteringen. Når du er ferdig med å ta bilde, velger du **OK** for å godta bildet.
    - Hvis du valgte **Velg bilde**, velger du et bilde i listen.

10. Velg **Ferdig**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace"></a>Godkjenne en utgiftsrapport ved å bruke det mobile arbeidsområdet Reiseregning og utlegg

1. Åpne det mobile arbeidsområdet **Reiseregning og utlegg** på mobilenheten.
2. **Utgiftsgodkjenninger** viser antall reiseregninger som er tilordnet til deg for godkjenning. Antallet oppdateres cirka hvert 30. minutt. Velg **Utgiftsgodkjenninger**.

    Du ser listen over reiseregninger som er tilordnet til deg for godkjenning.

3. Velg en reiseregning for å vise utgiftsdetaljene for den.
4. Velg en utgift for å vise detaljene for den. Informasjonen som vises for en utgift, omfatter detaljer for kvittering, gjest og spesifisering.
5. Tilbake på siden **Reiseregning** velger du å godkjenne eller avvise reiseregningen.
6. Skriv inn eventuelle kommentarer til godkjenningshandlingen.
7. Velg **Ferdig**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace"></a>Opprette en ny utgiftsrapport og sende den til godkjenning ved å bruke det mobile arbeidsområdet Reiseregning og utlegg

1. Åpne det mobile arbeidsområdet **Reiseregning og utlegg** på mobilenheten.
2. Velg **Utgiftoppføring**.
3. Velg **Ny rapport**, eller velg en eksisterende reiseregning i listen.
4. For nye reiseregninger angir du formålet og eventuell tilleggsinformasjon som er tilgjengelig. Denne informasjonen varierer avhengig av hvordan reiseregning og utlegg er konfigurert for firmaet.
5. Velg **Ferdig**.
6. Hvis du vil legge til eksisterende utgifter, for eksempel kredittkorttransaksjoner, i reiseregningen, velger du **Legg ved**.
7. Velg én eller flere utgifter i listen.
8. Velg **Ferdig**.
9. Hvis du vil legge til en ny utgift i reiseregningen, velger du **Ny utgift**.
10. Velg utgiftskategorien. Du ser en liste over utgiftskategorier som lastes inn i appen for bruk i frakoblet modus. Som standard lastes 50 elementer inn, men en utvikler kan endre dette antallet. Hvis utviklere vil ha mer informasjon, kan de se [Mobile-plattform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) Hvis kategorien din ikke finnes i listen, velger du **Søk** for å utføre et nettsøk. Søk etter utgiftskategori, eller bytt for å søke etter utgiftstype.
11. Valgfritt: Angi forhandleren for utgiften.
12. Angi transaksjonsdatoen for utgiften.
13. Angi beløpet for utgiften.
14. Velg valutaen for utgiften. Du ser en liste over valutakoder som lastes inn i appen for bruk i frakoblet modus. Som standard lastes 400 valutaer inn, men en utvikler kan endre dette antallet. Hvis utviklere vil ha mer informasjon, kan de se [Mobile-plattform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) Hvis valutaen din ikke finnes i listen, velger du **Søk** for å utføre et nettsøk. Søk etter valuta, eller bytt for å søke etter navn.
15. Velg **Ferdig**.
16. Hvis du vil legge til flere detaljer i utgiften, velger du **Legg til flere detaljer**. Hvilke felt som er tilgjengelige, avhenger av konfigurasjonen av reiseregning og utlegg for firmaet.
17. Hvis firmapolicyen krever en kvittering for utgiftene, velger du **Kvitteringer**, og deretter følger du denne fremgangsmåten:

    1. Velg **Registrer kvittering** eller **Legg ved kvittering**.
    2. Følg hvilket som helst av disse trinnene:

        - Hvis du valgte **Registrer kvittering**, følger du denne fremgangsmåten:

            1. Velg **Ta bilde** eller **Velg bilde**.
            2. Følg hvilket som helst av disse trinnene:

                - Hvis du valgte **Ta bilde**, følger du denne fremgangsmåten:

                    1. Du går til kameraet på mobilenheten slik at du kan ta et bilde av kvitteringen. Når du er ferdig med å ta bilde, velger du **OK** for å godta bildet.
                    2. Valgfritt: Angi et navn for bildet, og skriv inn eventuelle notater.

                - Hvis du valgte **Velg bilde**, følger du denne fremgangsmåten:

                    1. Velg et bilde fra listen.
                    2. Valgfritt: Angi et navn for bildet, og skriv inn eventuelle notater.

            3. Velg **Ferdig**.

        - Hvis du valgte **Legg ved kvittering**, følger du denne fremgangsmåten:

            1. Velg ett eller flere bilder i listen.
            2. Velg **Ferdig**.

    3. Velg **Tilbake**-knappen for å gå tilbake til utgiftsdetaljene.

18. Hvis firmapolicyen krever gjester for utgiften, velger du **Gjester**, og deretter følger du denne fremgangsmåten:

    1. Velg **Gjest**, **Tidligere gjester** eller **Medarbeidere**.
    2. Følg hvilket som helst av disse trinnene:

        - Hvis du valgte **Gjest**, følger du denne fremgangsmåten:

            1. Skriv inn navnet på gjesten.
            2. Valgfritt: Angi organisasjonen og/eller landet for gjesten.
            3. Valgfritt: Skriv inn stillingen til gjesten.
            4. Velg **Ferdig**.

        - Hvis du valgte **Tidligere gjester**, følger du denne fremgangsmåten:

            1. Velg én eller flere tidligere gjester i listen. Du ser en liste over tidligere gjester du har lagt til i tidligere reiseregninger som lastes inn i appen for frakoblet bruk. Som standard lastes 50 elementer inn, men en utvikler kan endre dette antallet. Hvis utviklere vil ha mer informasjon, kan de se [Mobile-plattform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) Hvis de tidligere gjestene dine ikke finnes i listen, velger du **Søk** for å utføre et nettsøk. Søk etter navn, eller bytt for å søke etter organisasjon, land eller stilling.
            2. Velg **Ferdig**.

        - Hvis du valgte **Medarbeidere**, følger du denne fremgangsmåten:

            1. Velg én eller flere medarbeidere i listen. Du ser en liste over medarbeidere som lastes inn i appen for bruk i frakoblet modus. Som standard lastes 50 elementer inn, men en utvikler kan endre dette antallet. Hvis utviklere vil ha mer informasjon, kan de se [Mobile-plattform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) Hvis medarbeiderne ikke finnes i listen, velger du **Søk** for å utføre et nettsøk. Søk etter navn, eller bytt for å søke etter firma eller stilling.
            2. Velg **Ferdig**.

    3. Velg **Tilbake**-knappen for å gå tilbake til utgiftsdetaljene.

19. Hvis firmapolicyen krever at utgiftene spesifiseres, velger du **Spesifiser**, og deretter følger du denne fremgangsmåten:

    1. Velg første dato som skal spesifiseres.
    2. Velg **Legg til spesifisering**.
    3. Velg underkategorien for utgiftsspesifiseringen. Du ser en liste over underkategorier for utgift som lastes inn i appen for bruk i frakoblet modus. Som standard lastes 50 elementer inn, men en utvikler kan endre dette antallet. Hvis utviklere vil ha mer informasjon, kan de se [Mobile-plattform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) Hvis underkategorien din ikke finnes i listen, velger du **Søk** for å utføre et nettsøk. Søk etter navn på underkategori for utgift.
    4. Angi transaksjonsbeløpet for spesifiseringen.
    5. Rediger transaksjonsdatoen hvis det er nødvendig.
    6. Velg **Ferdig**.
    7. Gjenta de foregående trinnene til du har lagt til alle spesifiseringer for den valgte datoen.
    8. For ytterligere dager kan du velge **Kopier til neste dag** for å kopiere spesifiseringer til neste dag. Du kan også velge datoen som skal spesifiseres, og deretter legge til spesifiseringer som du gjorde for den første datoen.
    9. Når du er ferdig med å spesifisere utgiften, velger du **Tilbake**-knappen for å gå tilbake til utgiftsdetaljene.

20. Velg **Tilbake**-knappen for å gå tilbake til **Reiseregning**-siden.
21. Gjenta de foregående trinnene til du har lagt til alle utgiftene.
22. Velg **Send inn**.
23. Skriv inn eventuelle kommentarer til godkjenneren.
24. Velg **Ferdig**.

## <a name="frequently-asked-questions"></a>Vanlige spørsmål

### <a name="why-doesnt-the-expense-mobile-app-enter-the-payment-method-by-default"></a>Hvorfor angir ikke mobilappen for utgifter betalingsmetoden som standard?

Organisasjoner kan tilpasse innstillingen **Standard betalingsmåte** for hver utgiftskategori etter hvert som de opprettes. Når du konfigurerer betalingsmetoder, kan du i tillegg sette feltet **Standard betalingsmåte** til **Bare import**.

Når **Bare import** er aktivert for en betalingsmetode, angis ikke betalingsmetoden som standard. Den kommer til å være tom i utgiftskategorier der denne betalingsmetoden er konfigurert. Denne virkemåten er konsekvent både i nettopplevelsen og mobilopplevelsen.
    
Når **Bare import** ikke er aktivert for en betalingsmetode, brukes den angitte verdien som standard for utgiftskategorier der denne betalingsmetoden er konfigurert. Det finnes imidlertid et kjent problem der standardverdien ikke angis i mobilappen for utgifter. Du kan omgå dette problemet ved å velge en betalingsmetode manuelt før du lagrer utgiftsrapporten. 

### <a name="why-cant-i-add-or-edit-financial-dimensions-in-the-expense-mobile-app"></a>Hvorfor kan jeg ikke legge til eller redigere finansdimensjoner i mobilappen for utgifter?

Det er ikke støtte for å angi dimensjoner og distribusjoner. Du kan omgå denne begrensningen ved å ha disse feltene angitt som standard i mobilappen ved å konfigurere standard finansdimensjoner per prosjekt eller ansatt.

### <a name="why-do-i-sometimes-see-a-synchronization-error-in-the-expense-mobile-app"></a>Hvorfor får jeg noen ganger en synkroniseringsfeil i mobilappen for utgifter?

Hvis utgiftslinjene ikke oppfyller policykravene og brukeren sender utgiftsrapporten uten hensyn til policyadvarselen, synkroniseres ikke mobildataene med serveren, og det oppstår en synkroniseringsfeil. Alle utgiftsrapporter som sendes etter at en synkroniseringsfeil oppstår, forblir i feiltilstand og fører til flere synkroniseringsfeil. Den eneste måten å løse denne situasjonen på, er å slette synkroniseringsvarslene manuelt. Dette problemet er løst ved å stoppe sending av utgiftsrapporter hvis det ikke tas hensyn til policyadvarsler, slik at synkroniseringsfeilene unngås.

### <a name="why-isnt-project-and-category-validation-correctly-reflected-in-the-expense-mobile-app"></a>Hvorfor gjenspeiles ikke prosjekt- og kategorivalidering riktig i mobilappen for utgifter?

Denne valideringen støttes ikke for øyeblikket. Den blir imidlertid kanskje støtte i fremtiden. 

### <a name="what-document-types-are-supported-in-the-expense-mobile-app"></a>Hvilke dokumenttyper støttes i mobilappen for utgifter?

Mobilappen for utgifter støtter bare bilder. Den støtter for øyeblikket ikke PDF-filer eller andre dokumenter.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
