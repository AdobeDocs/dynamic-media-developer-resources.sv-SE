---
title: Översikt över materialkatalog
description: Materialkataloger innehåller information om vinjetter, material och stöddata, som ICC-profiler, till servern.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d26371da-e992-4f63-a5be-190ce60eca2f
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Översikt över materialkatalog{#material-catalog-overview}

Materialkataloger innehåller information om vinjetter, material och stöddata, som ICC-profiler, till servern.

Varje materialkatalog består av en obligatorisk *katalogattributfil* och en uppsättning valfria *katalogdatafiler*:

* Vinjetteringsschemafilen, som specificerar vinjetter och mallar samt tillhörande metadata.
* Materialdatafilen som specificerar material och anger tillhörande texturbildfiler och metadata.
* Makrodefinitionsfilen som innehåller definitioner för begärandemakron.
* Profilmappningsfilen som specificerar ICC-färgprofiler.

Katalogdatafiler associeras med materialkataloger efter filreferenser i katalogattributfilen. Samma katalogdatafil kan delas av flera materialkataloger.

Katalogattributfiler måste ha filsuffixet [!DNL `.ini`] och måste finnas i *katalogmappen* för bildåtergivning ( [!DNL PlatformServer::ir.catalogRootPath]). Katalogdatafiler kan finnas i samma mapp eller i andra mappar som är tillgängliga för återgivningsservern.

**Uppdaterar materialkataloger**

Servern övervakar katalogmappen kontinuerligt. En materialkatalog, inklusive tillhörande katalogdatafiler, läses automatiskt in igen när huvudkatalogattributfilen har ändrats. Om du vill uppdatera materialkataloger på servern ersätter du först alla katalogdatafiler som behöver ändras och ersätter sedan katalogattributfilen (eller &quot;touch&quot;) för att utlösa en omladdning av katalogen.

**Standardkatalog**

Standardkatalogen innehåller standardvärden för alla katalogattribut för alla materialkataloger. Om det inte går att hitta ett visst attribut i en viss materialkatalog använder servern i stället motsvarande värde från standardkatalogen. På samma sätt kan standardkatalogen användas för att tillhandahålla standardvärden för specifika katalogdataposter (material och ICC-profiler). Om en viss datapost inte kan hittas i en viss materialkatalog försöker servern att hitta den i standardkatalogen i stället. På så sätt blir materialkataloger glesare ifyllda och det blir enklare att hantera globala attribut och data, till exempel delade mallar, makron och teckensnitt.

Standardkatalogen innehåller dessutom alla attribut och dataposter (ICC-profiler) när ingen specifik materialkatalog är inblandad i en åtgärd.

För att återgivningsservern ska fungera korrekt måste katalogattributfilen för standardkatalogen ha namnet [!DNL default.ini]. Den måste också alltid finnas i katalogmappen och måste vara fullt ifylld med alla nödvändiga attribut, exklusive `attribute::RootId` och referenserna till de olika katalogdatafilerna, som alla är valfria.

<!-- **See also**

`PlatformServer::ir.catalogRootPath` -->
