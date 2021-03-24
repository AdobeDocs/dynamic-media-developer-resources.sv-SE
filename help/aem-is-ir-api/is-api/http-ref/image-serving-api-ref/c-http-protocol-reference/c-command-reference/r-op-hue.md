---
description: Justera nyans. Ändrar nyansen för varje synlig pixel i lagret eller den sammansatta bilden med den angivna mängden.
solution: Experience Manager
title: op_hue
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '100'
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

Lager, kommando. Gäller det aktuella lagret eller den sammansatta bilden om `layer=comp`. Ignoreras av effektlager. CMYK-bilder eller -lager konverteras till RGB innan åtgärden tillämpas.

## Standard {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`, utan att nyansen ändras.
