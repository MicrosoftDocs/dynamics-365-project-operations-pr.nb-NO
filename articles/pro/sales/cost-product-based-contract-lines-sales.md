---
title: Produktbaserte kontraktlinjer for kostberegning – Lite
description: Dette emnet gir informasjon om oppretting
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9458a57863244a68359f57185325c03a46bd6569
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003553"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="d6750-103">Produktbaserte kontraktlinjer for kostberegning – Lite</span><span class="sxs-lookup"><span data-stu-id="d6750-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="d6750-104">_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="d6750-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="d6750-105">Produktbaserte kontraktlinjer i Dynamics 365 Project Operations inneholder feltet **Kostnadspris**, som lagrer kostnadsprisen på produktet for beregninger av nedstrømslønnsomhet.</span><span class="sxs-lookup"><span data-stu-id="d6750-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="d6750-106">Når en produktbasert kontraktlinje opprettes for et katalogprodukt, brukes standardkostnaden for linjen fra feltet **Standardkostnad** i produktkatalogen.</span><span class="sxs-lookup"><span data-stu-id="d6750-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="d6750-107">Feltet **Standardkostnad** i produktkatalogen konfigureres i organisasjonens standardvaluta.</span><span class="sxs-lookup"><span data-stu-id="d6750-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="d6750-108">Når enhetskostnaden er angitt som standard på kontraktlinjen, blir den konvertert til salgsvalutaen i kontrakten.</span><span class="sxs-lookup"><span data-stu-id="d6750-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="d6750-109">Enhetskostnad på en produktbasert kontraktlinje</span><span class="sxs-lookup"><span data-stu-id="d6750-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="d6750-110">Ved å ha en enhetskostnad på en produktbasert kontraktlinje er det mulig med ulike produktkostnader for hvert salg av en enhet.</span><span class="sxs-lookup"><span data-stu-id="d6750-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="d6750-111">Selv om dette ikke alltid er nødvendig, er det enkelte tilfeller der kunden kan få rabatt på kostnaden for produktet av leverandøren.</span><span class="sxs-lookup"><span data-stu-id="d6750-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="d6750-112">Tenk deg følgende scenario:</span><span class="sxs-lookup"><span data-stu-id="d6750-112">Consider the following scenario:</span></span>

<span data-ttu-id="d6750-113">Fabrikam Robotics installerer robotarmer på samlebåndene til Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="d6750-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="d6750-114">Fabrikam tilbyr installasjonstjenester, men robotarmene kommer fra Trey Research.</span><span class="sxs-lookup"><span data-stu-id="d6750-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="d6750-115">Hvis installasjonen av robotarmer hos Adatum Corporation åpner en ny bransjevertikal for Trey Research, kan de tilby en spesiell rabatt på denne avtalen til Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="d6750-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="d6750-116">I dette tilfellet oppretter Fabrikam en produktbasert kontraktlinje for robotarmer.</span><span class="sxs-lookup"><span data-stu-id="d6750-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="d6750-117">Det angis en enhetskostnad per for denne kontrakten.</span><span class="sxs-lookup"><span data-stu-id="d6750-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="d6750-118">Kostnaden er forskjellig fra kostnaden for robotarmer fra Trey Research.</span><span class="sxs-lookup"><span data-stu-id="d6750-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]