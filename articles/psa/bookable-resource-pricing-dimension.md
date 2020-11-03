---
title: Bruke bestillbar ressurs som en prisingsdimensjon
description: Dette emnet gir informasjon om hvordan du bruker en bestillbar ressurs som en prisingsdimensjon.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8a5c643745d8e10887965228da7abd8f56228006
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081719"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a>Bruke bestillbar ressurs som en prisingsdimensjon
Dette emnet gir informasjon om hvordan du bruker en bestillbar ressurs som en prisingsdimensjon. Hvis du ikke allerede har opprettet en løsning for prisdimensjon før du begynner, må du opprette en ny. Hvis du allerede har en løsning for prisingsdimensjon, kan du gjøre endringene i den løsningen. Hvis du ikke har opprettet en ny løsning for prisdimensjon for organisasjonen, må du fullføre prosedyrene i emnet [Opprette egendefinerte felt og enheter](create-custom-fields-entities.md).

## <a name="add-bookable-resource-to-forms-and-views"></a>Legge til bestillbar ressurs i skjemaer og visninger
Hvis du vil gjøre feltene synlige i brukergrensesnittet i løsningen for prisingsdimensjonen, må du gå gjennom alle skjemaer og visninger for de viktigste Project Service-enhetene og legge til disse feltene i skjemaene og visningene for disse enhetene.
Tabellen nedenfor er en omfattende liste over de medfølgende skjemaene og visningene som er oppført etter entitet, som må oppdateres. Hvis det finnes andre visninger eller skjemaer i tilpassingen på disse enhetene, legger du til de nye feltene også.
Åpne løsningsutforskeren for prisingsdimensjonsløsningen, og klikk deretter **Publiser alle tilpassinger**.


|   Enhet        | Skjemaer   |Visninger        |
| ------------------------------|---------------------------------|----------------------------------|
|  Rollepris|• Informasjon |• Aktive ressurskategoripriser<br> • Tilknyttet visning for ressurskategoripriser|
|  Rolleprispåslag|• Informasjon|• Aktive rolleprispåslag<br>• Tilknyttet visning for rolleprispåslag|
|  Tilbudslinjedetalj|• Prosjektinformasjon<br>• Hurtigoppretting av prosjekter|• Aktiv tilbudslinjedetalj<br>• Kombinerte tilbudslinjedetaljer<br>• Tilknyttet visning for tilbudslinjedetaljer|
|  Detalj for prosjektkontraktlinjer|• Prosjektinformasjon<br>• Hurtigoppretting av prosjekter|• Kombinerte kontraktlinjedetaljer<br>• Aktive kontraktlinjedetaljer<br>• Tilknyttet visning for kontraktlinjedetaljer|
|  Prosjektoppgave|• Informasjon<br>• Nytt skjema||
|  Prosjektteammedlem|• Informasjon<br>• Nytt skjema|• Aktive prosjektteammedlemmer<br>• Prosjektteammedlemmer<br>• Tilknyttet visning for prosjektteammedlemmer|
|  Tidsoppføring|• Informasjon<br>• Opprett tidsoppføring|• Mine tidsoppføringer etter dato<br>• Mine tidsoppføringer for denne uken<br>• Tidsoppføringer for godkjenning|
|  Journallinje|• Informasjon<br>• Hurtigoppretting|• Aktive journallinjer<br>• Tilknyttet visning for journallinjer|
|  Fakturalinjedetalj|• Informasjon<br>• Hurtigoppretting|• Aktive fakturalinjedetaljer<br>• Belastbare fakturatransaksjoner<br>• Gratis fakturatransaksjoner<br>• Tilknyttet visning for fakturalinjedetaljer<br>• Ikke-belastbare fakturatransaksjoner|
|  Faktisk|• Informasjon<br>• Aktive faktiske data|• Tilknyttet visning for faktiske data|

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a>Konfigurere bestillbar ressurs som en prisingsdimensjon

1. I webgrensesnittet går du til **Project Service** > **Innstillinger** > **Parametere**. På **Parameter** -siden i kategorien **Beløpsbaserte prisdimensjoner** kan du legge merke til at rutenettet i kategorien viser oppføringene i prisingsdimensjonsenheten. 
2. Legg den **bestillbare ressursen** i denne listen over prisdimensjoner som **msdyn_bookableresource**. 
3. Angi konteksten der den bestillbare ressursen fungerer som en prisingsdimensjon, og angi verdiene for **Gjelder kostnad** og **Gjelder salg**.
4. I **Dimensjonstype** -feltet velger du **Beløpsbasert**. 
5. Velg kostnads- og salgsprioriteten for den bestillbare ressursen. Når den tas med som en prisingsdimensjon, har en bestillbar ressurs vanligvis høyeste prioritet, slik at verdien **1** eller **0** , avhengig av hvordan du teller prioriteten, sørger for denne virkemåten.

## <a name="set-up-pricing-dimension-field-names"></a>Angi feltnavn for prisdimensjon

Når feltnavnet for en prisingsdimensjon i tabellen **Rollepris** er forskjellig fra feltnavnet i noen av de andre enhetene der prisstandarden må fungere, må prismodelloppføringen være klar over de forskjellige navnene.    
For den bestillbare ressursen har enheten **Prosjektteammedlemmer** et litt annet feltnavn ( **msdyn_bookableresourceid** ) enn for **Rollepris** -enheten ( **msdyn_bookableresource** ). Prisdimensjonsoppføringen for **msydn_bookableresource** må gjøres oppmerksom på dette. 
1. Dette gjør du ved å dobbeltklikke raden i rutenettet **Prisingsdimensjon** for å åpne siden **msdyn_bookableresource**.
2. På dimensjonssiden, i kategorien **Relatert** , klikker du **Feltnavn for prisdimensjon**.

 ![Kategorien Feltnavn for prisdimensjon](media/PD-fieldname.png)

4. I den tilknyttede visningen som åpnes, klikker du **Legg til nytt feltnavn for prisdimensjon**.

 ![Legge til nye feltnavn for prisdimensjon](media/Add-NewPD-fieldname.png)


Dette åpner siden **Nytt feltnavn for prisdimensjon** for **msdyn_bookableresource**. 

5. Legg til **msdyn_projectteam** i feltet **Logisk navn for enhet** og **msdyn_bookableresourceid** i feltet **Feltnavn**. Lagre oppføringen.

 ![Skjema for nytt feltnavn for prisdimensjon](media/PD-fieldname-Added.png)