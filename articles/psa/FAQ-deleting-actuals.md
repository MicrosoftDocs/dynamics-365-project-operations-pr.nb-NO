---
title: Hvorfor kan jeg ikke slette oppføringer fra den faktiske enheten?
description: Dette emnet gir informasjon om hvorfor du ikke kan slette oppføringer fra den faktiske enheten.
author: JPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
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
ms.openlocfilehash: 434be93cedb4772616b1e6d5cbe15fc715eed19a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993113"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="910ec-103">Hvorfor kan jeg ikke slette oppføringer fra den faktiske enheten?</span><span class="sxs-lookup"><span data-stu-id="910ec-103">Why can’t I delete records from the Actuals entity?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="910ec-104">Project Service Automation (PSA) tillater ikke sletting av faktiske verdier fordi de fungerer som kilden til sannheten for transaksjoner som har finansielle implikasjoner, til systemer på lavere nivåer, for eksempel hovedboken.</span><span class="sxs-lookup"><span data-stu-id="910ec-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="910ec-105">Hvis faktiske verdier kan slettes, kan det være det blir stilt spørsmål om integriteten til regnskapstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="910ec-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="910ec-106">Kunder bør bruke journaler til å opprette kompenserende transaksjoner for å etablere et revisjonsspor.</span><span class="sxs-lookup"><span data-stu-id="910ec-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]