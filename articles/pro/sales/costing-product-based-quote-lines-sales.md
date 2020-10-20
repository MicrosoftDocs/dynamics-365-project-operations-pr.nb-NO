---
title: Produktbaserte tilbudslinjer for kostberegning
description: Dette emnet inneholder informasjon om bruk av en kostpris på en produktbasert tilbudslinje.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 17b377eab5bcbc1a2327cb3ff87cc75d8de40953
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906270"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="ba000-103">Produktbaserte tilbudslinjer for kostberegning</span><span class="sxs-lookup"><span data-stu-id="ba000-103">Costing product-based quote lines</span></span>

<span data-ttu-id="ba000-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="ba000-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="ba000-105">Produktbaserte tilbudslinjer i Dynamics 365 Project Operations har også et **Kostpris**-felt.</span><span class="sxs-lookup"><span data-stu-id="ba000-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="ba000-106">Dette feltet brukes til å spore kostprisen for produktet i tilbudslinjen og for beregning av overskudd nedstrøms.</span><span class="sxs-lookup"><span data-stu-id="ba000-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="ba000-107">Når det opprettes en produktbasert tilbudslinje for et katalogprodukt, hentes kostnadene for den produktbaserte tilbudslinjen som standard fra feltet **Standardkostnad** i produktkatalogen.</span><span class="sxs-lookup"><span data-stu-id="ba000-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="ba000-108">Feltet Standardkostnad i produktkatalogen konfigureres i organisasjonens standardvaluta.</span><span class="sxs-lookup"><span data-stu-id="ba000-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="ba000-109">Standard enhetskostnad på den produktbaserte tilbudslinjen konverteres til salgsvalutaen i tilbudet.</span><span class="sxs-lookup"><span data-stu-id="ba000-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="ba000-110">Enhetskostnad på en produktbasert tilbudslinje</span><span class="sxs-lookup"><span data-stu-id="ba000-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="ba000-111">Formålet med å ha en enhetskostnad på en produktbasert tilbudslinje er å tillate ulike kostnader for et produkt for hvert salg.</span><span class="sxs-lookup"><span data-stu-id="ba000-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="ba000-112">Dette er ikke et typisk scenario, men noen ganger kan det hende at prisen på produktet blir rabattert av leverandøren, avhengig av kunden for det endelige salget.</span><span class="sxs-lookup"><span data-stu-id="ba000-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="ba000-113">Eksempel:</span><span class="sxs-lookup"><span data-stu-id="ba000-113">For example:</span></span>

<span data-ttu-id="ba000-114">Fabrikam Robotics installerer robotarmer på samlebåndene til A Datum Corporation.</span><span class="sxs-lookup"><span data-stu-id="ba000-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="ba000-115">Fabrikam leverer installasjonstjenester, men robotarmene blir skaffet fra Trey Robotics.</span><span class="sxs-lookup"><span data-stu-id="ba000-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="ba000-116">Hvis installasjonen av robotarmer hos A Datum Corporation åpner en ny bransjevertikal for Treys robotarmer, kan Trey gi en spesiell rabatt på denne avtalen til Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="ba000-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="ba000-117">I dette tilfellet vil Fabrikam opprette en produktbasert tilbudslinje for robotarmer og angi en spesiell kostnad per enhet for dette tilbudet.</span><span class="sxs-lookup"><span data-stu-id="ba000-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="ba000-118">Denne kostnaden er forskjellig fra standardkostnaden for Trey Robotic Arms.</span><span class="sxs-lookup"><span data-stu-id="ba000-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>
