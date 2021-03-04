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
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="d5f5b-104">Importere og vedlikeholde kredittkorttransaksjoner</span><span class="sxs-lookup"><span data-stu-id="d5f5b-104">Import and maintain credit card transactions</span></span>

<span data-ttu-id="d5f5b-105">Utgiftsrelaterte kredittkorttransaksjoner kan konfigureres slik at de importeres automatisk etter en regelmessig tidsplan.</span><span class="sxs-lookup"><span data-stu-id="d5f5b-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="d5f5b-106">Transaksjonene kan også importeres manuelt etter behov.</span><span class="sxs-lookup"><span data-stu-id="d5f5b-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="d5f5b-107">Kredittkorttransaksjonene importeres via dataenheten for kredittkorttransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="d5f5b-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="d5f5b-108">Hvis du vil ha mer informasjon om dataenheter, kan du se [Dataenheter](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span><span class="sxs-lookup"><span data-stu-id="d5f5b-108">For more information about data entities, see [Data entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="d5f5b-109">Importere kredittkorttransaksjoner</span><span class="sxs-lookup"><span data-stu-id="d5f5b-109">Import credit card transactions</span></span>

1. <span data-ttu-id="d5f5b-110">På siden **Kredittkorttransaksjoner** velger du **Importer transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="d5f5b-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="d5f5b-111">Hvis du åpner databehandling for første gang, må systemet oppdatere listen over dataenheter før du kan fortsette.</span><span class="sxs-lookup"><span data-stu-id="d5f5b-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="d5f5b-112">I **Navn**-feltet angir du en unik beskrivelse av importjobben.</span><span class="sxs-lookup"><span data-stu-id="d5f5b-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="d5f5b-113">I feltet **Kildedataformat** velger du formatet til filen som inneholder kredittkorttransaksjonene som skal importeres.</span><span class="sxs-lookup"><span data-stu-id="d5f5b-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="d5f5b-114">Velg **Last opp**, og finn og velg deretter filen som skal importeres.</span><span class="sxs-lookup"><span data-stu-id="d5f5b-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="d5f5b-115">Når du har lastet opp filen, validerer du tilordningen av kredittkorttransaksjonsfilen og kolonnene for dataenheten for kredittkorttransaksjoner ved å velge koblingen **Vis tilordning** på flisen.</span><span class="sxs-lookup"><span data-stu-id="d5f5b-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="d5f5b-116">Hvis det finnes tilordningsfeil, eller hvis du må endre tilordningen, må du gjøre tilordningen fra kategorien **Tilordningsvisualisering** eller kategorien **Tilordningsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="d5f5b-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="d5f5b-117">Hvis du vil automatisere kredittkorttransaksjonene, velger du **Opprett regelmessig datajobb**.</span><span class="sxs-lookup"><span data-stu-id="d5f5b-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="d5f5b-118">Deretter kan du angi regelmessigheten som definerer hvor ofte kredittkorttransaksjoner skal importeres.</span><span class="sxs-lookup"><span data-stu-id="d5f5b-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="d5f5b-119">Velg **OK** når du er ferdig.</span><span class="sxs-lookup"><span data-stu-id="d5f5b-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="d5f5b-120">Hvis du vil importere den valgte filen nå, velger du **Importer**.</span><span class="sxs-lookup"><span data-stu-id="d5f5b-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="d5f5b-121">Hvis det oppstår feil under importen, kan du vise utførelsesloggen eller oppsamlingsdataene for å se feilene du må rette for å sikre en vellykket import.</span><span class="sxs-lookup"><span data-stu-id="d5f5b-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="d5f5b-122">Hvis du må importere mer enn ett filformat, må du opprette separate importjobber for hver formattype.</span><span class="sxs-lookup"><span data-stu-id="d5f5b-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="d5f5b-123">Tilordne kredittkorttransaksjonene på nytt for avsluttede ansatte</span><span class="sxs-lookup"><span data-stu-id="d5f5b-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="d5f5b-124">Når en ansattoppføring avsluttes, deaktiveres kontoen for den ansattes Active Directory Domain Services (AD DS).</span><span class="sxs-lookup"><span data-stu-id="d5f5b-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="d5f5b-125">Det kan imidlertid hende at det finnes aktive kredittkorttransaksjoner som fremdeles må belastes og refunderes.</span><span class="sxs-lookup"><span data-stu-id="d5f5b-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="d5f5b-126">På siden **Kredittkorttransaksjoner** kan du tilordne den ansatte på nytt for en hvilken som helst kredittkorttransaksjon der den tilknyttede ansatte er avsluttet.</span><span class="sxs-lookup"><span data-stu-id="d5f5b-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="d5f5b-127">Velg en eller flere kredittkorttransaksjoner, og velg deretter **Tilordne transaksjoner på nytt**.</span><span class="sxs-lookup"><span data-stu-id="d5f5b-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="d5f5b-128">Du kan deretter velge en annen ansatt du vil tilordne kredittkorttransaksjonene til.</span><span class="sxs-lookup"><span data-stu-id="d5f5b-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="d5f5b-129">Når kredittkorttransaksjonene er tilordnet på nytt, kan de velges for en utgiftsrapport og betales gjennom den vanlige prosessen for refusjon av reiseregning.</span><span class="sxs-lookup"><span data-stu-id="d5f5b-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
