---
title: Opprette avanserte kontrakter for fakturering basert på fremdrift
description: Dette emnet forklarer hvordan du oppretter prosjektkontrakter slik at du kan generere fakturaer for kunder basert på en prosentandel av fullført arbeid.
author: RadhikaRS
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 3b445488100e0a8335a05505405953b173ff836c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999683"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Opprette avanserte kontrakter for fakturering basert på fremdrift
[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du oppretter prosjektkontrakter slik at du kan opprette fakturaer for kunder basert på en prosentandel av fullført arbeid. Fakturabeløpene beregnes automatisk for budsjettkategoriene for arbeid som du har angitt for et prosjekt. Faktureringstiden angis når du forhandler prosjektkontrakten med kunden.

Bruk fremgangsmåtene i dette emnet til å sette opp en kontrakt, et tilknyttet prosjekt og faktureringsreglene som beregner fakturabeløpene for budsjettkategoriene for arbeid som du har angitt for prosjektet.

Når du har opprettet kontrakten og prosjektet, kan du sette opp detaljer for prosjektet. Du kan for eksempel definere aktiviteter og tilordne arbeidere til prosjektet.

## <a name="example"></a>Eksempel

Organisasjonen din er et selskap som utvikler programvare. Du går med på å utvikle en lønnsregnskapspakke for en kunde for en total pris på 200 000 kroner. Organisasjonen din godtar å fakturere kunden etter hvert som du fullfører bestemte prosentandeler av prosjektet. Du konfigurerer følgende prosjektkategorier for arbeidet slik at du kan bruke dem i faktureringsprosessen:

- Konsulentvirksomhet
- Utforming
- Installasjon

Du definerer også faktureringsregler som automatisk beregner fakturabeløpene for prosentandelen av prosjektarbeid som er fullført for hver kategori.

Budsjettsjefen oppretter et budsjett for prosjektkategoriene. Mengden fullført arbeid beregnes automatisk som en prosentandel av faktisk arbeid sammenlignet med de budsjetterte mengdene.

## <a name="prerequisites"></a>Forutsetninger

Før du oppretter et prosjekt som bruker faktureringsregler, må du angi nummersekvensene for faktureringsregler og en gebyrjournal som brukes til å postere fremdriftsfakturaer.

1. Gå til **Prosjektstyring og regnskap** \> **Oppsett** \> **Parametere for prosjektstyring og regnskap**.
2. På siden **Parametere for prosjektstyring og regnskap**, i kategorien **Nummersekvenser**, setter du opp nummersekvensen du vil bruke når faktureringsregler opprettes.
3. Gå til **Prosjektstyring og regnskap** \> **Journaler** \> **Gebyr**.
4. På siden **Gebyrjournal** velger du **Ny** og angir journalnavnet.

## <a name="create-a-contract-for-progress-billings"></a>Opprette en kontrakt for fremdriftsfaktureringer

Følg denne prosedyren for å opprette en prosjektkontrakt for et fastprisprosjekt. Du oppretter en prosjektfaktura når arbeidet som er fullført på prosjektet, når en bestemt prosentandel.

1. Gå til **Prosjektstyring og regnskap** \> **Prosjekter** \> **Prosjektkontrakter**.
2. På siden **Prosjektkontrakter** velger du **Ny**.
3. I dialogboksen **Ny prosjektkontrakt** angir du følgende felt:

    - **Navn**
    - **Finansieringstype**
    - **Finansieringskilde**
    - **Salgsvaluta** – som standard brukes denne valutaen til kundefakturaer som er knyttet til prosjektkontrakten. Du kan imidlertid endre salgsvalutaen for en bestemt kundefaktura.

4. Velg **OK**. Informasjonen kopieres til overskriften på **Prosjektkontrakter**-siden.
5. På **Prosjektkontrakter**-siden fyller du ut resten av den nødvendige informasjonen for prosjektet.

## <a name="create-a-project-for-progress-billings"></a>Opprette et prosjekt for fremdriftsfaktureringer

Følg fremgangsmåten nedenfor for å opprette et prosjekt og eventuelle delprosjekter som er tilknyttet en prosjektkontrakt.

1. Gå til **Prosjektstyring og regnskap** \> **Prosjekter** \> **Alle prosjekter**.
2. På siden **Alle prosjekter** velger du **Ny**.
3. I dialogboksen **Nytt prosjekt**, i **Prosjekttype**-feltet, velger du **Tid og materiale**.
4. Velg en prosjektgruppe. En prosjektgruppe definerer bokføringsinformasjonen for prosjektene som er tilordnet gruppen.
5. Velg **Opprett prosjekt**.
6. Etter at du har opprettet prosjektet, setter du prosjektstadiet til **Pågår**.

## <a name="create-a-budget-for-a-project"></a>Opprette et budsjett for et prosjekt

Budsjettkategorier brukes til å automatisk beregne fakturabeløpene for prosentandelen arbeid som er fullført for hver kategori. Følg fremgangsmåten nedenfor for å opprette budsjettkategorier for de estimerte kostnadene.

1. Gå til **Prosjektstyring og regnskap** \> **Prosjekter** \> **Alle prosjekter**.
2. På siden **Alle prosjekter** velger du og åpner det ønskede prosjektet.
3. På **Prosjekter**-siden, i handlingsruten, i **Planlegg**-kategorien, i **Budsjett**-gruppen velger du **Prosjektbudsjett**.
4. På **Prosjektbudsjett**-siden angir du en estimert kostnad for hver kategori i prosjektet.

## <a name="create-billing-rules-for-progress-billings"></a>Opprette faktureringsregler for fremdriftsfaktureringer

1. Gå til **Prosjektstyring og regnskap** \> **Prosjekter** \> **Prosjektkontrakter**.
2. Velg en prosjektkontrakt på siden **Prosjektkontrakter**, og åpne den.
3. På siden med prosjektkontrakter, på hurtigfanen **Faktureringsregler**, velger du **Legg til**.
4. På siden **Faktureringsregel**, i **Linjetype**-feltet, velger du **Fremdrift**.
5. På hurtigfanen **Linjedetaljer for faktureringsregel**, i **Kontraktverdi**-feltet, angir du totalverdien for kontrakten.
6. I **Kategori**-feltet velger du kategorien der gebyrtransaksjonen skal bokføres.
7. I **Prosjekt**-feltet velger du prosjektet som bruker denne faktureringsregelen.
8. Valgfritt: Tilordne faktureringsregelen til flere prosjekter. På hurtigfanen **Prosjekt**, i delen **Tilgjengelige prosjekter**, velger du et prosjekt, og deretter velger du pil høyre for å legge til prosjektet i delen **Valgte prosjekter**.
9. Valgfritt: Beregne prosentbeløpet som kunden tilbakeholder fra betalinger på en faktura. På hurtigfanen **Tilbakeholdelsesbetingelser for betaling** velger du finansieringskilden, og deretter angir du tilbakeholdelsesprosenten i feltet **Tilbakeholdelsesprosent**.
10. Gjenta disse trinnene for å opprette flere faktureringsregler for prosjektkontrakten.


[!INCLUDE[footer-include](../includes/footer-banner.md)]