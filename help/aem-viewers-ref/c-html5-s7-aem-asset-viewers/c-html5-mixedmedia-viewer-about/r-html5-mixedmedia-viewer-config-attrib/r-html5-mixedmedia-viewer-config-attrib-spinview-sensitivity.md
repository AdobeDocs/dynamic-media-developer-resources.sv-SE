---
description: 'null'
seo-description: 'null'
seo-title: SpinView.sensitive
solution: Experience Manager
title: SpinView.sensitive
topic: Dynamic media
uuid: 7c63a7c5-ac75-485d-94ac-d1e133fbe44f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.sensitive{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *``*[, *`xKänslighetKänslighet`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> xKänslighet</span>[, <span class="varname"> känslighet</span>]</span> </p> </td> 
   <td colname="col2"> <p> Styr känsligheten för det vågräta och lodräta rotationsintervallet som utförs med en musdragning eller dragning. </p> <p> <span class="codeph"> Känslighet</span> anger hur många horisontella produktrotationer som görs om användaren drar musen vågrätt från ena sidan av vyn till den andra. Tre innebär till exempel att användaren ser tre fullständiga snurrningar för en fullständig dragningsgest. </p> <p>På samma sätt styr <span class="codeph"> yKänslighet</span> den lodräta rotationens känslighet. Värdet 1 innebär att en hel lodrät dragning eller dragning ändrar visningsvinkeln från det översta rotationsplanet till det understa (eller tvärtom). </p> <p>Om du anger ett negativt värde för <span class="codeph"> yKänslighet</span> inverteras riktningen för den lodräta rotationen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
