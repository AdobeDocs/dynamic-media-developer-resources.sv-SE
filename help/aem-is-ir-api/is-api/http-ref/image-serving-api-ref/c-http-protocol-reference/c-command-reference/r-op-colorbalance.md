---
title: op_colorbalance
description: Justera färgbalansen. Justerar värdet för varje RGB-färgkomponent separat.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 93476778-97b0-4ad5-b22a-093239e845f0
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---

# op_colorbalance{#op-colorbalance}

Justera färgbalansen. Justerar värdet för varje RGB-färgkomponent separat.

`op_colorbalance= *`redAdj`*, *`greenAdj`*, *`blueAdj`*`

<table id="simpletable_BBDAA6FE9A0E48E3BD8304BDED776713"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> redAdj</span> </p></td> 
  <td class="stentry"> <p>Justering av röda komponenter (-100..+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> greenAdj</span> </p></td> 
  <td class="stentry"> <p>Justering av grön komponent (-100..+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> blueAdj</span> </p></td> 
  <td class="stentry"> <p>Justering av blå komponent (-100..+100 int). </p></td> 
 </tr> 
</table>

Grå- och CMYK-indata konverteras till RGB med inbyggd konvertering som inte är korrekt när färghantering är aktiverat.

## Egenskaper {#section-dff9c934f7c1442bbd02379b688d82e2}

kommandot Lager. Gäller det aktuella lagret eller den sammansatta bilden om `layer=comp`. Ignoreras av effektlager. CMYK-bilder och -lager konverteras till RGB innan åtgärden tillämpas.

## Standard {#section-08d84ef715964f7daea86f5ef237d199}

`op_colorbalance=0,0,0` om du inte vill ändra färger.

## Exempel {#section-7e97fa36e01d4af8ab03fc9d493da1a1}

Justera färgbalansen mot rött:

... `&op_colorBalance=100,0,0&`...
