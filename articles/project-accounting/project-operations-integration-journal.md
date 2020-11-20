---
title: Journal for Project Operations-integrering
description: Dette emnet inneholder informasjon om hvordan du arbeider med integreringsjournalen i Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ffe3373184c8cd776bf3705fd674bedf221d9b77
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4133406"
---
# <a name="integration-journal-in-project-operations"></a>Journal for Project Operations-integrering

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Tid og utgifter-oppføringer oppretter **Faktisk**-transaksjoner, som representerer driftsvisningen av arbeid som fullføres mot et prosjekt. Dynamics 365 Project Operations gir regnskapsførere et verktøy for å gjennomgå transaksjoner og justere regnskapsattributtene etter behov. Når gjennomgangen og justeringene er fullført, blir transaksjonene postert til prosjektets underfinansjournal og økonomimodulen. En regnskapsfører kan utføre disse aktivitetene ved hjelp av journalen for **Project Operations-integrering** (**Dynamics 365 Finance** > **Prosjektstyring og regnskap** > **Journaler** > **Project Operations-integrering**-journalen.

![Integreringsjournalflyt](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Opprette oppføringer i journalen for Project Operations-integrering

Oppføringer i journalen for Project Operations-integrering opprettes ved hjelp av periodisk prosess, **Import fra oppsamlingstabell**. Du kan kjøre denne prosessen ved å gå til **Dynamics 365 Finance** > **Prosjektstyring og regnskap** > **Periodisk** > **Project Operations-integrering** > **Import fra oppsamlingstabell**. Du kan kjøre prosessen interaktivt eller konfigurere prosessen til å kjøre i bakgrunnen etter behov.

Når den periodiske prosessen kjører, blir faktiske verdier som ennå ikke er lagt til i journalen for Project Operations-ingetrering, funnet. Det opprettes en journallinje for hver faktiske transaksjon.
Systemet grupperer journallinjer i separate journaler basert på verdien som er valgt i feltet **Periodenhet på journal for Project Operations-integrering** (**Finance** > **Prosjektstyring og regnskap** > **Oppsett** > **Prosjektstyring og regnskapsparametre**, **Project Operations i kategorien Dynamics 365 Customer Engagement**). Mulige verdier for dette feltet inkluderer følgende:

  - _*Dager**: Faktiske verdier er gruppert etter transaksjonsdato. Det opprettes en separat journal for hver dag.
  - **Måneder**: Faktiske verdier grupperes etter kalendermåned. Det opprettes en separat journal for hver måned.
  - **År**: Faktiske verdier grupperes etter kalenderår. Det opprettes en separat journal for hvert år.
  - **Alle**: Alle faktiske transaksjoner er inkludert i samme integreringsjournal. Hvis journalen ikke er tilgjengelig når den periodiske prosessen kjører, for eksempel hvis journalen er i ferd med å postere transaksjoner, opprettes det en ny journal.

Journallinjer opprettes basert på faktiske verdier for prosjekter. Følgende liste inneholder noen av de mer viktige standard- og transformasjonsreglene:

  - Hver faktiske transaksjon for prosjekter har en linje i journalen for Project Operations-integrasjon. Kostnader og ikke-fakturerte salgstransaksjoner for tid og material-faktureringstype vises på separate linjer.
  - **Dato**-feltet representerer transaksjonensdatoen. Feltet **Regnskapsdato** representerer datoen da transaksjonen ble registrert i hovedboken. Hvis regnskapsdatoen er i en [lukket økonomisk periode](https://docs.microsoft.com/dynamics365/finance/general-ledger/close-general-ledger-at-period-end), og parameteren **Angi automatisk regnskapsdato i åpen finansperiode** er satt til kategorien **Økonomisk** på siden for **Prosjektstyring og regnskapsparametere**, blir regnskapsdatoen for transaksjonen justert til den første datoen i neste åpne finansperioden.
  - **Bilag**-feltet viser bilagsnummeret for hver faktiske transaksjon. Bilagsnummerserien defineres i kategorien **Nummersekvenser** på siden for **Prosjektstyring og regnskapsparametre**. Hver linje tilordnes et nytt nummer. Når bilaget er postert, kan du vise hvordan transaksjoner for kostnader og ufakturert salg er relatert ved å velge **Relaterte bilag** på siden **Bilagstransaksjon**.
  - Feltet **Kategori** representerer en prosjekttransaksjon og standarder basert på transaksjonskategorien for det relaterte faktiske prosjektverdien.
    - Hvis **Transaksjonskategori** er angitt i den faktiske verdien for prosjektet og det finnes en relatert **Prosjektkategori** i en gitt juridisk enhet, brukes denne prosjektkategorien som standard.
    - Hvis **Transaksjonskategori** ikke er angitt i den faktiske prosjektverdien, bruker systemet verdien i feltet for **prosjektkategoristandarder** i kategorien **Project Operations på Dynamics 365 Customer Engagement** på siden **Prosjektstyring og regnskapsparametre**.
  - Feltet **Ressurs** representerer prosjektressursen som er relatert til denne transaksjonen. Ressursen brukes som en referanse i prosjektfakturaforslag til kunder.
  - Feltet **Valutakurs** angis som standard fra **Valutakurs** som er angitt i Dynamics 365 Finance. Hvis valutakursoppsettet mangler, vil ikke periodeprosessen **Import fra oppsamling** legge til oppføringen i en journal, og det blir lagt til en feilmelding i jobbkjøringsloggen.
  - Feltet **Linjeegenskap** representerer faktureringstypen i prosjektets faktiske verdier. Linjeegenskap og faktureringstypetilordning defineres i kategorien **Project Operations på Dynamics 365 Customer Engagement** på siden for **Prosjektstyring og regnskapsparametre**.

Bare følgende regnskapsattributter kan oppdateres i journallinjene for Project Operations-integrasjon:

- **Mva-gruppe for fakturering** og **Mva-gruppe for faktureringsvare**
- **Finansdimensjoner** (ved hjelp av **Fordel beløp**-handling)

Integreringsjournallinjer kan slettes, men eventuelle ikke-bokførte linjer settes inn i kladden på nytt etter at du har kjørt den periodiske prosessen **Import fra oppsamling** på nytt.

Når du posterer integreringsjournalen, opprettes det en underfinansjournal for prosjekt og transaksjoner i økonomimodulen. Disse brukes i nedstøms kundefakturering, inntektsføring og finansrapportering.
