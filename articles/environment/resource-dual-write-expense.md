---
title: Integrering av utgiftshåndtering
description: Dette emnet gir informasjon om integrasjon av utgiftsrapport for Project Operations ved bruk av dobbeltskriving.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7fff69f062bf09fe7ceca61d951b535d2e010bfd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999998"
---
# <a name="expense-management-integration"></a>Integrering av utgiftshåndtering

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Dette emnet gir informasjon om integrasjon av utgiftsrapport for Project Operations [full utgiftsdistribusjon](../expense/expense-overview.md) ved bruk av dobbeltskriving.

## <a name="expense-categories"></a>Utgiftskategorier

I en full utgiftsdistribusjon opprettes og vedlikeholdes utgiftskategorier i Finance and Operations-apper. Fullfør følgende trinn for å opprette en ny utgiftskategori:

1. I Microsoft Dataverse oppretter du en **Transaksjon**-kategori. Integrering av dobbeltskriving synkroniserer denne transaksjonskategorien til Finance and Operations-apper. Hvis du vil ha mer informasjon, kan du se [Konfigurere prosjektkategorier](/dynamics365/project-operations/project-accounting/configure-project-categories) og [Integrering av Project Operations-oppsett og -konfigurasjonsdata](resource-dual-write-setup-integration.md). Som et resultat av denne integrasjonen oppretter systemet fire delte kategorioppføringer i Finance and Operations-apper.
2. I Økonomi går du til **Utgiftshåndtering** > **Oppsett** > **Delte kategorier** og velger en delt kategori med transaksjonsklassen **Utgift**. Angi **Kan brukes i utgift**-parameteren til **Sann** og definerer utgiftstypen som skal brukes.
3. Bruk denne delte kategorioppføringen til å opprette en ny utgiftskategori ved å gå til **Utgiftshåndtering** > **Oppsett** > **Utgiftskategorier** og velge **Ny**. Når oppføringen lagres, bruker dobbeltskriving tabelltilordningen **eksportenheten for prosjektutgift for Project Operations-integrering (msdyn\_expensecategories)** til å synkronisere denne oppføringen til Dataverse.

  ![Integrering av utgiftskategorier](./media/DW6ExpenseCategories.png)

Utgiftskategorier i Finance and Operations-apper er firmaspesifikke eller juridiske. Det finnes separate, tilsvarende juridiske enhetsspesifikke oppføringer i Dataverse. Når en prosjektleder beregner utgifter, kan de ikke velge utgiftskategorier som er opprettet for et prosjekt som eies av et annet firma enn firmaet som eier prosjektet de arbeider med. 

## <a name="expense-reports"></a>Utgiftsrapporter

Utgiftsrapporter opprettes og godkjennes i Finance and Operations-apper. Hvis du vil ha mer informasjon, kan du se [Opprette og behandle utgiftsrapporter i Dynamics 365 Project Operations](/learn/modules/create-process-expense-reports/). Når utgiftsrapporten er godkjent av prosjektlederen, legges den i økonomimodulen. I Project Operations posteres prosjektrelaterte utgiftsrapportlinjer ved hjelp av spesielle posteringsregler:

  - Prosjektrelaterte kostnader (inkludert ikke-reserverbar avgift) legges ikke umiddelbart inn på prosjektkostnadskonto i hovedboken, men posteres i stedet på kontoen for utgiftsintegrering. Denne kontoen konfigureres i **Prosjektstyring og regnskap** > **Oppsett** > **Prosjektstyring og regnskapsparametere**, kategorien **Project Operations i Dynamics 365 Customer Engagement**.
  - Dobbeltskriving synkroniseres til Dataverse ved bruk av tabelltilordningen **eksportenheten for prosjektutgift for Project Operations-integrering (msdyn\_expenses)**.
  - Underordnede avgifter, underleverandører og andre finansielle innlegg registreres etter gjeldende tidspunkt for innlegging av utgiftsrapport.

  ![Integrering av utgiftsrapporter](./media/DW6ExpenseReports.png)

Når en oppføring skrives til **Utgift**-enheten i Dataverse, utløser systemet den automatiske godkjenningsprosessen for oppføringen. Hvis det er nødvendig, kan den automatiserte godkjenningsprosessstatusen gjennomgås i Dataverse ved å gå til **Avanserte innstillinger** > **System** > **Systemjobber**. Når godkjenningen er fullført, opprettes oppføringer for utgiftstransaksjonsklasse i **Faktiske verdier**-enheten.

Utgiftsrelaterte faktiske verdier behandles deretter ved hjelp av tabelltilordningen med dobbeltskriving **Faktiske verdier for Project Operations-integrering (msdyn\_actuals)**. Hvis du vil ha mer informasjon, se [Prosjektestimater og faktiske verdier](resource-dual-write-estimates-actuals.md).

Den periodiske prosessen **Importer fra oppsamlingstabell** oppretter utgiftsrelaterte journallinjer i journalen for Project Operations-integrering. Forskyvningskontoen er som standard kontoen for utgiftsintegrering. Publiseringsintegreringskladden fjerner kontosaldoen for utgiftstransaksjonen og flytter utgiftsbeløpet til prosjektkostnadskontoen. Systemet oppretter også transaksjoner for underordnet prosjekt for nedstrømsfaking og inntektsføring.
