---
title: qlt
description: JPEG-kvalitet. Anger kodningsattribut för JPEG för att styra komprimeringsnivån. Detta varierar i sin tur filstorleken (mängden svarsdata) och, indirekt, den resulterande bildens visuella kvalitet.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8801a650-303c-47a3-8136-c8b2b7a80e9d
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 0%

---

# qlt{#qlt}

JPEG-kvalitet. Anger kodningsattribut för JPEG för att styra komprimeringsnivån. Detta varierar i sin tur filstorleken (mängden svarsdata) och, indirekt, den resulterande bildens visuella kvalitet.

` qlt= *`Kvalitet`*[, *`kroma`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> kvalitet </span> </span> </p> </td> 
  <td class="stentry"> <p>JPEG (1...100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> kroma </span> </span> </p> </td> 
  <td class="stentry"> <p>Nedsampling av färgvärden i JPEG (0=normal, 1=inaktiverad); valfritt, standardvärdet är 0. </p> </td> 
 </tr> 
</table>

Används endast om `fmt=jpg`. I annat fall ignoreras

Högre kvalitetsvärden ökar filstorleken och kvaliteten, lägre värden minskar filstorleken och minskar den upplevda bildkvaliteten. Värden över 90 genererar ofta bilder som inte kan särskiljas från den okomprimerade bilden.

Ange `chroma` flagga för att inaktivera nedsampling av kromaticitet i RGB som används av typiska JPEG-kodare. Detta kan öka den upplevda skärpan på kanterna i en bild när kanten definieras av en nyansändring i stället för intensitet. Om du anger den här flaggan kan filstorleken öka något. Experimentera med den här inställningen om texten ser något suddig ut.

The `chroma` ignoreras om utdatapixeltypen är CMYK eller grå.

## Exempel {#section-a6c263f15c29424a86ef267c96a6630a}

`http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80`
