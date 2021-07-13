---
description: Servern övervakar katalogmappen kontinuerligt och läser automatiskt in en bildkatalog igen, inklusive de associerade katalogdatafilerna, när den upptäcker att huvudkatalogattributfilen har ändrats.
solution: Experience Manager
title: Uppdaterar bildkataloger
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b520b4f3-6717-4768-99e2-78a76d1ede24
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 0%

---

# Uppdaterar bildkataloger{#updating-image-catalogs}

Servern övervakar katalogmappen kontinuerligt och läser automatiskt in en bildkatalog igen, inklusive de associerade katalogdatafilerna, när den upptäcker att huvudkatalogattributfilen har ändrats.

Om du vill uppdatera bildkataloger på servern ersätter du först alla katalogdatafiler som behöver ändras och ersätter (eller&quot;touch&quot;, för att uppdatera fildatumet) katalogattributfilen så att katalogen läses in igen.

## Inkrementella uppdateringar {#section-2c0f2c1b8480486d86920b5f2cfe72d2}

Inläsning och bearbetning av stora bildkataloger kan medföra en betydande belastning på servern och kan ha en negativ inverkan på serveråtgärder. För att minimera den här effekten bör du implementera en stegvis mekanism för kataloguppdatering, som fungerar så här:

En primär katalogfil som innehåller alla bilder läses in nattetid under låg trafiktid. Om det är nödvändigt att lägga till eller ändra poster i bildkatalogen skapas en annan bilddatafil som bara innehåller de nya eller ändrade posterna. Den här filen är registrerad som en sekundär bilddatafil i `attribute::CatalogFile`. Servern upptäcker att katalogattributfilen har ändrats och kontrollerar sedan vilka katalogdatafiler som har ändrats. Om huvudbilddatafilen inte har ändrats läser servern in eller läser bara in den inkrementella datafilen igen. Eftersom den här filen vanligtvis är mycket mindre än huvudkatalogfilen minskar effekten på servern avsevärt jämfört med att läsa in huvudkatalogen igen.

Inkrementella uppdateringar kan avsevärt minska påverkan på servern vid omfattande trafik. Vi rekommenderar att du regelbundet sammanfogar den inkrementella katalogdatafilen i huvudkatalogdatafilen under lågtrafiktimmar för att få optimala serverprestanda.
