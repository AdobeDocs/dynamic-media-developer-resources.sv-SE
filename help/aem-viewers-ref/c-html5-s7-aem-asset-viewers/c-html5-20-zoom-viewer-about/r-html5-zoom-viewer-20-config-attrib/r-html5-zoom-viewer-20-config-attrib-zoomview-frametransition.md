---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.frametransition
solution: Experience Manager
title: ZoomView.frametransition
topic: Dynamic media
uuid: 28e283ca-51d8-4d6c-9b8a-d16da21f4da1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 1%

---


# ZoomView.frametransition{#zoomview-frametransition}

` [ZoomView.|<containerId>_zoomView.]frametransition=none|fade|slide[, *`avstånd `*[, *`för varaktighet`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ingen|tona|bildruta  </span> </p> </td> 
   <td colname="col2"> <p>Anger vilken typ av effekt som används vid bildruteändring. <span class="codeph"> ingen  </span> står för någon övergång; bildruteändringen sker omedelbart. <span class="codeph"> toning  </span> innebär en övergång mellan gamla och nya bildrutor. <span class="codeph"> bildrutan  </span> aktiverar övergång där den gamla bildrutan glider ut ur vyn och den nya bildrutan glider in. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> varaktighet  </span> </span> </p> </td> 
   <td colname="col2"> <p>Anger längden (i sekunder) på <span class="codeph"> toningen </span> eller <span class="codeph"> bildrutan </span> övergångseffekten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> avstånd  </span> </span> </p> </td> 
   <td colname="col2"> <p>Avståndet mellan intilliggande bildrutor i övergången <span class="codeph"> för bildrutan </span> ligger mellan <span class="codeph"> 0 </span> och <span class="codeph"> 1 </span> och är relativt till komponentens bredd. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

Ingen.

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,1`
