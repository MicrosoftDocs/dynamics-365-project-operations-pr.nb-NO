---
title: Oversikt over faktureringsprosess
description: Denne artikkelen gir en prosessoversikt over fakturering i Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer.
author: sigitac
ms.date: 01/29/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 6b285a88be14a5972e9a4604713d7d35a3a442b6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923108"
---
# <a name="invoicing-process-overview"></a>Oversikt over faktureringsprosess

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Project Operations for ressursbaserte/ikke-lagerbeholdte scenarioer tilbyr omfattende funksjoner som er skreddersydd for behovene til både prosjektleder og regnskapssjef/prosjektansvarlig. Når det gjelder faktureringsprosessen, administrerer prosjektlederen prosjektfaktureringsreserven, og regnskapsføreren for utestående fordringer/prosjektregnskapsfører oppretter et kompatibelt og nøyaktig fakturadokument som er rettet mot kunder.

![Faktureringsflytskjema.](./media/invoicing-flow.png)

Prosjektkontraktlinjen definerer faktureringsmetoden for tilknyttede prosjekttransaksjoner. Når prosjektlederen godkjenner tids- og utgiftstransaksjoner, registrerer systemet transaksjonene i enheten **Faste verdier for prosiekt** og sender informasjonen til modulen **Prosjektstyring og regnskap** i Dynamics 365 Finance. Prosjektregnskapsføreren ser deretter gjennom og publiserer oppføringene ved hjelp av [journalen for Project Operations-integrering](../project-accounting/project-operations-integration-journal.md). Denne loggen inneholder viktige regnskapsdetaljer for faktiske prosjekter, for eksempel fakturering, mva-gruppe, mva-gruppe for faktureringselement og finansdimensjoner.

Prosjektlederen kan gå gjennom ufakturerte salgstransaksjoner ved hjelp av faktureringsmetoden i [Faktureringsrestanse for Tid og materiale](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) og fakturering med fast pris i [Milepæler for fast pris](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Med disse visningene kan du filtrere og velge transaksjoner som må tas med i den neste faktureringssyklusen, og deretter merke dem som **Klar for fakturering**.

Du kan [opprette en proformafaktura manuelt](../proforma-invoicing/create-manual-proforma-invoice.md) eller bruke en [periodisk prosess](../proforma-invoicing/configure-automated-invoice-creation.md). Prosjektlederen kan [justere et utkast til proformafaktura](../proforma-invoicing/manage-proforma-invoice.md) etter behov og deretter bekrefte den.

Den bekreftede proformafakturaen sendes til modulen **Prosjektstyring og regnskap** i Økonomi. Prosjektregnskapsføreren formater og oppdaterer prosjektfakturaforslaget, og legger deretter inn og skriver ut dokumentet. Publiserte prosjektfakturaer registreres i økonomimodulen, i tillegg til undergruppene Kunde og Prosjekt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]