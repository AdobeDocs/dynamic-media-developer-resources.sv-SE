---
description: Justera mättnad. Ändrar mättnaden för varje synlig pixel i lagret eller den sammansatta bilden.
solution: Experience Manager
title: op_saturation
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cd71e27e-6ccc-4ade-9bcf-af8e41bcf381
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---

# op_saturation{#op-saturation}

Justera mättnad. Ändrar mättnaden för varje synlig pixel i lagret eller den sammansatta bilden.

`op_saturation= *`adj`*`

<table id="simpletable_5F118A28FE674B06A16F6F19C56B4594"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Mättnadsjustering (-100..+100 int). </p></td> 
 </tr> 
</table>

`op_saturation=-100` tunnar ut bilden helt.

## Egenskaper {#section-9a3cc9ff060049449554dfa69d92fd53}

Lager, kommando. Gäller det aktuella lagret eller den sammansatta bilden om `layer=comp`. Ignoreras av effektlager.

## Standard {#section-ef0e78f55c8b4d22aee09104dad6410a}

`op_saturation=0`, utan att mättnaden förändras. CMYK-bilder eller -lager konverteras till RGB innan åtgärden tillämpas.

## Exempel {#section-033b272f1b7e4efeb94e841fd8095357}

Ändra ett färgfoto så att det ser ut som&quot;högdager&quot;:

`http://server/myRootId/myImageId?op_saturation=-60&op_brightness=45&op_contrast=-35`
