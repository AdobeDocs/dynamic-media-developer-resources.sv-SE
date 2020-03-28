---
description: JPEG-storlek i kB. Anger den maximala storleken för JPEG-svar i kilobyte.
seo-description: JPEG-storlek i kB. Anger den maximala storleken för JPEG-svar i kilobyte.
seo-title: jpegSize
solution: Experience Manager
title: jpegSize
topic: Scene7 Image Serving - Image Rendering API
uuid: 832163ca-0554-481d-b87f-bf322f415274
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# jpegSize{#jpegsize}

JPEG-storlek i kB. Anger den maximala storleken för JPEG-svar i kilobyte.

`jpegSize= *`size`*`

<table id="simpletable_EC2A8D8B65854B45B9CB184DA1069355"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> storlek</span></span> </p> </td> 
  <td class="stentry"> <p>Storlek i kilobyte. </p></td> 
 </tr> 
</table>

Om värdet är ett positivt värde, och om JPEG-svaret med den angivna JPEG-kvaliteten inte överstiger det här värdet, returneras bilden som svar. I annat fall försämras JPEG-kvaliteten tills den antingen skapar en bild som passar in i den angivna storleken eller tills den inte får plats. I det senare fallet misslyckas begäran med ett fel.

Värdet 0 innebär att svaret inte begränsas av storleken.

Negativa värden är inte tillåtna.

## Egenskaper {#section-19e544e77d35478b98fe8666f27d6968}

Begär attribut. Används oavsett aktuell lagerinställning. Ignoreras om utdatabildens format inte är JPEG.

## Standard {#section-198b798ed187453197e0969c641d6fb5}

0

## Exempel {#section-46bf806fd3ef4875b7726df32b6f834d}

Garantistorleken är inte för stor för att levereras till en enhet med begränsat minne:

`http://server/myRoodId/myImageId?qlt=60&wid=300&jpegSize=10`

## Se även {#section-98d472b39d6547969fce6dd86748c153}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [attribut::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
