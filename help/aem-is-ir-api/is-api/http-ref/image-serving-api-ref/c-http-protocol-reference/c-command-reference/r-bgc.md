---
title: bgc
description: Visa bakgrundsfärg. Anger bakgrundsfärgen för den sammansatta bilden (visningsbild).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39ca0d63-55c6-40be-88b6-cf73828cc355
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# bgc{#bgc}

Visa bakgrundsfärg. Anger bakgrundsfärgen för den sammansatta bilden (visningsbild).

`bgc= *`color`*`

<table id="simpletable_998CF426296945FEA48D19E33B71A17E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> color </span></span> </p> </td> 
  <td class="stentry"> <p>Grå, RGB eller CMYK-färgvärde. </p></td> 
 </tr> 
</table>

Anger en ogenomskinlig fyllningsfärg som ska användas för visningsbakgrunden. Visas bara om den sammansatta bilden har genomskinliga områden eller om den sammansatta bilden har ett annat proportioner än visningsrektangeln. Ignorerad om `fmt=tif-alpha`, `fmt=png-alpha` eller `req=mask`.

>[!NOTE]
>
>Färgsuffixet s ignoreras av `bgc=`. Färgvärden som anges med `bgc=` associeras alltid med respektive utdatafärgrymd.

## Egenskaper {#section-b729b50b1ea7433b82ba34ecd61839cd}

Visa attribut. Används oavsett den aktuella lagerinställningen. Ignoreras om `req=mask`, `fmt=tif-alpha`, `fmt=png-alpha`, `fmt=gif-alpha` eller `fmt=swf-alpha`.

Alla alfavärden som anges med färg ignoreras.

*`color`* antas tillhöra utdatafärgrymden (som anges med `icc=`) och ska ha samma pixeltyp som utdatabilden. Om pixeltyperna inte matchar konverteras *`color`* med naiv konvertering.

## Standard {#section-4e025cbd723547b5ab4450f7aad70da3}

`attribute::BkgColor`.

## Exempel {#section-7bcdfbc0e1274e86a69d39186b090789}

Ange en explicit bakgrundsfärg för en miniatyrbildsbegäran:

`http://server/myRootId/myImageId?req=tmb&bgc=214,245,130`

## Se även {#section-1e55f9f98f1847918a1725836a27cfaa}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93), [attribute::BkgColor](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-bkgcolor.md#reference-ed53106ee50442d7a2dd3e1f60e6f0f8), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a), [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [Color Management](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
