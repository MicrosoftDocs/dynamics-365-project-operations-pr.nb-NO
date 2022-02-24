---
title: Opprette og bruke tilbakeholdelsesbetingelser for leverandørbetaling
description: Dette emnet gir informasjon om hvordan du setter opp og vedlikeholder tilbakeholdelsesbetingelser for leverandørbetalinger.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: e6f6424b983f76a96825d76e1b4b81b54dc84b84
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270960"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Opprette og bruke tilbakeholdelsesbetingelser for leverandørbetaling

[!include [banner](../includes/banner.md)] 

Det er nyttig å konfigurere tilbakeholdelsesbetingelser for leverandørbetalinger for et prosjekt når organisasjonen vil beholde en del av betalingene til en leverandør. Dette kan for eksempel være når du vil holde tilbake betalingen til en leverandør til de leverte produktene oppfyller forventningene dine. Du kan angi tilbakeholdelsesbetingelser for leverandørbetalinger når du forhandler om en leverandørkontrakt.

## <a name="create-vendor-payment-retention-terms"></a>Opprette tilbakeholdelsesbetingelser for leverandørbetaling

Du kan angi prosentandelen av leverandørbetalingen for tilbakeholding og prosentandelen av de tidligere tilbakeholdte beløpene som skal frigis. Beløpene tilbakeholdes automatisk på leverandørfakturaer til kontrakten når den angitte fullføringsstatusen. Når du har angitt tilbakeholdelsesvilkårene, kan du bruke dem på alle prosjekter for den aktuelle leverandøren.

Bruk fremgangsmåten nedenfor for å konfigurere og vedlikeholde tilbakeholdingsbetingelser for leverandørbetalinger. 

1. Gå til **Prosjektstyring og regnskap** > **Tilbakeholding** > **Tilbakeholdelsesbetingelser for leverandørbetaling**.
2. Velg **Ny** for å legge til en ny tilbakeholdingsbetingelse for en leverandør. Verdien for **Regel-ID** for den nye betingelsen angis automatisk. 
3. Skriv inn en kort beskrivelse i **Beskrivelse**-feltet, og gå til hurtigfanen **Betingelser** og velg **Legg til linje** for å angi betingelsesverdier for følgende:

   - **Prosentandel av leverte enheter**: Angi en fullføringsprosent for betingelsen. Beløpene tilbakeholdes automatisk på leverandørfakturaer til prosjektets fullføringsfase er lik den angitte prosentandelen. Hvis du for eksempel angir 50,00, beholdes beløpene til prosjektet er 50 prosent fullført.
   - **Prosentandel som skal tilbakeholdes**: Angi en prosentandel av leverandørfakturabeløpet som skal tilbakeholdes. Hvis du for eksempel angir 10,00, tilbakeholdes 10 prosent av beløpet på en leverandørfaktura til prosjektet når fullføringsprosenten som angitt i feltet **Prosentandel av leverte enheter**.
   - **Prosentandel som skal frigis**: Velg **Legg til linje** for å angi en prosentandel av eventuelle tidligere tilbakeholdte beløp som skal frigis for det valgte fullføringsnivået for prosjektet.

> [!NOTE]
> Hvis du har mer enn én milepæl for ulike nivåer av prosjektfullføring, angir du en egen betingelseslinje for tilbakeholdelse for leverandører for hver tilbakeholdelsesregel. Hver linje kan angi en annen tilbakeholdingsprosent og en annen frigivelsesprosent for hvert angitte prosjektfullføringsnivå.

Når du har opprettet tilbakeholdelsesvilkår for en leverandør, kan du bruke vilkårene på et prosjekt.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Bruke tilbakeholdelsesbetingelser for en leverandør på et prosjekt

1. Gå til **Prosjektstyring og regnskap** > **Prosjekter** > **Alle prosjekter**, og åpne et prosjekt fra prosjektlistesiden.
2. På hurtigfanen **Leverandøravtaler** velger du **Legg til linje**.
3. Velg ett av følgende alternativer i feltet **Kontokode**: 

   - **Tabell**: Tilbakeholdelsesbetingelsene for leverandører gjelder for én enkelt leverandør.
   - **Gruppe**: Tilbakeholdelsesbetingelsene for leverandører gjelder for alle leverandører i en leverandørgruppe.
   - **Alle**: Tilbakeholdelsesbetingelsene for leverandører gjelder for alle leverandører.

4. I feltet the **Leverandør/Leverandørgruppe** velger du leverandøren eller leverandørgruppen som tilbakeholdelsesbetingelsene for leverandører gjelder for. Hvis du valgte **Alle** i forrige trinn, er dette feltet ikke tilgjengelig.
5. I feltet **Tilbakeholdelsesbetingelser for leverandører** velger du tilbakeholdelsesbetingelsene som du opprettet i den forrige prosedyren.
6. Hvis prosjektet også har PWP-betingelser (betal når betalt) satt opp for leverandøren, angir du terskelprosenten for prosjektet i feltet **PWP-terskelprosent**.

Tilbakeholdelsesbetingelsene for leverandører vises også i bestillinger som du oppretter for leverandøren.


[!INCLUDE[footer-include](../includes/footer-banner.md)]