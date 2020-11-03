---
title: Se gjennom restansen for fakturering for prosjekter og prosjektkontrakter
description: Dette emnet gir informasjon om hvordan du gjennomgår tids-, utgifts- og produktrestanse, og hvordan du merker dem som klare til fakturering.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: eb6d942d61bf8b5d20afb75c88716132a596bcbd
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081829"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>Se gjennom restansen for fakturering for prosjekter og prosjektkontrakter

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Når en transaksjon er klar til få en faktura opprettet og behandlet, skal transaksjonen merkes **Klar for fakturering**. Dette emnet beskriver transaksjonstypene som kan opprettes.

## <a name="review-the-time-and-material-billing-backlog"></a>Se gjennom faktureringsrestanse for tid og materiale

Når en tids- eller utgiftsoppføring sendes og godkjennes for et prosjekt, oppretter PSA en faktisk prosjektverdi. Hvis kombinasjonen av prosjektet og transaksjonsklassen tilordnes til en kontraktlinje for et tids-og-materiell-prosjekt, opprettes det to faktiske verdier når oppføringen godkjennes:

- Faktisk kostnad 
- Ufakturert faktisk salg

Ufakturerte faktiske verdier for salg representerer faktureringsrestansen, og faktureringsstatusen må være satt **Klar for fakturering**. Når en prosjektfaktura opprettes, blir ufakturerte faktiske verdier for salg merket som **Klar for fakturering** , kopiert over som fakturalinjedetaljer.

Hvis du vil se gjennom faktureringsrestansen for tid og materialer, går du til **Salg** \> **Fakturering** \> **Faktureringsrestanse for Tid og materiale**. Velg alle ufakturerte faktiske verdier for salg som er klare for fakturering, og velg deretter **Klar for fakturering**. Faktureringsstatusen for disse faktiske verdiene endres til **Klar for fakturering**.

![Faktureringsrestanse for Tid og materiale](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>Se gjennom faktureringsrestanse for produkt

Når en prosjektkontrakt i PSA har produktbaserte kontraktlinjer, vurderes disse linjene for fakturering hver gang det opprettes en faktura for prosjektkontrakten. Alle produkter som har kontraktlinjer som er merket **Klar for fakturering** , kopieres til prosjektfakturaen som prosjektfakturalinjer.

Hvis du vil se gjennom faktureringsresistansen for produkter, går du til **Salg** \> **Fakturering** \> **Faktureringsrestanse for produkt**. Merk av for alle de produktbaserte kontraktlinjene som er klare til fakturering, og velg deretter **Klar for fakturering**. Faktureringsstatusen for disse linjene endres til **Klar for fakturering**.

![Faktureringsrestanse for produkt](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>Se gjennom faktureringsmilepæler på fastepriskontrakter

Hver prosjektkontraktlinje som har en fastprisfaktureringsmetode, må definere kontraktmilepæler. Disse kontraktmilepælene kan bare faktureres hvis de er merket **Klar for fakturering**. 

Hvis du vil se gjennom faktureringsmilepæler, går du til **Salg** \> **Fakturering** \> **Milepæler for fast pris**. Velg milepælene som er klare for fakturering, og velg deretter **Klar for fakturering**. Faktureringsstatusen for disse milepælene endres til **Klar for fakturering**.

![Milepæler for fast pris](media/FPBacklog.png)