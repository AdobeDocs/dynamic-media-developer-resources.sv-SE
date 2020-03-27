---
description: Strängöversättningskarta. Avser ett locId som kan mappas till valfritt antal internalLocId.
seo-description: Strängöversättningskarta. Avser ett locId som kan mappas till valfritt antal internalLocId.
seo-title: LocaleStrMap
solution: Experience Manager
title: LocaleStrMap
topic: Scene7 Image Serving - Image Rendering API
uuid: 44207916-80a6-42cb-8bf1-fcf0f5194c6d
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# LocaleStrMap{#localestrmap}

Strängöversättningskarta. Avser ett locId som kan mappas till valfritt antal internalLocId.

` *``*&#42;['|' *`itemItem`*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> artikel </span> </p> </td> 
  <td class="stentry"> <p> <span class="varname"> locale </span>, <span class="varname"> locId </span>*[',' <span class="varname"> locId </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locale </span> </p> </td> 
  <td class="stentry"> <p>Språk (ej skiftlägeskänsligt). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId </span> </p> </td> 
  <td class="stentry"> <p>Internt språk-ID. </p> </td> 
 </tr> 
</table>

`LocaleStrMap` refererar till en `locId` som kan mappas till valfritt antal `internalLocId`.

Ett tomt *`locale`* värde matchar tomma och okända `locale=` strängar. Detta gör att du kan definiera en standardregel för okända språk.

Tomma *`locId`* värden tillåts och markerar *`defaultString`* ( *`defaultString`* det finns ingen språkområdesidentifierare). *`locId`* värden söks igenom i den angivna ordningen. Den första matchningen returneras.

Strängöversättning, när den är aktiverad, används för textsträngar i följande bildkatalogsfält:

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>Katalogfält</b> </td> 
   <td> <b>Strängelement i fält</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> katalog::ImageSet </span> </p> </td> 
   <td> <p>Alla underelement som innehåller en översättningsbar sträng (avgränsas av en kombination av avgränsare ',' ';' ':' och/eller fältets start/slut). </p> <p>Ett <span class="codeph"> 0xrrggbb- </span> färgvärde i början av ett lokaliserbart fält undantas från lokalisering och skickas vidare utan ändring. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> katalog::Map </span> </p> </td> 
   <td> <p>Ett attribut med enkla eller dubbla citattecken, förutom värdena för attributen <span class="codeph"> coords= </span> och <span class="codeph"> shape= </span> . </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> katalog::mål </span> </p> </td> 
   <td> <p>Värdet för alla <span class="filepath"> mål.*.label </span> och <span class="filepath"> target.*.userdata, </span> egenskap. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> katalog::UserData </span> </p> </td> 
   <td> <p>Värdet för en egenskap. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-8505a8525f6948ada3979f68c4081044}

Ett eller flera objekt, avgränsade med|, där varje objekt består av två eller flera kommaavgränsade strängvärden.

## Se även {#section-0c0516e4f83d42d38247308cab9b6708}

Lokaliseringsstöd, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribut::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [katalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [katalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [katalog::Target](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md)[,¥catalog::UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
