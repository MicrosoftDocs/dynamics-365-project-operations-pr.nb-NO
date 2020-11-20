---
title: Definere ressurskalendere
description: Dette emnet gir informasjon om hvordan du definerer arbeidstidskalendrene for ressurser i Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: daa49cf8ba9ba005a16777f590c4c06d024de529
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123930"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="33e65-103">Definere ressurskalendere</span><span class="sxs-lookup"><span data-stu-id="33e65-103">Define resource calendars</span></span>

<span data-ttu-id="33e65-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="33e65-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="33e65-105">Hver bestillbare ressurs som arbeider i et prosjekt, må ha en kalender for arbeidstid for å definere tilgjengeligheten deres.</span><span class="sxs-lookup"><span data-stu-id="33e65-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="33e65-106">Arbeidstimer for en ressurs kan defineres på to måter:</span><span class="sxs-lookup"><span data-stu-id="33e65-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="33e65-107">Definere individuelle kalenderregler for en ressurs</span><span class="sxs-lookup"><span data-stu-id="33e65-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="33e65-108">Bruke en eksisterende kalendermal for ressursen</span><span class="sxs-lookup"><span data-stu-id="33e65-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="33e65-109">Definerer arbeidstimer for en ressurs</span><span class="sxs-lookup"><span data-stu-id="33e65-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="33e65-110">Velg **Ressurser** på **Ressurser**-menyen.</span><span class="sxs-lookup"><span data-stu-id="33e65-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="33e65-111">Velg den aktuelle **bestillbare ressursen** i rutenettvisningen.</span><span class="sxs-lookup"><span data-stu-id="33e65-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="33e65-112">På siden **Ressursdetaljer** velger du kategorien **Arbeidstid**. Som standard vil kalenderen for bestillbare ressurser ha arbeidstimene til standard arbeidstidsmal som er definert for organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="33e65-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="33e65-113">Hvis du vil oppdatere arbeidstiden, høyre klikker du startdatoen for den foreslåtte kalenderregelen som skal defineres.</span><span class="sxs-lookup"><span data-stu-id="33e65-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="33e65-114">Bruk kalenderregelmenyen til å definere en kalenderregel for en bestemt dag, resten av serien eller hele kalenderen.</span><span class="sxs-lookup"><span data-stu-id="33e65-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="33e65-115">Når alternativet er valgt, kan du deretter definere følgende:</span><span class="sxs-lookup"><span data-stu-id="33e65-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="33e65-116">Hvilken dag i uken arbeidstimene skal gjelde for.</span><span class="sxs-lookup"><span data-stu-id="33e65-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="33e65-117">Arbeidstiden for hver dag.</span><span class="sxs-lookup"><span data-stu-id="33e65-117">The working times within each day.</span></span>
    - <span data-ttu-id="33e65-118">Den lokale tidssonen for kalenderregelen.</span><span class="sxs-lookup"><span data-stu-id="33e65-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="33e65-119">Hvis det er aktuelt, kan du også angi ikke-arbeidstid for regelen.</span><span class="sxs-lookup"><span data-stu-id="33e65-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="33e65-120">Bruke en kalendermal for en ressurs</span><span class="sxs-lookup"><span data-stu-id="33e65-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="33e65-121">Velg **Ressurser** på **Ressurser**-menyen.</span><span class="sxs-lookup"><span data-stu-id="33e65-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="33e65-122">I rutenettvisningen kan du velge opptil 25 **bestillbare ressurser** som skal oppdateres.</span><span class="sxs-lookup"><span data-stu-id="33e65-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="33e65-123">Velg **Angi kalender**, og en dialogboks vil be om en liste over tilgjengelige arbeidstidsmaler.</span><span class="sxs-lookup"><span data-stu-id="33e65-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="33e65-124">Velg malen malen du vil bruke, og velg deretter **Bruk**.</span><span class="sxs-lookup"><span data-stu-id="33e65-124">Select the template you want to use, and then select **Apply**.</span></span>
