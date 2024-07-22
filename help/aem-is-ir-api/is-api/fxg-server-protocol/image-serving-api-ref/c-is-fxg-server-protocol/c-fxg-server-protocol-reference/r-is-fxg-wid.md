---
title: wid
description: Visa bredd. Anger svarsbildens bredd (visningsbild).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5edd045c-600e-4295-9672-04a5c3bc651d
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---

# wid{#wid}

Visa bredd. Anger svarsbildens bredd (visningsbild).

`wid= *`val`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val </span></span> </p> </td> 
  <td class="stentry"> <p>Bildbredd i pixlar (int större än 0), </p></td> 
 </tr> 
</table>

## Standard {#section-830bae0b6bac440098444d7cdcb23e2e}

Om varken `wid=`, `hei=` eller `scale=` anges är svarsbilden den standardvisningsstorlek som anges i FXG-filen.

Rasterformat återges med standardvisningsstorlek (eller inställningen DefaultPix). Klicka på **[!UICONTROL Application Setup]** > **[!UICONTROL Publish Setup]** > **[!UICONTROL Image Server]** och ange värden för bredd och höjd. Mindre storlekar ger bättre prestanda. Spara inställningarna och utför en Image Serving Publish för att göra en ändring.

Om du använder ett `scale=1`-kommando återges en rasterformatbegäran med den storlek som anges i FXG-filen.

## Exempel {#section-2f72cb2653d54c6aaacf0d97521fb72c}

`http://server/is/agm/myRootId/myImageId?wid=200`

Om inget format anges återges bilden som en SWF-fil. I det här fallet har höjd och bredd ingen betydelse eftersom SWF vanligtvis utvidgas till webbläsarfönstrets storlek. Därför gäller `hei` och `wid` bara för raster- och PDF-format. Rasterformat:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alfa
* TIF-alfa
* PNG-alfa
