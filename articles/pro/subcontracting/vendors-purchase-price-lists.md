---
title: Administrasjon av leverandør- og innkjøpsprisliste i Project Operations
description: Denne artikkelen inneholder informasjon som hjelper deg å opprette og vedlikeholde leverandørdata og kjøpsprislister for utsetting.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6840ffcbc510fe6385dd3fdaf881e9700c4fdd18
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914138"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>Administrasjon av leverandør- og innkjøpsprisliste i Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

## <a name="vendors-in-project-operations"></a>Leverandører i Project Operations

Leverandørkontoer har relasjonstypen **Leverandør** eller **Forsyner** i Microsoft Dynamics 365 Project Operations. Du kan bare velge en kontooppføring som har en av disse relasjonstypene som leverandør ved en underkontrakt.

Du kan knytte en eller flere innkjøpsprislister til en leverandøroppføring. Hver innkjøpsprisliste som er knyttet til en leverandøroppføring, må imidlertid ha distinkte gyldighetsdatoer. Project Operations støtter ikke overlappende gyldighetsdatoer for kjøpsprislister.

Som standard brukes følgende felter og konsepter for en leverandøroppføring for alle underkontrakter som opprettes for leverandøren:

- Betalingsbetingelser
- Faktura til kontakt
- Primær kontakt

    > [!NOTE]
    > Som standard brukes primærkontakten for leverandøren som leverandørkontoleder for underkontrakten.

- Valuta
- Gjeldende kjøpsprislister

## <a name="purchase-price-lists-in-project-operations"></a>Kjøpsprislister i Project Operations

En prisliste der **Kontekst**-feltet er satt til **Kjøp**, regnes som en innkjøpsprisliste. Kjøpsprislister kan defineres til å representere en katalog med kjøpspriser for tid, utgifter og materiell. Kjøpsprislister ligner på kostnader og salgsprislister i Project Operations. Følgende konsepter gjelder for kjøpsprislister på samme måte som de gjelder for kostnads- og salgsprislister:

- **Gyldighetsdato** – Kjøpsprislister har gyldighetsdato. Gyldighetsdato representeres av feltene startdato og sluttdato i hver prisliste. Perioden mellom startdato og sluttdato er gyldighetsdatoen.
- **Valuta** – Valutaen i prislistehodet brukes som valutaen som kjøpspriser uttrykkes i for arbeid, utgiftskategorier og produkter i katalogen.
- **Standard tidsenhet** – Standard tidsenhet uttrykker arbeidskraftpriser for innkjøp. Tidsenhetsfeltet i en prisliste brukes bare til å angi en standardverdi. Denne verdien kan endres for individuelle rolleprisrader.

Kjøpsprislister kan knyttes til leverandøroppføringer som tilknytninger som kalles prosjektprislister. Disse prislistene brukes til å angi standardpriser på underkontraktlinjer. Når flere kjøpsprislister er knyttet til en leverandøroppføring, brukes den mest aktuelle prislisten som standard for underkontrakter som opprettes for leverandøren. Bare prislister der **Kontekst**-feltet er satt til **Kjøp**, kan knyttes til leverandøroppføringer.

### <a name="subcontract-specific-purchase-price-lists"></a>Underkontraktspesifikke kjøpsprislister

Kjøpsprislister kan også knyttes til underkontrakter som tilknytninger som kalles prosjektprislister. Disse prislistene brukes til å angi standardpriser på underkontraktlinjer. Når flere kjøpsprislister er knyttet til en underkontrakt, må hver av dem ha distinkte gyldighetsdatoer. Project Operations støtter ikke kjøpsprislister som har overlappende gyldighetsdato. Bare prislister der **Kontekst**-feltet er satt til **Kjøp**, kan knyttes til underkontrakter.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
