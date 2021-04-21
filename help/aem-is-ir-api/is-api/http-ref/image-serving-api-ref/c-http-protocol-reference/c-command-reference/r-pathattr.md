---
description: Text på bana-attribut.
solution: Experience Manager
title: pathAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---


# pathAttr{#pathattr}

Text på bana-attribut.

` pathAttr= *``*[, *``*[, *`directionstartPosendPos`*]]`

<table id="simpletable_EC76095316AF4F07B1DDCC0D72B814CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> riktning  </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> norm  </span> |  <span class="codeph"> omvänd  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> startPos  </span> </p> </td> 
  <td class="stentry"> <p>Textstartposition på bana (verklig 0.0...1.0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> endPos  </span> </p> </td> 
  <td class="stentry"> <p>Textslutposition på bana (verklig 0.0...&lt;2.0). </p> </td> 
 </tr> 
</table>

Ange `norm` om du vill rita text med början nära den första banans hörnpunkt och `reverse` om du vill rita text i motsatt riktning, med början nära den sista hörnpunkten.

*`startPos`* och  *`endPos`* det går att justera var på banan texten ska ritas. 0,0 motsvarar det första hörnet i banan och 1,0 det sista hörnet, mellanliggande värden anger avståndet längs banan mellan det första och sista hörnet.

## Egenskaper {#section-80f266da4e2549d89f022a3f9ff4584d}

Lagerattribut. Ignoreras om lagret inte innehåller kommandona `textPs=` och `textPath=`.

*`startPos`* måste vara större än eller lika med 0 och mindre än 1,0.  *`endPos`* måste vara större än  *`startPos`* och mindre än eller lika med 1.0 när det används på en öppen bana, eller mindre än eller lika med (  *`startPos`* + 1.0) när det används på en stängd bana.

## Standard {#section-3e757970885c45e7b6100e78dc08626f}

`pathAttr=norm,0,1`

## Se även {#section-b869745de1da4ef996dfda4af39ed14d}

[textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd) ,  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
