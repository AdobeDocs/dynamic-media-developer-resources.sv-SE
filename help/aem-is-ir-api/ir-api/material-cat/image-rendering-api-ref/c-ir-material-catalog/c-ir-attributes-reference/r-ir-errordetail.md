---
description: Information om felmeddelande. Anger detaljnivån för felmeddelanden som returneras via HTTP som error.message-värde.
seo-description: Information om felmeddelande. Anger detaljnivån för felmeddelanden som returneras via HTTP som error.message-värde.
seo-title: ErrorDetail
solution: Experience Manager
title: ErrorDetail
topic: Scene7 Image Serving - Image Rendering API
uuid: aab11640-95d7-427d-b79f-c477b2c9047e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 2%

---


# ErrorDetail{#errordetail}

Information om felmeddelande. Anger detaljnivån för felmeddelanden som returneras via HTTP som error.message-värde.

## Titel {#section-c10d75d72ee24d16a67cc8d927f1deba}

Följande värden är tillåtna:

<table id="simpletable_7904444FF9F14D678F05094CA9E45664"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Endast titel. Returnerar en kort allmän beskrivning av felet. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Kort meddelande. Reserverad för framtida bruk. Returnerar för närvarande samma information som 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Detaljerat meddelande. Innehåller information på användarnivå om felet. Kan innehålla känslig information, t.ex. filsökvägar. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Fullständig felsökningsinformation. Lägger till Java-stackspår när det är tillämpligt. Felbilder innehåller aldrig stackspår och returnerar i stället nivå 2-information i <span class="codeph"> $error.message</span>. </p></td> 
 </tr> 
</table>

* Nivå 0 rekommenderas för liveservrar som är tillgängliga för allmänheten.
* Nivå 2 rekommenderas för testnings-, kvalitetssäkrings- och programutvecklingsservrar.
* Information på nivå 3 kan vara användbar när du rapporterar problem till Scene7 Tech Support.

## Egenskaper {#section-f03f9a8edd6a4d99aff38fbec41c4b80}

Uppräknat värde, måste vara 0, 1, 2 eller 3.

## Standard {#section-5e78d550050840cc9a1de811c581b94f}

Ärvs från `default::ErrorDetail` om det inte anges eller om det är tomt.

## Se även {#section-474e71922d194c7ca06f2aad3b30e025}

[attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
