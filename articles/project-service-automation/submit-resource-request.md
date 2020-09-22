---
title: Send en ressursforespørsel
description: Dette emnet gir informasjon om å sende en forespørsel for en prosjektressurs.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
author: JohnPBurrows
ms.assetid: 9f4a6315-3905-4b15-8d06-e5dae30ccbb8
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2b706ae25af5ba85647c98353b5950663fafc292
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754161"
---
# <a name="submit-a-resource-request"></a>Send en ressursforespørsel

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Du kan sende et generert ressurskrav som en ressursforespørsel. Forespørselen sendes deretter til en ressurslederen for fullføring.

1. Klikk kategorien **Team** på siden **Prosjekter** for å vise en liste over bestillbare ressurser i Project Service Automation (PSA). 
2. Velg den generelle ressursen som har et ressurskrav, fra listen, og klikk deretter **Send forespørsel**.

![Sende en ressursforespørsel](media/RM-how-to-18.png)

Forespørselsstatusen for det generelle teammedlemmet blir endret **Sendt**.

Når forespørselen er utført av ressurslederen, erstattes den generelle ressursen av en navngitt ressurs hvis ressurslederen utfører forespørselen med bestilling av en navngitt ressurs. Ellers blir den generelle ressursen værende i teamet, og forespørselsstatusen endres til **Må gjennomgås** hvis ressurslederen har foreslått en navngitt ressurs.
