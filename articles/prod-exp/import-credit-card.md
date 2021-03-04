---
title: Importere og vedlikeholde kredittkorttransaksjoner
description: Dette emnet forklarer hvordan du importerer og vedlikeholder utgiftsrelaterte kredittkorttransaksjoner. Disse transaksjonene kan konfigureres slik at de importeres automatisk etter en regelmessig tidsplan, eller de kan importeres manuelt etter behov.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 7bf75c13bb190c7b992aa516f1593d886dfa604d
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960439"
---
# <a name="import-and-maintain-credit-card-transactions"></a>Importere og vedlikeholde kredittkorttransaksjoner

Utgiftsrelaterte kredittkorttransaksjoner kan konfigureres slik at de importeres automatisk etter en regelmessig tidsplan. Transaksjonene kan også importeres manuelt etter behov. Kredittkorttransaksjonene importeres via dataenheten for kredittkorttransaksjoner.

Hvis du vil ha mer informasjon om dataenheter, kan du se [Dataenheter](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).

## <a name="import-credit-card-transactions"></a>Importere kredittkorttransaksjoner

1. På siden **Kredittkorttransaksjoner** velger du **Importer transaksjoner**. Hvis du åpner databehandling for første gang, må systemet oppdatere listen over dataenheter før du kan fortsette.
2. I **Navn**-feltet angir du en unik beskrivelse av importjobben.
3. I feltet **Kildedataformat** velger du formatet til filen som inneholder kredittkorttransaksjonene som skal importeres.
4. Velg **Last opp**, og finn og velg deretter filen som skal importeres.
5. Når du har lastet opp filen, validerer du tilordningen av kredittkorttransaksjonsfilen og kolonnene for dataenheten for kredittkorttransaksjoner ved å velge koblingen **Vis tilordning** på flisen. Hvis det finnes tilordningsfeil, eller hvis du må endre tilordningen, må du gjøre tilordningen fra kategorien **Tilordningsvisualisering** eller kategorien **Tilordningsdetaljer**.
6. Hvis du vil automatisere kredittkorttransaksjonene, velger du **Opprett regelmessig datajobb**. Deretter kan du angi regelmessigheten som definerer hvor ofte kredittkorttransaksjoner skal importeres. Velg **OK** når du er ferdig.
7. Hvis du vil importere den valgte filen nå, velger du **Importer**.
8. Hvis det oppstår feil under importen, kan du vise utførelsesloggen eller oppsamlingsdataene for å se feilene du må rette for å sikre en vellykket import.

> [!NOTE]
> Hvis du må importere mer enn ett filformat, må du opprette separate importjobber for hver formattype.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Tilordne kredittkorttransaksjonene på nytt for avsluttede ansatte

Når en ansattoppføring avsluttes, deaktiveres kontoen for den ansattes Active Directory Domain Services (AD DS). Det kan imidlertid hende at det finnes aktive kredittkorttransaksjoner som fremdeles må belastes og refunderes. På siden **Kredittkorttransaksjoner** kan du tilordne den ansatte på nytt for en hvilken som helst kredittkorttransaksjon der den tilknyttede ansatte er avsluttet.

Velg en eller flere kredittkorttransaksjoner, og velg deretter **Tilordne transaksjoner på nytt**. Du kan deretter velge en annen ansatt du vil tilordne kredittkorttransaksjonene til. Når kredittkorttransaksjonene er tilordnet på nytt, kan de velges for en utgiftsrapport og betales gjennom den vanlige prosessen for refusjon av reiseregning.
