---
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---
# Riktlinjer för att bidra till Adobe Dynamic Media dokumentation om utvecklingsresurser

## Dokumentationsfilosofi

Adobe vet att användare av Adobe Dynamic Media arbetar i mycket konkurrensutsatta miljöer och strävar efter att skapa digitala upplevelser som skiljer dem från deras konkurrenter. Därför är det viktigt att Adobe när de levererar avancerade nya verktyg kompletteras med korrekt och tydlig dokumentation som gör det möjligt för kunden att omedelbart utnyttja sin investering i Dynamic Media och maximera avkastningen på investeringen.

Syftet med dokumentationen är att användarna ska få tillgång till aktuell dokumentation så snart som möjligt. Därför prioriterar vi korrekt, användbar dokumentation och strävar efter att kontinuerligt uppdatera och förbättra den.

## Dokumentationsbidrag

I syfte att kontinuerligt förbättra dokumentationen är hela användargruppen välkommen att bidra till dokumentationen. Vare sig det gäller förfrågningar eller frågor kan förbättringar av dokumentationen vara korrigeringar, förtydliganden, tillägg och ytterligare exempel.

## Dokumentationsstandarder

Även om vi välkomnar bidrag till vår dokumentation bör alla bidrag till dokumentationen, antingen i form av en begäran om att tjänsten ska fyllas i eller i form av ett problem, överensstämma med våra standarder för bidrag och dokumentation.

Bidrag som inte uppfyller dessa standarder kan avvisas.

### Vi dokumenterar standardanvändningsexempel.

Dokumentationen innehåller standardanvändningsexempel. Användningsfall som inte omfattas av standardinstallation och standardanvändning av produkten ingår inte i dokumentationen.

### Vi dokumenterar vanligtvis inte buggar eller deras tillfälliga lösningar.

Dokumentationen innehåller standardanvändningsexempel. Av den anledningen dokumenteras inte buggar, effekter orsakade av buggar och tillfälliga lösningar för buggar.

Undantag från den här regeln gäller versionsinformationen där kända problem kan listas med möjliga lösningar som har godkänts av Product Management.

### Dokumentationsbidragen är inte till för att besvara tekniska frågor.

Alla idéer du kan behöva förbättra dokumentationen är välkomna som bidrag. Kommentarer, problem och förfrågningar är dock avsedda för *avgifter* endast. De är inte avsedda att användas för att besvara frågor om hur du använder Dynamic Media, implementerar projektet eller löser tekniska problem.

Om du har frågor om hur du använder Dynamic Media eller om tekniska fel ska du rapportera dem via [Experience Cloud Enterprise Support Portal](https://experienceleague.adobe.com/sv?support-solution=General&amp;support-tab=home#support) eller diskuteras i [Experience Manager community.](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-manager/ct-p/adobe-experience-manager-community)

***Dokumentationsavgifter ersätter inte Adobe kundtjänst*** och alla sådana bidrag som söker svar på frågor som rör stöd avvisas.

### Bidragen ska tydligt hänvisa till berörda dokumentationssidor.

Om du skapar ett problem som kan föreslå förbättringar av dokumentationen måste du inkludera länkar till de sidor som påverkas. Om du skapar ett problem med hjälp av **Redigera den här sidan** på en dokumentationssida skapas problemet automatiskt med en länk till sidan.

Den här processen gäller inte för pull-begäranden eftersom pull-begäranden till sin natur refererar till de berörda sidorna.

## Riktlinjer för dokumentation

Vi ber att eventuella bidrag till vår dokumentation följer vissa riktlinjer för format.

Genom att följa dessa riktlinjer blir det enklare att granska ditt bidrag och det går därför snabbare att integrera det i vår dokumentation.

### Språk och format

#### Språk

* Dokumentationen skrivs och underhålls på amerikansk engelska.
* Håll meningar så enkla som möjligt.
* Se till att språket är klart och koncist.

Kom ihåg att läsarna av dokumentationen är från hela världen och att de inte kan förväntas vara inbyggda eller flytande engelska. Undvik kollokvialism och håll språket så tydligt och enkelt som möjligt.

#### Följ Microsoft®-formathandboken

[The Microsoft® Manual of Style](https://learn.microsoft.com/en-us/style-guide/welcome/) är en kostnadsfri handbok för dokumentationsformat som fokuserar på programvarudokumentation och Dynamic Media-dokumentation följer den här handboken när det är möjligt.

### Formatering

| Objekt | Stil |
|---|---|
| Element eller alternativ i användargränssnittet | **fet** |
| Filnamn, sökväg, användarindata, parametervärden | `monospaced` |
| Kod, kommandorad | ```Code Block``` |

### Skärmbilder

Skärmbilder ska användas med omdöme och endast när en textbeskrivning är otillräcklig.

Markörer eller andra anteckningar i skärmbilder (som röda ramar, pilar eller text) ska inte användas. Orsaken är att skärmbilder är enklare att återanvända eller replikera i lokaliserade versioner av dokumentationen.

### Versionsspecifika referenser

Undvik om möjligt direkta referenser till en viss version i dokumentationsinnehållet. Detta gör dokumentationen mer flexibel och utbyggbar för framtida versioner.