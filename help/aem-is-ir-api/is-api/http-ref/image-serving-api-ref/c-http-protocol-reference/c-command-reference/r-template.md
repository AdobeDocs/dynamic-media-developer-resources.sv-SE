---
description: Sammansättningsmall. Gör att du kan ange en sammansättningsmall som finns i en annan katalog än huvudkatalogen.
solution: Experience Manager
title: mall
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 56ebf2a1-f2c3-4b3f-8d0a-9383f1411440
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---

# mall{#template}

Sammansättningsmall. Här kan du ange en sammansättningsmall i en annan katalog än huvudkatalogen.

`template= *`mall`*`

<table id="simpletable_DEC6F4EB460D453B8F272C98C9C8B7E5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> object</span> </p> </td> 
  <td class="stentry"> <p>Mall. </p></td> 
 </tr> 
</table>

*`template`* måste vara en bildkatalogspost med malltexten i `catalog::Modifier`.

När `template=` finns, det objekt som anges i begärandesökvägen används inte som källa för lager 0. Det kan dock kallas en `src=` eller `mask=` var som helst i mallen genom att använda den fördefinierade sökvägsvariabeln `$object$` som `src=` värde. `catalog::Modifier` för objektet som anges i begärandesökvägen tillämpas bara om `$object$` i mallen, när `catalog::PostModifier` används alltid.

Lager 0 definieras i mallbrödtexten och kan vara ett bild-, enfärgat, textbaserat eller kapslat eller inbäddat begärandolager.

`catalog:PostModifier` av *`object`* ignoreras när *`object`* används med `template=`.

## Standard {#section-9de53ea27c4b4fd4811e40e345d8ba05}

Ingen.

## Egenskaper {#section-daf3afb1d09c45a6a394468d0874c439}

Begär attribut. Används oavsett den aktuella lagerinställningen.

## Exempel {#section-9a4f260ed43342b186b0fe855f34bca6}

Se exemplen i [Mallar](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Se även {#section-067587444f774469931ecafd5a39834c}

[object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [Mallar](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [Fördefinierad banvariabel](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)
