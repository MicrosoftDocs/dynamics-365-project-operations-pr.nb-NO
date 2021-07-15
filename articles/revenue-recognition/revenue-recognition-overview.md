---
title: Oversikt over inntektsføring
description: Dette emnet gir informasjon om inntektsføring i Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: ab9b36b71223b1bcfe48de5f9b68b6fb6a98f388
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368038"
---
# <a name="revenue-recognition-overview"></a>Oversikt over inntektsføring

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

I Dynamics 365 Project Operations kan det være forskjellige prinsipper for inntektsføring, basert på den valgte faktureringsmetoden for et prosjekt eller en del av prosjektet. Dette emnet gir informasjon om inntektsføring i Project Operations.

## <a name="transactions-accounted-using-time-and-material-billing-method"></a>Transaksjoner beregnet ved hjelp av faktureringsmetode for tid og materialer

- Kostnads- og inntektsføring er tilkoblet. Transaksjonskostnader og ufakturerte salg posteres ved hjelp av [Integreringsjournal for Project Operations](../project-accounting/project-operations-integration-journal.md).
- Prosjektkostnads- og inntektsprofil avgjør om ufakturerte salgstransaksjoner blir postert til økonomimodulen. Hvis **Avsett inntekt** er valgt, bruker systemet **VIA-salgsverdi** og **Påløpte inntekter – salgsverdi**-kontoene under postering. Nedenfor er et eksempel på denne metoden.  

  | Transaksjonstype | Debet/kredit | Mengde |
  | --- | --- | --- |
  | VIA – Salgsverdi | Debet | 100 |
  | Påløpt inntekt – Salgsverdi | Kredit | 100 |

- Inntekt gjenkjennes gjennom fakturering. Systemet bruker **Fakturert inntekt**-kontoen under postering. Nedenfor er et eksempel på denne metoden.  

  | Transaksjonstype | Debet/kredit | Mengde |
  | --- | --- | --- |
  | Kundesaldo | Debet | 120 |
  | Skyldig merverdiavgift | Kredit | 20 |
  | Fakturert inntekt | Kredit | 100 |

- Hvis inntekten var påløpt da det ufakturerte salget ble postert, tilbakefører systemet den påløpte inntekten ved fakturering.

  | Transaksjonstype | Debet/kredit | Mengde |
  | --- | --- | --- |
  | VIA – Salgsverdi | Kredit | 100 |
  | Påløpt inntekt – Salgsverdi | Debet | 100 |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a>Transaksjoner beregnet ved bruk av faktureringsmetode for fastpris

- Kostnads- og inntektsføring er separate. Transaksjonskostnader posteres ved hjelp av [Integreringsjournalen for Project Operations](../project-accounting/project-operations-integration-journal.md). Ufakturerte salgstransaksjoner opprettes ikke.
- Inntekt kan gjenkjennes under fakturering hvis prosjektkostnads- og inntektsprofilen har **Prinsipp brukt til beregninger for prosjektfullføring** satt til **Ingen VIA**. Bruk bare denne metoden for kortsiktige, enkle prosjekter.
- Inntekt kan gjenkjennes ved hjelp av inntektsestimat for fastpris, med enten **Fullført kontrakt** eller **Inntektsføring for fullføringsprosent**-metoden.

## <a name="additional-resources"></a>Ytterligere ressurser
[Konfigurer regnskap for fakturerbare prosjekter](../project-accounting/configure-accounting-billable-projects.md)

[Inntektsestimat for fastprisprosjekter](rev-rec-percentage-completion-method.md)

[Administrer inntektsestimater](rev-rec-completed-contract-method.md)

[Metoder for ferdigstillingskostnad](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]