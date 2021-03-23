---
description: Justera bildens opacitet. Gör att förgrundsopaciteten för en bild, text, enfärgat lager eller effektlager kan minskas.
seo-description: Justera bildens opacitet. Gör att förgrundsopaciteten för en bild, text, enfärgat lager eller effektlager kan minskas.
seo-title: opac
solution: Experience Manager
title: opac
uuid: 268279bd-d777-4afe-b175-841af7e55406
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---


# opac{#opac}

Justera bildens opacitet. Gör att förgrundsopaciteten för en bild, text, enfärgat lager eller effektlager kan minskas.

`opac= *``*[, *`opacitetOpacitet`*]`

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

Förgrundsopaciteten för ett bildlager bestäms av lagermasken eller bildens alfakanal, eller om ingen av dem finns, är den 100 %. Förgrundsopaciteten för ett textlager är 100 % och för ett enfärgat lager är `color=`.

`opac=` ändrar aldrig opaciteten för områden som är fyllda med  `color=` eller  `bgColor=`med undantag för förgrundsområden för enfärgade lager och effektlager (angivna med  `color=`).

När *`opacity`* anges i en bild, text eller enfärgat färglager används hela lagret, inklusive alla associerade effektlager, medan *`fillOpacity`* endast gäller innehållet i det primära lagret. När *`opacity`* anges i ett effektlager används det på effektlagret, medan *`fillOpacity`* ignoreras.

Den effektiva opaciteten för innehållet i huvudlagret är ( *`opacity`* * *`fillOpacity`* / 100). Effektiv opacitet för effektlager är (huvudvärde *`opacity`* * effekt *`opacity`* / 100).

## Egenskaper {#section-ac3f136ff1584a2eab87500b7164f7fa}

Lagerattribut. Gäller det aktuella lagret eller den sammansatta bilden om `layer=comp`.

## Standard {#section-abba67ed028049048ae43405ea69b164}

`opac=100,100`, utan ändring av lageropacitet.

## Exempel {#section-9710810e96af40538652e8ae4aadd3be}

… `&layer=1&text=variable%20opacity&opac=90,70&effect=-1&opac=50&`…

Textopaciteten i det här exemplet är 90*70/100=63 % och opaciteten för effektlagret är 90*50/100=45 %.

## Se även {#section-dbdad35ccd544590b4b11d31a9ab062e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) ,  [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)
