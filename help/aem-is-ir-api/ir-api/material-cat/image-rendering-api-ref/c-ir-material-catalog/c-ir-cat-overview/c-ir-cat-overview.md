---
description: Materialkataloger innehåller information om vinjetter, material och stöddata, som ICC-profiler, till servern.
seo-description: Materialkataloger innehåller information om vinjetter, material och stöddata, som ICC-profiler, till servern.
seo-title: Översikt över materialkatalog *
solution: Experience Manager
title: Översikt över materialkatalog *
topic: Scene7 Image Serving - Image Rendering API
uuid: f2128b64-8caf-4a59-b11f-604fe62bae69
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---


# Översikt över materialkatalog *{#material-catalog-overview}

Materialkataloger innehåller information om vinjetter, material och stöddata, som ICC-profiler, till servern.

Varje materialkatalog består av en obligatorisk *katalogattributfil* och en uppsättning valfria *katalogdatafiler*:

* Vinjetteringsschemafilen, som specificerar vinjetter och mallar samt tillhörande metadata.
* Materialdatafilen som specificerar material och anger tillhörande texturbildfiler och metadata.
* Makrodefinitionsfilen som innehåller definitioner för begärandemakron.
* Profilmappningsfilen som specificerar ICC-färgprofiler.

Katalogdatafiler associeras med materialkataloger efter filreferenser i katalogattributfilen. Samma katalogdatafil kan delas av flera materialkataloger.

Katalogattributfiler måste ha filsuffixet [!DNL .ini] och måste finnas i mappen Image Rendering *katalog* ( [!DNL PlatformServer::ir.catalogRootPath]). Katalogdatafiler kan finnas i samma mapp eller i andra mappar som är tillgängliga för återgivningsservern.

**Uppdaterar materialkataloger**

Servern övervakar katalogmappen kontinuerligt och läser automatiskt in en materialkatalog igen, inklusive de associerade katalogdatafilerna, när den upptäcker att huvudkatalogattributfilen har ändrats. Om du vill uppdatera materialkataloger på servern ersätter du först alla katalogdatafiler som behöver ändras och ersätter sedan katalogattributfilen (eller &quot;touch&quot;) för att utlösa en omladdning av katalogen.

**Standardkatalog**

Standardkatalogen innehåller standardvärden för alla katalogattribut för alla materialkataloger. Om det inte går att hitta ett visst attribut i en viss materialkatalog använder servern i stället motsvarande värde från standardkatalogen. På samma sätt kan standardkatalogen användas för att tillhandahålla standardvärden för specifika katalogdataposter (material och ICC-profiler). Om en viss datapost inte kan hittas i en viss materialkatalog försöker servern hitta den i standardkatalogen i stället. På så sätt blir materialkataloger glesare ifyllda och det blir enklare att hantera globala attribut och data, som delade mallar, makron, teckensnitt osv.

Standardkatalogen innehåller dessutom alla attribut och dataposter (ICC-profiler) när ingen specifik materialkatalog är inblandad i en åtgärd.

För att återgivningsservern ska fungera på rätt sätt måste katalogattributfilen för standardkatalogen ha namnet [!DNL default.ini], måste alltid finnas i katalogmappen och måste vara fullt ifylld med alla nödvändiga attribut, förutom `attribute::RootId` och referenserna till de olika katalogdatafilerna, som alla är valfria.

**Se även**

`PlatformServer::ir.catalogRootPath`
