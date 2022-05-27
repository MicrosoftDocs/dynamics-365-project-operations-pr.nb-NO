---
title: Konfigurer kredittkortintegrering
description: Dette emnet forklarer hvordan du arbeider med utgiftsrelaterte kredittkorttransaksjoner.
author: suvaidya
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2c9d993f1999b0be24794bbe828afa8eb74744e9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577065"
---
# <a name="set-up-credit-card-integration"></a>Konfigurer kredittkortintegrering

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Utgiftsrelaterte kredittkorttransaksjoner kan konfigureres slik at de importeres automatisk etter en regelmessig tidsplan. Transaksjonene kan også importeres manuelt etter behov. Kredittkorttransaksjonene importeres via dataenheten for kredittkorttransaksjoner.

## <a name="import-credit-card-transactions"></a>Importere kredittkorttransaksjoner

Følg denne fremgangsmåten for å importere kredittkorttransaksjoner:

1. På siden **Kredittkorttransaksjoner** velger du **Importer transaksjoner**. Hvis du åpner dataadministrasjon for første gang, må systemet oppdatere listen over dataenheter før du kan fortsette.
2. I **Navn**-feltet angir du en unik beskrivelse av importjobben.
3. I feltet **Kildedataformat** velger du formatet til filen som inneholder kredittkorttransaksjonene som skal importeres.
4. Velg **Last opp**, og finn og velg deretter filen som skal importeres.
5. Når du har lastet opp filen, validerer du tilordningen av kredittkorttransaksjonsfilen og kolonnene for dataenheten for kredittkorttransaksjoner ved å velge koblingen **Vis tilordning** på flisen. Hvis det finnes tilordningsfeil, eller hvis du må endre tilordningen, må du gjøre tilordningen fra kategorien **Tilordningsvisualisering** eller kategorien **Tilordningsdetaljer**.
6. Hvis du vil automatisere kredittkorttransaksjonene, velger du **Opprett regelmessig datajobb**. Deretter kan du angi regelmessigheten som definerer hvor ofte kredittkorttransaksjoner skal importeres. Velg **OK** når du er ferdig.
7. Hvis du vil importere den valgte filen nå, velger du **Importer**.
8. Hvis det oppstår feil under importen, kan du vise utføringsloggen eller oppsamlingsdataene for å se feilene du må rette opp, for å sikre at importen blir vellykket.

> [!NOTE]
> Hvis du må importere mer enn ett filformat, må du opprette separate importjobber for hver formattype.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Tilordne kredittkorttransaksjonene på nytt for avsluttede ansatte

Når en ansattoppføring avsluttes, deaktiveres den ansattes Active Directory Domain Services-konto (AD DS). Det kan imidlertid hende at det finnes aktive kredittkorttransaksjoner som fremdeles må belastes og refunderes. På **Kredittkorttransaksjoner**-siden kan du tilordne den ansatte på nytt for en kredittkorttransaksjon der den tilknyttede ansatte er avsluttet.

Velg en eller flere kredittkorttransaksjoner, og velg deretter **Tilordne transaksjoner på nytt**. Du kan deretter velge en annen ansatt du vil tilordne kredittkorttransaksjonene til. Når kredittkorttransaksjonene er tilordnet på nytt, kan de velges for en utgiftsrapport og betales gjennom den vanlige prosessen for refusjon av reiseregning.

## <a name="delete-credit-card-transactions"></a>Slette kredittkorttransaksjoner 

Noen ganger kan det hende at enkelte transaksjoner må slettes etter at kredittkorttransaksjoner er importert. Årsaken kan være at transaksjonene er duplikater eller dataene ikke er nøyaktige. Administratorer kan bruke funksjonen **"Slett kredittkorttransaksjoner"** for å velge og slette kredittkorttransaksjoner som **ikke er knyttet til** en utgiftsrapport. 

1. Gå til **Periodiske oppgaver** > **Slett kredittkorttransaksjoner**.
2. Velg **Filter**, og oppgi informasjon for å identifisere oppføringene som skal inkluderes.
3. Velg **OK** for å slette oppføringene. 

## <a name="storing-credit-card-numbers"></a>Lagre kredittkortnumre

Det finnes tre alternativer for lagring av kredittkortnumre. Kredittkortnumre lagres på siden **Parametere for reiseregning og utlegg**.

- **Hindre kortnummerregistrering** – Kredittkortnumre lagres ikke.
- **Hash-kortnumre (lagre siste 4 sifre)** – De fire siste sifrene i kredittkortnumre lagres i et kryptert format.
- **Lagre kortnumre** – Kredittkortnumre lagres i et ukryptert format. Dette alternativet oppfyller ikke datasikkerhetsstandarden (Data Security Standard (DSS)) til betalingskortbransjen (Payment Card Industry (PCI)). Organisasjonsadministratorer bør derfor la være å lagre kredittkortnumre eller i stedet lagre hash-kortnumre, slik at organisasjonen følger PCI DSS-forskriftene.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
