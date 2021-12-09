---
title: Sidvy
description: Huvudvyn består av katalogbilden. Den kan svepas för att komma till en annan sida eller zoomas.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d3368115-15e7-4d9d-a417-a3c82c9a8a64
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Sidvy{#page-view}

Huvudvyn består av katalogbilden. Den kan svepas för att komma till en annan sida eller zoomas.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-egenskaper för huvudvisningsområdet**

Visningsområdets utseende styrs av följande CSS-klassväljare:

```
.s7ecatalogviewer .s7pageview
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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Huvudvyns bakgrundsfärg i hexadecimalt format. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> markör </span> </p> </td> 
   <td colname="col2"> <p>Markör som visas över huvudvyn. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att göra huvudvyn genomskinlig.

```
.s7ecatalogviewer .s7pageview { 
 background-color: transparent; 
}
```

På datorer har komponenten stöd för `cursortype` attributväljare som kan tillämpas på `.s7pageview` och styr typen av markör baserat på komponentens tillstånd och användaråtgärder. Följande `cursortype` värden stöds:

<table id="table_45B83F6CCDE84C36B0E087CA9144BFE6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Värde </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> standard </span> </p> </td> 
   <td colname="col2"> <p>Visas när bilden inte kan zoomas på grund av en liten bildupplösning, komponentinställningar eller båda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin </span> </p> </td> 
   <td colname="col2"> <p>Visas när bilden kan zoomas in. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> återställ </span> </p> </td> 
   <td colname="col2"> <p>Visas när bilden har maximal zoomnivå och kan återställas till ursprungligt läge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> dra </span> </p> </td> 
   <td colname="col2"> <p>Visas när användaren panorerar bilden som är i zoomläge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bild </span> </p> </td> 
   <td colname="col2"> <p>Visas när användaren utför en bildväxling genom vågrät dragning eller snärtning. </p> </td> 
  </tr> 
 </tbody> 
</table>

Den sidavgränsare som visuellt skiljer de vänstra och högra sidorna i det kataloguppslaget styrs med följande CSS-klassväljare:

`.s7ecatalogviewer .s7pageview .s7pagedivider`

<table id="table_77EBC9A77BF14CF4974F8F43C709A207"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Bredden på sidavgränsaren. Ange till <span class="codeph"> 0 </span> px om du vill dölja avgränsaren helt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Bilden som du vill använda som sidavgränsare. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill ha en 40 pixlar bred sidavgränsare med halvgenomskinlig bild.

```
.s7ecatalogviewer .s7pageview .s7pagedivider { 
 width:40px; 
 background-image:url(images/sdk/divider.png); 
}
```

>[!NOTE]
>
>När `frametransition` modifieraren är inställd på `turn` eller `auto` (på stationära datorer) styrs siddelarens utseende av `pageturnstyle` modifierare och `.s7pagedivider` CSS-klassen ignoreras.

Det går att konfigurera visningen av anpassade musmarkörer över huvudvisningsområdet. Den här funktionen styrs med ytterligare attributväljare tillämpade på `.s7ecatalogviewer .s7pageview` CSS-klass:

<table id="table_908164DECF9347A19A9696A23BBDB1A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> standard </span> </p> </td> 
   <td colname="col2"> <p> Normalt visas en pil för en bild som inte kan zoomas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin </span> </p> </td> 
   <td colname="col2"> <p> Visar när en bild kan zoomas in. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> återställ </span> </p> </td> 
   <td colname="col2"> <p>Visar när en bild har zoomats maximalt och kan återställas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> dra </span> </p> </td> 
   <td colname="col2"> <p>Visar när användaren utför dra-åtgärd på inzoomad bild </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bild </span> </p> </td> 
   <td colname="col2"> <p>Visar när användaren byter bild med gest </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - ha olika musmarkörer för varje typ av komponentläge.

```
.s7ecatalogviewer .s7pageview[cursortype="default"] { 
cursor:auto; 
} 
.s7ecatalogviewer .s7pageview[cursortype="zoomin"] { 
cursor:url(images/zoomin_cursor.cur), auto; 
} 
.s7ecatalogviewer .s7pageview[cursortype="reset"] { 
cursor:url(images/zoomout_cursor.cur), auto; 
} 
.s7ecatalogviewer .s7pageview [cursortype="slide"] { 
cursor:url(images/slide_cursor.cur), auto; 
} 
.s7ecatalogviewer .s7pageview[cursortype="drag"] { 
cursor:url(images/drag_cursor.cur), auto; 
}
```
