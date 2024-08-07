---
title: op_noise
description: Lägg till brus. Lägger till slumpmässigt brus i förgrundsbildens data eller i ett effektlagers förgrund.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eeadd3ab-80ff-4f9b-b5b7-4f3da6feebde
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---

# op_noise{#op-noise}

Lägg till brus. Lägger till slumpmässigt brus i förgrundsbildens data eller i ett effektlagers förgrund.

`op_noise= *`val`*[,uniform|gaussian[, *`monokrom`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> val</span> </p> </td> 
   <td colname="col2"> <p>Mängd brus i procent (0...100 int). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> enhetlig </span> </p> </td> 
   <td colname="col2"> <p>Välj enhetlig brusfördelning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> gaussiska </span> </p> </td> 
   <td colname="col2"> <p>Välj gaussisk brusfördelning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> monokrom </span> </p> </td> 
   <td colname="col2"> <p>Ange 0 för färgbrus, 1 för grått brus. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`monochrome`* ignoreras för gråskalebilder.

## Egenskaper {#section-1f1a64c791f545a3bf1abd0b0e575d87}

kommandot Lager. Gäller det aktuella lagret eller den sammansatta bilden om `layer=comp`.

## Standard {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`, utan brus.
