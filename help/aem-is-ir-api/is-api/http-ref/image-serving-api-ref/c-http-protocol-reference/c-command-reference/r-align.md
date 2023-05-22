---
description: Justera bild med Visa. Justerar den sammansatta bilden (eventuellt efter skalning, om scl= även anges) inom visningsrektangeln som definieras av wid= och hei=.
solution: Experience Manager
title: justera
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 01001cc6-1a60-4d6b-a27f-ea5822be6d11
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 0%

---

# justera{#align}

Justera bild med Visa. Justerar den sammansatta bilden (eventuellt efter skalning, om scl= även anges) inom visningsrektangeln som definieras av wid= och hei=.

` align= *`vågrät`*, *`vert`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> vågrät </span> </span> </p> </td> 
  <td class="stentry"> <p>vågrät justering (verklig, -1.0...1.0) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> vert </span> </span> </p> </td> 
  <td class="stentry"> <p>lodrät justering (verklig, -1.0...1.0) </p> </td> 
 </tr> 
</table>

Ange `align=-1,-1` om du vill justera den sammansatta bildens övre vänstra hörn mot vyns övre vänstra hörn anger du `align=1,1` om du vill justera längst ned, till höger om bilden mot vyns nedre högra hörn. För standardförfrågningar om bilder och miniatyrbilder fylls alla områden i vyn som inte täcks av sammansatta bilddata med `bgc=`.

## Egenskaper {#section-3fbec8206fc944eda4746d8be84f3b41}

Visa attribut. ( `align=` används också för att definiera justeringen mellan en vattenstämpelbild och den sammansatta bild som vattenstämpeln används på.) Används oavsett aktuell lagerinställning. Ignorerad om endast en av `wid=` och `hei=` anges och när `fit=constrain` eller `fit=stretch`.

## Standard {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`som centrerar bilden i visningsrektangeln.

## Exempel {#section-2c9447aa2e184fb8ab1a4370dc61d554}

Följande begäran passar `myImage` till en 200 x 200 pixlar stor visningsrektangel.

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

If `myImage` är exakt fyrkantig, fyller hela visningsrektangeln. If `myImage` har stående proportioner, skalas till 200 pixlar hög och centreras vågrätt i vyn. If `myImage` har liggande proportioner, skalas till 200 pixlar bred och justeras mot vyns överkant. I samtliga fall är den returnerade bilden exakt 200 × 200 pixlar stor. allt utrymme som inte täcks av den skalade `myImage` fylls med `attribute::BkgColor` (ange bgc= om du vill styra bakgrundsfärgen dynamiskt).

## Se även {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [Vattenstämplar](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)
