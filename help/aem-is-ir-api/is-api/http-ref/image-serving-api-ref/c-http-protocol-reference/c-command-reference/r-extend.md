---
description: Utöka lager. Lägger till marginaler i ett lager eller beskär lagrets rektangel.
seo-description: Utöka lager. Lägger till marginaler i ett lager eller beskär lagrets rektangel.
seo-title: utöka
solution: Experience Manager
title: utöka
topic: Scene7 Image Serving - Image Rendering API
uuid: 7ca69994-e788-41a9-93ac-f22b6b9920d0
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# utöka{#extend}

Utöka lager. Lägger till marginaler i ett lager eller beskär lagrets rektangel.

`extend= *`vänster`*, *``*, *``*, *`höger nederkant`*`

`extendN= *``*, *``*, *``*, *`leftNtopNrightNbottomN`*`

<table id="simpletable_1DCCD469712B423C8154630127DC5F54"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> vänster,övre,nedre,höger</span></span> </p></td> 
  <td class="stentry"> <p>Antal pixlar att lägga till (eller ta bort från, om värdet är negativt) i den vänstra, övre, högra och nedre kanten av lagerrektangeln (int, int, int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> vänsterN,övreN,nedreN,högerN</span></span> </p></td> 
  <td class="stentry"> <p>Mängd utrymme som ska läggas till (eller tas bort från, om värdet är negativt) i den vänstra, övre, högra och nedre kanten av lagerrektangeln, uttryckt som normaliserade värden i förhållande till storleken på den ursprungliga lagerrektangeln (reella, reella, reella). </p></td> 
 </tr> 
</table>

`extend=` används på lagret *när* bilden har beskurits ( `crop=`) och alla lageromformningar, inklusive `rotate=`, har tillämpats.

Det utökade området fylls med `bgColor=`eller förblir genomskinligt om det inte anges.

Argumentvärden för `extendN=` är normaliserade i förhållande till storleken på lagerrektangeln efter lageromformningar, inklusive `rotate=` har tillämpats.

## Egenskaper {#section-8fc94de871f841f3bf5e1df135972ca9}

Lagerattribut. Gäller för lager 0 om `layer=comp`. Ignoreras av effektlager.

## Standard {#section-de7473649cb9406b8d99028c74c4b8dc}

`extend=0,0,0,0`, om du inte vill ändra lagrets rektangel.

## Exempel {#section-cc6d8e76f3dd4607ac31cb095d86c9fe}

**Beskär en bild och lägg sedan till en 5 pixlar bred, röd kant:**

`…&cropN=.2,.3,.8,.9&extend=5,5,5,5&bgColor=255,0,0&…`

**Skalförändra en bild till 200 pixlar bred och lägg till titeltext i en marginal på 30 pixlar ovanför bilden.**

Observera att höjden på den sammansatta bilden varierar beroende på bildens proportioner.

`http://server/myRootId/myImageId?size=200,0&extend=0,30,0,0&origin=0,0 layer=1&text=title-text&origin=0,0`

## Se även {#section-2d9572be32ca4602b60920b3810f3638}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b), [origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
