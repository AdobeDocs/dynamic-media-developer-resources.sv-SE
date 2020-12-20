---
description: Funktionerna och syntaxen för bildkataloger beskrivs i det här avsnittet.
seo-description: Funktionerna och syntaxen för bildkataloger beskrivs i det här avsnittet.
seo-title: Bildkataloger
solution: Experience Manager
title: Bildkataloger
topic: Scene7 Image Serving - Image Rendering API
uuid: d329807a-22b0-42a3-9297-8dad7a1dce43
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---


# Bildkataloger{#image-catalogs}

Funktionerna och syntaxen för bildkataloger beskrivs i det här avsnittet.

Bildkataloger har följande funktioner:

* Tillåt beständig koppling av bilder med vissa metadata- och modifieringskommandon.

   Poster i bildkataloger refereras med en genvägsnotation ` *`rootId/objId`*`, där ` *`rootId`*` identifierar bildkatalogen och ` *`objId`*` identifierar en datapost i katalogen.
* Ange standardvärden för vissa begärandeattribut, t.ex. JPEG-kvalitet eller om en vattenstämpel ska användas.
* Hantera teckensnitt, ICC-profiler, makrodefinitioner och frågemallar

Även om inga specifika bildkataloger är definierade är alla funktioner i bildkataloger tillgängliga via standardkatalogen ( [!DNL default.ini]).

Om ` *`rootId`*` i URL-sökvägen för begäran matchar `attribute::RootId` för en viss bildkatalog, kommer den katalogen att bli huvudkatalog för denna begäran. Huvudkatalogen innehåller standardattribut och standardinställningar för hela begäran. Om ingen matchning hittas används standardkatalogen i stället.

En katalog som identifieras i ett `src=`- eller `mask=`-kommando ger följande katalogattribut och data till det aktuella lagret:

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
   <td> <p> standardtillägget för alla bildfilsbanor i det aktuella lagret </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Expiration</span> </p> </td> 
   <td> <p> standard för <span class="codeph">-katalog::Förfallotid</span> eller utgångsdatum för det aktuella lagret om ingen katalogpost är inblandad </p> </td> 
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
   <td> <p> standard för <span class="codeph">-katalog::Upplösning</span> endast </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> katalog::Ankarpunkt</span> </p> </td> 
   <td> <p> standard för det aktuella lagrets <span class="codeph">-ankarpunktsvärde=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> katalog::Förfallotid</span> </p> </td> 
   <td> <p> det minsta utgångsvärdet för alla lager används som svarsbildens time-to-live-värde </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> katalog::IccProfile</span> </p> </td> 
   <td> <p> källbildens färgprofil för det aktuella lagret </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> katalog::Map</span> </p> </td> 
   <td> <p> bildmappningsdata för det aktuella lagret </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> katalog::MaskPath</span> </p> </td> 
   <td> <p> standard för <span class="codeph"> mask=</span> för det aktuella lagret </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> katalog::Modifier</span> </p> </td> 
   <td> <p> prefixkommandon för det aktuella lagret (varje kommando i <span class="codeph">-katalogen::Modifier</span> kan åsidosättas av samma kommando i URL:en, om det anges för samma lager) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> katalog::Path</span> </p> </td> 
   <td> <p> källbildfilen för det aktuella lagret </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> katalog::PostModifier</span> </p> </td> 
   <td> <p> postfix-kommandon för det aktuella lagret (liknar <span class="codeph">-katalog::Modifier</span>, men kommandon i <span class="codeph">-katalog::PostModifier</span> åsidosätter samma kommandon som anges i URL:en eller i <span class="codeph">-katalog::Modifier</span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> katalog::Upplösning</span> </p> </td> 
   <td> <p> objektupplösningen för det aktuella lagret </p> </td> 
  </tr> 
 </tbody> 
</table>

I samma lager måste `src=` och `mask=` referera till samma bildkatalog (om någon).

En katalog som identifieras i ett `icc=`-kommando används bara för att leta upp en post från katalogens ICC-profiltabell. Inga andra katalogattribut eller data berörs.

Om ` *`rootId`*` matchar en katalog och ` *`objId`*` matchas med `catalog::Id` i den här katalogen ersätts ` *`rootId/objId`*` av katalogposten på något av följande sätt:

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## Se även {#section-00e4f6b39cd14244bcce537a3f831259}

[Referens](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) för bildkatalog,  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
