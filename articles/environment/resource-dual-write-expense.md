---
title: Integrering av utgiftshåndtering
description: Denne artikkelen inneholder informasjon om integrering av utgiftsrapport i Project Operations ved hjelp av dobbel skriving.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: da37adcf63a10b9f245283d377e70fd08b3aa9c5
ms.sourcegitcommit: 385081ecc839d7d4a557eda2bb1578ca073f7e41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/19/2022
ms.locfileid: "9528017"
---
# <a name="expense-management-integration"></a>Integrering av utgiftshåndtering

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Denne artikkelen inneholder informasjon om integrering av utgiftsrapporter i Project Operations [full utgiftsdistribusjon](../expense/expense-overview.md) ved hjelp av dobbel skriving.

## <a name="expense-categories"></a>Utgiftskategorier

I en full utgiftsdistribusjon opprettes og vedlikeholdes utgiftskategorier i økonomi- og driftsapper. Fullfør følgende trinn for å opprette en ny utgiftskategori:

1. I Microsoft Dataverse oppretter du en **Transaksjon**-kategori. Integrering av dobbel skriving vil synkronisere denne transaksjonskategorien med økonomi- og driftsapper. Hvis du vil ha mer informasjon, kan du se [Konfigurere prosjektkategorier](/dynamics365/project-operations/project-accounting/configure-project-categories) og [Integrering av Project Operations-oppsett og -konfigurasjonsdata](resource-dual-write-setup-integration.md). Som et resultat av denne integrasjonen oppretter systemet fire delte kategorioppføringer i økonomi- og driftsapper.
2. I Økonomi går du til **Utgiftshåndtering** > **Oppsett** > **Delte kategorier** og velger en delt kategori med transaksjonsklassen **Utgift**. Angi **Kan brukes i utgift**-parameteren til **Sann** og definerer utgiftstypen som skal brukes.
3. Bruk denne delte kategorioppføringen til å opprette en ny utgiftskategori ved å gå til **Utgiftshåndtering** > **Oppsett** > **Utgiftskategorier** og velge **Ny**. Når oppføringen lagres, bruker dobbeltskriving tabelltilordningen **eksportenheten for prosjektutgift for Project Operations-integrering (msdyn\_expensecategories)** til å synkronisere denne oppføringen til Dataverse.

  ![Integrering av utgiftskategorier.](./media/DW6ExpenseCategories.png)

Utgiftskategorier i økonomi- og driftsapper er firmaspesifikke eller spesifikke for juridisk enhet. Det finnes separate, tilsvarende juridiske enhetsspesifikke oppføringer i Dataverse. Når en prosjektleder beregner utgifter, kan de ikke velge utgiftskategorier som er opprettet for et prosjekt som eies av et annet firma enn firmaet som eier prosjektet de arbeider med. 

## <a name="expense-reports"></a>Utgiftsrapporter

Kostnadsrapporter opprettes og godkjennes i økonomi- og driftsapper. Hvis du vil ha mer informasjon, kan du se [Opprette og behandle utgiftsrapporter i Dynamics 365 Project Operations](/training/modules/create-process-expense-reports/). Når utgiftsrapporten er godkjent av prosjektlederen, legges den i økonomimodulen. I Project Operations posteres prosjektrelaterte utgiftsrapportlinjer ved hjelp av spesielle posteringsregler:

  - Prosjektrelaterte kostnader (inkludert ikke-reserverbar avgift) legges ikke umiddelbart inn på prosjektkostnadskonto i hovedboken, men posteres i stedet på kontoen for utgiftsintegrering. Denne kontoen konfigureres i **Prosjektstyring og regnskap** > **Oppsett** > **Prosjektstyring og regnskapsparametere**, kategorien **Project Operations i Dynamics 365 Customer Engagement**.
  - Dobbeltskriving synkroniseres til Dataverse ved bruk av tabelltilordningen **eksportenheten for prosjektutgift for Project Operations-integrering (msdyn\_expenses)**.
  - Underordnede avgifter, underleverandører og andre finansielle innlegg registreres etter gjeldende tidspunkt for innlegging av utgiftsrapport.

  ![Integrering av utgiftsrapporter.](./media/DW6ExpenseReports.png)

Når en oppføring skrives til **Utgift**-enheten i Dataverse, utløser systemet den automatiske godkjenningsprosessen for oppføringen. Hvis det er nødvendig, kan den automatiserte godkjenningsprosessstatusen gjennomgås i Dataverse ved å gå til **Avanserte innstillinger** > **System** > **Systemjobber**. Når godkjenningen er fullført, opprettes oppføringer for utgiftstransaksjonsklasse i **Faktiske verdier**-enheten.

Utgiftsrelaterte faktiske verdier behandles deretter ved hjelp av tabelltilordningen med dobbeltskriving **Faktiske verdier for Project Operations-integrering (msdyn\_actuals)**. Hvis du vil ha mer informasjon, se [Prosjektestimater og faktiske verdier](resource-dual-write-estimates-actuals.md).

Den periodiske prosessen **Importer fra oppsamlingstabell** oppretter utgiftsrelaterte journallinjer i journalen for Project Operations-integrering. Forskyvningskontoen er som standard kontoen for utgiftsintegrering. Publiseringsintegreringskladden fjerner kontosaldoen for utgiftstransaksjonen og flytter utgiftsbeløpet til prosjektkostnadskontoen. Systemet oppretter også transaksjoner for underordnet prosjekt for nedstrømsfaking og inntektsføring.
