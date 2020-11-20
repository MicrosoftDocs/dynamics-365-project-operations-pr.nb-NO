---
title: Sende en ressursforespørsel
description: Dette emnet gir informasjon om å sende en forespørsel for en prosjektressurs.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: 50f076b89c5ac7fee4866534cbd47d81f92f3ab3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131291"
---
# <a name="submitting-a-resource-request"></a>Sende en ressursforespørsel

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Du kan sende et generert ressurskrav som en ressursforespørsel. Forespørselen sendes deretter til en ressurslederen for fullføring.

1. Klikk kategorien **Team** på siden **Prosjekter** for å vise en liste over bestillbare ressurser i Project Service Automation (PSA). 
2. Velg den generelle ressursen som har et ressurskrav, fra listen, og klikk deretter **Send forespørsel**.

![Sende en ressursforespørsel](media/RM-how-to-18.png)

Forespørselsstatusen for det generelle teammedlemmet blir endret **Sendt**.

Når forespørselen er utført av ressurslederen, erstattes den generelle ressursen av en navngitt ressurs hvis ressurslederen utfører forespørselen med bestilling av en navngitt ressurs. Ellers blir den generelle ressursen værende i teamet, og forespørselsstatusen endres til **Må gjennomgås** hvis ressurslederen har foreslått en navngitt ressurs.
