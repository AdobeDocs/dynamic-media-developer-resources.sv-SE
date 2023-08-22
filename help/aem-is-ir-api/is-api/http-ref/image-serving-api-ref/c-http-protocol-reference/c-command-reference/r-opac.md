---
title: opac
description: Justera bildens opacitet. Gör att förgrundsopaciteten för en bild, text, enfärgat lager eller effektlager kan minskas.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38e0e1dc-46c0-48a4-b676-f7e6d262392f
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# opac{#opac}

Justera bildens opacitet. Gör att förgrundsopaciteten för en bild, text, enfärgat lager eller effektlager kan minskas.

`opac= *`opacitet`*[, *`fillOpacity`*]`

<table id="simpletable_DA4B5D86C496480886FADB284AD6047F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> opacitet</span> </p> </td> 
  <td class="stentry"> <p>Primär opacitet (0...100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> fillOpacity</span> </p></td> 
  <td class="stentry"> <p>Fyllningsopacitet (0...100 int). </p></td> 
 </tr> 
</table>

Förgrundsopaciteten för ett bildlager bestäms av lagermasken eller bildens alfakanal, eller om ingen av dem finns, är den 100 %. Förgrundsopaciteten för ett textlager är 100 % och för ett enfärgat lager anges med `color=`.

`opac=` ändrar aldrig opaciteten för ytor som fylls med `color=` eller `bgColor=`, förutom förgrundsområdena för enfärgade lager och effektlager (anges med `color=`).

När det anges i en bild, text eller enfärgat lager, *`opacity`* använder hela lagret, inklusive alla associerade effektlager, medan *`fillOpacity`* används bara på det primära lagrets innehåll. När det anges i ett effektlager, *`opacity`* används på effektlagret, medan *`fillOpacity`* ignoreras.

Den effektiva opaciteten för innehållet i huvudlagret är ( *`opacity`* &#42; *`fillOpacity`* / 100). Effektiv opacitet för effektlager är (huvudvärde) *`opacity`* &#42; effekt *`opacity`* / 100).

## Egenskaper {#section-ac3f136ff1584a2eab87500b7164f7fa}

Lagerattribut. Gäller det aktuella lagret eller den sammansatta bilden om `layer=comp`.

## Standard {#section-abba67ed028049048ae43405ea69b164}

`opac=100,100`, utan ändring av lageropacitet.

## Exempel {#section-9710810e96af40538652e8ae4aadd3be}

… `&layer=1&text=variable%20opacity&opac=90,70&effect=-1&opac=50&`…

Textopaciteten i detta exempel är 90&#42;70/100=63 % och effektlagrets opacitet är 90&#42;50/100=45 %.

## Se även {#section-dbdad35ccd544590b4b11d31a9ab062e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)
