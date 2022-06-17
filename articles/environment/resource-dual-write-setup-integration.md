---
title: Integrering av Project Operations-oppsett og -konfigurasjonsdata
description: Denne artikkelen inneholder informasjon om hvordan du konfigurerer tilordninger med dobbel skriving for Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 173ff01e938af48d2d6488d5e59cf4e74b3af8e4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914552"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Integrering av Project Operations-oppsett og -konfigurasjonsdata

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Denne artikkelen inneholder informasjon om integrering av dobbel skriving i Project Operations for oppsett- og konfigurasjonsenheter.

## <a name="project-contracts-contract-lines-and-projects"></a>Prosjektkontrakter, kontraktlinjer og prosjekter

Prosjektkontrakter, kontraktlinjer og prosjekter opprettes i Dataverse og synkroniseres med økonomi- og driftsapper for ytterligere regnskapsføring. Oppføringene i disse enhetene kan bare opprettes og slettes i Dataverse. Regnskapsattributter, for eksempel standardverdier for salgsavgiftsgrupper og finansdimensjoner, kan imidlertid legges til i oppføringene i økonomi- og driftsapper.

  ![Konsepter for prosjektkontraktintegrering.](./media/1ProjectContract.jpg)

Kundeemner, salgsmuligheter og tilbud for salgsaktiviteter spores i Dataverse og synkroniseres ikke med økonomi- og driftsapper fordi det ikke er knyttet nedstrømsregnskap til denne aktiviteten.

Prosjektkontraktfunksjonaliteten i Dataverse oppretter en prosjektkontraktoppføring i økonomi- og driftsapper ved hjelp av tabelltilordningen **Prosjektkontrakthoder (salesorders)**. Lagring av en prosjektkontrakt i Dataverse starter også opprettingen av en oppføring for en kundeenhet for prosjektkontrakt. Denne oppføringen synkroniseres med økonomi- og driftsapper ved hjelp av tabelltilordningen **Prosjektfinansieringskilde (msdyn\_projectcontractssplitbillingrules)**. Denne tilordningen synkroniserer også tillegg, oppdateringer og slettinger av prosjektkontrakter. Deling av faktureringsprosenter mellom prosjektkontraktkunder håndteres bare i Dataverse og synkroniseres ikke med økonomi- og driftsapper.

Når en prosjektkontrakt er opprettet i Dataverse, kan prosjektregnskapsføreren oppdatere regnskapsattributtene for denne prosjektkontrakten i økonomi- og driftsapper ved å gå til **Prosjektstyring og regnskap** > **Prosjektkontrakter** > **Oppsett** > **Vis standardregnskap**. Regnskapsføreren kan gå gjennom attributter i operasjonelle prosjektkontrakter, for eksempel ønsket leveringsdato og kontraktbeløp, ved å velge prosjektkontrakt-ID-en i økonomi- og driftsapper, som åpner den relaterte prosjektkontraktoppføringen i Dataverse.

Prosjektenheten synkroniseres til økonomi- og driftsapper ved hjelp av tabelltilordningen **Prosjekter V2 (msdyn\_projects)**. Prosjektregnskapsføreren kan gjøre følgende:

  - Gå gjennom prosjekter i økonomi- og driftsapper ved å gå til **Prosjektstyring og regnskap** > **Alle prosjekter**. 
  - Oppdater regnskapsattributter for prosjektet i økonomi- og driftsapper ved å gå til **Prosjektstyring og regnskap** > **Alle prosjekter** > **Oppsett** > **Vis standardregnskap**.  
  - Gå gjennom operasjonelle prosjektattributter, for eksempel beregnet start- og sluttdato, ved å velge prosjekt-ID-en i økonomi- og driftsapper, som åpner den relaterte prosjektoppføringen i Dataverse.

Et prosjekt er knyttet til en prosjektkontrakt via enheten **Prosjektkontraktlinje**.

Prosjektkontraktlinjer i Dataverse oppretter en faktureringsregel for prosjektkontrakt i økonomi- og driftsapper ved hjelp av tabelltilordningen **Prosjektkontraktlinjer (salesorderdetails)**. Faktureringsmetoden definerer faktureringsregeltypen for prosjektkontrakten i økonomi- og driftsapper:

  - Prosjektkontraktlinjer med en faktureringsmetode for tid og materiell oppretter en faktureringsregel med tids- og materialtype.
  - Kontraktlinjer med fast prisfaktureringsmetode oppretter en faktureringsregel for milepæler.

Prosjektkontraktlinjer kan gjennomgås av prosjektregnskapsføreren i økonomi- og driftsapper ved å gå til **Prosjektstyring og regnskap** > **Prosjektkontrakter** > **Oppsett** > **Vis standardregnskap**, og ved å gå gjennom detaljene på **Kontraktlinjer**-fanen. Regnskapsføreren kan også angi standard finansdimensjoner for kontraktlinjer med fast pris som faktureringsmetode på denne fanen.

## <a name="billing-milestones"></a>Faktureringsmilepæler

Prosjektkontraktlinjer som bruker faktureringsmetoden med fast pris, faktureres via faktureringsmilepæler. Faktureringsmilepæler synkroniseres til prosjektkontotransaksjoner i økonomi- og driftsapper ved å bruke tabelltilordningen **Milepæler for prosjektkontraktlinje for Project Operations (msdyn\_contractlinescheduleofvalues)**.

  ![Integrering av faktureringsmilepæler.](./media/2Milestones.jpg)

Regnskapsføreren kan gå gjennom transaksjoner på forretningsforbindelse og justere regnskapsattributtene for disse transaksjonene ved å gå til **Prosjektstyring og regnskap** > **Prosjektkontrakter** > **Oppretthold** > **A konto-transaksjoner** eller **Prosjektstyring og regnskap** > **Alle prosjekter** > **Oppretthold** > **A konto-transaksjoner**.

Når du først oppretter en faktureringsmilepæl for en gitt prosjektkontraktlinje, oppretter systemet automatisk et estimatprosjekt med fast pris for prosjektet som er knyttet til denne kontraktlinjen. Estimatprosjekter for fastprisomsetning kan gjennomgås ved å gå til **Prosjektstyring og regnskap** > **Estimatprosjekter for fastprisomsetning**.

### <a name="project-tasks"></a>Prosjektoppgaver

Prosjektoppgaver synkroniseres til økonomi- og driftsapper via tabelltilordningen **Prosjektoppgaver (msdyn\_projecttasks)** kun til referanseformål. Oppretting, oppdatering og sletting av operasjoner støttes ikke gjennom økonomi- og driftsapper.

  ![Integrasjon av prosjektoppgaver.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Prosjektressurser

Enheten **Prosjektressursroller** synkroniseres med økonomi- og driftsapper ved å bruke tabelltilordningen **Prosjektressursroller for alle firmaer (bookableresourcecategories)** kun til referanseformål. Siden ressursroller i Dataverse ikke er firmaspesifikke, oppretter systemet automatisk respektive firmaspesifikke ressursrolleoppføringer i økonomi- og driftsapper for alle juridiske enheter, inkludert i integreringsomfanget med dobbel skriving.

![Integrasjon av ressursroller.](./media/5Resources.jpg)

Prosjektressurser i Project Operations vedlikeholdes i Dataverse og synkroniseres ikke til økonomi- og driftsapper.

### <a name="transaction-categories"></a>Transaksjonskategorier

Transaksjonskategorier vedlikeholdes i Dataverse og synkroniseres til økonomi- og driftsapper ved hjelp av tabelltilordningen **Transaksjonskategorier for prosjekter (msdyn\_transactioncategories)**. Når transaksjonskategorioppføringen er synkronisert, oppretter systemet automatisk fire delte kategorioppføringer. Hver oppføring tilsvarer en transaksjonstype i økonomi- og driftsapper og kobler dem til transaksjonskategorioppføringen.

![Integrasjon av transaksjonskategorier.](./media/4TransactionCategories.jpg)

Bruk av transaksjonskategorier til estimater og faktiske verdier krever at prosjektregnskapsføreren eller systemadministrator oppretter tilsvarende prosjektkategorier i hver juridiske enhet. Hvis du vil ha mer informasjon, kan du se [Konfigurere prosjektkategorier](../project-accounting/configure-project-categories.md).
