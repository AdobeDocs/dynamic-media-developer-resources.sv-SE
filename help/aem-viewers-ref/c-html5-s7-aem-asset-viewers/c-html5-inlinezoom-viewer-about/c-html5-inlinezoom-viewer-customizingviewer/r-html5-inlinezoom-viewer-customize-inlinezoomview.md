---
description: Huvudvyn består av den statiska bilden, den zoomade bilden som visas i den utfällbara vyn ovanför den statiska bilden och det tips som visas ovanpå den statiska bilden.
solution: Experience Manager
title: Utfällbar zoomvy
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Textbunden zoom
role: Developer,User
exl-id: 7b4b5cc9-68ad-4e7a-a2d9-3bbced929145
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%

---

# Utfällbar zoomvy{#flyout-zoom-view}

Huvudvyn består av den statiska bilden, den zoomade bilden som visas i den utfällbara vyn ovanför den statiska bilden och det tips som visas ovanpå den statiska bilden.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-egenskaper för huvudvyn**

Utseendet på huvudvyn styrs med följande CSS-klassväljare:

```
.s7flyoutviewer .s7flyoutzoomview
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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Huvudvyns bakgrundsfärg. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att göra huvudvyn genomskinlig:

```
.s7flyoutviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

**CSS-egenskaper för tipsmeddelandet**

Utseendet på tipsmeddelandet styrs av följande CSS-klassväljare:

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

Det går att konfigurera teckensnittsstil, storlek och lodrät förskjutning via CSS. Den vågräta justeringen hanteras emellertid av visningsprogrammets logik. Det går inte att åsidosätta den via CSS med egenskaperna `left` eller `right`.

<table id="table_DCF6B69A9D8C4DB7A10C4572F7484799"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nederkant  </span> </p> </td> 
   <td colname="col2"> <p>Förskjutning längst ned i huvudvyn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> färg  </span> </p> </td> 
   <td colname="col2"> <p>Textfärg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Teckensnittsnamn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Teckenstorlek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad  </span> </p> </td> 
   <td colname="col2"> <p>Utfyllnad runt meddelandetexten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Bakgrundsfyllningsfärg för meddelandetext. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p>Meddelandetextens kantradie i bakgrunden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacitet  </span> </p> </td> 
   <td colname="col2"> <p>Meddelandetextens bakgrundsopacitet. </p> <p>Använd <span class="codeph">-filter:alpha(opacity-...) ) </span> för Internet Explorer 8 </p> </td> 
  </tr> 
 </tbody> 
</table>

Tipsmeddelandet kan lokaliseras. Mer information finns i [Lokalisering av element i användargränssnittet](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27).

.

Exempel - om du vill ställa in ett halvgenomskinligt tips med vitt Arial 12px-teckensnitt, förskjuts 50 pixlar från huvudvyns nederkant, utfyllnad och en rundad kant:

```
.s7flyoutviewer .s7flyoutzoomview .s7tip { 
bottom: 50px; 
color: #ffffff; 
font-family: Arial; 
font-size: 12px; 
padding-bottom: 10px; 
padding-top: 10px; 
padding-left: 12px; 
padding-right: 12px; 
background-color: #000000; 
border-radius: 4px; 
opacity: 0.5; 
filter: alpha(opacity = 50); 
}
```
