---
title: Bruke Transaksjonskategori som en prisdimensjon
description: Dette emnet gir informasjon om hvordan du bruker Transaksjonskategori-feltet som en prisdimensjon.
author: rumant
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ab8093aca9a33bbbaef41c6fc7d33cad930bfadd13b0f7587c3de9032ac0d630
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996133"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Bruke Transaksjonskategori som en prisdimensjon


_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_


Dette emnet forklarer hvordan du bruker **Transaksjonskategori**-feltet som en prisdimensjon. 

## <a name="prerequisites"></a>Forutsetninger
Før du fullfører prosedyrene i dette emnet, må du ha en ny prisdimensjonsløsning for organisasjonen. Hvis du ikke allerede har opprettet en, kan du se [Opprette egendefinerte felt og enheter som prisdimensjoner](create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-transaction-category-field-to-forms-and-views"></a>Legge til Transaksjonskategori-feltet i skjemaer og visninger
Hvis du vil gjøre **Transaksjonskategori**-feltet synlig i prisdimensjonsløsningen, må du legge til feltet i alle skjemaer og visninger som en enhet.

Tabellen nedenfor viser alle de medfølgende skjemaene og visningene etter enhet. Du må også legge til det nye feltet i andre ekstra skjemaer eller visninger i de egendefinerte enhetene.

|  Entity        | Skjemaer     |Visninger        |
| ------------------------------|---------------------------------|----------------------------------|
|  Rollepris| Informasjon |- Aktive ressurskategoripriser<br> - Tilknyttede ressurskategoripriser |
|  Rolleprispåslag| Informasjon|- Aktive rolleprispåslag<br>- Tilknyttede rolleprispåslag |
|  Tilbudslinjedetalj|- Prosjektinformasjon<br>- Hurtigoppretting av prosjekt| - Aktiv tilbudslinjedetalj<br>- Kombinerte tilbudslinjedetaljer<br>- Tilknyttet tilbudslinjedetalj |
|  Detalj for prosjektkontraktlinjer|- Prosjektinformasjon<br>- Hurtigoppretting av prosjekt|- Kombinerte kontraktlinjedetaljer<br>- Aktive kontraktlinjedetaljer<br>- Tilknyttede kontraktlinjedetaljer |
|  Prosjektoppgave|- Informasjon<br>- Nytt skjema| &nbsp; |
|  Prosjektteammedlem|- Informasjon<br>- Nytt skjema|- Aktive prosjektteammedlemmer<br>- Prosjektteammedlemmer<br>- Tilknyttede prosjektteammedlemmer |
|  Tidsoppføring|- Informasjon<br>- Opprett tidsoppføring|- Mine tidsoppføringer etter dato<br>- Mine tidsoppføringer for denne uken<br>- Tidsoppføringer til godkjenning|
|  Journallinje|- Informasjon<br>- Hurtigoppretting|- Aktive journallinjer<br>- Tilknyttet journallinje|
|  Fakturalinjedetalj|- Informasjon<br>- Hurtigoppretting|- Aktive fakturalinjedetaljer<br>- Belastbare fakturatransaksjoner<br>- Gratis fakturatransaksjoner<br>- Tilknyttet fakturalinjedetalj <br>- Ikke-belastbare fakturatransaksjoner|
|  Faktisk|- Informasjon<br>- Aktive faktiske data| Faktisk tilknyttet |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a>Konfigurere Transaksjonskategori-feltet som en prisdimensjon

1. Gå til **Innstillinger** > **Parametere**. 
2. På **Parametere**-siden i **Beløpsbaserte prisdimensjoner**-kategorien, bekrefter du at rutenettet viser oppføringene i **Prisdimensjoner**-enheten.
3. Legg til **Transaksjonskategori** i denne listen, og angi feltene **Gjelder kostnad** og **Gjelder salg** til **Ja**.
4. I **Dimensjonstype**-feltet velger du **Beløpsbasert**, og deretter velger du prioritet for **Transaksjonskategori** relatert til kostnad og salg.


[!INCLUDE[footer-include](../includes/footer-banner.md)]