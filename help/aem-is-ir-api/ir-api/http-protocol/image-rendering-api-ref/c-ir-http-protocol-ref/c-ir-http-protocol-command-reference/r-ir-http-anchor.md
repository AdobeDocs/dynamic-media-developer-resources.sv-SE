---
description: Bildankarpunkt (hotspot). Anger texturankarpunkten (hotspot) för den repeterbara texturen eller det dekala materialet.
seo-description: Bildankarpunkt (hotspot). Anger texturankarpunkten (hotspot) för den repeterbara texturen eller det dekala materialet.
seo-title: ankare
solution: Experience Manager
title: ankare
topic: Scene7 Image Serving - Image Rendering API
uuid: 1e695882-f97a-4208-b595-2851b91bdbfe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---


# ankare{#anchor}

Bildankarpunkt (hotspot). Anger texturankarpunkten (hotspot) för den repeterbara texturen eller det dekala materialet.

`anchor= *``*, *`xy`*`

`anchorN= *``*, *`xnyn`*`

<table id="simpletable_1D8E91D8424A424787C4D20C9B040115"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>,  <span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>Pixelförskjutning från källbildens övre vänstra hörn (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> xn</span>,  <span class="varname"> yn</span> </p></td> 
  <td class="stentry"> <p>Normaliserad förskjutning från källbildens mitt (verklig, verklig). </p></td> 
 </tr> 
</table>

En repeterbar textur används på ett vinjetteringsobjekt så att texturankarpunkten ( `anchor=`) finns vid objektets texturstartpunkt.

En dekal bild används på ett vinjetteringsobjekt så att den dekala fästpunkten finns vid objektets dekala utgångspunkt. Du kan justera det dolda läget ytterligare med kommandot `pos=`.

`anchorN=0,0` placerar bildankarpunkten i mitten av källbilden. `anchorN=-0.5,-0.5` eller  `anchor=0,0` finns i det övre vänstra hörnet och  `anchorN=0.5,0.5` finns i det nedre högra hörnet av källbilden.

## Egenskaper {#section-91f929d35cd745ab9e1eeecf45fcedae}

**Materialattribut**. Ignoreras om `align=2`, eller om materialet inte är en repeterbar textur, en skrivbordsunderlägg eller en dekalförinställning.

## Standard {#section-b06d728c2f664c29bacf810eefcbde69}

`catalog::Anchor`, om materialet är baserat på en katalogpost. Annars `anchor=0,0` (bildens övre vänstra hörn) för repeterbara texturer och bakgrundsbilder och `anchorN=0,0` (bildens mitt) för dekorationer.

## Se även {#section-b18bf0b035644ca5aedebbc64373718e}

[katalog::Anchor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-anchor.md#reference-d9b1d49db1fc440686f64b84453297ab) ,  [align=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7)
