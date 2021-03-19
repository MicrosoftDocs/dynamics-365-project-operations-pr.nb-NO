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
ms.openlocfilehash: cd60d338e2b2a2d74d4d7f55bb5a1723f10c29ab
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276180"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="cf71d-103">Konfigurere kredittkortintegrering</span><span class="sxs-lookup"><span data-stu-id="cf71d-103">Set up credit card integration</span></span>

<span data-ttu-id="cf71d-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="cf71d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cf71d-105">Utgiftsrelaterte kredittkorttransaksjoner kan konfigureres slik at de importeres automatisk etter en regelmessig tidsplan.</span><span class="sxs-lookup"><span data-stu-id="cf71d-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="cf71d-106">Transaksjonene kan også importeres manuelt etter behov.</span><span class="sxs-lookup"><span data-stu-id="cf71d-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="cf71d-107">Kredittkorttransaksjonene importeres via dataenheten for kredittkorttransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="cf71d-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="cf71d-108">Importere kredittkorttransaksjoner</span><span class="sxs-lookup"><span data-stu-id="cf71d-108">Import credit card transactions</span></span>

1. <span data-ttu-id="cf71d-109">På siden **Kredittkorttransaksjoner** velger du **Importer transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="cf71d-109">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="cf71d-110">Hvis du åpner databehandling for første gang, må systemet oppdatere listen over dataenheter før du kan fortsette.</span><span class="sxs-lookup"><span data-stu-id="cf71d-110">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="cf71d-111">I **Navn**-feltet angir du en unik beskrivelse av importjobben.</span><span class="sxs-lookup"><span data-stu-id="cf71d-111">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="cf71d-112">I feltet **Kildedataformat** velger du formatet til filen som inneholder kredittkorttransaksjonene som skal importeres.</span><span class="sxs-lookup"><span data-stu-id="cf71d-112">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="cf71d-113">Velg **Last opp**, og finn og velg deretter filen som skal importeres.</span><span class="sxs-lookup"><span data-stu-id="cf71d-113">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="cf71d-114">Når du har lastet opp filen, validerer du tilordningen av kredittkorttransaksjonsfilen og kolonnene for dataenheten for kredittkorttransaksjoner ved å velge koblingen **Vis tilordning** på flisen.</span><span class="sxs-lookup"><span data-stu-id="cf71d-114">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="cf71d-115">Hvis det finnes tilordningsfeil, eller hvis du må endre tilordningen, må du gjøre tilordningen fra kategorien **Tilordningsvisualisering** eller kategorien **Tilordningsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="cf71d-115">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="cf71d-116">Hvis du vil automatisere kredittkorttransaksjonene, velger du **Opprett regelmessig datajobb**.</span><span class="sxs-lookup"><span data-stu-id="cf71d-116">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="cf71d-117">Deretter kan du angi regelmessigheten som definerer hvor ofte kredittkorttransaksjoner skal importeres.</span><span class="sxs-lookup"><span data-stu-id="cf71d-117">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="cf71d-118">Velg **OK** når du er ferdig.</span><span class="sxs-lookup"><span data-stu-id="cf71d-118">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="cf71d-119">Hvis du vil importere den valgte filen nå, velger du **Importer**.</span><span class="sxs-lookup"><span data-stu-id="cf71d-119">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="cf71d-120">Hvis det oppstår feil under importen, kan du vise utførelsesloggen eller oppsamlingsdataene for å se feilene du må rette for å sikre en vellykket import.</span><span class="sxs-lookup"><span data-stu-id="cf71d-120">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="cf71d-121">Hvis du må importere mer enn ett filformat, må du opprette separate importjobber for hver formattype.</span><span class="sxs-lookup"><span data-stu-id="cf71d-121">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="cf71d-122">Tilordne kredittkorttransaksjonene på nytt for avsluttede ansatte</span><span class="sxs-lookup"><span data-stu-id="cf71d-122">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="cf71d-123">Når en ansattoppføring avsluttes, deaktiveres kontoen for den ansattes Active Directory Domain Services (AD DS).</span><span class="sxs-lookup"><span data-stu-id="cf71d-123">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="cf71d-124">Det kan imidlertid hende at det finnes aktive kredittkorttransaksjoner som fremdeles må belastes og refunderes.</span><span class="sxs-lookup"><span data-stu-id="cf71d-124">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="cf71d-125">På siden **Kredittkorttransaksjoner** kan du tilordne den ansatte på nytt for en hvilken som helst kredittkorttransaksjon der den tilknyttede ansatte er avsluttet.</span><span class="sxs-lookup"><span data-stu-id="cf71d-125">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="cf71d-126">Velg en eller flere kredittkorttransaksjoner, og velg deretter **Tilordne transaksjoner på nytt**.</span><span class="sxs-lookup"><span data-stu-id="cf71d-126">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="cf71d-127">Du kan deretter velge en annen ansatt du vil tilordne kredittkorttransaksjonene til.</span><span class="sxs-lookup"><span data-stu-id="cf71d-127">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="cf71d-128">Når kredittkorttransaksjonene er tilordnet på nytt, kan de velges for en utgiftsrapport og betales gjennom den vanlige prosessen for refusjon av reiseregning.</span><span class="sxs-lookup"><span data-stu-id="cf71d-128">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]