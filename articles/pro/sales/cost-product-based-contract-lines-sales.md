---
title: Produktbaserte kontraktlinjer for kostberegning – Lite
description: Dette emnet gir informasjon om oppretting
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e961bcf32a5dd662b7cd27a23eb5f664c45c292
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177253"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="3ab60-103">Produktbaserte kontraktlinjer for kostberegning – Lite</span><span class="sxs-lookup"><span data-stu-id="3ab60-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="3ab60-104">_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="3ab60-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="3ab60-105">Produktbaserte kontraktlinjer i Dynamics 365 Project operations omfatter feltet **Kostpris**, som lagrer kostprisen for produktet for beregninger av lønnsomhet nedstrøms.</span><span class="sxs-lookup"><span data-stu-id="3ab60-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="3ab60-106">Når det opprettes en produktbasert kontraktlinje for et katalogprodukt, hentes kostnadene for den produktbaserte kontraktlinjen som standard fra feltet **Standardkostnad** i produktkatalogen.</span><span class="sxs-lookup"><span data-stu-id="3ab60-106">When a product-based contract line is created for a catalog product, the cost of the product-based contract line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="3ab60-107">Feltet **Standardkostnad** i produktkatalogen konfigureres i organisasjonens standardvaluta.</span><span class="sxs-lookup"><span data-stu-id="3ab60-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="3ab60-108">Når enhetskostnaden er angitt som standard på kontraktlinjen, blir den konvertert til salgsvalutaen i kontrakten.</span><span class="sxs-lookup"><span data-stu-id="3ab60-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="3ab60-109">Enhetskostnad på en produktbasert kontraktlinje</span><span class="sxs-lookup"><span data-stu-id="3ab60-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="3ab60-110">Ved å ha en enhetskostnad på en produktbasert kontraktlinje er det mulig med ulike produktkostnader for hvert salg av en enhet.</span><span class="sxs-lookup"><span data-stu-id="3ab60-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="3ab60-111">Selv om dette ikke alltid er nødvendig, er det enkelte tilfeller der kunden kan få rabatt på kostnaden for produktet av leverandøren.</span><span class="sxs-lookup"><span data-stu-id="3ab60-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="3ab60-112">Tenk deg følgende scenario:</span><span class="sxs-lookup"><span data-stu-id="3ab60-112">Consider the following scenario:</span></span>

<span data-ttu-id="3ab60-113">Fabrikam Robotics installerer robotarmer på samlebåndene til Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="3ab60-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="3ab60-114">Fabrikam leverer installasjonstjenester, men robotarmene blir skaffet fra Trey Research.</span><span class="sxs-lookup"><span data-stu-id="3ab60-114">Fabrikam provides installation services but the robotic arms are procured from Trey Research.</span></span> <span data-ttu-id="3ab60-115">Hvis installasjonen av robotarmer hos Adatum Corporation åpner en ny bransjevertikal for Trey Research, kan de tilby en spesiell rabatt på denne avtalen til Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="3ab60-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="3ab60-116">I dette tilfellet oppretter Fabrikam en produktbasert kontraktlinje for robotarmer og angir en kostnad per enhet for denne kontrakten, som er forskjellig fra standardkostnaden for robotarmer fra Trey Research.</span><span class="sxs-lookup"><span data-stu-id="3ab60-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms and inputs a per unit cost for this contract that is different from the standard cost of robotic arms from Trey Research.</span></span>
