---
title: hei
description: Visa höjd. Anger svarsbildens höjd.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dcc9311d-4157-490b-9fc4-47060ddb0e37
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '164'
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

Rasterformat återges med standardvisningsstorlek (eller inställningen DefaultPix). Välj **[!UICONTROL Application Setup]** > **[!UICONTROL Publish Setup]** > **[!UICONTROL Image Server]** anger du sedan värden för bredd och höjd. Mindre storlekar ger bättre prestanda. Spara inställningarna och utför en bildserverkublicering för att tillämpa en ändring.

Om du använder en `scale=1` -kommandot återges en begäran om rasterformat med den storlek som anges i FXG-filen.

## Standard {#section-76ee3daa77cb468ab310821357cc9404}

If `wid=`, `hei=`, eller `scale=` Om inget anges är svarsbilden den standardvisningsstorlek som anges i FXG-filen.

## Exempel {#section-a91c14d31e71481ba054412d9f642885}

[!DNL `http://server/is/agm/myRootId/myImageId?hei=200`]

Om inget format anges återges bilden som en SWF-fil. I det här fallet har höjd och bredd ingen betydelse eftersom SWF vanligtvis utvidgas till webbläsarfönstrets storlek. Detta innebär att hei och wid endast gäller för raster- och PDF-format. Rasterformat:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alfa
* TIF-alfa
* PNG-alfa
