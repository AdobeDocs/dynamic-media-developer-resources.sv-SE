---
description: Parametern är gemensam för alla visningsprogram.
seo-description: Parametern är gemensam för alla visningsprogram.
seo-title: resurs
solution: Experience Manager
title: resurs
topic: Dynamic media
uuid: 6a72257f-d204-4258-b6f8-de6f7b00fd54
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 0%

---


# resurs{#asset}

Parametern är gemensam för alla visningsprogram.

` asset= *`assetId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> assetId  </span> </span> </p> </td> 
   <td colname="col2"> <p> Resurs-ID för den enskilda videon eller adaptiva videouppsättningen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Den här egenskapen är obligatorisk om inte parametern `video` används. Se [Stöd för extern video](../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3) under Video eller [Stöd för extern video](../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760) under Video360.

eller

` asset= *`image`*`

<table id="table_67E18F42E97C4AAAB0A2F67B7924765D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> image  </span> </span> </p> </td> 
   <td colname="col2"> <p> Anger en enda bild eller en Carousel-uppsättning. Använd dubbel HTTP-kodning för osäkra tecken som finns i bildnamnet eller namnet på Carousel-uppsättningen. </p> </td> 
  </tr> 
 </tbody> 
</table>

eller

` asset= *`imageimageListimageListWithModifiersmultiDimensionalSpinSetmodifiers `* | *``* | *``* | *``* [%3F *``*]`

<table id="table_A2A0ACD942E942BC99AF0DC80FB1C670"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> image  </span> </span> </p> </td> 
   <td colname="col2"> <p> Anger en enda bild. Använd dubbel HTTP-kodning för osäkra tecken som finns i bildnamnet. </p> <p>Eller anger en referens till en bilduppsättning. Visningsprogrammet hämtar bilduppsättningar från servern med hjälp av <span class="codeph"> req=set IS </span>-begäran. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imageList  </span> </span> </p> </td> 
   <td colname="col2"> <p> Anger en explicit bilduppsättning som består av en sorterad objektsekvens, eller bildrutor, avgränsade med kommatecken. </p> <p> <p>Obs!  Den här funktionen stöds i Adobe Scene7 Publishing System; det stöds inte i Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imageListWithModifiers  </span> </span> </p> </td> 
   <td colname="col2"> <p> Anger en explicit bilduppsättning där varje bildruta har sina egna Image Serving-modifierare. I det här fallet är listan med ramar omslutna av parenteser. Kontrollera att du använder dubbel HTTP-kodning för alla kommatecken som finns i den bildrutespecifika Image Serving-modifieraren. </p> <p> <p>Obs!  Den här funktionen stöds i Adobe Scene7 Publishing System; det stöds inte i Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> multiDimensionalSpinSet  </span> </span> </p> </td> 
   <td colname="col2"> <p>Anger en explicit flerdimensionell snurra med följande syntax: </p> <p> <span class="codeph"> ((  <span class="varname"> horizontalSpinSet  </span>)[,(  <span class="varname"> horizontalSpinSet  </span>)])  </span> </p> <p> där <span class="codeph"> <span class="varname"> horizontalSpinSet </span> </span> är en kommaseparerad lista med bildrutor för en given vågrät axel. Alla <span class="codeph"> <span class="varname"> horizontalSpinSet </span> </span> ska ha samma antal bildrutor. </p> <p> <p>Obs!  Den här funktionen stöds i Adobe Scene7 Publishing System; det stöds inte i Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> modifierare  </span> </span> </p> </td> 
   <td colname="col2"> <p> Image Serving, kommandon; Avgränsare för <span class="codeph"> &amp; </span> och <span class="codeph"> = </span> måste vara HTTP-kodade som <span class="codeph"> %26 </span> respektive <span class="codeph"> %3D </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

eller

` asset=( *``* | ( *``*; *``* | *``*; *``* | *``*; *``*); *``*;( *``*; *``* | *``*; *``* | *``*; *``*); *``*;] [%3F *`mediaSetVideoswatchIdimageswatchIdsetIdswatchIdIDvideoswatchIdimageswatchIdsetIdswatchIdIDmodifiers`*]`

<table id="table_D31C8507C02A4452A79DEDDEC62EF2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> mediaSet  </span> </span> </p> </td> 
   <td colname="col2"> <p> Anger en referens till en medieuppsättning. Visningsprogrammet hämtar medieuppsättningar från servern med hjälp av req=set IS-begäran. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> video  </span> </span> </p> </td> 
   <td colname="col2"> <p> En video eller adaptiv videouppsättning. </p> <p> <p>Obs!  Den här funktionen stöds i Adobe Scene7 Publishing System; det stöds inte i Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> image  </span> </span> </p> </td> 
   <td colname="col2"> <p> En bild. </p> <p> <p>Obs!  Den här funktionen stöds i Adobe Scene7 Publishing System; det stöds inte i Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> setId  </span> </span> </p> </td> 
   <td colname="col2"> <p> Färgruteuppsättning. </p> <p> <p>Obs!  Den här funktionen stöds i Adobe Scene7 Publishing System; det stöds inte i Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> swatchId  </span> </span> </p> </td> 
   <td colname="col2"> <p>Färgrutebild. </p> <p> <p>Obs!  Den här funktionen stöds i Adobe Scene7 Publishing System; det stöds inte i Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ID  </span> </span> </p> </td> 
   <td colname="col2"> <p> Identifierare för mediauppsättningens objekttyp kan vara något av följande: </p> <p> 
     <ul id="ul_3100F9356628498DA820C07F6F69CC9B"> 
      <li id="li_51B649A539F14510873CFDA85A6AA714"> <p> <span class="codeph"> advanced_image  </span> </p> <p>För enstaka bilder. </p> </li> 
      <li id="li_7E764D67294647C1A828F949E5ED1908"> <p> <span class="codeph"> advanced_swatchset  </span> </p> <p>För kapslade färgruteuppsättningar. </p> </li> 
      <li id="li_C942CED779B54110BCDC74188995FD5B"> <p> <span class="codeph"> snurra  </span> </p> <p>För snurra. </p> </li> 
      <li id="li_6EA5C54F078D4B24B44F1588BF083842"> <p> <span class="codeph"> video  </span> </p> <p>För enstaka video. </p> </li> 
      <li id="li_8110FA7E0CAB4681A2D8C15F2A656E69"> <p> <span class="codeph"> video_set  </span> </p> <p>För adaptiva videouppsättningar. </p> </li> 
     </ul> </p> <p> <p>Obs!  Den här funktionen stöds i Adobe Scene7 Publishing System; det stöds inte i Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> modifierare  </span> </span> </p> </td> 
   <td colname="col2"> <p> Image Serving, kommandon; Avgränsare för <span class="codeph"> &amp; </span> och <span class="codeph"> = </span> måste vara HTTP-kodade som <span class="codeph"> %26 </span> respektive <span class="codeph"> %3D </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Bilder som använder IR (Image Rendering) eller UGC (User-Generated Content) stöds inte av det här visningsprogrammet.

## Egenskaper {#section-10ee45d637134e0fbcd943c62578cb78}

Obligatoriskt.

## Standard {#section-d411e450028c460392cb8508f8ccc5d9}

Ingen.

## Exempel {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

En tillgångsreferens:

```
asset=Scene7SharedAssets/Backpack_B
```

eller

```
asset=/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg
```

eller

```
asset=/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4
```

eller

```
asset=/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner
```

eller

```
asset=Viewers/space_station_360-AVS
```

En referens till en bilduppsättning som definierats i en katalog:

```
asset=Viewers/Pluralist
```

Explicit bilduppsättning:

```
asset=Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C
```

Explicit bilduppsättning med bildrutespecifika bildservermodifierare:

```
asset=(Scene7SharedAssets/Backpack_B%3Fop_colorize%3D255%252C0%252C0,Scene7SharedAssets/Backpack_B%3Fop_colorize%3D0x00ff00)
```

En referens till en snurrfunktion som definieras i en katalog:

```
asset=Scene7SharedAssets/SpinSet-Sample
```

Explicit rotationsuppsättning:

```
asset=Scene7SharedAssets/Frame-1,Scene7SharedAssets/Frame-2,Scene7SharedAssets/Frame-3,Scene7SharedAssets/Frame-4,Scene7SharedAssets/Frame-5,Scene7SharedAssets/Frame-6,Scene7SharedAssets/Frame-7,Scene7SharedAssets/Frame-8
```

Explicit flerdimensionell rotation:

```
asset=((Scene7SharedAssets/ring1-25,Scene7SharedAssets/ring1-26,Scene7SharedAssets/ring1-27,Scene7SharedAssets/ring1-28,Scene7SharedAssets/ring1-29,Scene7SharedAssets/ring1-30,Scene7SharedAssets/ring1-31,Scene7SharedAssets/ring1-32,Scene7SharedAssets/ring1-33,Scene7SharedAssets/ring1-34,Scene7SharedAssets/ring1-35,Scene7SharedAssets/ring1-36),(Scene7SharedAssets/ring1-13,Scene7SharedAssets/ring1-14,Scene7SharedAssets/ring1-15,Scene7SharedAssets/ring1-16,Scene7SharedAssets/ring1-17,Scene7SharedAssets/ring1-18,Scene7SharedAssets/ring1-19,Scene7SharedAssets/ring1-20,Scene7SharedAssets/ring1-21,Scene7SharedAssets/ring1-22,Scene7SharedAssets/ring1-23,Scene7SharedAssets/ring1-24),(Scene7SharedAssets/ring1-01,Scene7SharedAssets/ring1-02,Scene7SharedAssets/ring1-03,Scene7SharedAssets/ring1-04,Scene7SharedAssets/ring1-05,Scene7SharedAssets/ring1-06,Scene7SharedAssets/ring1-07,Scene7SharedAssets/ring1-08,Scene7SharedAssets/ring1-09,Scene7SharedAssets/ring1-10,Scene7SharedAssets/ring1-11,Scene7SharedAssets/ring1-12))
```

Referens för en blandad medieuppsättning:

```
 asset=Scene7SharedAssets/Mixed_Media_Set_Sample
```

Explicit blandad mediauppsättning:

```
asset=Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;
```

Skärpemodifierare har lagts till i alla bilder i uppsättningen:

```
asset=Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C%3Fop_sharpen=%3D1
```

```
asset=Scene7SharedAssets/Mixed_Media_Set_Sample%3Fop_sharpen%3D1
```

```
asset=Viewers/Pluralist%3Fop_sharpen%3D1
```

