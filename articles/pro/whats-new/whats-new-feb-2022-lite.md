---
title: Nyheter februar 2022 – Project Operations Lite-distribusjon
description: Denne artikkelen inneholder informasjon om kvalitetsoppdateringene som er tilgjengelige i utgivelsen av Project Operations Lite-distribusjon fra februar 2022.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1203faa2dd53a8fb82cff0857a1725426ebff19a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922832"
---
# <a name="whats-new-february-2022---project-operations-lite-deployment"></a>Nyheter februar 2022 – Project Operations Lite-distribusjon

_Gjelder: Lite-distribusjon – avtale til proformafakturering_

Denne artikkelen gjelder følgende komponenter og versjoner av Microsoft Dynamics 365 Project Operations:

- Project Operations i et Dataverse-miljø, versjon 4.28.0.120

## <a name="features-included-in-this-release"></a>Funksjoner som er inkludert i denne versjonen

I denne versjonen kan du legge til opptil 300 teammedlemmer i ett enkelt prosjekt. Tidligere var grensen for antall teammedlemmer 150. For mer informasjon, se [Prosjektgrenser](../../project-management/create-wbs.md#project-limitations).

## <a name="quality-updates"></a>Kvalitetsoppdateringer

| Funksjonsområdet | Referansenummer | Kvalitetsoppdatering |
| --- | --- | --- |
| Fakturering og prising | 2497369 | Materialkorrigering må følge datoverdien i **Korreksjon**-parameterne. |
| Fakturering og prising | 2498697 | Forbedret sikkerhetskonfigurasjonen for **Tilbakekalling av tidsoppføring**. |
| Fakturering og prising | 2517455 | Handlingen **Oppdater fakturalinjetransaksjoner** må ikke tillates å bli utløst flere samtidige ganger for samme faktura. |
| Fakturering og prising | 2517465 | Handlingen **Deaktiver fakturalinjedetaljer** er blokkert fordi den ikke støttes. |
| Fakturering og prising | 2556660 | Løste datoeffektivitetskontrollene som utføres i prislisten som er knyttet til en oppføring for prosjektparametere. |
|   Administrasjon av salgsmuligheter | 2369202 | Korrigerte forretningslogikken som kontrollerer at prislister som har overlappende virkningsdatoer, kan knyttes til samme prosjektkontrakt. |
|   Administrasjon av salgsmuligheter | 2385965 | Korrigerte funksjonaliteten på **Kunder**-fanen på **Prosjektkontrakt**-siden når du velger **Lagre og lukk**. |
