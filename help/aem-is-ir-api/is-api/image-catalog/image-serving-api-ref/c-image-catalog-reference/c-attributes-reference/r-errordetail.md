---
description: Information om felmeddelande. Anger detaljnivån för felmeddelanden som returneras via HTTP som error.message-värde.
solution: Experience Manager
title: ErrorDetail
topic: Dynamic Media Image Serving - Image Rendering API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 2%

---


# ErrorDetail{#errordetail}

Information om felmeddelande. Anger detaljnivån för felmeddelanden som returneras via HTTP som error.message-värde.

Följande värden är tillåtna:

<table id="simpletable_26DC72727F224F2C8E97BF26619DB68B"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Endast titel. Returnerar en kort allmän beskrivning av felet. Rekommenderas för liveservrar som kan nås offentligt. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Kort meddelande. Reserverad för framtida bruk. Returnerar för närvarande samma information som 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Detaljerat meddelande. Innehåller information på användarnivå om felet. Kan innehålla känslig information, t.ex. filsökvägar. Rekommenderas för testnings-, kvalitetssäkring- och programutvecklingsservrar. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Fullständig felsökningsinformation. Lägger till Java-stackspår när det är tillämpligt. Felbilder innehåller aldrig stackspår och returnerar i stället nivå 2-information i <span class="codeph"> $error.message</span>. Den här informationen kan vara användbar när du rapporterar problem till Dynamic Media tekniska support. </p></td> 
 </tr> 
</table>

## Egenskaper {#section-e167895723ca4ad4ba283d3d7b4324de}

Uppräknat värde, måste vara 0, 1, 2 eller 3.

## Standard {#section-8f27098e509945a18676aca0675c8f41}

Ärvs från `default::ErrorDetail` om det inte anges eller om det är tomt.

## Se även {#section-5451b0525ed74121950bfc34726c3970}

[attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)
