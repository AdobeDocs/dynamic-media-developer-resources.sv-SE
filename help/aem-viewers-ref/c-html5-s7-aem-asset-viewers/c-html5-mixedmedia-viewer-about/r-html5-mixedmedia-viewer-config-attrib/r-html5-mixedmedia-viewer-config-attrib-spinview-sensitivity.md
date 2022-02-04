---
title: SpinView.sensitivity
description: SpinView.sensitivity
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 68df87db-b3c7-4a42-9ab6-742d96261ecd
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---

# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *`Känslighet`*[, *`Känslighet`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Känslighet</span>[, <span class="varname"> Känslighet</span>]</span> </p> </td> 
   <td colname="col2"> <p> Styr känsligheten för det vågräta och lodräta rotationsintervallet som utförs med en musdragning eller dragning. </p> <p> <span class="codeph"> Känslighet</span> Anger hur många horisontella produktrotationer som görs om användaren drar musen vågrätt från den ena sidan av vyn till den andra. Tre innebär till exempel att användaren ser tre fullständiga snurrningar för en fullständig dragningsgest. </p> <p>På samma sätt <span class="codeph"> Känslighet</span> styr den lodräta rotationens känslighet. Värdet 1 innebär att en hel lodrät dragning eller dragning ändrar visningsvinkeln från det översta rotationsplanet till det understa (eller omvänt). </p> <p>Ange ett negativt värde för <span class="codeph"> Känslighet</span> inverterar den lodräta rotationens riktning. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
