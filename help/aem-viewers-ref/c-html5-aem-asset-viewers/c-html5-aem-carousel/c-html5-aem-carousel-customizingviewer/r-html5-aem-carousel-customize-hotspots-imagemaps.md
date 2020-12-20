---
description: Visningsprogrammet visar hotspot-ikoner över huvudvyn på platser där hotspot-områden ursprungligen skapades i Dynamic Media av AEM Assets - on-demand.
seo-description: Visningsprogrammet visar hotspot-ikoner över huvudvyn på platser där hotspot-områden ursprungligen skapades i Dynamic Media av AEM Assets - on-demand.
seo-title: Aktiveringspunkter och bildscheman
solution: Experience Manager
title: Aktiveringspunkter och bildscheman
topic: Dynamic media
uuid: de7f4dc7-1a55-49d5-a712-7f178cc49068
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---


# Aktiveringspunkter och bildscheman{#hotspots-and-image-maps}

Visningsprogrammet visar hotspot-ikoner över huvudvyn på platser där hotspot-områden ursprungligen skapades i Dynamic Media av AEM Assets - on-demand.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-egenskaper för huvudvisningsområdet**

Utseendet på hotspot-ikonen styrs med följande CSS-klassväljare:

```
.s7carouselviewer .s7imagemapeffect .s7icon
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
   <td colname="col2"> <p>Ikoner med aktiveringspunkt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p>Placera inuti teckningsspriten, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Aktiveringspunktsikonens bredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Höjd på hotspot-ikon. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - ställ in en ikon med aktiveringspunkten 56 x 56 pixlar som visar olika bilder för de två olika ikonlägena:

```
.s7interactiveimage .s7imagemapeffect .s7icon { 
 background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
 width: 56px; 
 height: 56px; 
} 
.s7interactiveimage .s7imagemapeffect .s7icon:hover { 
 background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```

<!--<a id="section_26D0B8444D1F42D493793FF54968C0B9"></a>-->

**CSS-egenskaper för bildschemaområdet**

Utseendet på bildschemaområdet styrs med följande CSS-klassväljare:

`.s7carouselviewer .s7imagemapeffect .s7region`

<table id="table_DAE7A78AA4A74DC78B2D94F29E8E236B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background  </span> </p> </td> 
   <td colname="col2"> <p>Fyllningsfärg för bildschemaområde. </p> <p>Ange den här färgen i formaten <span class="codeph"> #RRGGBB </span>, <span class="codeph"> RGB(R,G,B) </span> eller <span class="codeph"> RGBA(R,G,B,A) </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Fyllningsfärg för bildschemaområde. </p> <p>Ange den här färgen i formaten <span class="codeph"> #RRGGBB </span>, <span class="codeph"> RGB(R,G,B) </span> eller <span class="codeph"> RGBA(R,G,B,A) </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p> Områdesformat för bildschemat. Ska anges som <span class="codeph"> width </span> <span class="codeph"> solid color </span>, där <span class="codeph"> width </span> uttrycks i pixlar, och <span class="codeph"> color </span> anges som <span class="codeph"> #RGGBB </span>, <span class="codeph"> RGB(R,G,B) &lt;a 11/&gt;, eller <span class="codeph"> RGBA(R,G,B,A) </span>.</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - ställ in ett genomskinligt bildschemaområde med en svart kant på en pixel:

```
.s7carouselviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```

