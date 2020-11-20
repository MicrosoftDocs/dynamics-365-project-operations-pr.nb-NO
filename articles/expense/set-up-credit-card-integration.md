---
title: Konfigurere kredittkortintegrering
description: Dette emnet forklarer hvordan du importerer og vedlikeholder utgiftsrelaterte kredittkorttransaksjoner.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: e0004f9096ea8a03745dbfce35fe0d32d3d707f6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120870"
---
# <a name="set-up-credit-card-integration"></a>Konfigurere kredittkortintegrering

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Utgiftsrelaterte kredittkorttransaksjoner kan konfigureres slik at de importeres automatisk etter en regelmessig tidsplan. Transaksjonene kan også importeres manuelt etter behov. Kredittkorttransaksjonene importeres via dataenheten for kredittkorttransaksjoner.

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
