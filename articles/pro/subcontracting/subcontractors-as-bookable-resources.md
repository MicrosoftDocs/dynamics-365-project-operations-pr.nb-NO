---
title: Konfigurer underleverandører som ressurser som kan reserveres
description: Dette emnet forklarer hvordan du konfigurerer og vedlikeholder underleverandørressurser som er opprettet fra brukere og kontakter i systemet, slik at de kan knyttes til underleverandører i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 07/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6d2f250063afc24de99e308d8d7583d1822bcabb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597258"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>Konfigurer underleverandører som ressurser som kan reserveres

[!include [banner](../../includes/dataverse-preview.md)]

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Følg denne fremgangsmåten for å konfigurere underleverandører som ressurser som kan reserveres i Microsoft Dynamics 365 Project Operations.

1. Gå til **Prosjekt** \> **Ressurser** og velg **Ny**.
2. Velg et av følgende alternativer i **Ressurstype**-feltet på siden **Ny ressurs som kan reserveres**:

    - **Bruker** – Velg denne ressurstypen hvis underleverandøren må ha tilgang til Project Operations for å angi tid eller utgifter. Hvis du velger **Bruker**, krever underleverandøren en gyldig lisens for å få tilgang til systemet.
    - **Kontakt** eller **Konto** – Velg en av disse ressurstypene hvis underleverandøren ikke krever tilgang til Project Operations, men må være tilgjengelig for oppgavetilordninger eller bestillinger på prosjekter. Ingen av disse ressurstypene gir tilgang til systemet. Velg **Konto** for å representere firmaet til leverandøren som en ressurs som kan reserveres. Velg **Kontakt** for å representere de individuelle ansatte for leverandøren.

3. Avhengig av ressurstypen du valgte, blir du bedt om å velge den tilsvarende bruker-,konto- eller kontaktoppføringen.
4. Velg Kontraktarbeider i **Arbeidertype**-feltet for å definere underleverandøren som en ressurs som kan reserveres.

    > [!NOTE]
    > Hvis du lar **Arbeidertype**-feltet stå tomt, blir ressursen som kan reserveres, betraktet som en ansatt.

5. Hvis du valgte **Kontraktarbeider** som type arbeider, velger du leverandøren som ressursen arbeider for.
6. Velg tidssonen for ressursen, og velg deretter **Lagre**. Hvis du vil tilordne en mal for arbeidstid til ressursen som kan reserveres, kan du velge **Angi kalender** på listesiden **Ressurs som kan reserveres**.

For å bli tilknyttet med en underkontraktlinje må en ressurs som kan reserveres, oppfylle disse betingelsene:

- Ressursen som kan reserveres, må være en kontraktarbeider.
- En ressurs som kan reserveres av ressurstypen **Kontakt**, må knyttes til leverandørkontoen som en kontakt. En ressurs som kan reserveres av ressurstypen **Bruker**, må ikke være knyttet til leverandørkontoen som en kontakt.
- Verdien i **Leverandør**-feltet for ressursen som kan reserveres, må samsvare med verdien i **Leverandør**-feltet for underkontrakten.

## <a name="update-the-type-of-worker-and-vendor-mapping-for-bookable-resources"></a>Oppdater tilordningstype for arbeidere og leverandører for ressurser som kan reserveres

**Arbeidertype**-feltet for en ressurs som kan reserveres, avgjør om ressursen som kan reserveres, er en kontraktarbeider eller en ansatt. **Leverandør**-feltet definerer leverandørkontoen som ressursen som kan reserveres. Ved å knytte en ressurs som kan reserves til en leverandør som en kontakt, angir du at kontakten er en ansatt i leverandørselskapet.

Hvis feltene **Arbeidertype** og **Leverandør** for en ressurs som kan reserveres, påvirker endringene eventuelle fremtidige valideringer av nye oppføringer som ressursen som kan reserveres, for eksempel tidsoppføringer. Endringene gjør imidlertid ikke eksisterende oppføringer ugyldige.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
