---
title: Mobilt arbeidsområde for tidsoppføring for prosjekt
description: Dette emnet gir informasjon om det mobile arbeidsområdet for tidsoppføring for prosjekt. Dette arbeidsområdet gjør det mulig for brukere å skrive inn og spare tid på et prosjekt ved hjelp av den mobile enheten.
author: Yowelle
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 64a80d931332a4d6edfcd175d7168a7815ddca38
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683964"
---
# <a name="project-time-entry-mobile-workspace"></a>Mobilt arbeidsområde for tidsoppføring for prosjekt

[!include [banner](../includes/banner.md)]

Dette emnet gir informasjon om det mobile arbeidsområdet for **Tidsoppføring for prosjekt**. Dette arbeidsområdet gjør det mulig for brukere å skrive inn og spare tid på et prosjekt ved hjelp av den mobile enheten.

Dette mobile arbeidsområdet er ment å skulle brukes med en Dynamics 365 Unified OPS-mobilapp. 

## <a name="overview"></a>Oversikt
Som en del av det daglige arbeidet er prosjektressurser ofte på stedet eller på reise. Med det mobile arbeidsområdet **Tidsoppføring for prosjekt** kan brukere angi fakturerbar eller ikke-fakturerbar tid mot et prosjekt på den mobile enheten de velger. Derfor kan prosjektressurser registrere tidsoppføringer når som helst og hvor som helst. De kan også vise tidsoppføringer som allerede er registrert. 

I det mobile arbeidsområdet **Tidsoppføring for prosjekt** kan brukere utføre disse oppgavene:

-   For en valgt dato angir du hvor mange timer du har brukt på en bestemt oppgave.
-   Søk etter prosjektnavn eller kunde for å finne prosjektet du vil registrere tid for.
-   Angi kategorien og aktiviteten for tiden du brukte.
-   Registrere tiden som fakturerbar eller ikke-fakturerbar for prosjektet.
-   Angi eventuelt eksterne eller interne kommentarer.

## <a name="prerequisites"></a>Forutsetninger
Forhåndskravene varierer basert på versjonen av Microsoft Dynamics 365 som er distribuert for organisasjonen.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Forutsetninger hvis du bruker Dynamics 365 Finance
Hvis Finance er distribuert for organisasjonen, må systemetadministrator publisere det mobile arbeidsområdet **Tidsoppføring for prosjekt**. Hvis du vil ha instruksjoner, kan du se [Publisere et mobilt arbeidsområde](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Forhåndskrav hvis du bruker versjon 1611 med plattformoppdatering 3 eller senere
Hvis versjon 1611 med plattformoppdatering 3 eller senere er distribuert for organisasjonen, må følgende forhåndskrav fullføres av systemadministrator. 

<table>
<thead>
<tr class="header">
<th>Forutsetning</th>
<th>Rolle</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>Implementer KB 4018050.</td>
<td>Systemadministrator</td>
<td>KB 4018050 er en X++-oppdatering eller hurtigreparasjon for metadata som inneholder det mobile arbeidsområdet <strong>Tidsoppføring for prosjekt</strong>. For å implementere KB 4018050 må systemadministrator følge fremgangsmåten nedenfor.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Last ned hurtigreparasjonen for metadata fra Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installer hurtigreparasjon for metadata</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Opprett en distribuerbar pakke</a> som inneholder <strong>ApplicationSuite</strong> - og <strong>ProjectMobile</strong> -modellene, og last deretter opp den distribuerbare pakken til LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Ta i bruk den distribuerbare pakken</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Publiser arbeidsområdet for <strong>Tidsoppføring for prosjekt</strong>.</td>
<td>Systemadministrator</td>
<td>Se <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publisere et mobilt arbeidsområde</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Laste ned og installere mobilappen

Last ned og installere Finance and Operations-mobilappen:

-   [For Android-telefoner](https://go.microsoft.com/fwlink/?linkid=850662)
-   [For iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Logge på mobilappen
1.  Start appen på mobilenheten.
2.  Angi Dynamics 365-URL-en din.
3.  Første gang du logger deg på, blir du bedt om å oppgi brukernavn og passord. Angi legitimasjonen din.
4.  Etter at du har logget på, vises de tilgjengelige arbeidsområdene for firmaet. Vær oppmerksom på at hvis systemetadministrator publiserer et nytt arbeidsområde senere, må du oppdatere listen over mobile arbeidsområder.

[![Dra for å oppdatere.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Registrer tid ved hjelp av det mobile arbeidsområdet Tidsoppføring for prosjekt
1.  På den mobile enheten velger du arbeidsområdet **Tidsoppføring for prosjekt**.
2.  Velg **Tidsoppføring**. Kalenderdatoene for inneværende uke vises.
3.  For en valgt dato velger du **Handlinger** &gt; **Ny oppføring**.
4.  Angi antall timer du vil registrere.
5.  Velg prosjektet for tidsoppføringen. En liste viser prosjektene som lastes inn i appen for bruk i frakoblet modus. Som standard lastes 50 elementer inn, men en utvikler kan endre dette antallet. Hvis du vil ha mer informasjon, kan du se [Mobile-plattform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page)
6.  Hvis prosjektet ikke finnes i listen, velger du **Søk**. Søk etter navn, eller bytt for å søke etter prosjektnavn eller kunde.
7.  Velg en kategori. En liste viser kategorier som lastes inn i appen for bruk i frakoblet modus. Som standard lastes 50 elementer inn, men en utvikler kan endre dette antallet. Hvis du vil ha mer informasjon, kan du se [Mobile-plattform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page)
8.  Hvis kategorien din ikke finnes i listen, velger du **Søk**. Søk etter kategori, eller bytt for å søke etter kategorinavn.
9.  Velg en aktivitet. En liste viser aktiviteter som lastes inn i appen for bruk i frakoblet modus. Som standard lastes 50 elementer inn, men en utvikler kan endre dette antallet. Hvis du vil ha mer informasjon, kan du se [Mobile-plattform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page)
10. Hvis aktiviteten din ikke finnes i listen, velger du **Søk**. Søk etter aktivitetsnummer, eller bytt for å søke etter formål.

11. Velg linjeegenskapen.
12. Valgfritt: Angi eventuelt eksterne og interne kommentarer.
13. Velg **Ferdig**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]