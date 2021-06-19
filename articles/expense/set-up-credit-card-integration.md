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
ms.openlocfilehash: 3555e894e206c2aafb30b0df1e52efadd69b0713
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001840"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="f793b-103">Konfigurer kredittkortintegrering</span><span class="sxs-lookup"><span data-stu-id="f793b-103">Set up credit card integration</span></span>

<span data-ttu-id="f793b-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="f793b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f793b-105">Utgiftsrelaterte kredittkorttransaksjoner kan konfigureres slik at de importeres automatisk etter en regelmessig tidsplan.</span><span class="sxs-lookup"><span data-stu-id="f793b-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="f793b-106">Transaksjonene kan også importeres manuelt etter behov.</span><span class="sxs-lookup"><span data-stu-id="f793b-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="f793b-107">Kredittkorttransaksjonene importeres via dataenheten for kredittkorttransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="f793b-107">The credit card transactions are imported through the credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="f793b-108">Importere kredittkorttransaksjoner</span><span class="sxs-lookup"><span data-stu-id="f793b-108">Import credit card transactions</span></span>

<span data-ttu-id="f793b-109">Følg denne fremgangsmåten for å importere kredittkorttransaksjoner:</span><span class="sxs-lookup"><span data-stu-id="f793b-109">To import credit card transactions, follow these steps:</span></span>

1. <span data-ttu-id="f793b-110">På siden **Kredittkorttransaksjoner** velger du **Importer transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="f793b-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="f793b-111">Hvis du åpner databehandling for første gang, må systemet oppdatere listen over dataenheter før du kan fortsette.</span><span class="sxs-lookup"><span data-stu-id="f793b-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="f793b-112">I **Navn**-feltet angir du en unik beskrivelse av importjobben.</span><span class="sxs-lookup"><span data-stu-id="f793b-112">In the **Name** field, enter a unique description for the import job.</span></span>
3. <span data-ttu-id="f793b-113">I feltet **Kildedataformat** velger du formatet til filen som inneholder kredittkorttransaksjonene som skal importeres.</span><span class="sxs-lookup"><span data-stu-id="f793b-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="f793b-114">Velg **Last opp**, og finn og velg deretter filen som skal importeres.</span><span class="sxs-lookup"><span data-stu-id="f793b-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="f793b-115">Når du har lastet opp filen, validerer du tilordningen av kredittkorttransaksjonsfilen og kolonnene for dataenheten for kredittkorttransaksjoner ved å velge koblingen **Vis tilordning** på flisen.</span><span class="sxs-lookup"><span data-stu-id="f793b-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="f793b-116">Hvis det finnes tilordningsfeil, eller hvis du må endre tilordningen, må du gjøre tilordningen fra kategorien **Tilordningsvisualisering** eller kategorien **Tilordningsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="f793b-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="f793b-117">Hvis du vil automatisere kredittkorttransaksjonene, velger du **Opprett regelmessig datajobb**.</span><span class="sxs-lookup"><span data-stu-id="f793b-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="f793b-118">Deretter kan du angi regelmessigheten som definerer hvor ofte kredittkorttransaksjoner skal importeres.</span><span class="sxs-lookup"><span data-stu-id="f793b-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="f793b-119">Velg **OK** når du er ferdig.</span><span class="sxs-lookup"><span data-stu-id="f793b-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="f793b-120">Hvis du vil importere den valgte filen nå, velger du **Importer**.</span><span class="sxs-lookup"><span data-stu-id="f793b-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="f793b-121">Hvis det oppstår feil under importen, kan du vise utføringsloggen eller oppsamlingsdataene for å se feilene du må rette opp, for å sikre at importen blir vellykket.</span><span class="sxs-lookup"><span data-stu-id="f793b-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help ensure a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="f793b-122">Hvis du må importere mer enn ett filformat, må du opprette separate importjobber for hver formattype.</span><span class="sxs-lookup"><span data-stu-id="f793b-122">If you need to import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="f793b-123">Tilordne kredittkorttransaksjonene på nytt for avsluttede ansatte</span><span class="sxs-lookup"><span data-stu-id="f793b-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="f793b-124">Når en ansattoppføring avsluttes, deaktiveres kontoen for den ansattes Active Directory Domain Services (AD DS).</span><span class="sxs-lookup"><span data-stu-id="f793b-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="f793b-125">Det kan imidlertid hende at det finnes aktive kredittkorttransaksjoner som fremdeles må belastes og refunderes.</span><span class="sxs-lookup"><span data-stu-id="f793b-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="f793b-126">På **Kredittkorttransaksjoner**-siden kan du tilordne den ansatte på nytt for en kredittkorttransaksjon der den tilknyttede ansatte er avsluttet.</span><span class="sxs-lookup"><span data-stu-id="f793b-126">On the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="f793b-127">Velg en eller flere kredittkorttransaksjoner, og velg deretter **Tilordne transaksjoner på nytt**.</span><span class="sxs-lookup"><span data-stu-id="f793b-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="f793b-128">Du kan deretter velge en annen ansatt du vil tilordne kredittkorttransaksjonene til.</span><span class="sxs-lookup"><span data-stu-id="f793b-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="f793b-129">Når kredittkorttransaksjonene er tilordnet på nytt, kan de velges for en utgiftsrapport og betales gjennom den vanlige prosessen for refusjon av reiseregning.</span><span class="sxs-lookup"><span data-stu-id="f793b-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

## <a name="delete-credit-card-transactions"></a><span data-ttu-id="f793b-130">Slette kredittkorttransaksjoner</span><span class="sxs-lookup"><span data-stu-id="f793b-130">Delete credit card transactions</span></span> 

<span data-ttu-id="f793b-131">Noen ganger kan det hende at enkelte transaksjoner må slettes etter at kredittkorttransaksjoner er importert.</span><span class="sxs-lookup"><span data-stu-id="f793b-131">Sometimes, after credit card transactions are imported, certain transactions may need to be deleted.</span></span> <span data-ttu-id="f793b-132">Dette kan skyldes at transaksjonene er duplikater eller fordi dataene kanskje ikke er nøyaktige.</span><span class="sxs-lookup"><span data-stu-id="f793b-132">This could be because the transactions are duplicates or because the data might isn't accurate.</span></span> <span data-ttu-id="f793b-133">Administratorer kan bruke funksjonen **"Slett kredittkorttransaksjoner"** for å velge og slette kredittkorttransaksjoner som **ikke er knyttet til** en utgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="f793b-133">Admins can use the **"Delete credit card transactions"** feature to select and delete credit card transactions that are **not attached** to an expense report.</span></span> 

1. <span data-ttu-id="f793b-134">Gå til **Periodiske oppgaver** > **Slett kredittkorttransaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="f793b-134">Go to **Periodic tasks** > **Delete credit card transactions**.</span></span>
2. <span data-ttu-id="f793b-135">Velg **Filter**, og oppgi informasjon for å identifisere oppføringene som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="f793b-135">Select **Filter** and provide information to identify the records to include.</span></span>
3. <span data-ttu-id="f793b-136">Velg **OK** for å slette oppføringene.</span><span class="sxs-lookup"><span data-stu-id="f793b-136">Select **OK** to delete the records.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
