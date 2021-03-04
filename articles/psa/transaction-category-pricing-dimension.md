---
title: Bruke transaksjonskategori som en prisdimensjon
description: Dette emnet gir informasjon om hvordan du bruker en transaksjonskategori som en prisingsdimensjon.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 00214aa2b514da71b331073cd0eeb5320c03e7d7
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150770"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Bruke transaksjonskategori som en prisdimensjon

[!include [banner](../includes/psa-now-project-operations.md)]

Dette emnet gir informasjon om hvordan du bruker en transaksjonskategori som en prisingsdimensjon. Hvis du ikke allerede har opprettet en løsning for prisdimensjon før du begynner, må du opprette en ny. Hvis du allerede har en løsning for prisingsdimensjon, kan du gjøre endringene i den løsningen. Hvis du ikke har opprettet en ny løsning for prisdimensjon for organisasjonen, må du fullføre prosedyrene i emnet [Opprette egendefinerte felt og enheter](create-custom-fields-entities.md).

## <a name="add-transaction-category-to-forms-and-views"></a>Legge til transaksjonskategori i skjemaer og visninger
Hvis du vil gjøre transaksjonskategorien synlig i brukergrensesnittet i løsningen for prisingsdimensjonen, må du gå gjennom alle skjemaer og visninger for de viktigste enhetene og legge til disse feltene i skjemaene og visningene for disse enhetene.
Tabellen nedenfor er en omfattende liste over de medfølgende skjemaene og visningen, oppført etter enhet, som må oppdateres med de nye feltene. Hvis det finnes andre visninger eller skjemaer i tilpassingen på disse enhetene, legger du til de nye feltene også.

|  Enhet        | Skjemaer     |Visninger        |
| ------------------------------|---------------------------------|----------------------------------|
|  Rollepris|• Informasjon |• Aktive ressurskategoripriser<br> • Tilknyttet visning for ressurskategoripriser|
|  Rolleprispåslag|• Informasjon|• Aktive rolleprispåslag<br>• Tilknyttet visning for rolleprispåslag|
|  Tilbudslinjedetalj|• Prosjektinformasjon<br>• Hurtigoppretting av prosjekter|• Aktiv tilbudslinjedetalj<br>• Kombinerte tilbudslinjedetaljer<br>• Tilknyttet visning for tilbudslinjedetaljer|
|  Detalj for prosjektkontraktlinjer|• Prosjektinformasjon<br>• Hurtigoppretting av prosjekter|• Kombinerte kontraktlinjedetaljer<br>• Aktive kontraktlinjedetaljer<br>• Tilknyttet visning for kontraktlinjedetaljer|
|  Prosjektoppgave|• Informasjon<br>• Nytt skjema||
|  Prosjektteammedlem|• Informasjon<br>• Nytt skjema|• Aktive prosjektteammedlemmer<br>• Prosjektteammedlemmer<br>• Tilknyttet visning for prosjektteammedlemmer|
|  Tidsoppføring|• Informasjon<br>• Opprett tidsoppføring|• Mine tidsoppføringer etter dato<br>• Mine tidsoppføringer for denne uken<br>• Tidsoppføringer for godkjenning|
|  Journallinje|• Informasjon<br>• Hurtigoppretting|• Aktive journallinjer<br>• Tilknyttet visning for journallinjer|
|  Fakturalinjedetalj|• Informasjon<br>• Hurtigoppretting|• Aktive fakturalinjedetaljer<br>• Belastbare fakturatransaksjoner<br>• Gratis fakturatransaksjoner<br>• Tilknyttet visning for fakturalinjedetaljer<br>• Ikke-belastbare fakturatransaksjoner|
|  Faktisk|• Informasjon<br>• Aktive faktiske data|• Tilknyttet visning for faktiske data|

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a>Konfigurere transaksjonskategori som en prisdimensjon

1. I webgrensesnittet går du til **Project Service** > **Innstillinger** > **Parametere**. 
2. På **Parametere**-siden i kategorien **Beløpsbaserte prisdimensjoner** kan du legge merke til at rutenettet i kategorien viser oppføringene i **Prisdimensjoner**-enheten.
3. Legg til **Transaksjonskategori** i denne listen, og angi feltene **Gjelder kostnad** og **Gjelder salg** til **Ja**.
4. I **Dimensjonstype**-feltet velger **Beløpsbasert**, og deretter velger du prioritet for **Transaksjonskategori** relatert til kostnad og salg.
