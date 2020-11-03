---
title: Planlegge ressurser for et prosjekt
description: Slik planlegger du ressurser for et prosjekt i Project Service
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
ms.openlocfilehash: db69348aac96cbfaaa865228c9230cbda4b1e784
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081826"
---
# <a name="schedule-resources-for-a-project-project-service"></a>Planlegge ressurser for et prosjekt (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Du kan sjekke ressurstilgjengeligheten for å få en oversikt over bestillingene, eller du kan filtrere visningen på ferdigheter, team, plassering og andre alternativer.  
  
Planleggingstavlen viser liste over ressurser og deres tilgjengelighet. Velg en visningsmodus for å vise tilgjengelighet etter **timer** , **dag** , **uke** eller **måned**.  
  
Før du bruker planleggingstavlen, er det viktig å konfigurere den. For mer informasjon, se [Konfigurere tidsplankortet (Field Service eller Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).
  
Hvis du bruker en eldre versjon, kan du sjekke ressurstilgjengelighet under [Vise ressurstilgjengelighet](../psa/view-resource-availability.md).  

> [!IMPORTANT]
>  For å bruke bestillingsfunksjonen for planleggingstavle, geokoding og plasseringstjenester må du slå på kart.  
> 
> 1. På hovedmenyen, klikker du **Ressursplanlegging** > **Administrasjon**.  
> 2. Klikk **Planleggingsparametre**.  
> 3. Åpne oppføring og bla ned til delen **Resource Scheduling Optimization**.  
> 4. I feltet **Koble til kart** velger du **Ja**.  
> 5. Godta vilkårene og lagre oppføringen.  
> 6. På hovedmenyen velger du **Project Service** > **Planleggingstavle**. Herfra er det flere måter å planlegge et bestillingskrav på manuelt. Velg metoden som passer for deg.
  
## <a name="find-available-resources"></a>Finne tilgjengelige ressurser

1.  Fra **Bestillingskrav** -listen høyreklikker du på en ikke planlagt bestilling, og velger ett av følgende:  
  
- Velg **Finn tilgjengelighet – gjeldende ressurser** for å finne en tilgjengelig ressurs fra listen på planleggingstavlen.  
- Velg **Finn tilgjengelighet – alle ressurser** for å finne en tilgjengelig ressurs fra ressurser i systemet  
   > [!NOTE]
   >  Når du gjør dette, viser filtrene alternativer for det valgte bestillingskravet.  
  
2. Når du ser en ledig luke, høyreklikker du tidsluken på planleggingstavlen, og velger **Bestill her**. Eller dra og slipp bestillingskravet til tilgjengelig tidsluke.  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>Bestill en ressurs ved hjelp av daglig visning og finn ut hvem som er underbestilt
  
1.  På planleggingstavlen velger du **Visningsmodus** og velger **Dager**.  
  
    Dette viser en rutenettvisning av hvor mange timer en ressurs er bestilt per dag og hvilke dager som de er gratis.  
  
2.  Klikk navnet på ressursen som du vil reservere, og velg deretter **Bestill**.  
  
3.  I dialogboksen **Ressursbestilling (opprett)** velger du prosjektet som du vil reservere ressursen for, sammen med bestillingsmetoden og start- og sluttidspunkt.  
  
4.  Velg **Bestill** når du er ferdig.  
  
## <a name="view-to-the-schedule-board"></a>Vise planleggingstavlen
  
1.  Velg et bestillingskrav som ikke er planlagt, fra listen nederst.  
  
2.  Dra bestillingskravet til en tilgjengelig ressurs-/tidsluke på planleggingstavlen.  
  
3.  Velg **Bestill** når du er ferdig.  
  
### <a name="additional-resources"></a>Ytterligere ressurser  
 [Veiledning for ressursansvarlig](../psa/resource-manager-guide.md)
