---
title: Avinstaller Dynamics 365 Project Operations
description: Dette emnet inneholder informasjon om hvordan du avinstallerer Dynamics 365 Project Operations.
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b87c9324b1c95c10ef1e18b0fbf4572bdbe76827
ms.sourcegitcommit: b8b7a59eee7d93638446e93726d270316e45ab3d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783655"
---
# <a name="uninstall-dynamics-365-project-operations"></a>Avinstaller Dynamics 365 Project Operations 

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Hvis du vil avinstallere Dynamics 365 Project Operations, må du være tilordnet rollen administrator.

1. Gå til **Innstillinger** > **Løsninger**.

    ![Innstillinger-siden.](./media/uninstall-proj-ops-solutions.png)
  
2. Fjern løsningene i nøyaktig samme rekkefølge som den de vises i, i tabellen nedenfor. 

    | Trinn | Løsningsnavn                                    | Merk                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 1 | msdyn_ProjectServiceUpgrade_managed.cab            | Hvis den ikke blir funnet, hopper du over denne løsningen.                                                            |
    | 2 | ProjectOperations_Anchor                           | Hvis den ikke blir funnet, hopper du over denne løsningen.                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | Hvis den ikke blir funnet, hopper du over denne løsningen.                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | Hvis den ikke blir funnet, hopper du over denne løsningen.                                                            |
    | 5 | ProjectService                                     | Ingen flere merknader.                                                                         |
    | 6 | ProjectServiceCore_Patch                           | Ingen flere merknader.                                                                         |
    | 7 | ProjectServiceCore                                 | Ingen flere merknader.                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | Hvis den ikke blir funnet, hopper du over denne løsningen.                                                            |
    | 9 | FieldServiceCommon                                 | Kreves for dobbeltskriving med Dynamics 365 Finance eller Dynamics 365 Supply Chain Management.   |
    | 10 | msdyn_AssetCommon                                  | Kreves for dobbeltskriving med Dynamics 365 Finance eller Dynamics 365 Supply Chain Management.   |
    | 11 | msdyn_TESA_Anchor                                  | Kreves for Dynamics 365 Field Service.                                                     |
    | 12 | msdyn_TESA_Patch                                   | Kreves for Dynamics 365 Field Service.                                                     |
    | 13 | msdyn_TESA                                         | Kreves for Dynamics 365 Field Service.                                                     |
    | 14 | ResourceSchedulingControls                         | Kreves for Dynamics 365 Field Service.                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Kreves for Dynamics 365 Field Service.                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | Kreves for Dynamics 365 Field Service.                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Kreves for Dynamics 365 Field Service.                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | Hvis den ikke blir funnet, hopper du over denne løsningen.                                                            |
    | 19 | Dynamics365Notes                                   | Hvis den ikke blir funnet, hopper du over denne løsningen.                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | Hvis den ikke blir funnet, hopper du over denne løsningen.                                                            |
    | 21 | DualWriteCore                                      | Hvis den ikke blir funnet, hopper du over denne løsningen.                                                            |
    | 22 | Dynamics365AssetManagementApp                      | Hvis den ikke blir funnet, hopper du over denne løsningen.                                                            |
    | 23 | Dynamics365AssetManagement                         | Hvis den ikke blir funnet, hopper du over denne løsningen.                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | Hvis den ikke blir funnet, hopper du over denne løsningen.                                                            |
    | 25 | Dynamics365FinanceExtended                         | Hvis den ikke blir funnet, hopper du over denne løsningen.                                                            |
    | 26 | HCMCommon                                          | Hvis den ikke blir funnet, hopper du over denne løsningen.                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | Hvis den ikke blir funnet, hopper du over denne løsningen.                                                            |
    | 28 | Part                                              | Hvis den ikke blir funnet, hopper du over denne løsningen.                                                            |
    | 29 | Dynamics365Company                                 | Hvis den ikke blir funnet, hopper du over denne løsningen.                                                            |
    | 30 | CurrencyExchangeRates                              | Hvis den ikke blir funnet, hopper du over denne løsningen.                                                            |
    | 31 | AssetCommon                                        | Hvis den ikke blir funnet, hopper du over denne løsningen.                                                            |
