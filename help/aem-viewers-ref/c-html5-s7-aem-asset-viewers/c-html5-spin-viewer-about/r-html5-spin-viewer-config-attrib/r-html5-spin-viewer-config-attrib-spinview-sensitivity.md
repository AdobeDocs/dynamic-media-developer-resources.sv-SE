---
description: SpinView.sensitivity
solution: Experience Manager
title: SpinView.sensitivity
topic: Dynamic media
uuid: 82cf1f26-3af0-494f-b918-fdc318959c75
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---


# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *``*[, *`xKänslighetKänslighet`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> xSensitivity</span>[,  <span class="varname"> ySensitivity</span>]</span> </p> </td> 
   <td colname="col2"> <p> Styr känsligheten för det vågräta och lodräta rotationsintervallet som utförs med en musdragning eller dragning. </p> <p> <span class="codeph"> </span> xSensitiviteter anger hur många horisontella produktrotationer som görs om användaren drar musen vågrätt från ena sidan av vyn till den andra. Tre innebär till exempel att användaren ser tre fullständiga snurrningar för en fullständig dragningsgest. </p> <p>På samma sätt styr <span class="codeph"> yKänslighet</span> känsligheten för den lodräta rotationen. Värdet 1 innebär att en hel lodrät dragning eller dragning ändrar visningsvinkeln från det översta rotationsplanet till det understa (eller tvärtom). </p> <p>Om du anger ett negativt värde för <span class="codeph"> ySensitivity</span> inverteras riktningen för den lodräta rotationen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
