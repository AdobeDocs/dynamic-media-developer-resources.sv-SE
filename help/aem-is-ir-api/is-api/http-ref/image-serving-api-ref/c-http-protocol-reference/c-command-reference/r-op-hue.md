---
title: op_hue
description: Justera nyans. Ändrar nyansen för varje synlig pixel i lagret eller den sammansatta bilden med den angivna mängden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b436bd31-12a9-42ed-9ad3-5ff91e3ccce9
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---

# op_hue{#op-hue}

Justera nyans. Ändrar nyansen för varje synlig pixel i lagret eller den sammansatta bilden med den angivna mängden.

`op_hue= *`adj`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Nyansjustering i grader (-180...+180 int). </p></td> 
 </tr> 
</table>

Baserat på ett 360-graders nyansintervall.

## Egenskaper {#section-55779644700b4c808a624cdf5a04447e}

kommandot Lager. Gäller det aktuella lagret eller den sammansatta bilden om `layer=comp`. Ignoreras av effektlager. CMYK-bilder eller -lager konverteras till RGB innan åtgärden tillämpas.

## Standard {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`, utan att nyansen ändras.
