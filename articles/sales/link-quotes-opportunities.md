---
title: Opprett prosjekttilbud fra salgsmuligheter
description: Denne emnet gir informasjon om oppretting av et prosjekttilbud fra en salgsmulighet.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081532"
---
# <a name="create-project-quotes-from-opportunities"></a>Opprett prosjekttilbud fra salgsmuligheter

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Tilbud kan opprettes fra prosjektmuligheter på følgende måter:

- Fra kategorien **Tilbud** på siden **Prosjektmuligheter**
- Fra flyten Salgsprosess for salgsmulighet
- Ved å oppdatere salgsmulighetsreferansen for et eksisterende tilbud

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a>Fra kategorien Tilbud på siden Prosjektmuligheter

Du kan opprette et prosjekttilbud fra en salgsmulighet ved å følge fremgangs måten nedenfor.

1. Åpne siden **Prosjektmuligheter** , og velg kategorien **Tilbud**. 
2. I delrutenettet **Tilbud** velger du **+** for å opprette det nye prosjekttilbudet basert på salgsmuligheten. Alle salgsmulighetslinjene og de relaterte prosjektprislistene kopieres til det nye tilbudet fra salgsmuligheten.

## <a name="from-the-opportunity-sales-process-flow"></a>Fra flyten Salgsprosess for salgsmulighet

Du kan opprette et tilbud fra flyten Salgsprosess for salgsmulighet ved å følge fremgangs måten nedenfor.

1. Åpne salgsmuligheten fra flyten Salgsprosess for salgsmulighet.
2. Velg fasen **Kvalifiser**. 
3. Velg **Neste** , og velg deretter **+ Opprett** for å opprette et nytt tilbud. Det meste av informasjonen i kategorien **Sammendrag** for dette nye tilbudet hentes som standard fra salgsmuligheten. 
4. Angi eventuell nødvendig informasjon som mangler, eller oppdater standardverdiene etter behov i kategorien **Sammendrag**.
5. Velg **Lagre**. Det nye tilbudet opprettes og knyttes til salgsmuligheten. Du kan nå vise tilbudsinformasjonen i kategorien **Tilbud** på siden **Salgsmulighet**. 

   Salgsprosessen for salgsmuligheten flyttes til neste fase, **Foreslå**.


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a>Ved å oppdatere salgsmulighetsreferansen for et eksisterende tilbud

Et eksisterende tilbud kan kobles til en salgsmulighet. Fullfør fremgangsmåten nedenfor for å oppdatere salgsmulighetsinformasjonen for et eksisterende tilbud.

1. Åpne siden **Tilbud** , og velg kategorien **Sammendrag**.
2. I **Salgsmulighet** -feltet velger du salgsmuligheten du vil knytte til tilbudet. Du kan se tilbudet i rutenettet **Tilbud** for salgsmuligheten. 
3. Ved hjelp av salgsprosessen for salgsmuligheten kan salgsmuligheten flyttes til neste fase, **Foreslå**. 

   Når du flytter en salgsmulighet til denne fasen, kan du velge dette tilbudet fra en liste over tilbud som er knyttet til denne salgsmuligheten. Hvis du velger dette tilbudet, angir du at det skal flyttes fremover.

   Alle de andre tilbudene som er knyttet til salgsmuligheten, vil fremdeles være tilgjengelig eog aktivee til ett av dem er vunnet. Du kan flytte salgsprosessen tilbake til den forrige fasen, **Kvalifiser** , og velge et nytt tilbud å flytte fremover med.
