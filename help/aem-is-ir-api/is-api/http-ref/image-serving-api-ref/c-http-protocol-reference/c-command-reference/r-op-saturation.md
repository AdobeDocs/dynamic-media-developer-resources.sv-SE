---
description: Justera mättnad. Ändrar mättnaden för varje synlig pixel i lagret eller den sammansatta bilden.
seo-description: Justera mättnad. Ändrar mättnaden för varje synlig pixel i lagret eller den sammansatta bilden.
seo-title: op_saturation
solution: Experience Manager
title: op_saturation
topic: Scene7 Image Serving - Image Rendering API
uuid: 5e987841-0c3b-4f68-96b1-fad8757f3402
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '107'
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
