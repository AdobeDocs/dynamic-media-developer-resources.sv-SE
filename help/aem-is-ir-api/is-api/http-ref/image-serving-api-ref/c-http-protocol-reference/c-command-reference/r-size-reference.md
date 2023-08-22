---
title: size
description: Lagerstorlek. Anger storleken eller den maximala lagerstorleken för ett lager, innan rotate=, perspective= och extend= används på lagret.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 55feeb32-b69d-4b95-80fb-c77f2612d255
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# size{#size}

Lagerstorlek. Anger storleken eller den maximala lagerstorleken för ett lager, innan rotate=, perspective= och extend= används på lagret.

` size= *`width`*, *`height`*`

` sizeN= *`widthN`*, *`heightN`*`

<table id="simpletable_FBE17D736F93485AA0053BF447B4CC9F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span>, <span class="varname"> height </span> </span> </p> </td> 
  <td class="stentry"> <p>Lagerstorleksbegränsning i pixlar (int, int, 0 eller högre). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> widthN </span>, <span class="varname"> heightN </span> </span> </p> </td> 
  <td class="stentry"> <p>Lagerstorleksbegränsning normaliserad i förhållande till lagrets 0-storlek (verklig, 0.0...1.0). </p> </td> 
 </tr> 
</table>

När det anges för ett bildlager, bibehåller size= lagerbildens bredd, höjd eller både och. Bilden skalas så att den inte är större än `size=`. Om en normaliserad storlek anges är den relativ till storleken på lagret 0. Om båda *`width`* och *`height`* anges skalas källbilden (efter `crop=` används) så att ingen dimension överskrider den angivna storleken. Källrektangelns proportioner bevaras i alla fall. Antingen *`width`* eller *`height`* kan anges till 0. I det här fallet beräknas värdet av servern baserat på bildens proportioner.

När det anges för ett textlager, `size=` anger textrutans storlek. *`width`* krävs, *`height`* kan anges till 0, i vilket fall layouttextens höjd används som lagerhöjd. Som standard infogar textlayoutmotorer radbrytningar för att säkerställa att texten alltid passar in vågrätt i det tillgängliga utrymmet. If *`height`* har angetts beskärs rader som inte får plats i det tillgängliga utrymmet ( `text=`) eller utelämnad ( `textPs=`). `text=` har stöd för ytterligare anpassningslägen, se `textAttr=` för mer information.

När det anges för ett enfärgat lager, `size=` definierar den exakta lagerstorleken. Båda värdena måste anges (om ingen mask anges). If `mask=` anges också, så att maskbilden anpassas `size=` på samma sätt som bilder skalas i bildlager.

## Egenskaper {#section-5f254b66fcba49bcb63f9c9ea40b230c}

Lagerattribut. Gäller för lager 0 om `layer=comp`. `sizeN=` tillåts inte för `layer=0` eller `layer=comp`. `sizeN=` är tillåtet för `layer=0` och `layer=comp` endast i katalogposter som definierar vattenstämpelbilder. I detta fall `sizeN` definierar skalningen av vattenstämpelbilden i förhållande till den sammansatta bild som vattenstämpeln används på. If `size=` anges, `res=` och `scale=` ignoreras för detta lager. Ignoreras av effektlager.

## Standard {#section-43d129deba6a441da66a1fdb63d1c85c}

`size=0,0`, är lagerstorleken obegränsad. För bildlager bestäms sedan lagerstorleken baserat på lagerbildens storlek efter eventuella `crop=`, `scale=`, eller `res=` åtgärder har tillämpats. För textlager, om `size=` om inget anges ändras storleken på lagret automatiskt så att det passar den återgivna texten.

Solida färglager kräver antingen en fullständigt angiven `size=`, a `mask=`, eller `clipPath=`.

## Exempel {#section-d1adaddd9e0b4ca881fd8e0a7541e5d9}

Se [Exempel A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) in [Mallar](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Se även {#section-63dfdf3750e249d2ab4c825ccd2e7181}

[scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065) , [res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [Textlager](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
