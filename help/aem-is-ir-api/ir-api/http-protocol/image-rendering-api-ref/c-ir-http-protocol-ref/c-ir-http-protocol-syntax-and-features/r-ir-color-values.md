---
description: Färgvärden för attributen color= och bgc= kan anges med hjälp av en lista med decimalvärden, kommaavgränsade komponentvärden eller en hex-notation, som liknar HTML.
solution: Experience Manager
title: Färgvärden
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 8%

---


# Färgvärden{#color-values}

Färgvärden för attributen color= och bgc= kan anges med hjälp av en lista med decimalvärden, kommaavgränsade komponentvärden eller en hex-notation, som liknar HTML.

<table id="simpletable_9B3A231D5BB14A3DB2B42B341E198341"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> färg</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">{red , green, blue} | grå } | { [ 0x ] hex6 } | { 0xhex2 }</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>röd, grön, blå, grå</i> </p></td> 
  <td class="stentry"> <p>Färgkomponentvärde (0...255, decimalheltal). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>hex6</i> </p></td> 
  <td class="stentry"> <p>Paketerat sexsiffrigt hexadecimalt RGB-färgvärde (RRGGBB). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>hex2</i> </p></td> 
  <td class="stentry"> <p>Paketerat tvåsiffrigt hexadecimalt grått färgvärde (0...FF). </p></td> 
 </tr> 
</table>

## Exempel {#section-a78732151d584e84abeb99f9ce8d7c24}

Några exempel på giltiga färgspecifikationer och deras motsvarande RGB-färgvärdestolkning:

<table id="simpletable_837B3173020240A5B7B2DB2F4CC57352"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,100,200 </p></td> 
  <td class="stentry"> <p>(0,100,200) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>128 </p></td> 
  <td class="stentry"> <p>(128 128 128) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0x010203 </p></td> 
  <td class="stentry"> <p>(1,2,3) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>00b1c2 </p></td> 
  <td class="stentry"> <p>(160,177,194) </p></td> 
 </tr> 
</table>

## Se även {#section-207d5cb918a94736a27445faa58917d3}

[color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa),  [bgc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-bgc.md#reference-3f5c78cea01c4a85aa582076d23aebb0),  [grout=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a)
