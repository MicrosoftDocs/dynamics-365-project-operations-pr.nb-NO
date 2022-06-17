---
title: Funksjonsendringer fra Project Service Automation til Project Operations
description: Denne artikkelen gir en oversikt over funksjonsendringene fra Project Service Automation til Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
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
ms.openlocfilehash: 8a6030faf777051ea1003679589af4bdf97322ab
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925362"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Funksjonsendringer fra Project Service Automation til Project Operations

Oppgraderingen fra Dynamics 365 Project Service Automation til Dynamics 365 Project Operations Lite blir levert i tre faser. Denne artikkelen inneholder informasjon om de viktigste endringene du kan forvente å se når oppgraderingen er fullført.

| Oppgraderingslevering | Fase 1 <br>(Januar 2022) | Fase 2 <br>(Aprilbølgen i 2022) | Fase 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Ingen avhengighet av arbeidsnedbrytningsstrukturen (WBS) for prosjekter. | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS er inkludert innen gjeldende støttede grenser for Project Operations. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| WBS utenfor gjeldende støttede grenser for Project Operations, inkludert støtte for Project Desktop Client. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Prosjektledelse

De viktigste endringene i brukeropplevelsen vil være innen prosjektplanlegging. Project Operations tar i bruk en ny moderne opplevelse ved administrasjon av en WBS-struktur (arbeidsnedbrytningsstruktur) ved å bruke planleggingsmulighetene fra [Project for the Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Forskjeller i planleggingserfaringen

Tabellen nedenfor oppsummerer planleggingsforskjellene mellom Project Service Automation og Project Operations.

|  Planlegging     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| Prosjektmaler – Mulighet til å definere og bruke prosjektmaler når et prosjekt opprettes  |  &nbsp;    | :heavy_check_mark: |
| Integrering av arbeidsnedbrytningsstruktur (WBS) med klient for stasjonær datamaskin   |    &nbsp;  | :heavy_check_mark: |
| Begrensninger – Start tidligst, Fullfør senest  | :heavy_check_mark: |   &nbsp;  |
| Milepæler – Oppgaver med null varighet   | :heavy_check_mark:  |  &nbsp;  |
| Ressursdrevne oppgaver vil respektere tilgjengeligheten av tildelte ressurser   | :heavy_check_mark: |  &nbsp;    |
| Tidsfaset redigering – Rediger planer og arbeid daglig   |   &nbsp;  | :heavy_check_mark: |
| Automatisk/manuell planlegging – Bruk prosjektplanleggingsmotoren til å planlegge oppgaver automatisk eller manuelt |  &nbsp; | :heavy_check_mark:  |
| Rediger store prosjekter direkte i brukergrensesnittet: Det er ingen begrensninger på størrelsen av planer som kan redigeres  | Grense på 500 oppgaver  | :heavy_check_mark:       |
| Prosent fullført – Merk oppgavefremdrift   | :heavy_check_mark:  |  &nbsp;  |
| [Tidsplanmoduser for prosjekt](../project-management/scheduling-modes.md) – Definer prosjektet som faste enheter, fast innsats eller fast varighet | :heavy_check_mark: | &nbsp; |
| Tidslinje – Bygg og tilpass tidslinjevisningen for å visualisere tidsplandetaljer og kommunisere med interessenter. | :heavy_check_mark:  | &nbsp; |
| Innsatsdrevne oppgaver – Planleggingsmotorstøtte for planlegging av en oppgave som innsatsdrevet  | :heavy_check_mark:  | &nbsp; |
| Dialogboksen **Oppgaveinformasjon** – Lagre oppgavedetaljer ved hjelp av en dialogboks | :heavy_check_mark:  |  &nbsp;  |
| Dra og slipp – Multivelg oppgaver, og endre posisjonen deres på WBS | :heavy_check_mark: | &nbsp;  |
| Fleksible vedvarende visninger – Definer mer detaljerte visninger av oppgaveattributter   | :heavy_check_mark:  | &nbsp; |
| Sorter og filtrer WBS  | :heavy_check_mark:  | &nbsp; |
| Tavlevisning for prosjektlevering uten fossefall  | :heavy_check_mark:   | &nbsp; |
| Tidslinjevisning – Interaktivt Gantt-diagram brukt til å visualisere og redigere WBS-en   | :heavy_check_mark:  | &nbsp; |
| Hurtigtaster – Bruk hurtigtaster til vanlige operasjoner, for eksempel innrykk eller innsetting  | :heavy_check_mark:  |  &nbsp; |
| Angre på flere nivåer – Utfør hva-skjer-hvis-analyse for å forstå virkningen av endringer ved å reversere og bruke et helt sett med operasjoner på nytt | :heavy_check_mark: | &nbsp; |
| Klipp ut / Kopier / Lim inn – Samarbeid om tidsplanutvikling ved å kopiere og lime inn tidsplandetaljer mellom apper  | :heavy_check_mark: | &nbsp; |
| Sjekklister for oppgaver – Legg til opptil 20 sjekklisteelementer i en oppgave   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Prosjektplanlegging

**Prosjekt**-siden i Project Operations har et betydelig antall forskjeller sammenlignet med **Prosjekt**-siden i Project Service Automation.

Følgende handlinger er fjernet fra **Prosjekter**-siden som en del av fase 1 av oppgraderingen:

  - **Åpne i MS Project**
  - **Opprett mal**
  - **Koble fra MS Project**

**Prosjekt**-siden i Project Operations inneholder følgende nye faner.

- **Materialestimater**
- **Faktureringsoppsett for oppgave**

**Status**-fanen er fjernet, og **Status**-feltet finnes nå på **Sammendrag**-fanen med planleggingsmodusen for prosjektet.

   ![Oppdateringer på Prosjekt-siden.](media/projectform.png)

**Tidsplan**-fanen har fått endret navnet til **Oppgave**-fanen, og den inneholder den nye prosjektplanleggingsopplevelsen med Project for the Web.

   ![Fanen Nye prosjektoppgaver.](media/tasktab.png)

## <a name="scheduling-modes"></a>Planleggingsmoduser

Project Operations har innført en ny funksjon, [Planleggingsmoduser](../project-management/scheduling-modes.md). Alle eksisterende Project Service Automation-prosjekter vil som standard være angitt til **Fast varighet** i Project Operations. Standarden for nye prosjekter kan imidlertid administreres ved å gå til **Innstillinger** > **Parametere** > **Parameter** > **Planleggingsmodus**.

   ![Innstillinger for prosjektparametere for planleggingsmodus.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Grenser for prosjektplanlegging

Project Operations er avhengig av Project for the Web for alle prosjektplanleggingsoperasjoner. Project for the Web styrer arbeidsnedbrytningsstrukturen ved hjelp av grensene i tabellen nedenfor.

| **Felt**                                          | **Grense**             |
|----------------------------------------------------|-----------------------|
| Maksimalt antall oppgaver for et prosjekt                  | 500                   |
| Maksimal total varighet for et prosjekt               | 3650 dager (10 år)  |
| Maksimalt antall ressurser for et prosjekt              | 300                   |
| Maksimalt antall koblinger (bare etterfølgende) for et prosjekt | 600                   |
| Maksimalt antall egendefinerte felter for et prosjekt          | 10                    |
| Maksimalt antall hierarkinivåer                            | 10 nivåer             |
| Maksimal antall koblinger (etterfølgene + foregående)            | 20                    |
| Maksimal varighet for bladoppgave                      | 1250 dager             |
| Maksimal varighet for en sammendragsoppgave                 | 3650 dager (10 år)  |
| Maksimalt antall ressurser tilordnet til en oppgave               | 20 ressurser          |
| Støttet datointervall for en oppgave                    | 1/1/2000 til 31/12/2149 |
| Sjekklistepunkter                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>Utvidbarhet og utvikling av prosjektplanlegging

Når du har oppgradert til Project Operations, må du bruke API-ene for prosjektplanlegging til å kjøre operasjoner for oppretting, oppdatering og sletting for følgende enheter:

|   Enhetsnavn           |   Logisk navn for enhet       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Prosjektoppgave            | msdyn_projecttask           |
| Avhengighet for prosjektoppgaver | msdyn_projecttaskdependency |
| Ressurstilordning     | msdyn_resourceassignment    |
| Prosjektsamling          | msdyn_projectbucket         |
| Prosjektteammedlem     | msdyn_projectteam           |

Hvis du for øyeblikket har tilpassinger som omfatter disse enhetene, kan du se [Bruk API-er for prosjektplan til å utføre operasjoner med planleggingsenheter](../project-management/schedule-api-preview.md) for implementeringsveiledning.

## <a name="data-model-changes"></a>Endringer i datamodellen

Som en del av fase 1 av oppgraderingen er det endringer i datamodellen. Disse endringene er først og fremst feltendringer for eksisterende enheter. I fase 1 er enhetene **msydn_project** og **msdyn_projectteam** en refaktorering av tilpasninger. 

> [!IMPORTANT]
> Denne delen oppdateres med flere enheter etter hvert som fremtidige oppgraderingsfaser er fullført.

Følgende felter er erstattet med nye felter:

|   Entity          |   Gammelt logisk navn   |   Nytt logisk navn    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

Følgende felter er lagt til:

|   Entity          |   Logisk navn                               |   Bekrivelse |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Viser aggregatet av faktiske avgiftssalg på prosjektet. Bare for bruk i Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialcost                     | Viser aggregatet av den faktiske materialkostnaden på prosjektet. Bare for bruk i Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialsales                    | Viser aggregatet av faktiske materialsalg på prosjektet. Bare for bruk i Project Service Automation. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | Kontraktlinjen som er knyttet til dette prosjektet. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Dette er et internt systemfelt som brukes for **Kopier prosjekt** relatert til korrelasjonsidentifikatoren. Bare for bruk i Project Service Automation. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Dette er et internt systemfelt, brukt for **Kopier prosjekt** relatert til øktidentifikatoren. Bare for bruk i Project Service Automation. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Siste synkroniserte globale xRM-revisjonstoken fra prosjektplanleggingstjenesten. |
| msdyn_project     | msdyn_msprojectdocument                      | Microsoft Project-dokumentet som tilhører prosjektet. |
| msdyn_project     | msdyn_plannedmaterialcost                    | Aggregatet av den planlagte materialkostnaden på prosjektet. Bare for bruk i Project Service Automation. |
| msdyn_project     | msdyn_plannedmaterialsales                   | Aggregatet av den planlagte salgskostnaden på prosjektet. Bare for bruk i Project Service Automation. |
| msdyn_project     | msdyn_program                                | Programmet dette prosjektet er relatert til. |
| msdyn_project     | msdyn_quotelineproject                       | Tilbudslinjen som er knyttet til dette prosjektet. |
| msdyn_project     | msdyn_replaylogheader                        | Toppteksten for loggene for ny avspilling. |
| msdyn_project     | msdyn_schedulemode                           | Standard planleggingsmodus som brukes for alle oppgaver på prosjektet.  |
| msdyn_project     | msdyn_taskearlieststart                      | Den tidligste startdatoen for en oppgave i prosjektet.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Prosjektteammedlemmet som dette prosjektteammedlemmet ble kopiert fra. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Angir om ressurskravet skal opprettes for et nylig opprettet generelt teammedlem.  |
| msdyn_projectteam | msdyn_deletestatus                           | Slettestatusen for teammedlemmet for å spore om det er sendt en sletteforespørsel til prosjektplanleggingstjenesten, og om den sender tilbake et svar innen det forventede tidsrommet. |
| msdyn_projectteam | msdyn_effortcompleted                        | Sporer innsatsen som teammedlemmet har gjort i tilordningene. |
| msdyn_projectteam | msdyn_effortremaining                        | Sporer innsatsen som teammedlemmet har igjen i tilordningene. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Venteperioden fra teammedlemmet sender en forespørsel om sletting til prosjektplanleggingstjenesten til teammedlemmet faktisk slettes i Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Tidsstempelet som skal registreres når teammedlemmets sletteforespørsel sendes til prosjektplanleggingstjenesten. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Viser prosjektteammedlemmet som dette prosjektteammedlemmet ble kopiert fra.  |

## <a name="project-templates"></a>Prosjektmaler

Project Operations støtter ikke prosjektmaler. Du kan imidlertid replikere mye av kjernefunksjonaliteten ved hjelp av [API-en for prosjektkopiering](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Støtte for Desktop-tillegget

Støtte for Microsoft Project Desktop-tillegget er ikke tilgjengelig i de to første fasene av oppgraderingen. I fase 3 vil kunder som har prosjekter som er større enn de gjeldende grensene for Project for the Web, kunne bruke tillegget for stasjonær datamaskin.

## <a name="editing-resource-assignment-contours"></a>Redigering av ressurstilordningsomfang

Muligheten til å redigere ressurstilordningsomfang vil være tilgjengelig når fase 2 av oppgraderingen er tilgjengelig.

## <a name="billing-and-pricing"></a>Fakturering og prising

Følgende nye funksjoner er lagt til i Project Operations. Disse funksjonene er additive av natur og har ikke innvirkning på Project Service Automation-datamodellen.

- [Registrering av materialbruk på prosjekter og prosjektoppgaver](../material/material-usage-log.md)
- [Administrasjon av underkontrakt](../pro/subcontracting/managing-subcontracts-overview.md)
- [Forskudd og honorarbaserte kontrakter](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Må ikke overskrides-status og valideringer for kontrakt](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Oppgavebasert fakturering](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Avskrevne komponenter

Tabellene nedenfor dokumenterer alle avskrevne felter som er flyttet til løsningen for avskrevne komponenter etter oppgradering. Hvis du vil ha mer informasjon og en kobling til løsningen, kan du se [Avskrevne komponenter i Dynamics 365 Project Service Automation 3x til Project Operations 4x](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>invoicedetail

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

