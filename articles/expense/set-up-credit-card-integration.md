---
title: Konfigurer kredittkortintegrering
description: Dette emnet forklarer hvordan du arbeider med utgiftsrelaterte kredittkorttransaksjoner.
author: suvaidya
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 51c364dff41d856e493581e1b87fd29571f641c70e7233bdebb910efbc64b983
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996223"
---
# <a name="set-up-credit-card-integration"></a>Konfigurer kredittkortintegrering

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Utgiftsrelaterte kredittkorttransaksjoner kan konfigureres slik at de importeres automatisk etter en regelmessig tidsplan. Transaksjonene kan også importeres manuelt etter behov. Kredittkorttransaksjonene importeres via dataenheten for kredittkorttransaksjoner.

## <a name="import-credit-card-transactions"></a>Importere kredittkorttransaksjoner

Følg denne fremgangsmåten for å importere kredittkorttransaksjoner:

1. På siden **Kredittkorttransaksjoner** velger du **Importer transaksjoner**. Hvis du åpner databehandling for første gang, må systemet oppdatere listen over dataenheter før du kan fortsette.
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

Når en ansattoppføring avsluttes, deaktiveres kontoen for den ansattes Active Directory Domain Services (AD DS). Det kan imidlertid hende at det finnes aktive kredittkorttransaksjoner som fremdeles må belastes og refunderes. På **Kredittkorttransaksjoner**-siden kan du tilordne den ansatte på nytt for en kredittkorttransaksjon der den tilknyttede ansatte er avsluttet.

Velg en eller flere kredittkorttransaksjoner, og velg deretter **Tilordne transaksjoner på nytt**. Du kan deretter velge en annen ansatt du vil tilordne kredittkorttransaksjonene til. Når kredittkorttransaksjonene er tilordnet på nytt, kan de velges for en utgiftsrapport og betales gjennom den vanlige prosessen for refusjon av reiseregning.

## <a name="delete-credit-card-transactions"></a>Slette kredittkorttransaksjoner 

Noen ganger kan det hende at enkelte transaksjoner må slettes etter at kredittkorttransaksjoner er importert. Dette kan skyldes at transaksjonene er duplikater eller fordi dataene kanskje ikke er nøyaktige. Administratorer kan bruke funksjonen **"Slett kredittkorttransaksjoner"** for å velge og slette kredittkorttransaksjoner som **ikke er knyttet til** en utgiftsrapport. 

1. Gå til **Periodiske oppgaver** > **Slett kredittkorttransaksjoner**.
2. Velg **Filter**, og oppgi informasjon for å identifisere oppføringene som skal inkluderes.
3. Velg **OK** for å slette oppføringene. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
