---
title: Ikoneffekt
description: Zoomindikatorn placeras över huvudvisningsområdet. Den visas när bilden är i ett återställningsläge och den är också beroende av parametern iconeffect.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: fee22d02-172c-4f82-9b6c-e06db530f400
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---

# Ikoneffekt{#icon-effect}

Zoomindikatorn placeras över huvudvisningsområdet. Den visas när bilden är i ett återställningsläge och den är också beroende av parametern iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Visningsområdets utseende styrs av följande CSS-klassväljare:

```
.s7ecatalogviewer .s7pageview .s7iconeffect
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
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se även <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Zoomindikatorns bredd i pixlar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Zoomindikatorns höjd i pixlar. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ikoneffekten stöder attributväljaren `media-type` som du kan använda för att använda olika ikoneffekter på olika enheter. I synnerhet motsvarar `media-type='standard'` stationära datorer där musindata normalt används och `media-type='multitouch'` motsvarar enheter med pekrörelser.

Exempel - för att ställa in en zoomindikator på 100 x 100 pixlar med olika grafik för stationära datorer och pekenheter.

```
.s7ecatalogviewer .s7pageview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7ecatalogviewer .s7pageview .s7iconeffect[media-type='standard'] { 
 background-image:url(images/v2/IconEffect_zoom.png); 
} 
.s7ecatalogviewer .s7pageview .s7iconeffect[media-type='multitouch'] { 
 background-image:url(images/v2/IconEffect_pinch.png); 
}
```
