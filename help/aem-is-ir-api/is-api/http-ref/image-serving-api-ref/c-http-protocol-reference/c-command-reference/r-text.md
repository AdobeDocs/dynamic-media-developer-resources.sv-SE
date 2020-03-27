---
description: Lagertext. Anger text och formatering för ett textlager.
seo-description: Lagertext. Anger text och formatering för ett textlager.
seo-title: text
solution: Experience Manager
title: text
topic: Scene7 Image Serving - Image Rendering API
uuid: 5b4f9282-83a3-488d-b5d2-deb2c92de564
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# text{#text}

Lagertext. Anger text och formatering för ett textlager.

` text= *`string`*`

<table id="simpletable_6C095D7F69874A8EA3D1D52103FA520C"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> string </span> </p> </td> 
  <td class="stentry"> <p>RTF-sträng eller oformaterad textsträng. </p> </td> 
 </tr> 
</table>

Alla inställningar för teckensnitt, teckenfärg och styckeformatering görs med RTF-kommandon. Mer information finns i [Textformatering](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) .

`text=` har stöd för automatisk skalning av texten för att fylla lagerektangeln som anges med `size=`.

Se [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d).

`text=` har stöd för automatisk storleksanpassning av textlagret så att det passar den återgivna texten (när `size=` inte har angetts eller när endast bredden har angetts). Observera att i detta fall endast ett av RTF-justeringskommandona `\ql`, `\qr`och `\qc` kan användas. annars returneras ett fel.

## Egenskaper {#section-8c0f020094a44c6b858454ef91ab4edf}

Lagerattribut. Gäller för `layer=0` if `layer=comp`. Ömsesidigt uteslutande med `src=` och `textPs=` i samma lager. den sista förekomsten av `text=`, `textPs=`och `src=` gäller och avgör om det är en bild eller ett textlager. Ignoreras av effektlager.

## Standard {#section-58958671e0ad479e8d5f6c1d41d7dc74}

Ingen.

## Exempel {#section-d011f765ec5c418d814a821019b0eef0}

Se exemplen i [Textformatering](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) och [Exempel A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) i [Mallar](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Se även {#section-207b779ab67342a5acd343e6bcc749c4}

[Textformatering](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c), [textplacering](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
