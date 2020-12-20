---
description: Språk-ID för översättning. Anger språk-ID för begäran.
seo-description: Språk-ID för översättning. Anger språk-ID för begäran.
seo-title: locale
solution: Experience Manager
title: locale
topic: Scene7 Image Serving - Image Rendering API
uuid: 82acc0bb-fd94-44c9-8ff9-3b9cefab4627
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---


# locale{#locale}

Språk-ID för översättning. Anger språk-ID för begäran.

`locale=[ *`locId`*]`

<table id="simpletable_C1899AD02C984ED3896B7620916637E7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> locId</span></span> </p> </td> 
  <td class="stentry"> <p>Språk-ID (sträng). </p></td> 
 </tr> 
</table>

Med detta id och de regler som anges med `attribute::LocaleMap` och `attribute::LocaleStrMap`, används i Image Serving en valfri katalog-id-översättning och stränglokalisering.

## Egenskaper {#section-1854a9902b884d9b8e8e713b6635723f}

Begär kommando. Gäller hela begäran, inklusive kapslade/inbäddade begäranden, oavsett var de anges. `locId` får endast innehålla ASCII-tecken för utskrift. Ignoreras om inga lokaliseringskartor har definierats i huvudkatalogen för den här begäran. Ett fel returneras om en tom eller ogiltig `locId` har angetts och ingen standardregel har definierats i `attribute::DefaultLocale`.

## Standard {#section-9699fbc26de6453e9029e0003c79a7ef}

`attribute::DefaultLocale` används när locale= inte har angetts.

## Se även {#section-28a586d43ac4429d98e318a580c92af4}

[attribute::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b) ,  [attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318),  [attribute::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e), Localization Support
