---
description: Lagertext (Adobe Photoshop-kompatibel). Anger textinnehållet för ett textlager.
seo-description: Lagertext (Adobe Photoshop-kompatibel). Anger textinnehållet för ett textlager.
seo-title: textPs
solution: Experience Manager
title: textPs
topic: Scene7 Image Serving - Image Rendering API
uuid: 45e587b6-8dc8-408c-ade6-d70025fd1117
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---


# textPs{#textps}

Lagertext (Adobe Photoshop-kompatibel). Anger textinnehållet för ett textlager.

`textPs= *`string`*`

<table id="simpletable_4E2D08FD4EEC4EDC9EFE9F6F2E22DB0C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> string</span> </span> </p> </td> 
  <td class="stentry"> <p>RTF-sträng (Rich-text-formatted). </p></td> 
 </tr> 
</table>

Alla inställningar för teckensnitt, teckenfärg och styckeformatering görs med RTF-kommandon.

Se [Textformatering](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c).

`textPs=` har stöd för utökade funktioner, t.ex. justering, textflöde i icke-rektangulära områden som definieras med  `textFlowPath=` och/eller  `textFlowXPath=`samt återgivning av text längs godtyckliga banor som definieras med  `textPath=`.

## Egenskaper {#section-a289dc26b6534b41998b1e241d5f2f92}

Lagerattribut. Gäller för `layer=0` om `layer=comp`. Mutuellt exklusiv med `src=` och `text=` i samma lager. Den sista förekomsten av `text=`, `textPs=` och `src=` gäller och avgör om det här är en bild eller ett textlager. Ignoreras av effektlager.

## Standard {#section-11c2ae2c96d64a0a9c207252df663e4d}

Ingen.

## Se även {#section-5c2b25767d2b47b5be817271ab12e13c}

[Textformatering](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c),  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d),  [text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef),  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowxpath.md#reference-c55d4e41a28f40aca6a24ca218c28542)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd)  [textFlowXPath=¥,¥textPath=¥,¥textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15)
