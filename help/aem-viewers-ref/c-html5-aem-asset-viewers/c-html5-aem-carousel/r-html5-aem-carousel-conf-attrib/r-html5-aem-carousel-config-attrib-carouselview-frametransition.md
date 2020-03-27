---
description: 'null'
seo-description: 'null'
seo-title: CarouselView.frametransition
solution: Experience Manager
title: CarouselView.frametransition
topic: Dynamic media
uuid: 9539ede1-08fb-4bfc-8a5a-870c7d84de7f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# CarouselView.frametransition{#carouselview-frametransition}

` [CarouselView.|<containerId>_carouselView.]frametransition=none|fade|slide[, *`avstånd`*[, *`för varaktighet`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ingen|tona|bildruta </span> </p> </td> 
   <td colname="col2"> <p>Anger vilken typ av effekt som används vid bildruteändring. <span class="codeph"> ingen </span> står för någon övergång, bildruteändringen sker omedelbart. </p> <p> <span class="codeph"> toning </span> innebär en övergång mellan gamla och nya bildrutor. </p> <p> <span class="codeph"> bildrutan </span> aktiverar övergång där den gamla bildrutan glider ut ur vyn och den nya bildrutan glider in. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> varaktighet </span></span> </p> </td> 
   <td colname="col2"> <p>Anger längden (i sekunder) för <span class="codeph"> tonings- </span> eller <span class="codeph"> bildruteövergångseffekten </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> mellanrum </span></span> </p> </td> 
   <td colname="col2"> <p>Avståndet mellan intilliggande bildrutor i <span class="codeph"> bildruteövergången är </span> mellan <span class="codeph"> 0 </span> och <span class="codeph"> 1 </span> och är relativt till komponentens bredd. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

Ingen.

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,0.3`
