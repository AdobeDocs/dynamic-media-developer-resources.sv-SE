---
description: Bildankarpunkt. Definierar fästpunkten för rektangeln för bilden, den heltäckande färgen eller textrutan innan du använder omformningar (crop=, scale=, rotate=, flip=). Fungerar även som centrum för rotation för rotate=.
seo-description: Bildankarpunkt. Definierar fästpunkten för rektangeln för bilden, den heltäckande färgen eller textrutan innan du använder omformningar (crop=, scale=, rotate=, flip=). Fungerar även som centrum för rotation för rotate=.
seo-title: ankare
solution: Experience Manager
title: ankare
topic: Scene7 Image Serving - Image Rendering API
uuid: 3b174360-9bb7-4dc8-83be-6b8c4ea88cd4
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# ankare{#anchor}

Bildankarpunkt. Definierar fästpunkten för rektangeln för bilden, den heltäckande färgen eller textrutan innan du använder omformningar (crop=, scale=, rotate=, flip=). Fungerar även som centrum för rotation för rotate=.

`anchor= *`coord`*`

`anchorN= *`coordN`*`

<table id="simpletable_3ED1CD0BF473439FA1132FC84B4452A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coord</span></span> </p> </td> 
  <td class="stentry"> <p>pixelförskjutning från källbildens övre vänstra hörn (int, int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p>normaliserad förskjutning från källbildens mitt (verklig, verklig) </p></td> 
 </tr> 
</table>

Fästpunkten omformas med bilden och blir lagerstartpunkten (om inte `origin=` också anges, i vilket fall `anchor=` används bara som mittpunkten för `rotate=`).

`anchorN=0,0` placerar bildankarpunkten i mitten av källbilden. `anchorN=-0.5,-0.5` eller `anchor=0,0` finns i det övre vänstra hörnet och `anchorN=0.5,0.5` i det nedre högra hörnet av källbilden.

## Egenskaper {#section-f08942bc6aae46a8b5d341faaff80640}

Källbildattribut. Gäller för det aktuella lagret eller för lagret 0 om `layer=comp`.

## Standard {#section-35d369fab1254f1a9b91684a6e169ad1}

Om `anchor=` inte anges används katalogen::Anchor. Om `catalog::Anchor` inte är definierad används bildrektangelns mitt (samma som att ange `anchorN=0,0`).

Textlager som innehåller `textPs=` och lager som innehåller `clipPath=` kan ha olika standardankarpunkter.

## Exempel {#section-cc127e6b1ea94524900b5c0dd8b4c7ec}

Se&quot;Exempel C&quot; i [Mallar](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Se även {#section-9877ea3a0743492aaa4fa1dfc9510b07}

[katalog::Anchor](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md) , [origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138), [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [textlager](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
