---
description: Om du klickar eller trycker på den här knappen zoomas en bild ut i huvudvyn. Den här knappen visas inte på mobiltelefoner för att spara skärmutrymme. Du kan ändra storlek, skal och position för knappen med hjälp av CSS.
seo-description: Om du klickar eller trycker på den här knappen zoomas en bild ut i huvudvyn. Den här knappen visas inte på mobiltelefoner för att spara skärmutrymme. Du kan ändra storlek, skal och position för knappen med hjälp av CSS.
seo-title: Knappen Zooma ut
solution: Experience Manager
title: Knappen Zooma ut
topic: Dynamic Media
uuid: edc46e24-d3d9-4d1e-8676-ec441936458d
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---


# Knappen Zooma ut{#zoom-out-button}

Om du klickar eller trycker på den här knappen zoomas en bild ut i huvudvyn. Den här knappen visas inte på mobiltelefoner för att spara skärmutrymme. Du kan ändra storlek, skal och position för knappen med hjälp av CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-egenskaper för huvudvisningsområdet**

Knappens utseende styrs med följande CSS-klassväljare:

```
.s7mixedmediaviewer .s7zoomoutbutton
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
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Placera från den övre kanten, inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> höger  </span> </p> </td> 
   <td colname="col2"> <p>Placera från den högra kanten, inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vänster  </span> </p> </td> 
   <td colname="col2"> <p>Placera från den vänstra kanten, inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nederkant  </span> </p> </td> 
   <td colname="col2"> <p>Placera från den nedre kanten, inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Knappens bredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Knappens höjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Bilden som visas för ett visst knappläge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Den här knappen stöder attributväljaren `state`, som kan användas för att tillämpa olika skal på olika knapplägen.

Knappens funktionsbeskrivning kan lokaliseras. Mer information finns i [Lokalisering av element i användargränssnittet](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

Exempel - för att ställa in en utzoomningsknapp som är 32 x 32 pixlar, placerad sex pixlar från den övre och högra kanten av visningsprogrammet och visa en annan bild för vart och ett av de fyra knapplägena.

```
.s7mixedmediaviewer .s7zoomoutbutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7mixedmediaviewer .s7zoomoutbutton [state='up'] { 
background-image:url(images/v2/ZoomOutButton_dark_up.png); 
} 
.s7mixedmediaviewer .s7zoomoutbutton [state='over'] {  
background-image:url(images/v2/ZoomOutButton_dark_over.png); 
} 
.s7mixedmediaviewer .s7zoomoutbutton [state='down'] {  
background-image:url(images/v2/ZoomOutButton_dark_down.png); 
} 
.s7mixedmediaviewer .s7zoomoutbutton [state='disabled'] { 
background-image:url(images/v2/ZoomOutButton_dark_disabled.png); 
}
```

