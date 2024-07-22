---
title: pos
description: Lagerposition.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2e9a1f3-7216-4ab0-9c37-57f083119cef
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---

# pos{#pos}

Lagerposition.

pos= *`coord`*

posN= *`coordN`*

<table id="simpletable_754F76EE00BF4129B07502647FF172B7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">-kod</span> </p> </td> 
  <td class="stentry"> <p>Pixelförskjutning från det här lagrets origo till origo för lagret 0 (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>Normaliserad förskjutning från det här lagrets ursprung till origo för lagret 0 (verklig, verklig). </p></td> 
 </tr> 
</table>

Om det finns en bild, text och enfärgslager anger `pos=` positionen för ett lagerankare i förhållande till ankarpunkten för lagret 0. Koordinatvärdena för `posN=` har normaliserats i förhållande till den faktiska storleken på lagret 0.

Om det finns effektlager flyttar `pos=` effektlagret i förhållande till det överordnade lagret.

Positiva värden flyttar lagret åt höger/nedåt och negativa åt vänster/uppåt. I `posN=0.5,0.5` flyttas lagret halva lagrets bredd 0 och höjd nedåt och åt höger.

## Egenskaper {#section-51a60cdc52d040538fef378ace7c2e7d}

Lagerattribut. Ignorerad om `layer=0` eller `layer=comp`.

## Standard {#section-70a6bc71ded5494e843194dfb6bf5a6c}

`posN=0,0`. Med den här koordinaten placeras lagerankarpunkten på samma plats som ankarpunkten för lager 0 om det är ett bild-, text- eller enfärgslager. Placerar ett effektlager direkt över eller under det överordnade lagret.

## Exempel {#section-a89a02c22f6b4260bfcf7c842cd6069d}

Se exempel A i [Mallar](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Se även {#section-812d95575ba542808e8387d0a8650606}

[origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)
