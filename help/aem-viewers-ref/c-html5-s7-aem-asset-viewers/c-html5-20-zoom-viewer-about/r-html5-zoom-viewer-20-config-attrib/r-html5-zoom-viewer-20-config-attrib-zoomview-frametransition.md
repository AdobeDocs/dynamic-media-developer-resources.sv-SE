---
title: ZoomView.frametransition
description: ZoomView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: f57a8a2e-63a1-4a59-9a25-b435d0ac39dc
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 1%

---

# ZoomView.frametransition{#zoomview-frametransition}

` [ZoomView.|<containerId>_zoomView.]frametransition=none|fade|slide[, *`varaktighet`*[, *`avstånd`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ingen|tona|bildruta </span> </p> </td> 
   <td colname="col2"> <p>Anger vilken typ av effekt som används vid bildruteändring. Attributet <span class="codeph"> ingen </span> står för ingen övergång, bildruteändringen sker omedelbart. Attributet <span class="codeph"> tona </span> betyder övertoningsövergång mellan gamla och nya bildrutor. Attributet <span class="codeph"> bild </span> aktiverar övergången där den gamla bildrutan glider ut ur vyn och den nya bildrutan glider in. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> varaktighet </span> </span> </p> </td> 
   <td colname="col2"> <p>Anger längden (i sekunder) för <span class="codeph"> tona </span> eller <span class="codeph"> bild </span> övergångseffekt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> avstånd </span> </span> </p> </td> 
   <td colname="col2"> <p>Avståndet mellan intilliggande bildrutor i <span class="codeph"> bild </span> övergång, har intervallet från <span class="codeph"> 0 </span> via <span class="codeph"> 1 </span> och är relativ till komponentens bredd. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

Ingen.

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,1`
