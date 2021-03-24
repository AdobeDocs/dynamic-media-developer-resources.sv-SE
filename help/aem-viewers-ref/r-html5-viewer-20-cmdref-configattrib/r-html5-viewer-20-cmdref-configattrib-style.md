---
description: style
solution: Experience Manager
title: style
feature: Dynamic Media Classic,visningsprogram,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---


# style{#style}

Du kan använda följande kommando både från frågesträngen för URL och från config. Kommandot som används i URL-frågesträngen har alltid företräde framför det kommando som finns i config.

`style= *`cssPath`*`

<table id="table_F800F787CF0342749B934DAEB600C0EB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> cssPath</span> </span> </p> </td> 
   <td colname="col2"> <p> Relativ eller absolut CSS-plats. </p> <p>Anger platsen för den anpassade CSS-filen. Om <span class="codeph"><span class="varname"> cssPath</span></span> är relativ tolkas den mot visningsprogrammets HTML-sidplats och värdet för parametern <span class="codeph"> contentUrl=</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Alla resursreferenser i CSS-filen tolkas mot CSS-filplatsen, inte mot platsen för den anropande HTML-sidan.

## Egenskaper {#section-8ce2a4493d454d97a9975fc7f9f4eb2c}

Valfritt.

## Standard {#section-79a827f7a3bb4f36b3d72c309155059e}

Ingen.

## Exempel {#section-f8a0c032979047a38041abfce3f7a70b}

`style=/skins/customStyle.css`

`style=etc/dam/presets/css/html5_interactiveimage.css`

`style=etc/dam/presets/css/html5_interactivevideo.css`

`style=etc/dam/presets/css/html5_carouselviewer_dotted_light.css`
