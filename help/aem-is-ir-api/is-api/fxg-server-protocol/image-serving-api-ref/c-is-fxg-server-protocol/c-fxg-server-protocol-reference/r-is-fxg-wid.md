---
description: Visa bredd. Anger svarsbildens bredd (visningsbild).
solution: Experience Manager
title: wid
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5edd045c-600e-4295-9672-04a5c3bc651d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '170'
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

Om ingen `wid=`, `hei=`, eller `scale=` anges är svarsbilden den standardvisningsstorlek som anges i FXG-filen.

Rasterformat återges med standardvisningsstorlek (eller inställningen DefaultPix). Klicka **[!UICONTROL Application Setup]** > **[!UICONTROL Publish Setup]** > **[!UICONTROL Image Server]** anger du sedan värdena för Bredd och Höjd. Mindre storlekar ger bättre prestanda. Du måste spara inställningarna och utföra en bildserverkublicering för att kunna tillämpa en ändring.

Om du använder en `scale=1` -kommandot återges en begäran om rasterformat med den storlek som anges i FXG-filen.

## Exempel {#section-2f72cb2653d54c6aaacf0d97521fb72c}

[!DNL http://server/is/agm/myRootId/myImageId?wid=200]

Om inget format anges återges bilden som en SWF-fil. I det här fallet har höjd och bredd ingen betydelse eftersom SWF vanligtvis utvidgas till webbläsarfönstrets storlek. Detta innebär att hei och wid endast gäller för raster- och PDF-format. Rasterformat:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alfa
* TIF-alfa
* PNG-alfa
