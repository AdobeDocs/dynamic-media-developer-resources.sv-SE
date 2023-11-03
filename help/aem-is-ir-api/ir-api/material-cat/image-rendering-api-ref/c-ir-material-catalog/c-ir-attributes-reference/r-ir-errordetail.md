---
title: ErrorDetail
description: Information om felmeddelande. Anger detaljnivån för felmeddelanden som returneras via HTTP som error.message-värde.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39d7fc44-7605-4f93-b2f9-0a6e8bc76ec7
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '166'
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
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Kort meddelande. Reserverad för framtida bruk. Returnerar för närvarande samma information som 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Detaljerat meddelande. Innehåller information på användarnivå om felet. Kan innehålla känslig information, till exempel filsökvägar. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Fullständig felsökningsinformation. Lägger till Java™-stackspår när det är tillämpligt. Felbilder innehåller aldrig stackspår och returnerar i stället nivå 2-information i <span class="codeph"> $error.message</span>. </p></td> 
 </tr> 
</table>

* Nivå 0 rekommenderas för liveservrar som är tillgängliga för allmänheten.
* Nivå 2 rekommenderas för testnings-, kvalitetssäkrings- och programutvecklingsservrar.
* Information på nivå 3 kan vara användbar vid rapportering av problem till Dynamic Media tekniska support.

## Egenskaper {#section-f03f9a8edd6a4d99aff38fbec41c4b80}

Uppräknat värde, måste vara 0, 1, 2 eller 3.

## Standard {#section-5e78d550050840cc9a1de811c581b94f}

Ärvs från `default::ErrorDetail` om den inte anges eller om den är tom.

## Se även {#section-474e71922d194c7ca06f2aad3b30e025}

[attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
