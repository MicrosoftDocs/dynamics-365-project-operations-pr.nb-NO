---
title: Opprette organisasjonsenheter
description: Slik oppretter du organisasjonsenheter i Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 4c653f5bd066fd174c8fb0996820628c1b281519
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081669"
---
# <a name="create-organizational-units-project-service"></a><span data-ttu-id="b6c96-103">Opprette organisasjonsenheter (Project Service)</span><span class="sxs-lookup"><span data-stu-id="b6c96-103">Create organizational units (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="b6c96-104">Selskapet ditt organiserer sannsynligvis sin konsulentvirksomhet etter geografi, funksjon eller andre områder.</span><span class="sxs-lookup"><span data-stu-id="b6c96-104">Your company probably organizes its consulting business by geography, function, or other areas.</span></span> <span data-ttu-id="b6c96-105">Du kan opprette organisasjonsenheter som gjenspeiler konsulentvirksomheten.</span><span class="sxs-lookup"><span data-stu-id="b6c96-105">You can create organizational units that reflect your consulting business.</span></span> <span data-ttu-id="b6c96-106">En [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-organisasjonsenhet er en gruppe eller en avdeling i et profesjonelt servicefirma som bruker fakturerbare ressurser med kostnadsrater som er atskilt fra andre slike grupper eller avdelinger i firmaet.</span><span class="sxs-lookup"><span data-stu-id="b6c96-106">A [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] organizational unit is a group or division in a professional services company that employs billable resources with cost rates that are distinct from other such groups or divisions in the company.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b6c96-107">En [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-organisasjonsenhet er atskilt fra en forretningsenhet i [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="b6c96-107">A [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] organizational unit is separate from a business unit in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span></span> <span data-ttu-id="b6c96-108">Forretningsenheter er mer en sikkerhetsstruktur som påvirker tilgangsnivåer til [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)]-informasjon, og er vanligvis organisert rundt firmaets divisjoner, for eksempel overordnet selskap og datterselskaper eller avdelinger.</span><span class="sxs-lookup"><span data-stu-id="b6c96-108">Business units are more of a security structure that affects levels of access to [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] information, and are usually organized around company divisions, like parent company and subsidiaries or divisions.</span></span> <span data-ttu-id="b6c96-109">Organisasjonsenheter representerer hvordan ditt konsulentfirma kategoriserer de ulike virksomhetene, enten etter geografisk plassering (for eksempel EMEA eller LATAM), etter funksjon (som produktutvikling eller IT-utsetting) eller andre parametere.</span><span class="sxs-lookup"><span data-stu-id="b6c96-109">Organizational units represent how your consulting company categorizes its different businesses, whether by geographic location (like EMEA or LATAM), by function (like Product Development or IT Outsourcing), or by other parameters.</span></span>  
  
1.  <span data-ttu-id="b6c96-110">Gå til **Project Service > Organisasjonsenheter**.</span><span class="sxs-lookup"><span data-stu-id="b6c96-110">Go to **Project Service > Organizational Units**.</span></span>  
  
2.  <span data-ttu-id="b6c96-111">Klikk **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b6c96-111">Click **New**.</span></span>  
  
3.  <span data-ttu-id="b6c96-112">I **Generelt** -området angir du et navn for organisasjonsenheten under **Navn** og fyller deretter ut de andre feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="b6c96-112">In the **General** area, enter a name for the organization unit in **Name** , and fill in the other fields as necessary.</span></span>  
  
4.  <span data-ttu-id="b6c96-113">Klikk **Lagre** for å opprette oppføringen slik at du kan fortsette å redigere den.</span><span class="sxs-lookup"><span data-stu-id="b6c96-113">Click **Save** to create the record so you can continue editing it.</span></span>  
  
5.  <span data-ttu-id="b6c96-114">Under **Kostprislister** klikker du **+** for å legge til en prisliste.</span><span class="sxs-lookup"><span data-stu-id="b6c96-114">Under **Cost Price Lists** , click **+** to add a price list.</span></span> <span data-ttu-id="b6c96-115">Du kan bare legge til prislister med **Kostnad** -konteksten her.</span><span class="sxs-lookup"><span data-stu-id="b6c96-115">You can only add price lists with the **Cost** context here.</span></span>  
  
6.  <span data-ttu-id="b6c96-116">I **Navn** -feltet klikker du **Søk** -knappen og velger en prisliste du vil gjøre tilgjengelig for denne organisasjonsenheten.</span><span class="sxs-lookup"><span data-stu-id="b6c96-116">In the **Name** field, click the **Search** button and select a price list you want to make available to this organizational unit.</span></span> <span data-ttu-id="b6c96-117">Fortsett å legge til prislister etter behov.</span><span class="sxs-lookup"><span data-stu-id="b6c96-117">Continue adding price lists as needed.</span></span>  
  
7.  <span data-ttu-id="b6c96-118">Når du er ferdig, klikker du **Lagre** nederst til høyre på skjermen.</span><span class="sxs-lookup"><span data-stu-id="b6c96-118">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="b6c96-119">Se også</span><span class="sxs-lookup"><span data-stu-id="b6c96-119">See Also</span></span>  
 [<span data-ttu-id="b6c96-120">Konfigurere Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b6c96-120">Configure Project Service Automation</span></span>](../psa/configure.md)
