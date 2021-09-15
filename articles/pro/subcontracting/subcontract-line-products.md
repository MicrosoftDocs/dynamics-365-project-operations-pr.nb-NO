---
title: Underkontraktlinjer for produkter
description: Dette emnet forklarer hvordan du registrerer underkontraktlinjer for produkter og bruker de forskjellige feltene til å registrere produktkjøp fra leverandører.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c0ddc39638ae9830eacc57f3e1def75aa36e6553
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323698"
---
# <a name="subcontract-lines-for-products"></a>Underkontraktlinjer for produkter

[!include [banner](../../includes/dataverse-preview.md)]

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

En underkontrakt i Dynamics 365 Project Operations kan ha en underleverandørlinje for produkter. Disse linjene gjør det mulig for en prosjektleder å kjøpe produkter fra leverandører som de deretter kan bruke på prosjektoppgaver.

Fullfør fremgangsmåten nedenfor for å opprette en underkontraktlinje for produkter i Project Operations.

1. Velg **Underkontrakter** på navigasjonssiden, og åpne underkontrakten du vil arbeide med. 
2. Velg **+ Ny** i fanen **Underkontraktlinjer** for å opprette en ny underkontraktlinje.
3. Velg **Materiale** i **Transaksjonsklasse**-feltet på **Hurtigoppretting**-siden, og angi eller velg den nødvendige feltinformasjonen. 
4. Velg **Lagre**.

Tabellen nedenfor inneholder informasjon om feltene på siden **Detaljer for underkontraktlinje** og **Hurtigoppretting** siden de er relevante for kjøp av produkter.

| Felt | Beskrivelse |
| ----- | ----------- |
| Navn | Navnet på underkontraktlinjen. |
| Beskrivelse | En kort beskrivelse av produkter som blir bestilt på underkontraktlinjen. |
| Linjetype | Denne feltverdien er som standard **antallsbasert**. |
| Faktureringsmetode |  Faktureringsmetoden for underkontraktlinjen. En milepælbasert fakturaplan er tilgjengelig for faktureringsmetoder med fast pris. |
| Transaksjonsklasse | Denne feltverdien er som standard **tid**. Hvis du vil opprette underkontraktlinjer for innkjøp av produkter, velger du **Materiale** i **Transaksjonsklasse**-feltet. Dette valget angir at underkontraktlinjen brukes til å registrere et kjøp av produkter som skal brukes på prosjekter. |
| Velg produkt | Velg om produktet som kjøpes, vedlikeholdes i produktkatalogen eller er et produkt som ikke er i produktkatalogen. |
| Produkt | Velg et aktivt produkt fra katalogen. Dette feltet er bare tilgjengelig når **Velg produkt** er satt til **Eksisterende**. |
| Ikke i produktkatalog | Angi navnet på produktet ikke i produktkatalogen. Dette feltet er bare tilgjengelig når **Velg produkt** er satt til **Ikke i produktkatalog**.  |
| Ønsket leveringsdato | Velg den nødvendige leveringsdatoen for produktene. Denne datoen brukes også til å velge en prosjektprisliste fra prosjektprislistene som er vedlagt underkontrakten. Kostnaden for produktet på underkontraktlinjen brukes deretter som standard fra den prislisten. |
| Avtalt leveringsdato | Velg datoen da det er avtalt at produktene skal leveres.  |
| Antall bestilt | Angi antall produkter som kjøpes fra leverandøren. Hvis en prosjektleder overtrekker fra dette antallet, vises det en advarsel. |
| Enhetsgruppe | Denne verdien brukes bare for katalogprodukter. Når både **Produkt** og **Ønsket leveringsdato** er valgt, velger systemet den aktuelle prislisten basert på leveringsdatoen. De relaterte prislisteelementene spørres om det samsvarende produktet. Verdiene for enhet og enhetsgruppe er standardverdier fra oppsettet i prislisteelementoppføringen. |
| Enhet | Denne verdien er standardverdi for enhetsoppsettet i prislisteelementoppføringen. Du kan endre dette til en annen enhet etter behov. Kombinasjonen av produkt og enhet brukes som standardverdi for enhetsprisen på underkontraktlinjen for eksisterende katalogprodukter. |
| Enhetspris | Enhetsprisen er standard ved å bruke kombinasjonen av produkt og enhet fra prislisteelementene knyttet til prosjektprislisten som gjelder for ønsket leveringsdato for underkontraktlinjen.  |
| Delsum | Dette skrivebeskyttede feltet beregnes som Antall x Enhetspris hvis begge feltene har angitt verdier. Hvis feltet **Antall**, **Enhetspris** eller begge er tomme, kan du angi en verdi manuelt.  |
| Merverdiavgift | Angi mva-verdien. |
| Totalbeløp | Dette beregnede feltet viser totalbeløpet for underkontraktlinjen etter inkluderte avgifter. Verdien i dette feltet beregnes som delsum + avgift. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
