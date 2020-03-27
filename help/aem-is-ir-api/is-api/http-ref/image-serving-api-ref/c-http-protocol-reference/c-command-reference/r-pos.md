---
description: Lagerposition.
seo-description: Lagerposition.
seo-title: pos
solution: Experience Manager
title: pos
topic: Scene7 Image Serving - Image Rendering API
uuid: e9872ce9-5c47-49c5-9c87-4fa8441c4770
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# pos{#pos}

Lagerposition.

pos= *`coord`*

posN= *`coordN`*

<table id="simpletable_754F76EE00BF4129B07502647FF172B7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>Pixelförskjutning från det här lagrets origo till origo för lagret 0 (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>Normaliserad förskjutning från det här lagrets ursprung till origo för lagret 0 (verklig, verklig). </p></td> 
 </tr> 
</table>

När det gäller bild-, text- och heltäckande färglager anger `pos=` positionen för en lagerfästpunkt i förhållande till lagrets fästpunkt 0. `posN=` Koordinatvärden normaliseras i förhållande till den faktiska storleken på lagret 0 rect.

Om det gäller effektlager, `pos=` flyttas effektlagret i förhållande till det överordnade lagret.

Positiva värden flyttar lagret åt höger/nedåt, negativa åt vänster/uppåt. `posN=0.5,0.5` flyttar lagret halva lagrets bredd 0 och höjd nedåt och åt höger.

## Egenskaper {#section-51a60cdc52d040538fef378ace7c2e7d}

Lagerattribut. Ignoreras om `layer=0` eller `layer=comp`.

## Standard {#section-70a6bc71ded5494e843194dfb6bf5a6c}

`posN=0,0`. Då placeras lagerankarpunkten på samma plats som ankarpunkten för lager 0 om det är en bild, text eller ett enfärgat färglager. Placerar ett effektlager direkt över eller under det överordnade lagret.

## Exempel {#section-a89a02c22f6b4260bfcf7c842cd6069d}

Se Exempel A i [mallar](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Se även {#section-812d95575ba542808e8387d0a8650606}

[origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)
