---
description: JPEG-kvalitet. Anger JPEG-kodningsattribut som styr komprimeringsnivån. Detta varierar i sin tur filstorleken (mängden svarsdata) och, indirekt, den resulterande bildens visuella kvalitet.
seo-description: JPEG-kvalitet. Anger JPEG-kodningsattribut som styr komprimeringsnivån. Detta varierar i sin tur filstorleken (mängden svarsdata) och, indirekt, den resulterande bildens visuella kvalitet.
seo-title: qlt
solution: Experience Manager
title: qlt
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 936607c1-20c3-4f76-b970-614b21c47dea
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---


# qlt{#qlt}

JPEG-kvalitet. Anger JPEG-kodningsattribut som styr komprimeringsnivån. Detta varierar i sin tur filstorleken (mängden svarsdata) och, indirekt, den resulterande bildens visuella kvalitet.

` qlt= *``*[, *`kvalitetkroma`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> kvalitet  </span> </span> </p> </td> 
  <td class="stentry"> <p>JPEG-kodningskvalitet (1...100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> kroma  </span> </span> </p> </td> 
  <td class="stentry"> <p>Nedsampling av färgvärden för JPEG (0=normal, 1=inaktiverad); valfritt, standardvärdet är 0. </p> </td> 
 </tr> 
</table>

Används endast om `fmt=jpg`. I annat fall ignoreras

Högre kvalitetsvärden ökar filstorleken och kvaliteten, lägre värden minskar filstorleken och minskar den upplevda bildkvaliteten. Värden över 90 genererar ofta bilder som inte kan särskiljas från den okomprimerade bilden.

Ställ in flaggan `chroma` för att inaktivera nedsampling av RGB-kromaticitet som används av vanliga JPEG-kodare. Detta kan öka den upplevda skärpan på kanterna i en bild när kanten definieras av en nyansändring i stället för intensitet. Om du anger den här flaggan kan filstorleken öka något. Experimentera med den här inställningen om texten ser något suddig ut.

`chroma` ignoreras om utdatapixeltypen är CMYK eller grå.

## Exempel {#section-a6c263f15c29424a86ef267c96a6630a}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80]
