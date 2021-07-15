---
title: Oversikt over faktureringsprosess
description: Dette emnet inneholder en prosessoversikt over fakturering i Project Operations for ressursbaserte eller ikke-lagerbaserte scenarioer.
author: sigitac
ms.date: 01/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: 0eab33c8640f665555cf5ec5b0f188e5af65a493
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369028"
---
# <a name="invoicing-process-overview"></a>Oversikt over faktureringsprosess

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Project Operations for ressursbaserte/ikke-lagerbeholdte scenarioer tilbyr omfattende funksjoner som er skreddersydd for behovene til både prosjektleder og regnskapssjef/prosjektansvarlig. Når det gjelder faktureringsprosessen, administrerer prosjektlederen prosjektfaktureringsreserven, og regnskapsføreren for utestående fordringer/prosjektregnskapsfører oppretter et kompatibelt og nøyaktig fakturadokument som er rettet mot kunder.

![Faktureringsflytskjema](./media/invoicing-flow.png)

Prosjektkontraktlinjen definerer faktureringsmetoden for tilknyttede prosjekttransaksjoner. Når prosjektlederen godkjenner tids- og utgiftstransaksjoner, registrerer systemet transaksjonene i enheten **Faktiske verdier for prosjekt** og sender informasjonen til modulen **Prosjektstyring og regnskap** i Dynamics 365 Finance. Prosjektregnskapsføreren ser deretter gjennom og publiserer oppføringene ved hjelp av [journalen for Project Operations-integrering](../project-accounting/project-operations-integration-journal.md). Denne loggen inneholder viktige regnskapsdetaljer for faktiske prosjekter, for eksempel fakturering, mva-gruppe, mva-gruppe for faktureringselement og finansdimensjoner.

Prosjektlederen kan gå gjennom ufakturerte salgstransaksjoner ved hjelp av faktureringsmetoden i [Faktureringsrestanse for Tid og materiale](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) og fakturering med fast pris i [Milepæler for fast pris](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Med disse visningene kan du filtrere og velge transaksjoner som må tas med i den neste faktureringssyklusen, og deretter merke dem som **Klar for fakturering**.

Du kan [opprette en proformafaktura manuelt](../proforma-invoicing/create-manual-proforma-invoice.md) eller bruke en [periodisk prosess](../proforma-invoicing/configure-automated-invoice-creation.md). Prosjektlederen kan [justere et utkast til proformafaktura](../proforma-invoicing/manage-proforma-invoice.md) etter behov og deretter bekrefte den.

Den bekreftede proformafakturaen sendes til modulen **Prosjektstyring og regnskap** i Økonomi. Prosjektregnskapsføreren formater og oppdaterer prosjektfakturaforslaget, og legger deretter inn og skriver ut dokumentet. Publiserte prosjektfakturaer registreres i økonomimodulen, i tillegg til undergruppene Kunde og Prosjekt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]