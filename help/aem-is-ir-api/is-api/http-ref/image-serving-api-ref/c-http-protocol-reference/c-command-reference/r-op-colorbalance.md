---
description: Justera färgbalansen. Justerar värdet för varje RGB-färgkomponent separat.
seo-description: Justera färgbalansen. Justerar värdet för varje RGB-färgkomponent separat.
seo-title: op_colorbalance
solution: Experience Manager
title: op_colorbalance
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 177aa6e3-1b32-4254-85f1-d7fe14116e3c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# op_colorbalance{#op-colorbalance}

Justera färgbalansen. Justerar värdet för varje RGB-färgkomponent separat.

`op_colorbalance= *``*, *``*, *`redAvslutgreenAvslutblueAdj`*`

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

Lager, kommando. Gäller det aktuella lagret eller den sammansatta bilden om `layer=comp`. Ignoreras av effektlager. CMYK-bilder och -lager konverteras till RGB innan åtgärden tillämpas.

## Standard {#section-08d84ef715964f7daea86f5ef237d199}

`op_colorbalance=0,0,0` utan färgändringar.

## Exempel {#section-7e97fa36e01d4af8ab03fc9d493da1a1}

Justera färgbalansen mot rött:

… `&op_colorBalance=100,0,0&`…
