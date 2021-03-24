---
description: ZoomView.frametransition
solution: Experience Manager
title: ZoomView.frametransition
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Zoom
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

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
