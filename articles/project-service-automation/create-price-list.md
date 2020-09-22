---
title: Opprette en prisliste
description: Slik oppretter du en prisliste i Project Service
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: bdd05aea-27a3-431d-9a80-2e220fb25e53
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 756af2fe3bc73d478b0355493aae6f0e49ac5835
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754205"
---
# <a name="create-a-price-list-project-service"></a>Opprette en prisliste (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Prislister gir en mal som kontoadministratorene kan bruke for oppretting av tilbud og prosjekter, og for fastsettelse av kostnadene for et prosjekt. De inneholder et linjeelementliste over roller og utgifter, og prisen du vil ta for hver. Du kan opprette flere prislister, slik at du kan ha separate prisstrukturer for ulike områder du selger produktene i, eller for ulike salgskanaler. Det er en god idé å opprette minst én prisliste for hver valuta du har tenkt å fakturere kundene i.  
  
Hvis du vil opprette økonomiske estimater for arbeid som skal leveres, kontrollerer du at alle prosjekter har en støttekostnads- og salgsprisliste. Definer en standardkostnads- og salgsprisliste som gjelder for alle prosjekter som opprettes i organisasjonen.  
  
Prislister er avhengige av roller og utgiftskategorier, så før du oppretter en prisliste, må du passe på at du allerede har konfigurert rollene og utgiftskategoriene du vil bruke under oppretting av prislisten.  
  
1.  Gå til **Project Service > Prislister**.  
  
2.  Klikk **Ny**.  
  
3.  I **Kontekst** velger du om denne prislisten er for **Kostnad**, **Kjøp** eller **Salg**.  
  
4.  I **Navnet** skriver du inn et navn for prislisten.  
  
5.  I **Valuta** velger du valutaen du vil bruke for fakturering eller etterkalkulering.  
  
6.  I **Tidsenhet** angir du tidsperioden prisen gjelder for, for eksempel dag eller time.  
  
7.  Fyll ut **Startdato**, **Sluttdato** og **Beskrivelse** etter behov.  
  
8.  Klikk **Lagre** for å opprette oppføringen slik at du kan fortsette å redigere den.  
  
9. Hvis du vil legge til en rollepris i prislisten, klikker du **+** under **Rollepriser**.  
  
10. I **Rollepris**-ruten fyller du ut detaljene, og klikker deretter **Lagre**. Fortsett å legge til rollepriser etter behov. Når du er ferdig, klikker du **Lagre** nederst til høyre på skjermen.  
  
11. Hvis du vil legge til en utgiftskategori i prislisten, klikker du **+** under **Kategoripriser**.  
  
12. I **Pris for transaksjonskategorier**-ruten fyller du ut detaljene, og klikker deretter **Lagre**. Fortsett å legge til kategoripriser etter behov. Når du er ferdig, klikker du **Lagre** nederst til høyre på skjermen.  
  
13. Hvis du vil legge til prislisteelementer i prislisten, klikker du **+** under **Prislisteelementer**.  
  
14. I **Prislisteelement**-ruten fyller du ut detaljene, og klikker deretter **Lagre**. Fortsett å legge til prislisteelementer etter behov. Når du er ferdig, klikker du **Lagre** nederst til høyre på skjermen.  
  
15. Hvis du vil legge til distriktsrelasjoner i prislisten, klikker du **+** under **Distriktsrelasjoner**.  
  
16. I **Ny tilkobling**-vinduet fyller du ut detaljene, og klikker deretter **Lagre**. Fortsett å legge til distriktsrelasjoner etter behov. Når du er ferdig, klikker du **Lagre** nederst til høyre på skjermen.  
  
### <a name="see-also"></a>Se også  
 [Konfigurere Project Service Automation](../project-service/configure.md)
