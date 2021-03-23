---
description: Zoomindikatorn visas i zoomvisningsområdet. Den visas när bilden är i ett återställningsläge och den är också beroende av parametern iconeffect.
seo-description: Zoomindikatorn visas i zoomvisningsområdet. Den visas när bilden är i ett återställningsläge och den är också beroende av parametern iconeffect.
seo-title: Zoomvy, ikon, effekt
solution: Experience Manager
title: Zoomvy, ikon, effekt
uuid: 69a44789-9587-4459-9c75-048773c9e368
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Mixa medieuppsättningar
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---


# Zoomvy, ikon, effekt{#zoom-view-icon-effect}

Zoomindikatorn visas i zoomvisningsområdet. Den visas när bilden är i ett återställningsläge och den är också beroende av parametern iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-egenskaper för huvudvisningsområdet**

Visningsområdets utseende styrs av följande CSS-klassväljare:

```
.s7mixedmediaviewer .s7zoomview .s7iconeffect
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
   <td colname="col2"> <p> Zoomindikatorteckningar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Zoomindikatorns bredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Zoomindikatorns höjd. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ikoneffekten stöder attributväljaren `media-type`, som du kan använda för att använda olika ikoneffekter på olika enheter. `media-type='standard'` motsvarar i synnerhet stationära datorer där musindata normalt används och `media-type='multitouch'` motsvarar enheter med pekrörelser.

Exempel - för att ställa in en zoomindikator på 100 x 100 pixlar med olika grafik för stationära datorer och pekenheter.

```
.s7mixedmediaviewer .s7zoomview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7mixedmediaviewer .s7zoomview .s7iconeffect[media-type='standard'] { 
 background-image:url(images/v2/IconEffect_zoom.png); 
} 
.s7mixedmediaviewer .s7zoomview .s7iconeffect[media-type='multitouch'] { 
 background-image:url(images/v2/IconEffect_pinch.png); 
}
```

