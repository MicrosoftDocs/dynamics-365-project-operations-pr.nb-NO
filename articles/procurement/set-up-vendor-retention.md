---
title: Definer leverandøroppbevaring
description: Dette emnet forklarer hvordan du konfigurerer leverandørbevaring.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e0cd7669c7d6b916261e2c85cce0f24ff241a075
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583716"
---
# <a name="set-up-vendor-retention"></a>Definer leverandøroppbevaring

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Dette emnet gir informasjon om hvordan du konfigurerer leverandørbevaring.

## <a name="set-up-a-vendor-retention-account-in-general-ledger"></a>Konfigurer en konto for leverandøroppbevaring i Økonomi modul

1. I Dynamics 365 Finance går du til **Økonomimodul** > **Bokføringsoppsett** > **Kontoer for automatiske transaksjoner**.
2. Legg til en ny linje.
3. Velg **Leverandørtilbakeholdelse** feltet **Bokføringstype**.
4. Velg hovedkontoen for bokføring av leverandørtilbakeholdelse.

## <a name="create-vendor-retention-terms"></a>Opprett betingelser for tilbakeholdelse av leverandør

Bruk siden **Tilbakeholdelsesbetingelser for leverandør** til å konfigurere og vedlikeholde tilbakeholdelsesbetingelser for leverandørbetalinger. Angi prosenten av en leverandørbetaling som skal holdes tilbake, og prosenten av tidligere tilbakeholdte beløp som skal frigis. Beløpene tilbakeholdes automatisk på leverandørfakturaer til kontrakten når den angitte fullføringsstatusen. Når det er angitt tilbakeholdelsesbetingelser for en leverandør, kan du bruke dem på alle prosjekter som leverandøren arbeider på.

1. I Finance går du til **Prosjektstyring og regnskap** > **Oppsett** > **Tilbakeholdelse** > **Betingelser for tilbakeholdelse av leverandørbetaling**.
2. Velg **Ny** for å legge til en ny tilbakeholdingsbetingelse for en leverandør. Verdien for feltet **Regel-ID** for den nye betingelsen angis automatisk. 
3. I feltet **Beskrivelse** skriver du inn et beskrivende navn for den nye betingelsen.
4. Velg **Legg til linje** i fanen **Betingelser** for å angi en betingelse for leverandørtilbakeholdelse.
5. I feltet **Prosent av leverte enheter** angir du en fullføringsprosent for regelen. Beløp tilbakeholdes automatisk på leverandørfakturaer til fullføringsstadiet for prosjektet er lik prosentdelen du angir. Hvis du for eksempel angir 50,00, beholdes beløpene til prosjektet er 50 prosent fullført.
6. I feltet **Prosent som skal tilbakeholdes** angir du prosenten av et leverandørfakturabeløp som skal tilbakeholdes. Hvis du for eksempel angir 10,00 i dette feltet, tilbakeholdes 10 prosent av beløpet på en leverandørfakturaene til prosjektet når fullføringsprosenten du valgte i feltet **Prosent av leverte enheter**.
7. I feltet **Prosent som skal frigis** velger du prosenten av eventuelle tidligere tilbakeholdte beløp som skal frigis på det valgte nivået av prosjektfullføring.

> [!NOTE]
> Hvis du har flere milepæler for ulike nivåer av prosjektfullføring, angir du en egen linje med betingelse for tilbakeholdelse av leverandørbetaling for hver enkelt tilbakeholdelsesregel. Hver linje kan ha en egen prosentdel for tilbakeholdelse, og en egen prosentdel som skal frigis, for hvert angitte nivå av prosjektfullføring.

## <a name="set-up-a-vendor-agreement-for-the-project"></a>Definer en leverandøravtale for prosjektet

Definer tilbakeholdelsesbetingelsene for leverandør som gjelder prosjektet. Tilbakeholdelsesbetingelsene for leverandører vises også i bestillinger som du oppretter for leverandøren.

1. I Finance går du til **Prosjektstyring og regnskap** > **Prosjekter** > **Alle prosjekter**. 
2. Velg et prosjekt, og velg **Prosjektgruppe** > **Leverandøravtaler** i handlingsruten.
3. Legg til en ny linje på **Leverandøravtaler**-siden.
4. Velg ett av følgende alternativer i feltet **Kontokode**:
   - **Tabell**: Tilbakeholdelsesbetingelsene for leverandører gjelder for én enkelt leverandør.
   - **Gruppe**: Tilbakeholdelsesbetingelsene for leverandører gjelder for alle leverandører i en leverandørgruppe.
   - **Alle**: Tilbakeholdelsesbetingelsene for leverandører gjelder for alle leverandører.
5. I feltet **Leverandør/Leverandørgruppe** velger du leverandøren eller leverandørgruppen som tilbakeholdelsesbetingelsene for leverandører gjelder for. Hvis du valgte **Alle** i forrige trinn, er dette feltet ikke tilgjengelig.
6. I feltet **Tilbakeholdelsesbetingelser for leverandør** velger du regel-ID-en for tilbakeholdelsesbetingelsene som skal brukes for denne leverandøren.

