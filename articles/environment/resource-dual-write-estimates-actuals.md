---
title: Integrering av prosjektestimater og faktiske verdier
description: Dette emnet gir informasjon om dobbeltskrivingsintegrasjon for Project Operations for prosjektestimater og faktiske data.
author: sigitac
manager: Annbe
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 88df3385fac0a78a827d65a77d3b04c9d6499536
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955804"
---
# <a name="project-estimates-and-actuals-integration"></a>Integrering av prosjektestimater og faktiske verdier

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Dette emnet gir informasjon om dobbeltskrivingsintegrasjon for Project Operations for prosjektestimater og faktiske data.

## <a name="project-estimates"></a>Prosjektestimater

Prosjektarbeid, utgifter og materialestimater opprettes og vedlikeholdes i Microsoft Dataverse og synkroniseres med Finance and Operations-apper for regnskapsformål. Opprettings-, oppdaterings- og sletteoperasjoner støttes ikke gjennom Finance and Operations-appene.

Oppretting av estimater krever en gyldig regnskapskonfigurasjon for prosjektet. Prosjekter som er tilknyttet kontraktlinjer, må ha en gyldig prosjektkostnads- og omsetningsprofil definert i reglene for prosjektkostnads- og omsetningsprofil. Hvis du vil ha mer informasjon, kan du se [Konfigure regnskap for fakturerbare prosjekter](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Arbeidsestimater

Arbeidestimater opprettes av prosjektlederen eller ressurslederen som også tilordner en generell eller navngitt ressurs til prosjektoppgaven. Du kan se gjennom ressurstilordningsoppføringer i kategorien **Ressurstilordninger** på **Prosjektdetaljer**-siden i Dataverse. Ressurstilordningsoppføringer i Dataverse oppretter timeprognoseoppføringer i Finance and Operations-apper ved hjelp av **Project Operations-integreringsenheten for timeestimater (msdyn\_resourceassignments)**.

   ![Integrering av arbeidsestimater](./Media/DW4LaborEstimates.png)

Dobbeltskriving synkroniserer ressurstilordningsoppføringer til oppsamlingstabellen (**ProjCDSEstimateHoursImport**), og bruker deretter forretningslogikk til å opprette og oppdatere timeprognoseoppføringer (**ProjForecastEmpl**).

Prosjektregnskapsføreren ser gjennom prognosetidsoppføringer som er opprettet i Finance and Operations-apper, ved å gå til **Prosjektstyring og regnskap** > **Alle prosjekter** > **Plan** > **Timeprognoser**.

## <a name="expense-estimates"></a>Utgiftsestimater

Kostnadsestimater opprettes av prosjektlederen i kategorien **Kostnadsestimater** på **Prosjektdetaljer**-siden i Dataverse. Oppføringer for kostnadsestimater lagres i enheten **Estimatlinje** i Dataverse. Disse estimatoppføringene har transaksjonsklasse, **Utgift** og synkroniseres til utgiftsprognoseoppføringer i Finance and Operations-apper ved hjelp av **Project Operations-integrasjonsenheten for utgiftsestimater (msdyn\_estimatelines)**.

   ![Integrering av utgiftsestimater](./Media/DW4ExpenseEstimates.png)

Dobbeltskriving synkroniserer utgiftsestimatsoppføringer til oppsamlingstabellen **ProjCDSEstimateExpenseImport)**, og bruker deretter forretningslogikk til å opprette og oppdatere utgiftsprognoseoppføringer (**ProjForecastCost**). Estimatlinjer lagrer oppføringer for salgsestimater og kostnadsestimater separat. Forretningslogikken i Finance and Operations-apper fyller ut én enkelt utgiftsprognoseoppføring ved hjelp av denne detaljen i oppsamlingstabellen.

Prosjektregnskapsføreren kan se gjennom utgiftsprognoseoppføringer i Finance and Operations-apper, ved å gå til **Prosjektstyring og regnskap** > **Alle prosjekter** > **Plan** > **Utgiftsprognoser**.

## <a name="material-estimates"></a>Materialestimater

Materialestimater opprettes av prosjektlederen i kategorien **Materialestimater** på **Prosjektdetaljer**-siden i Dataverse. Oppføringer for materialestimater lagres i enheten **Estimatlinje** i Dataverse. Disse estimatoppføringene har transaksjonsklassen **Material** og synkroniseres til vareprognoseoppføringer i Finance and Operations-apper ved hjelp av **Project Operations-integrasjonstabellen for materialestimater (msdyn\_estimatelines)**.

   ![Integrering av materialestimater](./Media/DW4MaterialEstimates.png)

Dobbeltskriving synkroniserer materialestimatsoppføringer til oppsamlingstabellen **ProjForecastSalesImpor**, og bruker deretter forretningslogikk til å opprette og oppdatere vareprognoseoppføringer (**ForecastSales**). Estimatlinjer lagrer oppføringer for salgsestimater og kostnadsestimater separat. Forretningslogikken i Finance and Operations-apper fyller ut én enkelt vareprognoseoppføring ved hjelp av denne detaljen i oppsamlingstabellen.

Prosjektregnskapsføreren kan se gjennom vareprognoseoppføringer i Finance and Operations-apper, ved å gå til **Prosjektstyring og regnskap** > **Alle prosjekter** > **Plan** > **Vareprognoser**.

## <a name="project-actuals"></a>Faktiske verdier for prosjekt

Faktiske prosjekter opprettes i Dataverse, basert på tid, utgifter, materiell og faktureringsaktivitet. Alle driftsattributter for disse transaksjonene, inkludert antall, kostnadspris, salgspris og prosjekt, registreres i denne Dataverse-enheten. Du finner mer informasjon i [Faktiske verdier](../actuals/actuals-overview.md). Faktiske oppføringer synkroniseres til Finance and Operations-apper ved hjelp av tabelltilordningen for dobbeltskriving **Faktiske verdier for Project Operations-integrering (msdyn\_actuals)** for nedstrømsregnskap.

   ![Integrering av faktiske verdier](./Media/DW4Actuals.png)

Tabelltilordningen for **faktiske verdier for Project Operations-integrering** synkroniserer alle oppføringene fra **Faktiske verdier**-enheten i Dataverse, med attributtet **Hopp over synkronisering (bare internt bruk)** satt til **Usann**. Denne attributtverdien angis automatisk i Dataverse når oppføringen opprettes. Eksempler der dette attributtet er satt til **Sann**, er:

  - Faktiske prosjektkostnader for firmatransaksjoner. Hvis du vil ha mer informasjon, kan du se [Opprette konserninterne transaksjoner](../project-accounting/create-intercompany-transactions.md). Disse oppføringene hoppes over fordi systemet gjenskaper de faktiske prosjektkostnadene i Finance and Operations-apper når den konserninterne leverandørfakturaen posteres.
  - Negative, ikke-fakturerte salgsoppføringer opprettes når proformafakturaen bekreftes. Disse oppføringene hoppes over fordi underbilaget for prosjekter i Finance and Operations-apper ikke reverserer den ikke-fakturerte salgsoppføringen ved fakturering, men endrer statusen til fullt fakturert.

Tabelltilordningen med dobbeltskriving synkroniserer de faktiske oppføringene til oppsamlingstabellen **ProjCDSActualsImport**. Disse oppføringene behandles av den periodiske prosessen **Importer fra oppsamlingstabell** når du oppretter journallinjer for integrering av Project Operations og prosjektfakturaforslagslinjer. Hvis du vil ha mer informasjon, kan du se [Journal for Project Operations-integrering](../project-accounting/project-operations-integration-journal.md).

Dataverse registrerer også koblingene mellom de faktiske transaksjonene for prosjekt i enheten **Transaksjonstilkobling**. Hvis du vil ha mer informasjon, kan du se [Koble faktiske verdier til opprinnelige oppføringer](../actuals/linkingactuals.md). Koblinger mellom faktiske transaksjoner synkroniseres også til Finance and Operations-apper ved hjelp av tabellkartet for dobbeltskriving, **Integrasjonsenhet for prosjekttransaksjonsrelasjoner (msdyn\_transactionconnections)**. Disse oppføringene brukes av den periodiske prosessen **Importer fra oppsamlingstabell** når du oppretter journallinjer for integrering av Project Operations og prosjektfakturaforslagslinjer.

Når du legger inn en integreringsjournal for Project Operations og et prosjektfakturaforslag, utløses en oppdatering i de respektive oppføringene i oppsamlingstabellen, **ProjCDSActualsImport**. Systemet registrerer følgende regnskapsattributter for faktiske transaksjoner:

- Regnskapsvalutabeløp
- Valutakurs
- Bilagsnummer
- Mva-beløp

Tabelltilordningen **Faktiske verdier for Project Operations-integrering** oppdaterer respektive faktiske oppføringsverdier i Dataverse med denne informasjonen.
