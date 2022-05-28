---
title: Journal for Project Operations-integrering
description: Dette emnet inneholder informasjon om hvordan du arbeider med integreringsjournalen i Project Operations.
author: sigitac
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5e1a455d055fe562a1946cc3b90c8274ef1a4b12
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582446"
---
# <a name="integration-journal-in-project-operations"></a>Journal for Project Operations-integrering

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Tid og utgifter-oppføringer oppretter **Faktisk**-transaksjoner, som representerer driftsvisningen av arbeid som fullføres mot et prosjekt. Dynamics 365 Project Operations gir regnskapsførere et verktøy for å gjennomgå transaksjoner og justere regnskapsattributtene etter behov. Når gjennomgangen og justeringene er fullført, blir transaksjonene postert til prosjektets underfinansjournal og økonomimodulen. En regnskapsfører kan utføre disse aktivitetene ved hjelp av **Project Operations-integrering**-journalen (**Dynamics 365 Finance** > **Prosjektstyring og regnskap** > **Journaler** > **Prosjekt Operations-integrering**-journalen.

![Integreringsjournalflyt.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Opprette oppføringer i journalen for Project Operations-integrering

Oppføringer i journalen for Project Operations-integrering opprettes ved hjelp av periodisk prosess, **Import fra oppsamlingstabell**. Du kan kjøre denne prosessen ved å gå til **Dynamics 365 Finance** > **Prosjektstyring og regnskap** > **Periodisk** > **Project Operations-integrering** > **Importer fra oppsamlingstabell**. Du kan kjøre prosessen interaktivt eller konfigurere prosessen til å kjøre i bakgrunnen etter behov.

Når den periodiske prosessen kjører, blir faktiske verdier som ennå ikke er lagt til i journalen for Project Operations-ingetrering, funnet. Det opprettes en journallinje for hver faktiske transaksjon.
Systemet grupperer journallinjer i separate journaler basert på verdien som er valgt i feltet **Periodeenhet i journalen for Project Operations-integrering** (**Finance** > **Prosjektstyring og regnskap** > **Oppsett** > **Parametere for prosjektstyring og regnskap**, fanen **Project Operations på Dynamics 365 Customer Engagement**). Mulige verdier for dette feltet inkluderer følgende:

  - **Dager**: Faktiske verdier er gruppert etter transaksjonsdato. Det opprettes en separat journal for hver dag.
  - **Måneder**: Faktiske verdier grupperes etter kalendermåned. Det opprettes en separat journal for hver måned.
  - **År**: Faktiske verdier grupperes etter kalenderår. Det opprettes en separat journal for hvert år.
  - **Alle**: Alle faktiske transaksjoner er inkludert i samme integreringsjournal. Hvis journalen ikke er tilgjengelig når den periodiske prosessen kjører, for eksempel hvis journalen er i ferd med å postere transaksjoner, opprettes det en ny journal.

Journallinjer opprettes basert på faktiske verdier for prosjekter. Følgende liste inneholder noen av de mer viktige standard- og transformasjonsreglene:

  - Hver faktiske transaksjon for prosjekter har en linje i journalen for Project Operations-integrasjon. Kostnader og ikke-fakturerte salgstransaksjoner for tid og material-faktureringstype vises på separate linjer.
  - **Dato**-feltet representerer transaksjonensdatoen. Feltet **Regnskapsdato** representerer datoen da transaksjonen ble registrert i hovedboken. Hvis regnskapsdatoen er i en [lukket økonomisk periode](/dynamics365/finance/general-ledger/close-general-ledger-at-period-end), og parameteren **Angi automatisk regnskapsdato i åpen finansperiode** er satt til kategorien **Økonomisk** på siden for **Prosjektstyring og regnskapsparametere**, blir regnskapsdatoen for transaksjonen justert til den første datoen i neste åpne finansperioden.
  - **Bilag**-feltet viser bilagsnummeret for hver faktiske transaksjon. Bilagsnummerserien defineres i kategorien **Nummersekvenser** på siden for **Prosjektstyring og regnskapsparametre**. Hver linje tilordnes et nytt nummer. Når bilaget er postert, kan du vise hvordan transaksjoner for kostnader og ufakturert salg er relatert ved å velge **Relaterte bilag** på siden **Bilagstransaksjon**.
  - Feltet **Kategori** representerer en prosjekttransaksjon og standarder basert på transaksjonskategorien for det relaterte faktiske prosjektverdien.
    - Hvis **Transaksjonskategori** er angitt i den faktiske verdien for prosjektet og det finnes en relatert **Prosjektkategori** i en gitt juridisk enhet, brukes denne prosjektkategorien som standard.
    - Hvis **Transaksjonskategori** ikke er angitt i det faktiske prosjektet, bruker systemet verdien i feltet **Standarder for prosjektkategori** på fanen **Project Operations på Dynamics 365 Customer Engagement** på siden **Parametere for prosjektstyring og regnskap** .
  - Feltet **Ressurs** representerer prosjektressursen som er relatert til denne transaksjonen. Ressursen brukes som en referanse i prosjektfakturaforslag til kunder.
  - Feltet **Valutakurs** henter verdiene som standard fra **Vekslingskurs for valuta** som er angitt i Dynamics 365 Finance. Hvis valutakursoppsettet mangler, vil ikke periodeprosessen **Import fra oppsamling** legge til oppføringen i en journal, og det blir lagt til en feilmelding i jobbkjøringsloggen.
  - Feltet **Linjeegenskap** representerer faktureringstypen i prosjektets faktiske verdier. Tilordning av linjeegenskaper og faktureringstype er definert på fanen **Project Operations på Dynamics 365 Customer Engagement** på siden **Parametere for prosjektstyring og regnskap**.

Bare følgende regnskapsattributter kan oppdateres i journallinjene for Project Operations-integrasjon:

- **Mva-gruppe for fakturering** og **Mva-gruppe for faktureringsvare**
- **Finansdimensjoner** (ved hjelp av **Fordel beløp**-handling)

Integreringsjournallinjer kan slettes, men eventuelle ikke-bokførte linjer settes inn i kladden på nytt etter at du har kjørt den periodiske prosessen **Import fra oppsamling** på nytt.

Når du posterer integreringsjournalen, opprettes det en underfinansjournal for prosjekt og transaksjoner i økonomimodulen. Disse brukes i nedstøms kundefakturering, inntektsføring og finansrapportering.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
