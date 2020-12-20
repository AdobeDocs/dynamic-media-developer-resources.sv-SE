---
description: Visa bredd. Anger svarsbildens bredd (visningsbild).
seo-description: Visa bredd. Anger svarsbildens bredd (visningsbild).
seo-title: wid
solution: Experience Manager
title: wid
topic: Scene7 Image Serving - Image Rendering API
uuid: b59b936c-abab-4f9d-95ca-0a09743ba0fb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 0%

---


# wid{#wid}

Visa bredd. Anger svarsbildens bredd (visningsbild).

`wid= *`val`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Bildbredd i pixlar (int större än 0), </p></td> 
 </tr> 
</table>

## Standard {#section-830bae0b6bac440098444d7cdcb23e2e}

Om varken `wid=`, `hei=` eller `scale=` anges är svarsbilden den standardvisningsstorlek som anges i FXG-filen.

Rasterformat återges med standardvisningsstorlek (eller inställningen DefaultPix). Klicka på **[!UICONTROL Application Setup]** > **[!UICONTROL Publish Setup]** > **[!UICONTROL Image Server]** och ange värden för bredd och höjd. Mindre storlekar ger bättre prestanda. Du måste spara inställningarna och utföra en bildserverkublicering för att kunna tillämpa en ändring.

Om du använder ett `scale=1`-kommando återges en begäran om rasterformat med den storlek som anges i FXG-filen.

## Exempel {#section-2f72cb2653d54c6aaacf0d97521fb72c}

[!DNL http://server/is/agm/myRootId/myImageId?wid=200]

Om inget format anges återges bilden som en SWF-fil. I det här fallet har höjd och bredd ingen betydelse eftersom SWF-filen vanligtvis utökas till webbläsarfönstrets storlek. Detta innebär att de bara gäller för raster- och PDF-format. Rasterformat:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-alfa
* PNG-alfa

