---
description: Visa höjd. Anger svarsbildens höjd.
solution: Experience Manager
title: hei
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dcc9311d-4157-490b-9fc4-47060ddb0e37
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# hei{#hei}

Visa höjd. Anger svarsbildens höjd.

`hei= *`val`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Bildhöjd i pixlar (int större än 0). </p></td> 
 </tr> 
</table>

Rasterformat återges med standardvisningsstorlek (eller inställningen DefaultPix). Klicka **[!UICONTROL Application Setup]** > **[!UICONTROL Publish Setup]** > **[!UICONTROL Image Server]** anger du sedan värdena för Bredd och Höjd. Mindre storlekar ger bättre prestanda. Du måste spara inställningarna och utföra en bildserverkublicering för att kunna tillämpa en ändring.

Om du använder en `scale=1` -kommandot återges en begäran om rasterformat med den storlek som anges i FXG-filen.

## Standard {#section-76ee3daa77cb468ab310821357cc9404}

Om ingen `wid=`, `hei=`, eller `scale=` anges är svarsbilden den standardvisningsstorlek som anges i FXG-filen.

## Exempel {#section-a91c14d31e71481ba054412d9f642885}

[!DNL http://server/is/agm/myRootId/myImageId?hei=200]

Om inget format anges återges bilden som en SWF-fil. I det här fallet har höjd och bredd ingen betydelse eftersom SWF vanligtvis utvidgas till webbläsarfönstrets storlek. Detta innebär att hei och wid endast gäller för raster- och PDF-format. Rasterformat:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alfa
* TIF-alfa
* PNG-alfa
