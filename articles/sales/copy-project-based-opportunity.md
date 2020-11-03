---
title: Kopiere prosjektbaserte salgsmuligheter
description: Dette emnet gir informasjon om hvordan du kopierer prosjektbaserte salgsmuligheter i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 89f5a63581f36b30634bdd302a6d360d6b5e75bd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081559"
---
# <a name="copy-project-based-opportunities"></a>Kopiere prosjektbaserte salgsmuligheter

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_


Salgsmuligheter for prosjekter kan enkelt kopieres for å opprette nye salgsmuligheter for prosjekter. 

1. Gå til siden med **salgsmuligheter for prosjekter** , og velg en salgsmulighet fra listen. Du kan også åpne siden med detaljer for en bestemt salgsmulighet. 
2. Velg **Kopier** på en av sidene. En dialogside som inneholder følgende feltinformasjon, åpnes. Kopieringsprosessen kan endres avhengig av verdiene du velger i denne dialogen.

    | **Felt** | **Relevans, formål og veiledning** | **Nedstrøms påvirkning** |
    | --- | --- | --- |
    | Emne | Angi relevant emne for salgsmuligehten. Når dialogboksen åpnes, setter systemet den til emnet for kildesalgsmuligheten med **-kopi** lagt til. | Dette feltet har ingen nedstrøms påvirkning. |
    | Konto | Referanser til kundens firma- eller forretningsforbindelsesoppføring. Når dialogboksen åpnes, setter systemet den til kontoen i kildesalgsmuligheten. | Dette feltet er den primære kunden for salgsmuligheten. |
    | Kontraktsenhet | Organisasjonsenheten som er ansvarlig for levering av prosjektene tilknyttet denne avtalen. Når dialogboksen åpnes, setter systemet den til kontraktenheten for kildesalgsmuligheten. | Kontraktenheten er avdelingen i firmaet som skal kjøre prosjektene etter at avtalen er lukket. Hver kontraktenhet har en valuta, og denne valutaen brukes til å rapportere beregnet og faktisk kostnad som påløpte under prosjektet. |
    | Valuta | Dette er valutaen som avtaletransaksjonene utføres i. Når dialogsiden åpnes, setter systemet den til valutaen for kildesalgsmuligheten. | Valutaen brukes til å standardisere en prisliste og bygge inn finansielle estimater i tilbudet. Til slutt brukes valutaen til å fakturere kunden når avtalen er vunnet. |
    | Kopier pris | En Ja/Nei-verdi som angir om prisingen for salgsmuligheten skal kopieres fra kildesalgsmuligheten. | Hvis **Ja** er valgt, kopieres prislistene fra kilde- til målsalgsmuligheten. Hvis du velger **Nei** , blir prislistene standard på nytt basert på de siste prislistene som ble definert. |

3. Velg **OK**. Systemet oppretter en kopi av prosjektsalgsmuligheten basert på de valgte parameterne, og den nye salgsmuligheten for prosjektet åpnes.
