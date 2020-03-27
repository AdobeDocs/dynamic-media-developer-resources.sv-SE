---
description: Rotationsindikatorn placeras över huvudvisningsområdet. Den visas när bilden är i ett återställningsläge och beror också på parametern iconeffect.
seo-description: Rotationsindikatorn placeras över huvudvisningsområdet. Den visas när bilden är i ett återställningsläge och beror också på parametern iconeffect.
seo-title: Ikoneffekt
solution: Experience Manager
title: Ikoneffekt
topic: Dynamic media
uuid: ce0524e4-fff4-45b0-8069-d5876802d66f
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Ikoneffekt{#icon-effect}

Rotationsindikatorn placeras över huvudvisningsområdet. Den visas när bilden är i ett återställningsläge och beror också på parametern iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-egenskaper för huvudvisningsområdet**

Visningsområdets utseende styrs av följande CSS-klassväljare:

```
.s7spinviewer .s7spinview .s7iconeffect
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
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Snurra indikatorteckningar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#section-b671c70acf284cb0aea678c2d2e4babc" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Rotationsindikatorns bredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höjd på snurrindikatorn. </p> </td> 
  </tr> 
 </tbody> 
</table>

Rotationsindikatorn har stöd för `state` attributväljaren som är inställd `spin_1D` för endimensionell snurra och för `spin_2D` flerdimensionell snurra.

Exempel - för att ställa in en zoomindikator på 100 x 100 pixlar.

```
.s7spinviewer .s7spinview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7spinviewer .s7spinview .s7iconeffect[state="spin_1D"] { 
background-image: url(images/spinIcon_1D.png); 
} 
.s7spinviewer .s7spinview .s7iconeffect[state="spin_2D"] { 
background-image: url(images/spinIcon_2D.png); 
}
```

