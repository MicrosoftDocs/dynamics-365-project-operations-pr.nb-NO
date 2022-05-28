---
title: Verifisering av leverandørfakturaer med godkjente faktiske verdier
description: Dette emnet forklarer hvordan Microsoft Dynamics 365 Project Operations lar prosjektledere verifisere leverandørfakturaer med de faktiske beløpene som ble godkjent etter hvert som underleverandører utførte arbeid og registrerte tid, samt utgiftene og materiellet som ble brukt av prosjektgruppemedlemmer.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3350a51bde2872036b79a789fae23ea6790fb21a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585482"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Verifisering av leverandørfakturaer med godkjente faktiske verdier

[!include [banner](../../includes/dataverse-preview.md)]

_ **Gjelder:** Lite-distribusjon – avtale til proformafakturering

Microsoft Dynamics 365 Project Operations lar prosjektledere kontrollere fakturalinjer for leverandører på følgende måter:

- Bruk **Verifiseringsstatus**-feltet på leverandørfakturalinjene.
- Hvis leverandørfakturalinjene refererer til en underkontraktlinje, kobler du faktiske kostnader fra underleverandøraktiviteten til disse leverandørfakturalinjene. Koblingen opprettes ved å samsvare faktiske kostnader med leverandørfakturalinjene.

    > [!NOTE]
    > Selv om verifiseringsstatus kan spores for fakturalinjer for leverandør som ikke refererer til en underkontrakt, kan ikke faktiske kostnader kobles til disse leverandørfakturalinjene.

## <a name="verification-status"></a>Verifiseringsstatus

Feltet **Verifiseringsstatus** på en leverandørfakturalinje angir verifiseringsstatusen. Følgende statuser støttes:

1. Ikke startet
2. Pågår
3. Fullført

Leverandørfakturalinjer som har verifiseringsstatusen **Ikke startet**, kan redigeres.

Leverandørfakturalinjer som har verifiseringsstatusen **Pågår**, kan ikke lenger redigeres. For en leverandørfakturalinje som refererer til en underleverandør, angis verifiseringsstatusen automatisk til **Pågår** så snart den faktiske kostnaden samsvares med leverandørfakturalinjen.

Leverandørfakturalinjer som har verifiseringsstatusen **Fullført**, kan ikke lenger redigeres. Når alle linjene på en leverandørfaktura har denne verifiseringsstatusen, kan leverandørfakturaen bekreftes.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Samsvar faktiske kostnader til leverandørfakturalinjer

Samsvar av faktiske kostnader bidrar til verifiseringsprosessen på en leverandørfakturalinje. Følg denne fremgangsmåten for å samsvare faktiske kostnader med en leverandørfakturalinje.

1. Åpne leverandørfakturalinjen, og velg fanen **Ikke samsvarte faktiske kostnader**. Et rutenett viser en liste over faktiske kostnader som refererer til samme underkontraktslinje som leverandørfakturalinjen.
2. Velg én eller flere av de faktiske kostnadene, og velg deretter **Samsvar** på verktøylinjen over rutenettet. Systemet validerer at de valgte faktiske kostnadene kan samsvares. Når valideringen er bestått, kobles de faktiske kostnadene til leverandørfakturalinjen.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Valideringsvilkår som brukes til å koble faktiske kostnader til leverandørfakturalinjer

I løpet av samsvarsprosessen kan du bare opprette en kobling mellom en faktisk kostnad og en leverandørfakturalinje hvis begge følgende betingelser er oppfylt:

- **Justeringsstatus**-feltet for hver valgte faktiske kostnad må være tomt. Med andre ord må de faktiske kostnadene ikke ha blitt erstattet av andre faktiske kostnader under en tilbakekallings-, annullerings- eller korrigeringsjournalprosess.
- Verdiene i de følgende feltene samsvares mellom leverandørfakturalinjen og den valgte faktiske kostnaden. Hvis et felt ikke er angitt på leverandørfakturalinjen, vurderes det ikke som samsvarende.

    - Prosjektkontrakt
    - Prosjektkontraktlinjer
    - Transaksjonsklasse
    - Project
    - Oppgave
    - Ressurskategori
    - Transaksjonskategori
    - Produkt
    - Underkontraktlinje
    - Ressurs som kan reserveres

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Opphev samsvar for faktiske verdier fra en leverandørfakturalinje

Oppheving av samsvar med faktiske kostnader kan også hjelpe deg med verifiseringsprosessen på en leverandørfaktura ved å la tidligere opprettede koblinger fjernes. Det kan bare oppheves samsvar for faktiske kostnader fra leverandørfakturalinjer som har verifiseringsstatusen **Pågår**. Følg denne fremgangsmåten for å oppheve samsvar for faktiske kostnader fra en leverandørfakturalinje.

1. Åpne leverandørfakturalinjen, og velg fanen **Samsvarte faktiske kostnader**. Et rutenett viser en liste over faktiske kostnader som refererer til leverandørfakturalinjen.
2. Velg én eller flere av de faktiske kostnadene, og velg deretter **Opphev samsvar** på verktøylinjen over rutenettet.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
