---
title: Hvorfor kan jeg ikke slette oppføringer fra den faktiske enheten?
description: Dette emnet gir informasjon om hvorfor du ikke kan slette oppføringer fra den faktiske enheten.
author: JPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: e3122c5d9495b3ff9a683f477e719ce0c228a84d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286080"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="34027-103">Hvorfor kan jeg ikke slette oppføringer fra den faktiske enheten?</span><span class="sxs-lookup"><span data-stu-id="34027-103">Why can’t I delete records from the Actuals entity?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="34027-104">Project Service Automation (PSA) tillater ikke sletting av faktiske verdier fordi de fungerer som kilden til sannheten for transaksjoner som har finansielle implikasjoner, til systemer på lavere nivåer, for eksempel hovedboken.</span><span class="sxs-lookup"><span data-stu-id="34027-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="34027-105">Hvis faktiske verdier kan slettes, kan det være det blir stilt spørsmål om integriteten til regnskapstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="34027-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="34027-106">Kunder bør bruke journaler til å opprette kompenserende transaksjoner for å etablere et revisjonsspor.</span><span class="sxs-lookup"><span data-stu-id="34027-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]