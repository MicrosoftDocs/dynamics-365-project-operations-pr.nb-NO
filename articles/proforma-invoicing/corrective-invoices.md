---
title: Korrigerte fakturaer
description: Dette emnet inneholder informasjon om korrigerte fakturaer.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e14da1c07d5b697de6caf1b9041c30581ecff102
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898093"
---
# <a name="corrected-invoices"></a>Korrigerte fakturaer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Bekreftede fakturaer kan redigeres. Når du redigerer en bekreftet faktura, opprettes det et korrigert fakturautkast. Fordi det antas at du vil tilbakeføre alle transaksjonene og antallene fra den opprinnelige fakturaen, inneholder denne korrigerte fakturaen alle transaksjonene fra den opprinnelige fakturaen, og alle antallene i den er 0 (null).

Hvis noen av transaksjonene ikke krever rettelser, kan du fjerne dem fra det korrigerte fakturautkastet. Hvis du vil tilbakeføre eller bare returnere et delvis antall, kan du redigere Antall-feltet i linjedetaljene. Hvis du åpner fakturalinjedetaljene, kan du se det opprinnelige fakturaantallet. Du kan deretter redigere det gjeldende fakturaantallet slik at det blir mindre enn eller større enn det opprinnelige fakturaantallet.

Når du bekrefter en korrigert faktura, tilbakeføres det opprinnelige faktiske fakturerte salget, og et nytt faktisk fakturert salg opprettes. Hvis antallet ble redusert, vil forskjellen føre til at et nytt, ikke-fakturert faktisk salg også opprettes. Hvis det opprinnelige fakturerte salget for eksempel var på åtte timer, og den korrigerte fakturalinjedetaljen har et redusert antall på seks timer, tilbakeføres den opprinnelige, fakturerte salgslinjen, og det opprettes to nye faktiske verdier:

- Et fakturert faktisk salg på seks timer.
- Et ikke-fakturert faktisk salg for de resterende to timene. Denne transaksjonen kan enten faktureres senere eller merkes som ikke-belastbar, avhengig av forhandlingene med kunden.
