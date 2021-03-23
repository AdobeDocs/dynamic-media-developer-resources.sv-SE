---
description: Servern övervakar katalogmappen kontinuerligt och läser automatiskt in en bildkatalog igen, inklusive de associerade katalogdatafilerna, när den upptäcker att huvudkatalogattributfilen har ändrats.
seo-description: Servern övervakar katalogmappen kontinuerligt och läser automatiskt in en bildkatalog igen, inklusive de associerade katalogdatafilerna, när den upptäcker att huvudkatalogattributfilen har ändrats.
seo-title: Uppdaterar bildkataloger
solution: Experience Manager
title: Uppdaterar bildkataloger
uuid: 7e2557c4-1155-429b-a630-a2aff6725a3b
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---


# Uppdaterar bildkataloger{#updating-image-catalogs}

Servern övervakar katalogmappen kontinuerligt och läser automatiskt in en bildkatalog igen, inklusive de associerade katalogdatafilerna, när den upptäcker att huvudkatalogattributfilen har ändrats.

Om du vill uppdatera bildkataloger på servern ersätter du först alla katalogdatafiler som behöver ändras och ersätter (eller&quot;touch&quot;, för att uppdatera fildatumet) katalogattributfilen så att katalogen läses in igen.

## Inkrementella uppdateringar {#section-2c0f2c1b8480486d86920b5f2cfe72d2}

Inläsning och bearbetning av stora bildkataloger kan medföra en betydande belastning på servern och kan ha en negativ inverkan på serveråtgärder. För att minimera den här effekten bör du implementera en stegvis mekanism för kataloguppdatering, som fungerar så här:

En primär katalogfil som innehåller alla bilder läses in nattetid under låg trafiktid. Om det är nödvändigt att lägga till eller ändra poster i bildkatalogen skapas en annan bilddatafil som bara innehåller de nya eller ändrade posterna. Den här filen är registrerad som en sekundär bilddatafil i `attribute::CatalogFile`. Servern upptäcker att katalogattributfilen har ändrats och kontrollerar sedan vilka katalogdatafiler som har ändrats. Om huvudbilddatafilen inte har ändrats läser servern in eller läser bara in den inkrementella datafilen igen. Eftersom den här filen vanligtvis är mycket mindre än huvudkatalogfilen minskar effekten på servern avsevärt jämfört med att läsa in huvudkatalogen igen.

Inkrementella uppdateringar kan avsevärt minska påverkan på servern vid omfattande trafik. Vi rekommenderar att du regelbundet sammanfogar den inkrementella katalogdatafilen i huvudkatalogdatafilen under lågtrafiktimmar för att få optimala serverprestanda.
