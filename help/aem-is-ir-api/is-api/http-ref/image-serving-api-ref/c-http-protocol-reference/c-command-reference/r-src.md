---
title: src
description: Lagerbild.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 88b89e70-59cf-4fb9-bbe7-0ac5eff792f1
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---

# src{#src}

Lagerbild.

` src= *`object`*|{[is|ir|fxg]'{' *`nestedRequest`*'}'}`

<table id="simpletable_59104309B8284B21ABCE7DC95BF5A273"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> object </span> </p> </td> 
  <td class="stentry"> <p>Bildobjekt. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> nestedRequest </span> </p> </td> 
  <td class="stentry"> <p>Kapslad bildhantering, bildåtergivning eller extern begäran. </p> </td> 
 </tr> 
</table>

## Beskrivning {#section-59ec6dc2afcb43efb34dbb0f7733543f}

Anger källbilden för ett bildlager.

*`object`* kan vara antingen en katalogpost eller en bild/SVG-fil.

Se [object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0).

Kapslade eller inbäddade begäranden omsluts av klammerparenteser. Förutse en inbäddad bildserverbegäran med `is`, en inbäddad begäran om bildåtergivning med `ir`och en begäran om en FXG-grafikåtergivning med `fxg`. En begäran till en extern server antas om inget prefix anges.

Se [Begär kapsling och inbäddning](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b).

## Egenskaper {#section-2c22bb89a35d470f833df8ba898efd93}

Lagerattribut. Gäller för `layer=0` if `layer=comp`. Ömsesidigt exklusiv med `text=` och `textPs=` i samma lager; den sista förekomsten av `text=`, `textPs=`, eller `src=` styr och avgör om det här är en bild eller ett textlager. Ignoreras av effektlager.

*`object`*kan inte matcha en annan katalogpost som innehåller en `src=` eller `mask=` kommando i sin `catalog::Modifier`. (Använd kapsling av begäranden för att uppnå en liknande effekt.)

The `is`, `ir`och `fxg` är skiftlägeskänsliga.

## Standard {#section-a92f3882041b4d43ae2caf014647165f}

För lager 0 används objektet från bankomponenten i URL:en om `src=` har inte angetts. Inget standardvärde för andra lager.

## Se även {#section-e467e03330564796932ac081f1c9c1d0}

[katalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f), [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [Mallar](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [Begär kapsling och inbäddning](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
