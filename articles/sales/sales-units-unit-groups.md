---
title: Enheter og enhetsgrupper
description: Dette emnet gir informasjon om hvordan du oppretter enheter og enhetsgrupper i Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 345a4f38ad0bc5acddb90cfd8cb3e92154e46513
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081743"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="4f2dc-103">Enheter og enhetsgrupper</span><span class="sxs-lookup"><span data-stu-id="4f2dc-103">Units and unit groups</span></span>

<span data-ttu-id="4f2dc-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="4f2dc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4f2dc-105">Enhetene er antallet eller målene som du kan selge produktene eller tjenestene i.</span><span class="sxs-lookup"><span data-stu-id="4f2dc-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="4f2dc-106">Hvis du for eksempel selger hageutstyr, kan du selge frø i pakker, bokser og paller.</span><span class="sxs-lookup"><span data-stu-id="4f2dc-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="4f2dc-107">En enhetsgruppe er en samling av disse ulike enhetene.</span><span class="sxs-lookup"><span data-stu-id="4f2dc-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="4f2dc-108">Hvis du vil fullføre trinnene i dette emnet, må du sørge for at du er tilordnet rollen Systemadministrator- eller Sales Professional-leder eller tilsvarende tillatelser.</span><span class="sxs-lookup"><span data-stu-id="4f2dc-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="4f2dc-109">Opprette en enhetsgruppe</span><span class="sxs-lookup"><span data-stu-id="4f2dc-109">Create a unit group</span></span>

1. <span data-ttu-id="4f2dc-110">Velg **Enheter** i områdekartet.</span><span class="sxs-lookup"><span data-stu-id="4f2dc-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="4f2dc-111">Velg **Ny** , og skriv inn enhetsnavnet i dialogboksen **Opprett enhetsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="4f2dc-111">Select **New** , and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="4f2dc-112">Skriv inn laveste felles målenheten som produktet skal selges i, i feltet **Primærenhet**.</span><span class="sxs-lookup"><span data-stu-id="4f2dc-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="4f2dc-113">Du kan for eksempel skrive inn "stykk" eller "ounce".</span><span class="sxs-lookup"><span data-stu-id="4f2dc-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="4f2dc-114">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="4f2dc-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="4f2dc-115">Legge til enheter i en enhetsgruppe</span><span class="sxs-lookup"><span data-stu-id="4f2dc-115">Add units to a unit group</span></span>

1. <span data-ttu-id="4f2dc-116">Åpne en enhetsgruppe, og velg **Enheter** i kategorien **Relatert**.</span><span class="sxs-lookup"><span data-stu-id="4f2dc-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="4f2dc-117">Du ser at primærenheten allerede er lagt til.</span><span class="sxs-lookup"><span data-stu-id="4f2dc-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="4f2dc-118">Velg **Legg til ny enhet**. På siden **Hurtigoppretting: Enhet** i **Navn** -feltet angir du navnet på enheten.</span><span class="sxs-lookup"><span data-stu-id="4f2dc-118">Select **Add New Unit** , and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="4f2dc-119">I **Antall** -feltet angir du antallet som enheten skal inneholde.</span><span class="sxs-lookup"><span data-stu-id="4f2dc-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="4f2dc-120">Hvis en boks inneholder for eksempel 2 deler, ville du skrevet "2".</span><span class="sxs-lookup"><span data-stu-id="4f2dc-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="4f2dc-121">I **Basisenhet** -feltet velger du en basisenhet for å fastsette den laveste målenheten for enheten.</span><span class="sxs-lookup"><span data-stu-id="4f2dc-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="4f2dc-122">Du kan for eksempel velge "Stykk".</span><span class="sxs-lookup"><span data-stu-id="4f2dc-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="4f2dc-123">Velg **Lagre** :</span><span class="sxs-lookup"><span data-stu-id="4f2dc-123">Select **Save** :</span></span>
