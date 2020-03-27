---
description: Justera nyans. Ändrar nyansen för varje synlig pixel i lagret eller den sammansatta bilden med den angivna mängden.
seo-description: Justera nyans. Ändrar nyansen för varje synlig pixel i lagret eller den sammansatta bilden med den angivna mängden.
seo-title: op_hue
solution: Experience Manager
title: op_hue
topic: Scene7 Image Serving - Image Rendering API
uuid: 23da539e-0192-4dc4-a19b-41aa94a82730
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
