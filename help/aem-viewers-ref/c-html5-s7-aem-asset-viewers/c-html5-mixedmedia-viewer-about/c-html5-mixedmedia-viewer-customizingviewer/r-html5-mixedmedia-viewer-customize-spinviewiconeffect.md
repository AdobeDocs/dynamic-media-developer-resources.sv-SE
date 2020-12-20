---
description: Rotationsindikatorn visas i rotationsvyområdet. Den visas när bilden är i ett återställningsläge och beror också på parametern iconeffect.
seo-description: Rotationsindikatorn visas i rotationsvyområdet. Den visas när bilden är i ett återställningsläge och beror också på parametern iconeffect.
seo-title: Ikonen Snurra vy, effekt
solution: Experience Manager
title: Ikonen Snurra vy, effekt
topic: Dynamic media
uuid: 33445a3d-51dc-47a4-a8d1-87d25ea001e1
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---


# Ikoneffekt för snurra vy{#spin-view-icon-effect}

Rotationsindikatorn visas i rotationsvyområdet. Den visas när bilden är i ett återställningsläge och beror också på parametern iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-egenskaper för huvudvisningsområdet**

Visningsområdets utseende styrs av följande CSS-klassväljare:

```
.s7mixedmediaviewer .s7spinview .s7iconeffect
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Snurra indikatorteckningar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Rotationsindikatorns bredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Höjd på snurrindikatorn. </p> </td> 
  </tr> 
 </tbody> 
</table>

Rotationsindikatorn har stöd för attributväljaren `state` som är inställd på `spin_1D` vid endimensionell snurra och på `spin_2D` vid flerdimensionell snurra.

Exempel - för att ställa in en zoomindikator på 100 x 100 pixlar.

```
.s7mixedmediaviewer .s7spinview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7mixedmediaviewer .s7spinview .s7iconeffect[state="spin_1D"] { 
background-image: url(images/spinIcon_1D.png); 
} 
.s7mixedmediaviewer .s7spinview .s7iconeffect[state="spin_2D"] { 
background-image: url(images/spinIcon_2D.png); 
}
```

