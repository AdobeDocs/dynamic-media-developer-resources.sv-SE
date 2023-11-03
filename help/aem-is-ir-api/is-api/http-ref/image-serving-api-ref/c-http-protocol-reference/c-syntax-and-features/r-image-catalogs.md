---
description: Funktionerna och syntaxen för bildkataloger beskrivs i det här avsnittet.
solution: Experience Manager
title: Bildkataloger
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c83ad2-a932-4df2-92ff-ab34d4a5b1a7
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%

---

# Bildkataloger{#image-catalogs}

Funktionerna och syntaxen för bildkataloger beskrivs i det här avsnittet.

Bildkataloger har följande funktioner:

* Tillåt beständig koppling av bilder med vissa metadata- och modifieringskommandon.

  Poster i bildkataloger refereras med en genvägsnotation `*`rootId/objId`*`, där `*`rootId`*` identifierar bildkatalogen och `*`objId`*` identifierar en datapost i katalogen.
* Ange standardvärden för vissa attribut, t.ex. JPEG-kvalitet eller om en vattenstämpel ska användas.
* Hantera teckensnitt, ICC-profiler, makrodefinitioner och frågemallar

Även om inga specifika bildkataloger är definierade är alla funktioner i bildkataloger tillgängliga som standardkatalog ( [!DNL default.ini]).

If `*`rootId`*` i begärans URL-sökväg matchar `attribute::RootId` för en viss bildkatalog blir den katalogen huvudkatalog för denna begäran. Huvudkatalogen innehåller standardattribut och standardinställningar för hela begäran. Om ingen matchning hittas används standardkatalogen i stället.

En katalog som identifieras i en `src=` eller `mask=` -kommandot innehåller följande katalogattribut och data till det aktuella lagret:

<table id="table_D3FA66EA5D054745900DE5A120885AA8"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Attribut/data</b> </th> 
   <th class="entry"> <b> Anteckningar</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::DefaultExt</span> </p> </td> 
   <td> <p> standardtillägget för alla bildfilsbanor i aktuellt lager </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Expiration</span> </p> </td> 
   <td> <p> standard för <span class="codeph"> katalog::Förfallotid</span> eller utgångsdatum för aktuellt lager om ingen katalogpost är inblandad </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Icc*</span> </p> </td> 
   <td> <p> den aktuella ICC-färgprofilen, återgivningsmetoden och svartpunktskompensationsflaggan för begäran och/eller det aktuella lagret </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootPath</span> </p> </td> 
   <td> <p> används för alla källfilssökvägar i det aktuella lagret </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Resolution</span> </p> </td> 
   <td> <p> standard för <span class="codeph"> katalog::Upplösning</span> endast </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> katalog::Ankarpunkt</span> </p> </td> 
   <td> <p> standard för <span class="codeph"> anchor=</span> det aktuella lagrets värde </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> katalog::Förfallotid</span> </p> </td> 
   <td> <p> det minsta utgångsvärdet för alla lager används som svarsbildens time-to-live-värde </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> katalog::IccProfile</span> </p> </td> 
   <td> <p> källbildens färgprofil för aktuellt lager </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> katalog::Map</span> </p> </td> 
   <td> <p> bildmappningsdata för det aktuella lagret </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> katalog::MaskPath</span> </p> </td> 
   <td> <p> standard för <span class="codeph"> mask=</span> för aktuellt lager </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> katalog::Modifier</span> </p> </td> 
   <td> <p> prefixkommandon för det aktuella lagret (varje kommando i <span class="codeph"> katalog::Modifier</span> kan åsidosättas av samma kommando i URL:en, om det anges för samma lager) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> katalog::Path</span> </p> </td> 
   <td> <p> källbildfilen för aktuellt lager </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> katalog::PostModifier</span> </p> </td> 
   <td> <p> postfix-kommandon för det aktuella lagret (liknar <span class="codeph"> katalog::Modifier</span>, men kommandon i <span class="codeph"> katalog::PostModifier</span> åsidosätta samma kommandon som anges i URL:en eller i <span class="codeph"> katalog::Modifier</span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> katalog::Upplösning</span> </p> </td> 
   <td> <p> objektupplösningen för det aktuella lagret </p> </td> 
  </tr> 
 </tbody> 
</table>

Inom samma lager `src=` och `mask=` måste referera till samma bildkatalog (om sådan finns).

En katalog som identifieras i en `icc=` -kommandot används bara för att söka efter en post från katalogens ICC-profiltabell. Inga andra katalogattribut eller data berörs.

If, `*`rootId`*` matchar en katalog, och `*`objId`*` matchas med `catalog::Id` i den här katalogen `*`rootId/objId`*` ersätts med katalogposten ungefär så här:

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## Se även {#section-00e4f6b39cd14244bcce537a3f831259}

[Referens för bildkatalog](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
