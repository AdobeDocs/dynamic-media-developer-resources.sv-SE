---
title: Ikoneffekt
description: Zoomindikatorn placeras över huvudvisningsområdet. Den visas när bilden är i ett återställningsläge och den är också beroende av parametern iconeffect.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 45ab21e0-1f9e-48c9-8a8f-7a54e273db30
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# Ikoneffekt{#icon-effect}

Zoomindikatorn placeras över huvudvisningsområdet. Den visas när bilden är i ett återställningsläge och den är också beroende av parametern iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-egenskaper för huvudvisningsområdet**

Visningsområdets utseende styrs av följande CSS-klassväljare:

```
.s7basiczoomviewer .s7zoomview .s7iconeffect
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
   <td colname="col2"> <p> Zoomindikatorteckningar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-customizingviewer/c-html5-20-basic-zoom-viewer-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Zoomindikatorns bredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Zoomindikatorns höjd. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ikoneffekt har stöd för `media-type` attributväljare, som du kan använda för att använda olika ikoneffekter på olika enheter. I synnerhet `media-type='standard'` motsvarar stationära datorer där musindata normalt används och `media-type='multitouch'` motsvarar enheter med pekrörelser.

Exempel - för att ställa in en zoomindikator på 100 x 100 pixlar med olika grafik för stationära datorer och pekenheter.

```
.s7basiczoomviewer .s7zoomview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7basiczoomviewer .s7zoomview .s7iconeffect[media-type='standard'] { 
 background-image:url(images/v2/IconEffect_zoom.png); 
} 
.s7basiczoomviewer .s7zoomview .s7iconeffect[media-type='multitouch'] { 
 background-image:url(images/v2/IconEffect_pinch.png); 
}
```
