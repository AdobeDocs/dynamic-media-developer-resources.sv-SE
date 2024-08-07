---
title: locale
description: Översättningsspråk-ID. Anger språk-ID för begäran.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d937dfa5-95dd-49fd-ac23-e77e07b0642c
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---

# locale{#locale}

Översättningsspråk-ID. Anger språk-ID för begäran.

`locale=[ *`locId`*]`

<table id="simpletable_C1899AD02C984ED3896B7620916637E7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> locId </span></span> </p> </td> 
  <td class="stentry"> <p>Språk-ID (sträng). </p></td> 
 </tr> 
</table>

Med detta ID och de regler som anges med `attribute::LocaleMap` och `attribute::LocaleStrMap` använder Image Serving den valfria katalog-ID-översättningen och stränglokaliseringen.

## Egenskaper {#section-1854a9902b884d9b8e8e713b6635723f}

Begär kommando. Gäller hela begäran, inklusive kapslade/inbäddade begäranden, oavsett var de anges. `locId` får endast innehålla utskrivbara ASCII-tecken. Ignoreras om inga lokaliseringskartor har definierats i huvudkatalogen för den här begäran. Ett fel returneras om tom eller ogiltig `locId` har angetts och ingen standardregel har definierats i `attribute::DefaultLocale`.

## Standard {#section-9699fbc26de6453e9029e0003c79a7ef}

`attribute::DefaultLocale` används när locale= inte har angetts.

## Se även {#section-28a586d43ac4429d98e318a580c92af4}

[attribute::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b) , [attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [attribute::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e), Localization Support
