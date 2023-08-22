---
title: ankare
description: Bildankarpunkt. Definierar fästpunkten för rektangeln för bilden, den heltäckande färgen eller textrutan innan du använder omformningar (crop=, scale=, rotate=, flip=). Fungerar även som centrum för rotation för rotate=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f62ae048-0dcc-4e93-a9f1-2e4db6bef51f
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# ankare{#anchor}

Bildankarpunkt. Definierar fästpunkten för rektangeln för bilden, den heltäckande färgen eller textrutan innan du använder omformningar (crop=, scale=, rotate=, flip=). Fungerar även som centrum för rotation för rotate=.

`anchor= *`coord`*`

`anchorN= *`coordN`*`

<table id="simpletable_3ED1CD0BF473439FA1132FC84B4452A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coord</span> </span> </p> </td> 
  <td class="stentry"> <p>pixelförskjutning från källbildens övre vänstra hörn (int, int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p>normaliserad förskjutning från källbildens mitt (verklig, verklig) </p></td> 
 </tr> 
</table>

Fästpunkten omformas med bilden och blir lagerstartpunkten (om inte `origin=` anges också, i vilket fall `anchor=` används endast som rotationscenter för `rotate=`).

`anchorN=0,0` placerar bildankarpunkten i mitten av källbilden. `anchorN=-0.5,-0.5` eller `anchor=0,0` finns i det övre vänstra hörnet, och `anchorN=0.5,0.5` finns längst ned till höger i källbilden.

## Egenskaper {#section-f08942bc6aae46a8b5d341faaff80640}

Källbildattribut. Gäller för det aktuella lagret eller för lagret 0 om `layer=comp`.

## Standard {#section-35d369fab1254f1a9b91684a6e169ad1}

If `anchor=` har inte angetts, catalog::Anchor används. If `catalog::Anchor` är inte definierad, bildrektangelns mitt används (samma som att ange `anchorN=0,0`).

Textlager som innehåller `textPs=` och lager som `clipPath=` kan ha olika standardankarpunkter.

## Exempel {#section-cc127e6b1ea94524900b5c0dd8b4c7ec}

Se&quot;Exempel C&quot; i [Mallar](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Se även {#section-9877ea3a0743492aaa4fa1dfc9510b07}

[katalog::Ankarpunkt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md) , [origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138), [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [Textlager](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
