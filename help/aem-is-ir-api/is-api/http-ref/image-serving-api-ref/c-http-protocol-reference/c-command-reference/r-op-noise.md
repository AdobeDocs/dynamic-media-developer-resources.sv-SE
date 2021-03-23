---
description: Lägg till brus. Lägger till slumpmässigt brus i förgrundsbildens data eller i ett effektlagers förgrund.
seo-description: Lägg till brus. Lägger till slumpmässigt brus i förgrundsbildens data eller i ett effektlagers förgrund.
seo-title: op_noise
solution: Experience Manager
title: op_noise
uuid: 531f7a94-149b-4090-a163-a1895156250b
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---


# op_noise{#op-noise}

Lägg till brus. Lägger till slumpmässigt brus i förgrundsbildens data eller i ett effektlagers förgrund.

`op_noise= *``*[,uniform|gaussian[, *`valmonokrom`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> val</span> </p> </td> 
   <td colname="col2"> <p>Mängd brus i procent (0...100 int). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> enhetlig</span> </p> </td> 
   <td colname="col2"> <p>Välj enhetlig brusfördelning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> gaussisk</span> </p> </td> 
   <td colname="col2"> <p>Välj gaussisk brusfördelning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> monokrom</span> </p> </td> 
   <td colname="col2"> <p>Ange 0 för färgbrus, 1 för grått brus. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`monochrome`* ignoreras för gråskalebilder.

## Egenskaper {#section-1f1a64c791f545a3bf1abd0b0e575d87}

Lager, kommando. Gäller det aktuella lagret eller den sammansatta bilden om `layer=comp`.

## Standard {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`, utan brus.
