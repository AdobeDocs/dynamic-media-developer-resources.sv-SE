---
description: Skalförändra bilden. Skalar en lagerkällbild utifrån faktor i förhållande till den högupplösta bilden.
seo-description: Skalförändra bilden. Skalar en lagerkällbild utifrån faktor i förhållande till den högupplösta bilden.
seo-title: scale
solution: Experience Manager
title: scale
uuid: f5540df8-60d9-4efc-99fe-733cdc8268ea
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---


# scale{#scale}

Skalförändra bilden. Skalar en lagerkällbild utifrån faktor i förhållande till den högupplösta bilden.

`scale= *`faktor`*`

<table id="simpletable_AC596A87494A4213A7D1C76612E8F2FD"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> faktor</span> </p> </td> 
  <td class="stentry"> <p>Skalfaktor (verklig, större än 0,0). </p></td> 
 </tr> 
</table>

Ingen skalförändring används när `scale=1`. *`factor`* är mindre än 1.0 nedskalas och större än 1.0 förstorar källbilden.

## Egenskaper {#section-3c7eb45527394fe79b1ddba6c1fcca09}

Källbild/maskattribut. Ignoreras om `size=` har angetts för det aktuella lagret. Åsidosätter `res=`. Gäller för lager 0 om det anges för `layer=comp`. Ignoreras om lagret inte är associerat med en bild eller mask.

## Standard {#section-26e64904362342a5a62c5f6598f330c4}

Om inget anges används `res=`. Om `res=` inte anges används bilden utan skalning.

## Se även {#section-61a11f30d37341d58c10df759bfff951}

[res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55) ,  [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
