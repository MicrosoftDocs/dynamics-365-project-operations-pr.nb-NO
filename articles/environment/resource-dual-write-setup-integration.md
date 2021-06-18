---
title: Integrering av Project Operations-oppsett og -konfigurasjonsdata
description: Dette emnet gir informasjon om hvordan du konfigurerer tilordninger for dobbel skriving for Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1e9ca9407404274648f359be42d350137775ae55
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001078"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Integrering av Project Operations-oppsett og -konfigurasjonsdata

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Dette emnet gir informasjon om dobbeltskrivingsintegrasjon for Project Operations for oppetts- og konfigurasjonsenheter.

## <a name="project-contracts-contract-lines-and-projects"></a>Prosjektkontrakter, kontraktlinjer og prosjekter

Prosjektkontrakter, kontraktlinjer og prosjekter opprettes i Dataverse og synkroniseres til Finance and Operations-apper for ekstra regnskap. Oppføringene i disse enhetene kan bare opprettes og slettes i Dataverse. Regnskapsattributter, for eksempel standardverdier for salgsavgiftsgrupper og finansdimensjoner, kan imidlertid legges til i oppføringene i Finance and Operations-appene.

  ![Konsepter for prosjektkontraktintegrering](./media/1ProjectContract.jpg)

Kundeemner, salgsmuligheter og tilbud for salgsaktiviteter spores i Dataverse og synkroniseres ikke til Finance and Operations-apper fordi det ikke er knyttet nedstrømsregnskap til denne aktiviteten.

Prosjektkontraktfunksjonaliteten i Dataverse oppretter en prosjektkontraktoppføring i Finance and Operations-apper ved hjelp av tabelltilordningen **Prosjektkontrakthoder (salgsordrer)**. Lagring av en prosjektkontrakt i Dataverse starter også opprettingen av en oppføring for en kundeenhet for prosjektkontrakt. Denne oppføringen synkroniseres til Finance and Operations-apper ved hjelp av tabelltilordningen **Prosjektfinansieringskilde (msdyn\_projectcontractssplitbillingrules)**. Denne tilordningen synkroniserer også tillegg, oppdateringer og slettinger av prosjektkontrakter. Deling av faktureringsprosenter mellom prosjektkontraktkunder opprettes bare i Dataverse og synkroniseres ikke til Finance and Operations-apper.

Når en prosjektkontrakt er opprettet i Dataverse, kan prosjektregnskapsføreren oppdatere regnskapsattributtene for denne prosjektkontrakten i Finance and Operations-apper ved å gå til **Prosjektstyring og regnskap** > **Prosjektkontrakter** > **Konfigurer** > **Vis standardregnskap**. Regnskapsføreren kan gå gjennom attributter for operasjonell prosjektkontrakt, for eksempel ønsket leveringsdato og kontraktbeløp, ved å velge prosjektkontrakt-ID-en i Finance and Operations-apper som åpner den relaterte prosjektkontraktoppføringen i Dataverse.

Prosjektenheten synkroniseres til Finance and Operations-apper ved hjelp av tabelltilordningen **Prosjekter V2 (msdyn\_projects)**. Prosjektregnskapsføreren kan gjøre følgende:

  - Gå gjennom prosjekter i Finance and Operations-apper ved å gå til **Prosjektstyring og regnskap** > **Alle prosjekter**. 
  - Oppdatere regnskapsattributter for prosjektet i Finance and Operations-apper ved å gå til **Prosjektstyring og regnskap** > **Alle prosjekter** > **Konfigurer** > **Vis standardregnskap**.  
  - Gå gjennom operasjonelle prosjektattributter, for eksempel beregnet start- og sluttdato, ved å velge prosjekt-ID-en i Finance and Operations-apper som åpner den relaterte prosjektoppføringen i Dataverse.

Et prosjekt er knyttet til en prosjektkontrakt via enheten **Prosjektkontraktlinje**.

Prosjektkontraktlinjer i Dataverse oppretter en prosjektkontraktfaktureringsregel i Finance and Operations-apper ved hjelp av tabelltilordningen **Prosjektkontraktlinjer (salgsordredetaljer)**. Faktureringsmetoden definerer regeltypen for prosjektkontraktfakturering i Finance and Operations-apper:

  - Prosjektkontraktlinjer med en faktureringsmetode for tid og materiell oppretter en faktureringsregel med tids- og materialtype.
  - Kontraktlinjer med fast prisfaktureringsmetode oppretter en faktureringsregel for milepæler.

Prosjektkontraktlinjer kan gjennomgås av prosjektregnskapsføreren i Finance and Operations-apper ved å gå til **Prosjektstyring og regnskap** > **Prosjektkontrakter** > **Konfigurer** > **Vis standardregnskap**, og se gjennom detaljene i kategorien **Kontraktlinjer**. Regnskapsføreren kan også angi standard finansdimensjoner for kontraktlinjer med fast prisfaktureringsmetode i denne kategorien.

## <a name="billing-milestones"></a>Faktureringsmilepæler

Prosjektkontraktlinjer som bruker faktureringsmetoden med fast pris, faktureres via faktureringsmilepæler. Faktureringsmilepæler synkroniseres for å prosjektere A konto-transaksjoner i Finance and Operations-apper ved hjelp av tabelltilordningen **Kontraktlinjemilepæler for Project Operations-integrering (msdyn\_contractlinescheduleofvalues)**.

  ![Integrering av faktureringsmilepæler](./media/2Milestones.jpg)

Regnskapsføreren kan gå gjennom transaksjoner på forretningsforbindelse og justere regnskapsattributtene for disse transaksjonene ved å gå til **Prosjektstyring og regnskap** > **Prosjektkontrakter** > **Oppretthold** > **A konto-transaksjoner** eller **Prosjektstyring og regnskap** > **Alle prosjekter** > **Oppretthold** > **A konto-transaksjoner**.

Når du først oppretter en faktureringsmilepæl for en gitt prosjektkontraktlinje, oppretter systemet automatisk et estimatprosjekt med fast pris for prosjektet som er knyttet til denne kontraktlinjen. Estimatprosjekter for fastprisomsetning kan gjennomgås ved å gå til **Prosjektstyring og regnskap** > **Estimatprosjekter for fastprisomsetning**.

### <a name="project-tasks"></a>Prosjektoppgaver

Prosjektoppgaver synkroniseres til Finance and Operations-apper via tabelltilordningen **Prosjektoppgaver (msdyn\_projecttasks)** bare for referanseformål. Opprettings-, oppdaterings- og slettingsoperasjoner støttes ikke via Finance and Operations-apper.

  ![Integrasjon av prosjektoppgaver](./media/3Tasks.jpg)

## <a name="project-resources"></a>Prosjektressurser

Enheten **Prosjektressursroller** synkroniseres til Finance and Operations-apper ved hjelp av tabelltilordningen **Prosjektressursroller for alle selskaper (bookableresourcecategories)** bare for referanseformål. Siden ressursroller i Dataverse ikke er firmaspesifikke, oppretter systemet automatisk respektive firmaspesifikke ressursrolleoppføringer i Finance and Operations-apper automatisk for alle juridiske enheter inkludert i integrasjonsomfanget for dobbel skriving.

![Integrasjon av ressursroller](./media/5Resources.jpg)

Prosjektressurser i Project Operations vedlikeholdes i Dataverse og synkroniseres ikke til Finance and Operations-apper.

### <a name="transaction-categories"></a>Transaksjonskategorier

Transaksjonskategorier vedlikeholdes i Dataverse og synkroniseres til Finance and Operations-apper ved hjelp av tabelltilordningen **Prosjekttransaksjonskategorier (msdyn\_transactioncategories)**. Når transaksjonskategorioppføringen er synkronisert, oppretter systemet automatisk fire delte kategorioppføringer. Hver oppføring tilsvarer en transaksjonstype i Finance and Operations-apper og kobler dem til transaksjonskategorioppføringen.

![Integrasjon av transaksjonskategorier](./media/4TransactionCategories.jpg)

Bruk av transaksjonskategorier til estimater og faktiske verdier krever at prosjektregnskapsføreren eller systemadministrator oppretter tilsvarende prosjektkategorier i hver juridiske enhet. Hvis du vil ha mer informasjon, kan du se [Konfigurere prosjektkategorier](../project-accounting/configure-project-categories.md).
